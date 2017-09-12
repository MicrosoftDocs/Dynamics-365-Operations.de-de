---
title: "Teilweise Lagerplatz-Zykluszählung"
description: "Zykluszählungspläne leiten die tatsächlichen Zähloperationen. Sie können festlegen, dass nur bestimmte Produkte und Produktvarianten anstelle aller verfügbaren Lagerbestände eines Lagerplatzes gezählt werden."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="5e38a-105">Teilweise Lagerplatz-Zykluszählung</span><span class="sxs-lookup"><span data-stu-id="5e38a-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5e38a-106">Zykluszählungspläne leiten die tatsächlichen Zähloperationen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="5e38a-107">Sie können festlegen, dass nur bestimmte Produkte und Produktvarianten anstelle aller verfügbaren Lagerbestände eines Lagerplatzes gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="5e38a-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="5e38a-108">Wenn Sie Zykluszählpläne nutzen, um Inventurarbeit zu generieren, können Sie die tatsächlichen Zähloperationen lenken.</span><span class="sxs-lookup"><span data-stu-id="5e38a-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="5e38a-109">Sie können festlegen, dass nur bestimmte Produkte und Produktvarianten anstelle aller verfügbaren Lagerbestände eines Lagerplatzes gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="5e38a-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="5e38a-110">Indem Sie nach bestimmten Produkten filtern, kann der Lagerortleiter Prüfungsgemeinkosten senken, Konsolidierungsfehler vermeiden und Zeit sparen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="5e38a-111">So konfigurieren Sie eine teilweise Lagerplatz-Zykluszählung</span><span class="sxs-lookup"><span data-stu-id="5e38a-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="5e38a-112">Wenn Sie den Lagerortarbeitsprozess für Zähloperationen verwenden, wird eine Arbeitskopfzeile für jeden Lagerplatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e38a-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="5e38a-113">Wenn Sie den Zykluszählplan definieren, können Sie die Abfrage **Lagerplätze auswählen** verwenden, um die Zykluszählarbeit zu reduzieren, die generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5e38a-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="5e38a-114">Wenn Sie Produkte für den Zykluszählplan auswählen, können Sie Produkt- und Produktvariantenabfragen verwenden, um das Zählen zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="5e38a-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="5e38a-115">Sie können eine **Arbeitsvorlage** einem Zykluszählplan zuordnen, um zu definieren, wie die Zykluszählarbeit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e38a-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="5e38a-116">Auf die Arbeitsvorlage für Zählvorgänge wird direkt vom Zykluszählplan verwiesen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="5e38a-117">Wenn Sie die Arbeitsvorlagendetails definieren, können Sie die Option **Arbeitspositionsumbrüche** verwenden, um anzugeben, ob die Inventurarbeitspositionen nach Positionsnummer oder Produktvariantennummer gruppiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="5e38a-118">Diese Einstellung ist erforderlich, wenn Sie verfügbare Lagerbestände nur für bestimmte Produkte an einem Lagerplatz zählen möchten.</span><span class="sxs-lookup"><span data-stu-id="5e38a-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="5e38a-119">Die Zykluszählungsarbeitspositionen, die erstellt werden, bekommen die Informationsebene, die Sie hier definieren. Der geführte Zählvorgang wird auf Basis dieser Ebene durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e38a-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="5e38a-120">Wenn Sie Zykluszählpläne mit Arbeitsvorlagen verknüpfen, indem Sie die Option **Arbeitspositionsumbrüche** verwenden, ist das Feld **Teilweise Zykluszählung** für die Zykluszählungsarbeit ausgewählt, die erstellt wird, und mehrere Zykluszählungsarbeitspositionen werden auf Basis der Definition der Arbeitsvorlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e38a-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="5e38a-121">Bevor teilweise Zykluszählungsarbeit verarbeitet werden kann, müssen Sie zumindest **Artikelnummer anzeigen** für das Menüelement des mobilen Geräts als Teil des Zykluszählungssetups auswählen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="5e38a-122">Der Lagerortoperator wird aufgefordert, nur Zähldaten zu erfassen, die zu den Zählpositionen (Positionsnummern und Produktdimensionen) gehören.</span><span class="sxs-lookup"><span data-stu-id="5e38a-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="5e38a-123">Der gesamte andere verfügbare Bestand wird für diesen Zählungsprozess ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5e38a-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="5e38a-124">Beim teilweisen Zykluszählungsprozess werden Datum/Uhrzeit von **Letzte permanente Inventur** für den Lagerplatz nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5e38a-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="5e38a-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e38a-125">Example</span></span>
<span data-ttu-id="5e38a-126">In vorliegenden Beispiel muss nur Artikelnummer A0001 in Lagerort 61 gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="5e38a-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="5e38a-127">Es wird eine neue Arbeitsvorlage für die Zykluszählung erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e38a-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="5e38a-128">Die Option **Arbeitspositionsumbrüche** wird verwendet, um fortlaufende Zählarbeitspositionen nach Artikelnummer zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="5e38a-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="5e38a-129">Deshalb hat die Zykluszählungsarbeit, die erstellt wird, pro Artikelnummer Positionen.</span><span class="sxs-lookup"><span data-stu-id="5e38a-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="5e38a-130">Sie können die Positionen auch nach Produktvariantennummer gruppieren.</span><span class="sxs-lookup"><span data-stu-id="5e38a-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="5e38a-131">Ein neuer Zykluszählungsplan wird erstellt, der auf die neue erstellte Arbeitsvorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="5e38a-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="5e38a-132">Der Zykluszählungsplan enthält alle Lagerplätze in Lagerort 61 (Abfrage **Lagerplätze auswählen**), die Bestand für Artikelnummer A0001 haben.</span><span class="sxs-lookup"><span data-stu-id="5e38a-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="5e38a-133">Die Auswahl bestimmter Produkte wird im Abschnitt **Produktauswahlen des Zykluszählungsplans** definiert.</span><span class="sxs-lookup"><span data-stu-id="5e38a-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="5e38a-134">Sie können Produkte für Zykluszählungspläne auswählen, indem Sie das Feld **Leere Lagerplätze** auf **Leere ausschließen** setzen. Wenn der Zykluszählungsplan verarbeitet wird, wird teilweise Zykluszählungsarbeit für Artikelnummer A0001 erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e38a-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="5e38a-135">Der tatsächliche Zählprozess kann über das Menüelement des mobilen Geräts für geführte Zykluszählung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e38a-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="5e38a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e38a-136">See also</span></span>
--------

[<span data-ttu-id="5e38a-137">Zykluszählung</span><span class="sxs-lookup"><span data-stu-id="5e38a-137">Cycle counting</span></span>](cycle-counting.md)


