--- 
title: ER Erstellen eine Formatkonfiguration (November 2016)
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="3202b-103">ER Erstellen eine Formatkonfiguration (November 2016)</span><span class="sxs-lookup"><span data-stu-id="3202b-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3202b-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="3202b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="3202b-105">Diese Formatkonfiguration definiert das Format von elektronischen Dokumenten, die für die Verarbeitung von Zahlungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3202b-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="3202b-106">In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen Litware, Inc. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur "Modell für ausgewählte Datenquellen zuweisen abschließen".</span><span class="sxs-lookup"><span data-stu-id="3202b-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="3202b-107">Dient zum Erstellen einer neuen Format-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3202b-107">Create a new format configuration</span></span>
1. <span data-ttu-id="3202b-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="3202b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3202b-109">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="3202b-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3202b-110">Wählen Sie 'Zahlungen (vereinfachtes Modell)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="3202b-111">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3202b-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="3202b-112">Wählen Sie im neuen Feld geben Sie "Format auf Grundlage Datenmodell PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="3202b-113">Geben Sie im Feld "Name" "BACS (Großbritannien fiktiv)" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="3202b-114">BACS (Großbritannien fiktiven Namens)</span><span class="sxs-lookup"><span data-stu-id="3202b-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="3202b-115">Geben Sie im Textfeld "BACS-Kreditorenzahlungsformat (Großbritannien fiktiven Namens)" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="3202b-116">BACS-Kreditorenzahlungsformat (Großbritannien fiktiven Namens)</span><span class="sxs-lookup"><span data-stu-id="3202b-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="3202b-117">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="3202b-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="3202b-118">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="3202b-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="3202b-119">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3202b-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="3202b-120">Ein spezielles Format elektronischer Dokumente kann definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3202b-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="3202b-121">Lassen Sie das Feld leer, wenn Sie ein Format zur Laufzeit auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="3202b-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="3202b-122">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="3202b-123">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="3202b-123">Click Create configuration.</span></span>
    * <span data-ttu-id="3202b-124">Ein neuer Konfiguration wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="3202b-124">A new configuration has been created.</span></span> <span data-ttu-id="3202b-125">Die Entwurfsversion kann verwendet werden, um das Designformat für die Verwaltung von elektronischen Dokumenten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3202b-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="3202b-126">Entwerfen Sie Format elektronischer Dokumente</span><span class="sxs-lookup"><span data-stu-id="3202b-126">Design format of electronic document</span></span>
1. <span data-ttu-id="3202b-127">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="3202b-127">Click Designer.</span></span>
2. <span data-ttu-id="3202b-128">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3202b-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="3202b-129">Wählen Sie in der Struktur 'Common\File' aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="3202b-130">Geben Sie im Feld Name "Xml" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="3202b-131">XML</span><span class="sxs-lookup"><span data-stu-id="3202b-131">Xml</span></span>  
5. <span data-ttu-id="3202b-132">Geben Sie im Feld Kodierung "UTF-8" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="3202b-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="3202b-133">UTF-8</span></span>  
6. <span data-ttu-id="3202b-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-134">Click OK.</span></span>
7. <span data-ttu-id="3202b-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="3202b-136">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="3202b-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="3202b-137">Geben Sie im Feld Name "Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="3202b-138">Nachricht</span><span class="sxs-lookup"><span data-stu-id="3202b-138">Message</span></span>  
10. <span data-ttu-id="3202b-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-139">Click OK.</span></span>
11. <span data-ttu-id="3202b-140">Wählen Sie in der Struktur „XML\Nachricht” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="3202b-141">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-141">Click Add Element.</span></span>
13. <span data-ttu-id="3202b-142">Geben Sie im Feld "Name" 'ProcessingDate' ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="3202b-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="3202b-143">ProcessingDate</span></span>  
14. <span data-ttu-id="3202b-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-144">Click OK.</span></span>
15. <span data-ttu-id="3202b-145">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-145">Click Add Element.</span></span>
16. <span data-ttu-id="3202b-146">Geben Sie im Feld Name "MessageId" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="3202b-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="3202b-147">MessageId</span></span>  
17. <span data-ttu-id="3202b-148">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-148">Click OK.</span></span>
18. <span data-ttu-id="3202b-149">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-149">Click Add Element.</span></span>
19. <span data-ttu-id="3202b-150">Geben Sie im Feld "Name" "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="3202b-151">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="3202b-151">Payments</span></span>  
20. <span data-ttu-id="3202b-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-152">Click OK.</span></span>
21. <span data-ttu-id="3202b-153">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="3202b-154">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-154">Click Add Element.</span></span>
23. <span data-ttu-id="3202b-155">Geben Sie im Feld Name "Item" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="3202b-156">Artikel</span><span class="sxs-lookup"><span data-stu-id="3202b-156">Item</span></span>  
24. <span data-ttu-id="3202b-157">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-157">Click OK.</span></span>
25. <span data-ttu-id="3202b-158">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="3202b-159">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="3202b-160">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="3202b-161">Geben Sie im Feld Name "Id" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="3202b-162">Kennung</span><span class="sxs-lookup"><span data-stu-id="3202b-162">Id</span></span>  
29. <span data-ttu-id="3202b-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-163">Click OK.</span></span>
30. <span data-ttu-id="3202b-164">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="3202b-165">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="3202b-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="3202b-166">Geben Sie im Feld Name "Vendor" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="3202b-167">Lieferant</span><span class="sxs-lookup"><span data-stu-id="3202b-167">Vendor</span></span>  
33. <span data-ttu-id="3202b-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-168">Click OK.</span></span>
34. <span data-ttu-id="3202b-169">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="3202b-170">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-170">Click Add Element.</span></span>
36. <span data-ttu-id="3202b-171">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="3202b-172">Name</span><span class="sxs-lookup"><span data-stu-id="3202b-172">Name</span></span>  
37. <span data-ttu-id="3202b-173">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-173">Click OK.</span></span>
38. <span data-ttu-id="3202b-174">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-174">Click Add Element.</span></span>
39. <span data-ttu-id="3202b-175">Geben Sie im Feld Name "Bank" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="3202b-176">Bank</span><span class="sxs-lookup"><span data-stu-id="3202b-176">Bank</span></span>  
40. <span data-ttu-id="3202b-177">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-177">Click OK.</span></span>
41. <span data-ttu-id="3202b-178">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="3202b-179">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-179">Click Add Element.</span></span>
43. <span data-ttu-id="3202b-180">Geben Sie im Feld "Name" "RoutingNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="3202b-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="3202b-181">RoutingNumber</span></span>  
44. <span data-ttu-id="3202b-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-182">Click OK.</span></span>
45. <span data-ttu-id="3202b-183">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-183">Click Add Element.</span></span>
46. <span data-ttu-id="3202b-184">Geben Sie im Feld "Name" "AccountNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="3202b-185">AccountNumber-</span><span class="sxs-lookup"><span data-stu-id="3202b-185">AccountNumber</span></span>  
47. <span data-ttu-id="3202b-186">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-186">Click OK.</span></span>
48. <span data-ttu-id="3202b-187">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="3202b-188">Klicken Sie auf Kopieren.</span><span class="sxs-lookup"><span data-stu-id="3202b-188">Click Copy.</span></span>
50. <span data-ttu-id="3202b-189">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="3202b-190">Klicken Sie auf Einfügen.</span><span class="sxs-lookup"><span data-stu-id="3202b-190">Click Paste.</span></span>
52. <span data-ttu-id="3202b-191">Geben Sie im Feld Name "Zahler" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="3202b-192">Zahlender</span><span class="sxs-lookup"><span data-stu-id="3202b-192">Payer</span></span>  
53. <span data-ttu-id="3202b-193">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="3202b-194">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-194">Click Add Element.</span></span>
55. <span data-ttu-id="3202b-195">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="3202b-196">Währung</span><span class="sxs-lookup"><span data-stu-id="3202b-196">Currency</span></span>  
56. <span data-ttu-id="3202b-197">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-197">Click OK.</span></span>
57. <span data-ttu-id="3202b-198">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-198">Click Add Element.</span></span>
58. <span data-ttu-id="3202b-199">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="3202b-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3202b-200">Description</span></span>  
59. <span data-ttu-id="3202b-201">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-201">Click OK.</span></span>
60. <span data-ttu-id="3202b-202">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-202">Click Add Element.</span></span>
61. <span data-ttu-id="3202b-203">Geben Sie im Feld "Name" 'TransDate' ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="3202b-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="3202b-204">TransDate</span></span>  
62. <span data-ttu-id="3202b-205">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-205">Click OK.</span></span>
63. <span data-ttu-id="3202b-206">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-206">Click Add Element.</span></span>
64. <span data-ttu-id="3202b-207">Geben Sie im Feld Namen "Amount" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="3202b-208">Dauer</span><span class="sxs-lookup"><span data-stu-id="3202b-208">Amount</span></span>  
65. <span data-ttu-id="3202b-209">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="3202b-210">Bereiten Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen vor</span><span class="sxs-lookup"><span data-stu-id="3202b-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="3202b-211">Wählen Sie in der Struktur „XML\Nachricht\ProcessingDate” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="3202b-212">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="3202b-213">Wählen Sie in der Struktur „Text\DateTime” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="3202b-214">Geben Sie im Feld "Format" "yyyy-MM-dd" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="3202b-215">jjjj-MM-tt</span><span class="sxs-lookup"><span data-stu-id="3202b-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="3202b-216">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-216">Click OK.</span></span>
6. <span data-ttu-id="3202b-217">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\TransDate” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="3202b-218">Klicken Sie auf „DateTime hinzufügen”.</span><span class="sxs-lookup"><span data-stu-id="3202b-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="3202b-219">Geben Sie im Feld "Format" "yyyy-MM-dd" ein.</span><span class="sxs-lookup"><span data-stu-id="3202b-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="3202b-220">jjjj-MM-tt</span><span class="sxs-lookup"><span data-stu-id="3202b-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="3202b-221">Wählen Sie im Feld DateTime-Typ die Option „Date” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="3202b-222">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-222">Click OK.</span></span>
11. <span data-ttu-id="3202b-223">Wählen Sie in der Struktur „XML\Nachricht\MessageId” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="3202b-224">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="3202b-225">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="3202b-226">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-226">Click OK.</span></span>
15. <span data-ttu-id="3202b-227">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Name” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="3202b-228">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-228">Click Add String.</span></span>
17. <span data-ttu-id="3202b-229">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-229">Click OK.</span></span>
18. <span data-ttu-id="3202b-230">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="3202b-231">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-231">Click Add String.</span></span>
20. <span data-ttu-id="3202b-232">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-232">Click OK.</span></span>
21. <span data-ttu-id="3202b-233">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="3202b-234">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-234">Click Add String.</span></span>
23. <span data-ttu-id="3202b-235">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-235">Click OK.</span></span>
24. <span data-ttu-id="3202b-236">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Name” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="3202b-237">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-237">Click Add String.</span></span>
26. <span data-ttu-id="3202b-238">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-238">Click OK.</span></span>
27. <span data-ttu-id="3202b-239">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="3202b-240">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-240">Click Add String.</span></span>
29. <span data-ttu-id="3202b-241">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-241">Click OK.</span></span>
30. <span data-ttu-id="3202b-242">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="3202b-243">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-243">Click Add String.</span></span>
32. <span data-ttu-id="3202b-244">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-244">Click OK.</span></span>
33. <span data-ttu-id="3202b-245">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Währung” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="3202b-246">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-246">Click Add String.</span></span>
35. <span data-ttu-id="3202b-247">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-247">Click OK.</span></span>
36. <span data-ttu-id="3202b-248">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Beschreibung” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="3202b-249">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-249">Click Add String.</span></span>
38. <span data-ttu-id="3202b-250">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-250">Click OK.</span></span>
39. <span data-ttu-id="3202b-251">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Betrag” aus.</span><span class="sxs-lookup"><span data-stu-id="3202b-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="3202b-252">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3202b-252">Click Add String.</span></span>
41. <span data-ttu-id="3202b-253">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3202b-253">Click OK.</span></span>
42. <span data-ttu-id="3202b-254">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="3202b-254">Click Save.</span></span>
43. <span data-ttu-id="3202b-255">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3202b-255">Close the page.</span></span>


