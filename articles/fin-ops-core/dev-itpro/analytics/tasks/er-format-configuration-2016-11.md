---
title: ER Erstellen eine Formatkonfiguration (November 2016)
description: In diesem Thema wird beschrieben, wie Sie eine Formatkonfiguration für die elektronische Berichterstellung (EB) verwalten.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cb86c1486223e982f8cbddc8eadaaf1c8ced4f8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565189"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="4c567-103">ER Erstellen eine Formatkonfiguration (November 2016)</span><span class="sxs-lookup"><span data-stu-id="4c567-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c567-104">In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="4c567-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="4c567-105">Diese Formatkonfiguration definiert das Format von elektronischen Dokumenten, die für die Verarbeitung von Zahlungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c567-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="4c567-106">In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen Litware, Inc. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur „Modell für ausgewählte Datenquellen zuweisen abschließen“.</span><span class="sxs-lookup"><span data-stu-id="4c567-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="4c567-107">Dient zum Erstellen einer neuen Format-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c567-107">Create a new format configuration</span></span>
1. <span data-ttu-id="4c567-108">Wechseln Sie zu **Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="4c567-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="4c567-109">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="4c567-110">Wählen Sie **Zahlungen (vereinfachtes Modell)** in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="4c567-111">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c567-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="4c567-112">Wenn **Konfiguration erstellen** nicht angezeigt wird, müssen Sie den Entwurfsmodus der Seite **Elektronische Berichterstellungsparameter** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4c567-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="4c567-113">Im **neuen** Feld geben Sie **Format auf Grundlage Datenmodell PaymentModel** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="4c567-114">Geben Sie im Feld **Name** **BACS (Großbritannien fiktiv)** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="4c567-115">Geben Sie im Feld **Beschreibung** den Typ **BACS-Kreditorenzahlungsformat (Großbritannien fiktiv** en Namens)" ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="4c567-116">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="4c567-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="4c567-117">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="4c567-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="4c567-118">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="4c567-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="4c567-119">Ein spezielles Format elektronischer Dokumente kann definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4c567-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="4c567-120">Lassen Sie das Feld leer, wenn Sie ein Format zur Laufzeit auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="4c567-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="4c567-121">Geben Sie im Feld **Datenmodelldefinition** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="4c567-122">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-122">Click **Create configuration**.</span></span> <span data-ttu-id="4c567-123">Ein neuer Konfiguration wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="4c567-123">A new configuration has been created.</span></span> <span data-ttu-id="4c567-124">Die Entwurfsversion kann verwendet werden, um das Designformat für die Verwaltung von elektronischen Dokumenten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4c567-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="4c567-125">Entwerfen Sie Format elektronischer Dokumente</span><span class="sxs-lookup"><span data-stu-id="4c567-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="4c567-126">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="4c567-126">Click **Designer**.</span></span>
2. <span data-ttu-id="4c567-127">Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c567-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="4c567-128">Wählen Sie in der Struktur **Common\File** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="4c567-129">Geben Sie im Feld **Name** **Xml** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="4c567-130">Geben Sie im Feld **Kodierung** **UTF-8** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="4c567-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-131">Click **OK**.</span></span>
7. <span data-ttu-id="4c567-132">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-132">Click **Add**.</span></span>
8. <span data-ttu-id="4c567-133">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="4c567-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="4c567-134">Geben Sie im Feld **Name** **Nachricht** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="4c567-135">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-135">Click **OK**.</span></span>
11. <span data-ttu-id="4c567-136">Wählen Sie in der Struktur **XML\Nachricht** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="4c567-137">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="4c567-138">Geben Sie im Feld **Name** **ProcessingDate** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="4c567-139">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-139">Click **OK**.</span></span>
15. <span data-ttu-id="4c567-140">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="4c567-141">Geben Sie im Feld Name **MessageId** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="4c567-142">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-142">Click **OK**.</span></span>
18. <span data-ttu-id="4c567-143">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="4c567-144">Geben Sie im Feld **Name** **Zahlungen** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="4c567-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-145">Click **OK**.</span></span>
21. <span data-ttu-id="4c567-146">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="4c567-147">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="4c567-148">Geben Sie im Feld **Name** **Item** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="4c567-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-149">Click **OK**.</span></span>
25. <span data-ttu-id="4c567-150">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="4c567-151">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-151">Click **Add**.</span></span>
27. <span data-ttu-id="4c567-152">Wählen Sie in der Struktur **XML\Attribute** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="4c567-153">Geben Sie im Feld Name **Id** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="4c567-154">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-154">Click **OK**.</span></span>
30. <span data-ttu-id="4c567-155">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-155">Click **Add**.</span></span>
31. <span data-ttu-id="4c567-156">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="4c567-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="4c567-157">Geben Sie im Feld Name **Lieferant** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="4c567-158">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-158">Click **OK**.</span></span>
34. <span data-ttu-id="4c567-159">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="4c567-160">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="4c567-161">Geben Sie im Feld "Typ" **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="4c567-162">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-162">Click **OK**.</span></span>
38. <span data-ttu-id="4c567-163">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="4c567-164">Geben Sie im Feld **Name** **Bank** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="4c567-165">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-165">Click **OK**.</span></span>
41. <span data-ttu-id="4c567-166">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="4c567-167">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="4c567-168">Geben Sie im Feld **Name** **RoutingNumber** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="4c567-169">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-169">Click **OK**.</span></span>
45. <span data-ttu-id="4c567-170">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="4c567-171">Geben Sie im Feld **Name** **AccountNumber** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="4c567-172">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-172">Click **OK**.</span></span>
48. <span data-ttu-id="4c567-173">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="4c567-174">Klicken Sie auf **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="4c567-174">Click **Copy**.</span></span>
50. <span data-ttu-id="4c567-175">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="4c567-176">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-176">Click **Paste**.</span></span>
52. <span data-ttu-id="4c567-177">Geben Sie im Feld **Name** **Zahler** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="4c567-178">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="4c567-179">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="4c567-180">Geben Sie im Feld **Name** **Währung** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="4c567-181">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-181">Click **OK**.</span></span>
57. <span data-ttu-id="4c567-182">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="4c567-183">Geben Sie im Feld **Name** **Beschreibung** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="4c567-184">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-184">Click **OK**.</span></span>
60. <span data-ttu-id="4c567-185">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="4c567-186">Geben Sie im Feld Typ **TransDate** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="4c567-187">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-187">Click **OK**.</span></span>
63. <span data-ttu-id="4c567-188">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="4c567-189">Geben Sie im Feld Namen **Betrag** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="4c567-190">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="4c567-191">Bereiten Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen vor</span><span class="sxs-lookup"><span data-stu-id="4c567-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="4c567-192">Wählen Sie in der Struktur **XML\Nachricht\ProcessingDate** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="4c567-193">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="4c567-194">Wählen Sie in der Struktur **Text\DateTime** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="4c567-195">Geben Sie im Feld **Format** **yyyy-MM-dd** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="4c567-196">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-196">Click **OK**.</span></span>
6. <span data-ttu-id="4c567-197">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\TransDate** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="4c567-198">Klicken Sie auf **DateTime hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="4c567-199">Geben Sie im Feld **Format** **yyyy-MM-dd** ein.</span><span class="sxs-lookup"><span data-stu-id="4c567-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="4c567-200">Wählen Sie im Feld **DateTime**-Typ die Option **Date** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="4c567-201">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-201">Click **OK**.</span></span>
11. <span data-ttu-id="4c567-202">Wählen Sie in der Struktur **XML\Nachricht\MessageId** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="4c567-203">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="4c567-204">Wählen Sie in der Struktur **Text\String** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="4c567-205">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-205">Click **OK**.</span></span>
15. <span data-ttu-id="4c567-206">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Name** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="4c567-207">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-207">Click **Add String**.</span></span>
17. <span data-ttu-id="4c567-208">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-208">Click **OK**.</span></span>
18. <span data-ttu-id="4c567-209">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="4c567-210">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-210">Click **Add String**.</span></span>
20. <span data-ttu-id="4c567-211">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-211">Click **OK**.</span></span>
21. <span data-ttu-id="4c567-212">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="4c567-213">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-213">Click **Add String**.</span></span>
23. <span data-ttu-id="4c567-214">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-214">Click **OK**.</span></span>
24. <span data-ttu-id="4c567-215">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Name** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="4c567-216">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-216">Click **Add String**.</span></span>
26. <span data-ttu-id="4c567-217">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-217">Click **OK**.</span></span>
27. <span data-ttu-id="4c567-218">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="4c567-219">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-219">Click **Add String**.</span></span>
29. <span data-ttu-id="4c567-220">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-220">Click **OK**.</span></span>
30. <span data-ttu-id="4c567-221">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="4c567-222">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-222">Click **Add String**.</span></span>
32. <span data-ttu-id="4c567-223">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-223">Click **OK**.</span></span>
33. <span data-ttu-id="4c567-224">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Währung** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="4c567-225">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-225">Click **Add String**.</span></span>
35. <span data-ttu-id="4c567-226">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-226">Click **OK**.</span></span>
36. <span data-ttu-id="4c567-227">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="4c567-228">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-228">Click **Add String**.</span></span>
38. <span data-ttu-id="4c567-229">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-229">Click **OK**.</span></span>
39. <span data-ttu-id="4c567-230">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Betrag** aus.</span><span class="sxs-lookup"><span data-stu-id="4c567-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="4c567-231">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4c567-231">Click **Add String**.</span></span>
41. <span data-ttu-id="4c567-232">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c567-232">Click **OK**.</span></span>
42. <span data-ttu-id="4c567-233">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4c567-233">Click **Save**.</span></span>
43. <span data-ttu-id="4c567-234">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4c567-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]