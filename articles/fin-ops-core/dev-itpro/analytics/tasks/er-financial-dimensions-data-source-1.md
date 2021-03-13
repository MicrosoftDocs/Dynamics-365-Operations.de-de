---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92d29d954debddd509eaba6b710f39b218da2c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092174"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="00493-104">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)</span><span class="sxs-lookup"><span data-stu-id="00493-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00493-105">In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="00493-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="00493-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="00493-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="00493-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="00493-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="00493-108">Neues Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="00493-108">Create a new data model</span></span>
1. <span data-ttu-id="00493-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="00493-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="00493-110">Überprüfen Sie, ob „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="00493-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="00493-111">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="00493-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="00493-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="00493-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="00493-113">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00493-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="00493-114">Geben Sie im Feld "Name" "Finanzdimensions-Beispielmodell" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="00493-115">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="00493-115">Click Create configuration.</span></span>
6. <span data-ttu-id="00493-116">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="00493-116">Click Designer.</span></span>
7. <span data-ttu-id="00493-117">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="00493-118">Geben Sie im Feld "Name" "Erfassung" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="00493-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-119">Click Add.</span></span>
10. <span data-ttu-id="00493-120">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="00493-121">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="00493-122">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-122">Click Add.</span></span>
    * <span data-ttu-id="00493-123">Wir fügen unserem Modell eine neue Datensatzliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="00493-123">We will add to our model a new record list.</span></span> <span data-ttu-id="00493-124">Diese Liste enthält die Einstellungen aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="00493-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="00493-125">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Einstellungen der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="00493-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="00493-126">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="00493-127">Geben Sie im Feld "Name" "Dimensionseinstellung" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="00493-128">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="00493-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="00493-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-129">Click Add.</span></span>
17. <span data-ttu-id="00493-130">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="00493-131">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="00493-132">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="00493-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="00493-133">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-133">Click Add.</span></span>
21. <span data-ttu-id="00493-134">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="00493-135">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="00493-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-136">Click Add.</span></span>
24. <span data-ttu-id="00493-137">Wählen Sie in der Struktur 'Erfassung' aus.</span><span class="sxs-lookup"><span data-stu-id="00493-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="00493-138">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="00493-139">Geben Sie im Feld "Name" "Journal" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="00493-140">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="00493-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="00493-141">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-141">Click Add.</span></span>
29. <span data-ttu-id="00493-142">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="00493-143">Geben Sie im Feld "Name" "Charge" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="00493-144">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="00493-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="00493-145">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-145">Click Add.</span></span>
33. <span data-ttu-id="00493-146">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="00493-147">Geben Sie im Feld "Name" "Buchung" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="00493-148">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="00493-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="00493-149">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-149">Click Add.</span></span>
37. <span data-ttu-id="00493-150">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="00493-151">Geben Sie im Feld "Name" "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="00493-152">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="00493-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="00493-153">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-153">Click Add.</span></span>
41. <span data-ttu-id="00493-154">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="00493-155">Geben Sie im Feld "Name" "Soll" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="00493-156">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="00493-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="00493-157">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-157">Click Add.</span></span>
45. <span data-ttu-id="00493-158">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="00493-159">Geben Sie im Feld "Name" "Haben" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="00493-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-160">Click Add.</span></span>
48. <span data-ttu-id="00493-161">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="00493-162">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="00493-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="00493-163">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="00493-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="00493-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-164">Click Add.</span></span>
52. <span data-ttu-id="00493-165">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="00493-166">Geben Sie im Feld "Name" "Beleg" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="00493-167">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-167">Click Add.</span></span>
55. <span data-ttu-id="00493-168">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="00493-169">Geben Sie im Feld "Name" "Dimensionsdaten" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="00493-170">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="00493-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="00493-171">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-171">Click Add.</span></span>
    * <span data-ttu-id="00493-172">Wir haben unserem Modell einen neue Datensatzliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="00493-172">We added to our model a new record list.</span></span> <span data-ttu-id="00493-173">Diese Liste enthält die Werte aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen).</span><span class="sxs-lookup"><span data-stu-id="00493-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="00493-174">Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Werte der Dimension angezeigen.</span><span class="sxs-lookup"><span data-stu-id="00493-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="00493-175">Der Dimensionsname wird auch in diesem Datensatz als nutzbares Feld angezeigt (z. B. zur Auswahl).</span><span class="sxs-lookup"><span data-stu-id="00493-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="00493-176">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="00493-177">Geben Sie im Feld "Name" "Code" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="00493-178">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="00493-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="00493-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-179">Click Add.</span></span>
63. <span data-ttu-id="00493-180">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="00493-181">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="00493-182">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-182">Click Add.</span></span>
66. <span data-ttu-id="00493-183">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00493-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="00493-184">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="00493-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="00493-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00493-185">Click Add.</span></span>
69. <span data-ttu-id="00493-186">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="00493-186">Click Save.</span></span>
70. <span data-ttu-id="00493-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="00493-187">Close the page.</span></span>

![ER Datenmodell Designerseite](../media/er-financial-dimensions-guides-data-model.png)

