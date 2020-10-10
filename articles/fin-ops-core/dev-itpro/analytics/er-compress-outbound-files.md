---
title: Komprimieren großer Dokumente, die in der elektronischen Berichterstellung generiert werden
description: In diesem Thema wird erläutert, wie Sie große Dokumente komprimieren, die von einem Format für die elektronische Berichterstellung (EB) generiert werden.
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ef024185c4654804f6f260a43c1bf294b33c10e2
ms.sourcegitcommit: 6e290b0d3aeedd0e234ac4f1df92b1b9afd6fccc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829678"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Komprimieren großer Dokumente, die in der elektronischen Berichterstellung generiert werden 

[!include [banner](../includes/banner.md)]

Sie können das [Framework für die elektronische Berichterstellung (EB)](general-electronic-reporting.md) verwenden, um eine Lösung zu konfigurieren, die Transaktionsdaten abruft, um ein ausgehendes Dokument zu generieren. Dieses generierte Dokument ist möglicherweise sehr groß. Wenn dieser Dokumenttyp generiert wird, wird der Speicher des [Anwendungsobjektservers (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) zur Speicherung verwendet. Irgendwann muss das Dokument dann aus Ihrer Microsoft Dynamics 365 Finance-Anwendung heruntergeladen werden. Derzeit ist die maximale Größe eines einzelnen Dokuments, das in EB generiert werden kann, auf 2 Gigabyte (GB) begrenzt. Des Weiteren [begrenzt](https://fix.lcs.dynamics.com/Issue/Details?bugId=489291) Finance die Größe einer heruntergeladenene Datei derzeit auf 1 GB. Daher müssen Sie eine EB-Lösung konfigurieren, die die Wahrscheinlichkeit verringert, dass diese Einschränkungen überschritten werden und Sie eine Ausnahme **Stream war zu lang** oder **Überlauf oder Unterlauf in der Rechenoperation** erhalten.

Wenn Sie eine Lösung konfigurieren, können Sie Ihr EB-Format im Vorgangs-Designer anpassen, indem Sie ein Stammelement vom Typ **Ordner** hinzufügen, um den Inhalt zu komprimieren, der von einem der verschachtelten Elemente generiert wird. Die Komprimierung arbeitet „just in time“, sodass die maximale Speichernutzung und die Größe der herunterzuladenden Datei verringert werden können.

> [!NOTE]
> Die Komprimierung nimmt einen zusätzlichen Prozentsatz der CPU-Auslastung in Anspruch.

Weitere Informationen zu diesem Ansatz erhalten Sie, wenn Sie das Beispiel in diesem Thema abschließen.

## <a name="example-compress-an-outbound-document"></a>Beispiel: Komprimieren eines ausgehenden Dokuments

Dieses Beispiel zeigt, wie ein Benutzer, dem die Rolle **Systemadministrator** oder **Funktionaler Berater für elektronische Berichterstellung** zugewiesen ist, ein EB-Format konfigurieren kann, um ein generiertes Dokument zu komprimieren.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Prozeduren in diesem Thema abschließen können, müssen die folgenden Schritte abgeschlossen werden.

1. [Aktivieren eines Konfigurationsanbieters](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Importieren Sie die EB-Beispielkonfigurationen](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Überprüfen Sie das importierte Format](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Derzeit beginnt die Formatstruktur mit dem Element **Bericht** vom Typ **Datei** und enthält XML-Elemente. Daher wird ein ausgehendes Dokument im XML-Format generiert und es wird keine Komprimierung verwendet.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Generieren Sie ein EB-Format, um ein unkomprimiertes Dokument zu erhalten

1. [Führen Sie das importierte Format aus](er-defer-xml-element.md#run-the-imported-format).
2. Beachten Sie, dass die Größe des generierten Dokuments im XML-Format 3 Kilobyte (KB) beträgt.

    ![Vorschau des unkomprimierten ausgehenden Dokuments](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Ändern des Formats, um die generierte Ausgabe zu komprimieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** die Konfigurationsstruktur für **Modell zum Erlernen verzögerter Elemente**.
3. Wähle Sie die Konfiguration **Format zum Verstehen verzögerter XML-Elemente** aus.
4. Wählen Sie **Designer** aus, um die Formatstruktur zu ändern.
5. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Format** die Option **Stamm hinzufügen** aus, um ein Stammformatelement hinzuzufügen.
6. Wählen Sie im Dialogfeld **Hinzufügen** **Verbreitet\\Ordner** aus.
7. Wählen Sie **OK** aus, um das Hinzufügen des neuen Stammelements zu bestätigen.
8. Wählen Sie **Speichern** aus.

> [!NOTE]
> Die Formatstruktur beginnt mit dem Element des Typs **Ordner**. Dieses Element generiert eine Ausgabe als komprimierte Datei (ZIP-Format). Wenn ein Dokument, das vom Element **Bericht** generiert wird, in eine ausgehende ZIP-Datei eingefügt wird, wird sein Inhalt komprimiert, um die Größe der ausgehenden Datei zu verringern.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Generieren eines EB-Formats, um ein komprimiertes Dokument zu erhalten

1. Wählen Sie auf der Seite **Formatdesigner** die Option **Ausführen** aus.
2. Laden Sie die vom Webbrowser angebotene ZIP-Datei herunter und öffnen Sie sie zur Überprüfung.
3. Beachten Sie, dass die Größe des generierten Dokuments im ZIP-Format 1 KB beträgt.

    > [!NOTE] 
    > Die Komprimierungsrate der XML-Datei, die diese ZIP-Datei enthält, beträgt 87 Prozent. Die Komprimierungsrate hängt von den Daten ab, die komprimiert werden.

    ![Vorschau des komprimierten ausgehenden Dokuments](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Wenn das EB-[Ziel](electronic-reporting-destinations.md) für das Formatelement konfiguriert ist, das die Ausgabe generiert (in diesem Beispiel das Element **Bericht**), wird die Komprimierung der Ausgabe umgangen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)

[Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)

[Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md)
