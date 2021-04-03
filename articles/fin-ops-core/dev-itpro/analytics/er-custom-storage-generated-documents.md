---
title: Angeben eines benutzerdefinierten Speicherorts für generierte Dokumente
description: In diesem Thema wird erläutert, wie Sie die Liste der Speicherorte für Dokumente erweitern, die von Formaten der electronischen Berichterstellung (ER) generiert werden.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: b71ad5a9701922eb94b1d611e2d3f6a945ce6c06
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562237"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Angeben eines benutzerdefinierten Speicherorts für generierte Dokumente

[!include[banner](../includes/banner.md)]

Mit der Anwendungsprogrammierschnittstelle (API) des Framework der elektronischen Berichterstellung (ER) können Sie die Liste der Speicherorte für Dokumente, die von ER-Formaten generiert werden, erweitern. Dieses Thema enthält einen Überblick über die Hauptaufgaben, die Sie erledigen müssen, um einen benutzerdefinierten Speicherort hinzuzufügen.

## <a name="prerequisites"></a>Voraussetzungen

Sie müssen eine Topologie bereitstellen, die einen fortlaufenden Build unterstützt. (Weitere Informationen finden Sie unter [Bereitstellen von Topologien, die fortlaufenden Build und Testautomatisierung unterstützen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Für eine der folgenden Rollen benötigen Sie Zugriff auf diese Topologie:

- Entwickler für elektronische Berichterstellung
- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

Sie müssen zudem Zugriff auf die Entwicklungsumgebung für diese Topologie haben.

## <a name="create-or-import-an-er-format-configuration"></a>Erstellen oder Importieren einer ER-Formatkonfiguration

In der aktuellen Topologie [erstellen Sie ein neues ER-Format](tasks/er-format-configuration-2016-11.md), um Dokumente zu generieren, für die Sie einen benutzerdefinierten Speicherort hinzuzufügen möchten. Alternativ [importieren Sie ein vorhandenes ER-Format in diese Topologie](general-electronic-reporting-manage-configuration-lifecycle.md).

![Formatdesignerseite](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Das ER-Format, das Sie erstellen oder importieren, muss mindestens eines der folgenden Formatelemente enthalten:
>
> - Datei
> - Ordner
> - Merge-Programm
> - Anhang

## <a name="create-a-new-document-type"></a>Erstellen eines neuen Dokumenttyps

Um festzulegen, wie Dokumente, die von einem ER-Format erzeugt werden, weitergeleitet werden, müssen Sie [Elektronische Berichtsziele (ER)](electronic-reporting-destinations.md) konfigurieren. In jedem ER-Ziel, das konfiguriert wird, um generierten Dokumente als Dateien zu speichern, müssen Sie einen Dokumenttyp des Dokumentverwaltungsframework angeben. Verschiedene Dokumenttypen können verwendet werden, um Dokumente weiterzuleiten, die von verschiedenen ER-Formaten generiert werden.

1. Fügen Sie einen neuen [Dokumenttyp](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) für das ER-Format hinzu, das Sie bereits erstellt oder importiert haben. In der folgenden Abbildung lautet der Dokumenttyp **FileX**.
2. Um dieses Dokumenttyp von anderen Dokumenttypen zu unterscheiden, schließen Sie ein bestimmtes Schlüsselwort in seinem Namen ein. Beispielsweise lautet der Name in der folgenden Abbildung **(LOKALER) Ordner**.
3. Geben Sie im Feld **Klasse** die Option **Datei zuordnen** an.
4. Geben Sie im Feld **Gruppe** die Option **Datei** an.

![Seite „Dokumenttypen”](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Dokumenttypen sind unternehmensspezifisch Zur Verwendung eines ER-Formats mit einem konfigurierten Ziel in mehreren Unternehmen müssen Sie einen separaten Dokumenttyp für jedes Unternehmen konfigurieren.

## <a name="review-source-code"></a>Quellcode überprüfen

Überprüfen Sie den Code der **insertFile()**-Methode der Klasse **ERDocuManagement**. Beachten Sie, dass das Ereignis **AttachingFile()** ausgelöst wird, während die generierte Datei an einen Datensatz angefügt wurde.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

Das Ereignis **AttachingFile()** wird ausgelöst, wenn die folgenden ER-Ziele verarbeitet werden:

- **Archiv** – Wenn das Ziel verwendet wird, wird ein neuer Datensatz für das ER-Format, das ausgeführt wird, in der ERFormatMappingRunJobTable-Tabelle erstellt. Das Feld **Archiviert** in diesem Datensatz wird auf **Falsch** festgelegt. Wenn das ER-Format erfolgreich ausgeführt wird, wird das generierte Dokument an diesen Datensatz angefügt, und das Ereignis **AttachingFile()** wird verwendet. Der Dokumenttyp, der in diesem ER-Ziel ausgewählt wird, bestimmt den Speicherort für die angefügte Datei (Microsoft Azure-Speicher oder ein Microsoft SharePoint-Ordner).
- **Einzelvorgangsarchiv** – Wenn dieses Ziel verwendet wird, wird ein neuer Datensatz für das ER-Formular, das ausgeführt wird, in der ERFormatMappingRunJobTable-Tabelle erstellt. Das Feld **Archiviert** in diesem Datensatz wird auf **Wahr** festgelegt. Wenn das ER-Format erfolgreich ausgeführt wird, wird das generierte Dokument an diesen Datensatz angefügt, und das Ereignis **AttachingFile()** wird verwendet. Der Dokumenttyp, der in den ER-Parametern konfiguriert wird, bestimmt den Speicherort für die angefügte Datei (Azure-Speicher oder ein SharePoint-Ordner).

![Parameterseite der elektronischen Berichterstellung](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Das Ziel einer elektronischen Berichterstellung konfigurieren

1. Konfigurieren Sie das archivierte Ziel für eines der zuvor genannten Elemente (Datei, Ordner, Merger-Programm oder Anhang) des ER-Formats, das von Ihnen erstelltoder importiert wurde. Eine Anleitung finden Sie unter [ER-Konfigurationsziele](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Verwenden Sie den Dokumenttyp, den Sie zuvor für das konfigurierte Ziel hinzugefügt haben. (Im Beispiel in diesem Thema lautet der Dokumenttyp **FileX**.)

![Dialogfeld" Zieleinstellungen"](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Quellcode ändern

1. Fügen Sie Ihrem Microsoft Visual Studio-Projekt eine neue Klasse hinzu, und schreiben Sie Code, um das **AttachingFile()**-Ereignis zu abonnieren, das zuvor erwähnt wurde. (Weitere Informationen zum Erweiterbarkeitsmuster, das verwendet wird, finden Sie unter [Reaktion unter Verwendung von EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)) Beispiel: In der neuen Klasse schreiben Sie Code, der die folgenden Aktionen ausführt:

    1. Generierte Dateien in einem Ordner des lokalen Dateisystems des Servers speichern, auf dem Application Object Server (AOS) ausgeführt wird.
    2. Speichern Sie diese generierten Dateien nur, wenn der neuen Dokumenttyp (beispielsweise der Typ **FileX** mit "(LOKALE)-Schlüsselwort im Namen) verwendet wird, während eine Datei an den Datensatz im ER-AusführungsJobprotokoll angefügt ist.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Ihr Projekt neu erstellen

## <a name="run-the-er-format-that-you-created-or-imported"></a>Ausführen des erstellten oder importierten ER-Formats

1. Führen Sie das ER-Format aus, das von Ihnen erstellt oder importiert wurde.
2. Wechseln Sie zu **Organisationsverwaltung \>Elektronische Berichterstellung \> Einzelvorgänge für elektronische Berichterstellung**. Suchen Sie den Datensatz, der für diesen Ausführungseinzelvorgang erstellt wurde, und dem die generierte Datei angehängt wurde.
3. Untersuchen Sie den lokalen **C:\\0**-Ordner, um dieselbe generierte Datei zu finden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Ziele für elektronische Berichterstellung (EB)](electronic-reporting-destinations.md)
- [Startseite für Erweiterbarkeit](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]