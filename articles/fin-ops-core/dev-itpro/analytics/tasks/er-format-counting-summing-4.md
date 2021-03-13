---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 4: Format ausführen)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat für das Zählen und Summieren basierend auf Daten der bereits generierten Textausgabe konfigurieren. (Teil 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092946"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="8c615-104">ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 4: Format ausführen)</span><span class="sxs-lookup"><span data-stu-id="8c615-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c615-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="8c615-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="8c615-106">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c615-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="8c615-107">Um diese Schritte auszuführent, müssen Sie erst die Schritte im Aufgabenleitfaden ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 3: Nutzung von Berechnungen für Ausgaben) ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c615-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="8c615-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c615-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="8c615-109">Testen Sie diese zur Konfiguration zur Generierung von Intrastat-Berichten.</span><span class="sxs-lookup"><span data-stu-id="8c615-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="8c615-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="8c615-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8c615-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="8c615-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8c615-112">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="8c615-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="8c615-113">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="8c615-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="8c615-114">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="8c615-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="8c615-115">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c615-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="8c615-116">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="8c615-116">Click User parameters.</span></span>
8. <span data-ttu-id="8c615-117">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="8c615-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="8c615-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c615-118">Click OK.</span></span>
10. <span data-ttu-id="8c615-119">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8c615-119">Click Edit.</span></span>
11. <span data-ttu-id="8c615-120">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="8c615-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="8c615-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8c615-121">Click Save.</span></span>
13. <span data-ttu-id="8c615-122">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="8c615-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="8c615-123">Erweitern Sie den Bereich "Elektronische Berichterstellung".</span><span class="sxs-lookup"><span data-stu-id="8c615-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="8c615-124">Wählen Sie die Konfiguration Intrastat (DE) mit Berechnungs- und Summierungs-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c615-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="8c615-125">Wählen Sie die Konfiguration Intrastat (DE) mit Berechnungs- und Summierungs-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c615-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="8c615-126">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="8c615-126">Click Save.</span></span>
18. <span data-ttu-id="8c615-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c615-127">Close the page.</span></span>
19. <span data-ttu-id="8c615-128">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="8c615-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="8c615-129">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="8c615-129">Click Output.</span></span>
21. <span data-ttu-id="8c615-130">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="8c615-130">Click Report.</span></span>
    * <span data-ttu-id="8c615-131">Führen Sie den Intrastat-Bericht-Generierungsprozess aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="8c615-132">Legen Sie das Datum "2000-01-01" im Feld "Von Datum" fest.</span><span class="sxs-lookup"><span data-stu-id="8c615-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="8c615-133">Definieren Sie Start- und Enddaten für den Berichtszeitraum, die die vorhandenen Formularbuchungen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="8c615-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="8c615-134">Legen Sie das Datum "2022-12-31" im Feld "Bis Datum" fest.</span><span class="sxs-lookup"><span data-stu-id="8c615-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="8c615-135">Definieren Sie Start- und Enddaten für den Berichtszeitraum, die die vorhandenen Formularbuchungen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="8c615-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="8c615-136">Wählen Sie im Feld "Richtung" "Empfang" aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="8c615-137">Wählen Sie "Ja" im Feld "Datei generieren" aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="8c615-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c615-138">Click OK.</span></span>
    * <span data-ttu-id="8c615-139">Prüfen Sie die erstellten Ausgaben über die zusammengefassten Positionen am Ende.</span><span class="sxs-lookup"><span data-stu-id="8c615-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="8c615-140">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8c615-140">Click New.</span></span>
28. <span data-ttu-id="8c615-141">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8c615-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="8c615-142">Wählen Sie im Feld "Richtung" "Versand" aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="8c615-143">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="8c615-144">Geben Sie im Feld "Ware" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="8c615-145">Legen Sie "Gewicht" auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="8c615-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="8c615-146">Legen Sie "Rechnungsbetrag" auf "10000" fest.</span><span class="sxs-lookup"><span data-stu-id="8c615-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="8c615-147">Legen Sie "Statistikbetrag" auf "10000" fest.</span><span class="sxs-lookup"><span data-stu-id="8c615-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="8c615-148">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="8c615-148">Click Output.</span></span>
36. <span data-ttu-id="8c615-149">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="8c615-149">Click Report.</span></span>
37. <span data-ttu-id="8c615-150">Wählen Sie im Feld "Richtung" "Versand" aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="8c615-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c615-151">Click OK.</span></span>
    * <span data-ttu-id="8c615-152">Prüfen Sie die erstellten Ausgaben über die zusammengefassten Positionen am Ende.</span><span class="sxs-lookup"><span data-stu-id="8c615-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="8c615-153">Beachten Sie, dass er sich im Vergleich zu dem ersten Durchlauf geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8c615-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="8c615-154">Führen Sie diese Konfiguration im Debugmodus aus, um die gesammelten Zählungs- und Summierungsdaten zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="8c615-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="8c615-155">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c615-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8c615-156">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="8c615-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="8c615-157">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="8c615-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="8c615-158">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="8c615-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="8c615-159">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c615-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="8c615-160">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="8c615-160">Click User parameters.</span></span>
7. <span data-ttu-id="8c615-161">Wählen Sie "Ja" im Feld "Im Debugmodus ausführen" aus.</span><span class="sxs-lookup"><span data-stu-id="8c615-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="8c615-162">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c615-162">Click OK.</span></span>
9. <span data-ttu-id="8c615-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c615-163">Close the page.</span></span>
10. <span data-ttu-id="8c615-164">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="8c615-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="8c615-165">Klicken Sie auf "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="8c615-165">Click Output.</span></span>
12. <span data-ttu-id="8c615-166">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="8c615-166">Click Report.</span></span>
13. <span data-ttu-id="8c615-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c615-167">Click OK.</span></span>
14. <span data-ttu-id="8c615-168">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c615-168">Close the page.</span></span>
15. <span data-ttu-id="8c615-169">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c615-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="8c615-170">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="8c615-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="8c615-171">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="8c615-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="8c615-172">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="8c615-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="8c615-173">Klicken Sie auf Debugprotokolle.</span><span class="sxs-lookup"><span data-stu-id="8c615-173">Click Debug logs.</span></span>
    * <span data-ttu-id="8c615-174">Beachten Sie, dass ein debuggensprotokolldatensatz für den Ausführungsprozess der ausgewählten Konfiguration erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c615-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="8c615-175">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="8c615-175">Click Attach.</span></span>
21. <span data-ttu-id="8c615-176">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="8c615-176">Click Open.</span></span>
    * <span data-ttu-id="8c615-177">Prüfen Sie die erstellte XML-Datei, die die Inventur- und Zusammenfassungsdetails enthält, die bei der Ausführung der ausgewählten Konfiguration gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="8c615-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

