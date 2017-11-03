---
title: Kostenelementdimensionen
description: "Als eine der Kernpfeiler bei der Kostenrechnung werden Kostenelementdimensionen verwendet, um zu kategorisieren und nachzuverfolgen, wo Kosten hinfließen."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f47c75b6f6f4533501070f78698de82cf70f9bd
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="b84c2-103">Kostenelementdimensionen</span><span class="sxs-lookup"><span data-stu-id="b84c2-103">Cost element dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b84c2-104">Als eine der Kernpfeiler bei der Kostenrechnung werden Kostenelementdimensionen verwendet, um zu kategorisieren und nachzuverfolgen, wo Kosten hinfließen.</span><span class="sxs-lookup"><span data-stu-id="b84c2-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="b84c2-105">Ein Kostenelement entspricht einem kostenrelevanten Artikel in dem Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="b84c2-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="b84c2-106">Grundsätzlich kann es jeder Elementtyp auf der untersten Ebene in einem Unternehmen sein, wohin die Kosten fließen können.</span><span class="sxs-lookup"><span data-stu-id="b84c2-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="b84c2-107">Kostenelemente als Konzeptbereich von Sachkonten zu allen kostenrelevanten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b84c2-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="b84c2-108">Aktuell unterstützt die Kostenrechnung Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="b84c2-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="b84c2-109">Zwei Typen von Kostenelementen</span><span class="sxs-lookup"><span data-stu-id="b84c2-109">Two types of cost elements</span></span>
<span data-ttu-id="b84c2-110">Es gibt zwei Typen von Kostenelementen: primäre Kostenelemente und sekundäre Kostenelemente.</span><span class="sxs-lookup"><span data-stu-id="b84c2-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="b84c2-111">In der folgenden Tabelle wird der Unterschied zwischen beiden Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b84c2-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b84c2-112"><strong>Primäre Kostenelemente</strong></span><span class="sxs-lookup"><span data-stu-id="b84c2-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="b84c2-113"><strong>Sekundäre Kostenelemente</strong></span><span class="sxs-lookup"><span data-stu-id="b84c2-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b84c2-114">Die primären Kostenelemente stellen den Kostenfluss von der Finanzbuchhaltung zur Kostenrechnung dar.</span><span class="sxs-lookup"><span data-stu-id="b84c2-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="b84c2-115">Die Kostenelementstruktur entspricht der Gewinn- und Verlustkontostruktur im Hauptbuch, wo ein Kostenelement einem Hauptkonto entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="b84c2-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="b84c2-116">Nicht alle Hauptkonten werden notwendigerweise als Kostenelemente dargestellt, je nach den Geschäftsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="b84c2-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="b84c2-117">Beispiele von primären Kostenelementen sind unter Anderem:</span><span class="sxs-lookup"><span data-stu-id="b84c2-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="b84c2-118">Wareneinsätze (COGs)</span><span class="sxs-lookup"><span data-stu-id="b84c2-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="b84c2-119">Indirekte Materialkosten</span><span class="sxs-lookup"><span data-stu-id="b84c2-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="b84c2-120">Personalkosten</span><span class="sxs-lookup"><span data-stu-id="b84c2-120">Personnel costs</span></span></li>
<li><span data-ttu-id="b84c2-121">Energiekosten</span><span class="sxs-lookup"><span data-stu-id="b84c2-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="b84c2-122">Die sekundären Kostenelemente stellen den Fluss der Kosten intern dar, da diese Kosten nur in der Kostenrechnung erstellt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b84c2-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="b84c2-123">Sie werden verwendet, um sicherzustellen, dass die Kostenquelle nachverfolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b84c2-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="b84c2-124">Diese Kostenelemente werden in Kostenzuteilungen und bei Gemeinkostenberechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b84c2-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="b84c2-125">Beispiele von sekunären Kostenelementen sind unter Anderem:</span><span class="sxs-lookup"><span data-stu-id="b84c2-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="b84c2-126">Produktionskosten</span><span class="sxs-lookup"><span data-stu-id="b84c2-126">Production costs</span></span></li>
<li><span data-ttu-id="b84c2-127">Gemeinkosten für Produktion, Material und Marketing</span><span class="sxs-lookup"><span data-stu-id="b84c2-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="b84c2-128">Kostenelementdimensionen und Kostenelement-Dimensionsmitglieder</span><span class="sxs-lookup"><span data-stu-id="b84c2-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="b84c2-129">Kostenelemente werden als *Kostenelementdimensionen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b84c2-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="b84c2-130">Die einzelnen Dimensionswerte werden *Kostenelement-Dimensionsmitglieder* genannt.</span><span class="sxs-lookup"><span data-stu-id="b84c2-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="b84c2-131">Beispielsweise haben Sie eine US-Kontenplanstruktur (COA), die die Basis für ihre Offenlegungspflicht ist.</span><span class="sxs-lookup"><span data-stu-id="b84c2-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="b84c2-132">Diese COA wird als Kostenelementdimension verwendet.</span><span class="sxs-lookup"><span data-stu-id="b84c2-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="b84c2-133">Die Konten, die primäre Kostenelemente sind, werden als Kostenelement-Dimensionsmitglieder in der Kostenrechnung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b84c2-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="b84c2-134">Das folgende Screenshot zeigt ein Beispiel der Hauptkonten als die Kostenelementdimension mit ihren tatsächlichen Hauptkonten als die Kostenelement-Dimensionsmitglieder an.</span><span class="sxs-lookup"><span data-stu-id="b84c2-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="b84c2-135">[![Kostenelementdimensionen](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="b84c2-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="b84c2-136">Kostenelement-Dimensionsmitglieder über Datenkonnektoren importieren</span><span class="sxs-lookup"><span data-stu-id="b84c2-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="b84c2-137">Um die Einstellungen der Kostenelement-Dimensionsmitglieder in der Kostenrechnung zu vereinfachen, können Sie Datenkonnektoren verwenden, die entweder vorkonfiguriert sind oder Ihr benutzerdefinierter Build sind, um die primären Kostenelemente aus einem oder mehreren Quellsystemen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b84c2-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="b84c2-138">Implementierungsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="b84c2-138">Implementation considerations</span></span>
<span data-ttu-id="b84c2-139">Da Kostenelemente die unterste Ebene der Kostendetails darstellen, sollten Sie sicherstellen, dass alle Kostenelemente, die zur Berichterstellung auf Führungsebene erforderlich sind, einbezogen werden, wenn Sie die Kostenelementstruktur implementieren.</span><span class="sxs-lookup"><span data-stu-id="b84c2-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="b84c2-140">Es kann eine Herausforderung sein, eine entsprechenden Anzahl von Kostenelementen für die Kostensteuerung zu finden.</span><span class="sxs-lookup"><span data-stu-id="b84c2-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="b84c2-141">Wenn Sie Tausende von Kostenelementen haben, kann es schwierig sein, jedes Kostenelement zu steuern.</span><span class="sxs-lookup"><span data-stu-id="b84c2-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="b84c2-142">Alternativ können Sie Kostenelemente gruppieren und die Kostensteuerung auf einer aggregierten Ebene verwalten.</span><span class="sxs-lookup"><span data-stu-id="b84c2-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




