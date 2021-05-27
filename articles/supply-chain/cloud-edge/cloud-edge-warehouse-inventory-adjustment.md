---
title: Lagerregulierung des Lagerorts
description: Dieses Thema enthält Informationen über die Erfassung und Verarbeitung von Lagerort-Bestandsanpassungen, wenn Sie Scale-Units verwenden.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026132"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="c2070-103">Lagerregulierung des Lagerorts</span><span class="sxs-lookup"><span data-stu-id="c2070-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c2070-104">Die Funktion Lagerbestand-Anpassung wird beim Ausführen von Cloud- und Edge-Scale-Einheiten für [Fertigungs-Workloads](cloud-edge-workload-manufacturing.md) und [Workloads der Lagerortverwaltung](cloud-edge-workload-warehousing.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2070-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="c2070-105">enn eine Arbeitskraft eine Bestandsanpassung mit der Lager-App gegen einen Scale-Unit-Workload der Lagerortverwaltung durchführt, muss die physische Bestandsaktualisierung durch den Batch-Auftrag **Lagerort-Bestandsanpassungs-Journal** verarbeitet werden, den Sie unter **Lagerverwaltung > Periodische Aufgaben > Lagerort-Bestandsanpassungs-Journal** ausführen und planen.</span><span class="sxs-lookup"><span data-stu-id="c2070-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="c2070-106">Die folgenden Lagerort-App-Arbeitsprozesse verwenden derzeit die **Erfassung von Bestandskorrekturen** bei Scale-Unit Workloads:</span><span class="sxs-lookup"><span data-stu-id="c2070-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="c2070-107">Anpassung ein/aus</span><span class="sxs-lookup"><span data-stu-id="c2070-107">Adjustment in/out</span></span>
- <span data-ttu-id="c2070-108">Permanente Inventur</span><span class="sxs-lookup"><span data-stu-id="c2070-108">Cycle counting</span></span>
- <span data-ttu-id="c2070-109">Ladungsträgerladung</span><span class="sxs-lookup"><span data-stu-id="c2070-109">License plate loading</span></span>

<span data-ttu-id="c2070-110">Mehrere Transaktionen bei im Rahmen jeder Bestandsanpassung erstellt, da die Hub- und Skalierungseinheiteneinsätze die Datensätze für den Bestand gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="c2070-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="c2070-111">Beispiel für Bestandsanpassung</span><span class="sxs-lookup"><span data-stu-id="c2070-111">Inventory adjustment example</span></span>

<span data-ttu-id="c2070-112">In diesem Beispiel hat eine Arbeitskraft im Lagerort die App Lagerort verwendet, um das Hinzufügen von Lagerbestand zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2070-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="c2070-113">Der Scale-Unit Workload erstellt zunächst eine Lagerort-Bestandsanpassungstransaktion für die positive physische Anpassung, die dann mit dem Hub synchronisiert wird und zu einer Erhöhung des Lagerbestands auf dem Hub führt.</span><span class="sxs-lookup"><span data-stu-id="c2070-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="c2070-114">Typ</span><span class="sxs-lookup"><span data-stu-id="c2070-114">Type</span></span>                                    | <span data-ttu-id="c2070-115">Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="c2070-115">Scale unit</span></span> | <span data-ttu-id="c2070-116">Planungsrichtung</span><span class="sxs-lookup"><span data-stu-id="c2070-116">Direction</span></span> | <span data-ttu-id="c2070-117">Hub</span><span class="sxs-lookup"><span data-stu-id="c2070-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="c2070-118">Lagerregulierung des Lagerorts</span><span class="sxs-lookup"><span data-stu-id="c2070-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="c2070-119">+1</span><span class="sxs-lookup"><span data-stu-id="c2070-119">+1</span></span>         | ->        | <span data-ttu-id="c2070-120">+1</span><span class="sxs-lookup"><span data-stu-id="c2070-120">+1</span></span>  |

<span data-ttu-id="c2070-121">Der Hub verarbeitet dann eine Zähljournalbuchung, die über [Nachrichtenprozessor-Nachrichten](cloud-edge-message-processor-messages.md) empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c2070-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="c2070-122">Damit wird der zusätzliche Lagerbestand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c2070-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="c2070-123">Um doppelte Bestände zu vermeiden, erstellt der Hub als Teil dieses Prozesses eine Offset-Transaktion und entfernt den zuvor erfassten Lagerbestand, der sich auf den Lagerort-Bestandsabgleich bezieht.</span><span class="sxs-lookup"><span data-stu-id="c2070-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="c2070-124">Typ</span><span class="sxs-lookup"><span data-stu-id="c2070-124">Type</span></span>                                    | <span data-ttu-id="c2070-125">Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="c2070-125">Scale unit</span></span> | <span data-ttu-id="c2070-126">Planungsrichtung</span><span class="sxs-lookup"><span data-stu-id="c2070-126">Direction</span></span> | <span data-ttu-id="c2070-127">Hub</span><span class="sxs-lookup"><span data-stu-id="c2070-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="c2070-128">Inventur</span><span class="sxs-lookup"><span data-stu-id="c2070-128">Counting</span></span>                                | <span data-ttu-id="c2070-129">+1</span><span class="sxs-lookup"><span data-stu-id="c2070-129">+1</span></span>         | <-        | <span data-ttu-id="c2070-130">+1</span><span class="sxs-lookup"><span data-stu-id="c2070-130">+1</span></span>  |
| <span data-ttu-id="c2070-131">Lagerort-Bestandsanpassung (Offset)</span><span class="sxs-lookup"><span data-stu-id="c2070-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="c2070-132">-1</span><span class="sxs-lookup"><span data-stu-id="c2070-132">-1</span></span>         | <-        | <span data-ttu-id="c2070-133">-1</span><span class="sxs-lookup"><span data-stu-id="c2070-133">-1</span></span>  |

<span data-ttu-id="c2070-134">Nachdem eine Scale-Unit ein **Abgleichsjournal für den Lagerort** auf dem Hub erstellt hat, können Sie sowohl das **Zähljournal** als auch das **Gegenbuchung** überprüfen, die vom Hub als Teil des Abgleichsprozesses erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c2070-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="c2070-135">Sie können jede dieser Journaleinträge und Transaktionen im Supply Chain Management überprüfen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c2070-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="c2070-136">Melden Sie sich bei der Scale-Unit an.</span><span class="sxs-lookup"><span data-stu-id="c2070-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="c2070-137">Gehe zu **Lagerortverwaltung \> Periodische Aufgaben \> Erfassung des Lagerort-Bestandes**.</span><span class="sxs-lookup"><span data-stu-id="c2070-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="c2070-138">Suchen und öffnen Sie auf der Seite **Lagerort-Bestandsanpassungsjournal** das Journal, das die Änderung des Lagerbestands erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="c2070-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="c2070-139">Der Bereich **Journalzeilen** zeigt jede Anpassung, die von diesem Journal erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="c2070-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="c2070-140">Melden Sie sich am Hub an.</span><span class="sxs-lookup"><span data-stu-id="c2070-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="c2070-141">Gehe zu **Lagerortverwaltung \> Periodische Aufgaben \> Erfassung des Lagerort-Bestandes**.</span><span class="sxs-lookup"><span data-stu-id="c2070-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="c2070-142">Auf der Seite **Lagerort-Bestandsanpassungsjournal** sollte das gleiche Journal aufgeführt sein, wenn Hub und Scale-Unit synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2070-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="c2070-143">Öffnen Sie die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="c2070-143">Open the journal.</span></span> <span data-ttu-id="c2070-144">Wenn die [Nachrichten des Nachrichtenverarbeiters](cloud-edge-message-processor-messages.md) verarbeitet wurden, sehen Sie in der Kopfzeile Verknüpfungen zum **Zähljournal** und zur **Gegenbuchung**.</span><span class="sxs-lookup"><span data-stu-id="c2070-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="c2070-145">Das **Zähljournal** sollte die gleichen Dimensionswerte wie die Journalzeilen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c2070-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="c2070-146">Die **Gegenbuchung** sollte den Offset anzeigen, der die doppelte Bestandskorrektur beseitigt.</span><span class="sxs-lookup"><span data-stu-id="c2070-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="c2070-147">Wenn alle Synchronisierungen und Verarbeitungen abgeschlossen sind, werden das **Zähljournal** und das **Gegenbuchung** wieder mit der Scale-Unit synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c2070-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="c2070-148">Diese können auch auf der entsprechenden Seite **Erfassung der Lagerort-Bestandsanpassung** eingesehen werden.</span><span class="sxs-lookup"><span data-stu-id="c2070-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
