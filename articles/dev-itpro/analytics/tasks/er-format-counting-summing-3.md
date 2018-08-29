--- 
title: "Verwenden von Berechnungen zum Generieren der Ausgabe für das Zählen und Summieren"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e09b9fc87619d87c1de0e68ff370c0d6ebe72fc8
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="use-computations-to-generate-the-output-for-counting-and-summing"></a><span data-ttu-id="81bd9-103">Verwenden von Berechnungen zum Generieren der Ausgabe für das Zählen und Summieren</span><span class="sxs-lookup"><span data-stu-id="81bd9-103">Use computations to generate the output for counting and summing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81bd9-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="81bd9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="81bd9-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="81bd9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="81bd9-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 2: Berechnungen konfigurieren)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="81bd9-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="81bd9-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="81bd9-108">Konfigurieren Sie diesen Bericht für Inventarisierungs- und Zusammenfassungsinformationen</span><span class="sxs-lookup"><span data-stu-id="81bd9-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="81bd9-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="81bd9-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="81bd9-110">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="81bd9-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="81bd9-111">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="81bd9-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="81bd9-112">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="81bd9-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="81bd9-113">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="81bd9-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="81bd9-114">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="81bd9-114">Click Designer.</span></span>
7. <span data-ttu-id="81bd9-115">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="81bd9-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="81bd9-116">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="81bd9-117">Fügen Sie eine neue Datenquelle hinzu, um die Liste der gemerkten Blöcken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="81bd9-118">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="81bd9-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="81bd9-119">Geben Sie im Feld "Name" "$BlocksList" ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="81bd9-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="81bd9-120">$BlocksList</span></span>  
11. <span data-ttu-id="81bd9-121">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="81bd9-121">Click Edit formula.</span></span>
12. <span data-ttu-id="81bd9-122">Wählen Sie in der Strukturdarstellung 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="81bd9-123">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-123">Click Add function.</span></span>
14. <span data-ttu-id="81bd9-124">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-124">Click Add data source.</span></span>
15. <span data-ttu-id="81bd9-125">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', ' ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="81bd9-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="81bd9-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="81bd9-127">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', "\*")' ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="81bd9-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="81bd9-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="81bd9-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81bd9-129">Click Save.</span></span>
    * <span data-ttu-id="81bd9-130">Das Muster "\*" bedeutet, dass alle Blöcke der Liste für diesen Datensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="81bd9-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="81bd9-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81bd9-131">Close the page.</span></span>
19. <span data-ttu-id="81bd9-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81bd9-132">Click OK.</span></span>
20. <span data-ttu-id="81bd9-133">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-133">Click the Format tab.</span></span>
21. <span data-ttu-id="81bd9-134">Wählen Sie in der Struktur "Intrastat\Data" aus.</span><span class="sxs-lookup"><span data-stu-id="81bd9-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="81bd9-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="81bd9-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="81bd9-136">Wählen Sie in der Struktur 'Text\Sequence'..</span><span class="sxs-lookup"><span data-stu-id="81bd9-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="81bd9-137">Geben Sie im Feld "Name" die Zeichenfolge "Summen nach Blöcken' ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="81bd9-138">Summen nach Blöcken</span><span class="sxs-lookup"><span data-stu-id="81bd9-138">Totals by blocks</span></span>  
25. <span data-ttu-id="81bd9-139">Wählen Sie im Feld "Sonderzeichen" "Neue Zeile - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="81bd9-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="81bd9-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81bd9-140">Click OK.</span></span>
27. <span data-ttu-id="81bd9-141">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="81bd9-142">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="81bd9-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="81bd9-143">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="81bd9-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="81bd9-144">Geben Sie im Feld "Name" "Block code" ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="81bd9-145">Blockcode</span><span class="sxs-lookup"><span data-stu-id="81bd9-145">Block code</span></span>  
31. <span data-ttu-id="81bd9-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81bd9-146">Click OK.</span></span>
32. <span data-ttu-id="81bd9-147">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="81bd9-147">Click Add String.</span></span>
33. <span data-ttu-id="81bd9-148">Geben Sie im Feld "Name" 'Lines counting' ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="81bd9-149">Inventarisierte Positionen</span><span class="sxs-lookup"><span data-stu-id="81bd9-149">Lines counting</span></span>  
34. <span data-ttu-id="81bd9-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81bd9-150">Click OK.</span></span>
35. <span data-ttu-id="81bd9-151">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="81bd9-151">Click Add String.</span></span>
36. <span data-ttu-id="81bd9-152">Geben Sie im Feld Name "Total amount" ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="81bd9-153">Gesamtstundenzahl</span><span class="sxs-lookup"><span data-stu-id="81bd9-153">Total amount</span></span>  
37. <span data-ttu-id="81bd9-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81bd9-154">Click OK.</span></span>
38. <span data-ttu-id="81bd9-155">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="81bd9-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="81bd9-156">Wählen Sie in der Struktur '$BlocksList' aus.</span><span class="sxs-lookup"><span data-stu-id="81bd9-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="81bd9-157">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="81bd9-157">Click Bind.</span></span>
    * <span data-ttu-id="81bd9-158">Erstellen Sie eine Zusammenfassungsposition für jeden gemerkten Block.</span><span class="sxs-lookup"><span data-stu-id="81bd9-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="81bd9-159">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-159">Click the Format tab.</span></span>
42. <span data-ttu-id="81bd9-160">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="81bd9-161">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="81bd9-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="81bd9-162">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="81bd9-162">Click Edit formula.</span></span>
45. <span data-ttu-id="81bd9-163">Geben Sie im Feld 'Formel' '"Block id: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="81bd9-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="81bd9-164">"Block id: " &</span></span>  
46. <span data-ttu-id="81bd9-165">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="81bd9-166">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="81bd9-167">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-167">Click Add data source.</span></span>
49. <span data-ttu-id="81bd9-168">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81bd9-168">Click Save.</span></span>
50. <span data-ttu-id="81bd9-169">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81bd9-169">Close the page.</span></span>
51. <span data-ttu-id="81bd9-170">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-170">Click the Format tab.</span></span>
52. <span data-ttu-id="81bd9-171">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="81bd9-172">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="81bd9-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="81bd9-173">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="81bd9-173">Click Edit formula.</span></span>
    * <span data-ttu-id="81bd9-174">Erstellen Sie eine Ausgabe für die Anzahl der Positionen für jeden Block in diesen Bericht.</span><span class="sxs-lookup"><span data-stu-id="81bd9-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="81bd9-175">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="81bd9-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="81bd9-176">"Anzahl der Positionen in diesem Block: " &</span><span class="sxs-lookup"><span data-stu-id="81bd9-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="81bd9-177">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="81bd9-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="81bd9-178">"Anzahl der Positionen in diesem Block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="81bd9-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="81bd9-179">Wählen Sie in der Strukturdarstellung 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="81bd9-180">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-180">Click Add function.</span></span>
59. <span data-ttu-id="81bd9-181">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-181">Click Add data source.</span></span>
60. <span data-ttu-id="81bd9-182">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="81bd9-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="81bd9-183">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="81bd9-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="81bd9-184">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="81bd9-185">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="81bd9-186">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-186">Click Add data source.</span></span>
64. <span data-ttu-id="81bd9-187">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="81bd9-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="81bd9-188">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="81bd9-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="81bd9-189">Wählen Sie in der Struktur '$RecName' aus.</span><span class="sxs-lookup"><span data-stu-id="81bd9-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="81bd9-190">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81bd9-190">Click Add data source.</span></span>
67. <span data-ttu-id="81bd9-191">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="81bd9-192">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="81bd9-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="81bd9-193">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81bd9-193">Click Save.</span></span>
69. <span data-ttu-id="81bd9-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81bd9-194">Close the page.</span></span>
70. <span data-ttu-id="81bd9-195">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-195">Click the Format tab.</span></span>
71. <span data-ttu-id="81bd9-196">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="81bd9-197">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="81bd9-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="81bd9-198">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="81bd9-198">Click Edit formula.</span></span>
    * <span data-ttu-id="81bd9-199">Erstellen Sie eine Ausgabe mit dem fakturierten Gesamtbetrag für jeden Block im Bericht.</span><span class="sxs-lookup"><span data-stu-id="81bd9-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="81bd9-200">Geben Sie im Feld Formel '"Summe des berechneten Betrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="81bd9-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="81bd9-201">"Summe des Rechnungsbetrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="81bd9-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="81bd9-202">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81bd9-202">Click Save.</span></span>
76. <span data-ttu-id="81bd9-203">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81bd9-203">Close the page.</span></span>
77. <span data-ttu-id="81bd9-204">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81bd9-204">Click Save.</span></span>
78. <span data-ttu-id="81bd9-205">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81bd9-205">Close the page.</span></span>


