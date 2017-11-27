---
title: "Wichtige historische Daten für Bedarfsplanungen"
description: "Um genaue Bedarfsplanungen zu erhalten, benötigen Sie historische Bedarfsdaten pro Artikel oder Artikelverteilungsschlüssel. In diesem Thema wird erläutert, wie Datenentitäten verwendet werden, um historische Bedarfsdaten aus jedem beliebigen System zu importieren, sodass Sie eine längere Historie von Bedarfsplanungsdaten haben."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 02daa312d74311432c0c468e3e691637dcf94157
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="88994-104">Wichtige historische Daten für Bedarfsplanungen</span><span class="sxs-lookup"><span data-stu-id="88994-104">Import historical data for demand forecasts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="88994-105">Um die Genauigkeit von Bedarfsplanungen zu gewährleisten, benötigen Sie so viele historische Bedarfsdaten wie möglich pro Artikel oder Artikelvereilungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="88994-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="88994-106">Wenn die historischen Bedarfsdaten nicht bereits importiert sind, verwenden Sie die Datenentität **Historischer externer Bedarf** (ReqDemPlanHistoricalExternalDemandEntity) in Microsoft Dynamics 365 for Finance and Operations, um sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="88994-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="88994-107">Im Arbeitsbereich **Datenverwaltung** können Sie eine Übersicht aller Felder in der Entität anzeigen.</span><span class="sxs-lookup"><span data-stu-id="88994-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="88994-108">Öffnen Sie den Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="88994-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="88994-109">Klicken Sie auf die Kachel **Datenentitäten**.</span><span class="sxs-lookup"><span data-stu-id="88994-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="88994-110">Durchsuchen Sie die Entitätsliste nach **Historischer externer Bedarf**.</span><span class="sxs-lookup"><span data-stu-id="88994-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="88994-111">Klicken Sie auf **Zielfelder**.</span><span class="sxs-lookup"><span data-stu-id="88994-111">Click **Target fields**.</span></span> <span data-ttu-id="88994-112">Die folgenden Entitätsfelder sind obligatorisch: Standort (**DeliveringSiteId**), Datum (**DemandDate**), Menge (**DemandQuantity**) sowie entweder Artikelnummer (**ItemNumber**) oder Artikelverteilungsschlüssel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="88994-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="88994-113">Um die Datenentität zu verwenden, müssen Sie über eine Microsoft Excel-Datei oder eine durch Trennzeichen getrennte Datei (CSV-Datei) verfügen, die die historischen Bedarfsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="88994-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="88994-114">Das folgende Beispiel zeigt, wie die Daten aus einer CSV-Datei importiert werden.</span><span class="sxs-lookup"><span data-stu-id="88994-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="88994-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="88994-115">Example</span></span>

<span data-ttu-id="88994-116">Sie können die folgende Datei als Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="88994-116">You can use the following file as an example.</span></span> <span data-ttu-id="88994-117">Laden Sie Die [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) herunter.</span><span class="sxs-lookup"><span data-stu-id="88994-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="88994-118">Diese Datei enthält die historischen Bedarfsdaten für Artikel D0001.</span><span class="sxs-lookup"><span data-stu-id="88994-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="88994-119">Sie enthält nur die folgenden Pflichtfelder: Standort, Menge und das Bedarfsdatum.</span><span class="sxs-lookup"><span data-stu-id="88994-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="88994-120">Wählen Sie das Unternehmen aus, in das die historischen Bedarfsdaten importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88994-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="88994-121">Öffnen Sie den Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="88994-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="88994-122">Klicken Sie auf die Kachel **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="88994-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="88994-123">Geben Sie einen Namen für das Importprojekt ein, wie **Historischen Bedarf für Artikel D0001 importieren**.</span><span class="sxs-lookup"><span data-stu-id="88994-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="88994-124">Wählen Sie im Feld **Quelldatenformat** das Dateiformat der Datei aus, die Sie importieren.</span><span class="sxs-lookup"><span data-stu-id="88994-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="88994-125">Um die HistoricalDemandData-Datei für dieses Beispiel zu importieren, wählen Sie **CSV** aus.</span><span class="sxs-lookup"><span data-stu-id="88994-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="88994-126">Wählen Sie im Feld **Entitätsname** die Option **Historischer externer Bedarf** aus.</span><span class="sxs-lookup"><span data-stu-id="88994-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="88994-127">Speichern Sie die Datei auf Ihrem Computer, und laden Sie sie dann hoch.</span><span class="sxs-lookup"><span data-stu-id="88994-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="88994-128">Klicken Sie auf **Import**.</span><span class="sxs-lookup"><span data-stu-id="88994-128">Click **Import**.</span></span>
9. <span data-ttu-id="88994-129">Die Seite **Ausführungszusammenfassung** wird automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="88994-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="88994-130">Überprüfen Sie die importierten Daten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="88994-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="88994-131">Nachdem Sie die historischen Bedarfsdaten importiert haben, können Sie eine Bedarfsplanung generieren.</span><span class="sxs-lookup"><span data-stu-id="88994-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="see-also"></a><span data-ttu-id="88994-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88994-132">See also</span></span>

[<span data-ttu-id="88994-133">Eine statistische Grundplanung generieren</span><span class="sxs-lookup"><span data-stu-id="88994-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

