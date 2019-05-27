---
title: Wichtige historische Daten für Bedarfsplanungen
description: Um genaue Bedarfsplanungen zu erhalten, benötigen Sie historische Bedarfsdaten pro Artikel oder Artikelverteilungsschlüssel. In diesem Thema wird erläutert, wie Datenentitäten verwendet werden, um historische Bedarfsdaten aus jedem beliebigen System zu importieren, sodass Sie eine längere Historie von Bedarfsplanungsdaten haben.
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 018694c79c6dd64e19b010848aad8acd36b0a9a8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555132"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="e03e9-104">Wichtige historische Daten für Bedarfsplanungen</span><span class="sxs-lookup"><span data-stu-id="e03e9-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e03e9-105">Um die Genauigkeit von Bedarfsplanungen zu gewährleisten, benötigen Sie so viele historische Bedarfsdaten wie möglich pro Artikel oder Artikelvereilungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e03e9-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="e03e9-106">Wenn die historischen Bedarfsdaten nicht bereits importiert sind, verwenden Sie die Datenentität **Historischer externer Bedarf** (ReqDemPlanHistoricalExternalDemandEntity) in Microsoft Dynamics 365 for Finance and Operations, um sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="e03e9-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="e03e9-107">Im Arbeitsbereich **Datenverwaltung** können Sie eine Übersicht aller Felder in der Entität anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e03e9-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="e03e9-108">Öffnen Sie den Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="e03e9-109">Klicken Sie auf die Kachel **Datenentitäten**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="e03e9-110">Durchsuchen Sie die Entitätsliste nach **Historischer externer Bedarf**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="e03e9-111">Klicken Sie auf **Zielfelder**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-111">Click **Target fields**.</span></span> <span data-ttu-id="e03e9-112">Die folgenden Entitätsfelder sind obligatorisch: Standort (**DeliveringSiteId**), Datum (**DemandDate**), Menge (**DemandQuantity**) sowie entweder Artikelnummer (**ItemNumber**) oder Artikelverteilungsschlüssel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="e03e9-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="e03e9-113">Um die Datenentität zu verwenden, müssen Sie über eine Microsoft Excel-Datei oder eine durch Trennzeichen getrennte Datei (CSV-Datei) verfügen, die die historischen Bedarfsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="e03e9-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="e03e9-114">Das folgende Beispiel zeigt, wie die Daten aus einer CSV-Datei importiert werden.</span><span class="sxs-lookup"><span data-stu-id="e03e9-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="e03e9-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e03e9-115">Example</span></span>

<span data-ttu-id="e03e9-116">Sie können die folgende Datei als Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="e03e9-116">You can use the following file as an example.</span></span> <span data-ttu-id="e03e9-117">Laden Sie Die [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) herunter.</span><span class="sxs-lookup"><span data-stu-id="e03e9-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="e03e9-118">Diese Datei enthält die historischen Bedarfsdaten für Artikel D0001.</span><span class="sxs-lookup"><span data-stu-id="e03e9-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="e03e9-119">Sie enthält nur die folgenden Pflichtfelder: Standort, Menge und das Bedarfsdatum.</span><span class="sxs-lookup"><span data-stu-id="e03e9-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="e03e9-120">Wählen Sie das Unternehmen aus, in das die historischen Bedarfsdaten importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e03e9-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="e03e9-121">Öffnen Sie den Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="e03e9-122">Klicken Sie auf die Kachel **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="e03e9-123">Geben Sie einen Namen für das Importprojekt ein, wie **Historischen Bedarf für Artikel D0001 importieren**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="e03e9-124">Wählen Sie im Feld **Quelldatenformat** das Dateiformat der Datei aus, die Sie importieren.</span><span class="sxs-lookup"><span data-stu-id="e03e9-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="e03e9-125">Um die HistoricalDemandData-Datei für dieses Beispiel zu importieren, wählen Sie **CSV** aus.</span><span class="sxs-lookup"><span data-stu-id="e03e9-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="e03e9-126">Wählen Sie im Feld **Entitätsname** die Option **Historischer externer Bedarf** aus.</span><span class="sxs-lookup"><span data-stu-id="e03e9-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="e03e9-127">Speichern Sie die Datei auf Ihrem Computer, und laden Sie sie dann hoch.</span><span class="sxs-lookup"><span data-stu-id="e03e9-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="e03e9-128">Klicken Sie auf **Import**.</span><span class="sxs-lookup"><span data-stu-id="e03e9-128">Click **Import**.</span></span>
9. <span data-ttu-id="e03e9-129">Die Seite **Ausführungszusammenfassung** wird automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e03e9-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="e03e9-130">Überprüfen Sie die importierten Daten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="e03e9-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="e03e9-131">Nachdem Sie die historischen Bedarfsdaten importiert haben, können Sie eine Bedarfsplanung generieren.</span><span class="sxs-lookup"><span data-stu-id="e03e9-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e03e9-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e03e9-132">Additional resources</span></span>

[<span data-ttu-id="e03e9-133">Eine statistische Grundplanung generieren</span><span class="sxs-lookup"><span data-stu-id="e03e9-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
