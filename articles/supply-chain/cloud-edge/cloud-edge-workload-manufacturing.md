---
title: Arbeitsauslastungen bei der Fertigungsausführung für Cloud- und Edge-Scale-Einheiten
description: Dieses Thema beschreibt, wie Arbeitsauslastungen für die Fertigungsausführung mit Cloud- und Edge Scale-Units funktionieren.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2021
ms.locfileid: "6183995"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="09e9b-103">Workloads in der Fertigungsausführung für Cloud- und Edge-Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="09e9b-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="09e9b-104">Der Workload für die Fertigungsausführung ist zu diesem Zeitpunkt in der Vorschau verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09e9b-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="09e9b-105">Einige Geschäftsfunktionen werden in der öffentlichen Vorschau nicht vollständig unterstützt, wenn Arbeitsauslastungen mit Scale-Units verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09e9b-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="09e9b-106">Bei der Ausführung der Fertigung bieten Skalierungseinheiten die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="09e9b-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="09e9b-107">Maschinenbediener und Werkstattleiter können auf den operativen Produktionsplan zugreifen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="09e9b-108">Maschinenbediener können den Plan auf dem neuesten Stand halten, indem sie diskrete und Prozessfertigungsaufträge ausführen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="09e9b-109">Der Fertigungsleiter kann den Betriebsplan anpassen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="09e9b-110">Die Arbeiter können auf die Zeiterfassung zugreifen, um die korrekte Berechnung der Löhne sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="09e9b-111">Dieses Thema beschreibt, wie Arbeitsauslastungen für die Fertigungsausführung mit Cloud- und Edge Scale-Units funktionieren.</span><span class="sxs-lookup"><span data-stu-id="09e9b-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="09e9b-112">Der Fertigungslebenszyklus</span><span class="sxs-lookup"><span data-stu-id="09e9b-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="09e9b-113">Wie die folgende Abbildung zeigt, ist der Fertigungslebenszyklus in drei Phasen unterteilt: *Planen*, *Ausführen* und *Fertigstellen*.</span><span class="sxs-lookup"><span data-stu-id="09e9b-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="09e9b-114">[![Phasen der Fertigungsausführung bei Verwendung einer einzigen Umgebung](media/mes-phases.png "Phasen der Fertigungsausführung bei Verwendung einer einzigen Umgebung")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="09e9b-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="09e9b-115">Die Phase _Planen_ umfasst Produktdefinition, Planung, Auftragserstellung und -terminierung sowie Freigabe.</span><span class="sxs-lookup"><span data-stu-id="09e9b-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="09e9b-116">Der Freigabeschritt kennzeichnet den Übergang von der Phase _Planen_ zur Phase _Ausführen_.</span><span class="sxs-lookup"><span data-stu-id="09e9b-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="09e9b-117">Wenn ein Produktionsauftrag freigegeben wird, sind die Produktionsaufträge auf der Produktionsfläche sichtbar und bereit zur Ausführung.</span><span class="sxs-lookup"><span data-stu-id="09e9b-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="09e9b-118">Wenn ein Produktionsauftrag als abgeschlossen markiert wird, wechselt er von der Phase _Ausführen_ in die Phase _Finalisieren_.</span><span class="sxs-lookup"><span data-stu-id="09e9b-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="09e9b-119">In der Phase _Finalisieren_ durchlaufen die Registrierungen aus der Phase *Ausführen* einen Workflow zur Genehmigung, wo sie berechnet, genehmigt und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="09e9b-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="09e9b-120">An diesem Punkt ist der Produktionsauftrag abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-120">At that point, the production order is completed.</span></span> <span data-ttu-id="09e9b-121">Damit ist die Grundlage für die Entlohnung der Arbeitskräfte geschaffen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="09e9b-122">Aufteilung der Phase „Ausführen“ in eine separate Arbeitsauslastung</span><span class="sxs-lookup"><span data-stu-id="09e9b-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="09e9b-123">Wie die folgende Abbildung zeigt, wird bei Verwendung von Scale-Units die Phase _Ausführen_ als separate Arbeitsauslastung aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="09e9b-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="09e9b-124">[![Ausführungsphasen, wenn Scale-Units verwendet werden](media/mes-phases-workloads.png "Fertigungsausführungsphasen bei Verwendung von Scale-Units")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="09e9b-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="09e9b-125">Das Modell geht nun von einer Einzelinstanz-Installation zu einem Modell über, das auf dem Hub und Scale-Units basiert.</span><span class="sxs-lookup"><span data-stu-id="09e9b-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="09e9b-126">Die Phasen _Planen_ und _Finalisieren_ laufen als Back-Office-Operationen auf dem Hub, und die Arbeitsauslastung der Fertigungsausführung läuft auf den Scale-Units.</span><span class="sxs-lookup"><span data-stu-id="09e9b-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="09e9b-127">Die Daten werden asynchron zwischen dem Hub und den Scale-Units übertragen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="09e9b-128">Wenn ein Produktionsauftrag auf dem Hub freigegeben wird, werden alle Daten, die zur Verarbeitung von Produktionsaufträgen erforderlich sind, an die Scale-Unit übertragen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="09e9b-129">Zu diesen Daten gehören Produktionsaufträge, Arbeitspläne, Stücklisten und Produkte.</span><span class="sxs-lookup"><span data-stu-id="09e9b-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="09e9b-130">Daten, die sich nicht auf einen Produktionsauftrag beziehen (z. B. indirekte Aktivitäten, Abwesenheitscodes und Produktionsparameter), werden ebenfalls vom Hub an die Scale-Unit übertragen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="09e9b-131">In der Regel können Daten, die aus dem Hub stammen und an die Scale-Unit übertragen werden, nur im Hub erstellt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="09e9b-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="09e9b-132">Zum Beispiel kann ein neuer Abwesenheitscode oder eine indirekte Aktivität nicht auf der Scale-Unit erstellt werden – sie können nur für die Registrierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09e9b-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="09e9b-133">Die Registrierungen, die während der Ausführung auf der Scale-Unit vorgenommen werden, werden dann an den Hub übertragen, wo die Zeit- und Anwesenheitsgenehmigung, der Bestand und die finanziellen Aktualisierungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="09e9b-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="09e9b-134">Manufacturing Execution Tasks, die auf Arbeitsauslastungen ausgeführt werden können</span><span class="sxs-lookup"><span data-stu-id="09e9b-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="09e9b-135">Die folgenden Manufacturing Execution Tasks können derzeit auf Arbeitsauslastungen ausgeführt werden, wenn Scale-Units verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="09e9b-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="09e9b-136">Einbuchung, Anmeldung, Ausbuchung und Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="09e9b-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="09e9b-137">Einzelvorgang starten</span><span class="sxs-lookup"><span data-stu-id="09e9b-137">Start job</span></span>
- <span data-ttu-id="09e9b-138">Aufträge bündeln</span><span class="sxs-lookup"><span data-stu-id="09e9b-138">Bundle jobs</span></span>
- <span data-ttu-id="09e9b-139">Fortschritt melden</span><span class="sxs-lookup"><span data-stu-id="09e9b-139">Report progress</span></span>
- <span data-ttu-id="09e9b-140">Ausschuss melden</span><span class="sxs-lookup"><span data-stu-id="09e9b-140">Report scrap</span></span>
- <span data-ttu-id="09e9b-141">Indirekte Aktivität</span><span class="sxs-lookup"><span data-stu-id="09e9b-141">Indirect activity</span></span>
- <span data-ttu-id="09e9b-142">Pause</span><span class="sxs-lookup"><span data-stu-id="09e9b-142">Break</span></span>
- <span data-ttu-id="09e9b-143">Fertig melden und einlagern (erfordert, dass Sie auch den Workload für die Lagerausführung auf Ihrer Skalierungseinheit ausführen, siehe auch [Fertig melden und auf einer Skalierungseinheit einlagern](#RAF))</span><span class="sxs-lookup"><span data-stu-id="09e9b-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="09e9b-144">Arbeiten mit Arbeitsauslastungen zur Fertigungsausführung auf dem Hub</span><span class="sxs-lookup"><span data-stu-id="09e9b-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="09e9b-145">Normalerweise laufen die Prozesse, die für die Ausführung von Arbeitsauslastungen in der Fertigungsausführung erforderlich sind, automatisch, um den Hub und alle Scale-Units bei Bedarf synchron zu halten.</span><span class="sxs-lookup"><span data-stu-id="09e9b-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="09e9b-146">Wenn Sie jedoch Probleme haben, können Sie die Verarbeitung von Rohregistrierungen, die von Arbeitsauslastungen empfangen werden, manuell auslösen und/oder das Protokoll der Registrierungsverarbeitung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="09e9b-147">Manuelles Verarbeiten von Rohregistrierungen</span><span class="sxs-lookup"><span data-stu-id="09e9b-147">Manually process raw registrations</span></span>

<span data-ttu-id="09e9b-148">Ein Batch-Job im Supply Chain Management läuft automatisch, um alle Registrierungen zu verarbeiten, die von den Arbeitsauslastungen empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="09e9b-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="09e9b-149">Dieser Job erstellt die erforderlichen Produktionserfassungen und Logbucheinträge, wenn eine Registrierung für einen abgeschlossenen Auftrag in der Arbeitsauslastung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="09e9b-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="09e9b-150">Obwohl der Job normalerweise automatisch läuft, können Sie ihn jederzeit manuell ausführen, indem Sie sich am Hub anmelden und zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice-Arbeitsauslastung \> Rohregistrierungen verarbeiten** gehen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="09e9b-151">Prüfen Sie das Verarbeitungsprotokoll für Rohregistrierungen</span><span class="sxs-lookup"><span data-stu-id="09e9b-151">Check the raw registration processing log</span></span>

<span data-ttu-id="09e9b-152">Um das Protokoll der Registrierungsverarbeitung zu überprüfen, melden Sie sich beim Hub an und gehen Sie zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice Arbeitsauslastung \> Rohregistrierungsverarbeitungsprotokoll**.</span><span class="sxs-lookup"><span data-stu-id="09e9b-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="09e9b-153">Die Seite **Rohregistrierungs-Verarbeitungsprotokoll** zeigt eine Liste der verarbeiteten Rohregistrierungen und den Status der einzelnen Registrierungen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="09e9b-154">![Rohregistrierungs-Verarbeitungsprotokoll-Seite](media/mes-processing-log.png "Rohregistrierungs-Verarbeitungsprotokollseite")</span><span class="sxs-lookup"><span data-stu-id="09e9b-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="09e9b-155">Sie können jede Registrierung in der Liste bearbeiten, indem Sie sie auswählen und dann eine der folgenden Schaltflächen im Aktivitätsbereich wählen:</span><span class="sxs-lookup"><span data-stu-id="09e9b-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="09e9b-156">**Bearbeiten** - Manuelles Bearbeiten der ausgewählten Registrierung.</span><span class="sxs-lookup"><span data-stu-id="09e9b-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="09e9b-157">Diese Aktion kann nützlich sein, wenn der Job _Rohregistrierungen verarbeiten_ nicht gelaufen ist oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="09e9b-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="09e9b-158">**Abbrechen** - Bricht die ausgewählte Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="09e9b-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="09e9b-159">Arbeiten mit Arbeitsauslastungen der Fertigungsausführung auf einer Scale-Unit</span><span class="sxs-lookup"><span data-stu-id="09e9b-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="09e9b-160">Normalerweise laufen die Prozesse, die für die Ausführung von Arbeitsauslastungen in der Fertigungsausführung erforderlich sind, automatisch, um den Hub und alle Scale-Units bei Bedarf synchron zu halten.</span><span class="sxs-lookup"><span data-stu-id="09e9b-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="09e9b-161">Wenn Sie jedoch Probleme haben, können Sie den Verlauf der Aufträge prüfen, die auf einer Scale-Unit verarbeitet wurden, oder den Auftrag _Manufacturing Hub to Scale-Unit message processor_ manuell ausführen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="09e9b-162">Prüfen der Historie von Fertigungsaufträgen, die auf einer Scale-Unit verarbeitet wurden</span><span class="sxs-lookup"><span data-stu-id="09e9b-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="09e9b-163">Um die Historie der Fertigungsaufträge einzusehen, die auf einer Scale-Unit verarbeitet wurden, melden Sie sich an der Scale-Unit-Maschine an und gehen Sie zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice-Arbeitsauslastung \> Historie der Verarbeitung von Fertigungsaufträgen**.</span><span class="sxs-lookup"><span data-stu-id="09e9b-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="09e9b-164">Die Seite **Verarbeitungshistorie von Fertigungsaufträgen** zeigt die Verarbeitungshistorie der Produktionsaufträge auf der Scale-Unit.</span><span class="sxs-lookup"><span data-stu-id="09e9b-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="09e9b-165">Sie können jeden Produktionsauftrag in der Liste bearbeiten, indem Sie ihn auswählen und dann eine der folgenden Schaltflächen im Aktivitätsbereich wählen:</span><span class="sxs-lookup"><span data-stu-id="09e9b-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="09e9b-166">**Bearbeiten** - Den ausgewählten Produktionsauftrag manuell bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="09e9b-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="09e9b-167">**Abbrechen** - Den ausgewählten Produktionsauftrag abbrechen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="09e9b-168">Fertigungs-Hub zu Scale-Unit Nachrichtenprozessorauftrag</span><span class="sxs-lookup"><span data-stu-id="09e9b-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="09e9b-169">Der Job _Manufacturing hub to scale unit message processor_ verarbeitet Daten vom Hub zur Scale-Unit.</span><span class="sxs-lookup"><span data-stu-id="09e9b-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="09e9b-170">Dieser Job wird automatisch gestartet, wenn die Arbeitsauslastung der Fertigungsausführung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="09e9b-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="09e9b-171">Sie können ihn jedoch jederzeit manuell ausführen, indem Sie zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice-Arbeitsauslastung \> Manufacturing Hub to Scale-Unit Message Processor** gehen.</span><span class="sxs-lookup"><span data-stu-id="09e9b-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="09e9b-172">Fertig melden und auf einer Skalierungseinheit einlagern</span><span class="sxs-lookup"><span data-stu-id="09e9b-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="09e9b-173">Im aktuellen Release werden Vorgänge zum Fertig melden und einlagern (für Fertig-, Co- und Nebenprodukte) vom [Workload für die Lagerausführung](cloud-edge-workload-warehousing.md) unterstützt (nicht der Workload für die Fertigungsausführung).</span><span class="sxs-lookup"><span data-stu-id="09e9b-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="09e9b-174">Um diese Funktionalität bei der Verbindung mit einer Skalierungseinheit zu verwenden, müssen Sie daher Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="09e9b-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="09e9b-175">Installieren Sie sowohl den Workload für die Lagerausführungs als auch für die Fertigungsausführung auf Ihrer Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="09e9b-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="09e9b-176">Verwenden Sie die Mobile Warehouse Management-App, um den Abschluss zu melden und die Einlagerungsarbeiten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="09e9b-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="09e9b-177">Die Produktionsausführungsoberfläche unterstützt diese Prozesse derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="09e9b-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
