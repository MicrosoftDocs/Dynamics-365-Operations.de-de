---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 3: Nutzen von Berechnungen für die Ausgabe)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "347076"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="6c59d-103">ER Konfigurieren des Formats für Inventuren und Summierungen (Teil 3: Nutzen von Berechnungen für die Ausgabe)</span><span class="sxs-lookup"><span data-stu-id="6c59d-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c59d-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="6c59d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6c59d-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c59d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6c59d-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 2: Berechnungen konfigurieren)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="6c59d-107">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c59d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="6c59d-108">Konfigurieren Sie diesen Bericht für Inventarisierungs- und Zusammenfassungsinformationen</span><span class="sxs-lookup"><span data-stu-id="6c59d-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="6c59d-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="6c59d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6c59d-110">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="6c59d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="6c59d-111">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="6c59d-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="6c59d-112">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="6c59d-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="6c59d-113">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="6c59d-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="6c59d-114">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="6c59d-114">Click Designer.</span></span>
7. <span data-ttu-id="6c59d-115">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6c59d-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="6c59d-116">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="6c59d-117">Fügen Sie eine neue Datenquelle hinzu, um die Liste der gemerkten Blöcken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="6c59d-118">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="6c59d-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="6c59d-119">Geben Sie im Feld "Name" "$BlocksList" ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="6c59d-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="6c59d-120">$BlocksList</span></span>  
11. <span data-ttu-id="6c59d-121">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c59d-121">Click Edit formula.</span></span>
12. <span data-ttu-id="6c59d-122">Wählen Sie in der Strukturdarstellung 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="6c59d-123">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-123">Click Add function.</span></span>
14. <span data-ttu-id="6c59d-124">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-124">Click Add data source.</span></span>
15. <span data-ttu-id="6c59d-125">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', ' ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="6c59d-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6c59d-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="6c59d-127">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', "\*")' ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="6c59d-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="6c59d-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="6c59d-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c59d-129">Click Save.</span></span>
    * <span data-ttu-id="6c59d-130">Das Muster "\*" bedeutet, dass alle Blöcke der Liste für diesen Datensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6c59d-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="6c59d-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c59d-131">Close the page.</span></span>
19. <span data-ttu-id="6c59d-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6c59d-132">Click OK.</span></span>
20. <span data-ttu-id="6c59d-133">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-133">Click the Format tab.</span></span>
21. <span data-ttu-id="6c59d-134">Wählen Sie in der Struktur "Intrastat\Data" aus.</span><span class="sxs-lookup"><span data-stu-id="6c59d-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="6c59d-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6c59d-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6c59d-136">Wählen Sie in der Struktur 'Text\Sequence'..</span><span class="sxs-lookup"><span data-stu-id="6c59d-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="6c59d-137">Geben Sie im Feld "Name" die Zeichenfolge "Summen nach Blöcken' ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="6c59d-138">Summen nach Blöcken</span><span class="sxs-lookup"><span data-stu-id="6c59d-138">Totals by blocks</span></span>  
25. <span data-ttu-id="6c59d-139">Wählen Sie im Feld "Sonderzeichen" "Neue Zeile - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="6c59d-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="6c59d-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6c59d-140">Click OK.</span></span>
27. <span data-ttu-id="6c59d-141">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="6c59d-142">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6c59d-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="6c59d-143">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="6c59d-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="6c59d-144">Geben Sie im Feld "Name" "Block code" ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="6c59d-145">Blockcode</span><span class="sxs-lookup"><span data-stu-id="6c59d-145">Block code</span></span>  
31. <span data-ttu-id="6c59d-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6c59d-146">Click OK.</span></span>
32. <span data-ttu-id="6c59d-147">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6c59d-147">Click Add String.</span></span>
33. <span data-ttu-id="6c59d-148">Geben Sie im Feld "Name" 'Lines counting' ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="6c59d-149">Inventarisierte Positionen</span><span class="sxs-lookup"><span data-stu-id="6c59d-149">Lines counting</span></span>  
34. <span data-ttu-id="6c59d-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6c59d-150">Click OK.</span></span>
35. <span data-ttu-id="6c59d-151">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6c59d-151">Click Add String.</span></span>
36. <span data-ttu-id="6c59d-152">Geben Sie im Feld Name "Total amount" ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="6c59d-153">Gesamtstundenzahl</span><span class="sxs-lookup"><span data-stu-id="6c59d-153">Total amount</span></span>  
37. <span data-ttu-id="6c59d-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6c59d-154">Click OK.</span></span>
38. <span data-ttu-id="6c59d-155">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6c59d-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="6c59d-156">Wählen Sie in der Struktur '$BlocksList' aus.</span><span class="sxs-lookup"><span data-stu-id="6c59d-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="6c59d-157">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="6c59d-157">Click Bind.</span></span>
    * <span data-ttu-id="6c59d-158">Erstellen Sie eine Zusammenfassungsposition für jeden gemerkten Block.</span><span class="sxs-lookup"><span data-stu-id="6c59d-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="6c59d-159">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-159">Click the Format tab.</span></span>
42. <span data-ttu-id="6c59d-160">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="6c59d-161">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6c59d-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="6c59d-162">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c59d-162">Click Edit formula.</span></span>
45. <span data-ttu-id="6c59d-163">Geben Sie im Feld 'Formel' '"Block id: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="6c59d-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="6c59d-164">"Block id: " &</span></span>  
46. <span data-ttu-id="6c59d-165">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="6c59d-166">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="6c59d-167">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-167">Click Add data source.</span></span>
49. <span data-ttu-id="6c59d-168">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c59d-168">Click Save.</span></span>
50. <span data-ttu-id="6c59d-169">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c59d-169">Close the page.</span></span>
51. <span data-ttu-id="6c59d-170">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-170">Click the Format tab.</span></span>
52. <span data-ttu-id="6c59d-171">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="6c59d-172">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6c59d-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="6c59d-173">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c59d-173">Click Edit formula.</span></span>
    * <span data-ttu-id="6c59d-174">Erstellen Sie eine Ausgabe für die Anzahl der Positionen für jeden Block in diesen Bericht.</span><span class="sxs-lookup"><span data-stu-id="6c59d-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="6c59d-175">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="6c59d-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="6c59d-176">"Anzahl der Positionen in diesem Block: " &</span><span class="sxs-lookup"><span data-stu-id="6c59d-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="6c59d-177">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="6c59d-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="6c59d-178">"Anzahl der Positionen in diesem Block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="6c59d-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="6c59d-179">Wählen Sie in der Strukturdarstellung 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="6c59d-180">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-180">Click Add function.</span></span>
59. <span data-ttu-id="6c59d-181">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-181">Click Add data source.</span></span>
60. <span data-ttu-id="6c59d-182">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="6c59d-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="6c59d-183">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6c59d-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="6c59d-184">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="6c59d-185">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="6c59d-186">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-186">Click Add data source.</span></span>
64. <span data-ttu-id="6c59d-187">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="6c59d-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="6c59d-188">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="6c59d-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="6c59d-189">Wählen Sie in der Struktur '$RecName' aus.</span><span class="sxs-lookup"><span data-stu-id="6c59d-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="6c59d-190">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c59d-190">Click Add data source.</span></span>
67. <span data-ttu-id="6c59d-191">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6c59d-192">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="6c59d-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="6c59d-193">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c59d-193">Click Save.</span></span>
69. <span data-ttu-id="6c59d-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c59d-194">Close the page.</span></span>
70. <span data-ttu-id="6c59d-195">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-195">Click the Format tab.</span></span>
71. <span data-ttu-id="6c59d-196">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="6c59d-197">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6c59d-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="6c59d-198">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c59d-198">Click Edit formula.</span></span>
    * <span data-ttu-id="6c59d-199">Erstellen Sie eine Ausgabe mit dem fakturierten Gesamtbetrag für jeden Block im Bericht.</span><span class="sxs-lookup"><span data-stu-id="6c59d-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="6c59d-200">Geben Sie im Feld Formel '"Summe des berechneten Betrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="6c59d-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6c59d-201">"Summe des Rechnungsbetrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="6c59d-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="6c59d-202">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c59d-202">Click Save.</span></span>
76. <span data-ttu-id="6c59d-203">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c59d-203">Close the page.</span></span>
77. <span data-ttu-id="6c59d-204">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c59d-204">Click Save.</span></span>
78. <span data-ttu-id="6c59d-205">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c59d-205">Close the page.</span></span>

