---
title: Erstellen von Arbeitsaufträgen
description: In diesem Thema wird erläutert, wie Sie Arbeitsaufträge in der Anlagenverwaltung erstellen.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 76306fb31e7e5297e6a5d64b97b5bd09b64349ee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500573"
---
# <a name="creating-work-orders"></a><span data-ttu-id="76d5a-103">Erstellen von Arbeitsaufträgen</span><span class="sxs-lookup"><span data-stu-id="76d5a-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76d5a-104">Nachdem Sie vorbeugende Wartungsaufträge geplant haben, ist der nächste Schritt, Arbeitsaufträge für diese zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="76d5a-105">Sie können diesen Schritt mithilfe eines der Wartungszeitpläne ausführen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="76d5a-106">Die geplanten Einzelvorgänge in einem Wartungszeitplan können verschiedene Referenztypen haben, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76d5a-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="76d5a-107">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="76d5a-107">Reference type</span></span> | <span data-ttu-id="76d5a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76d5a-108">Description</span></span> |
|---|---|
| <span data-ttu-id="76d5a-109">Wartungspläne</span><span class="sxs-lookup"><span data-stu-id="76d5a-109">Maintenance plans</span></span> | <span data-ttu-id="76d5a-110">Vorbeugende Wartungsaufträge auf Grundlage der Wartungsplantypen *Zeit* oder *Zähler*.</span><span class="sxs-lookup"><span data-stu-id="76d5a-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="76d5a-111">Wartungsdurchgänge</span><span class="sxs-lookup"><span data-stu-id="76d5a-111">Maintenance rounds</span></span> | <span data-ttu-id="76d5a-112">Vorbeugende Wartungsaufträge, die mehrere Anlagen enthalten, die einen ähnlichen Wartungstyp erfordern.</span><span class="sxs-lookup"><span data-stu-id="76d5a-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="76d5a-113">Wartungsanfrage</span><span class="sxs-lookup"><span data-stu-id="76d5a-113">Maintenance request</span></span> | <span data-ttu-id="76d5a-114">Eine manuell erstellte Anforderung zur Wartung oder Reparatur einer Anlage.</span><span class="sxs-lookup"><span data-stu-id="76d5a-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="76d5a-115">Diese Anforderung kann in einen Arbeitsauftrag konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="76d5a-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="76d5a-116">Erstellen von Arbeitsaufträgen basierend auf Ihrem Wartungsplan</span><span class="sxs-lookup"><span data-stu-id="76d5a-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="76d5a-117">Führen Sie die folgenden Schritte aus, um Arbeitsaufträge zu erstellen, die auf Ihrem Wartungsplan basieren.</span><span class="sxs-lookup"><span data-stu-id="76d5a-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="76d5a-118">Öffnen Sie eine der folgenden Seiten, je nachdem, wie Sie Zeitplanelemente für Ihre Arbeitsaufträge auswählen möchten:</span><span class="sxs-lookup"><span data-stu-id="76d5a-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="76d5a-119">Alle Wartungszeitpläne (**Anlagenerwaltung \> Verwaltungszeitplan \> Alle Wartungszeitpläne**)</span><span class="sxs-lookup"><span data-stu-id="76d5a-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="76d5a-120">Offene Wartungszeitplanpositionen (**Anlagenerwaltung \> Verwaltungszeitplan \> Offene Wartungszeitplanpositionen**)</span><span class="sxs-lookup"><span data-stu-id="76d5a-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="76d5a-121">Offene Wartungszeitplanpools (**Anlagenerwaltung \> Verwaltungszeitplan \> Offene Wartungszeitplanpools**)</span><span class="sxs-lookup"><span data-stu-id="76d5a-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="76d5a-122">Aktivieren Sie im Raster das Kontrollkästchen für jeden geplanten Wartungsauftrag, für den Sie einen Arbeitsauftrag erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="76d5a-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="76d5a-123">Wählen Sie im Aktionsbereich **Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="76d5a-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="76d5a-124">Das Dialogfeld **Arbeitsaufträge erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76d5a-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="76d5a-125">Die Gesamtanzahl von Planungsstunden für die ausgewählten Positionen wird im Feld **Wartungsprognosestunden** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76d5a-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Das Dialogfeld „Arbeitsaufträge erstellen“](media/18-preventive-maintenance.png)

1. <span data-ttu-id="76d5a-127">Im Abschnitt **Parameter** geben Sie die Anzahl der Arbeitsaufträge an, die erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="76d5a-128">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="76d5a-128">Select one of the following options:</span></span>

    - <span data-ttu-id="76d5a-129">**Ein Arbeitsauftrag pro Position** – Erstellen Sie einen Arbeitsauftrag pro Wartungszeitplanposition.</span><span class="sxs-lookup"><span data-stu-id="76d5a-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="76d5a-130">**Ein Arbeitsauftrag pro** – Erstellen Sie Arbeitsaufträge, die gemäß den Einstellungen der anderen Optionen gruppiert sind, die verfügbar werden, wenn Sie diese Option auswählen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="76d5a-131">In dem Feld **Arbeitsauftragstyp** wählen Sie den Arbeitsauftragstyp aus, der für alle von Ihnen erstellten Arbeitsaufträge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d5a-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="76d5a-132">Wählen Sie **OK** aus, um die Arbeitsaufträge gemäß Ihren Einstellungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="76d5a-133">Gruppieren Sie Arbeitsauftragspositionen, die automatisch erstellt werden, während ein Wartungszeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76d5a-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="76d5a-134">Mit dieser Funktion können Sie Regeln für die Gruppierung von Arbeitsauftragspositionen unter einem einzelnen Arbeitsauftrag definieren, wenn das System so eingerichtet ist, dass Arbeitsaufträge basierend auf einem Wartungszeitplan automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="76d5a-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="76d5a-135">Bisher konnten automatisch generierte Arbeitsaufträge nur eine Position enthalten.</span><span class="sxs-lookup"><span data-stu-id="76d5a-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="76d5a-136">Sie können Arbeitsaufträge jetzt jedoch beispielsweise nach Anlage, Anlagentyp oder funktionalem Standort gruppieren.</span><span class="sxs-lookup"><span data-stu-id="76d5a-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="76d5a-137">(Manuell erstellte Arbeitsaufträge können bereits auf diese Weise gruppiert werden, wie im vorherigen Abschnitt dieses Themas beschrieben.)</span><span class="sxs-lookup"><span data-stu-id="76d5a-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="76d5a-138">Aktivieren der Gruppierung für automatisch generierte Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="76d5a-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="76d5a-139">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="76d5a-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="76d5a-140">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="76d5a-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="76d5a-141">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="76d5a-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="76d5a-142">**Modul:** *Anlagenverwaltung*</span><span class="sxs-lookup"><span data-stu-id="76d5a-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="76d5a-143">**Funktionsname:** *Regeln zum Gruppieren von Arbeitsaufträgen während der Ausführung eines Wartungsplans anwenden*</span><span class="sxs-lookup"><span data-stu-id="76d5a-143">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="76d5a-144">Einrichten der Gruppierung für automatisch generierte Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="76d5a-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="76d5a-145">Um die Gruppierung für automatisch generierte Arbeitsaufträge einzurichten, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="76d5a-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="76d5a-146">Wechseln Sie zu **Anlagenverwaltung \> Einrichtung \> Vorbeugende Wartung \> Wartungszeitpläne**.</span><span class="sxs-lookup"><span data-stu-id="76d5a-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="76d5a-147">Führen Sie für jeden Plan, in dem Sie gruppierte Arbeitsaufträge generieren möchten, die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="76d5a-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="76d5a-148">Wählen Sie im Listenbereich den Plan aus.</span><span class="sxs-lookup"><span data-stu-id="76d5a-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="76d5a-149">Auf dem Inforegister **Positionen** stellen Sie sicher, dass das Kontrollkästchen **Automatisch einrichten** in jeder Position aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76d5a-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="76d5a-150">Wechseln Sie zu **Anlagenverwaltung \> Periodisch \> Vorbeugende Wartung \> Wartungspläne terminieren**.</span><span class="sxs-lookup"><span data-stu-id="76d5a-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="76d5a-151">In dem Dialogfeld **Wartungspläne terminieren** im Abschnitt **Periode** geben Sie den Zeithorizont für den Plan an (wie weit Sie nach vorne schauen müssen, wenn Sie geplante Wartungszeitpläne finden, für die Arbeit generiert werden soll).</span><span class="sxs-lookup"><span data-stu-id="76d5a-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="76d5a-152">Stellen Sie Option **Arbeitsauftrag automatisch aus Zeitplan erstellen** auf *Ja*.</span><span class="sxs-lookup"><span data-stu-id="76d5a-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="76d5a-153">Wählen Sie im Abschnitt **Arbeitsauftrag** eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="76d5a-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="76d5a-154">**Ein Arbeitsauftrag pro Position** – Erstellen Sie einen Arbeitsauftrag pro Wartungszeitplanposition.</span><span class="sxs-lookup"><span data-stu-id="76d5a-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="76d5a-155">(Diese Option bietet die gleiche Funktionalität, die verfügbar ist, wenn die Funktion *Regeln zum Gruppieren von Arbeitsaufträgen während der Ausführung eines Wartungsplans anwenden* ausgeschaltet ist.)</span><span class="sxs-lookup"><span data-stu-id="76d5a-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="76d5a-156">**Ein Arbeitsauftrag pro** – Erstellen Sie Arbeitsaufträge, die gemäß den Einstellungen der anderen Optionen gruppiert sind, die verfügbar werden, wenn Sie diese Option auswählen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="76d5a-157">Wenn Sie möchten, dass die Optionen angewendet werden, wenn Sie nur einige Ihrer Wartungspläne ausführen, klicken Sie auf das Inforegister **Einzuschließende Datensätze**, fügen Sie Filter nach Bedarf hinzu, genau wie bei anderen Stapelverarbeitungsaufträgen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="76d5a-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="76d5a-158">Richten Sie auf dem Inforegister **Im Hintergrund ausführen** Stapel- und Planungsoptionen nach Bedarf ein, genau wie bei anderen Stapelverarbeitungsaufträgen in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="76d5a-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="76d5a-159">Wählen **OK**, um die ausgewählten Wartungszeitpläne auszuführen und/oder zu planen.</span><span class="sxs-lookup"><span data-stu-id="76d5a-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]