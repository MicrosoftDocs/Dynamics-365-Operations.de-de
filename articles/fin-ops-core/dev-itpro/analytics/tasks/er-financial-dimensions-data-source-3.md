---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684786"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="3da91-103">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)</span><span class="sxs-lookup"><span data-stu-id="3da91-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3da91-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="3da91-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="3da91-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3da91-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3da91-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 2: Modellzuordnung)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="3da91-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="3da91-107">Entwerfen eines Berichts zur Darstellung von Finanzdimensionen</span><span class="sxs-lookup"><span data-stu-id="3da91-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="3da91-108">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="3da91-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3da91-109">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="3da91-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="3da91-110">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3da91-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="3da91-111">Geben Sie im Feld "Neu" "Format basierend auf Finandimensions-Beispieldatenmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="3da91-112">Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3da91-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="3da91-113">Geben Sie im Feld "Name" "Sachkontoerfassungbericht" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="3da91-114">Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.</span><span class="sxs-lookup"><span data-stu-id="3da91-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="3da91-115">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="3da91-115">Click Create configuration.</span></span>
8. <span data-ttu-id="3da91-116">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="3da91-116">Click Designer.</span></span>
9. <span data-ttu-id="3da91-117">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3da91-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="3da91-118">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="3da91-119">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="3da91-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-120">Click OK.</span></span>
13. <span data-ttu-id="3da91-121">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="3da91-122">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="3da91-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="3da91-123">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="3da91-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-124">Click OK.</span></span>
17. <span data-ttu-id="3da91-125">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="3da91-126">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="3da91-127">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="3da91-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-128">Click OK.</span></span>
21. <span data-ttu-id="3da91-129">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="3da91-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="3da91-130">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="3da91-131">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="3da91-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="3da91-132">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="3da91-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-133">Click OK.</span></span>
26. <span data-ttu-id="3da91-134">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="3da91-135">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="3da91-136">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="3da91-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-137">Click OK.</span></span>
30. <span data-ttu-id="3da91-138">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="3da91-139">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="3da91-140">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="3da91-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="3da91-141">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="3da91-142">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-142">Click OK.</span></span>
35. <span data-ttu-id="3da91-143">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="3da91-144">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="3da91-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-145">Click OK.</span></span>
38. <span data-ttu-id="3da91-146">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="3da91-147">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="3da91-148">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-148">Click OK.</span></span>
41. <span data-ttu-id="3da91-149">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="3da91-150">Geben Sie im Feld Name "Dt" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="3da91-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-151">Click OK.</span></span>
44. <span data-ttu-id="3da91-152">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="3da91-153">Geben Sie im Feld Name "Ct" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="3da91-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-154">Click OK.</span></span>
47. <span data-ttu-id="3da91-155">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="3da91-156">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="3da91-157">Geben Sie im Feld "Name" "Dimensionen" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="3da91-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-158">Click OK.</span></span>
51. <span data-ttu-id="3da91-159">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="3da91-160">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="3da91-161">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="3da91-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="3da91-162">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="3da91-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-163">Click OK.</span></span>
56. <span data-ttu-id="3da91-164">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="3da91-165">Geben Sie im Feld 'Name' "Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="3da91-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-166">Click OK.</span></span>
59. <span data-ttu-id="3da91-167">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3da91-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="3da91-168">Geben Sie im Feld Name "Desc" ein.</span><span class="sxs-lookup"><span data-stu-id="3da91-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="3da91-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3da91-169">Click OK.</span></span>
<span data-ttu-id="3da91-170">![EB-Vorgangs-Designerseite](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="3da91-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="3da91-171">Zuweisen von Berichtselementen zu Datenquellen</span><span class="sxs-lookup"><span data-stu-id="3da91-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="3da91-172">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3da91-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="3da91-173">In der Struktur erweitern Sie "Modell: Datenmodell-Finanzdimensionsbeispielmodell".</span><span class="sxs-lookup"><span data-stu-id="3da91-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="3da91-174">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="3da91-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="3da91-175">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="3da91-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="3da91-176">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="3da91-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="3da91-177">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="3da91-178">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Beschreibung: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="3da91-179">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-179">Click Bind.</span></span>
9. <span data-ttu-id="3da91-180">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Wert: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="3da91-181">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="3da91-182">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-182">Click Bind.</span></span>
12. <span data-ttu-id="3da91-183">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="3da91-184">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="3da91-185">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-185">Click Bind.</span></span>
15. <span data-ttu-id="3da91-186">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="3da91-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="3da91-187">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="3da91-188">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-188">Click Bind.</span></span>
18. <span data-ttu-id="3da91-189">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Ct: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="3da91-190">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Haben: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="3da91-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="3da91-191">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-191">Click Bind.</span></span>
21. <span data-ttu-id="3da91-192">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dt: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="3da91-193">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Soll: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="3da91-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="3da91-194">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-194">Click Bind.</span></span>
24. <span data-ttu-id="3da91-195">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Währung: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="3da91-196">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Währung: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="3da91-197">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-197">Click Bind.</span></span>
27. <span data-ttu-id="3da91-198">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Datum: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="3da91-199">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="3da91-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="3da91-200">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-200">Click Bind.</span></span>
30. <span data-ttu-id="3da91-201">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Beleg: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="3da91-202">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Beleg: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="3da91-203">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-203">Click Bind.</span></span>
33. <span data-ttu-id="3da91-204">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="3da91-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="3da91-205">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="3da91-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="3da91-206">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-206">Click Bind.</span></span>
36. <span data-ttu-id="3da91-207">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Charge: XML Attribut'.</span><span class="sxs-lookup"><span data-stu-id="3da91-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="3da91-208">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="3da91-209">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-209">Click Bind.</span></span>
39. <span data-ttu-id="3da91-210">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="3da91-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="3da91-211">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="3da91-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="3da91-212">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-212">Click Bind.</span></span>
42. <span data-ttu-id="3da91-213">Wählen Sie in der Strukturdarstellung "Root: XML Element\Unternehmen: XML-Attribut".</span><span class="sxs-lookup"><span data-stu-id="3da91-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="3da91-214">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Unternehmen: String'.</span><span class="sxs-lookup"><span data-stu-id="3da91-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="3da91-215">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="3da91-215">Click Bind.</span></span>
45. <span data-ttu-id="3da91-216">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="3da91-216">Click Save.</span></span>
46. <span data-ttu-id="3da91-217">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3da91-217">Close the page.</span></span>
<span data-ttu-id="3da91-218">![EB-Vorgangs-Designerseite](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="3da91-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

