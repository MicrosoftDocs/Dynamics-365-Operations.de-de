---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 3)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565237"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="8e21d-104">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 3: Berichtsentwurf)</span><span class="sxs-lookup"><span data-stu-id="8e21d-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e21d-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="8e21d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="8e21d-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="8e21d-107">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 2: Modellzuordnung)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e21d-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="8e21d-108">Entwerfen eines Berichts zur Darstellung von Finanzdimensionen</span><span class="sxs-lookup"><span data-stu-id="8e21d-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="8e21d-109">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8e21d-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8e21d-110">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="8e21d-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8e21d-111">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8e21d-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8e21d-112">Geben Sie im Feld "Neu" "Format basierend auf Finandimensions-Beispieldatenmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="8e21d-113">Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e21d-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="8e21d-114">Geben Sie im Feld "Name" "Sachkontoerfassungbericht" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="8e21d-115">Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.</span><span class="sxs-lookup"><span data-stu-id="8e21d-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="8e21d-116">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8e21d-116">Click Create configuration.</span></span>
8. <span data-ttu-id="8e21d-117">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8e21d-117">Click Designer.</span></span>
9. <span data-ttu-id="8e21d-118">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8e21d-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="8e21d-119">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="8e21d-120">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="8e21d-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-121">Click OK.</span></span>
13. <span data-ttu-id="8e21d-122">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="8e21d-123">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="8e21d-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="8e21d-124">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="8e21d-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-125">Click OK.</span></span>
17. <span data-ttu-id="8e21d-126">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="8e21d-127">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="8e21d-128">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="8e21d-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-129">Click OK.</span></span>
21. <span data-ttu-id="8e21d-130">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="8e21d-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="8e21d-131">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="8e21d-132">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="8e21d-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="8e21d-133">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="8e21d-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-134">Click OK.</span></span>
26. <span data-ttu-id="8e21d-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="8e21d-136">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="8e21d-137">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="8e21d-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-138">Click OK.</span></span>
30. <span data-ttu-id="8e21d-139">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="8e21d-140">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="8e21d-141">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="8e21d-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="8e21d-142">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="8e21d-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-143">Click OK.</span></span>
35. <span data-ttu-id="8e21d-144">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="8e21d-145">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="8e21d-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-146">Click OK.</span></span>
38. <span data-ttu-id="8e21d-147">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="8e21d-148">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="8e21d-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-149">Click OK.</span></span>
41. <span data-ttu-id="8e21d-150">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="8e21d-151">Geben Sie im Feld Name "Dt" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="8e21d-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-152">Click OK.</span></span>
44. <span data-ttu-id="8e21d-153">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="8e21d-154">Geben Sie im Feld Name "Ct" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="8e21d-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-155">Click OK.</span></span>
47. <span data-ttu-id="8e21d-156">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="8e21d-157">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="8e21d-158">Geben Sie im Feld "Name" "Dimensionen" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="8e21d-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-159">Click OK.</span></span>
51. <span data-ttu-id="8e21d-160">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="8e21d-161">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="8e21d-162">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="8e21d-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="8e21d-163">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="8e21d-164">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-164">Click OK.</span></span>
56. <span data-ttu-id="8e21d-165">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="8e21d-166">Geben Sie im Feld 'Name' "Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="8e21d-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-167">Click OK.</span></span>
59. <span data-ttu-id="8e21d-168">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8e21d-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="8e21d-169">Geben Sie im Feld Name "Desc" ein.</span><span class="sxs-lookup"><span data-stu-id="8e21d-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="8e21d-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e21d-170">Click OK.</span></span>
<span data-ttu-id="8e21d-171">![EB-Vorgangs-Designerseite](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="8e21d-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="8e21d-172">Zuweisen von Berichtselementen zu Datenquellen</span><span class="sxs-lookup"><span data-stu-id="8e21d-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="8e21d-173">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8e21d-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8e21d-174">In der Struktur erweitern Sie "Modell: Datenmodell-Finanzdimensionsbeispielmodell".</span><span class="sxs-lookup"><span data-stu-id="8e21d-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8e21d-175">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="8e21d-176">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="8e21d-177">In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="8e21d-178">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="8e21d-179">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Beschreibung: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="8e21d-180">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-180">Click Bind.</span></span>
9. <span data-ttu-id="8e21d-181">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Wert: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="8e21d-182">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="8e21d-183">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-183">Click Bind.</span></span>
12. <span data-ttu-id="8e21d-184">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="8e21d-185">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="8e21d-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-186">Click Bind.</span></span>
15. <span data-ttu-id="8e21d-187">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="8e21d-188">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="8e21d-189">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-189">Click Bind.</span></span>
18. <span data-ttu-id="8e21d-190">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Ct: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="8e21d-191">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Haben: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="8e21d-192">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-192">Click Bind.</span></span>
21. <span data-ttu-id="8e21d-193">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dt: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="8e21d-194">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Soll: Gleitkommazahl'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="8e21d-195">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-195">Click Bind.</span></span>
24. <span data-ttu-id="8e21d-196">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Währung: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="8e21d-197">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Währung: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="8e21d-198">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-198">Click Bind.</span></span>
27. <span data-ttu-id="8e21d-199">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Datum: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="8e21d-200">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="8e21d-201">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-201">Click Bind.</span></span>
30. <span data-ttu-id="8e21d-202">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Beleg: XML-Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="8e21d-203">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Beleg: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="8e21d-204">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-204">Click Bind.</span></span>
33. <span data-ttu-id="8e21d-205">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="8e21d-206">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="8e21d-207">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-207">Click Bind.</span></span>
36. <span data-ttu-id="8e21d-208">Wählen Sie in der Strukturdarstellung 'Root: XML Element\Charge: XML Attribut'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="8e21d-209">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="8e21d-210">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-210">Click Bind.</span></span>
39. <span data-ttu-id="8e21d-211">Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="8e21d-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="8e21d-212">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="8e21d-213">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-213">Click Bind.</span></span>
42. <span data-ttu-id="8e21d-214">Wählen Sie in der Strukturdarstellung "Root: XML Element\Unternehmen: XML-Attribut".</span><span class="sxs-lookup"><span data-stu-id="8e21d-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="8e21d-215">In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Unternehmen: String'.</span><span class="sxs-lookup"><span data-stu-id="8e21d-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="8e21d-216">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8e21d-216">Click Bind.</span></span>
45. <span data-ttu-id="8e21d-217">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="8e21d-217">Click Save.</span></span>
46. <span data-ttu-id="8e21d-218">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8e21d-218">Close the page.</span></span>
<span data-ttu-id="8e21d-219">![EB-Vorgangs-Designerseite](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="8e21d-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]