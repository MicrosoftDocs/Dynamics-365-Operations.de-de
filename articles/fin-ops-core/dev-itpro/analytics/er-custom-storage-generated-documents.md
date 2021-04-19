---
title: Angeben eines benutzerdefinierten Speicherorts für generierte Dokumente
description: In diesem Thema wird erläutert, wie Sie die Liste der Speicherorte für Dokumente erweitern, die von Formaten der electronischen Berichterstellung (ER) generiert werden.
author: NickSelin
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
ms.openlocfilehash: dab70b213efc7e7a3537aa2b47b9edf38d492d34
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753719"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="2afe2-103">Angeben eines benutzerdefinierten Speicherorts für generierte Dokumente</span><span class="sxs-lookup"><span data-stu-id="2afe2-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2afe2-104">Mit der Anwendungsprogrammierschnittstelle (API) des Framework der elektronischen Berichterstellung (ER) können Sie die Liste der Speicherorte für Dokumente, die von ER-Formaten generiert werden, erweitern.</span><span class="sxs-lookup"><span data-stu-id="2afe2-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="2afe2-105">Dieses Thema enthält einen Überblick über die Hauptaufgaben, die Sie erledigen müssen, um einen benutzerdefinierten Speicherort hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2afe2-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2afe2-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2afe2-106">Prerequisites</span></span>

<span data-ttu-id="2afe2-107">Sie müssen eine Topologie bereitstellen, die einen fortlaufenden Build unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2afe2-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="2afe2-108">(Weitere Informationen finden Sie unter [Bereitstellen von Topologien, die fortlaufenden Build und Testautomatisierung unterstützen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Für eine der folgenden Rollen benötigen Sie Zugriff auf diese Topologie:</span><span class="sxs-lookup"><span data-stu-id="2afe2-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="2afe2-109">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2afe2-109">Electronic reporting developer</span></span>
- <span data-ttu-id="2afe2-110">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2afe2-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="2afe2-111">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="2afe2-111">System administrator</span></span>

<span data-ttu-id="2afe2-112">Sie müssen zudem Zugriff auf die Entwicklungsumgebung für diese Topologie haben.</span><span class="sxs-lookup"><span data-stu-id="2afe2-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="2afe2-113">Erstellen oder Importieren einer ER-Formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2afe2-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="2afe2-114">In der aktuellen Topologie [erstellen Sie ein neues ER-Format](tasks/er-format-configuration-2016-11.md), um Dokumente zu generieren, für die Sie einen benutzerdefinierten Speicherort hinzuzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="2afe2-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="2afe2-115">Alternativ [importieren Sie ein vorhandenes ER-Format in diese Topologie](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="2afe2-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Formatdesignerseite](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="2afe2-117">Das ER-Format, das Sie erstellen oder importieren, muss mindestens eines der folgenden Formatelemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="2afe2-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="2afe2-118">Datei</span><span class="sxs-lookup"><span data-stu-id="2afe2-118">File</span></span>
> - <span data-ttu-id="2afe2-119">Ordner</span><span class="sxs-lookup"><span data-stu-id="2afe2-119">Folder</span></span>
> - <span data-ttu-id="2afe2-120">Merge-Programm</span><span class="sxs-lookup"><span data-stu-id="2afe2-120">Merger</span></span>
> - <span data-ttu-id="2afe2-121">Anhang</span><span class="sxs-lookup"><span data-stu-id="2afe2-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="2afe2-122">Erstellen eines neuen Dokumenttyps</span><span class="sxs-lookup"><span data-stu-id="2afe2-122">Create a new document type</span></span>

<span data-ttu-id="2afe2-123">Um festzulegen, wie Dokumente, die von einem ER-Format erzeugt werden, weitergeleitet werden, müssen Sie [Elektronische Berichtsziele (ER)](electronic-reporting-destinations.md) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2afe2-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="2afe2-124">In jedem ER-Ziel, das konfiguriert wird, um generierten Dokumente als Dateien zu speichern, müssen Sie einen Dokumenttyp des Dokumentverwaltungsframework angeben.</span><span class="sxs-lookup"><span data-stu-id="2afe2-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="2afe2-125">Verschiedene Dokumenttypen können verwendet werden, um Dokumente weiterzuleiten, die von verschiedenen ER-Formaten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="2afe2-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="2afe2-126">Fügen Sie einen neuen [Dokumenttyp](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) für das ER-Format hinzu, das Sie bereits erstellt oder importiert haben.</span><span class="sxs-lookup"><span data-stu-id="2afe2-126">Add a new [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="2afe2-127">In der folgenden Abbildung lautet der Dokumenttyp **FileX**.</span><span class="sxs-lookup"><span data-stu-id="2afe2-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="2afe2-128">Um dieses Dokumenttyp von anderen Dokumenttypen zu unterscheiden, schließen Sie ein bestimmtes Schlüsselwort in seinem Namen ein.</span><span class="sxs-lookup"><span data-stu-id="2afe2-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="2afe2-129">Beispielsweise lautet der Name in der folgenden Abbildung **(LOKALER) Ordner**.</span><span class="sxs-lookup"><span data-stu-id="2afe2-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="2afe2-130">Geben Sie im Feld **Klasse** die Option **Datei zuordnen** an.</span><span class="sxs-lookup"><span data-stu-id="2afe2-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="2afe2-131">Geben Sie im Feld **Gruppe** die Option **Datei** an.</span><span class="sxs-lookup"><span data-stu-id="2afe2-131">In the **Group** field, specify **File**.</span></span>

![Seite „Dokumenttypen”](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="2afe2-133">Dokumenttypen sind unternehmensspezifisch</span><span class="sxs-lookup"><span data-stu-id="2afe2-133">Document types are company-specific.</span></span> <span data-ttu-id="2afe2-134">Zur Verwendung eines ER-Formats mit einem konfigurierten Ziel in mehreren Unternehmen müssen Sie einen separaten Dokumenttyp für jedes Unternehmen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2afe2-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="2afe2-135">Quellcode überprüfen</span><span class="sxs-lookup"><span data-stu-id="2afe2-135">Review source code</span></span>

<span data-ttu-id="2afe2-136">Überprüfen Sie den Code der **insertFile()**-Methode der Klasse **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="2afe2-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="2afe2-137">Beachten Sie, dass das Ereignis **AttachingFile()** ausgelöst wird, während die generierte Datei an einen Datensatz angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="2afe2-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>


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

<span data-ttu-id="2afe2-138">Das Ereignis **AttachingFile()** wird ausgelöst, wenn die folgenden ER-Ziele verarbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="2afe2-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="2afe2-139">**Archiv** – Wenn das Ziel verwendet wird, wird ein neuer Datensatz für das ER-Format, das ausgeführt wird, in der ERFormatMappingRunJobTable-Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="2afe2-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="2afe2-140">Das Feld **Archiviert** in diesem Datensatz wird auf **Falsch** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2afe2-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="2afe2-141">Wenn das ER-Format erfolgreich ausgeführt wird, wird das generierte Dokument an diesen Datensatz angefügt, und das Ereignis **AttachingFile()** wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="2afe2-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="2afe2-142">Der Dokumenttyp, der in diesem ER-Ziel ausgewählt wird, bestimmt den Speicherort für die angefügte Datei (Microsoft Azure-Speicher oder ein Microsoft SharePoint-Ordner).</span><span class="sxs-lookup"><span data-stu-id="2afe2-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="2afe2-143">**Einzelvorgangsarchiv** – Wenn dieses Ziel verwendet wird, wird ein neuer Datensatz für das ER-Formular, das ausgeführt wird, in der ERFormatMappingRunJobTable-Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="2afe2-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="2afe2-144">Das Feld **Archiviert** in diesem Datensatz wird auf **Wahr** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2afe2-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="2afe2-145">Wenn das ER-Format erfolgreich ausgeführt wird, wird das generierte Dokument an diesen Datensatz angefügt, und das Ereignis **AttachingFile()** wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="2afe2-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="2afe2-146">Der Dokumenttyp, der in den ER-Parametern konfiguriert wird, bestimmt den Speicherort für die angefügte Datei (Azure-Speicher oder ein SharePoint-Ordner).</span><span class="sxs-lookup"><span data-stu-id="2afe2-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Parameterseite der elektronischen Berichterstellung](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="2afe2-148">Das Ziel einer elektronischen Berichterstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2afe2-148">Configure an ER destination</span></span>

1. <span data-ttu-id="2afe2-149">Konfigurieren Sie das archivierte Ziel für eines der zuvor genannten Elemente (Datei, Ordner, Merger-Programm oder Anhang) des ER-Formats, das von Ihnen erstelltoder importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2afe2-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="2afe2-150">Eine Anleitung finden Sie unter [ER-Konfigurationsziele](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="2afe2-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="2afe2-151">Verwenden Sie den Dokumenttyp, den Sie zuvor für das konfigurierte Ziel hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="2afe2-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="2afe2-152">(Im Beispiel in diesem Thema lautet der Dokumenttyp **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="2afe2-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialogfeld" Zieleinstellungen"](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="2afe2-154">Quellcode ändern</span><span class="sxs-lookup"><span data-stu-id="2afe2-154">Modify source code</span></span>

1. <span data-ttu-id="2afe2-155">Fügen Sie Ihrem Microsoft Visual Studio-Projekt eine neue Klasse hinzu, und schreiben Sie Code, um das **AttachingFile()**-Ereignis zu abonnieren, das zuvor erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="2afe2-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="2afe2-156">(Weitere Informationen zum Erweiterbarkeitsmuster, das verwendet wird, finden Sie unter [Reaktion unter Verwendung von EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)) Beispiel: In der neuen Klasse schreiben Sie Code, der die folgenden Aktionen ausführt:</span><span class="sxs-lookup"><span data-stu-id="2afe2-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="2afe2-157">Generierte Dateien in einem Ordner des lokalen Dateisystems des Servers speichern, auf dem Application Object Server (AOS) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2afe2-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="2afe2-158">Speichern Sie diese generierten Dateien nur, wenn der neuen Dokumenttyp (beispielsweise der Typ **FileX** mit "(LOKALE)-Schlüsselwort im Namen) verwendet wird, während eine Datei an den Datensatz im ER-AusführungsJobprotokoll angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="2afe2-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

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

2. <span data-ttu-id="2afe2-159">Ihr Projekt neu erstellen</span><span class="sxs-lookup"><span data-stu-id="2afe2-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="2afe2-160">Ausführen des erstellten oder importierten ER-Formats</span><span class="sxs-lookup"><span data-stu-id="2afe2-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="2afe2-161">Führen Sie das ER-Format aus, das von Ihnen erstellt oder importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2afe2-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="2afe2-162">Wechseln Sie zu **Organisationsverwaltung \>Elektronische Berichterstellung \> Einzelvorgänge für elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="2afe2-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="2afe2-163">Suchen Sie den Datensatz, der für diesen Ausführungseinzelvorgang erstellt wurde, und dem die generierte Datei angehängt wurde.</span><span class="sxs-lookup"><span data-stu-id="2afe2-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="2afe2-164">Untersuchen Sie den lokalen **C:\\0**-Ordner, um dieselbe generierte Datei zu finden.</span><span class="sxs-lookup"><span data-stu-id="2afe2-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2afe2-165">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2afe2-165">Additional resources</span></span>

- [<span data-ttu-id="2afe2-166">Ziele für elektronische Berichterstellung (EB)</span><span class="sxs-lookup"><span data-stu-id="2afe2-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="2afe2-167">Startseite für Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="2afe2-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]