---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570191"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="fe7b4-104">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)</span><span class="sxs-lookup"><span data-stu-id="fe7b4-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe7b4-105">In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fe7b4-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="fe7b4-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="fe7b4-108">Neues Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="fe7b4-108">Create a new data model</span></span>
1. <span data-ttu-id="fe7b4-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fe7b4-110">Überprüfen Sie, ob „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="fe7b4-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="fe7b4-111">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="fe7b4-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="fe7b4-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="fe7b4-113">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="fe7b4-114">Geben Sie im Feld "Name" "Finanzdimensions-Beispielmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="fe7b4-115">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-115">Click Create configuration.</span></span>
6. <span data-ttu-id="fe7b4-116">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-116">Click Designer.</span></span>
7. <span data-ttu-id="fe7b4-117">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="fe7b4-118">Geben Sie im Feld "Name" "Erfassung" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="fe7b4-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-119">Click Add.</span></span>
10. <span data-ttu-id="fe7b4-120">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="fe7b4-121">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="fe7b4-122">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-122">Click Add.</span></span>
    * <span data-ttu-id="fe7b4-123">Wir fügen unserem Modell eine neue Datensatzliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-123">We will add to our model a new record list.</span></span> <span data-ttu-id="fe7b4-124">Diese Liste enthält die Einstellungen aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="fe7b4-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="fe7b4-125">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Einstellungen der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="fe7b4-126">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="fe7b4-127">Geben Sie im Feld "Name" "Dimensionseinstellung" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="fe7b4-128">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="fe7b4-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-129">Click Add.</span></span>
17. <span data-ttu-id="fe7b4-130">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="fe7b4-131">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="fe7b4-132">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="fe7b4-133">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-133">Click Add.</span></span>
21. <span data-ttu-id="fe7b4-134">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="fe7b4-135">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="fe7b4-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-136">Click Add.</span></span>
24. <span data-ttu-id="fe7b4-137">Wählen Sie in der Struktur 'Erfassung' aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="fe7b4-138">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="fe7b4-139">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="fe7b4-140">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="fe7b4-141">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-141">Click Add.</span></span>
29. <span data-ttu-id="fe7b4-142">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="fe7b4-143">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="fe7b4-144">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="fe7b4-145">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-145">Click Add.</span></span>
33. <span data-ttu-id="fe7b4-146">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="fe7b4-147">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="fe7b4-148">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="fe7b4-149">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-149">Click Add.</span></span>
37. <span data-ttu-id="fe7b4-150">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="fe7b4-151">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="fe7b4-152">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="fe7b4-153">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-153">Click Add.</span></span>
41. <span data-ttu-id="fe7b4-154">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="fe7b4-155">Geben Sie im Feld "Name" "Soll" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="fe7b4-156">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="fe7b4-157">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-157">Click Add.</span></span>
45. <span data-ttu-id="fe7b4-158">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="fe7b4-159">Geben Sie im Feld "Name" "Haben" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="fe7b4-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-160">Click Add.</span></span>
48. <span data-ttu-id="fe7b4-161">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="fe7b4-162">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="fe7b4-163">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="fe7b4-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-164">Click Add.</span></span>
52. <span data-ttu-id="fe7b4-165">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="fe7b4-166">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="fe7b4-167">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-167">Click Add.</span></span>
55. <span data-ttu-id="fe7b4-168">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="fe7b4-169">Geben Sie im Feld "Name" "Dimensionsdaten" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="fe7b4-170">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="fe7b4-171">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-171">Click Add.</span></span>
    * <span data-ttu-id="fe7b4-172">Wir haben unserem Modell einen neue Datensatzliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-172">We added to our model a new record list.</span></span> <span data-ttu-id="fe7b4-173">Diese Liste enthält die Werte aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="fe7b4-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="fe7b4-174">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Werte der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="fe7b4-175">Der Dimensionsname wird auch in diesem Datensatz als nutzbares Feld angezeigt (z. B. zur Auswahl).</span><span class="sxs-lookup"><span data-stu-id="fe7b4-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="fe7b4-176">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="fe7b4-177">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="fe7b4-178">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="fe7b4-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-179">Click Add.</span></span>
63. <span data-ttu-id="fe7b4-180">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="fe7b4-181">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="fe7b4-182">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-182">Click Add.</span></span>
66. <span data-ttu-id="fe7b4-183">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="fe7b4-184">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="fe7b4-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-185">Click Add.</span></span>
69. <span data-ttu-id="fe7b4-186">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-186">Click Save.</span></span>
70. <span data-ttu-id="fe7b4-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fe7b4-187">Close the page.</span></span>

![ER Datenmodell Designerseite](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]