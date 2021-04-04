---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 3: Nutzen von Berechnungen für die Ausgabe)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat für das Zählen und Summieren basierend auf Daten der bereits generierten Textausgabe konfigurieren. (Teil 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af95399118b9059b9bead3a1b84203cf3b6e74c2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567115"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="1ccd7-104">ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 3: Nutzen von Berechnungen für die Ausgabe)</span><span class="sxs-lookup"><span data-stu-id="1ccd7-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ccd7-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="1ccd7-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="1ccd7-107">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden „ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 2: Berechnungen konfigurieren)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="1ccd7-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="1ccd7-109">Konfigurieren Sie diesen Bericht für Inventarisierungs- und Zusammenfassungsinformationen</span><span class="sxs-lookup"><span data-stu-id="1ccd7-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="1ccd7-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1ccd7-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1ccd7-112">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="1ccd7-113">Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="1ccd7-114">Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="1ccd7-115">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-115">Click Designer.</span></span>
7. <span data-ttu-id="1ccd7-116">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="1ccd7-117">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="1ccd7-118">Fügen Sie eine neue Datenquelle hinzu, um die Liste der gemerkten Blöcken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="1ccd7-119">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="1ccd7-120">Geben Sie im Feld "Name" "$BlocksList" ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="1ccd7-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="1ccd7-121">$BlocksList</span></span>  
11. <span data-ttu-id="1ccd7-122">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-122">Click Edit formula.</span></span>
12. <span data-ttu-id="1ccd7-123">Wählen Sie in der Strukturdarstellung 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="1ccd7-124">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-124">Click Add function.</span></span>
14. <span data-ttu-id="1ccd7-125">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-125">Click Add data source.</span></span>
15. <span data-ttu-id="1ccd7-126">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', ' ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="1ccd7-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="1ccd7-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="1ccd7-128">Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', "\*")' ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="1ccd7-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="1ccd7-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="1ccd7-130">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-130">Click Save.</span></span>
    * <span data-ttu-id="1ccd7-131">Das Muster „\*“ bedeutet, dass alle Blöcke der Liste für diesen Datensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="1ccd7-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-132">Close the page.</span></span>
19. <span data-ttu-id="1ccd7-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-133">Click OK.</span></span>
20. <span data-ttu-id="1ccd7-134">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-134">Click the Format tab.</span></span>
21. <span data-ttu-id="1ccd7-135">Wählen Sie in der Struktur "Intrastat\Data" aus.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="1ccd7-136">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="1ccd7-137">Wählen Sie in der Struktur 'Text\Sequence'..</span><span class="sxs-lookup"><span data-stu-id="1ccd7-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="1ccd7-138">Geben Sie im Feld "Name" die Zeichenfolge "Summen nach Blöcken' ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="1ccd7-139">Summen nach Blöcken</span><span class="sxs-lookup"><span data-stu-id="1ccd7-139">Totals by blocks</span></span>  
25. <span data-ttu-id="1ccd7-140">Wählen Sie im Feld "Sonderzeichen" "Neue Zeile - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="1ccd7-141">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-141">Click OK.</span></span>
27. <span data-ttu-id="1ccd7-142">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="1ccd7-143">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="1ccd7-144">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="1ccd7-145">Geben Sie im Feld "Name" "Block code" ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="1ccd7-146">Blockcode</span><span class="sxs-lookup"><span data-stu-id="1ccd7-146">Block code</span></span>  
31. <span data-ttu-id="1ccd7-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-147">Click OK.</span></span>
32. <span data-ttu-id="1ccd7-148">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-148">Click Add String.</span></span>
33. <span data-ttu-id="1ccd7-149">Geben Sie im Feld "Name" 'Lines counting' ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="1ccd7-150">Inventarisierte Positionen</span><span class="sxs-lookup"><span data-stu-id="1ccd7-150">Lines counting</span></span>  
34. <span data-ttu-id="1ccd7-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-151">Click OK.</span></span>
35. <span data-ttu-id="1ccd7-152">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-152">Click Add String.</span></span>
36. <span data-ttu-id="1ccd7-153">Geben Sie im Feld Name "Total amount" ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="1ccd7-154">Gesamtstundenzahl</span><span class="sxs-lookup"><span data-stu-id="1ccd7-154">Total amount</span></span>  
37. <span data-ttu-id="1ccd7-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-155">Click OK.</span></span>
38. <span data-ttu-id="1ccd7-156">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="1ccd7-157">Wählen Sie in der Struktur '$BlocksList' aus.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="1ccd7-158">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-158">Click Bind.</span></span>
    * <span data-ttu-id="1ccd7-159">Erstellen Sie eine Zusammenfassungsposition für jeden gemerkten Block.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="1ccd7-160">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-160">Click the Format tab.</span></span>
42. <span data-ttu-id="1ccd7-161">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="1ccd7-162">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="1ccd7-163">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-163">Click Edit formula.</span></span>
45. <span data-ttu-id="1ccd7-164">Geben Sie im Feld 'Formel' '"Block id: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="1ccd7-165">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="1ccd7-165">"Block id: " &</span></span>  
46. <span data-ttu-id="1ccd7-166">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="1ccd7-167">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="1ccd7-168">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-168">Click Add data source.</span></span>
49. <span data-ttu-id="1ccd7-169">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-169">Click Save.</span></span>
50. <span data-ttu-id="1ccd7-170">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-170">Close the page.</span></span>
51. <span data-ttu-id="1ccd7-171">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-171">Click the Format tab.</span></span>
52. <span data-ttu-id="1ccd7-172">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="1ccd7-173">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="1ccd7-174">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-174">Click Edit formula.</span></span>
    * <span data-ttu-id="1ccd7-175">Erstellen Sie eine Ausgabe für die Anzahl der Positionen für jeden Block in diesen Bericht.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="1ccd7-176">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & ' ein.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="1ccd7-177">"Anzahl der Positionen in diesem Block: " &</span><span class="sxs-lookup"><span data-stu-id="1ccd7-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="1ccd7-178">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="1ccd7-179">"Anzahl der Positionen in diesem Block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="1ccd7-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="1ccd7-180">Wählen Sie in der Strukturdarstellung 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="1ccd7-181">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-181">Click Add function.</span></span>
59. <span data-ttu-id="1ccd7-182">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-182">Click Add data source.</span></span>
60. <span data-ttu-id="1ccd7-183">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="1ccd7-184">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="1ccd7-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="1ccd7-185">Erweitern Sie in der Struktur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="1ccd7-186">Wählen Sie in der Struktur '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="1ccd7-187">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-187">Click Add data source.</span></span>
64. <span data-ttu-id="1ccd7-188">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="1ccd7-189">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="1ccd7-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="1ccd7-190">Wählen Sie in der Struktur '$RecName' aus.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="1ccd7-191">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-191">Click Add data source.</span></span>
67. <span data-ttu-id="1ccd7-192">Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="1ccd7-193">"Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="1ccd7-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="1ccd7-194">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-194">Click Save.</span></span>
69. <span data-ttu-id="1ccd7-195">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-195">Close the page.</span></span>
70. <span data-ttu-id="1ccd7-196">Klicken Sie auf die Registerkarte 'Format'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-196">Click the Format tab.</span></span>
71. <span data-ttu-id="1ccd7-197">Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="1ccd7-198">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="1ccd7-199">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-199">Click Edit formula.</span></span>
    * <span data-ttu-id="1ccd7-200">Erstellen Sie eine Ausgabe mit dem fakturierten Gesamtbetrag für jeden Block im Bericht.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="1ccd7-201">Geben Sie im Feld Formel '"Summe des berechneten Betrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="1ccd7-202">"Summe des Rechnungsbetrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="1ccd7-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="1ccd7-203">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-203">Click Save.</span></span>
76. <span data-ttu-id="1ccd7-204">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-204">Close the page.</span></span>
77. <span data-ttu-id="1ccd7-205">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1ccd7-205">Click Save.</span></span>
78. <span data-ttu-id="1ccd7-206">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]