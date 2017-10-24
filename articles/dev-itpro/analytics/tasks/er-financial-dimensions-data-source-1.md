--- 
title: "Entwerfen von Datenmodell zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.openlocfilehash: d8a03c4b85666975a7b42d46f3afdd35019e9b93
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="e8397-103">Entwerfen von Datenmodell zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="e8397-103">Design data model to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8397-104">In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="e8397-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e8397-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e8397-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e8397-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="e8397-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="e8397-107">Neues Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="e8397-107">Create a new data model</span></span>
1. <span data-ttu-id="e8397-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="e8397-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e8397-109">Überprüfen Sie, ob "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="e8397-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="e8397-110">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="e8397-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="e8397-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="e8397-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e8397-112">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e8397-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="e8397-113">Geben Sie im Feld "Name" "Finanzdimensions-Beispielmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="e8397-114">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8397-114">Click Create configuration.</span></span>
6. <span data-ttu-id="e8397-115">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="e8397-115">Click Designer.</span></span>
7. <span data-ttu-id="e8397-116">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e8397-117">Geben Sie im Feld "Name" "Erfassung" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="e8397-118">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-118">Click Add.</span></span>
10. <span data-ttu-id="e8397-119">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="e8397-120">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="e8397-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-121">Click Add.</span></span>
    * <span data-ttu-id="e8397-122">Wir fügen unserem Modell eine neue Datensatzliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8397-122">We will add to our model a new record list.</span></span> <span data-ttu-id="e8397-123">Diese Liste enthält die Einstellungen aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="e8397-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="e8397-124">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Einstellungen der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="e8397-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="e8397-125">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="e8397-126">Geben Sie im Feld "Name" "Dimensionseinstellung" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="e8397-127">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="e8397-128">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-128">Click Add.</span></span>
17. <span data-ttu-id="e8397-129">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="e8397-130">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="e8397-131">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="e8397-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-132">Click Add.</span></span>
21. <span data-ttu-id="e8397-133">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e8397-134">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="e8397-135">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-135">Click Add.</span></span>
24. <span data-ttu-id="e8397-136">Wählen Sie in der Struktur 'Erfassung' aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="e8397-137">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="e8397-138">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="e8397-139">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="e8397-140">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-140">Click Add.</span></span>
29. <span data-ttu-id="e8397-141">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="e8397-142">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="e8397-143">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="e8397-144">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-144">Click Add.</span></span>
33. <span data-ttu-id="e8397-145">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="e8397-146">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="e8397-147">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="e8397-148">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-148">Click Add.</span></span>
37. <span data-ttu-id="e8397-149">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="e8397-150">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="e8397-151">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="e8397-152">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-152">Click Add.</span></span>
41. <span data-ttu-id="e8397-153">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="e8397-154">Geben Sie im Feld "Name" "Soll" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="e8397-155">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="e8397-156">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-156">Click Add.</span></span>
45. <span data-ttu-id="e8397-157">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="e8397-158">Geben Sie im Feld "Name" "Haben" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="e8397-159">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-159">Click Add.</span></span>
48. <span data-ttu-id="e8397-160">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="e8397-161">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="e8397-162">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="e8397-163">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-163">Click Add.</span></span>
52. <span data-ttu-id="e8397-164">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="e8397-165">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="e8397-166">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-166">Click Add.</span></span>
55. <span data-ttu-id="e8397-167">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="e8397-168">Geben Sie im Feld "Name" "Dimensionsdaten" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="e8397-169">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="e8397-170">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-170">Click Add.</span></span>
    * <span data-ttu-id="e8397-171">Wir haben unserem Modell einen neue Datensatzliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e8397-171">We added to our model a new record list.</span></span> <span data-ttu-id="e8397-172">Diese Liste enthält die Werte aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="e8397-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="e8397-173">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Werte der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="e8397-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="e8397-174">Der Dimensionsname wird auch in diesem Datensatz als nutzbares Feld angezeigt (z. B. zur Auswahl).</span><span class="sxs-lookup"><span data-stu-id="e8397-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="e8397-175">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="e8397-176">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="e8397-177">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="e8397-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="e8397-178">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-178">Click Add.</span></span>
63. <span data-ttu-id="e8397-179">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="e8397-180">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="e8397-181">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-181">Click Add.</span></span>
66. <span data-ttu-id="e8397-182">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e8397-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="e8397-183">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="e8397-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="e8397-184">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8397-184">Click Add.</span></span>
69. <span data-ttu-id="e8397-185">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e8397-185">Click Save.</span></span>
70. <span data-ttu-id="e8397-186">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e8397-186">Close the page.</span></span>


