---
title: Archivieren des ER-Zieltyps
description: In diesem Thema wird erläutert, wie für jede FOLDER- oder FILE-Komponente eines EB-Formats (elektronische Berichterstellung) ein Archivziel konfiguriert wird.
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 079eda04fcc41fc637419a83452db10b89ed1ab9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894027"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="dba53-103">Archivieren des ER-Zieltyps</span><span class="sxs-lookup"><span data-stu-id="dba53-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dba53-104">Sie können für jede Komponente **Ordner** oder **Datei** eines EB-Formats ein Archivierungsziel konfigurieren, das zum Generieren ausgehender Dokumente konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="dba53-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="dba53-105">Basierend auf der Zieleinstellung wird ein generiertes Dokument als Anhang eines Datensatzes der ER-Einzelvorgangsliste gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dba53-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="dba53-106">Um die Ergebnisse anzuzeigen, wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Einzelvorgänge für elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="dba53-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="dba53-107">Mit dieser Option können Sie das generierte Dokument an einen SharePoint-Ordner oder Microsoft Azure-Speicher senden.</span><span class="sxs-lookup"><span data-stu-id="dba53-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="dba53-108">Legen Sie **Aktiviert** auf **Ja** fest, um die Ausgabe an ein Ziel zu senden, das über den ausgewählten Dokumenttyp definiert ist.</span><span class="sxs-lookup"><span data-stu-id="dba53-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="dba53-109">Nur Dokumenttypen mit der Gruppe **Datei** stehen zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="dba53-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="dba53-110">Sie legen die Dokument-[Typen](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) unter **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Dokumenttypen** fest.</span><span class="sxs-lookup"><span data-stu-id="dba53-110">You define document [types](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="dba53-111">Die Konfiguration für ER-Ziele ist identisch mit der Konfiguration für das Dokumentverwaltungssystem.</span><span class="sxs-lookup"><span data-stu-id="dba53-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="dba53-112">[![Seite „Dokumenttypen”](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="dba53-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="dba53-113">Der Speicherort bestimmt, wo die Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="dba53-113">The location determines where the file is saved.</span></span> <span data-ttu-id="dba53-114">Nachdem das Ziel **Archiv** aktiviert ist, können Sie die Ergebnisse im Einzelvorgangsarchiv speichern.</span><span class="sxs-lookup"><span data-stu-id="dba53-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="dba53-115">Sie können die Ergebnisse **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Elektronische Berichterstellung archivierte Einzelvorgänge** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dba53-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="dba53-116">Wählen Sie einen Dokumenttyp im Einzelvorgangsarchiv unter **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstattung** \> **Parameter für elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="dba53-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="dba53-117">Weitere Informationen finden Sie unter [Konfigurieren des Frameworks für elektronische Berichterstellung (EB)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="dba53-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="dba53-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="dba53-118">SharePoint</span></span>

<span data-ttu-id="dba53-119">Sie können eine Datei in einem bestimmten SharePoint-Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="dba53-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="dba53-120">Zum Definieren des standardmäßigen SharePoint-Servers navigieren Sie zu **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Parameter für Dokumentverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="dba53-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="dba53-121">Konfigurieren Sie auf der Registerkarte **SharePoint** den SharePoint-Ordner.</span><span class="sxs-lookup"><span data-stu-id="dba53-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="dba53-122">Anschließend können Sie ihn als Ordner auswählen, in dem die ER-Ausgabe gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="dba53-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="dba53-123">Der **SharePoint**-Speicherort muss in diesem Dokumenttyp ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="dba53-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="dba53-124">[![Einen SharePoint-Ordner auswählen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="dba53-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="dba53-125">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="dba53-125">Azure Storage</span></span>

<span data-ttu-id="dba53-126">Wenn der Dokumenttypspeicherort auf **Azure-Speicher** festgelegt ist, können Sie eine Datei in Azure Storage speichern.</span><span class="sxs-lookup"><span data-stu-id="dba53-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="dba53-127">Das EB-Framework speichert Dateien dauerhaft im Azure Blob Storage, wohingegen das Datenverwaltungsframework die 7-Tage-Aufbewahrungsrichtlinie für Dokumente anwendet, die verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dba53-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="dba53-128">Weitere Informationen finden Sie unter [API zum Abrufen des Nachrichtenstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) und [Statusprüfungs-API](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="dba53-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="dba53-129">Die EB-bezogenen Dateien werden so lange wie nötig als Anhänge von Anwendungstabellendatensätzen im Azure Blob Storage gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dba53-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="dba53-130">Eine einzelne Datei wird zusammen mit dem Anwendungstabellendatensatz, an den diese Datei angehängt wurde, aus dem Azure Blob Storage gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dba53-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dba53-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dba53-131">Additional resources</span></span>

- [<span data-ttu-id="dba53-132">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="dba53-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="dba53-133">Zielorte für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="dba53-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="dba53-134">Konfigurieren der Dokumentverwaltung</span><span class="sxs-lookup"><span data-stu-id="dba53-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]