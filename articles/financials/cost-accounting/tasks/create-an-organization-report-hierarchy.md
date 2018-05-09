--- 
title: Eine Organisationsberichtshierarchie erstellen
description: "Gehen Sie folgendermaßen vor, um eine Berichtshierarchie für Organisationsberichterstellung zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69fccd6b59e25fe0f39c107c59c1682cc545ebd2
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="0b657-103">Eine Organisationsberichtshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="0b657-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b657-104">Gehen Sie folgendermaßen vor, um eine Berichtshierarchie für Organisationsberichterstellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b657-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="0b657-105">Der Zweck dieser Buchung ist, Sie durch die Dimensionshierarchie zu führen, sodass Sie den Vorgang fortsetzen können, bis die gesamte Organisationsberichterstellungsstruktur erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0b657-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="0b657-106">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b657-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="0b657-107">Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.</span><span class="sxs-lookup"><span data-stu-id="0b657-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="0b657-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-108">Click New.</span></span>
3. <span data-ttu-id="0b657-109">Wählen Sie im Feld HierarchyTypeComboBox Dimensionsklassifizierungs-Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="0b657-110">Wählen Sie Dimensionsklassifizierungs-Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="0b657-111">Der Typ Dimensionsklassifizierungshierarchie wird zur Regeldefinition und zu Berichterstellungszwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b657-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="0b657-112">Er unterstützt alle Dimensionen, wie Kostenobjekte, Kostenelemente und statistischen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="0b657-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="0b657-113">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="0b657-113">Click Create.</span></span>
5. <span data-ttu-id="0b657-114">Geben Sie im Feld "Hierarchiename den Typ Organisation USP2 ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="0b657-115">Geben Sie im Feld Dimension einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="0b657-116">Wählen Sie Kostenstellen.</span><span class="sxs-lookup"><span data-stu-id="0b657-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="0b657-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-117">Click Save.</span></span>
8. <span data-ttu-id="0b657-118">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="0b657-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="0b657-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-119">Click New.</span></span>
10. <span data-ttu-id="0b657-120">Geben Sie im Feld Knotennamen den Typ CEO ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="0b657-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-121">Click Save.</span></span>
12. <span data-ttu-id="0b657-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-122">Click New.</span></span>
13. <span data-ttu-id="0b657-123">Geben Sie im Feld Knotennamen den Typ CEO ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="0b657-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-124">Click Save.</span></span>
15. <span data-ttu-id="0b657-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-125">Click New.</span></span>
16. <span data-ttu-id="0b657-126">Geben Sie im Feld Knotennamen den Typ CEO ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="0b657-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-127">Click Save.</span></span>
18. <span data-ttu-id="0b657-128">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-128">Click New.</span></span>
19. <span data-ttu-id="0b657-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b657-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="0b657-130">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b657-131">Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b657-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="0b657-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-132">Click Save.</span></span>
22. <span data-ttu-id="0b657-133">Wählen Sie in der Strukturdarstellung Oganisation USP2\CEO\CEO Kostenstellen</span><span class="sxs-lookup"><span data-stu-id="0b657-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="0b657-134">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-134">Click New.</span></span>
24. <span data-ttu-id="0b657-135">Geben Sie im Feld Knotennamen den Typ Region West ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="0b657-136">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-136">Click Save.</span></span>
26. <span data-ttu-id="0b657-137">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-137">Click New.</span></span>
27. <span data-ttu-id="0b657-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b657-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="0b657-139">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b657-140">Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b657-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="0b657-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-141">Click Save.</span></span>
30. <span data-ttu-id="0b657-142">Wählen Sie in der Struktur Organisation USP2\CEO ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="0b657-143">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-143">Click New.</span></span>
32. <span data-ttu-id="0b657-144">Geben Sie im Feld Knotennamen den Typ CFO Kostenstellen ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="0b657-145">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-145">Click Save.</span></span>
34. <span data-ttu-id="0b657-146">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-146">Click New.</span></span>
35. <span data-ttu-id="0b657-147">Geben Sie im Feld Knotennamen den Typ Marketing-Kampagne ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="0b657-148">Geben Sie im Feld Knotennamen den Typ Marketing-Kampagne ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="0b657-149">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-149">Click Save.</span></span>
38. <span data-ttu-id="0b657-150">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-150">Click New.</span></span>
39. <span data-ttu-id="0b657-151">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b657-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="0b657-152">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b657-153">Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b657-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="0b657-154">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-154">Click Save.</span></span>
42. <span data-ttu-id="0b657-155">Wählen Sie in der Strukturdarstellung "Organisation USP2\CEO\CFO Kostenstellen".</span><span class="sxs-lookup"><span data-stu-id="0b657-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="0b657-156">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-156">Click New.</span></span>
44. <span data-ttu-id="0b657-157">Geben Sie im Feld Knotennamen den Typ Handelsmesse  ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="0b657-158">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-158">Click Save.</span></span>
46. <span data-ttu-id="0b657-159">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-159">Click New.</span></span>
47. <span data-ttu-id="0b657-160">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b657-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="0b657-161">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b657-162">Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b657-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="0b657-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-163">Click Save.</span></span>
50. <span data-ttu-id="0b657-164">Wählen Sie in der Struktur Organisation USP2\CEO ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="0b657-165">Geben Sie im Feld Knotennamen den Typ CIO Kostenstellen ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="0b657-166">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-166">Click Save.</span></span>
53. <span data-ttu-id="0b657-167">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-167">Click New.</span></span>
54. <span data-ttu-id="0b657-168">Geben Sie im Feld Knotennamen den Typ Callcenters ein.</span><span class="sxs-lookup"><span data-stu-id="0b657-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="0b657-169">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-169">Click Save.</span></span>
56. <span data-ttu-id="0b657-170">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b657-170">Click New.</span></span>
57. <span data-ttu-id="0b657-171">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b657-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="0b657-172">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0b657-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b657-173">Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b657-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="0b657-174">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0b657-174">Click Save.</span></span>


