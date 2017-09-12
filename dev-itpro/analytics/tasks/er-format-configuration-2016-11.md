--- 
title: Erstellen einer Formatkonfiguration zur elektronischen Berichterstellung (ER)
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="5f9b8-103">Erstellen einer Formatkonfiguration zur elektronischen Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="5f9b8-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f9b8-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="5f9b8-105">Diese Formatkonfiguration definiert das Format von elektronischen Dokumenten, die für die Verarbeitung von Zahlungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="5f9b8-106">In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen Litware, Inc. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur "Modell für ausgewählte Datenquellen zuweisen abschließen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="5f9b8-107">Dient zum Erstellen einer neuen Format-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-107">Create a new format configuration</span></span>
1. <span data-ttu-id="5f9b8-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5f9b8-109">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5f9b8-110">Wählen Sie 'Zahlungen (vereinfachtes Modell)' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="5f9b8-111">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="5f9b8-112">Wählen Sie im neuen Feld geben Sie "Format auf Grundlage Datenmodell PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="5f9b8-113">Geben Sie im Feld "Name" "BACS (Großbritannien fiktiv)" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="5f9b8-114">BACS (Großbritannien fiktiven Namens)</span><span class="sxs-lookup"><span data-stu-id="5f9b8-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="5f9b8-115">Geben Sie im Textfeld "BACS-Kreditorenzahlungsformat (Großbritannien fiktiven Namens)" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="5f9b8-116">BACS-Kreditorenzahlungsformat (Großbritannien fiktiven Namens)</span><span class="sxs-lookup"><span data-stu-id="5f9b8-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="5f9b8-117">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5f9b8-118">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5f9b8-119">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="5f9b8-120">Ein spezielles Format elektronischer Dokumente kann definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="5f9b8-121">Lassen Sie das Feld leer, wenn Sie ein Format zur Laufzeit auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="5f9b8-122">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="5f9b8-123">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-123">Click Create configuration.</span></span>
    * <span data-ttu-id="5f9b8-124">Ein neuer Konfiguration wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-124">A new configuration has been created.</span></span> <span data-ttu-id="5f9b8-125">Die Entwurfsversion kann verwendet werden, um das Designformat für die Verwaltung von elektronischen Dokumenten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="5f9b8-126">Entwerfen Sie Format elektronischer Dokumente</span><span class="sxs-lookup"><span data-stu-id="5f9b8-126">Design format of electronic document</span></span>
1. <span data-ttu-id="5f9b8-127">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-127">Click Designer.</span></span>
2. <span data-ttu-id="5f9b8-128">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="5f9b8-129">Wählen Sie in der Struktur 'Common\File' aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="5f9b8-130">Geben Sie im Feld Name "Xml" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="5f9b8-131">XML</span><span class="sxs-lookup"><span data-stu-id="5f9b8-131">Xml</span></span>  
5. <span data-ttu-id="5f9b8-132">Geben Sie im Feld Kodierung "UTF-8" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="5f9b8-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="5f9b8-133">UTF-8</span></span>  
6. <span data-ttu-id="5f9b8-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-134">Click OK.</span></span>
7. <span data-ttu-id="5f9b8-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="5f9b8-136">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="5f9b8-137">Geben Sie im Feld Name "Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="5f9b8-138">Nachricht</span><span class="sxs-lookup"><span data-stu-id="5f9b8-138">Message</span></span>  
10. <span data-ttu-id="5f9b8-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-139">Click OK.</span></span>
11. <span data-ttu-id="5f9b8-140">Wählen Sie in der Struktur „XML\Nachricht” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="5f9b8-141">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-141">Click Add Element.</span></span>
13. <span data-ttu-id="5f9b8-142">Geben Sie im Feld "Name" 'ProcessingDate' ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="5f9b8-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="5f9b8-143">ProcessingDate</span></span>  
14. <span data-ttu-id="5f9b8-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-144">Click OK.</span></span>
15. <span data-ttu-id="5f9b8-145">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-145">Click Add Element.</span></span>
16. <span data-ttu-id="5f9b8-146">Geben Sie im Feld Name "MessageId" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="5f9b8-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="5f9b8-147">MessageId</span></span>  
17. <span data-ttu-id="5f9b8-148">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-148">Click OK.</span></span>
18. <span data-ttu-id="5f9b8-149">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-149">Click Add Element.</span></span>
19. <span data-ttu-id="5f9b8-150">Geben Sie im Feld "Name" "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="5f9b8-151">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="5f9b8-151">Payments</span></span>  
20. <span data-ttu-id="5f9b8-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-152">Click OK.</span></span>
21. <span data-ttu-id="5f9b8-153">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="5f9b8-154">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-154">Click Add Element.</span></span>
23. <span data-ttu-id="5f9b8-155">Geben Sie im Feld Name "Item" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="5f9b8-156">Artikel</span><span class="sxs-lookup"><span data-stu-id="5f9b8-156">Item</span></span>  
24. <span data-ttu-id="5f9b8-157">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-157">Click OK.</span></span>
25. <span data-ttu-id="5f9b8-158">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="5f9b8-159">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="5f9b8-160">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="5f9b8-161">Geben Sie im Feld Name "Id" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="5f9b8-162">Kennung</span><span class="sxs-lookup"><span data-stu-id="5f9b8-162">Id</span></span>  
29. <span data-ttu-id="5f9b8-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-163">Click OK.</span></span>
30. <span data-ttu-id="5f9b8-164">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="5f9b8-165">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="5f9b8-166">Geben Sie im Feld Name "Vendor" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="5f9b8-167">Lieferant</span><span class="sxs-lookup"><span data-stu-id="5f9b8-167">Vendor</span></span>  
33. <span data-ttu-id="5f9b8-168">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-168">Click OK.</span></span>
34. <span data-ttu-id="5f9b8-169">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="5f9b8-170">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-170">Click Add Element.</span></span>
36. <span data-ttu-id="5f9b8-171">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="5f9b8-172">Name</span><span class="sxs-lookup"><span data-stu-id="5f9b8-172">Name</span></span>  
37. <span data-ttu-id="5f9b8-173">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-173">Click OK.</span></span>
38. <span data-ttu-id="5f9b8-174">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-174">Click Add Element.</span></span>
39. <span data-ttu-id="5f9b8-175">Geben Sie im Feld Name "Bank" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="5f9b8-176">Bank</span><span class="sxs-lookup"><span data-stu-id="5f9b8-176">Bank</span></span>  
40. <span data-ttu-id="5f9b8-177">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-177">Click OK.</span></span>
41. <span data-ttu-id="5f9b8-178">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="5f9b8-179">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-179">Click Add Element.</span></span>
43. <span data-ttu-id="5f9b8-180">Geben Sie im Feld "Name" "RoutingNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="5f9b8-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="5f9b8-181">RoutingNumber</span></span>  
44. <span data-ttu-id="5f9b8-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-182">Click OK.</span></span>
45. <span data-ttu-id="5f9b8-183">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-183">Click Add Element.</span></span>
46. <span data-ttu-id="5f9b8-184">Geben Sie im Feld "Name" "AccountNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="5f9b8-185">AccountNumber-</span><span class="sxs-lookup"><span data-stu-id="5f9b8-185">AccountNumber</span></span>  
47. <span data-ttu-id="5f9b8-186">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-186">Click OK.</span></span>
48. <span data-ttu-id="5f9b8-187">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="5f9b8-188">Klicken Sie auf Kopieren.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-188">Click Copy.</span></span>
50. <span data-ttu-id="5f9b8-189">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="5f9b8-190">Klicken Sie auf Einfügen.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-190">Click Paste.</span></span>
52. <span data-ttu-id="5f9b8-191">Geben Sie im Feld Name "Zahler" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="5f9b8-192">Zahlender</span><span class="sxs-lookup"><span data-stu-id="5f9b8-192">Payer</span></span>  
53. <span data-ttu-id="5f9b8-193">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="5f9b8-194">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-194">Click Add Element.</span></span>
55. <span data-ttu-id="5f9b8-195">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="5f9b8-196">Währung</span><span class="sxs-lookup"><span data-stu-id="5f9b8-196">Currency</span></span>  
56. <span data-ttu-id="5f9b8-197">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-197">Click OK.</span></span>
57. <span data-ttu-id="5f9b8-198">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-198">Click Add Element.</span></span>
58. <span data-ttu-id="5f9b8-199">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="5f9b8-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f9b8-200">Description</span></span>  
59. <span data-ttu-id="5f9b8-201">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-201">Click OK.</span></span>
60. <span data-ttu-id="5f9b8-202">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-202">Click Add Element.</span></span>
61. <span data-ttu-id="5f9b8-203">Geben Sie im Feld "Name" 'TransDate' ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="5f9b8-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="5f9b8-204">TransDate</span></span>  
62. <span data-ttu-id="5f9b8-205">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-205">Click OK.</span></span>
63. <span data-ttu-id="5f9b8-206">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-206">Click Add Element.</span></span>
64. <span data-ttu-id="5f9b8-207">Geben Sie im Feld Namen "Amount" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="5f9b8-208">Dauer</span><span class="sxs-lookup"><span data-stu-id="5f9b8-208">Amount</span></span>  
65. <span data-ttu-id="5f9b8-209">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="5f9b8-210">Bereiten Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen vor</span><span class="sxs-lookup"><span data-stu-id="5f9b8-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="5f9b8-211">Wählen Sie in der Struktur „XML\Nachricht\ProcessingDate” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="5f9b8-212">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="5f9b8-213">Wählen Sie in der Struktur „Text\DateTime” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="5f9b8-214">Geben Sie im Feld "Format" "yyyy-MM-dd" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="5f9b8-215">jjjj-MM-tt</span><span class="sxs-lookup"><span data-stu-id="5f9b8-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="5f9b8-216">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-216">Click OK.</span></span>
6. <span data-ttu-id="5f9b8-217">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\TransDate” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="5f9b8-218">Klicken Sie auf „DateTime hinzufügen”.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="5f9b8-219">Geben Sie im Feld "Format" "yyyy-MM-dd" ein.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="5f9b8-220">jjjj-MM-tt</span><span class="sxs-lookup"><span data-stu-id="5f9b8-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="5f9b8-221">Wählen Sie im Feld DateTime-Typ die Option „Date” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="5f9b8-222">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-222">Click OK.</span></span>
11. <span data-ttu-id="5f9b8-223">Wählen Sie in der Struktur „XML\Nachricht\MessageId” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="5f9b8-224">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="5f9b8-225">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="5f9b8-226">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-226">Click OK.</span></span>
15. <span data-ttu-id="5f9b8-227">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Name” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="5f9b8-228">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-228">Click Add String.</span></span>
17. <span data-ttu-id="5f9b8-229">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-229">Click OK.</span></span>
18. <span data-ttu-id="5f9b8-230">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="5f9b8-231">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-231">Click Add String.</span></span>
20. <span data-ttu-id="5f9b8-232">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-232">Click OK.</span></span>
21. <span data-ttu-id="5f9b8-233">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="5f9b8-234">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-234">Click Add String.</span></span>
23. <span data-ttu-id="5f9b8-235">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-235">Click OK.</span></span>
24. <span data-ttu-id="5f9b8-236">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Name” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="5f9b8-237">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-237">Click Add String.</span></span>
26. <span data-ttu-id="5f9b8-238">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-238">Click OK.</span></span>
27. <span data-ttu-id="5f9b8-239">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="5f9b8-240">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-240">Click Add String.</span></span>
29. <span data-ttu-id="5f9b8-241">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-241">Click OK.</span></span>
30. <span data-ttu-id="5f9b8-242">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="5f9b8-243">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-243">Click Add String.</span></span>
32. <span data-ttu-id="5f9b8-244">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-244">Click OK.</span></span>
33. <span data-ttu-id="5f9b8-245">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Währung” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="5f9b8-246">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-246">Click Add String.</span></span>
35. <span data-ttu-id="5f9b8-247">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-247">Click OK.</span></span>
36. <span data-ttu-id="5f9b8-248">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Beschreibung” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="5f9b8-249">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-249">Click Add String.</span></span>
38. <span data-ttu-id="5f9b8-250">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-250">Click OK.</span></span>
39. <span data-ttu-id="5f9b8-251">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Betrag” aus.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="5f9b8-252">Klicken Sie auf "Zeichenfolge hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-252">Click Add String.</span></span>
41. <span data-ttu-id="5f9b8-253">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-253">Click OK.</span></span>
42. <span data-ttu-id="5f9b8-254">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-254">Click Save.</span></span>
43. <span data-ttu-id="5f9b8-255">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-255">Close the page.</span></span>


