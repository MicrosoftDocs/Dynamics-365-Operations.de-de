--- 
title: Verkaufsangebote erstellen und bearbeiten
description: Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 84b67bc0216ca5af61b4d93260ca392a8ffd7209
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="f2d3e-103">Verkaufsangebote erstellen und bearbeiten</span><span class="sxs-lookup"><span data-stu-id="f2d3e-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2d3e-104">Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="f2d3e-105">Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="f2d3e-106">Ein Verkaufsangebot erstellen</span><span class="sxs-lookup"><span data-stu-id="f2d3e-106">Create a sales quotation</span></span>
1. <span data-ttu-id="f2d3e-107">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="f2d3e-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-108">Click New.</span></span>
3. <span data-ttu-id="f2d3e-109">Wählen Sie im Feld "Kontotyp" "Interessent" aus.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="f2d3e-110">Geben Sie im Feld '"Interessent' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="f2d3e-111">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-111">Expand the General section.</span></span>
    * <span data-ttu-id="f2d3e-112">Da Sie sich für die Erstellung eines Angebots über den Bereich "Vertrieb und Marketing" entschieden haben, wird der Typ automatisch auf Verkaufsangebot festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="f2d3e-113">Um ein Angebot für ein Projekt zu erstellen, müssen Sie über das Projektverwaltungs- und Buchhaltungsmodul zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="f2d3e-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-114">Click OK.</span></span>
    * <span data-ttu-id="f2d3e-115">Die Felder und Aktivitäten der Angebotspositionen sind mit denen in den Auftragspositionen vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="f2d3e-116">Wie Aufträge können auch Angebote für einen bestimmten Artikel erstellt werden. Wenn Artikelnummer nicht bekannt ist oder nicht zum Zeitpunkt der Erstellung Angebots vorhanden ist, können Angebote für eine Verkaufskategorie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="f2d3e-117">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="f2d3e-118">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="f2d3e-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-119">Close the page.</span></span>
10. <span data-ttu-id="f2d3e-120">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f2d3e-121">Sind gültige Handelsvereinbarungen für den zur Position ausgewählten Artikel vorhanden, werden die entsprechenden Preise und Rabatte automatisch in die Angebotsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="f2d3e-122">Stellen Sie sicher, dass das Feld "Preis je Einheit" einen Wert enthält. Sie können auch Rabattwerte eingeben.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="f2d3e-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-123">Click Save.</span></span>
12. <span data-ttu-id="f2d3e-124">Klicken Sie im Aktivitätsbereich auf "Verkaufsangebot".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="f2d3e-125">Klicken Sie auf "Summen".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-125">Click Totals.</span></span>
14. <span data-ttu-id="f2d3e-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-126">Click OK.</span></span>
15. <span data-ttu-id="f2d3e-127">Klicken Sie auf "Verkaufsangebotsposition".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="f2d3e-128">Klicken Sie auf "Preise".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-128">Click Prices.</span></span>
    * <span data-ttu-id="f2d3e-129">In der Seite "Ausführungspreissimulation" können Sie mit der Anpassung des erwarteten Umsatzerlöses oder der Rentabilität des Angebots auf Grundlage des gewünschten "Preis je Einheit", des Rabattbetrags, des Rabattprozentsatzes, des Gesamtbetrags, der Gewinnspanne bzw. des Deckungsbeitrags experimentieren.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="f2d3e-130">Wenn Sie mit den Zielvorgaben zufrieden sind, wenden Sie den Vorschlag auf die Angebotsposition an und die preisbezogene Felder werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="f2d3e-131">Sie können so viele Preissimulationen erstellen wie gewünscht.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-131">You can create as many price simulations as you wish.</span></span> <span data-ttu-id="f2d3e-132">Wenn Sie auf "Neu" klicken, werden die Preisbedingungen von der aktuellen Angebotsposition zur Seite kopiert.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="f2d3e-133">Sie können die Werte in jedem der preisbezogene Felder auf die Zielwerte ändern.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="f2d3e-134">Eine Änderung in einem der Felder löst eine Neuberechnung für alle anderen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="f2d3e-135">Damit das System die Handelsspanne und den Deckungsbeitrag berechnen kann, müssen die Einheitenkosten des Produkts muss bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="f2d3e-136">Verwenden Sie Registerkarte "Simulierte Preise" für eine detaillierte Ansicht der ursprünglichen Preise, der vorgeschlagenen Änderungen und ihrer Auswirkungen auf den Angebotssummen.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="f2d3e-137">Wenn eine Simulation für einen neuen Betrag auf ein Angebot angewendet wird, berechnet das System neu und legt einen neuen Wert für das Feld Preis je Einheit" fest.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="f2d3e-138">Wenn die Simulation auf Grundlage eines neuen Deckungsbeitrags oder ein neues Deckungsbeitragsverhältnis basiert, wird nur das Feld "Nettobetrag" aktualisiert. Der Preis je Einheit ist leer.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="f2d3e-139">In beiden Fällen werden alle Rabatten für die Angebotsposition gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="f2d3e-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-140">Close the page.</span></span>
18. <span data-ttu-id="f2d3e-141">Klicken Sie im Aktivitätsbereich auf "Angebot".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="f2d3e-142">Klicken Sie auf "Angebot versenden".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-142">Click Send quotation.</span></span>
20. <span data-ttu-id="f2d3e-143">Wählen Sie "Ja" im Feld "Angebot drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="f2d3e-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-144">Click OK.</span></span>
    * <span data-ttu-id="f2d3e-145">Der Bericht kann einige Minute dauern.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-145">The report may take a minute to generate.</span></span> <span data-ttu-id="f2d3e-146">Schließen Sie nicht die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="f2d3e-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="f2d3e-148">Ein Verkaufsangebot aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f2d3e-148">Update a sales quotation</span></span>
1. <span data-ttu-id="f2d3e-149">Klicken Sie im Aktivitätsbereich auf "Nachverfolgung".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="f2d3e-150">Klicken Sie auf "In Debitor konvertieren".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="f2d3e-151">Geben Sie im Feld "Kundenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="f2d3e-152">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-152">Click Check.</span></span>
    * <span data-ttu-id="f2d3e-153">Stellen Sie sicher, das eine Nachricht anzeigt, dass die Kontonummer frei ist.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="f2d3e-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-154">Click OK.</span></span>
    * <span data-ttu-id="f2d3e-155">Das System hat nun ein neues Debitorenkonto für den Interessenten im Angebot erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="f2d3e-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-156">Close the page.</span></span>
7. <span data-ttu-id="f2d3e-157">Klicken Sie im Aktivitätsbereich auf "Nachverfolgung".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="f2d3e-158">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-158">Click Confirm.</span></span>
9. <span data-ttu-id="f2d3e-159">Geben Sie im Feld 'Grund' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="f2d3e-160">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-160">Click OK.</span></span>
11. <span data-ttu-id="f2d3e-161">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="f2d3e-162">Klicken Sie auf "Aufträge".</span><span class="sxs-lookup"><span data-stu-id="f2d3e-162">Click Sales orders.</span></span>
13. <span data-ttu-id="f2d3e-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d3e-163">Close the page.</span></span>


