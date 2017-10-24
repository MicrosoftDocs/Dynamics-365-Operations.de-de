---
title: "Quarantäneaufträge"
description: "In diesem Artikel wird beschrieben, wie Quarantäneaufträge zum Sperren von Beständen verwendet werden."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="quarantine-orders"></a><span data-ttu-id="de3bc-103">Quarantäneaufträge</span><span class="sxs-lookup"><span data-stu-id="de3bc-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="de3bc-104">In diesem Artikel wird beschrieben, wie Quarantäneaufträge zum Sperren von Beständen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de3bc-104">This article describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="de3bc-105">Quarantäneaufträge können verwendet werden, um Bestand zu sperren.</span><span class="sxs-lookup"><span data-stu-id="de3bc-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="de3bc-106">Beispielsweise empfiehlt es sich, Artikel aus Gründen der Qualitätskontrolle unter Quarantäne zu stellen.</span><span class="sxs-lookup"><span data-stu-id="de3bc-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="de3bc-107">Bestand, der unter Quarantäne gestellt wurde, wird an einen Quarantänelagerort übertragen.</span><span class="sxs-lookup"><span data-stu-id="de3bc-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="de3bc-108">**Hinweis:** Wenn Sie die erweiterten Lagerortverwaltungsprozesse (in der Lagerortverwaltung) verwenden, wir die Quarantäneauftragsverarbeitung nur für Rückholaufträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="de3bc-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-onhand-inventory-items"></a><span data-ttu-id="de3bc-109">Verfügbare Lagerartikel unter Quarantäne stellen</span><span class="sxs-lookup"><span data-stu-id="de3bc-109">Quarantine onhand inventory items</span></span>
<span data-ttu-id="de3bc-110">Wenn Sie Artikel unter Quarantäne stellen, können Sie die Quarantäneaufträge entweder manuell erstellen oder das System so einrichten, dass die Quarantäneaufträge automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="de3bc-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="de3bc-111">Um Quarantäneaufträge automatisch zu erstellen, wählen Sie die **Quarantäneverwaltung**-Option auf der **Richtlinien für Lagerbestand**-Registerkarte auf der **Lagersteuerungsgruppen**-Seite aus.</span><span class="sxs-lookup"><span data-stu-id="de3bc-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="de3bc-112">Sie müssen außerdem im Feld **Quarantänelagerort** einen standardmäßigen Quarantänelagerort für den empfangenden Lagerort eingeben.</span><span class="sxs-lookup"><span data-stu-id="de3bc-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="de3bc-113">Wenn der physisch verfügbare Lagerbestand in einer Bestellung oder einem Produktionsauftrag erfasst wird, werden Quarantäneelemente automatisch an einen Quarantänelagerort in Microsoft Dynamics 365 for Finance and Operations verschoben.</span><span class="sxs-lookup"><span data-stu-id="de3bc-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="de3bc-114">Diese Verschiebung tritt auf, da der Status des Quarantäneauftrags in **Gestartet** geändert wird.</span><span class="sxs-lookup"><span data-stu-id="de3bc-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="de3bc-115">Wenn Sie Quarantäneaufträge manuell erstellen, ist es nicht nötig anzufordern, dass der Artikel in der Artikelmodellgruppe für die Quarantäneverwaltung zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="de3bc-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="de3bc-116">Für diesen Vorgang müssen Sie den verfügbaren Lagerbestand, der unter Quarantäne gestellt werden soll, und den Quarantänelagerort angeben, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="de3bc-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="de3bc-117">Sie können den Quarantäneauftragsstatus verwenden, um die Planung des Vorgangs zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="de3bc-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="de3bc-118">Status des Quarantäneauftrags</span><span class="sxs-lookup"><span data-stu-id="de3bc-118">Quarantine order statuses</span></span>
<span data-ttu-id="de3bc-119">Quarantäneaufträge können folgende Status annehmen:</span><span class="sxs-lookup"><span data-stu-id="de3bc-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="de3bc-120">Erstellt</span><span class="sxs-lookup"><span data-stu-id="de3bc-120">Created</span></span>
-   <span data-ttu-id="de3bc-121">Gestartet</span><span class="sxs-lookup"><span data-stu-id="de3bc-121">Started</span></span>
-   <span data-ttu-id="de3bc-122">Fertig gemeldet</span><span class="sxs-lookup"><span data-stu-id="de3bc-122">Reported as finished</span></span>
-   <span data-ttu-id="de3bc-123">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="de3bc-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="de3bc-124">Erstellt</span><span class="sxs-lookup"><span data-stu-id="de3bc-124">Created</span></span>

<span data-ttu-id="de3bc-125">Wenn ein Quarantäneauftrag manuell erstellt wird, aber der Artikel noch nicht im Quarantänelagerort ist, erhält der Quarantäneauftrag den Status **Erstellt**.</span><span class="sxs-lookup"><span data-stu-id="de3bc-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="de3bc-126">Es werden zwei Lagerbuchungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="de3bc-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="de3bc-127">Eine Transaktion ist eine Problemtransaktion, die den Status **In Auftrag**, **Physisch reserviert**, oder **Entnommen** haben kann.</span><span class="sxs-lookup"><span data-stu-id="de3bc-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="de3bc-128">Die andere Transaktion ist eine Empfangstransaktion, die am Quarantänelagerort den Status **Bestellt** oder **Erfasst** haben kann.</span><span class="sxs-lookup"><span data-stu-id="de3bc-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="de3bc-129">Sie können Bestandsaktualisierungen mit den üblichen Prozessen reservieren, abholen oder erfassen.</span><span class="sxs-lookup"><span data-stu-id="de3bc-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="de3bc-130">Gestartet</span><span class="sxs-lookup"><span data-stu-id="de3bc-130">Started</span></span>

<span data-ttu-id="de3bc-131">Wenn ein Quarantäneauftrag den Status **Gestartet** aufweist, wird der Bestand vom regulären Lagerort an den Quarantänelagerort übertragen und es werden zwei Bestandtransaktionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="de3bc-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="de3bc-132">Eine Transaktion hat den Status **Entnommen** und die andere Transkation hat den Status **Erhalten**.</span><span class="sxs-lookup"><span data-stu-id="de3bc-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="de3bc-133">Gleichzeitig werden zwei Lagerbuchungen für die Rückumlagerung erstellt.</span><span class="sxs-lookup"><span data-stu-id="de3bc-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="de3bc-134">Diese Buchungen werden nicht mit einem Datum versehen.</span><span class="sxs-lookup"><span data-stu-id="de3bc-134">These transactions aren't dated.</span></span> <span data-ttu-id="de3bc-135">Eine Transaktion hat den Status **physisch reserviert** und die andere Transkation hat den Status **Bestellt**.</span><span class="sxs-lookup"><span data-stu-id="de3bc-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="de3bc-136">Fertig gemeldet</span><span class="sxs-lookup"><span data-stu-id="de3bc-136">Reported as finished</span></span>

<span data-ttu-id="de3bc-137">Per Klick auf **Als beendet melden** können Sie einen begonnenen Quarantäneauftrag als beendet melden.</span><span class="sxs-lookup"><span data-stu-id="de3bc-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="de3bc-138">Der Artikel wird aus der Quarantäne entlassen, jedoch noch nicht an den normalen Lagerort umgelagert.</span><span class="sxs-lookup"><span data-stu-id="de3bc-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="de3bc-139">Die Rückverschiebung zum normalen Lagerort kann mithilfe einer Wareneingangserfassung erfolgen, die während der Prozesses "Als beendet melden" ausgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="de3bc-139">The movement back to the regular warehouse can be procesed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="de3bc-140">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="de3bc-140">Ended</span></span>

<span data-ttu-id="de3bc-141">Wenn ein Quarantäneauftrag beendet wird, wird der Artikel vom Quarantänelagerort zurück an den normalen Lagerort umgelagert.</span><span class="sxs-lookup"><span data-stu-id="de3bc-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="de3bc-142">Der Status der Artikelbuchung wird am Quarantänelagerort auf **Verkauft** und am normalen Lagerort auf **Gekauft** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="de3bc-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="de3bc-143">Quarantäneauftrags-Ausschuss</span><span class="sxs-lookup"><span data-stu-id="de3bc-143">Quarantine order scrap</span></span>
<span data-ttu-id="de3bc-144">Als Teil des Quarantäneauftragsprozesses ist es möglich, Bestand als Ausschuss kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="de3bc-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="de3bc-145">Wenn Ausschuss verarbeitet wird, wird der Bestand durch eine Problemtransaktion vom Quarantänelagerort auf **Verkauft** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="de3bc-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="de3bc-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de3bc-146">See also</span></span>
--------

[<span data-ttu-id="de3bc-147">Sperrung von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="de3bc-147">Inventory blocking</span></span>](inventory-blocking.md)

