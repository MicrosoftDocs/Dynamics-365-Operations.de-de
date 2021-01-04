---
title: ER Erstellen eine Formatkonfiguration (November 2016)
description: In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4cd3960594ab37ca867792c655cfd28dc332fa9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684762"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="00ba6-103">ER Erstellen eine Formatkonfiguration (November 2016)</span><span class="sxs-lookup"><span data-stu-id="00ba6-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00ba6-104">In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="00ba6-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="00ba6-105">Diese Formatkonfiguration definiert das Format von elektronischen Dokumenten, die für die Verarbeitung von Zahlungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00ba6-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="00ba6-106">In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen Litware, Inc. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur „Modell für ausgewählte Datenquellen zuweisen abschließen“.</span><span class="sxs-lookup"><span data-stu-id="00ba6-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="00ba6-107">Dient zum Erstellen einer neuen Format-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="00ba6-107">Create a new format configuration</span></span>
1. <span data-ttu-id="00ba6-108">Wechseln Sie zu **Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="00ba6-109">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="00ba6-110">Wählen Sie **Zahlungen (vereinfachtes Modell)** in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="00ba6-111">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00ba6-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="00ba6-112">Wenn **Konfiguration erstellen** nicht angezeigt wird, müssen Sie den Entwurfsmodus der Seite **Elektronische Berichterstellungsparameter** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="00ba6-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="00ba6-113">Im **neuen** Feld geben Sie **Format auf Grundlage Datenmodell PaymentModel** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="00ba6-114">Geben Sie im Feld **Name** **BACS (Großbritannien fiktiv)** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="00ba6-115">Geben Sie im Feld **Beschreibung** den Typ **BACS-Kreditorenzahlungsformat (Großbritannien fiktiv** en Namens)" ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="00ba6-116">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="00ba6-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="00ba6-117">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="00ba6-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="00ba6-118">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="00ba6-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="00ba6-119">Ein spezielles Format elektronischer Dokumente kann definiert werden.</span><span class="sxs-lookup"><span data-stu-id="00ba6-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="00ba6-120">Lassen Sie das Feld leer, wenn Sie ein Format zur Laufzeit auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="00ba6-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="00ba6-121">Geben Sie im Feld **Datenmodelldefinition** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="00ba6-122">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-122">Click **Create configuration**.</span></span> <span data-ttu-id="00ba6-123">Ein neuer Konfiguration wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="00ba6-123">A new configuration has been created.</span></span> <span data-ttu-id="00ba6-124">Die Entwurfsversion kann verwendet werden, um das Designformat für die Verwaltung von elektronischen Dokumenten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="00ba6-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="00ba6-125">Entwerfen Sie Format elektronischer Dokumente</span><span class="sxs-lookup"><span data-stu-id="00ba6-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="00ba6-126">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-126">Click **Designer**.</span></span>
2. <span data-ttu-id="00ba6-127">Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00ba6-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="00ba6-128">Wählen Sie in der Struktur **Common\File** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="00ba6-129">Geben Sie im Feld **Name** **Xml** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="00ba6-130">Geben Sie im Feld **Kodierung** **UTF-8** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="00ba6-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-131">Click **OK**.</span></span>
7. <span data-ttu-id="00ba6-132">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-132">Click **Add**.</span></span>
8. <span data-ttu-id="00ba6-133">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="00ba6-134">Geben Sie im Feld **Name** **Nachricht** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="00ba6-135">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-135">Click **OK**.</span></span>
11. <span data-ttu-id="00ba6-136">Wählen Sie in der Struktur **XML\Nachricht** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="00ba6-137">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="00ba6-138">Geben Sie im Feld **Name** **ProcessingDate** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="00ba6-139">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-139">Click **OK**.</span></span>
15. <span data-ttu-id="00ba6-140">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="00ba6-141">Geben Sie im Feld Name **MessageId** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="00ba6-142">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-142">Click **OK**.</span></span>
18. <span data-ttu-id="00ba6-143">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="00ba6-144">Geben Sie im Feld **Name** **Zahlungen** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="00ba6-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-145">Click **OK**.</span></span>
21. <span data-ttu-id="00ba6-146">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="00ba6-147">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="00ba6-148">Geben Sie im Feld **Name** **Item** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="00ba6-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-149">Click **OK**.</span></span>
25. <span data-ttu-id="00ba6-150">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="00ba6-151">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-151">Click **Add**.</span></span>
27. <span data-ttu-id="00ba6-152">Wählen Sie in der Struktur **XML\Attribute** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="00ba6-153">Geben Sie im Feld Name **Id** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="00ba6-154">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-154">Click **OK**.</span></span>
30. <span data-ttu-id="00ba6-155">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-155">Click **Add**.</span></span>
31. <span data-ttu-id="00ba6-156">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="00ba6-157">Geben Sie im Feld Name **Lieferant** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="00ba6-158">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-158">Click **OK**.</span></span>
34. <span data-ttu-id="00ba6-159">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="00ba6-160">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="00ba6-161">Geben Sie im Feld "Typ" **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="00ba6-162">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-162">Click **OK**.</span></span>
38. <span data-ttu-id="00ba6-163">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="00ba6-164">Geben Sie im Feld **Name** **Bank** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="00ba6-165">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-165">Click **OK**.</span></span>
41. <span data-ttu-id="00ba6-166">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="00ba6-167">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="00ba6-168">Geben Sie im Feld **Name** **RoutingNumber** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="00ba6-169">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-169">Click **OK**.</span></span>
45. <span data-ttu-id="00ba6-170">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="00ba6-171">Geben Sie im Feld **Name** **AccountNumber** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="00ba6-172">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-172">Click **OK**.</span></span>
48. <span data-ttu-id="00ba6-173">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="00ba6-174">Klicken Sie auf **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-174">Click **Copy**.</span></span>
50. <span data-ttu-id="00ba6-175">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="00ba6-176">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-176">Click **Paste**.</span></span>
52. <span data-ttu-id="00ba6-177">Geben Sie im Feld **Name** **Zahler** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="00ba6-178">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="00ba6-179">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="00ba6-180">Geben Sie im Feld **Name** **Währung** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="00ba6-181">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-181">Click **OK**.</span></span>
57. <span data-ttu-id="00ba6-182">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="00ba6-183">Geben Sie im Feld **Name** **Beschreibung** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="00ba6-184">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-184">Click **OK**.</span></span>
60. <span data-ttu-id="00ba6-185">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="00ba6-186">Geben Sie im Feld Typ **TransDate** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="00ba6-187">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-187">Click **OK**.</span></span>
63. <span data-ttu-id="00ba6-188">Klicken Sie auf **Element hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="00ba6-189">Geben Sie im Feld Namen **Betrag** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="00ba6-190">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="00ba6-191">Bereiten Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen vor</span><span class="sxs-lookup"><span data-stu-id="00ba6-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="00ba6-192">Wählen Sie in der Struktur **XML\Nachricht\ProcessingDate** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="00ba6-193">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="00ba6-194">Wählen Sie in der Struktur **Text\DateTime** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="00ba6-195">Geben Sie im Feld **Format** **yyyy-MM-dd** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="00ba6-196">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-196">Click **OK**.</span></span>
6. <span data-ttu-id="00ba6-197">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\TransDate** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="00ba6-198">Klicken Sie auf **DateTime hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="00ba6-199">Geben Sie im Feld **Format** **yyyy-MM-dd** ein.</span><span class="sxs-lookup"><span data-stu-id="00ba6-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="00ba6-200">Wählen Sie im Feld **DateTime**-Typ die Option **Date** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="00ba6-201">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-201">Click **OK**.</span></span>
11. <span data-ttu-id="00ba6-202">Wählen Sie in der Struktur **XML\Nachricht\MessageId** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="00ba6-203">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="00ba6-204">Wählen Sie in der Struktur **Text\String** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="00ba6-205">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-205">Click **OK**.</span></span>
15. <span data-ttu-id="00ba6-206">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Name** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="00ba6-207">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-207">Click **Add String**.</span></span>
17. <span data-ttu-id="00ba6-208">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-208">Click **OK**.</span></span>
18. <span data-ttu-id="00ba6-209">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="00ba6-210">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-210">Click **Add String**.</span></span>
20. <span data-ttu-id="00ba6-211">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-211">Click **OK**.</span></span>
21. <span data-ttu-id="00ba6-212">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="00ba6-213">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-213">Click **Add String**.</span></span>
23. <span data-ttu-id="00ba6-214">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-214">Click **OK**.</span></span>
24. <span data-ttu-id="00ba6-215">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Name** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="00ba6-216">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-216">Click **Add String**.</span></span>
26. <span data-ttu-id="00ba6-217">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-217">Click **OK**.</span></span>
27. <span data-ttu-id="00ba6-218">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="00ba6-219">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-219">Click **Add String**.</span></span>
29. <span data-ttu-id="00ba6-220">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-220">Click **OK**.</span></span>
30. <span data-ttu-id="00ba6-221">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="00ba6-222">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-222">Click **Add String**.</span></span>
32. <span data-ttu-id="00ba6-223">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-223">Click **OK**.</span></span>
33. <span data-ttu-id="00ba6-224">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Währung** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="00ba6-225">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-225">Click **Add String**.</span></span>
35. <span data-ttu-id="00ba6-226">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-226">Click **OK**.</span></span>
36. <span data-ttu-id="00ba6-227">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="00ba6-228">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-228">Click **Add String**.</span></span>
38. <span data-ttu-id="00ba6-229">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-229">Click **OK**.</span></span>
39. <span data-ttu-id="00ba6-230">Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Betrag** aus.</span><span class="sxs-lookup"><span data-stu-id="00ba6-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="00ba6-231">Klicken Sie auf **Zeichenfolge hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-231">Click **Add String**.</span></span>
41. <span data-ttu-id="00ba6-232">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-232">Click **OK**.</span></span>
42. <span data-ttu-id="00ba6-233">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="00ba6-233">Click **Save**.</span></span>
43. <span data-ttu-id="00ba6-234">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="00ba6-234">Close the page.</span></span>

