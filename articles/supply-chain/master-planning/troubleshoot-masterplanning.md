---
title: Behebung von Problemen bei der Produktprogrammplanung
description: Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Produktprogrammplanung auftreten können.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8e78634c0efb1c401297559ce40b2ca30519f3bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809469"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="9ed1d-103">Fehlerbehebung bei der Produktprogrammplanung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-103">Troubleshoot master planning</span></span>

<span data-ttu-id="9ed1d-104">Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Produktprogrammplanung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="9ed1d-105">Die Stücklistenauflösung verhält sich für umgewandelte Produktionsaufträge und für geschätzte Produktionsaufträge für manuell erstellte Arbeiten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ed1d-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-106">Issue description</span></span>

<span data-ttu-id="9ed1d-107">Wenn ein Produktionsauftrag umgewandelt ist, werden die Elemente nicht aufgelöst, wenn Sie die Stückliste auflösen.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="9ed1d-108">Wenn Sie jedoch einen Arbeitsauftrag manuell erstellen und dann den Produktionsauftrag schätzen, werden die Elemente aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ed1d-109">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-109">Issue resolution</span></span>

<span data-ttu-id="9ed1d-110">Das System arbeitet wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-110">The system is working as expected.</span></span> <span data-ttu-id="9ed1d-111">Die Auflösung, die erfolgt, wenn der Produktionsauftrag umgewandelt wird, zeigt auf den Planauftrag, aber es scheint nicht so, als ob der Planauftrag in diesem Fall aktuell umgewandelt ist.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="9ed1d-112">Wenn der Produktionsauftrag jedoch geschätzt wurde, wird die Auflösung vom freigegebenen Produktionsauftrag ausgelöst, wenn kein Planauftrag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="9ed1d-113">Der Wert Verzögerung wird nicht aktualisiert, wenn ich einen Planauftrag neu terminiere.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="9ed1d-114">Um die Verzögerung für Planaufträge zu aktualisieren, öffnen Sie das Dialogfeld **Umplanung** für den Planauftrag.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="9ed1d-115">Stellen Sie auf dem Inforegister **Auflösung** sicher, dass die Option **Auflösung nach Neuterminierung durchführen** auf *Ja* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="9ed1d-116">Die Produktionsplanung berücksichtigt nicht die Sicherheitsmargen, die in der Elementabdeckung für Bedarfsverursacher festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ed1d-117">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-117">Issue description</span></span>

<span data-ttu-id="9ed1d-118">Die Produktprogrammplanung berücksichtigt die Sicherheitsabstände.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="9ed1d-119">Bei der Terminierung von geplanten Produktionsaufträgen werden die Sicherheitsmargen jedoch ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ed1d-120">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-120">Issue resolution</span></span>

<span data-ttu-id="9ed1d-121">Ränder werden nur bei der Produktprogrammplanung berücksichtigt, nicht bei der manuellen Terminierung.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="9ed1d-122">Die Sicherheitsmargen sind als Puffer während der Planungsphase gedacht, um einen gewissen „Spielraum“ für den tatsächlichen Prozess zu haben.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="9ed1d-123">Um das gewünschte Ergebnis zu erhalten, können Sie die Marge entfernen.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="9ed1d-124">Der Arbeitsplan muss dann so aktualisiert werden, dass er die gewünschte Zeit enthält (z. B. als Warteschlangenzeit).</span><span class="sxs-lookup"><span data-stu-id="9ed1d-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="9ed1d-125">Sowohl die Produktprogrammplanung als auch die manuelle Terminierung sollten dann das gleiche Ergebnis liefern.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="9ed1d-126">Planaufträge werden generiert, obwohl wir Elemente auf Lager haben und bereits Produktionsaufträge für sie existieren.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="9ed1d-127">Sie können dieses Problem möglicherweise beheben, indem Sie den Wert **Positive Tage** für die betreffenden Gruppen auf der Seite **Deckungsgruppe** erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="9ed1d-128">Diese Änderung bewirkt, dass das System ermittelt, ob der vorhandene Bestand für den Bedarf verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="9ed1d-129">Dann wird für die Elemente, die auf Lager sind, kein neuer Planauftrag generiert.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="9ed1d-130">Die Produktprogrammplanung scheint Kapazitätsbeschränkungen nicht zu respektieren und terminiert mehr als die verfügbare Kapazität.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ed1d-131">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-131">Issue description</span></span>

<span data-ttu-id="9ed1d-132">Wenn Sie eine Vorgangsterminierung verwenden, bei der es eine endliche Kapazität gibt und der Arbeitsplan eine Mischung aus Bedarfen sowohl für eine Ressourcengruppe als auch für einzelne Ressourcen angibt, besteht eine kleine Chance auf Überbuchung aufgrund der Art und Weise, wie der Algorithmus auf Kapazitätskonflikte prüft.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="9ed1d-133">Diese Überbuchung kann auftreten, wenn Sie Helfer zur Ausführung der Produktprogrammplanung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="9ed1d-134">Sie tritt am ehesten auf, wenn es viele Aufträge gibt, die eine relativ kurze Laufzeit haben.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ed1d-135">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-135">Issue resolution</span></span>

<span data-ttu-id="9ed1d-136">Wenn es wichtig ist, dass bei der Vorgangsterminierung keine Überbuchung auftritt, können Sie den Terminierungsteil der Produktprogrammplanung single-threaded machen, indem Sie die Option **Genaue endliche Kapazität für Vorgangsterminierung** auf der Seite **Parameter der Produktprogrammplanung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="9ed1d-137">Diese Option ist standardmäßig nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-137">This option isn't available by default.</span></span> <span data-ttu-id="9ed1d-138">Sie müssen sie manuell auf der Seite hinzufügen, indem Sie die Funktionen zur Personalisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="9ed1d-139">Wenn Sie diese Option verwenden, läuft die Planung aufgrund der fehlenden Parallelverarbeitung langsamer.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="9ed1d-140">Die Aktualisierung geplanter Aufträge nimmt viel Zeit in Anspruch.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ed1d-141">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-141">Issue description</span></span>

<span data-ttu-id="9ed1d-142">Wenn Sie die Bedarfsmenge und/oder das Lieferdatum eines Planauftrags aktualisieren, dauert es normalerweise mindestens 30 Sekunden pro Auftrag, bis die Aktualisierung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ed1d-143">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="9ed1d-143">Issue resolution</span></span>

<span data-ttu-id="9ed1d-144">Dies ist ein bekanntes Problem mit der integrierten Produktprogrammplanung.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="9ed1d-145">Es wird durch die zugrundeliegende Autoauflösung durch die Stücklisten-Struktur während der Bearbeitungen verursacht.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="9ed1d-146">Dieses Problem wird in der Planungsoptimierung behoben, wo ein Planer die relevanten Aufträge aktualisieren und genehmigen kann und, wenn gewünscht, einen Planungslauf auslöst, um die Planaufträge für die zugrunde liegende Stückliste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="9ed1d-147">Eine Möglichkeit, die Leistung mit der eingebauten Produktprogrammplanung zu verbessern, ist Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9ed1d-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="9ed1d-148">Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="9ed1d-149">Wählen Sie einen Plan aus.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-149">Select a plan.</span></span>
1. <span data-ttu-id="9ed1d-150">Erweitern Sie das Inforegister **Zeitfenster in Tagen**.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="9ed1d-151">Legen Sie **Auflösung** auf *Ja* fest und setzen Sie das Feld unterhalb dieser Einstellung auf 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="9ed1d-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="9ed1d-152">Dadurch wird der Zeitraum für Auflösungen, die für diesen Masterplan durchgeführt werden, auf einen Tag begrenzt.</span><span class="sxs-lookup"><span data-stu-id="9ed1d-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]