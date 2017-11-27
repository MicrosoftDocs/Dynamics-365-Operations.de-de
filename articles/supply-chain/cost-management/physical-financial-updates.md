---
title: "Physische und wertmäßige Aktualisierungen"
description: "Dieses Thema bietet einen Überblick darüber, welche Buchungsarten eine Erhöhung oder eine Verringerung der Lagermenge zur Folge haben."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e62bdbfb7b88f66ea1f6e4d57b6150c8b0bffb04
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="40fff-103">Physische und wertmäßige Aktualisierungen</span><span class="sxs-lookup"><span data-stu-id="40fff-103">Physical and financial updates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="40fff-104">Dieses Thema bietet einen Überblick darüber, welche Buchungsarten eine Erhöhung oder eine Verringerung der Lagermenge zur Folge haben.</span><span class="sxs-lookup"><span data-stu-id="40fff-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="40fff-105">Lagerbuchungen können in Microsoft Dynamics 365 for Finance and Operations sowohl physisch als auch wertmäßig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="40fff-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="40fff-106">Einige Typen physischer und wertmäßiger Buchungen erhöhen die Lagermenge, während andere die Menge verringern.</span><span class="sxs-lookup"><span data-stu-id="40fff-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="40fff-107">Physische Erhöhung</span><span class="sxs-lookup"><span data-stu-id="40fff-107">Physical increases</span></span>
<span data-ttu-id="40fff-108">Beim Ausführen einer physischen Buchung besitzt der Buchungsdatensatz den Status **Eingegangen**.</span><span class="sxs-lookup"><span data-stu-id="40fff-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="40fff-109">Folgende Buchungen gelten als physische Zunahmen:</span><span class="sxs-lookup"><span data-stu-id="40fff-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="40fff-110">Bestellungszugang</span><span class="sxs-lookup"><span data-stu-id="40fff-110">Purchase order receipt</span></span>
-   <span data-ttu-id="40fff-111">Lieferschein-Retoure für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="40fff-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="40fff-112">Einen Produktionsauftrag als abgeschlossen melden</span><span class="sxs-lookup"><span data-stu-id="40fff-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="40fff-113">Nebenprodukt der Entnahmeliste eines Produktionsauftrags</span><span class="sxs-lookup"><span data-stu-id="40fff-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="40fff-114">Wertmäßige Erhöhung</span><span class="sxs-lookup"><span data-stu-id="40fff-114">Financial increases</span></span>
<span data-ttu-id="40fff-115">Beim Ausführen einer wertmäßigen Buchung besitzt der Buchungsdatensatz, durch den sich eine Zunahme der Menge ergibt, den Status **Eingekauft**.</span><span class="sxs-lookup"><span data-stu-id="40fff-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="40fff-116">Folgende Buchungen gelten als wertmäßige Zunahmen:</span><span class="sxs-lookup"><span data-stu-id="40fff-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="40fff-117">Kreditorenrechnung</span><span class="sxs-lookup"><span data-stu-id="40fff-117">Vendor invoice</span></span>
-   <span data-ttu-id="40fff-118">Auftragsrechnung für eine Retoure</span><span class="sxs-lookup"><span data-stu-id="40fff-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="40fff-119">Nachkalkulation für einen Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="40fff-119">Production order costing</span></span>
-   <span data-ttu-id="40fff-120">Lagererfassungen mit positiver Menge (beispielsweise Bewegungs-, Gewinn- und Verlust-, Inventur-, Stücklisten- oder Umlagerungserfassungen)</span><span class="sxs-lookup"><span data-stu-id="40fff-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="40fff-121">Buchungen mit Mengenerhöhung</span><span class="sxs-lookup"><span data-stu-id="40fff-121">Transactions that increase quantity</span></span>
<span data-ttu-id="40fff-122">Buchungen, durch die sich eine Erhöhung der Menge ergibt, werden zum laufenden Durchschnittseinstandspreis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40fff-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="40fff-123">Finance and Operations berechnet einen laufenden Durchschnittseinstandspreis, der auf den Kosten der einzelnen Buchungen für jede Lagerungsdimension basiert, die wertmäßig verfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="40fff-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="40fff-124">Informationen zu laufenden Durchschnittseinstandspreisen finden Sie unter [Laufender Durchschnittseinstandspreis](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="40fff-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="40fff-125">Buchungen mit Mengenverringerung</span><span class="sxs-lookup"><span data-stu-id="40fff-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="40fff-126">Der laufende Durchschnittseinstandspreis wird von Finance and Operations beim Ausführen einer Buchung verwendet, durch die sich eine Verringerung der Menge ergibt – unabhängig davon, welches Lagermodell dem jeweiligen Bestand zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="40fff-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="40fff-127">Die Buchung, durch die sich eine Verringerung der Menge ergibt, darf vor der Buchung nicht per Markierung mit einer anderen Buchung verknüpft worden sein.</span><span class="sxs-lookup"><span data-stu-id="40fff-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="40fff-128">Wird der Wert des physisch verfügbaren Bestands negativ, werden von Finance and Operations die Lagerkosten verwendet, die für den Artikel auf der Seite **Artikel** definiert sind.</span><span class="sxs-lookup"><span data-stu-id="40fff-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="40fff-129">**Hinweis:** Bei aktivierter Funktion für mehrere Standorte werden statt dieser Kosten die Lagerkosten verwendet, die auf der Seite **Standardauftragseinstellungen** für den Standort definiert sind.</span><span class="sxs-lookup"><span data-stu-id="40fff-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="40fff-130">Vergleich zwischen physischen und wertmäßigen Abgängen</span><span class="sxs-lookup"><span data-stu-id="40fff-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="40fff-131">Beim Ausführen einer physischen Abgangsbuchung besitzt der Buchungsdatensatz den Status **Abgesetzt**.</span><span class="sxs-lookup"><span data-stu-id="40fff-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="40fff-132">Folgende Buchungen gelten als physische Abgänge:</span><span class="sxs-lookup"><span data-stu-id="40fff-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="40fff-133">Kommissionierlistenerfassung für einen Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="40fff-133">Production order picking list journal</span></span>
-   <span data-ttu-id="40fff-134">Auftragslieferschein</span><span class="sxs-lookup"><span data-stu-id="40fff-134">Sales order packing slip</span></span>
-   <span data-ttu-id="40fff-135">Lieferschein-Retoure für eine Bestellung</span><span class="sxs-lookup"><span data-stu-id="40fff-135">Purchase order packing slip return</span></span>

<span data-ttu-id="40fff-136">Beim Ausführen einer wertmäßigen Buchung besitzt der Buchungsdatensatz den Status **Verkauft**.</span><span class="sxs-lookup"><span data-stu-id="40fff-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="40fff-137">Folgende Buchungen gelten als wertmäßige Abgänge:</span><span class="sxs-lookup"><span data-stu-id="40fff-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="40fff-138">Einen Produktionsauftrag beenden</span><span class="sxs-lookup"><span data-stu-id="40fff-138">Ending a production order</span></span>
-   <span data-ttu-id="40fff-139">Auftragsrechnungen</span><span class="sxs-lookup"><span data-stu-id="40fff-139">Sales order invoice</span></span>
-   <span data-ttu-id="40fff-140">Rücksendung einer Kreditorenrechnung</span><span class="sxs-lookup"><span data-stu-id="40fff-140">Vendor invoice return</span></span>
-   <span data-ttu-id="40fff-141">Lagererfassungen mit negativer Menge (beispielsweise Bewegungs-, Gewinn- und Verlust-, Inventur-, Stücklisten- oder Umlagerungserfassungen)</span><span class="sxs-lookup"><span data-stu-id="40fff-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="40fff-142">Buchungen, durch die sich eine Verringerung der Menge ergibt, werden zum laufenden Durchschnittseinstandspreis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40fff-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="40fff-143">Daher müssen Abgangsbuchungen beim Lagerabschluss mit Zugangsbuchungen ausgeglichen werden. Die Grundlage hierfür bildet das den einzelnen Artikeln zugewiesene Lagermodell.</span><span class="sxs-lookup"><span data-stu-id="40fff-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




