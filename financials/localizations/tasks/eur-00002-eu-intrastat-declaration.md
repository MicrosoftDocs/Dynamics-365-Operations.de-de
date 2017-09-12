--- 
title: EU-Intrastat-Meldung generieren
description: "Diese Prozedur führt Sie durch die Schritte, die erforderlich sind, um die Intrastat-Meldung im elektronischen Dateiformat zu exportieren und die Meldungsdaten in einem Excel-Format in der Vorschau anzuzeigen."
author: Anasyash
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f74da78232c477224c8fa753e9755b7f9d13174d
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="generate-an-eu-intrastat-declaration"></a><span data-ttu-id="90bd0-103">EU-Intrastat-Meldung generieren</span><span class="sxs-lookup"><span data-stu-id="90bd0-103">Generate an EU Intrastat declaration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90bd0-104">Diese Prozedur führt Sie durch die Schritte, die erforderlich sind, um die Intrastat-Meldung im elektronischen Dateiformat zu exportieren und die Meldungsdaten in einem Excel-Format in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="90bd0-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="90bd0-105">Bevor Sie diese Prozedur abschließen können, müssen Sie Transaktionen zum Intrastat übertragen.</span><span class="sxs-lookup"><span data-stu-id="90bd0-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="90bd0-106">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="90bd0-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="90bd0-107">Importkonfigurationen mit Einstellungen</span><span class="sxs-lookup"><span data-stu-id="90bd0-107">Import configurations with settings</span></span>
1. <span data-ttu-id="90bd0-108">Wechseln Sie zu "Arbeitsbereiche" > "Elektronische Berichterstellung"</span><span class="sxs-lookup"><span data-stu-id="90bd0-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="90bd0-109">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="90bd0-109">Click Set active.</span></span>
3. <span data-ttu-id="90bd0-110">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="90bd0-110">Click Repositories.</span></span>
4. <span data-ttu-id="90bd0-111">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="90bd0-111">Click Open.</span></span>
5. <span data-ttu-id="90bd0-112">Öffnen Sie den Spaltenfilter "Konfigurationsname".</span><span class="sxs-lookup"><span data-stu-id="90bd0-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="90bd0-113">Wenden Sie einen Filter auf das Feld "Konfigurationsname" mit einem Wert von "Intrastat (DE)" unter Verwendung des Filteroperators "Beginnt mit" an.</span><span class="sxs-lookup"><span data-stu-id="90bd0-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="90bd0-114">Sie sollten den Konfigurationsnamen auswählen, der für das Land Ihrer juristischen Person gültig ist.</span><span class="sxs-lookup"><span data-stu-id="90bd0-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="90bd0-115">Bei dieser Prozedur wird die deutsche juristische Person (DEMF) als Beispiel benutzt, daher sollte "Intrastat DE" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="90bd0-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="90bd0-116">Klicken Sie auf "Importieren" und klicken Sie dann auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="90bd0-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="90bd0-117">Öffnen Sie den Spaltenfilter "Konfigurationsname".</span><span class="sxs-lookup"><span data-stu-id="90bd0-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="90bd0-118">Wenden Sie einen Filter auf das Feld "Konfigurationsname" mit einem Wert von "Intrastat-Bericht" unter Verwendung des Filteroperators "Beginnt mit" an.</span><span class="sxs-lookup"><span data-stu-id="90bd0-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="90bd0-119">Klicken Sie auf "Importieren" und klicken Sie dann auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="90bd0-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="90bd0-120">Richten Sie Außenhandelsparameter ein</span><span class="sxs-lookup"><span data-stu-id="90bd0-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="90bd0-121">Wechseln Sie zu Steuer > Einstellungen > Außenhandel > Außenhandelsparameter.</span><span class="sxs-lookup"><span data-stu-id="90bd0-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="90bd0-122">Erweitern Sie den Bereich "Elektronische Berichterstellung".</span><span class="sxs-lookup"><span data-stu-id="90bd0-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="90bd0-123">Geben Sie im Feld "Dateiformatzuordnung" einen Wert "Intrastat (DE)" ein oder wählen Sie einen solchen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="90bd0-124">Geben Sie im Feld "Berichtformatzuordnung" einen Wert "Intrastat-Bericht" ein oder wählen Sie einen solchen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="90bd0-125">Erweitern Sie den Abschnitt "Rundungsregeln".</span><span class="sxs-lookup"><span data-stu-id="90bd0-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="90bd0-126">Sie sollten Rundungsregeln einrichten, die in Ihrem Land/Ihrer Region für Intrastat-Berichte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="90bd0-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="90bd0-127">Geben Sie im Feld "Rundungsregel" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="90bd0-128">Geben Sie Rundungsgenauigkeit ein, beispielsweise "0.01".</span><span class="sxs-lookup"><span data-stu-id="90bd0-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="90bd0-129">Geben Sie im Feld "Anzahl von Dezimalen für Betrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="90bd0-130">Geben Sie beispielsweise "2" ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="90bd0-131">Wählen Sie im Feld "Rundung unter 1 kg" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="90bd0-132">Beispielsweise wählen Sie "Aufrunden auf 1 kg" aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="90bd0-133">Geben Sie im Feld "Rundungsregel" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="90bd0-134">Geben Sie beispielsweise "1 "für das Runden des Gewichts auf die ganze Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="90bd0-135">Erweitern Sie den Abschnitt "Untergrenze".</span><span class="sxs-lookup"><span data-stu-id="90bd0-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="90bd0-136">Geben Sie im Feld "Gewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="90bd0-137">Geben Sie beispielsweise "10 "als das Mindestgewicht ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="90bd0-138">Geben Sie im Feld "Betrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="90bd0-139">Geben Sie beispielsweise "200 "als den Mindestbetrag ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="90bd0-140">Geben Sie im Feld "Ware" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="90bd0-141">Richten Sie Komprimierung von Intrastat ein</span><span class="sxs-lookup"><span data-stu-id="90bd0-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="90bd0-142">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Komprimierung von Intrastat".</span><span class="sxs-lookup"><span data-stu-id="90bd0-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="90bd0-143">Klicken Sie auf "Entfernen".</span><span class="sxs-lookup"><span data-stu-id="90bd0-143">Click Remove.</span></span>
3. <span data-ttu-id="90bd0-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90bd0-145">Wählen Sie beispielsweise "Ware" im Abschnitt "Verfügbar" aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="90bd0-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="90bd0-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="90bd0-147">Generieren Sie eine Intrastat-Meldung</span><span class="sxs-lookup"><span data-stu-id="90bd0-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="90bd0-148">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat"</span><span class="sxs-lookup"><span data-stu-id="90bd0-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="90bd0-149">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="90bd0-149">Click Validate.</span></span>
    * <span data-ttu-id="90bd0-150">Die Überprüfung erfolgt gemäß des Felds "Einstellungen prüfen" auf der Seite "Außenhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="90bd0-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="90bd0-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="90bd0-151">Click OK.</span></span>
4. <span data-ttu-id="90bd0-152">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="90bd0-152">Click Update.</span></span>
5. <span data-ttu-id="90bd0-153">Klicken Sie auf "Untergrenze".</span><span class="sxs-lookup"><span data-stu-id="90bd0-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="90bd0-154">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="90bd0-155">Geben Sie beispielsweise "1. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="90bd0-156">Wählen Sie "Ja" im Feld "Komprimieren" aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="90bd0-157">Geben Sie im Feld "Enddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="90bd0-158">Geben Sie beispielsweise "31. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="90bd0-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="90bd0-159">Click OK.</span></span>
10. <span data-ttu-id="90bd0-160">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="90bd0-160">Click Update.</span></span>
11. <span data-ttu-id="90bd0-161">Klicken Sie auf "Komprimieren".</span><span class="sxs-lookup"><span data-stu-id="90bd0-161">Click Compress.</span></span>
    * <span data-ttu-id="90bd0-162">Diese Komprimierung geschieht gemäß dem, wie Sie die Komprimierung von Intrastat-Einstellungen einstellen.</span><span class="sxs-lookup"><span data-stu-id="90bd0-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="90bd0-163">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="90bd0-164">Geben Sie beispielsweise "1. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="90bd0-165">Geben Sie im Feld "Enddatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="90bd0-166">Geben Sie beispielsweise "31. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="90bd0-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="90bd0-167">Click OK.</span></span>
15. <span data-ttu-id="90bd0-168">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="90bd0-168">Click Update.</span></span>
16. <span data-ttu-id="90bd0-169">Klicken Sie auf "Sequenznummern von neuem generieren".</span><span class="sxs-lookup"><span data-stu-id="90bd0-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="90bd0-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="90bd0-170">Click OK.</span></span>
18. <span data-ttu-id="90bd0-171">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="90bd0-171">Click Output.</span></span>
19. <span data-ttu-id="90bd0-172">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="90bd0-172">Click Report.</span></span>
20. <span data-ttu-id="90bd0-173">Geben Sie im Feld "Von Datum" das erste Datum des Berichtszeitraums ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="90bd0-174">Legen Sie beispielsweise das Datum auf den 1. Januar 2015 fest.</span><span class="sxs-lookup"><span data-stu-id="90bd0-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="90bd0-175">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="90bd0-176">Geben Sie beispielsweise "31. Januar, 2015" ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="90bd0-177">Wählen Sie "Ja" im Feld "Datei generieren" aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="90bd0-178">Geben Sie im Feld "Dateiname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="90bd0-179">Wählen Sie "Ja" im Feld "Bericht erzeugen" aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="90bd0-180">Geben Sie im Feld "Berichtsdateiname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="90bd0-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="90bd0-181">Wählen Sie im Feld "Richtung" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="90bd0-182">Wählen Sie z. B. "Versand" aus.</span><span class="sxs-lookup"><span data-stu-id="90bd0-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="90bd0-183">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="90bd0-183">Click OK.</span></span>


