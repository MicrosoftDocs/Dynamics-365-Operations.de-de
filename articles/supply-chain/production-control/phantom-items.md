---
title: Phantomartikel
description: "In diesem Thema wird  ausführlich beschrieben, wie der Positionstyp \"Phantom\" für die Positionen einer Stückliste (BOM) und die Formel in Microsoft Dynamics 365 for Finance and Operations verwendet werden kann."
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: de-de
ms.lasthandoff: 10/01/2018

---

# <a name="phantom-items"></a><span data-ttu-id="4a0aa-103">Phantomartikel</span><span class="sxs-lookup"><span data-stu-id="4a0aa-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a0aa-104">In diesem Thema wird  ausführlich beschrieben, wie der Positionstyp "Phantom" für die Positionen einer Stückliste (BOM) und die Formel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="4a0aa-105">In der folgenden Abbildung ist (a) die Stückliste für Produkt H und Teile F, G und und (b) ist der Arbeitsplan für Produkte H und Teil F.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Produkt H und Teil F](media/product-H-part-F.png)


<span data-ttu-id="4a0aa-107">Diese Abbildung zeigt ein Beispiel einer Stückliste in zwei Ebenen.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="4a0aa-108">Produkt H stellt ein Produkt für eine Maschinenzusammenstellung dar.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="4a0aa-109">Die Maschinenmontage besteht aus zwei Teilen, einer elektrische Einheit (F), die zwei Materialien hat (A und B) und eine Gruppe Verpackungsmaterialien (G), die auch zwei Materialien hat (C und D).</span><span class="sxs-lookup"><span data-stu-id="4a0aa-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="4a0aa-110">Ein anderes Material (E) wird bei der allgemeinen Zusammenstellung der Maschine verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Produkt H und Teil F](media/product-H-part-B.png)

<span data-ttu-id="4a0aa-112">Die hier verwendete Darstellung zeigt die erstellte Stückliste für Produkt H. Diese Struktur bietet einen guten Überblick der Teile und Komponenten der gesamten Maschinenmontage.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="4a0aa-113">Aber Produktdesigner ziehen es möglicherweise vor, die Stückliste so zu sehen und diese Struktur wird vielleicht nicht korrekt so dargestellt, wie die Maschine im Fertigungsbereich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="4a0aa-114">Beispielsweise zeigt die Konstruktionsstückliste in der vorherigen Abbildung, dass das elektrische Einzelteil F als separater Teil auf einem separaten Arbeitsauftrag zusammengestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="4a0aa-115">Allerdings kann es im Fertigungsbereich möglicherweise optimaler beurteilt werden, die elektrische Einheit im Rahmen der Gesamtmaschinenzusammenstellung und nicht als separaten Arbeitsauftrag zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="4a0aa-116">Diese Konstruktionsstückliste gibt auch an, dass Teil G ein separater Teil ist.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="4a0aa-117">Allerdings ist in dieser Struktur Teil G nicht ein physisches Teil, sondern eine Zusammenstellung von Verpackungsmaterialien.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="4a0aa-118">Auch wenn eine Konstruktionsstückliste möglicherweise einen hohen Wert für den Entwurf eines Produkts sowie der Verwaltung dieses Designs bereitstellt, ist er möglicherweise nicht die logischste Möglichkeit, den Fertigungssteuerungsprozess des Produkts zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="4a0aa-119">Möglicherweise stellt die Produktions-Stückliste die beste Methode dar, ein Produkt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="4a0aa-120">Die folgende Abbildung zeigt, wie die vorhergehende Konstruktionsstückliste in eine Produktionsstückliste übergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="4a0aa-121">In dieser Grafik ist (a) die Stückliste für Produkt H und b ist der Arbeitsplan für Produkt H.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="4a0aa-122">In dieser Struktur wird angezeigt, dass es keinen Hinweis von Teilen F und G gibt und das Material, das aus diesen Teile besteht, wurde auf die folgenden Stücklistenebene gehoben.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="4a0aa-123">Im Gegensatz zur Konstruktionsstückliste, die zwei Arbeitskarten hatte, hat die Produktionsstückliste nur eine Arbeitskarte.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="4a0aa-124">Der Verpackungsarbeitsgang, der mit Teil G verknüpft war, wurde ebenfalls erhöht und ist nun Teil der Arbeitskarte für Produkt H. Die Zusammenstellung der elektrische Einheit ist der erste Arbeitsgang.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="4a0aa-125">Dieser Auftrag ergibt Sinn, weil diese Einheit im folgenden Arbeitsgang verwendet wird, der die Maschinenzusammenstellung ist.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="4a0aa-126">Der letzte Arbeitsgang ist der Verpackungsarbeitsgang, der zwei Verpackungsmaterialien verbraucht (C und D).</span><span class="sxs-lookup"><span data-stu-id="4a0aa-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="4a0aa-127">In Microsoft Dynamics 365 for Finance and Operations ist der Übergang zwischen der Konstruktionsstückliste und der Produktionsstückliste über den Phantomstücklistenpositionstyp aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-127">In Microsoft Dynamics 365 for Finance and Operations, the transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="4a0aa-128">Während die Bedingung" Phantom" angegeben wird, sind die Komponenten F und G während des Übergangs zwischen den zwei Stücklistentypen verschwunden.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="4a0aa-129">In diesem Beispiel wird der Positionstyps "Phantom" für die Stücklistenpositionen für Teile F und G in der Konstruktionsstückliste angewendet.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="4a0aa-130">Wenn ein Produktions- oder Chargenauftrag erstellt wird, wird die Konstruktionsstückliste in die Produktionsstückliste oder den Chargenauftrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="4a0aa-131">Wird der Auftrag vorkalkuliert, erfolgt der Übergang von der Konstruktionsstückliste zur Produktionsstückliste wie in den vorhergehenden Bildern dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="4a0aa-132">Auf der Arbeitskarte in der zweiten Abbildung werden die Verpackungsmaterialien C und D als Input für den Arbeitsgang eingegeben.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="4a0aa-133">Mehrstufige Phantomstücklistenstrukturen</span><span class="sxs-lookup"><span data-stu-id="4a0aa-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="4a0aa-134">Die Phantompositionsart kann in mehrstufigen Stücklistenstrukturen wie in der folgenden Abbildung dargestellt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="4a0aa-135">In dieser Grafik ist (a) die Stückliste für Produkt G und (b) ist der Arbeitsplan für Teile E und F und Produkt G.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Produkt G und Teil F mit Begleitkarten](media/product-G-route-sheet-G.png)


<span data-ttu-id="4a0aa-137">Die folgende Abbildung zeigt die resultierende Fertigungsstückliste und den Arbeitsplan, wenn die  Stücklistenpositionen für Teile E und F konfiguriert werden, sodass der Positionstyp Phantom ist.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="4a0aa-138">In dieser Grafik ist (a) die Stückliste für Produkt G und (b) ist der Arbeitsplan für Produkt G.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="4a0aa-140">Phantom und Arbeitsplan-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="4a0aa-140">Phantom and route network</span></span>
<span data-ttu-id="4a0aa-141">Phantomstücklisten können für eine Stückliste verwendet werden, die auch ein Arbeitsplan-Netzwerk haben.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="4a0aa-142">In einem Arbeitsplannetzwerk können eine oder mehrere Arbeitsgänge gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="4a0aa-143">Die folgende Abbildung zeigt ein Beispiel eines Routennetzes an, das in einer mehrere Ebenen umfassenden Stückliste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="4a0aa-144">In dieser Grafik ist (a) die Stückliste für Produkt G und Teil F und (b) ist der Arbeitsplan für Produkt G und Teil F, die ein Arbeitsplannetzwerk haben.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Produkt G und Teil F](media/product-G-part-F.png)


<span data-ttu-id="4a0aa-146">In der folgenden Abbildung ist (a) die Stückliste für Produkt G und Teile F und (b) ist der Arbeitsplan für Produkte G und Teil F.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Produkt G und Teil F mit Begleitkarten](media/product-G-part-F-with-route-sheet.png)
