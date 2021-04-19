---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 1)
author: NickSelin
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
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752459"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="72c02-104">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)</span><span class="sxs-lookup"><span data-stu-id="72c02-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72c02-105">In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="72c02-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="72c02-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="72c02-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="72c02-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="72c02-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="72c02-108">Neues Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="72c02-108">Create a new data model</span></span>
1. <span data-ttu-id="72c02-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="72c02-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="72c02-110">Überprüfen Sie, ob „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="72c02-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="72c02-111">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="72c02-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="72c02-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="72c02-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="72c02-113">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="72c02-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="72c02-114">Geben Sie im Feld "Name" "Finanzdimensions-Beispielmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="72c02-115">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="72c02-115">Click Create configuration.</span></span>
6. <span data-ttu-id="72c02-116">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="72c02-116">Click Designer.</span></span>
7. <span data-ttu-id="72c02-117">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="72c02-118">Geben Sie im Feld "Name" "Erfassung" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="72c02-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-119">Click Add.</span></span>
10. <span data-ttu-id="72c02-120">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="72c02-121">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="72c02-122">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-122">Click Add.</span></span>
    * <span data-ttu-id="72c02-123">Wir fügen unserem Modell eine neue Datensatzliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="72c02-123">We will add to our model a new record list.</span></span> <span data-ttu-id="72c02-124">Diese Liste enthält die Einstellungen aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="72c02-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="72c02-125">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Einstellungen der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="72c02-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="72c02-126">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="72c02-127">Geben Sie im Feld "Name" "Dimensionseinstellung" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="72c02-128">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="72c02-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-129">Click Add.</span></span>
17. <span data-ttu-id="72c02-130">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="72c02-131">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="72c02-132">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="72c02-133">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-133">Click Add.</span></span>
21. <span data-ttu-id="72c02-134">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="72c02-135">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="72c02-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-136">Click Add.</span></span>
24. <span data-ttu-id="72c02-137">Wählen Sie in der Struktur 'Erfassung' aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="72c02-138">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="72c02-139">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="72c02-140">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="72c02-141">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-141">Click Add.</span></span>
29. <span data-ttu-id="72c02-142">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="72c02-143">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="72c02-144">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="72c02-145">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-145">Click Add.</span></span>
33. <span data-ttu-id="72c02-146">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="72c02-147">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="72c02-148">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="72c02-149">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-149">Click Add.</span></span>
37. <span data-ttu-id="72c02-150">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="72c02-151">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="72c02-152">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="72c02-153">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-153">Click Add.</span></span>
41. <span data-ttu-id="72c02-154">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="72c02-155">Geben Sie im Feld "Name" "Soll" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="72c02-156">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="72c02-157">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-157">Click Add.</span></span>
45. <span data-ttu-id="72c02-158">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="72c02-159">Geben Sie im Feld "Name" "Haben" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="72c02-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-160">Click Add.</span></span>
48. <span data-ttu-id="72c02-161">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="72c02-162">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="72c02-163">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="72c02-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-164">Click Add.</span></span>
52. <span data-ttu-id="72c02-165">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="72c02-166">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="72c02-167">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-167">Click Add.</span></span>
55. <span data-ttu-id="72c02-168">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="72c02-169">Geben Sie im Feld "Name" "Dimensionsdaten" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="72c02-170">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="72c02-171">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-171">Click Add.</span></span>
    * <span data-ttu-id="72c02-172">Wir haben unserem Modell einen neue Datensatzliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="72c02-172">We added to our model a new record list.</span></span> <span data-ttu-id="72c02-173">Diese Liste enthält die Werte aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="72c02-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="72c02-174">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Werte der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="72c02-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="72c02-175">Der Dimensionsname wird auch in diesem Datensatz als nutzbares Feld angezeigt (z. B. zur Auswahl).</span><span class="sxs-lookup"><span data-stu-id="72c02-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="72c02-176">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="72c02-177">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="72c02-178">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="72c02-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="72c02-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-179">Click Add.</span></span>
63. <span data-ttu-id="72c02-180">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="72c02-181">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="72c02-182">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-182">Click Add.</span></span>
66. <span data-ttu-id="72c02-183">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="72c02-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="72c02-184">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="72c02-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="72c02-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72c02-185">Click Add.</span></span>
69. <span data-ttu-id="72c02-186">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="72c02-186">Click Save.</span></span>
70. <span data-ttu-id="72c02-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="72c02-187">Close the page.</span></span>

![ER Datenmodell Designerseite](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]