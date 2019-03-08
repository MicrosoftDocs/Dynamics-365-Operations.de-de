---
title: Dispositionsregeln für Artikel definieren
description: Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320626"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="05b55-103">Dispositionsregeln für Artikel definieren</span><span class="sxs-lookup"><span data-stu-id="05b55-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05b55-104">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="05b55-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="05b55-105">Diese Aufzeichnung zeigt, wie Dispositionsregeln erstellt und Deckungseinstellungen für bestimmte Artikel überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="05b55-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="05b55-106">Sie zeigt auch, wie Standardbestandseinstellungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05b55-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="05b55-107">Erstellen einer Dispositionssteuerungsgruppe</span><span class="sxs-lookup"><span data-stu-id="05b55-107">Create a coverage group</span></span>
1. <span data-ttu-id="05b55-108">Wechseln Sie zu "Dispositionssteuerungsgruppe".</span><span class="sxs-lookup"><span data-stu-id="05b55-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="05b55-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05b55-109">Click New.</span></span>
3. <span data-ttu-id="05b55-110">Geben Sie im Feld "Dispositionssteuerungsgruppe" die Zeichenfolge "Bedarf" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="05b55-111">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="05b55-112">Geben Sie im Feld Kalender einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="05b55-113">Wählen Sie im Feld "Kalender" den Kalender aus, den der Produktprogrammplan verwendet, um Auffüllungsvorschläge für Artikel in dieser Gruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="05b55-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="05b55-114">Wählen Sie im Feld "Dispositionsverfahren" die Option "Bedarf" aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="05b55-115">Wählen Sie Anforderungen dieser Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="05b55-116">Geben Sie im Feld "Planungszeitraum (Tage)" den Wert "90" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="05b55-117">Für Artikel in dieser Gruppe, erstellt der Produktprogrammplan Wiederbeschaffungsvorschläge für bis 90 Tage in die Zukunft.</span><span class="sxs-lookup"><span data-stu-id="05b55-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="05b55-118">Geben Sie im Feld "Negative Tage" den Wert "1" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="05b55-119">Geben Sie im Feld "Positive Tage" den Wert "1" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="05b55-120">Erweitern oder reduzieren Sie den Abschnitt Andere.</span><span class="sxs-lookup"><span data-stu-id="05b55-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="05b55-121">Im Feld "Zum Bedarfsdatum hinzugefügter Warenzugang Toleranzzeit" geben Sie "1" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="05b55-122">Wenn z. B. der Sicherheitszuschlag für den Warenzugang auf 1 Tag festgelegt ist und für eine Bestellposition ein Zugang am 15. Mai eingeplant ist, errechnet der Produktprogrammplan ein angepasstes Warenzugangsdatum ab dem 16. Mai berechnet.</span><span class="sxs-lookup"><span data-stu-id="05b55-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="05b55-123">Im Feld "Vom Bedarfsdatum abgezogener Sicherheitszuschlag für Warenabgang" geben Sie "1" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="05b55-124">Wenn z. B. der Sicherheitszuschlag auf 1 Tag festgelegt ist und für eine Auftragsposition eine Lieferung am 15. Mai eingeplant ist, wird beim Produktprogrammplanungslauf als angepasstes Lieferdatum der 14. Mai berechnet.</span><span class="sxs-lookup"><span data-stu-id="05b55-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="05b55-125">Geben Sie im Feld "Sicherheitszuschlag für Wiederbestellung, der zur Durchlaufzeit eines Artikels addiert wird" den Wert "1" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="05b55-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05b55-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="05b55-127">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="05b55-127">Create a new product</span></span>
1. <span data-ttu-id="05b55-128">Wechseln Sie zu "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="05b55-128">Go to Released products.</span></span>
2. <span data-ttu-id="05b55-129">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05b55-129">Click New.</span></span>
3. <span data-ttu-id="05b55-130">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="05b55-131">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="05b55-132">Klicken Sie im Feld "Artikelmodellgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05b55-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="05b55-133">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="05b55-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05b55-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="05b55-135">Klicken Sie im Feld "Artikelgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05b55-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="05b55-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="05b55-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05b55-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="05b55-138">Klicken Sie im Feld "Lagerdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05b55-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="05b55-139">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="05b55-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05b55-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="05b55-141">Klicken Sie im Feld "Rückverfolgungsangaben-Gruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05b55-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="05b55-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="05b55-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05b55-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="05b55-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05b55-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="05b55-145">Standardmäßige Auftragseinstellungen einrichten</span><span class="sxs-lookup"><span data-stu-id="05b55-145">Setup default order settings</span></span>
1. <span data-ttu-id="05b55-146">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="05b55-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="05b55-147">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="05b55-147">Click Default order settings.</span></span>
3. <span data-ttu-id="05b55-148">Geben Sie im Feld "Einkaufsstandort" den Standort ein, der als Standard verwendet wird, wenn Bestellungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="05b55-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="05b55-149">Geben Sie im Feld "Bestandsstandort" den Standort ein, an dem der Artikel gelagert wird.</span><span class="sxs-lookup"><span data-stu-id="05b55-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="05b55-150">Erweitern oder reduzieren Sie den Abschnitt Bestand.</span><span class="sxs-lookup"><span data-stu-id="05b55-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="05b55-151">Legen Sie "Mehrfach" auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="05b55-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="05b55-152">Legen Sie die "Minimale</span><span class="sxs-lookup"><span data-stu-id="05b55-152">Set Min.</span></span> <span data-ttu-id="05b55-153">Auftragsmenge" auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="05b55-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="05b55-154">Legen Sie die "Maximale</span><span class="sxs-lookup"><span data-stu-id="05b55-154">Set Max.</span></span> <span data-ttu-id="05b55-155">Auftragsmenge" auf "100" fest.</span><span class="sxs-lookup"><span data-stu-id="05b55-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="05b55-156">Legen Sie die "Standardauftragsmenge" auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="05b55-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="05b55-157">Geben Sie im Feld "Lieferzeit Einkauf" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="05b55-158">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen Arbeitstage.</span><span class="sxs-lookup"><span data-stu-id="05b55-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="05b55-159">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05b55-159">Click Save.</span></span>
13. <span data-ttu-id="05b55-160">Wählen Sie im Feld "Standardauftragstyp" die Option "Bestellung" aus.</span><span class="sxs-lookup"><span data-stu-id="05b55-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="05b55-161">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05b55-161">Click Save.</span></span>
15. <span data-ttu-id="05b55-162">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05b55-162">Close the page.</span></span>
    * <span data-ttu-id="05b55-163">Schließen Sie die Einstellungsseite "Standardauftrag".</span><span class="sxs-lookup"><span data-stu-id="05b55-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="05b55-164">Einen Artikel zu einer Dispositionssteuerungsgruppe hinzufügen</span><span class="sxs-lookup"><span data-stu-id="05b55-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="05b55-165">Erweitern oder reduzieren Sie den Abschnitt Plan.</span><span class="sxs-lookup"><span data-stu-id="05b55-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="05b55-166">Klicken Sie im Feld "Dispositionssteuerungsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05b55-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="05b55-167">Suchen Sie in der Liste die "Dispositionssteuerungsgruppe", die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="05b55-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="05b55-168">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05b55-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="05b55-169">Artikeldispositionsregeln erstellen</span><span class="sxs-lookup"><span data-stu-id="05b55-169">Create item coverage rules</span></span>
1. <span data-ttu-id="05b55-170">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="05b55-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="05b55-171">Klicken Sie auf "Artikeldeckung".</span><span class="sxs-lookup"><span data-stu-id="05b55-171">Click Item coverage.</span></span>
3. <span data-ttu-id="05b55-172">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05b55-172">Click New.</span></span>
4. <span data-ttu-id="05b55-173">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="05b55-173">Click the General tab.</span></span>
5. <span data-ttu-id="05b55-174">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von "Deckungsgruppeneinstellungen überschreiben".</span><span class="sxs-lookup"><span data-stu-id="05b55-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="05b55-175">Geben Sie im Feld "Planungszeitraum (Tage)" den Wert "60" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="05b55-176">Obwohl Artikel in der Dispositionssteuerungsgruppe "Bedarf" 90 Tage im Voraus geplant werden, wird dieser Artikel 60 Tage im Voraus geplant.</span><span class="sxs-lookup"><span data-stu-id="05b55-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="05b55-177">Geben Sie im Feld "Negative Tage" den Wert "2" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="05b55-178">Geben Sie im Feld "Positive Tage" den Wert "2" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="05b55-179">Klicken Sie auf die Registerkarte "Durchlaufzeit".</span><span class="sxs-lookup"><span data-stu-id="05b55-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="05b55-180">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="05b55-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="05b55-181">Geben Sie im Feld "Bestellzeit" den Wert "5" ein.</span><span class="sxs-lookup"><span data-stu-id="05b55-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="05b55-182">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05b55-182">Click Save.</span></span>

