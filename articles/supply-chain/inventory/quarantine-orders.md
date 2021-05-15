---
title: Quarantäneaufträge
description: Dieses Thema beschreibt, wie Sie Quarantäneaufträge verwenden, um Bestände zu sperren.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956181"
---
# <a name="quarantine-orders"></a><span data-ttu-id="74209-103">Quarantäneaufträge</span><span class="sxs-lookup"><span data-stu-id="74209-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74209-104">Dieses Thema beschreibt, wie Sie Quarantäneaufträge verwenden, um Bestände zu sperren.</span><span class="sxs-lookup"><span data-stu-id="74209-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="74209-105">Mit Quarantäneaufträgen können Sie Bestände sperren.</span><span class="sxs-lookup"><span data-stu-id="74209-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="74209-106">Beispielsweise empfiehlt es sich, Artikel aus Gründen der Qualitätskontrolle unter Quarantäne zu stellen.</span><span class="sxs-lookup"><span data-stu-id="74209-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="74209-107">Bestand, der unter Quarantäne gestellt wurde, wird an einen Quarantänelagerort übertragen.</span><span class="sxs-lookup"><span data-stu-id="74209-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="74209-108">Wenn Sie erweiterte Lagerortverwaltungsprozesse (in der Lagerortverwaltung) verwenden, wird die Quarantäneauftragsverarbeitung nur für Rücklieferungen von Verkaufsaufträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="74209-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="74209-109">Verfügbare Lagerartikel unter Quarantäne stellen</span><span class="sxs-lookup"><span data-stu-id="74209-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="74209-110">Wenn Sie Artikel unter Quarantäne stellen, können Sie die Quarantäneaufträge entweder manuell erstellen oder das System so einrichten, dass sie bei der eingehenden Verarbeitung automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="74209-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="74209-111">Um das System so festzulegen, dass es automatisch Quarantäneaufträge erzeugt, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="74209-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="74209-112">Gehen Sie zu **Inventarverwaltung \> Einrichten \> Bestand \> Element-Modellgruppen**.</span><span class="sxs-lookup"><span data-stu-id="74209-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="74209-113">Wählen Sie eine relevante Modellgruppe im Listenbereich aus oder erstellen Sie eine neue Modellgruppe.</span><span class="sxs-lookup"><span data-stu-id="74209-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="74209-114">Aktivieren Sie auf der Registerkarte **Inventarrichtlinien** das Kontrollkästchen **Quarantäneverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="74209-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="74209-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="74209-115">Close the page.</span></span>
1. <span data-ttu-id="74209-116">Geben Sie im Feld **Quarantänelager** für die empfangenden Lagerorte ein Standard-Quarantänelager an.</span><span class="sxs-lookup"><span data-stu-id="74209-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="74209-117">Wenn ein Element, das als im Lagerort eingegangen registriert ist, zu einer Modellgruppe gehört, in der das Kontrollkästchen **Quarantäneverwaltung** aktiviert ist, erzeugt das System einen Quarantäneauftrag für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="74209-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="74209-118">Der Quarantäneauftrag weist die Arbeitskräfte an, das Element in das Quarantäne-Lagerort zu bringen.</span><span class="sxs-lookup"><span data-stu-id="74209-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="74209-119">Wenn Sie Quarantäne-Aufträge manuell auf der Seite **Quarantäne-Aufträge** erstellen, muss das Element nicht in der zugehörigen Artikelmodellgruppe für die Quarantäne-Verwaltung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="74209-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="74209-120">Für diesen Vorgang müssen Sie den verfügbaren Lagerbestand, der unter Quarantäne gestellt werden soll, und den Quarantänelagerort angeben, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="74209-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="74209-121">Sie können den Quarantäneauftragsstatus verwenden, um die Planung des Vorgangs zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="74209-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="74209-122">Status des Quarantäneauftrags</span><span class="sxs-lookup"><span data-stu-id="74209-122">Quarantine order statuses</span></span>

<span data-ttu-id="74209-123">Quarantäneaufträge können folgende Status annehmen:</span><span class="sxs-lookup"><span data-stu-id="74209-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="74209-124">Erstellt</span><span class="sxs-lookup"><span data-stu-id="74209-124">Created</span></span>
- <span data-ttu-id="74209-125">Gestartet</span><span class="sxs-lookup"><span data-stu-id="74209-125">Started</span></span>
- <span data-ttu-id="74209-126">Fertig gemeldet</span><span class="sxs-lookup"><span data-stu-id="74209-126">Reported as finished</span></span>
- <span data-ttu-id="74209-127">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="74209-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="74209-128">Erstellt</span><span class="sxs-lookup"><span data-stu-id="74209-128">Created</span></span>

<span data-ttu-id="74209-129">Wenn ein Quarantäneauftrag manuell erstellt wird, aber der Artikel noch nicht im Quarantänelagerort ist, erhält der Quarantäneauftrag den Status **Erstellt**.</span><span class="sxs-lookup"><span data-stu-id="74209-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="74209-130">Es werden zwei Lagerbuchungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="74209-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="74209-131">Eine Transaktion ist eine Problemtransaktion, die den Status **In Auftrag**, **Physisch reserviert**, oder **Entnommen** haben kann.</span><span class="sxs-lookup"><span data-stu-id="74209-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="74209-132">Die andere Transaktion ist eine Empfangstransaktion, die am Quarantänelagerort den Status **Bestellt** oder **Erfasst** haben kann.</span><span class="sxs-lookup"><span data-stu-id="74209-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="74209-133">Sie können Bestandsaktualisierungen mit den üblichen Prozessen reservieren, abholen oder erfassen.</span><span class="sxs-lookup"><span data-stu-id="74209-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="74209-134">Gestartet</span><span class="sxs-lookup"><span data-stu-id="74209-134">Started</span></span>

<span data-ttu-id="74209-135">Wenn ein Quarantäneauftrag den Status **Gestartet** aufweist, wird der Bestand vom regulären Lagerort an den Quarantänelagerort übertragen und es werden zwei Bestandtransaktionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="74209-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="74209-136">Eine Transaktion hat den Status **Entnommen** und die andere Transkation hat den Status **Erhalten**.</span><span class="sxs-lookup"><span data-stu-id="74209-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="74209-137">Gleichzeitig werden zwei Lagerbuchungen für die Rückumlagerung erstellt.</span><span class="sxs-lookup"><span data-stu-id="74209-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="74209-138">Diese Buchungen werden nicht mit einem Datum versehen.</span><span class="sxs-lookup"><span data-stu-id="74209-138">These transactions aren't dated.</span></span> <span data-ttu-id="74209-139">Eine Transaktion hat den Status **physisch reserviert** und die andere Transkation hat den Status **Bestellt**.</span><span class="sxs-lookup"><span data-stu-id="74209-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="74209-140">Als fertig gemeldet</span><span class="sxs-lookup"><span data-stu-id="74209-140">Reported as finished</span></span>

<span data-ttu-id="74209-141">Um einen gestarteten Quarantäneauftrag als beendet zu melden, öffnen Sie den Auftrag und wählen Sie **Als beendet melden** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="74209-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="74209-142">Das Element wird aus der Quarantäne freigegeben, aber noch nicht zurück in den regulären Lagerort verschoben.</span><span class="sxs-lookup"><span data-stu-id="74209-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="74209-143">Die Bewegung zurück zum regulären Lagerort kann über eine Wareneingangserfassung verarbeitet werden, die während des Berichts als abgeschlossener Prozess initialisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74209-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="74209-144">Beendet</span><span class="sxs-lookup"><span data-stu-id="74209-144">Ended</span></span>

<span data-ttu-id="74209-145">Wenn ein Quarantäneauftrag beendet wird, wird der Artikel vom Quarantänelagerort zurück an den normalen Lagerort umgelagert.</span><span class="sxs-lookup"><span data-stu-id="74209-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="74209-146">Der Status der Artikelbuchung wird am Quarantänelagerort auf *Verkauft* und am normalen Lagerort auf *Gekauft* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74209-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="74209-147">Quarantäneauftrags-Ausschuss</span><span class="sxs-lookup"><span data-stu-id="74209-147">Quarantine order scrap</span></span>

<span data-ttu-id="74209-148">Als Teil des Quarantäneauftragsprozesses ist es möglich, Bestand als Ausschuss kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="74209-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="74209-149">Wenn Sie Ausschuss verarbeiten, wird der Status des Bestandes durch eine Ausgabe-Transaktion aus dem Quarantäne-Lagerort auf *Verkauft* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74209-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74209-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="74209-150">Additional resources</span></span>

- [<span data-ttu-id="74209-151">Sperrung von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="74209-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
