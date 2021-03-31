---
title: Einen Produktprogrammplanungslauf überwachen
description: In diesem Abschnitt wird erläutert, wie der Produktionsplaner sehen kann, ob ein Masterplanungslauf läuft.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2dea87ac106e79339b8cb6bb2c28e36e35de4a1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226098"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="7c44f-103">Einen Produktprogrammplanungslauf überwachen</span><span class="sxs-lookup"><span data-stu-id="7c44f-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="7c44f-104">Verwenden Sie ein Gantt-Diagramm, um den Fortschritt der Masterplanung zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="7c44f-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="7c44f-105">Auf der Seite **Masterplanungsfortschritt anzeigen** können Sie Details zu historischen Masterplanungsläufen als Gantt-Diagramm anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="7c44f-106">Diese Funktionalität kann Ihnen helfen, die Zeit zu verstehen, die für die verschiedenen Phasen der Masterplanung aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c44f-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="7c44f-107">Für einen aktuellen aktiven Planungsauftrag kann die Seite **Masterplanungsfortschritt anzeigen** verwendet werden, um den Fortschritt zu verfolgen und die geschätzte Restzeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="7c44f-108">Einschalten und Verwenden der Visualisierungsfunktion für den Fortschritt des Masterplans</span><span class="sxs-lookup"><span data-stu-id="7c44f-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="7c44f-109">Um diese Funktionalität zu nutzen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="7c44f-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="7c44f-110">Wählen Sie im Arbeitsbereich **Feature-Management** auf der Registerkarte **Neu** **Masterplanung Fortschrittsvisualisierung** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="7c44f-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="7c44f-111">Wenn die Funktion nicht auf der Registerkarte **Neu** erscheint, schauen Sie auf die Registerkarten **Nicht aktiviert** und **Alle**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="7c44f-112">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-112">Select **Enable now**.</span></span> <span data-ttu-id="7c44f-113">Alternativ können Sie auch **Terminplanung** wählen und dann die Zeit auswählen, zu der die Funktion eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c44f-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="7c44f-114">Auf der Seite **Masterplanungsfortschritt anzeigen** können sowohl historische Planungsaufträge als auch aktive Planungsaufträge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7c44f-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="7c44f-115">Um Aufträge zur historischen Planung anzuzeigen, gibt es zwei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="7c44f-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="7c44f-116">Gehen Sie zu **Masterplanung \> Einrichtung \> Pläne \> Masterpläne**, und wählen Sie dann im Aktionsbereich **Verlauf**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="7c44f-117">Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="7c44f-118">Gehen Sie zu **Masterplanung \> Arbeitsbereiche \> Masterplanung**, klicken Sie auf der Masterplantafel auf **Historie**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="7c44f-119">Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="7c44f-120">Um aktive Planungsjobs anzuzeigen, gibt es zwei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="7c44f-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="7c44f-121">Gehen Sie zu **Masterplanung \> Arbeitsbereiche \> Masterplanung**, wählen Sie im Aktionsbereich **Unfertiger Planungsprozess**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="7c44f-122">Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="7c44f-123">Gehen Sie zu **Masterplanung \> Arbeitsbereiche \> Masterplanung**, klicken Sie auf der Masterplantafel auf **Fortschritt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="7c44f-124">Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="7c44f-125">Beachten Sie, dass Sie aktive Aufträge nur dann anzeigen können, wenn ein Planungsauftrag bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="7c44f-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="7c44f-126">Analysieren eines Masterplanungsauftrags</span><span class="sxs-lookup"><span data-stu-id="7c44f-126">Analyze a master planning job</span></span>

<span data-ttu-id="7c44f-127">Im Gantt-Diagramm können Sie jeden der folgenden Planungsprozesse erweitern, um zusätzliche Details über die aufgewendete Zeit anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="7c44f-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="7c44f-128">Initialisierung wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="7c44f-128">Initializing</span></span>
- <span data-ttu-id="7c44f-129">Daten werden gelöscht und eingefügt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-129">Deleting and inserting data</span></span>
- <span data-ttu-id="7c44f-130">Dispositionsplanung</span><span class="sxs-lookup"><span data-stu-id="7c44f-130">Coverage planning</span></span>
- <span data-ttu-id="7c44f-131">Verzögerungen</span><span class="sxs-lookup"><span data-stu-id="7c44f-131">Delays</span></span>
- <span data-ttu-id="7c44f-132">Aktivitätsmeldungen</span><span class="sxs-lookup"><span data-stu-id="7c44f-132">Action messages</span></span>
- <span data-ttu-id="7c44f-133">Abschluss</span><span class="sxs-lookup"><span data-stu-id="7c44f-133">Finalization</span></span>
- <span data-ttu-id="7c44f-134">Automatische Umwandlung</span><span class="sxs-lookup"><span data-stu-id="7c44f-134">Auto-firming</span></span>

<span data-ttu-id="7c44f-135">Das Gantt-Diagramm ist ein nützliches Werkzeug, wenn Sie die Auswirkungen der Verwendung von Aktionsnachrichten sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="7c44f-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="7c44f-136">Navigation im Gantt-Diagramm</span><span class="sxs-lookup"><span data-stu-id="7c44f-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="7c44f-137">Um die ausgewählte Gruppe zu erweitern und die Details anzuzeigen, wählen Sie das Pluszeichen (**+**) in der Baumansicht.</span><span class="sxs-lookup"><span data-stu-id="7c44f-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="7c44f-138">Um die ausgewählte Gruppe zu komprimieren, wählen Sie das Minuszeichen (**-**) in der Baumansicht.</span><span class="sxs-lookup"><span data-stu-id="7c44f-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="7c44f-139">Sie können Ihre Tastatur zur Navigation verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c44f-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="7c44f-140">Verwenden Sie die Tasten **Pfeil nach oben** und **Pfeil nach unten**, um zwischen den Zeilen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="7c44f-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="7c44f-141">Verwenden Sie die Schaltflächen **Rechter Pfeil** und **Linker Pfeil**, um Gruppen auf- und zuklappen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="7c44f-142">Um alle Ebenen im Gantt-Diagramm zu öffnen oder zu schließen, wählen Sie **Alle erweitern** oder **Alle komprimieren**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="7c44f-143">Um die zugehörige Bearbeitungszeit anzuzeigen, fahren Sie mit der Maus über eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7c44f-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="7c44f-144">(Aufgaben sind die unterste Ebene im Gantt-Diagramm.)</span><span class="sxs-lookup"><span data-stu-id="7c44f-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="7c44f-145">Anzeigen eines zusätzlichen Masterplanungslaufs zum Vergleich von Jobs</span><span class="sxs-lookup"><span data-stu-id="7c44f-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="7c44f-146">Durch die Auswahl eines Masterplanungsauftrags im Feld **Zeige zusätzlichen Masterplanungslauf** können Sie einen zusätzlichen Masterplanungslauf im Gantt-Diagramm anzeigen und die beiden Aufträge vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="7c44f-147">Anzeige der Stücklistenstufen</span><span class="sxs-lookup"><span data-stu-id="7c44f-147">BOM-level display</span></span>

<span data-ttu-id="7c44f-148">Stücklistenstufen werden für die Disposition, Verzögerungen, Aktionen und Fixierungen unterschiedlich dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="7c44f-149">**Deckungsplanung** - Stücklistenstufen werden wie erwartet dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="7c44f-150">Sie werden von oben nach unten berechnet.</span><span class="sxs-lookup"><span data-stu-id="7c44f-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="7c44f-151">**Beispiel:** Stücklistenstufe 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="7c44f-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="7c44f-152">**Verzögerungen** - Stücklistenstufen werden angezeigt, wenn die Stücklistenstufen der Versorgungsplanung mit -1 multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="7c44f-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="7c44f-153">(Mit anderen Worten, sie haben ein negatives Vorzeichen.)</span><span class="sxs-lookup"><span data-stu-id="7c44f-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="7c44f-154">**Beispiel:** Stücklistenstufe -2, -1, 0</span><span class="sxs-lookup"><span data-stu-id="7c44f-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="7c44f-155">**Aktionsmeldung** - Stücklistenstufen werden wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="7c44f-156">Sie werden von oben nach unten berechnet.</span><span class="sxs-lookup"><span data-stu-id="7c44f-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="7c44f-157">**Beispiel:** Stücklistenstufe 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="7c44f-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="7c44f-158">**Automatische Umwandlung** - Stücklistenstufen werden mit 999 abzüglich der Versorgungsplanungsstücklistenstufe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="7c44f-159">**Beispiel:** Stücklistenstufe 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="7c44f-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="7c44f-160">Die folgende Tabelle fasst das Verhalten zusammen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="7c44f-161">Stücklistenstufe, die angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="7c44f-161">BOM level that is shown</span></span> | <span data-ttu-id="7c44f-162">Endprodukt</span><span class="sxs-lookup"><span data-stu-id="7c44f-162">End item</span></span> | <span data-ttu-id="7c44f-163">Unterkomponente</span><span class="sxs-lookup"><span data-stu-id="7c44f-163">Subcomponent</span></span> | <span data-ttu-id="7c44f-164">Rohmaterial</span><span class="sxs-lookup"><span data-stu-id="7c44f-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="7c44f-165">Dispositionsplanung</span><span class="sxs-lookup"><span data-stu-id="7c44f-165">Coverage planning</span></span> | <span data-ttu-id="7c44f-166">0</span><span class="sxs-lookup"><span data-stu-id="7c44f-166">0</span></span> | <span data-ttu-id="7c44f-167">1</span><span class="sxs-lookup"><span data-stu-id="7c44f-167">1</span></span> | <span data-ttu-id="7c44f-168">2</span><span class="sxs-lookup"><span data-stu-id="7c44f-168">2</span></span> |
| <span data-ttu-id="7c44f-169">Verzögerungen</span><span class="sxs-lookup"><span data-stu-id="7c44f-169">Delays</span></span> | <span data-ttu-id="7c44f-170">0</span><span class="sxs-lookup"><span data-stu-id="7c44f-170">0</span></span> | <span data-ttu-id="7c44f-171">–1</span><span class="sxs-lookup"><span data-stu-id="7c44f-171">–1</span></span> | <span data-ttu-id="7c44f-172">–2</span><span class="sxs-lookup"><span data-stu-id="7c44f-172">–2</span></span> |
| <span data-ttu-id="7c44f-173">Aktivitätsmeldung</span><span class="sxs-lookup"><span data-stu-id="7c44f-173">Action message</span></span> | <span data-ttu-id="7c44f-174">0</span><span class="sxs-lookup"><span data-stu-id="7c44f-174">0</span></span> | <span data-ttu-id="7c44f-175">1</span><span class="sxs-lookup"><span data-stu-id="7c44f-175">1</span></span> | <span data-ttu-id="7c44f-176">2</span><span class="sxs-lookup"><span data-stu-id="7c44f-176">2</span></span> |
| <span data-ttu-id="7c44f-177">Automatische Umwandlung</span><span class="sxs-lookup"><span data-stu-id="7c44f-177">Auto-firming</span></span> | <span data-ttu-id="7c44f-178">999</span><span class="sxs-lookup"><span data-stu-id="7c44f-178">999</span></span> | <span data-ttu-id="7c44f-179">998</span><span class="sxs-lookup"><span data-stu-id="7c44f-179">998</span></span> | <span data-ttu-id="7c44f-180">997</span><span class="sxs-lookup"><span data-stu-id="7c44f-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="7c44f-181">Visualisieren des Fortschritts</span><span class="sxs-lookup"><span data-stu-id="7c44f-181">Visualize progress</span></span>

<span data-ttu-id="7c44f-182">Wenn Sie einen Masterplanungsauftrag anzeigen, der gerade ausgeführt wird, wird der Fortschritt durch Farben im Gantt-Diagramm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="7c44f-183">Die folgenden Farben gelten für das blaue Thema.</span><span class="sxs-lookup"><span data-stu-id="7c44f-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="7c44f-184">Bei anderen Farbthemen sind die Farben unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="7c44f-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="7c44f-185">**Dunkelblau** - Erledigte Planungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="7c44f-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="7c44f-186">**Orange** - Die Aufgabe, die gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c44f-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="7c44f-187">**Hellblau** - Die Schätzung für die verbleibenden Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="7c44f-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="7c44f-188">Die Farbe wird im Gantt-Diagramm nur auf der untersten Ebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c44f-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="7c44f-189">Wählen Sie **Alle erweitern**, um alle Aufgaben im Masterplanungsauftrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="7c44f-190">Die Schätzung der verbleibenden Aufgaben basiert auf historischen Masterplanungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="7c44f-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="7c44f-191">Durchführung der Masterplanung und Verfolgung der Bearbeitungszeit</span><span class="sxs-lookup"><span data-stu-id="7c44f-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="7c44f-192">Wählen Sie im Standard-Dashboard **Masterplanung**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="7c44f-193">Geben Sie im Feld **Plan** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7c44f-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="7c44f-194">Wählen Sie **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="7c44f-194">Select **Run**.</span></span>
1. <span data-ttu-id="7c44f-195">Stellen Sie die Option **Verarbeitungszeit der Tracks** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="7c44f-196">Geben Sie im Feld **Anzahl von Threads** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7c44f-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="7c44f-197">Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="7c44f-198">Wählen Sie im Raster die Zeile aus, in der das Feld **Feld** auf **Artikelnummer** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="7c44f-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="7c44f-199">Geben Sie im Feld **Kriterien** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7c44f-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="7c44f-200">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c44f-200">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]