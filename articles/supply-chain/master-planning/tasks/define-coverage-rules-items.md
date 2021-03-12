---
title: Dispositionsregeln für Artikel definieren
description: Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999880"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="e0c00-103">Dispositionsregeln für Artikel definieren</span><span class="sxs-lookup"><span data-stu-id="e0c00-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0c00-104">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="e0c00-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e0c00-105">Diese Aufzeichnung zeigt, wie Dispositionsregeln erstellt und Deckungseinstellungen für bestimmte Artikel überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e0c00-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="e0c00-106">Sie zeigt auch, wie Standardbestandseinstellungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0c00-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="e0c00-107">Erstellen einer Dispositionssteuerungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e0c00-107">Create a coverage group</span></span>
1. <span data-ttu-id="e0c00-108">Wechseln Sie zu **Navigationsbereich > Module > Produktprogrammplanung > Einstellungen > Dispositionssteuerungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="e0c00-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-109">Click **New**.</span></span>
3. <span data-ttu-id="e0c00-110">Geben Sie im Feld **Dispositionssteuerungsgruppe** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="e0c00-111">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="e0c00-112">Geben Sie im Feld **Kalender** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="e0c00-113">Wählen Sie im Feld "Kalender" den Kalender aus, den der Produktprogrammplan verwendet, um Auffüllungsvorschläge für Artikel in dieser Gruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0c00-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="e0c00-114">Wählen Sie im Feld **Dispositionsverfahren** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="e0c00-115">Wählen Sie für diese Prozedur „Anforderung“ aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="e0c00-116">Geben Sie im Feld **Planungszeitraum (Tage)** den Wert „90“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="e0c00-117">Für Artikel in dieser Gruppe, erstellt der Produktprogrammplan Wiederbeschaffungsvorschläge für bis 90 Tage in die Zukunft.</span><span class="sxs-lookup"><span data-stu-id="e0c00-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="e0c00-118">Geben Sie im Feld **Negative Tage** den Wert „1“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="e0c00-119">Geben Sie im Feld **Positive Tage** den Wert „1“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="e0c00-120">Erweitern oder reduzieren Sie den Abschnitt **Andere**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="e0c00-121">Geben Sie unter dem Abschnitt **Sicherheitszuschläge in Tagen** im Feld **Zum Bedarfsdatum hinzugefügter Sicherheitszuschlag für Warenzugang** den Wert „1“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="e0c00-122">Wenn z. B. der Sicherheitszuschlag für den Warenzugang auf 1 Tag festgelegt ist und für eine Bestellposition ein Zugang am 15. Mai eingeplant ist, errechnet der Produktprogrammplan ein angepasstes Warenzugangsdatum ab dem 16. Mai berechnet.</span><span class="sxs-lookup"><span data-stu-id="e0c00-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="e0c00-123">Geben Sie im Feld **Vom Bedarfsdatum abgezogener Sicherheitszuschlag für Warenabgang** den Wert „1“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="e0c00-124">Wenn z. B. der Sicherheitszuschlag auf 1 Tag festgelegt ist und für eine Auftragsposition eine Lieferung am 15. Mai eingeplant ist, wird beim Produktprogrammplanungslauf als angepasstes Lieferdatum der 14. Mai berechnet.</span><span class="sxs-lookup"><span data-stu-id="e0c00-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="e0c00-125">Geben Sie im Feld **Sicherheitszuschlag für Wiederbestellung, der zur Durchlaufzeit eines Artikels addiert wird** den Wert „1“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="e0c00-126">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="e0c00-127">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="e0c00-127">Create a new product</span></span>
1. <span data-ttu-id="e0c00-128">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="e0c00-129">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-129">Click **New**.</span></span>
3. <span data-ttu-id="e0c00-130">Geben Sie im Feld **Produktnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="e0c00-131">Geben Sie im Feld **Produktname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="e0c00-132">Klicken Sie im Feld **Artikelmodellgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e0c00-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e0c00-133">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0c00-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e0c00-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0c00-135">Klicken Sie im Feld **Artikelgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e0c00-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e0c00-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e0c00-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e0c00-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e0c00-138">Klicken Sie im Feld **Lagerdimensionsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e0c00-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="e0c00-139">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e0c00-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e0c00-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e0c00-141">Klicken Sie im Feld **Rückverfolgungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e0c00-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e0c00-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="e0c00-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e0c00-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e0c00-144">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="e0c00-145">Standardmäßige Auftragseinstellungen einrichten</span><span class="sxs-lookup"><span data-stu-id="e0c00-145">Setup default order settings</span></span>
1. <span data-ttu-id="e0c00-146">Klicken Sie im **Aktivitätsbereich** auf **Plan**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="e0c00-147">Klicken Sie unter **Auftragseinstellungen** auf **Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="e0c00-148">Geben Sie unter **Bestellung** im Feld **Standardstandort** den Standort ein, der als Standard verwendet werden soll, wenn Bestellungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e0c00-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="e0c00-149">Geben Sie im Feld **Standardlagerort** den Standort ein, an dem der Artikel gelagert wird.</span><span class="sxs-lookup"><span data-stu-id="e0c00-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="e0c00-150">Erweitern oder reduzieren Sie den Abschnitt **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="e0c00-151">Geben Sie im Feld **Mehrfach** den Wert „10“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="e0c00-152">Geben Sie im Feld **Minimale Auftragsmenge** den Wert „10“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="e0c00-153">Geben Sie im Feld **Maximale Auftragsmenge** den Wert „100“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="e0c00-154">Geben Sie im Feld **Standard-Auftragsmenge** den Wert „10“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="e0c00-155">Geben Sie im Feld **Lieferzeit Einkauf** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="e0c00-156">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Arbeitstage**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="e0c00-157">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-157">Click **Save**.</span></span>
13. <span data-ttu-id="e0c00-158">Wählen Sie im Feld **Standardauftragstyp** die Option „Bestellung“ aus.</span><span class="sxs-lookup"><span data-stu-id="e0c00-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="e0c00-159">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-159">Click **Save**.</span></span>
15. <span data-ttu-id="e0c00-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0c00-160">Close the page.</span></span> <span data-ttu-id="e0c00-161">Schließen Sie die Einstellungsseite "Standardauftrag".</span><span class="sxs-lookup"><span data-stu-id="e0c00-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="e0c00-162">Einen Artikel zu einer Dispositionssteuerungsgruppe hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e0c00-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="e0c00-163">Erweitern oder reduzieren Sie den Abschnitt **Plan**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="e0c00-164">Klicken Sie im Feld **Dispositionssteuerungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e0c00-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e0c00-165">Suchen Sie in der Liste die **Dispositionssteuerungsgruppe**, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e0c00-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="e0c00-166">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e0c00-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="e0c00-167">Artikeldispositionsregeln erstellen</span><span class="sxs-lookup"><span data-stu-id="e0c00-167">Create item coverage rules</span></span>
1. <span data-ttu-id="e0c00-168">Klicken Sie im **Aktivitätsbereich** auf **Plan**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="e0c00-169">Klicken Sie unter **Disposition** auf **Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="e0c00-170">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-170">Click **New**.</span></span>
4. <span data-ttu-id="e0c00-171">Klicken Sie auf die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="e0c00-172">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von **Deckungsgruppeneinstellungen überschreiben**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="e0c00-173">Geben Sie im Feld **Planungszeitraum (Tage)** den Wert „60“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="e0c00-174">Obwohl Artikel in der Dispositionssteuerungsgruppe "Bedarf" 90 Tage im Voraus geplant werden, wird dieser Artikel 60 Tage im Voraus geplant.</span><span class="sxs-lookup"><span data-stu-id="e0c00-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="e0c00-175">Geben Sie im Feld **Negative Tage** den Wert „2“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="e0c00-176">Geben Sie im Feld **Positive Tage** den Wert „2“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="e0c00-177">Klicken Sie auf die Registerkarte **Vorlaufzeit**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="e0c00-178">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von **Einkauf**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="e0c00-179">Geben Sie im Feld **Bestellzeit** den Wert „5“ ein.</span><span class="sxs-lookup"><span data-stu-id="e0c00-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="e0c00-180">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e0c00-180">Click **Save**.</span></span>

