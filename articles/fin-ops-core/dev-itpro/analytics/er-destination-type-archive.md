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
# <span data-ttu-id="81660-103"><a name="ArchiveDestinationType">Archivziel</a></span><span class="sxs-lookup"><span data-stu-id="81660-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81660-104">Sie können ein Archivierungsziel für jede ORDNER- oder DATEI-Komponente eines ER-Formats konfigurieren, das zum Generieren ausgehender Dokumente konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="81660-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="81660-105">Basierend auf der Zieleinstellung wird ein generiertes Dokument als Anhang eines Datensatzes der ER-Einzelvorgangsliste gespeichert.</span><span class="sxs-lookup"><span data-stu-id="81660-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="81660-106">Mit dieser Option können Sie das generierte Dokument an einen SharePoint-Ordner oder Microsoft Azure-Speicher senden.</span><span class="sxs-lookup"><span data-stu-id="81660-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="81660-107">Legen Sie **Aktiviert** auf **Ja** fest, um die Ausgabe an ein Ziel zu senden, das über den ausgewählten Dokumenttyp definiert ist.</span><span class="sxs-lookup"><span data-stu-id="81660-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="81660-108">Nur Dokumenttypen mit der Gruppe **Datei** stehen zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="81660-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="81660-109">Sie legen die Dokument-[Typen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) unter **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Dokumenttypen** fest.</span><span class="sxs-lookup"><span data-stu-id="81660-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="81660-110">Die Konfiguration für ER-Ziele ist identisch mit der Konfiguration für das Dokumentverwaltungssystem.</span><span class="sxs-lookup"><span data-stu-id="81660-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="81660-111">[![Seite „Dokumenttypen”](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="81660-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="81660-112">Der Speicherort bestimmt, wo die Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="81660-112">The location determines where the file is saved.</span></span> <span data-ttu-id="81660-113">Nachdem das Ziel **Archiv** aktiviert ist, können Sie die Ergebnisse im Einzelvorgangsarchiv speichern.</span><span class="sxs-lookup"><span data-stu-id="81660-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="81660-114">Sie können die Ergebnisse **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Elektronische Berichterstellung archivierte Einzelvorgänge** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="81660-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="81660-115">Wählen Sie einen Dokumenttyp im Einzelvorgangsarchiv unter **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstattung** \> **Parameter für elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="81660-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="81660-116">Weitere Informationen finden Sie unter [Konfigurieren des Frameworks für elektronische Berichterstellung (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="81660-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="81660-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="81660-117">SharePoint</span></span>

<span data-ttu-id="81660-118">Sie können eine Datei in einem bestimmten SharePoint-Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="81660-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="81660-119">Zum Definieren des standardmäßigen SharePoint-Servers navigieren Sie zu **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Parameter für Dokumentverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="81660-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="81660-120">Konfigurieren Sie auf der Registerkarte **SharePoint** den SharePoint-Ordner.</span><span class="sxs-lookup"><span data-stu-id="81660-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="81660-121">Anschließend können Sie ihn als Ordner auswählen, in dem die ER-Ausgabe gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="81660-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="81660-122">Der **SharePoint**-Speicherort muss in diesem Dokumenttyp ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="81660-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="81660-123">[![Einen SharePoint-Ordner auswählen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="81660-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="81660-124">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="81660-124">Azure Storage</span></span>

<span data-ttu-id="81660-125">Wenn der Dokumenttypspeicherort auf **Azure-Speicher** festgelegt ist, können Sie eine Datei in Azure Storage speichern.</span><span class="sxs-lookup"><span data-stu-id="81660-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81660-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81660-126">Additional resources</span></span>

- [<span data-ttu-id="81660-127">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="81660-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="81660-128">Zielorte für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="81660-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="81660-129">Konfigurieren der Dokumentverwaltung</span><span class="sxs-lookup"><span data-stu-id="81660-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
