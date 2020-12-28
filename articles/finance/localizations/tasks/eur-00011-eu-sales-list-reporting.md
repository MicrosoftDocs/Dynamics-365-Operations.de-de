---
title: EUR-00011 Zusammenfassende Meldung einrichten
description: Diese Aufgabe führt Sie durch einen Überblick über die Voraussetzungen, die für zusammenfassende Meldungen erforderlich sind.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c312e14247c42acd5e0de5df02833275d9e3a4f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407729"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="41884-103">EUR-00011 Zusammenfassende Meldung einrichten</span><span class="sxs-lookup"><span data-stu-id="41884-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41884-104">Diese Aufgabe führt Sie durch einen Überblick über die Voraussetzungen, die für zusammenfassende Meldungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="41884-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="41884-105">Weitere Informationen über zusammenfassende Meldungen, einschließlich erforderliche Voraussetzungen, finden Sie in der Hilfe.</span><span class="sxs-lookup"><span data-stu-id="41884-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="41884-106">Diese Aufgabe gilt für alle europäischen Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="41884-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="41884-107">Das Handbuch wurde mithilfe des Demodatenunternehmens DEMF und folglich Deutschland als Exemplarinlandsland/region erstellt.</span><span class="sxs-lookup"><span data-stu-id="41884-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="41884-108">Das Handbuch verwendet ebenfalls Portugal als Exemplar EU-Land/Region.</span><span class="sxs-lookup"><span data-stu-id="41884-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="41884-109">Diese Aufgaben richten sich an Systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="41884-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="41884-110">Elektronische Berichterstellungskonfigurationen für zusammenfassende Meldungen importieren</span><span class="sxs-lookup"><span data-stu-id="41884-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="41884-111">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="41884-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="41884-112">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="41884-112">Click Set active.</span></span>
3. <span data-ttu-id="41884-113">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="41884-113">Click Repositories.</span></span>
4. <span data-ttu-id="41884-114">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="41884-114">Click Open.</span></span>
5. <span data-ttu-id="41884-115">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="41884-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="41884-116">Klicken Sie auf "Erweitertes Filtern/Sortieren".</span><span class="sxs-lookup"><span data-stu-id="41884-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="41884-117">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="41884-117">Click Add.</span></span>
8. <span data-ttu-id="41884-118">Wählen Sie im Feld "Feld" "Konfigurationsname" aus.</span><span class="sxs-lookup"><span data-stu-id="41884-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="41884-119">Geben Sie im Feld "Kriterien""Zusammenfassende Meldung (DE)" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="41884-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="41884-120">Click OK.</span></span>
11. <span data-ttu-id="41884-121">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="41884-121">Click Import.</span></span>
12. <span data-ttu-id="41884-122">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="41884-122">Click Yes.</span></span>
13. <span data-ttu-id="41884-123">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="41884-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="41884-124">Klicken Sie auf "Erweitertes Filtern/Sortieren".</span><span class="sxs-lookup"><span data-stu-id="41884-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="41884-125">Klicken Sie auf 'Zurücksetzen'.</span><span class="sxs-lookup"><span data-stu-id="41884-125">Click Reset.</span></span>
16. <span data-ttu-id="41884-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="41884-126">Click Add.</span></span>
17. <span data-ttu-id="41884-127">Wählen Sie im Feld "Feld" "Konfigurationsname" aus.</span><span class="sxs-lookup"><span data-stu-id="41884-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="41884-128">Geben Sie im Feld "Kriterien""Zusammenfassende Meldung nach Zeilen anzeigen" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="41884-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="41884-129">Click OK.</span></span>
20. <span data-ttu-id="41884-130">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="41884-130">Click Import.</span></span>
21. <span data-ttu-id="41884-131">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="41884-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="41884-132">Mehrwertsteuercodes für zusammenfassende Meldungen einrichten</span><span class="sxs-lookup"><span data-stu-id="41884-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="41884-133">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuercodes".</span><span class="sxs-lookup"><span data-stu-id="41884-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="41884-134">Verwenden Sie den Schnellfilter, um im Feld "Mehrwertsteuercode" nach dem Wert 'VAT19' zu filtern.</span><span class="sxs-lookup"><span data-stu-id="41884-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="41884-135">Erweitern Sie den Abschnitt "Berichtseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="41884-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="41884-136">Überprüfen Sie, ob die Auswahl "Ausgeschlossen" auf "Nein" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="41884-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="41884-137">Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um diese Einstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="41884-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="41884-138">Mehrwertsteuergruppen für zusammenfassende Meldungen einrichten</span><span class="sxs-lookup"><span data-stu-id="41884-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="41884-139">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuergruppen".</span><span class="sxs-lookup"><span data-stu-id="41884-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="41884-140">Verwenden Sie den Schnellfilter, um im Feld "Mehrwertsteuergruppe" nach dem Wert 'AR-DOM' zu filtern.</span><span class="sxs-lookup"><span data-stu-id="41884-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="41884-141">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="41884-141">Click Edit.</span></span>
4. <span data-ttu-id="41884-142">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="41884-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="41884-143">Markieren Sie in der Liste die erste Zeile.</span><span class="sxs-lookup"><span data-stu-id="41884-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="41884-144">Aktivieren Sie das Kontrollkästchen "Befreit".</span><span class="sxs-lookup"><span data-stu-id="41884-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="41884-145">Markieren Sie in der Liste die zweite Zeile.</span><span class="sxs-lookup"><span data-stu-id="41884-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="41884-146">Aktivieren Sie das Kontrollkästchen "Befreit".</span><span class="sxs-lookup"><span data-stu-id="41884-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="41884-147">Markieren Sie in der Liste die dritte Zeile.</span><span class="sxs-lookup"><span data-stu-id="41884-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="41884-148">Aktivieren Sie das Kontrollkästchen "Befreit".</span><span class="sxs-lookup"><span data-stu-id="41884-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="41884-149">Artikel-Mehrwertsteuergruppen für zusammenfassende Meldungen einrichten</span><span class="sxs-lookup"><span data-stu-id="41884-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="41884-150">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Artikel-Mehrwertsteuergruppen".</span><span class="sxs-lookup"><span data-stu-id="41884-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="41884-151">Verwenden Sie den Schnellfilter, um im Feld "Artikel-Mehrwertsteuergruppe" nach dem Wert 'FULL' zu filtern.</span><span class="sxs-lookup"><span data-stu-id="41884-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="41884-152">Überprüfen Sie, ob die Auswahl "Berichtstyp" auf "Artikel" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="41884-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="41884-153">Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um den Wert für dieses Feld zu ändern.</span><span class="sxs-lookup"><span data-stu-id="41884-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="41884-154">Verwenden Sie den Schnellfilter, um im Feld "Artikel-Mehrwertsteuergruppe" nach dem Wert 'RED' zu filtern.</span><span class="sxs-lookup"><span data-stu-id="41884-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="41884-155">Überprüfen Sie, ob die Auswahl "Berichtstyp" auf "Dienstleistung" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="41884-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="41884-156">Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um den Wert für dieses Feld zu ändern.</span><span class="sxs-lookup"><span data-stu-id="41884-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="41884-157">Länder-/Regionsparameter für zusammenfassende Meldungen einrichten</span><span class="sxs-lookup"><span data-stu-id="41884-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="41884-158">Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Länder-/Regionsparameter".</span><span class="sxs-lookup"><span data-stu-id="41884-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="41884-159">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41884-159">Click New.</span></span>
3. <span data-ttu-id="41884-160">Geben Sie im Feld "Land/Region" "PRT" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="41884-161">Geben Sie im Feld "Mehrwertsteuer" "PT" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="41884-162">Umsatzsteuernummern erstellen</span><span class="sxs-lookup"><span data-stu-id="41884-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="41884-163">Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "USt-IdNr.".</span><span class="sxs-lookup"><span data-stu-id="41884-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="41884-164">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41884-164">Click New.</span></span>
3. <span data-ttu-id="41884-165">Geben Sie im Feld "Land/Region" "PRT" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="41884-166">Geben Sie im Feld "USt-IdNr." die Zeichenfolge "PT12345" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="41884-167">Parameter für Zusammenfassende Meldung einrichten</span><span class="sxs-lookup"><span data-stu-id="41884-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="41884-168">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="41884-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="41884-169">Klicken Sie auf die Registerkarte "Zusammenfassenden Meldung".</span><span class="sxs-lookup"><span data-stu-id="41884-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="41884-170">Wählen Sie "Ja" im Feld "Einkäufe übertragen"aus.</span><span class="sxs-lookup"><span data-stu-id="41884-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="41884-171">Erweitern Sie den Abschnitt "Rundungsregeln".</span><span class="sxs-lookup"><span data-stu-id="41884-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="41884-172">Legen Sie die Rundungsregel auf "0,1" fest.</span><span class="sxs-lookup"><span data-stu-id="41884-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="41884-173">Wählen Sie "Ja" im Feld "Mindestwert verwenden".</span><span class="sxs-lookup"><span data-stu-id="41884-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="41884-174">Geben Sie im Feld "Dezimalstellen '2' ein.</span><span class="sxs-lookup"><span data-stu-id="41884-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="41884-175">Erweitern Sie den Bereich "Elektronische Berichterstellung".</span><span class="sxs-lookup"><span data-stu-id="41884-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="41884-176">Wählen Sie im Feld "Dateiformatzuordnung" "Zusammenfassende Meldung (DE)"aus.</span><span class="sxs-lookup"><span data-stu-id="41884-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="41884-177">Geben Sie im Feld "Berichtformatzuordnung" "Zusammenfassende Meldung nach Zeilen anzeigen" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="41884-178">Klicken Sie auf die Schaltfläche "Länder-/Regionseigenschaften".</span><span class="sxs-lookup"><span data-stu-id="41884-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="41884-179">Vergewissern Sie sich, dass das Feld "Länder-/Regionsart" auf "Inland" für Land/Region DEU ist.</span><span class="sxs-lookup"><span data-stu-id="41884-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="41884-180">Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um den Wert für dieses Feld zu ändern.</span><span class="sxs-lookup"><span data-stu-id="41884-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="41884-181">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41884-181">Click New.</span></span>
13. <span data-ttu-id="41884-182">Geben Sie im Feld "Land/Region" "PRT" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="41884-183">Geben Sie im Feld "Intrastat-Code" "PT" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="41884-184">Wählen Sie im Feld "Land/Region" 'EU'.</span><span class="sxs-lookup"><span data-stu-id="41884-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="41884-185">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="41884-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="41884-186">Überprüfen Sie, dass ein Nummernkreis für die Referenz "Zusammenfassende Meldung" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="41884-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="41884-187">Einen Debitor für Demozwecke der zusammenfassenden Meldungen erstellen</span><span class="sxs-lookup"><span data-stu-id="41884-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="41884-188">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="41884-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="41884-189">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="41884-189">Click New.</span></span>
3. <span data-ttu-id="41884-190">Geben Sie im Feld "Debitorenkonto" den Wert 'PRT-001' ein.</span><span class="sxs-lookup"><span data-stu-id="41884-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="41884-191">Geben Sie im Feld "Name" "Debitor aus Portugal" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="41884-192">Wählen Sie im Feld "Debitorengruppe" "10" aus.</span><span class="sxs-lookup"><span data-stu-id="41884-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="41884-193">Wählen Sie im Feld "Mehrwertsteuergruppe" "AR-DOM" aus.</span><span class="sxs-lookup"><span data-stu-id="41884-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="41884-194">Wählen Sie im Feld "USt-IdNr." die Zeichenfolge "PT12345".</span><span class="sxs-lookup"><span data-stu-id="41884-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="41884-195">Geben Sie im Feld "Land/Region" "PRT" ein.</span><span class="sxs-lookup"><span data-stu-id="41884-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="41884-196">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="41884-196">Click Save.</span></span>

