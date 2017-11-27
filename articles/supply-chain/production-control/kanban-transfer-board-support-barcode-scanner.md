---
title: "Unterstützung der Kanban-Übertragungskarte für Strichcodescanner"
description: "Die Kanban-Umlagerungsübersicht unterstützt die Scanner-Eingabe von einem Widgetstrichcodescanner bei der Auswahl, dem Starten, dem Abschluss und dem Leeren eines Kanban-Einzelvorgangs."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8393efd51032271d3023f1e0569425a16222cc3
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="1fe3b-103">Unterstützung der Kanban-Übertragungskarte für Strichcodescanner</span><span class="sxs-lookup"><span data-stu-id="1fe3b-103">Kanban transfer board support for barcode scanners</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1fe3b-104">Die Kanban-Umlagerungsübersicht unterstützt die Scanner-Eingabe von einem Widgetstrichcodescanner bei der Auswahl, dem Starten, dem Abschluss und dem Leeren eines Kanban-Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="1fe3b-105">Erfassungsmodi</span><span class="sxs-lookup"><span data-stu-id="1fe3b-105">Registration modes</span></span>
------------------

<span data-ttu-id="1fe3b-106">Auf dem Inforegister **Scanner-Erfassung** können Sie den Registrierungsmodus auswählen, der die Aktivität steuert, wenn Sie eine Kanban-Kartennummer scannen oder manuell im Nummernfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>
| <span data-ttu-id="1fe3b-107">Erfassungsmodus festlegen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-107">Set registration mode</span></span> | <span data-ttu-id="1fe3b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe3b-109">Start</span><span class="sxs-lookup"><span data-stu-id="1fe3b-109">Start</span></span>                 | <span data-ttu-id="1fe3b-110">Registriert einen Kanban-Umlagerungseinzelvorgang als 'In Bearbeitung'.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="1fe3b-111">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-111">Complete</span></span>              | <span data-ttu-id="1fe3b-112">Registriert einen Kanban-Umlagerungseinzelvorgang als 'Abgeschlossen'.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="1fe3b-113">Leer</span><span class="sxs-lookup"><span data-stu-id="1fe3b-113">Empty</span></span>                 | <span data-ttu-id="1fe3b-114">Registriert die Handhabungseinheit, auf die von der Kanban-Karte verwiesen wird, als leer.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="1fe3b-115">Auswählen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-115">Select</span></span>                | <span data-ttu-id="1fe3b-116">Registriert eine Kanban-Kartennummer und wählt automatisch den Einzelvorgang in der Kanban-Einzelvorgangsliste aus.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="1fe3b-117">Erfassungsmodusauswahl</span><span class="sxs-lookup"><span data-stu-id="1fe3b-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="1fe3b-118">Wenn Sie einen Barcodeleser verwenden, um einen Einzelvorgang auszuwählen, ändert sich der Ansichtsmodus der Kanban-Übersicht.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="1fe3b-119">In diesem Modus gelten folgende Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="1fe3b-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="1fe3b-120">Nur der gescannte Kanban-Einzelvorgang wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="1fe3b-121">Die Details des gewählten Einzelvorgangs werden auf dem Inforegister **Details** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="1fe3b-122">Das Inforegister **Meldungen** zeigt nur Nachrichten für den ausgewählten Einzelvorgang an.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="1fe3b-123">Sie können den Status des Einzelvorgangs ändern, indem Sie die Funktionen verwenden, die im Aktivitätsbereich verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="1fe3b-124">Die Kanban-Übertragungskarte zeigt weiterhin nur einen einzelnen Einzelvorgang für diesen Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="1fe3b-125">Sie können die Informationen in der Liste der Einzelvorgänge manuell aktualisieren, indem Sie auf **Aktualisieren** (UMSCHALT+F5) im Aktivitätsbereich klicken.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="1fe3b-126">Nachdem Sie die Informationen aktualisiert haben, werden die vollständigen Ergebnisse für den Einzelvorgangsfilter wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="1fe3b-127">Einzelvorgangsstatus und mögliche Maßnahmen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-127">Job status and possible actions</span></span>
<span data-ttu-id="1fe3b-128">Der Status des ausgewählten Einzelvorgangs und der Status sämtlicher angeschlossenen Einzelvorgänge für Ereignis-Kanbans bestimmt, ob Sie den Einzelvorgang weiter bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="1fe3b-129">Die folgende Tabelle enthält Informationen zu diesen Status und Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="1fe3b-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="1fe3b-130">Die Status, die für Einzelvorgänge verfügbar sind, oder für die Handhabungseinheiten, auf die von den Einzelvorgängen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="1fe3b-131">Jede Aufgabe, die Sie für den Einzelvorgang ausführen können.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fe3b-132">Einzelvorgangstyp</span><span class="sxs-lookup"><span data-stu-id="1fe3b-132">Job type</span></span></th>
<th><span data-ttu-id="1fe3b-133">Einzelvorgangsstatus oder Status der Handhabungseinheit</span><span class="sxs-lookup"><span data-stu-id="1fe3b-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="1fe3b-134">Entnahmeliste aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1fe3b-134">Update picking list</span></span></th>
<th><span data-ttu-id="1fe3b-135">Start</span><span class="sxs-lookup"><span data-stu-id="1fe3b-135">Start</span></span></th>
<th><span data-ttu-id="1fe3b-136">Registrierung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1fe3b-136">Update registration</span></span></th>
<th><span data-ttu-id="1fe3b-137">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-137">Complete</span></span></th>
<th><span data-ttu-id="1fe3b-138">Leer</span><span class="sxs-lookup"><span data-stu-id="1fe3b-138">Empty</span></span></th>
<th><span data-ttu-id="1fe3b-139">Ereignis-Kanbans erstellen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fe3b-140">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="1fe3b-141">Nicht geplant</span><span class="sxs-lookup"><span data-stu-id="1fe3b-141">Not planned</span></span></li>
<li><span data-ttu-id="1fe3b-142">Keine angeschlossenen Einzelvorgänge oder angeschlossenen Einzelvorgänge sind "Abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="1fe3b-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="1fe3b-143">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-143">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-144">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-144">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-145">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-145">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-146">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-146">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-147">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-147">No</span></span></td>
<td><span data-ttu-id="1fe3b-148">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fe3b-149">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="1fe3b-150">Nicht geplant</span><span class="sxs-lookup"><span data-stu-id="1fe3b-150">Not planned</span></span></li>
<li><span data-ttu-id="1fe3b-151">Der angeschlossene Einzelvorgang ist nicht "Abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="1fe3b-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="1fe3b-152">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-152">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-153">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-153">No</span></span></td>
<td><span data-ttu-id="1fe3b-154">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-154">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-155">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-155">No</span></span></td>
<td><span data-ttu-id="1fe3b-156">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-156">No</span></span></td>
<td><span data-ttu-id="1fe3b-157">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fe3b-158">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-158">Transfer</span></span></td>
<td><span data-ttu-id="1fe3b-159">In Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-159">In progress</span></span></td>
<td><span data-ttu-id="1fe3b-160">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-160">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-161">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-161">No</span></span></td>
<td><span data-ttu-id="1fe3b-162">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-162">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-163">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-163">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-164">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-164">No</span></span></td>
<td><span data-ttu-id="1fe3b-165">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fe3b-166">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-166">Transfer</span></span></td>
<td><span data-ttu-id="1fe3b-167">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-167">Completed</span></span></td>
<td><span data-ttu-id="1fe3b-168">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-168">No</span></span></td>
<td><span data-ttu-id="1fe3b-169">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-169">No</span></span></td>
<td><span data-ttu-id="1fe3b-170">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-170">No</span></span></td>
<td><span data-ttu-id="1fe3b-171">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-171">No</span></span></td>
<td><span data-ttu-id="1fe3b-172">Ja</span><span class="sxs-lookup"><span data-stu-id="1fe3b-172">Yes</span></span></td>
<td><span data-ttu-id="1fe3b-173">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fe3b-174">Übertragung oder Prozess</span><span class="sxs-lookup"><span data-stu-id="1fe3b-174">Transfer or process</span></span></td>
<td><span data-ttu-id="1fe3b-175">Leer</span><span class="sxs-lookup"><span data-stu-id="1fe3b-175">Empty</span></span></td>
<td><span data-ttu-id="1fe3b-176">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-176">No</span></span></td>
<td><span data-ttu-id="1fe3b-177">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-177">No</span></span></td>
<td><span data-ttu-id="1fe3b-178">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-178">No</span></span></td>
<td><span data-ttu-id="1fe3b-179">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-179">No</span></span></td>
<td><span data-ttu-id="1fe3b-180">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-180">No</span></span></td>
<td><span data-ttu-id="1fe3b-181">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fe3b-182">Übertragung oder Prozess</span><span class="sxs-lookup"><span data-stu-id="1fe3b-182">Transfer or process</span></span></td>
<td><span data-ttu-id="1fe3b-183">Eine Kanban-Karte wurde nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="1fe3b-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="1fe3b-184">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-184">No</span></span></td>
<td><span data-ttu-id="1fe3b-185">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-185">No</span></span></td>
<td><span data-ttu-id="1fe3b-186">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-186">No</span></span></td>
<td><span data-ttu-id="1fe3b-187">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-187">No</span></span></td>
<td><span data-ttu-id="1fe3b-188">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-188">No</span></span></td>
<td><span data-ttu-id="1fe3b-189">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fe3b-190">Übertragung oder Prozess</span><span class="sxs-lookup"><span data-stu-id="1fe3b-190">Transfer or process</span></span></td>
<td><span data-ttu-id="1fe3b-191">Eine Kanban-Karte wurde gefunden, aber keinem Kanban zugewiesen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="1fe3b-192">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-192">No</span></span></td>
<td><span data-ttu-id="1fe3b-193">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-193">No</span></span></td>
<td><span data-ttu-id="1fe3b-194">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-194">No</span></span></td>
<td><span data-ttu-id="1fe3b-195">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-195">No</span></span></td>
<td><span data-ttu-id="1fe3b-196">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-196">No</span></span></td>
<td><span data-ttu-id="1fe3b-197">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fe3b-198">Verarbeiten</span><span class="sxs-lookup"><span data-stu-id="1fe3b-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="1fe3b-199">Nicht geplant</span><span class="sxs-lookup"><span data-stu-id="1fe3b-199">Not planned</span></span></li>
<li><span data-ttu-id="1fe3b-200">Vorbereitet</span><span class="sxs-lookup"><span data-stu-id="1fe3b-200">Prepared</span></span></li>
<li><span data-ttu-id="1fe3b-201">In Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="1fe3b-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="1fe3b-202">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-202">No</span></span></td>
<td><span data-ttu-id="1fe3b-203">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-203">No</span></span></td>
<td><span data-ttu-id="1fe3b-204">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-204">No</span></span></td>
<td><span data-ttu-id="1fe3b-205">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-205">No</span></span></td>
<td><span data-ttu-id="1fe3b-206">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-206">No</span></span></td>
<td><span data-ttu-id="1fe3b-207">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fe3b-208">Verarbeiten</span><span class="sxs-lookup"><span data-stu-id="1fe3b-208">Process</span></span></td>
<td><span data-ttu-id="1fe3b-209">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="1fe3b-209">Completed</span></span></td>
<td><span data-ttu-id="1fe3b-210">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-210">No</span></span></td>
<td><span data-ttu-id="1fe3b-211">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-211">No</span></span></td>
<td><span data-ttu-id="1fe3b-212">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-212">No</span></span></td>
<td><span data-ttu-id="1fe3b-213">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-213">No</span></span></td>
<td><span data-ttu-id="1fe3b-214">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-214">No</span></span></td>
<td><span data-ttu-id="1fe3b-215">Nein</span><span class="sxs-lookup"><span data-stu-id="1fe3b-215">No</span></span></td>
</tr>
</tbody>
</table>






