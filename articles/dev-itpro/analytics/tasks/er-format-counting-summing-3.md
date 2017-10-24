--- 
title: "Verwenden von Berechnungen zum Erstellen der Ausgabe für das Zählen und Summieren für elektronische Berichterstellung (ER)"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 143856f65eaf1d6d667f4f7dfb229807da6f4ad8
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="ff4ea-103">Verwenden von Berechnungen zum Erstellen der Ausgabe für das Zählen und Summieren für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="ff4ea-103">Use computations to make the output for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff4ea-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="ff4ea-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ff4ea-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 2: Berechnungen konfigurieren)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="ff4ea-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="ff4ea-108">Konfigurieren Sie diesen Bericht für Inventarisierungs- und Zusammenfassungsinformationen</span><span class="sxs-lookup"><span data-stu-id="ff4ea-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="ff4ea-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ff4ea-110">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ff4ea-111">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="ff4ea-112">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="ff4ea-113">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="ff4ea-114">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-114">Click Designer.</span></span>
7. <span data-ttu-id="ff4ea-115">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="ff4ea-116">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="ff4ea-117">Fügen Sie eine neue Datenquelle hinzu, um die Liste der gemerkten Blöcken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="ff4ea-118">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="ff4ea-119">Geben Sie im Feld "Name" "$BlocksList" ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="ff4ea-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="ff4ea-120">$BlocksList</span></span>  
11. <span data-ttu-id="ff4ea-121">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-121">Click Edit formula.</span></span>
12. <span data-ttu-id="ff4ea-122">Wählen Sie in der Strukturdarstellung 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="ff4ea-123">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-123">Click Add function.</span></span>
14. <span data-ttu-id="ff4ea-124">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-124">Click Add data source.</span></span>
15. <span data-ttu-id="ff4ea-125">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', ' ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="ff4ea-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="ff4ea-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="ff4ea-127">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', "*")' ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "*")'.</span></span>
    * <span data-ttu-id="ff4ea-128">COLLECTEDLIST('$BlockName', "*")</span><span class="sxs-lookup"><span data-stu-id="ff4ea-128">COLLECTEDLIST('$BlockName', "*")</span></span>  
17. <span data-ttu-id="ff4ea-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-129">Click Save.</span></span>
    * <span data-ttu-id="ff4ea-130">Das Muster "*" bedeutet, dass alle Blöcke der Liste für diesen Datensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-130">The pattern “*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="ff4ea-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-131">Close the page.</span></span>
19. <span data-ttu-id="ff4ea-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-132">Click OK.</span></span>
20. <span data-ttu-id="ff4ea-133">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-133">Click the Format tab.</span></span>
21. <span data-ttu-id="ff4ea-134">Wählen Sie in der Struktur "Intrastat\Data" aus.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="ff4ea-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ff4ea-136">Wählen Sie in der Struktur 'Text\Sequence'..</span><span class="sxs-lookup"><span data-stu-id="ff4ea-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="ff4ea-137">Geben Sie im Feld "Name" die Zeichenfolge "Summen nach Blöcken' ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="ff4ea-138">Summen nach Blöcken</span><span class="sxs-lookup"><span data-stu-id="ff4ea-138">Totals by blocks</span></span>  
25. <span data-ttu-id="ff4ea-139">Wählen Sie im Feld "Sonderzeichen" "Neue Zeile - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="ff4ea-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-140">Click OK.</span></span>
27. <span data-ttu-id="ff4ea-141">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="ff4ea-142">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="ff4ea-143">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="ff4ea-144">Geben Sie im Feld "Name" "Block code" ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="ff4ea-145">Blockcode</span><span class="sxs-lookup"><span data-stu-id="ff4ea-145">Block code</span></span>  
31. <span data-ttu-id="ff4ea-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-146">Click OK.</span></span>
32. <span data-ttu-id="ff4ea-147">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-147">Click Add String.</span></span>
33. <span data-ttu-id="ff4ea-148">Geben Sie im Feld "Name" 'Lines counting' ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="ff4ea-149">Inventarisierte Positionen</span><span class="sxs-lookup"><span data-stu-id="ff4ea-149">Lines counting</span></span>  
34. <span data-ttu-id="ff4ea-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-150">Click OK.</span></span>
35. <span data-ttu-id="ff4ea-151">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-151">Click Add String.</span></span>
36. <span data-ttu-id="ff4ea-152">Geben Sie im Feld Name "Total amount" ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="ff4ea-153">Gesamtstundenzahl</span><span class="sxs-lookup"><span data-stu-id="ff4ea-153">Total amount</span></span>  
37. <span data-ttu-id="ff4ea-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-154">Click OK.</span></span>
38. <span data-ttu-id="ff4ea-155">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="ff4ea-156">Wählen Sie in der Struktur '$BlocksList' aus.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="ff4ea-157">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-157">Click Bind.</span></span>
    * <span data-ttu-id="ff4ea-158">Erstellen Sie eine Zusammenfassungsposition für jeden gemerkten Block.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="ff4ea-159">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-159">Click the Format tab.</span></span>
42. <span data-ttu-id="ff4ea-160">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="ff4ea-161">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="ff4ea-162">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-162">Click Edit formula.</span></span>
45. <span data-ttu-id="ff4ea-163">Geben Sie im Feld 'Formel' '"Block id: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="ff4ea-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="ff4ea-164">"Block id: " &</span></span>  
46. <span data-ttu-id="ff4ea-165">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="ff4ea-166">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="ff4ea-167">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-167">Click Add data source.</span></span>
49. <span data-ttu-id="ff4ea-168">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-168">Click Save.</span></span>
50. <span data-ttu-id="ff4ea-169">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-169">Close the page.</span></span>
51. <span data-ttu-id="ff4ea-170">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-170">Click the Format tab.</span></span>
52. <span data-ttu-id="ff4ea-171">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="ff4ea-172">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="ff4ea-173">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-173">Click Edit formula.</span></span>
    * <span data-ttu-id="ff4ea-174">Erstellen Sie eine Ausgabe für die Anzahl der Positionen für jeden Block in diesen Bericht.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="ff4ea-175">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="ff4ea-176">"Anzahl der Positionen in diesem Block:  " &</span><span class="sxs-lookup"><span data-stu-id="ff4ea-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="ff4ea-177">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="ff4ea-178">"Anzahl der Positionen in diesem Block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="ff4ea-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="ff4ea-179">Wählen Sie in der Strukturdarstellung 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="ff4ea-180">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-180">Click Add function.</span></span>
59. <span data-ttu-id="ff4ea-181">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-181">Click Add data source.</span></span>
60. <span data-ttu-id="ff4ea-182">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="ff4ea-183">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="ff4ea-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="ff4ea-184">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="ff4ea-185">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="ff4ea-186">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-186">Click Add data source.</span></span>
64. <span data-ttu-id="ff4ea-187">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="ff4ea-188">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="ff4ea-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="ff4ea-189">Wählen Sie in der Struktur '$RecName' aus.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="ff4ea-190">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-190">Click Add data source.</span></span>
67. <span data-ttu-id="ff4ea-191">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="ff4ea-192">"Anzahl der Positionen in diesem Block:  " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="ff4ea-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
68. <span data-ttu-id="ff4ea-193">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-193">Click Save.</span></span>
69. <span data-ttu-id="ff4ea-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-194">Close the page.</span></span>
70. <span data-ttu-id="ff4ea-195">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-195">Click the Format tab.</span></span>
71. <span data-ttu-id="ff4ea-196">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="ff4ea-197">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="ff4ea-198">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-198">Click Edit formula.</span></span>
    * <span data-ttu-id="ff4ea-199">Erstellen Sie eine Ausgabe mit dem fakturierten Gesamtbetrag für jeden Block im Bericht.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="ff4ea-200">Geben Sie im Feld Formel '"Summe des berechneten Betrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="ff4ea-201">"Summe des Rechnungsbetrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="ff4ea-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
75. <span data-ttu-id="ff4ea-202">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-202">Click Save.</span></span>
76. <span data-ttu-id="ff4ea-203">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-203">Close the page.</span></span>
77. <span data-ttu-id="ff4ea-204">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ff4ea-204">Click Save.</span></span>
78. <span data-ttu-id="ff4ea-205">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-205">Close the page.</span></span>


