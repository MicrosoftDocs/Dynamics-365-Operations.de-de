---
title: Wichtige historische Daten für Bedarfsplanungen
description: Um genaue Bedarfsplanungen zu erhalten, benötigen Sie historische Bedarfsdaten pro Artikel oder Artikelverteilungsschlüssel. In diesem Thema wird erläutert, wie Datenentitäten verwendet werden, um historische Bedarfsdaten aus jedem beliebigen System zu importieren, sodass Sie eine längere Historie von Bedarfsplanungsdaten haben.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6ba2e1a3a884d29bff491f914aa2d5f9ece2b84
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154226"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="eddf0-104">Wichtige historische Daten für Bedarfsplanungen</span><span class="sxs-lookup"><span data-stu-id="eddf0-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eddf0-105">Um die Genauigkeit von Bedarfsplanungen zu gewährleisten, benötigen Sie so viele historische Bedarfsdaten wie möglich pro Artikel oder Artikelvereilungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="eddf0-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="eddf0-106">Wenn die historischen Bedarfsdaten nicht bereits importiert sind, verwenden Sie die Datenentität **Historischer externer Bedarf** (ReqDemPlanHistoricalExternalDemandEntity) in Dynamics 365 Supply Chain Management, um sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="eddf0-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="eddf0-107">Im Arbeitsbereich **Datenverwaltung** können Sie eine Übersicht aller Felder in der Entität anzeigen.</span><span class="sxs-lookup"><span data-stu-id="eddf0-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="eddf0-108">Öffnen Sie den Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="eddf0-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="eddf0-109">Wählen Sie die Kachel **Datenentitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="eddf0-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="eddf0-110">Durchsuchen Sie die Entitätsliste nach **Historischer externer Bedarf**.</span><span class="sxs-lookup"><span data-stu-id="eddf0-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="eddf0-111">Wählen Sie **Zielfelder** aus.</span><span class="sxs-lookup"><span data-stu-id="eddf0-111">Select **Target fields**.</span></span> <span data-ttu-id="eddf0-112">Die folgenden Entitätsfelder sind obligatorisch: Standort (**DeliveringSiteId**), Datum (**DemandDate**), Menge (**DemandQuantity**) sowie entweder Artikelnummer (**ItemNumber**) oder Artikelverteilungsschlüssel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="eddf0-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="eddf0-113">Um die Datenentität zu verwenden, müssen Sie über eine Microsoft Excel-Datei oder eine durch Trennzeichen getrennte Datei (CSV-Datei) verfügen, die die historischen Bedarfsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="eddf0-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="eddf0-114">Das folgende Beispiel zeigt, wie die Daten aus einer CSV-Datei importiert werden.</span><span class="sxs-lookup"><span data-stu-id="eddf0-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="eddf0-115">Weitere Informationen zum Importieren von Daten, einschließlich zum Bereinigen von Daten nach einem Import, finden Sie unter [Übersicht zu Datenimportaufträgen und Datenexportaufträgen](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) und in den verwandten Themen.</span><span class="sxs-lookup"><span data-stu-id="eddf0-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="eddf0-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eddf0-116">Example</span></span>

<span data-ttu-id="eddf0-117">Sie können die folgende Datei als Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="eddf0-117">You can use the following file as an example.</span></span> <span data-ttu-id="eddf0-118">Laden Sie Die [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/) herunter.</span><span class="sxs-lookup"><span data-stu-id="eddf0-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="eddf0-119">Diese Datei enthält die historischen Bedarfsdaten für Artikel D0001.</span><span class="sxs-lookup"><span data-stu-id="eddf0-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="eddf0-120">Sie enthält nur die folgenden Pflichtfelder: Standort, Menge und das Bedarfsdatum.</span><span class="sxs-lookup"><span data-stu-id="eddf0-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="eddf0-121">Wählen Sie das Unternehmen aus, in das die historischen Bedarfsdaten importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eddf0-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="eddf0-122">Öffnen Sie den Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="eddf0-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="eddf0-123">Wählen Sie die Kachel **Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="eddf0-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="eddf0-124">Geben Sie einen Namen für das Importprojekt ein, wie **Historischen Bedarf für Artikel D0001 importieren**.</span><span class="sxs-lookup"><span data-stu-id="eddf0-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="eddf0-125">Wählen Sie im Feld **Quelldatenformat** das Dateiformat der Datei aus, die Sie importieren.</span><span class="sxs-lookup"><span data-stu-id="eddf0-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="eddf0-126">Um die HistoricalDemandData-Datei für dieses Beispiel zu importieren, wählen Sie **CSV** aus.</span><span class="sxs-lookup"><span data-stu-id="eddf0-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="eddf0-127">Wählen Sie im Feld **Entitätsname** die Option **Historischer externer Bedarf** aus.</span><span class="sxs-lookup"><span data-stu-id="eddf0-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="eddf0-128">Speichern Sie die Datei auf Ihrem Computer, und laden Sie sie dann hoch.</span><span class="sxs-lookup"><span data-stu-id="eddf0-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="eddf0-129">**Import** auswählen</span><span class="sxs-lookup"><span data-stu-id="eddf0-129">Select **Import**.</span></span>
9. <span data-ttu-id="eddf0-130">Die Seite **Ausführungszusammenfassung** wird automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="eddf0-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="eddf0-131">Überprüfen Sie die importierten Daten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="eddf0-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="eddf0-132">Nachdem Sie die historischen Bedarfsdaten importiert haben, können Sie eine Bedarfsplanung generieren.</span><span class="sxs-lookup"><span data-stu-id="eddf0-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eddf0-133">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eddf0-133">Additional resources</span></span>

[<span data-ttu-id="eddf0-134">Eine statistische Grundplanung generieren</span><span class="sxs-lookup"><span data-stu-id="eddf0-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="eddf0-135">Einzelvorgänge für Datenimport und ‑export – Übersicht</span><span class="sxs-lookup"><span data-stu-id="eddf0-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)
