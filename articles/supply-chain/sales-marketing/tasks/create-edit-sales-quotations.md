---
title: Verkaufsangebote erstellen und bearbeiten
description: Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546109"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="d4b3b-103">Verkaufsangebote erstellen und bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d4b3b-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4b3b-104">Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="d4b3b-105">Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="d4b3b-106">Ein Verkaufsangebot erstellen</span><span class="sxs-lookup"><span data-stu-id="d4b3b-106">Create a sales quotation</span></span>
1. <span data-ttu-id="d4b3b-107">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="d4b3b-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-108">Click New.</span></span>
3. <span data-ttu-id="d4b3b-109">Wählen Sie im Feld "Kontotyp" "Interessent" aus.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="d4b3b-110">Geben Sie im Feld '"Interessent' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="d4b3b-111">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-111">Expand the General section.</span></span>
    * <span data-ttu-id="d4b3b-112">Da Sie sich für die Erstellung eines Angebots über den Bereich "Vertrieb und Marketing" entschieden haben, wird der Typ automatisch auf Verkaufsangebot festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="d4b3b-113">Um ein Angebot für ein Projekt zu erstellen, müssen Sie über das Projektverwaltungs- und Buchhaltungsmodul zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="d4b3b-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-114">Click OK.</span></span>
    * <span data-ttu-id="d4b3b-115">Die Felder und Aktivitäten der Angebotspositionen sind mit denen in den Auftragspositionen vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="d4b3b-116">Wie Aufträge können auch Angebote für einen bestimmten Artikel erstellt werden. Wenn Artikelnummer nicht bekannt ist oder nicht zum Zeitpunkt der Erstellung Angebots vorhanden ist, können Angebote für eine Verkaufskategorie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="d4b3b-117">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="d4b3b-118">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="d4b3b-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-119">Close the page.</span></span>
10. <span data-ttu-id="d4b3b-120">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d4b3b-121">Sind gültige Handelsvereinbarungen für den zur Position ausgewählten Artikel vorhanden, werden die entsprechenden Preise und Rabatte automatisch in die Angebotsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="d4b3b-122">Stellen Sie sicher, dass das Feld "Preis je Einheit" einen Wert enthält. Sie können auch Rabattwerte eingeben.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="d4b3b-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-123">Click Save.</span></span>
12. <span data-ttu-id="d4b3b-124">Klicken Sie im Aktivitätsbereich auf "Verkaufsangebot".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="d4b3b-125">Klicken Sie auf "Summen".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-125">Click Totals.</span></span>
14. <span data-ttu-id="d4b3b-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-126">Click OK.</span></span>
15. <span data-ttu-id="d4b3b-127">Klicken Sie auf "Verkaufsangebotsposition".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="d4b3b-128">Klicken Sie auf "Preise".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-128">Click Prices.</span></span>
    * <span data-ttu-id="d4b3b-129">In der Seite "Ausführungspreissimulation" können Sie mit der Anpassung des erwarteten Umsatzerlöses oder der Rentabilität des Angebots auf Grundlage des gewünschten "Preis je Einheit", des Rabattbetrags, des Rabattprozentsatzes, des Gesamtbetrags, der Gewinnspanne bzw. des Deckungsbeitrags experimentieren.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="d4b3b-130">Wenn Sie mit den Zielvorgaben zufrieden sind, wenden Sie den Vorschlag auf die Angebotsposition an und die preisbezogene Felder werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="d4b3b-131">Sie können so viele Preissimulationen erstellen wie gewünscht.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="d4b3b-132">Wenn Sie auf "Neu" klicken, werden die Preisbedingungen von der aktuellen Angebotsposition zur Seite kopiert.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="d4b3b-133">Sie können die Werte in jedem der preisbezogene Felder auf die Zielwerte ändern.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="d4b3b-134">Eine Änderung in einem der Felder löst eine Neuberechnung für alle anderen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="d4b3b-135">Damit das System die Handelsspanne und den Deckungsbeitrag berechnen kann, müssen die Einheitenkosten des Produkts muss bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="d4b3b-136">Verwenden Sie Registerkarte "Simulierte Preise" für eine detaillierte Ansicht der ursprünglichen Preise, der vorgeschlagenen Änderungen und ihrer Auswirkungen auf den Angebotssummen.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="d4b3b-137">Wenn eine Simulation für einen neuen Betrag auf ein Angebot angewendet wird, berechnet das System neu und legt einen neuen Wert für das Feld Preis je Einheit" fest.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="d4b3b-138">Wenn die Simulation auf Grundlage eines neuen Deckungsbeitrags oder ein neues Deckungsbeitragsverhältnis basiert, wird nur das Feld "Nettobetrag" aktualisiert. Der Preis je Einheit ist leer.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="d4b3b-139">In beiden Fällen werden alle Rabatten für die Angebotsposition gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="d4b3b-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-140">Close the page.</span></span>
18. <span data-ttu-id="d4b3b-141">Klicken Sie im Aktivitätsbereich auf "Angebot".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="d4b3b-142">Klicken Sie auf "Angebot versenden".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-142">Click Send quotation.</span></span>
20. <span data-ttu-id="d4b3b-143">Wählen Sie "Ja" im Feld "Angebot drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="d4b3b-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-144">Click OK.</span></span>
    * <span data-ttu-id="d4b3b-145">Der Bericht kann einige Minute dauern.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-145">The report may take a minute to generate.</span></span> <span data-ttu-id="d4b3b-146">Schließen Sie nicht die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="d4b3b-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="d4b3b-148">Ein Verkaufsangebot aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d4b3b-148">Update a sales quotation</span></span>
1. <span data-ttu-id="d4b3b-149">Klicken Sie im Aktivitätsbereich auf "Nachverfolgung".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="d4b3b-150">Klicken Sie auf "In Debitor konvertieren".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="d4b3b-151">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="d4b3b-152">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-152">Click Check.</span></span>
    * <span data-ttu-id="d4b3b-153">Stellen Sie sicher, das eine Nachricht anzeigt, dass die Kontonummer frei ist.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="d4b3b-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-154">Click OK.</span></span>
    * <span data-ttu-id="d4b3b-155">Das System hat nun ein neues Debitorenkonto für den Interessenten im Angebot erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="d4b3b-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-156">Close the page.</span></span>
7. <span data-ttu-id="d4b3b-157">Klicken Sie im Aktivitätsbereich auf "Nachverfolgung".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="d4b3b-158">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-158">Click Confirm.</span></span>
9. <span data-ttu-id="d4b3b-159">Geben Sie im Feld 'Grund' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="d4b3b-160">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-160">Click OK.</span></span>
11. <span data-ttu-id="d4b3b-161">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="d4b3b-162">Klicken Sie auf "Aufträge".</span><span class="sxs-lookup"><span data-stu-id="d4b3b-162">Click Sales orders.</span></span>
13. <span data-ttu-id="d4b3b-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4b3b-163">Close the page.</span></span>

