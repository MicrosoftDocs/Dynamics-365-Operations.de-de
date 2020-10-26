---
title: Lagerort-App-Ereignisse
description: In diesem Thema wird die Verarbeitung von Lager-App-Ereignissen beschrieben, mit der Lager-App-Ereignismeldungen als Teil eines Stapelauftrags verarbeitet werden.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988378"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="938cd-103">Verarbeitung von Lager-App-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="938cd-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="938cd-104">Batchaufträge, die in Supply Chain Management ausgeführt werden, können Daten aus einer Warteschlange zur Verarbeitung von Ereignissen verwenden, die von der Lager-App ausgegeben wurden, um bei Bedarf auf die signalisierten Ereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="938cd-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="938cd-105">Diese Funktion fügt der Warteschlange relevante Ereignisse als Reaktion auf bestimmte Arten von Aktionen hinzu, die von Mitarbeitern ausgeführt werden, die die App verwenden.</span><span class="sxs-lookup"><span data-stu-id="938cd-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="938cd-106">Ein Beispiel ist die Verwendung von **Erstellen und Verarbeiten von Umlagerungsaufträgen über die Lager-App**. Mit dieser Funktion werden die Überschrift und Positionen des Umlagerungsauftrags im Back-End erstellt und aktualisiert, wenn das System den Stapelauftrag **Verarbeiten von Lager-App-Ereignissen** ausführt.</span><span class="sxs-lookup"><span data-stu-id="938cd-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="938cd-107">Aktivieren Sie die Funktion Lager-App-Ereignisse verarbeiten</span><span class="sxs-lookup"><span data-stu-id="938cd-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="938cd-108">Bevor Sie diese Funktion nutzen können, müssen Sie diese auf Ihrem System aktivieren.</span><span class="sxs-lookup"><span data-stu-id="938cd-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="938cd-109">Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="938cd-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="938cd-110">Die Funktion Lager-App-Ereignisse verarbeiten ist aufgeführt als:</span><span class="sxs-lookup"><span data-stu-id="938cd-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="938cd-111">**Module** ‑ Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="938cd-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="938cd-112">**Funktionsname** - Lager-App-Ereignisse verarbeiten</span><span class="sxs-lookup"><span data-stu-id="938cd-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="938cd-113">Richten Sie einen Stapelauftrag ein, um Lager-App-Ereignisse zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="938cd-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="938cd-114">Lagerort-App-Ereignisse verarbeiten</span><span class="sxs-lookup"><span data-stu-id="938cd-114">Process warehouse app events</span></span>

<span data-ttu-id="938cd-115">Richten Sie einen geplanten Stapelauftrag ein, um die Lager-App-Ereignisse für die Erstellung des Umlagerungsauftrags und die Positionenaktualisierungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="938cd-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="938cd-116">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Lager-App-Ereignisse verarbeiten**.</span><span class="sxs-lookup"><span data-stu-id="938cd-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="938cd-117">Das Dialogfeld Lager-App-Ereignisse verarbeiten wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="938cd-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="938cd-118">Erweitern Sie das Inforegister **Im Hintergrund ausführen** und setzen Sie **Batchverarbeitung** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="938cd-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="938cd-119">Wählen Sie im Inforegister **Im Hintergrund ausführen** **Serie**.</span><span class="sxs-lookup"><span data-stu-id="938cd-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="938cd-120">Das Dialogfeld **Serie festlegen** öffnet sich.</span><span class="sxs-lookup"><span data-stu-id="938cd-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="938cd-121">Legen Sie den passenden Zeitplan für Ihr Unternehmen fest.</span><span class="sxs-lookup"><span data-stu-id="938cd-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="938cd-122">Wählen Sie **OK**, um zum Dialogfeld **Verarbeiten von Lager-App-Ereignissen** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="938cd-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="938cd-123">Wählen Sie **OK** im Dialogfeld **Lager-App-Ereignisse verarbeiten**, um den Stapelauftrag der Stapelwarteschlange hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="938cd-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="938cd-124">Abfrage von Lager-App-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="938cd-124">Query warehouse app events</span></span>

<span data-ttu-id="938cd-125">Sie können die Ereigniswarteschlange und die von der Lager-App generierten Ereignismeldungen anzeigen, indem Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Protokolle für mobile Geräte\> Lager-App-Ereignisse** gehen.</span><span class="sxs-lookup"><span data-stu-id="938cd-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="938cd-126">Der Standardprozess für Ereigniswarteschlangen</span><span class="sxs-lookup"><span data-stu-id="938cd-126">The standard event queue process</span></span>

<span data-ttu-id="938cd-127">Die Ereigniswarteschlange für Lager-Apps wird normalerweise mit dem folgenden beschriebenen Flow verwendet:</span><span class="sxs-lookup"><span data-stu-id="938cd-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="938cd-128">Ein Ereignis wird mit einer Ereignismeldung zur Warteschlange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="938cd-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="938cd-129">Die neue Nachricht hat zunächst den Ereignisstatus **Warten**, was bedeutet, dass der Stapelauftrag **Verarbeiten von Lager-App-Ereignissen** diese Nachricht nicht aufnimmt und nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="938cd-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="938cd-130">Sobald der Nachrichtenstatus auf **In Warteschlange** aktualisiert wird, nimmt der Stapelauftrag **Lager-App-Ereignisse verarbeiten** das Ereignis auf und verarbeitet es.</span><span class="sxs-lookup"><span data-stu-id="938cd-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="938cd-131">Der Stapelauftrag aktualisiert die Ereigniszustände entweder auf **Abgeschlossen** oder **Fehlgeschlagen**, abhängig davon, ob der angeforderte Prozess möglich war.</span><span class="sxs-lookup"><span data-stu-id="938cd-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="938cd-132">Wenn alle zugehörigen Ereignismeldungen **Abgeschlossen** sind, wird das Ereignis aus der Warteschlange gelöscht.</span><span class="sxs-lookup"><span data-stu-id="938cd-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="938cd-133">Ein detailliertes Beispiel finden Sie unter [Erstellen eines Umlagerungsauftrags aus der Lager-App-Verarbeiten](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="938cd-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="938cd-134">Behandeln von Ereignisfehlern</span><span class="sxs-lookup"><span data-stu-id="938cd-134">Handle event errors</span></span>

<span data-ttu-id="938cd-135">Im Rahmen der Lager-Ereignisverarbeitung empfängt die angeforderte Nachrichtenaktivität möglicherweise keine Prozesse vom Stapelauftrag.</span><span class="sxs-lookup"><span data-stu-id="938cd-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="938cd-136">In diesem Fall ändert sich die Ereignismeldung in **Fehlgeschlagen**.</span><span class="sxs-lookup"><span data-stu-id="938cd-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="938cd-137">Sie können die **Stapelverarbeitungsprotokoll**-Informationen verwenden, um zu erfahren, warum und welche Maßnahmen erforderlich sind, um Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="938cd-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="938cd-138">Ein detailliertes Beispiel finden Sie unter [Erstellen eines Umlagerungsauftrags aus der Lager-App](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="938cd-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="938cd-139">So setzen Sie eine fehlgeschlagene Lager-App-Ereignismeldung zurück:</span><span class="sxs-lookup"><span data-stu-id="938cd-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="938cd-140">Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Protokolle für mobile Geräte \> Lager-App-Ereignisse**.</span><span class="sxs-lookup"><span data-stu-id="938cd-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="938cd-141">Auf dem Inforegister **Lager-App-Ereignismeldungen** suchen und wählen Sie ein relevantes Ereignis aus, das **Fehlgeschlagen** in der Spalte **Ereignisstatus** anzeigt.</span><span class="sxs-lookup"><span data-stu-id="938cd-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="938cd-142">Wählen Sie **Zurücksetzen** auf der Symbolleiste **Lager-App-Ereignismeldungen** .</span><span class="sxs-lookup"><span data-stu-id="938cd-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="938cd-143">Arbeiten Sie weiter, bis alle relevanten Meldungen zurückgesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="938cd-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="938cd-144">Sie können auch eine **Fehlgeschlagen**-Ereignismeldung mit der Option **Löschen** auf der Symbolleiste **Lager-App-Ereignismeldungen** entfernen.</span><span class="sxs-lookup"><span data-stu-id="938cd-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
