---
title: EUR-00002 Generieren Sie eine EU-Intrastat-Meldung
description: Diese Prozedur führt Sie durch die Schritte, die erforderlich sind, um die Intrastat-Meldung im elektronischen Dateiformat zu exportieren und die Meldungsdaten in einem Excel-Format in der Vorschau anzuzeigen.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1236f27a3a5c208ffec41374a6593d1f0e7c4433
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566789"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="0ccc7-103">EUR-00002 Generieren Sie eine EU-Intrastat-Meldung</span><span class="sxs-lookup"><span data-stu-id="0ccc7-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ccc7-104">Diese Prozedur führt Sie durch die Schritte, die erforderlich sind, um die Intrastat-Meldung im elektronischen Dateiformat zu exportieren und die Meldungsdaten in einem Excel-Format in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="0ccc7-105">Bevor Sie diese Prozedur abschließen können, müssen Sie Transaktionen zum Intrastat übertragen.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="0ccc7-106">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="0ccc7-107">Importkonfigurationen mit Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0ccc7-107">Import configurations with settings</span></span>
1. <span data-ttu-id="0ccc7-108">Wechseln Sie zu "Arbeitsbereiche" > "Elektronische Berichterstellung"</span><span class="sxs-lookup"><span data-stu-id="0ccc7-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="0ccc7-109">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="0ccc7-109">Click Set active.</span></span>
3. <span data-ttu-id="0ccc7-110">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-110">Click Repositories.</span></span>
4. <span data-ttu-id="0ccc7-111">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-111">Click Open.</span></span>
5. <span data-ttu-id="0ccc7-112">Öffnen Sie den Spaltenfilter "Konfigurationsname".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="0ccc7-113">Wenden Sie einen Filter auf das Feld "Konfigurationsname" mit einem Wert von "Intrastat (DE)" unter Verwendung des Filteroperators "Beginnt mit" an.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="0ccc7-114">Sie sollten den Konfigurationsnamen auswählen, der für das Land Ihrer juristischen Person gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="0ccc7-115">Bei dieser Prozedur wird die deutsche juristische Person (DEMF) als Beispiel benutzt, daher sollte "Intrastat DE" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="0ccc7-116">Klicken Sie auf "Importieren" und klicken Sie dann auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="0ccc7-117">Öffnen Sie den Spaltenfilter "Konfigurationsname".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="0ccc7-118">Wenden Sie einen Filter auf das Feld "Konfigurationsname" mit einem Wert von "Intrastat-Bericht" unter Verwendung des Filteroperators "Beginnt mit" an.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="0ccc7-119">Klicken Sie auf "Importieren" und klicken Sie dann auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="0ccc7-120">Richten Sie Außenhandelsparameter ein</span><span class="sxs-lookup"><span data-stu-id="0ccc7-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="0ccc7-121">Wechseln Sie zu Steuer > Einstellungen > Außenhandel > Außenhandelsparameter.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="0ccc7-122">Erweitern Sie den Bereich "Elektronische Berichterstellung".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="0ccc7-123">Geben Sie im Feld "Dateiformatzuordnung" einen Wert "Intrastat (DE)" ein oder wählen Sie einen solchen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="0ccc7-124">Geben Sie im Feld "Berichtformatzuordnung" einen Wert "Intrastat-Bericht" ein oder wählen Sie einen solchen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="0ccc7-125">Erweitern Sie den Abschnitt "Rundungsregeln".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="0ccc7-126">Sie sollten Rundungsregeln einrichten, die in Ihrem Land/Ihrer Region für Intrastat-Berichte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="0ccc7-127">Geben Sie im Feld "Rundungsregel" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="0ccc7-128">Geben Sie Rundungsgenauigkeit ein, beispielsweise "0.01".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="0ccc7-129">Geben Sie im Feld "Anzahl von Dezimalen für Betrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="0ccc7-130">Geben Sie beispielsweise "2" ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="0ccc7-131">Wählen Sie im Feld "Rundung unter 1 kg" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="0ccc7-132">Beispielsweise wählen Sie "Aufrunden auf 1 kg" aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="0ccc7-133">Geben Sie im Feld "Rundungsregel" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="0ccc7-134">Geben Sie beispielsweise "1 "für das Runden des Gewichts auf die ganze Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="0ccc7-135">Erweitern Sie den Abschnitt "Untergrenze".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="0ccc7-136">Geben Sie im Feld "Gewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="0ccc7-137">Geben Sie beispielsweise "10 "als das Mindestgewicht ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="0ccc7-138">Geben Sie im Feld "Betrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="0ccc7-139">Geben Sie beispielsweise "200 "als den Mindestbetrag ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="0ccc7-140">Geben Sie im Feld "Ware" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="0ccc7-141">Richten Sie Komprimierung von Intrastat ein</span><span class="sxs-lookup"><span data-stu-id="0ccc7-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="0ccc7-142">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Komprimierung von Intrastat".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="0ccc7-143">Klicken Sie auf "Entfernen".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-143">Click Remove.</span></span>
3. <span data-ttu-id="0ccc7-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ccc7-145">Wählen Sie beispielsweise "Ware" im Abschnitt "Verfügbar" aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="0ccc7-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="0ccc7-147">Generieren Sie eine Intrastat-Meldung</span><span class="sxs-lookup"><span data-stu-id="0ccc7-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="0ccc7-148">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat"</span><span class="sxs-lookup"><span data-stu-id="0ccc7-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="0ccc7-149">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-149">Click Validate.</span></span>
    * <span data-ttu-id="0ccc7-150">Die Überprüfung erfolgt gemäß des Felds "Einstellungen prüfen" auf der Seite "Außenhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="0ccc7-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-151">Click OK.</span></span>
4. <span data-ttu-id="0ccc7-152">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-152">Click Update.</span></span>
5. <span data-ttu-id="0ccc7-153">Klicken Sie auf "Untergrenze".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="0ccc7-154">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="0ccc7-155">Geben Sie beispielsweise "1. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="0ccc7-156">Wählen Sie "Ja" im Feld "Komprimieren" aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="0ccc7-157">Geben Sie im Feld "Enddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="0ccc7-158">Geben Sie beispielsweise "31. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="0ccc7-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-159">Click OK.</span></span>
10. <span data-ttu-id="0ccc7-160">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-160">Click Update.</span></span>
11. <span data-ttu-id="0ccc7-161">Klicken Sie auf "Komprimieren".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-161">Click Compress.</span></span>
    * <span data-ttu-id="0ccc7-162">Diese Komprimierung geschieht gemäß dem, wie Sie die Komprimierung von Intrastat-Einstellungen einstellen.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="0ccc7-163">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="0ccc7-164">Geben Sie beispielsweise "1. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="0ccc7-165">Geben Sie im Feld "Enddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="0ccc7-166">Geben Sie beispielsweise "31. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="0ccc7-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-167">Click OK.</span></span>
15. <span data-ttu-id="0ccc7-168">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-168">Click Update.</span></span>
16. <span data-ttu-id="0ccc7-169">Klicken Sie auf "Sequenznummern von neuem generieren".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="0ccc7-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-170">Click OK.</span></span>
18. <span data-ttu-id="0ccc7-171">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-171">Click Output.</span></span>
19. <span data-ttu-id="0ccc7-172">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-172">Click Report.</span></span>
20. <span data-ttu-id="0ccc7-173">Geben Sie im Feld "Von Datum" das erste Datum des Berichtszeitraums ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="0ccc7-174">Legen Sie beispielsweise das Datum auf den 1. Januar 2015 fest.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="0ccc7-175">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0ccc7-176">Geben Sie beispielsweise "31. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="0ccc7-177">Wählen Sie "Ja" im Feld "Datei generieren" aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="0ccc7-178">Geben Sie im Feld "Dateiname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="0ccc7-179">Wählen Sie "Ja" im Feld "Bericht erzeugen" aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="0ccc7-180">Geben Sie im Feld "Berichtsdateiname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="0ccc7-181">Wählen Sie im Feld "Richtung" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="0ccc7-182">Wählen Sie z. B. "Versand" aus.</span><span class="sxs-lookup"><span data-stu-id="0ccc7-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="0ccc7-183">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ccc7-183">Click OK.</span></span>

