---
title: Unterstützung der Kanban-Übertragungskarte für Strichcodescanner
description: Die Kanban-Umlagerungsübersicht unterstützt die Scanner-Eingabe von einem Widgetstrichcodescanner bei der Auswahl, dem Starten, dem Abschluss und dem Leeren eines Kanban-Einzelvorgangs.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "319453"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="90361-103">Unterstützung der Kanban-Übertragungskarte für Strichcodescanner</span><span class="sxs-lookup"><span data-stu-id="90361-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90361-104">Die Kanban-Umlagerungsübersicht unterstützt die Scanner-Eingabe von einem Widgetstrichcodescanner bei der Auswahl, dem Starten, dem Abschluss und dem Leeren eines Kanban-Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="90361-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="90361-105">Erfassungsmodi</span><span class="sxs-lookup"><span data-stu-id="90361-105">Registration modes</span></span>
------------------

<span data-ttu-id="90361-106">Auf dem Inforegister **Scanner-Erfassung** können Sie den Registrierungsmodus auswählen, der die Aktivität steuert, wenn Sie eine Kanban-Kartennummer scannen oder manuell im Nummernfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="90361-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="90361-107">Erfassungsmodus festlegen</span><span class="sxs-lookup"><span data-stu-id="90361-107">Set registration mode</span></span> | <span data-ttu-id="90361-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90361-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90361-109">Start</span><span class="sxs-lookup"><span data-stu-id="90361-109">Start</span></span>                 | <span data-ttu-id="90361-110">Registriert einen Kanban-Umlagerungseinzelvorgang als 'In Bearbeitung'.</span><span class="sxs-lookup"><span data-stu-id="90361-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="90361-111">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="90361-111">Complete</span></span>              | <span data-ttu-id="90361-112">Registriert einen Kanban-Umlagerungseinzelvorgang als 'Abgeschlossen'.</span><span class="sxs-lookup"><span data-stu-id="90361-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="90361-113">Leer</span><span class="sxs-lookup"><span data-stu-id="90361-113">Empty</span></span>                 | <span data-ttu-id="90361-114">Registriert die Handhabungseinheit, auf die von der Kanban-Karte verwiesen wird, als leer.</span><span class="sxs-lookup"><span data-stu-id="90361-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="90361-115">Auswählen</span><span class="sxs-lookup"><span data-stu-id="90361-115">Select</span></span>                | <span data-ttu-id="90361-116">Registriert eine Kanban-Kartennummer und wählt automatisch den Einzelvorgang in der Kanban-Einzelvorgangsliste aus.</span><span class="sxs-lookup"><span data-stu-id="90361-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="90361-117">Erfassungsmodusauswahl</span><span class="sxs-lookup"><span data-stu-id="90361-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="90361-118">Wenn Sie einen Barcodeleser verwenden, um einen Einzelvorgang auszuwählen, ändert sich der Ansichtsmodus der Kanban-Übersicht.</span><span class="sxs-lookup"><span data-stu-id="90361-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="90361-119">In diesem Modus gelten folgende Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="90361-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="90361-120">Nur der gescannte Kanban-Einzelvorgang wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90361-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="90361-121">Die Details des gewählten Einzelvorgangs werden auf dem Inforegister **Details** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90361-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="90361-122">Das Inforegister **Meldungen** zeigt nur Nachrichten für den ausgewählten Einzelvorgang an.</span><span class="sxs-lookup"><span data-stu-id="90361-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="90361-123">Sie können den Status des Einzelvorgangs ändern, indem Sie die Funktionen verwenden, die im Aktivitätsbereich verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="90361-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="90361-124">Die Kanban-Übertragungskarte zeigt weiterhin nur einen einzelnen Einzelvorgang für diesen Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="90361-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="90361-125">Sie können die Informationen in der Liste der Einzelvorgänge manuell aktualisieren, indem Sie auf **Aktualisieren** (UMSCHALT+F5) im Aktivitätsbereich klicken.</span><span class="sxs-lookup"><span data-stu-id="90361-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="90361-126">Nachdem Sie die Informationen aktualisiert haben, werden die vollständigen Ergebnisse für den Einzelvorgangsfilter wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90361-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="90361-127">Einzelvorgangsstatus und mögliche Maßnahmen</span><span class="sxs-lookup"><span data-stu-id="90361-127">Job status and possible actions</span></span>
<span data-ttu-id="90361-128">Der Status des ausgewählten Einzelvorgangs und der Status sämtlicher angeschlossenen Einzelvorgänge für Ereignis-Kanbans bestimmt, ob Sie den Einzelvorgang weiter bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="90361-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="90361-129">Die folgende Tabelle enthält Informationen zu diesen Status und Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="90361-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="90361-130">Die Status, die für Einzelvorgänge verfügbar sind, oder für die Handhabungseinheiten, auf die von den Einzelvorgängen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="90361-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="90361-131">Jede Aufgabe, die Sie für den Einzelvorgang ausführen können.</span><span class="sxs-lookup"><span data-stu-id="90361-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="90361-132">Einzelvorgangstyp</span><span class="sxs-lookup"><span data-stu-id="90361-132">Job type</span></span></th>
<th><span data-ttu-id="90361-133">Einzelvorgangsstatus oder Status der Handhabungseinheit</span><span class="sxs-lookup"><span data-stu-id="90361-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="90361-134">Entnahmeliste aktualisieren</span><span class="sxs-lookup"><span data-stu-id="90361-134">Update picking list</span></span></th>
<th><span data-ttu-id="90361-135">Start</span><span class="sxs-lookup"><span data-stu-id="90361-135">Start</span></span></th>
<th><span data-ttu-id="90361-136">Registrierung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="90361-136">Update registration</span></span></th>
<th><span data-ttu-id="90361-137">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="90361-137">Complete</span></span></th>
<th><span data-ttu-id="90361-138">Leer</span><span class="sxs-lookup"><span data-stu-id="90361-138">Empty</span></span></th>
<th><span data-ttu-id="90361-139">Ereignis-Kanbans erstellen</span><span class="sxs-lookup"><span data-stu-id="90361-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90361-140">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="90361-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="90361-141">Nicht geplant</span><span class="sxs-lookup"><span data-stu-id="90361-141">Not planned</span></span></li>
<li><span data-ttu-id="90361-142">Keine angeschlossenen Einzelvorgänge oder angeschlossenen Einzelvorgänge sind "Abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="90361-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="90361-143">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-143">Yes</span></span></td>
<td><span data-ttu-id="90361-144">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-144">Yes</span></span></td>
<td><span data-ttu-id="90361-145">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-145">Yes</span></span></td>
<td><span data-ttu-id="90361-146">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-146">Yes</span></span></td>
<td><span data-ttu-id="90361-147">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-147">No</span></span></td>
<td><span data-ttu-id="90361-148">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90361-149">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="90361-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="90361-150">Nicht geplant</span><span class="sxs-lookup"><span data-stu-id="90361-150">Not planned</span></span></li>
<li><span data-ttu-id="90361-151">Der angeschlossene Einzelvorgang ist nicht "Abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="90361-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="90361-152">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-152">Yes</span></span></td>
<td><span data-ttu-id="90361-153">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-153">No</span></span></td>
<td><span data-ttu-id="90361-154">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-154">Yes</span></span></td>
<td><span data-ttu-id="90361-155">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-155">No</span></span></td>
<td><span data-ttu-id="90361-156">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-156">No</span></span></td>
<td><span data-ttu-id="90361-157">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90361-158">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="90361-158">Transfer</span></span></td>
<td><span data-ttu-id="90361-159">In Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="90361-159">In progress</span></span></td>
<td><span data-ttu-id="90361-160">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-160">Yes</span></span></td>
<td><span data-ttu-id="90361-161">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-161">No</span></span></td>
<td><span data-ttu-id="90361-162">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-162">Yes</span></span></td>
<td><span data-ttu-id="90361-163">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-163">Yes</span></span></td>
<td><span data-ttu-id="90361-164">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-164">No</span></span></td>
<td><span data-ttu-id="90361-165">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90361-166">Umlagerung</span><span class="sxs-lookup"><span data-stu-id="90361-166">Transfer</span></span></td>
<td><span data-ttu-id="90361-167">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="90361-167">Completed</span></span></td>
<td><span data-ttu-id="90361-168">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-168">No</span></span></td>
<td><span data-ttu-id="90361-169">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-169">No</span></span></td>
<td><span data-ttu-id="90361-170">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-170">No</span></span></td>
<td><span data-ttu-id="90361-171">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-171">No</span></span></td>
<td><span data-ttu-id="90361-172">Ja</span><span class="sxs-lookup"><span data-stu-id="90361-172">Yes</span></span></td>
<td><span data-ttu-id="90361-173">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90361-174">Übertragung oder Prozess</span><span class="sxs-lookup"><span data-stu-id="90361-174">Transfer or process</span></span></td>
<td><span data-ttu-id="90361-175">Leer</span><span class="sxs-lookup"><span data-stu-id="90361-175">Empty</span></span></td>
<td><span data-ttu-id="90361-176">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-176">No</span></span></td>
<td><span data-ttu-id="90361-177">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-177">No</span></span></td>
<td><span data-ttu-id="90361-178">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-178">No</span></span></td>
<td><span data-ttu-id="90361-179">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-179">No</span></span></td>
<td><span data-ttu-id="90361-180">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-180">No</span></span></td>
<td><span data-ttu-id="90361-181">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90361-182">Übertragung oder Prozess</span><span class="sxs-lookup"><span data-stu-id="90361-182">Transfer or process</span></span></td>
<td><span data-ttu-id="90361-183">Eine Kanban-Karte wurde nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="90361-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="90361-184">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-184">No</span></span></td>
<td><span data-ttu-id="90361-185">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-185">No</span></span></td>
<td><span data-ttu-id="90361-186">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-186">No</span></span></td>
<td><span data-ttu-id="90361-187">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-187">No</span></span></td>
<td><span data-ttu-id="90361-188">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-188">No</span></span></td>
<td><span data-ttu-id="90361-189">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90361-190">Übertragung oder Prozess</span><span class="sxs-lookup"><span data-stu-id="90361-190">Transfer or process</span></span></td>
<td><span data-ttu-id="90361-191">Eine Kanban-Karte wurde gefunden, aber keinem Kanban zugewiesen</span><span class="sxs-lookup"><span data-stu-id="90361-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="90361-192">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-192">No</span></span></td>
<td><span data-ttu-id="90361-193">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-193">No</span></span></td>
<td><span data-ttu-id="90361-194">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-194">No</span></span></td>
<td><span data-ttu-id="90361-195">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-195">No</span></span></td>
<td><span data-ttu-id="90361-196">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-196">No</span></span></td>
<td><span data-ttu-id="90361-197">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90361-198">Verarbeiten</span><span class="sxs-lookup"><span data-stu-id="90361-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="90361-199">Nicht geplant</span><span class="sxs-lookup"><span data-stu-id="90361-199">Not planned</span></span></li>
<li><span data-ttu-id="90361-200">Vorbereitet</span><span class="sxs-lookup"><span data-stu-id="90361-200">Prepared</span></span></li>
<li><span data-ttu-id="90361-201">In Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="90361-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="90361-202">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-202">No</span></span></td>
<td><span data-ttu-id="90361-203">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-203">No</span></span></td>
<td><span data-ttu-id="90361-204">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-204">No</span></span></td>
<td><span data-ttu-id="90361-205">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-205">No</span></span></td>
<td><span data-ttu-id="90361-206">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-206">No</span></span></td>
<td><span data-ttu-id="90361-207">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90361-208">Verarbeiten</span><span class="sxs-lookup"><span data-stu-id="90361-208">Process</span></span></td>
<td><span data-ttu-id="90361-209">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="90361-209">Completed</span></span></td>
<td><span data-ttu-id="90361-210">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-210">No</span></span></td>
<td><span data-ttu-id="90361-211">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-211">No</span></span></td>
<td><span data-ttu-id="90361-212">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-212">No</span></span></td>
<td><span data-ttu-id="90361-213">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-213">No</span></span></td>
<td><span data-ttu-id="90361-214">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-214">No</span></span></td>
<td><span data-ttu-id="90361-215">Nein</span><span class="sxs-lookup"><span data-stu-id="90361-215">No</span></span></td>
</tr>
</tbody>
</table>





