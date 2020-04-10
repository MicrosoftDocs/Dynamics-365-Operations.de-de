---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbbc81eaf8c13e8d13e30a0276e38453e07ead9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142523"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="ba6ef-103">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)</span><span class="sxs-lookup"><span data-stu-id="ba6ef-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba6ef-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ba6ef-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ba6ef-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 2: Modellzuordnung)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="ba6ef-107">Entwerfen eines Berichts zur Darstellung von Finanzdimensionen</span><span class="sxs-lookup"><span data-stu-id="ba6ef-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="ba6ef-108">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ba6ef-109">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ba6ef-110">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="ba6ef-111">Geben Sie im Feld "Neu" "Format basierend auf Finandimensions-Beispieldatenmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="ba6ef-112">Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="ba6ef-113">Geben Sie im Feld "Name" "Sachkontoerfassungbericht" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="ba6ef-114">Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="ba6ef-115">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-115">Click Create configuration.</span></span>
8. <span data-ttu-id="ba6ef-116">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-116">Click Designer.</span></span>
9. <span data-ttu-id="ba6ef-117">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="ba6ef-118">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="ba6ef-119">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="ba6ef-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-120">Click OK.</span></span>
13. <span data-ttu-id="ba6ef-121">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="ba6ef-122">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="ba6ef-123">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="ba6ef-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-124">Click OK.</span></span>
17. <span data-ttu-id="ba6ef-125">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="ba6ef-126">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="ba6ef-127">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="ba6ef-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-128">Click OK.</span></span>
21. <span data-ttu-id="ba6ef-129">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="ba6ef-130">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ba6ef-131">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="ba6ef-132">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="ba6ef-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-133">Click OK.</span></span>
26. <span data-ttu-id="ba6ef-134">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="ba6ef-135">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="ba6ef-136">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="ba6ef-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-137">Click OK.</span></span>
30. <span data-ttu-id="ba6ef-138">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="ba6ef-139">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="ba6ef-140">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="ba6ef-141">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="ba6ef-142">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-142">Click OK.</span></span>
35. <span data-ttu-id="ba6ef-143">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="ba6ef-144">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="ba6ef-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-145">Click OK.</span></span>
38. <span data-ttu-id="ba6ef-146">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="ba6ef-147">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="ba6ef-148">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-148">Click OK.</span></span>
41. <span data-ttu-id="ba6ef-149">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="ba6ef-150">Geben Sie im Feld Name "Dt" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="ba6ef-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-151">Click OK.</span></span>
44. <span data-ttu-id="ba6ef-152">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="ba6ef-153">Geben Sie im Feld Name "Ct" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="ba6ef-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-154">Click OK.</span></span>
47. <span data-ttu-id="ba6ef-155">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="ba6ef-156">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="ba6ef-157">Geben Sie im Feld "Name" "Dimensionen" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="ba6ef-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-158">Click OK.</span></span>
51. <span data-ttu-id="ba6ef-159">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="ba6ef-160">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="ba6ef-161">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="ba6ef-162">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="ba6ef-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-163">Click OK.</span></span>
56. <span data-ttu-id="ba6ef-164">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="ba6ef-165">Geben Sie im Feld 'Name' "Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="ba6ef-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-166">Click OK.</span></span>
59. <span data-ttu-id="ba6ef-167">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="ba6ef-168">Geben Sie im Feld Name "Desc" ein.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="ba6ef-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="ba6ef-170">Zuweisen von Berichtselementen zu Datenquellen</span><span class="sxs-lookup"><span data-stu-id="ba6ef-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="ba6ef-171">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ba6ef-172">In der Struktur erweitern Sie "Modell: Datenmodell-Finanzdimensionsbeispielmodell".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ba6ef-173">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="ba6ef-174">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="ba6ef-175">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="ba6ef-176">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="ba6ef-177">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Beschreibung: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="ba6ef-178">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-178">Click Bind.</span></span>
9. <span data-ttu-id="ba6ef-179">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Wert: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="ba6ef-180">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="ba6ef-181">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-181">Click Bind.</span></span>
12. <span data-ttu-id="ba6ef-182">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="ba6ef-183">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="ba6ef-184">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-184">Click Bind.</span></span>
15. <span data-ttu-id="ba6ef-185">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="ba6ef-186">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="ba6ef-187">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-187">Click Bind.</span></span>
18. <span data-ttu-id="ba6ef-188">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Ct: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="ba6ef-189">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Haben: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="ba6ef-190">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-190">Click Bind.</span></span>
21. <span data-ttu-id="ba6ef-191">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dt: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="ba6ef-192">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Soll: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="ba6ef-193">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-193">Click Bind.</span></span>
24. <span data-ttu-id="ba6ef-194">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Währung: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="ba6ef-195">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Währung: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="ba6ef-196">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-196">Click Bind.</span></span>
27. <span data-ttu-id="ba6ef-197">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Datum: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="ba6ef-198">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="ba6ef-199">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-199">Click Bind.</span></span>
30. <span data-ttu-id="ba6ef-200">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Beleg: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="ba6ef-201">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Beleg: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="ba6ef-202">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-202">Click Bind.</span></span>
33. <span data-ttu-id="ba6ef-203">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="ba6ef-204">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="ba6ef-205">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-205">Click Bind.</span></span>
36. <span data-ttu-id="ba6ef-206">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Charge: XML Attribut'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="ba6ef-207">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="ba6ef-208">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-208">Click Bind.</span></span>
39. <span data-ttu-id="ba6ef-209">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="ba6ef-210">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="ba6ef-211">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-211">Click Bind.</span></span>
42. <span data-ttu-id="ba6ef-212">Wählen Sie in der Strukturdarstellung "Root: XML Element\Unternehmen: XML-Attribut".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="ba6ef-213">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Unternehmen: String'.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="ba6ef-214">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-214">Click Bind.</span></span>
45. <span data-ttu-id="ba6ef-215">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ba6ef-215">Click Save.</span></span>
46. <span data-ttu-id="ba6ef-216">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ba6ef-216">Close the page.</span></span>

