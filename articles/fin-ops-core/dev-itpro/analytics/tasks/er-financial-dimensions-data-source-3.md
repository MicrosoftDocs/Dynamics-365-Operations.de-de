---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 3)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752411"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="f2bd7-104">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)</span><span class="sxs-lookup"><span data-stu-id="f2bd7-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2bd7-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f2bd7-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f2bd7-107">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 2: Modellzuordnung)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="f2bd7-108">Entwerfen eines Berichts zur Darstellung von Finanzdimensionen</span><span class="sxs-lookup"><span data-stu-id="f2bd7-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="f2bd7-109">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f2bd7-110">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f2bd7-111">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f2bd7-112">Geben Sie im Feld "Neu" "Format basierend auf Finandimensions-Beispieldatenmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="f2bd7-113">Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="f2bd7-114">Geben Sie im Feld "Name" "Sachkontoerfassungbericht" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="f2bd7-115">Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="f2bd7-116">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-116">Click Create configuration.</span></span>
8. <span data-ttu-id="f2bd7-117">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-117">Click Designer.</span></span>
9. <span data-ttu-id="f2bd7-118">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="f2bd7-119">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="f2bd7-120">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="f2bd7-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-121">Click OK.</span></span>
13. <span data-ttu-id="f2bd7-122">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="f2bd7-123">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="f2bd7-124">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="f2bd7-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-125">Click OK.</span></span>
17. <span data-ttu-id="f2bd7-126">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="f2bd7-127">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="f2bd7-128">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="f2bd7-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-129">Click OK.</span></span>
21. <span data-ttu-id="f2bd7-130">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="f2bd7-131">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="f2bd7-132">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="f2bd7-133">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="f2bd7-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-134">Click OK.</span></span>
26. <span data-ttu-id="f2bd7-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="f2bd7-136">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="f2bd7-137">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="f2bd7-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-138">Click OK.</span></span>
30. <span data-ttu-id="f2bd7-139">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="f2bd7-140">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="f2bd7-141">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="f2bd7-142">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="f2bd7-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-143">Click OK.</span></span>
35. <span data-ttu-id="f2bd7-144">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="f2bd7-145">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="f2bd7-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-146">Click OK.</span></span>
38. <span data-ttu-id="f2bd7-147">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="f2bd7-148">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="f2bd7-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-149">Click OK.</span></span>
41. <span data-ttu-id="f2bd7-150">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="f2bd7-151">Geben Sie im Feld Name "Dt" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="f2bd7-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-152">Click OK.</span></span>
44. <span data-ttu-id="f2bd7-153">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="f2bd7-154">Geben Sie im Feld Name "Ct" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="f2bd7-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-155">Click OK.</span></span>
47. <span data-ttu-id="f2bd7-156">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="f2bd7-157">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="f2bd7-158">Geben Sie im Feld "Name" "Dimensionen" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="f2bd7-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-159">Click OK.</span></span>
51. <span data-ttu-id="f2bd7-160">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="f2bd7-161">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="f2bd7-162">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="f2bd7-163">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="f2bd7-164">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-164">Click OK.</span></span>
56. <span data-ttu-id="f2bd7-165">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="f2bd7-166">Geben Sie im Feld 'Name' "Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="f2bd7-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-167">Click OK.</span></span>
59. <span data-ttu-id="f2bd7-168">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="f2bd7-169">Geben Sie im Feld Name "Desc" ein.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="f2bd7-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-170">Click OK.</span></span>
<span data-ttu-id="f2bd7-171">![EB-Vorgangs-Designerseite](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="f2bd7-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="f2bd7-172">Zuweisen von Berichtselementen zu Datenquellen</span><span class="sxs-lookup"><span data-stu-id="f2bd7-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="f2bd7-173">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="f2bd7-174">In der Struktur erweitern Sie "Modell: Datenmodell-Finanzdimensionsbeispielmodell".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f2bd7-175">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="f2bd7-176">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="f2bd7-177">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="f2bd7-178">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="f2bd7-179">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Beschreibung: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="f2bd7-180">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-180">Click Bind.</span></span>
9. <span data-ttu-id="f2bd7-181">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Wert: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="f2bd7-182">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="f2bd7-183">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-183">Click Bind.</span></span>
12. <span data-ttu-id="f2bd7-184">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="f2bd7-185">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="f2bd7-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-186">Click Bind.</span></span>
15. <span data-ttu-id="f2bd7-187">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="f2bd7-188">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="f2bd7-189">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-189">Click Bind.</span></span>
18. <span data-ttu-id="f2bd7-190">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Ct: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="f2bd7-191">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Haben: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="f2bd7-192">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-192">Click Bind.</span></span>
21. <span data-ttu-id="f2bd7-193">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dt: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="f2bd7-194">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Soll: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="f2bd7-195">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-195">Click Bind.</span></span>
24. <span data-ttu-id="f2bd7-196">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Währung: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="f2bd7-197">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Währung: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="f2bd7-198">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-198">Click Bind.</span></span>
27. <span data-ttu-id="f2bd7-199">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Datum: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="f2bd7-200">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="f2bd7-201">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-201">Click Bind.</span></span>
30. <span data-ttu-id="f2bd7-202">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Beleg: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="f2bd7-203">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Beleg: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="f2bd7-204">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-204">Click Bind.</span></span>
33. <span data-ttu-id="f2bd7-205">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="f2bd7-206">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="f2bd7-207">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-207">Click Bind.</span></span>
36. <span data-ttu-id="f2bd7-208">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Charge: XML Attribut'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="f2bd7-209">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="f2bd7-210">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-210">Click Bind.</span></span>
39. <span data-ttu-id="f2bd7-211">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="f2bd7-212">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="f2bd7-213">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-213">Click Bind.</span></span>
42. <span data-ttu-id="f2bd7-214">Wählen Sie in der Strukturdarstellung "Root: XML Element\Unternehmen: XML-Attribut".</span><span class="sxs-lookup"><span data-stu-id="f2bd7-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="f2bd7-215">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Unternehmen: String'.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="f2bd7-216">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-216">Click Bind.</span></span>
45. <span data-ttu-id="f2bd7-217">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-217">Click Save.</span></span>
46. <span data-ttu-id="f2bd7-218">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2bd7-218">Close the page.</span></span>
<span data-ttu-id="f2bd7-219">![EB-Vorgangs-Designerseite](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="f2bd7-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]