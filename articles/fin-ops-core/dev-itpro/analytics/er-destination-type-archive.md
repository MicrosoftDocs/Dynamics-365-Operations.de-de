---
title: Archivieren des ER-Zieltyps
description: In diesem Artikel wird erläutert, wie für jede FOLDER- oder FILE-Komponente eines EB-Formats (elektronische Berichterstellung) ein Archivziel konfiguriert wird.
author: kfend
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: d907bf391c0629d62da489cea90a05eabaf69ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285454"
---
# <a name="archive-er-destination-type"></a>Archivieren des ER-Zieltyps

[!include [banner](../includes/banner.md)]

Sie können für jede Komponente **Ordner** oder **Datei** eines EB-Formats ein Archivierungsziel konfigurieren, das zum Generieren ausgehender Dokumente konfiguriert ist. Basierend auf der Zieleinstellung wird ein generiertes Dokument als Anhang eines Datensatzes der ER-Einzelvorgangsliste gespeichert. Um die Ergebnisse anzuzeigen, wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Einzelvorgänge für elektronische Berichterstellung**.

Mit dieser Option können Sie das generierte Dokument an einen SharePoint-Ordner oder Microsoft Azure-Speicher senden. Legen Sie **Aktiviert** auf **Ja** fest, um die Ausgabe an ein Ziel zu senden, das über den ausgewählten Dokumenttyp definiert ist. Nur Dokumenttypen mit der Gruppe **Datei** stehen zur Auswahl. Sie legen die Dokument-[Typen](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) unter **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Dokumenttypen** fest. Die Konfiguration für ER-Ziele ist identisch mit der Konfiguration für das Dokumentverwaltungssystem.

[![Seite „Dokumenttypen“.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Der Speicherort bestimmt, wo die Datei gespeichert wird. Nachdem das Ziel **Archiv** aktiviert ist, können Sie die Ergebnisse im Einzelvorgangsarchiv speichern. Sie können die Ergebnisse **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Elektronische Berichterstellung archivierte Einzelvorgänge** anzeigen.

> [!NOTE]
> Wählen Sie einen Dokumenttyp im Einzelvorgangsarchiv unter **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstattung** \> **Parameter für elektronische Berichterstellung** aus. Weitere Informationen finden Sie unter [Konfigurieren des Frameworks für elektronische Berichterstellung (EB)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Sie können eine Datei in einem bestimmten SharePoint-Ordner speichern. Zum Definieren des standardmäßigen SharePoint-Servers navigieren Sie zu **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Parameter für Dokumentverwaltung**. Konfigurieren Sie auf der Registerkarte **SharePoint** den SharePoint-Ordner. Anschließend können Sie ihn als Ordner auswählen, in dem die ER-Ausgabe gespeichert wird. Der **SharePoint**-Speicherort muss in diesem Dokumenttyp ausgewählt werden.

[![Einen SharePoint-Ordner auswählen.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

Wenn der Dokumenttypspeicherort auf **Azure-Speicher** festgelegt ist, können Sie eine Datei in Azure Storage speichern.

> [!NOTE] 
> Das EB-Framework speichert Dateien dauerhaft im Azure Blob Storage, wohingegen das Datenverwaltungsframework die 7-Tage-Aufbewahrungsrichtlinie für Dokumente anwendet, die verarbeitet werden müssen. Weitere Informationen finden Sie unter [API zum Abrufen des Nachrichtenstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) und [Statusprüfungs-API](../data-entities/data-management-api.md#status-check-api). Die EB-bezogenen Dateien werden so lange wie nötig als Anhänge von Anwendungstabellendatensätzen im Azure Blob Storage gespeichert. Eine einzelne Datei wird zusammen mit dem Anwendungstabellendatensatz, an den diese Datei angehängt wurde, aus dem Azure Blob Storage gelöscht.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)
- [Konfigurieren der Dokumentverwaltung](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
