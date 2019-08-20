---
title: Wartungsanfrage-Lebenszyklusstatus
description: In diesem Thema wird beschrieben, wie Wartungsanfrage-Lebenszyklusstatus in Asset Management eingerichtet werden.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f68e11a1cd14bc35282b957a4262cbecdd627b3b
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790498"
---
# <a name="maintenance-request-states"></a><span data-ttu-id="cabf1-103">Wartungsanfrage-Lebenszyklusstatus</span><span class="sxs-lookup"><span data-stu-id="cabf1-103">Maintenance request states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="cabf1-104">Wartungsanfrage-Lebenszyklusstatus definieren die Phasen, die eine Anfrage durchlaufen kann.</span><span class="sxs-lookup"><span data-stu-id="cabf1-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="cabf1-105">Hierzu gehören **Erstellt**, **Aktiv** und **Beendet**.</span><span class="sxs-lookup"><span data-stu-id="cabf1-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="cabf1-106">Wenn eine Wartungsanfrage in einen Arbeitsauftrag konvertiert wird, sollte der Wartungsanfrage-Lebenszyklusstatus in **Beendet** oder **Geschlossen** aktualisiert werden, um anzugeben, dass die Wartungsanfrage nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cabf1-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="cabf1-107">Auf der Listenseite **Alle Wartungsanfragen** sehen Sie alle Wartungsanfragen unabhängig von ihrem Lebenszyklusstatus.</span><span class="sxs-lookup"><span data-stu-id="cabf1-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="cabf1-108">Wartungsanfrage-Lebenszyklusstatus einrichten</span><span class="sxs-lookup"><span data-stu-id="cabf1-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="cabf1-109">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Lebenszyklusstatus** aus.</span><span class="sxs-lookup"><span data-stu-id="cabf1-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="cabf1-110">Wählen Sie **Neu** aus, um einen Wartungsanfrage-Lebenszyklusstatus zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cabf1-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="cabf1-111">Geben Sie im Feld **Lebenszyklusstatus** eine Kennung für den Lebenszyklusstatus ein.</span><span class="sxs-lookup"><span data-stu-id="cabf1-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="cabf1-112">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="cabf1-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="cabf1-113">Auf dem Inforegister **Details** wird im Feld **Lebenszyklusmodelle** die Anzahl von Wartungsanfrage-Lebenszyklusmodellen angezeigt, die diesen Lebenszyklusstatus verwenden.</span><span class="sxs-lookup"><span data-stu-id="cabf1-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="cabf1-114">Legen Sie auf dem Inforegister **Allgemein** die Option **Aktiv** auf **Ja** fest, wenn eine Wartungsanfrage aktiv sein soll, während sie diesen Lebenszyklusstatus hat.</span><span class="sxs-lookup"><span data-stu-id="cabf1-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="cabf1-115">Legen Sie die Option **Tatsächliches Ende festlegen** auf **Ja** fest, wenn automatisch ein tatsächliches Enddatum und eine Uhrzeit für eine Wartungsanfrage eingegeben werden sollen, die diesen Lebenszyklusstatus hat.</span><span class="sxs-lookup"><span data-stu-id="cabf1-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="cabf1-116">Legen Sie die Option **Arbeitsauftrag erstellen** auf **Ja** fest, wenn ein Arbeitsauftrag aus einer Wartungsanfrage erstellt werden kann, die diesen Lebenszyklusstatus hat.</span><span class="sxs-lookup"><span data-stu-id="cabf1-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="cabf1-117">Legen Sie die Option **Löschen** auf **Ja** fest, wenn eine Wartungsanfrage gelöscht werden kann, während sie diesen Lebenszyklusstatus hat.</span><span class="sxs-lookup"><span data-stu-id="cabf1-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="cabf1-118">Auf dem Inforegister **Aktualisieren** sind die Optionen **Zugang** und **Abgang** im Abschnitt **Anlage** relevant, wenn Sie die Depotreparatur verwenden. Legen Sie die entsprechende Option auf **Ja** fest, wenn der Anlagenlebenszyklusstatus von Anlagen, die in einer Wartungsanfrage ausgewählt werden, automatisch in **Zugang** oder **Abgang** aktualisiert werden soll, wenn der Wartungsanfrage-Lebenszyklusstatus dieser Wartungsanfrage auf **Zugang** oder **Abgang** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cabf1-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="cabf1-119">Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfrage-Lebenszyklusstatus**.</span><span class="sxs-lookup"><span data-stu-id="cabf1-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Abbildung 1](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="cabf1-121">Wartungsanfrage-Lebenszyklusstatus, -Lebenszyklusstatusgruppen und -typen stehen mit Arbeitsauftrag-Lebenszyklusstatus, -Lebenszyklusstatusgruppen und -typen in Zusammenhang und werden genauso wie diese verwendet.</span><span class="sxs-lookup"><span data-stu-id="cabf1-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="cabf1-122">Wartungsanfrage-Lebenszyklusmodelle einrichten</span><span class="sxs-lookup"><span data-stu-id="cabf1-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="cabf1-123">Nachdem Sie die Lebenszyklusstatus erstellt haben, die für die Wartungsanfragen erforderlich sind, können diese in Lebenszyklusstatusgruppen oder Lebenszyklusmodelle aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="cabf1-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="cabf1-124">Wartungsanfrage-Lebenszyklusmodelle werden verwendet, um den Fluss zu erstellen, der für verschiedene Arten von Wartungsanfragen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cabf1-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="cabf1-125">Es sollte mindestens ein Wartungsanfrage-Lebenszyklusmodell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cabf1-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="cabf1-126">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Lebenszyklusmodelle** aus.</span><span class="sxs-lookup"><span data-stu-id="cabf1-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="cabf1-127">Wählen Sie **Neu** aus, um ein Wartungsanfrage-Lebenszyklusmodell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cabf1-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="cabf1-128">Geben Sie im Feld **Lebenszyklusmodell** eine Kennung für das Lebenszyklusmodell ein.</span><span class="sxs-lookup"><span data-stu-id="cabf1-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="cabf1-129">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="cabf1-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="cabf1-130">Auf dem Inforegister **Details** wird im Feld **Lebenszyklusstatus** die Anzahl von Lebenszyklusstatus angezeigt, die in diesem Lebenszyklusmodel ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="cabf1-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="cabf1-131">Im Feld **Wartungsanfragentypen** wird die Anzahl der Wartungsanfragentypen angezeigt, die dieses Lebenszyklusmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="cabf1-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="cabf1-132">Wählen Sie auf dem Inforegister **Lebenszyklusstatus** die Lebenszyklusstatus aus, die in das Lebenszyklusmodell einbezogen werden sollen:</span><span class="sxs-lookup"><span data-stu-id="cabf1-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="cabf1-133">Um einen Lebenszyklusstatus in das Lebenszyklusmodell einzuschließen, wählen Sie ihn im Bereich **Verbleibende Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts ![Nach-Rechts-Pfeil](media/03-setup-for-requests.png), um ihn in den Bereich **Ausgewählte Lebenszyklusstatus** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="cabf1-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="cabf1-134">Um alle verfügbaren Lebenszyklusstatus in das Lebenszyklusmodell einzuschließen, wählen Sie die Schaltfläche **Alle verfügbaren Status auswählen** ![Alle verfügbaren Status auswählen](media/04-setup-for-requests.png) aus.</span><span class="sxs-lookup"><span data-stu-id="cabf1-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="cabf1-135">Alle Lebenszyklusstatus werden in den Bereich **Ausgewählte Lebenszyklusstatus** verschoben.</span><span class="sxs-lookup"><span data-stu-id="cabf1-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="cabf1-136">Um einen Lebenszyklusstatus aus dem Lebenszyklusmodell zu entfernen, wählen Sie ihn im Bereich **Ausgewählte Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach links ![Nach-Links-Pfeil](media/05-setup-for-requests.png), um ihn in den Bereich **Verbleibende Lebenszyklusstatus** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="cabf1-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="cabf1-137">Auf dem Inforegister **Allgemein** sind die Felder im Abschnitt **Aktualisierungen** relevant, wenn Sie die Depotreparatur verwenden.</span><span class="sxs-lookup"><span data-stu-id="cabf1-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="cabf1-138">Wählen Sie im Feld **Lebenszyklusstatus bei Anlagenzugang** den Anlagenlebenszyklusstatus aus, auf den Anlagen, die in einer Wartungsanfrage ausgewählt werden, automatisch aktualisiert werden sollen, wenn sie zur Depotreparatur eingehen.</span><span class="sxs-lookup"><span data-stu-id="cabf1-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="cabf1-139">Wählen Sie im Feld **Lebenszyklusstatus bei Anlagenauslieferung** den Lebenszyklusstatus aus, auf den Anlagen, die in einer Wartungsanfrage ausgewählt werden, automatisch aktualisiert werden sollen, wenn sie nach der Reparatur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cabf1-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="cabf1-140">Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfrage-Lebenszyklusmodelle**.</span><span class="sxs-lookup"><span data-stu-id="cabf1-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Abbildung 2](media/06-setup-for-requests.png)
