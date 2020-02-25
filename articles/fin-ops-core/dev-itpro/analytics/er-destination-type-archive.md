---
title: Archivieren des ER-Zieltyps
description: Dieses Thema enthält Informationen zum Konfigurieren eines Archivierungsziels für jede ORDNER- oder DATEI-Komponente eines ER-Formats (Electronic Reporting, elektronische Berichterstellung), das zum Generieren ausgehender Dokumente konfiguriert ist.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019788"
---
# <a name="ArchiveDestinationType">Archivziel</a>

[!include [banner](../includes/banner.md)]

Sie können ein Archivierungsziel für jede ORDNER- oder DATEI-Komponente eines ER-Formats konfigurieren, das zum Generieren ausgehender Dokumente konfiguriert ist. Basierend auf der Zieleinstellung wird ein generiertes Dokument als Anhang eines Datensatzes der ER-Einzelvorgangsliste gespeichert.

Mit dieser Option können Sie das generierte Dokument an einen SharePoint-Ordner oder Microsoft Azure-Speicher senden. Legen Sie **Aktiviert** auf **Ja** fest, um die Ausgabe an ein Ziel zu senden, das über den ausgewählten Dokumenttyp definiert ist. Nur Dokumenttypen mit der Gruppe **Datei** stehen zur Auswahl. Sie legen die Dokument-[Typen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) unter **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Dokumenttypen** fest. Die Konfiguration für ER-Ziele ist identisch mit der Konfiguration für das Dokumentverwaltungssystem.

[![Seite „Dokumenttypen”](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Der Speicherort bestimmt, wo die Datei gespeichert wird. Nachdem das Ziel **Archiv** aktiviert ist, können Sie die Ergebnisse im Einzelvorgangsarchiv speichern. Sie können die Ergebnisse **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Elektronische Berichterstellung archivierte Einzelvorgänge** anzeigen.

> [!NOTE]
> Wählen Sie einen Dokumenttyp im Einzelvorgangsarchiv unter **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstattung** \> **Parameter für elektronische Berichterstellung** aus. Weitere Informationen finden Sie unter [Konfigurieren des Frameworks für elektronische Berichterstellung (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Sie können eine Datei in einem bestimmten SharePoint-Ordner speichern. Zum Definieren des standardmäßigen SharePoint-Servers navigieren Sie zu **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Parameter für Dokumentverwaltung**. Konfigurieren Sie auf der Registerkarte **SharePoint** den SharePoint-Ordner. Anschließend können Sie ihn als Ordner auswählen, in dem die ER-Ausgabe gespeichert wird. Der **SharePoint**-Speicherort muss in diesem Dokumenttyp ausgewählt werden.

[![Einen SharePoint-Ordner auswählen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

Wenn der Dokumenttypspeicherort auf **Azure-Speicher** festgelegt ist, können Sie eine Datei in Azure Storage speichern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)
- [Konfigurieren der Dokumentverwaltung](../../fin-ops/organization-administration/configure-document-management.md)
