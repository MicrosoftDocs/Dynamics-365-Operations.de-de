--- 
title: "Ausführen des Formats zum Zählen und Summieren"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e3569e48bcc063b2423a60038732e8e53dbea2cb
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="run-the-format-to-do-counting-and-summing"></a><span data-ttu-id="c8e0c-103">Ausführen des Formats zum Zählen und Summieren</span><span class="sxs-lookup"><span data-stu-id="c8e0c-103">Run the format to do counting and summing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8e0c-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c8e0c-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c8e0c-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 3: Nutzung von Berechnungen für Ausgaben)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="c8e0c-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="c8e0c-108">Testen Sie diese zur Konfiguration zur Generierung von Intrastat-Berichten.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="c8e0c-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c8e0c-110">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c8e0c-111">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="c8e0c-112">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="c8e0c-113">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="c8e0c-114">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="c8e0c-115">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-115">Click User parameters.</span></span>
8. <span data-ttu-id="c8e0c-116">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="c8e0c-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-117">Click OK.</span></span>
10. <span data-ttu-id="c8e0c-118">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-118">Click Edit.</span></span>
11. <span data-ttu-id="c8e0c-119">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="c8e0c-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-120">Click Save.</span></span>
13. <span data-ttu-id="c8e0c-121">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="c8e0c-122">Erweitern Sie den Bereich "Elektronische Berichterstellung".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="c8e0c-123">Wählen Sie die Konfiguration “Intrastat (DE) mit Berechnungs- und Summierumngs"-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="c8e0c-124">Wählen Sie die Konfiguration “Intrastat (DE) mit Berechnungs- und Summierumngs"-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="c8e0c-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-125">Click Save.</span></span>
18. <span data-ttu-id="c8e0c-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-126">Close the page.</span></span>
19. <span data-ttu-id="c8e0c-127">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="c8e0c-128">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-128">Click Output.</span></span>
21. <span data-ttu-id="c8e0c-129">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-129">Click Report.</span></span>
    * <span data-ttu-id="c8e0c-130">Führen Sie den Intrastat-Bericht-Generierungsprozess aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="c8e0c-131">Legen Sie das Datum "2000-01-01" im Feld "Von Datum" fest.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="c8e0c-132">Definieren Sie Start- und Enddaten für den Berichtszeitraum, die die vorhandenen Formularbuchungen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="c8e0c-133">Legen Sie das Datum "2022-12-31" im Feld "Bis Datum" fest.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="c8e0c-134">Definieren Sie Start- und Enddaten für den Berichtszeitraum, die die vorhandenen Formularbuchungen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="c8e0c-135">Wählen Sie im Feld "Richtung" "Empfang" aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="c8e0c-136">Wählen Sie "Ja" im Feld "Datei generieren" aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="c8e0c-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-137">Click OK.</span></span>
    * <span data-ttu-id="c8e0c-138">Prüfen Sie die erstellten Ausgaben über die zusammengefassten Positionen am Ende.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="c8e0c-139">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-139">Click New.</span></span>
28. <span data-ttu-id="c8e0c-140">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="c8e0c-141">Wählen Sie im Feld "Richtung" "Versand" aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="c8e0c-142">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="c8e0c-143">Geben Sie im Feld "Ware" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="c8e0c-144">Legen Sie "Gewicht" auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="c8e0c-145">Legen Sie "Rechnungsbetrag" auf "10000" fest.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="c8e0c-146">Legen Sie "Statistikbetrag" auf "10000" fest.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="c8e0c-147">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-147">Click Output.</span></span>
36. <span data-ttu-id="c8e0c-148">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-148">Click Report.</span></span>
37. <span data-ttu-id="c8e0c-149">Wählen Sie im Feld "Richtung" "Versand" aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="c8e0c-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-150">Click OK.</span></span>
    * <span data-ttu-id="c8e0c-151">Prüfen Sie die erstellten Ausgaben über die zusammengefassten Positionen am Ende.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="c8e0c-152">Beachten Sie, dass er sich im Vergleich zu dem ersten Durchlauf geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="c8e0c-153">Führen Sie diese Konfiguration im Debugmodus aus, um die gesammelten Zählungs- und Summierungsdaten zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="c8e0c-154">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c8e0c-155">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="c8e0c-156">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="c8e0c-157">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="c8e0c-158">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="c8e0c-159">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-159">Click User parameters.</span></span>
7. <span data-ttu-id="c8e0c-160">Wählen Sie "Ja" im Feld "Im Debugmodus ausführen" aus.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="c8e0c-161">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-161">Click OK.</span></span>
9. <span data-ttu-id="c8e0c-162">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-162">Close the page.</span></span>
10. <span data-ttu-id="c8e0c-163">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="c8e0c-164">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-164">Click Output.</span></span>
12. <span data-ttu-id="c8e0c-165">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-165">Click Report.</span></span>
13. <span data-ttu-id="c8e0c-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-166">Click OK.</span></span>
14. <span data-ttu-id="c8e0c-167">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-167">Close the page.</span></span>
15. <span data-ttu-id="c8e0c-168">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="c8e0c-169">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="c8e0c-170">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="c8e0c-171">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="c8e0c-172">Klicken Sie auf Debugprotokolle.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-172">Click Debug logs.</span></span>
    * <span data-ttu-id="c8e0c-173">Beachten Sie, dass ein debuggensprotokolldatensatz für den Ausführungsprozess der ausgewählten Konfiguration erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="c8e0c-174">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-174">Click Attach.</span></span>
21. <span data-ttu-id="c8e0c-175">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="c8e0c-175">Click Open.</span></span>
    * <span data-ttu-id="c8e0c-176">Prüfen Sie die erstellte XML-Datei, die die Inventur- und Zusammenfassungsdetails enthält, die bei der Ausführung der ausgewählten Konfiguration gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="c8e0c-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


