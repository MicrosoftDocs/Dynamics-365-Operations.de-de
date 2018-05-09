--- 
title: Datenmodell zur Verwendung von Finanzdimensionen als Datenquelle entwerfen
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8b951546cb0cc0d0415f48c49e8b53c5f4720f9e
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source"></a><span data-ttu-id="2c919-103">Datenmodell zur Verwendung von Finanzdimensionen als Datenquelle entwerfen</span><span class="sxs-lookup"><span data-stu-id="2c919-103">Design data model to use financial dimensions as a data source</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c919-104">In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="2c919-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="2c919-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2c919-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="2c919-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="2c919-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="2c919-107">Neues Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="2c919-107">Create a new data model</span></span>
1. <span data-ttu-id="2c919-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="2c919-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2c919-109">Überprüfen Sie, ob "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="2c919-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="2c919-110">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="2c919-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="2c919-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="2c919-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2c919-112">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c919-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="2c919-113">Geben Sie im Feld "Name" "Finanzdimensions-Beispielmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="2c919-114">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c919-114">Click Create configuration.</span></span>
6. <span data-ttu-id="2c919-115">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="2c919-115">Click Designer.</span></span>
7. <span data-ttu-id="2c919-116">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="2c919-117">Geben Sie im Feld "Name" "Erfassung" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="2c919-118">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-118">Click Add.</span></span>
10. <span data-ttu-id="2c919-119">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="2c919-120">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="2c919-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-121">Click Add.</span></span>
    * <span data-ttu-id="2c919-122">Wir fügen unserem Modell eine neue Datensatzliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="2c919-122">We will add to our model a new record list.</span></span> <span data-ttu-id="2c919-123">Diese Liste enthält die Einstellungen aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="2c919-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="2c919-124">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Einstellungen der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="2c919-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="2c919-125">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="2c919-126">Geben Sie im Feld "Name" "Dimensionseinstellung" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="2c919-127">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="2c919-128">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-128">Click Add.</span></span>
17. <span data-ttu-id="2c919-129">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="2c919-130">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="2c919-131">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="2c919-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-132">Click Add.</span></span>
21. <span data-ttu-id="2c919-133">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="2c919-134">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="2c919-135">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-135">Click Add.</span></span>
24. <span data-ttu-id="2c919-136">Wählen Sie in der Struktur 'Erfassung' aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="2c919-137">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="2c919-138">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="2c919-139">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="2c919-140">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-140">Click Add.</span></span>
29. <span data-ttu-id="2c919-141">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="2c919-142">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="2c919-143">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="2c919-144">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-144">Click Add.</span></span>
33. <span data-ttu-id="2c919-145">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="2c919-146">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="2c919-147">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="2c919-148">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-148">Click Add.</span></span>
37. <span data-ttu-id="2c919-149">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="2c919-150">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="2c919-151">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="2c919-152">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-152">Click Add.</span></span>
41. <span data-ttu-id="2c919-153">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="2c919-154">Geben Sie im Feld "Name" "Soll" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="2c919-155">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="2c919-156">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-156">Click Add.</span></span>
45. <span data-ttu-id="2c919-157">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="2c919-158">Geben Sie im Feld "Name" "Haben" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="2c919-159">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-159">Click Add.</span></span>
48. <span data-ttu-id="2c919-160">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="2c919-161">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="2c919-162">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="2c919-163">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-163">Click Add.</span></span>
52. <span data-ttu-id="2c919-164">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="2c919-165">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="2c919-166">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-166">Click Add.</span></span>
55. <span data-ttu-id="2c919-167">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="2c919-168">Geben Sie im Feld "Name" "Dimensionsdaten" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="2c919-169">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="2c919-170">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-170">Click Add.</span></span>
    * <span data-ttu-id="2c919-171">Wir haben unserem Modell einen neue Datensatzliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2c919-171">We added to our model a new record list.</span></span> <span data-ttu-id="2c919-172">Diese Liste enthält die Werte aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="2c919-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="2c919-173">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Werte der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="2c919-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="2c919-174">Der Dimensionsname wird auch in diesem Datensatz als nutzbares Feld angezeigt (z. B. zur Auswahl).</span><span class="sxs-lookup"><span data-stu-id="2c919-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="2c919-175">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="2c919-176">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="2c919-177">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="2c919-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="2c919-178">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-178">Click Add.</span></span>
63. <span data-ttu-id="2c919-179">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="2c919-180">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="2c919-181">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-181">Click Add.</span></span>
66. <span data-ttu-id="2c919-182">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2c919-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="2c919-183">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="2c919-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="2c919-184">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c919-184">Click Add.</span></span>
69. <span data-ttu-id="2c919-185">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2c919-185">Click Save.</span></span>
70. <span data-ttu-id="2c919-186">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c919-186">Close the page.</span></span>


