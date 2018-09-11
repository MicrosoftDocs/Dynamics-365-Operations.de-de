--- 
title: "Buchungen an Intrastat übertragen"
description: "Diese Prozedur zeigt Ihnen Schritt für Schritt, wie Sie Intrastat-Parameter einrichten und Transaktionen nach Intrastat übertragen."
author: Anasyash
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: aac902f54c263114957d799264918b7fb74e6e09
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="05af5-103">Buchungen an Intrastat übertragen</span><span class="sxs-lookup"><span data-stu-id="05af5-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05af5-104">Diese Prozedur zeigt Ihnen Schritt für Schritt, wie Sie Intrastat-Parameter einrichten und Transaktionen nach Intrastat übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="05af5-105">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="05af5-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="05af5-106">Erstellen Sie einen neuen und aktualisieren Sie einen vorhandenen Warencode</span><span class="sxs-lookup"><span data-stu-id="05af5-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="05af5-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Einrichtung" > "Kategorien und Attribute" > "Kategorienhierarchie".</span><span class="sxs-lookup"><span data-stu-id="05af5-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="05af5-108">Suchen Sie in der Liste den Datensatz "Intrastat-Warencodes" oder wählen Sie diesen aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="05af5-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05af5-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="05af5-110">Wählen Sie in der Struktur "einen Datensatz" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="05af5-111">Wählen Sie beispielsweise "Intrastat\Lautsprecher" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="05af5-112">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="05af5-112">Click Edit.</span></span>
6. <span data-ttu-id="05af5-113">Erweitern Sie den Abschnitt "Außenhandel".</span><span class="sxs-lookup"><span data-stu-id="05af5-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="05af5-114">Geben Sie im Feld "Besondere Maßeinheit" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-115">Wählen Sie beispielsweise "Stck." aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="05af5-116">Wählen Sie "Ja" im Feld "Gewicht nicht anwendbar" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="05af5-117">Wählen Sie in der Struktur "Intrastat" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="05af5-118">Klicken Sie auf Neuer Kategorieknoten.</span><span class="sxs-lookup"><span data-stu-id="05af5-118">Click New category node.</span></span>
11. <span data-ttu-id="05af5-119">Geben Sie im Feld "Name" den Namen der Ware ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="05af5-120">Geben Sie beispielsweise "Andere Ware" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="05af5-121">Geben Sie im Feld "Code" den Warencode ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="05af5-122">Geben Sie beispielsweise "995 00 00" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="05af5-123">Geben Sie im Feld "Anzeigename" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="05af5-124">Geben Sie beispielsweise "Sonstige" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="05af5-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05af5-125">Click Save.</span></span>
15. <span data-ttu-id="05af5-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05af5-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="05af5-127">Weisen Sie Warencode zur Produkthierarchie und zum freigegebenen Produkt zu</span><span class="sxs-lookup"><span data-stu-id="05af5-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="05af5-128">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="05af5-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="05af5-129">Filtern Sie beispielsweise nach dem Feld "Name" mit einem Wert von "Vertrieb".</span><span class="sxs-lookup"><span data-stu-id="05af5-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="05af5-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="05af5-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="05af5-131">Erweitern Sie "einen Kategorieknoten" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="05af5-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="05af5-132">Erweitern Sie beispielsweise "Vertriebshierarchie\Audiogeräte für Zuhause".</span><span class="sxs-lookup"><span data-stu-id="05af5-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="05af5-133">Wählen Sie in der Struktur "die Kategorie aus, die dem Warencode zugewiesen werden soll".</span><span class="sxs-lookup"><span data-stu-id="05af5-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="05af5-134">Wählen Sie beispielsweise "Vertriebshierarchie\Audiogeräte für Zuhause\Lautsprecher" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="05af5-135">Erweitern Sie den Abschnitt "Warencodes".</span><span class="sxs-lookup"><span data-stu-id="05af5-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="05af5-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="05af5-136">Click Add.</span></span>
7. <span data-ttu-id="05af5-137">Wählen Sie im Feld "Hierarchie auswählen" die Option "Intrastat" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="05af5-138">Suchen Sie in der Liste den Warencode und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="05af5-139">Wählen Sie beispielsweise "920 20 34 Lautsprecher" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="05af5-140">Klicken Sie auf "SelectCodes".</span><span class="sxs-lookup"><span data-stu-id="05af5-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="05af5-141">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-141">Click OK.</span></span>
11. <span data-ttu-id="05af5-142">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="05af5-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="05af5-143">Wählen Sie in der Liste das freigegebene Produkt aus, das Sie dem Warencode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="05af5-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="05af5-144">Wählen Sie beispielsweise "D0001" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="05af5-145">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="05af5-145">Click Edit.</span></span>
14. <span data-ttu-id="05af5-146">Erweitern Sie den Abschnitt "Außenhandel".</span><span class="sxs-lookup"><span data-stu-id="05af5-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="05af5-147">Geben Sie im Feld "Ware" den Warencode ein</span><span class="sxs-lookup"><span data-stu-id="05af5-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="05af5-148">Wählen Sie beispielsweise den Wert "920 20 34 Lautsprecher" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="05af5-149">Geben Sie im Feld "Prozentsatz für Belastungen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="05af5-150">Geben Sie beispielsweise "3" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="05af5-151">Geben Sie im Feld "Land/Region" ein Ursprungsland oder -region ein oder wählen Sie diese aus</span><span class="sxs-lookup"><span data-stu-id="05af5-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="05af5-152">Wählen Sie beispielsweise "AUT" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="05af5-153">Erweitern Sie den Abschnitt "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="05af5-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="05af5-154">Geben Sie im Feld "Nettogewicht" ein Gewicht in kg ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="05af5-155">Geben Sie beispielsweise "2,5" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="05af5-156">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05af5-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="05af5-157">Richten Sie Intrastat-Transaktionscodes und Außenhandelsparameter ein</span><span class="sxs-lookup"><span data-stu-id="05af5-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="05af5-158">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Transaktionscodes"</span><span class="sxs-lookup"><span data-stu-id="05af5-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="05af5-159">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05af5-159">Click New.</span></span>
3. <span data-ttu-id="05af5-160">Geben Sie im Feld "Transaktionscode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="05af5-161">Geben Sie beispielsweise "21" für den Transaktionscode ein, der als Rückgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05af5-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="05af5-162">Geben Sie im Feld "Name" den Namen des Transaktionscodes ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="05af5-163">Geben Sie beispielsweise "Rückgabe" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="05af5-164">Wählen Sie im Feld "Statistischer Betrag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="05af5-165">Wählen Sie beispielsweise "Leer" aus, was angibt, dass der statistische Wert, der für Transaktionen mit Transaktionscode "21" gemeldet werden soll, immer null ist.</span><span class="sxs-lookup"><span data-stu-id="05af5-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="05af5-166">Wechseln Sie zu Steuer > Einstellungen > Außenhandel > Außenhandelsparameter.</span><span class="sxs-lookup"><span data-stu-id="05af5-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="05af5-167">Geben Sie im Feld "Transaktionscode" einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-168">Wählen Sie beispielsweise "11" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="05af5-169">Geben Sie im Feld "Gutschrift" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-170">Dieser Wert identifiziert zudem die physische Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="05af5-170">This value also identifies the physical return.</span></span> <span data-ttu-id="05af5-171">Die Gutschrift für die physische Rückgabe wird in die Intrastat-Erfassung mit entgegengesetzter Richtung übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="05af5-172">Beispielsweise wird die Rückgabe des Zugangs als Versand übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="05af5-173">Andernfalls wird die Gutschrift als eine Korrektur betrachtet und wird mit der gleichen Richtung und entgegengesetztem Vorzeichen übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="05af5-174">Beispielsweise wird die Korrektur des Eingangs als Zugang mit negativem Betrag übertragen, und die aktive Markierung wird auf "Korrektur" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05af5-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="05af5-175">Erweitern Sie den Abschnitt "Übertragen".</span><span class="sxs-lookup"><span data-stu-id="05af5-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="05af5-176">Wählen Sie "Ja" im Feld "Artikel mit Warencode" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="05af5-177">Wählen Sie diese Option aus, um nur die Transaktionen mit einem zugewiesenen Warencode zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="05af5-178">Transaktionen ohne einen Warencode werden nicht an Intrastat übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="05af5-179">Im Feld "Umbuchen, wenn folgendes Kriterium erfüllt wird" wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="05af5-180">Beispielsweise wählen Sie "Einer der markierten" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="05af5-181">Erweitern Sie den Abschnitt "Warencodehierarchie".</span><span class="sxs-lookup"><span data-stu-id="05af5-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="05af5-182">Klicken Sie auf die Schaltfläche "Länder-/Regionseigenschaften".</span><span class="sxs-lookup"><span data-stu-id="05af5-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="05af5-183">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05af5-183">Click New.</span></span>
15. <span data-ttu-id="05af5-184">Wählen Sie im Feld Name/Region einen Wert aus oder geben Sie ihn ein«».</span><span class="sxs-lookup"><span data-stu-id="05af5-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-185">Beispielsweise wählen Sie den Wert "FRA" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="05af5-186">Geben Sie in das Feld "Intrastat-Code" den ISO-Code für das Land ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="05af5-187">Geben Sie beispielsweise "FR" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="05af5-188">Wählen Sie im Feld "Land/Region" 'EU'.</span><span class="sxs-lookup"><span data-stu-id="05af5-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="05af5-189">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="05af5-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="05af5-190">Richten Sie "Lieferarten" sowie Regeln zum Einschließen von Belastungen in Intrastat ein</span><span class="sxs-lookup"><span data-stu-id="05af5-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="05af5-191">Wechseln Sie zu "Vertrieb und Marketing" > "Einstellungen" > "Verteilung" > "Lieferarten"</span><span class="sxs-lookup"><span data-stu-id="05af5-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="05af5-192">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="05af5-193">Wählen Sie beispielsweise "20 Air" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="05af5-194">Erweitern Sie den Abschnitt "Außenhandel".</span><span class="sxs-lookup"><span data-stu-id="05af5-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="05af5-195">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="05af5-195">Click Edit.</span></span>
5. <span data-ttu-id="05af5-196">Geben Sie im Feld "Transport" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-197">Wählen Sie beispielsweise "02" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="05af5-198">Wechseln Sie zu "Debitoren" > "Belastungseinstellung" > "Belastungscode".</span><span class="sxs-lookup"><span data-stu-id="05af5-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="05af5-199">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="05af5-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="05af5-200">Filtern Sie beispielsweise im Feld "Belastungscode" mit einem Wert von "Fracht".</span><span class="sxs-lookup"><span data-stu-id="05af5-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="05af5-201">Erweitern Sie den Abschnitt "Außenhandel".</span><span class="sxs-lookup"><span data-stu-id="05af5-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="05af5-202">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="05af5-202">Click Edit.</span></span>
10. <span data-ttu-id="05af5-203">Wählen Sie "Ja" im Feld "Intrastat-Rechungswert" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="05af5-204">Der Betrag wird auf das Feld "Rechnungszuschläge" übertragen und wird mit dem Betrag zusammengefasst, der im Feld "Rechnungsbetrag" übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="05af5-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="05af5-205">Wählen Sie "Ja" im Feld "Statistischer Intrastat-Wert" aus, wenn der Betrag der Änderungen zum Feld "Statistische Belastungen" übertragen werden muss und mit "Statistischer Betrag" zusammengefasst werden muss.</span><span class="sxs-lookup"><span data-stu-id="05af5-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="05af5-206">Verkaufen Sie Produkte für EU-Debitoren</span><span class="sxs-lookup"><span data-stu-id="05af5-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="05af5-207">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="05af5-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="05af5-208">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05af5-208">Click New.</span></span>
3. <span data-ttu-id="05af5-209">Wählen Sie im Feld "Debitorenkonto" einen EU-Debitor aus</span><span class="sxs-lookup"><span data-stu-id="05af5-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="05af5-210">Wählen Sie beispielsweise "DE-012 Litware Einzelhandel" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="05af5-211">Erweitern Sie den Abschnitt "Lieferung".</span><span class="sxs-lookup"><span data-stu-id="05af5-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="05af5-212">Geben Sie im Feld "Lieferart" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-213">Wählen Sie beispielsweise "20 Air" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="05af5-214">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-214">Click OK.</span></span>
7. <span data-ttu-id="05af5-215">Platzieren Sie den Cursor in der ersten Zeile von Auftragspositionen.</span><span class="sxs-lookup"><span data-stu-id="05af5-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="05af5-216">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-217">Wählen Sie beispielsweise "D001" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="05af5-218">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="05af5-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="05af5-219">Klicken Sie auf die Registerkarte "Außenhandel".</span><span class="sxs-lookup"><span data-stu-id="05af5-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="05af5-220">Der Transport wird automatisch aus der ausgewählten "Lieferart" ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="05af5-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="05af5-221">Geben Sie im Feld "Hafen" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="05af5-222">Klicken Sie auf "Finanzdaten".</span><span class="sxs-lookup"><span data-stu-id="05af5-222">Click Financials.</span></span>
    * <span data-ttu-id="05af5-223">Gemäß der Einstellungen wird dieser Betrag in den Intrastat-Rechnungswert einbezogen.</span><span class="sxs-lookup"><span data-stu-id="05af5-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="05af5-224">Klicken Sie auf "Belastungen verwalten".</span><span class="sxs-lookup"><span data-stu-id="05af5-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="05af5-225">Geben Sie im Feld "Belastungscode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-226">Wählen Sie z. B. "FRACHT" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="05af5-227">Aktivieren Sie das Kontrollkästchen "Beibehalten".</span><span class="sxs-lookup"><span data-stu-id="05af5-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="05af5-228">Geben Sie im Feld "Wert der Belastungen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="05af5-229">Geben Sie beispielsweise "10" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="05af5-230">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05af5-230">Click Save.</span></span>
18. <span data-ttu-id="05af5-231">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05af5-231">Close the page.</span></span>
19. <span data-ttu-id="05af5-232">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="05af5-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="05af5-233">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="05af5-233">Click Invoice.</span></span>
21. <span data-ttu-id="05af5-234">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="05af5-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="05af5-235">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="05af5-236">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="05af5-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="05af5-237">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="05af5-238">Geben Sie beispielsweise "31.01.2015" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="05af5-239">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-239">Click OK.</span></span>
26. <span data-ttu-id="05af5-240">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-240">Click OK.</span></span>
27. <span data-ttu-id="05af5-241">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05af5-241">Close the page.</span></span>
28. <span data-ttu-id="05af5-242">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="05af5-242">Click New.</span></span>
29. <span data-ttu-id="05af5-243">Wählen Sie im Feld "Debitorenkonto" einen EU-Debitor aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="05af5-244">Wählen Sie beispielsweise "DE-013 Trey-Großhandel" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="05af5-245">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-245">Click OK.</span></span>
31. <span data-ttu-id="05af5-246">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="05af5-247">Wählen Sie beispielsweise "D0001" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="05af5-248">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="05af5-248">Click Save.</span></span>
33. <span data-ttu-id="05af5-249">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="05af5-249">Click Invoice.</span></span>
34. <span data-ttu-id="05af5-250">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="05af5-251">Geben Sie beispielsweise das Datum "31.01.2015" ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="05af5-252">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-252">Click OK.</span></span>
36. <span data-ttu-id="05af5-253">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="05af5-254">Buchungen an Intrastat übertragen</span><span class="sxs-lookup"><span data-stu-id="05af5-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="05af5-255">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="05af5-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="05af5-256">Klicken Sie auf Übertragen.</span><span class="sxs-lookup"><span data-stu-id="05af5-256">Click Transfer.</span></span>
3. <span data-ttu-id="05af5-257">Wählen Sie "Ja" im Feld "Debitorenrechnung" aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="05af5-258">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="05af5-258">Click Filter.</span></span>
5. <span data-ttu-id="05af5-259">Markieren Sie in der Liste die Zeile mit "Datum"</span><span class="sxs-lookup"><span data-stu-id="05af5-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="05af5-260">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05af5-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="05af5-261">Geben Sie beispielsweise den Filter für die Periode "Januar 2015" ein (der genaue Wert hängt von Ihrem Datumsformat ab): 01.01.2015..31.01.2015</span><span class="sxs-lookup"><span data-stu-id="05af5-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="05af5-262">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-262">Click OK.</span></span>
8. <span data-ttu-id="05af5-263">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="05af5-263">Click OK.</span></span>
9. <span data-ttu-id="05af5-264">Suchen Sie in der Liste den übertragenen Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05af5-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="05af5-265">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="05af5-265">Click the General tab.</span></span>
    * <span data-ttu-id="05af5-266">Überprüfen Sie die übertragenen Daten, einschließlich Land/Region des Ziels/der Lieferung, Ursprungsland, Gewicht, Menge, die Menge in zusätzlichen Einheiten, die Ware, der Transaktionscode, die Rechnungsbeträge und die statistischen Beträge.</span><span class="sxs-lookup"><span data-stu-id="05af5-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="05af5-267">Sie können die Daten im Bedarfsfall ändern.</span><span class="sxs-lookup"><span data-stu-id="05af5-267">You can modify data if necessary.</span></span>  


