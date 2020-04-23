---
title: Anlagenlebenszyklusstatus
description: In diesem Thema werden Anlagenlebenszyklusstatus und Lebenszyklusmodelle in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1752298ce726b904defb1c826a1e2d5014286e1f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216527"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="64e70-103">Anlagenlebenszyklusstatus</span><span class="sxs-lookup"><span data-stu-id="64e70-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="64e70-104">In diesem Thema werden Anlagenlebenszyklusstatus und Lebenszyklusmodelle in Asset Management erläutert.</span><span class="sxs-lookup"><span data-stu-id="64e70-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="64e70-105">Anlagenlebenszyklusstatus werden verwendet, um festzulegen, ob eine Anlage aktiv oder inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="64e70-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="64e70-106">So können Sie zum Beispiel Anlagenlebenszyklusstatus wie **Erstellt**, **Aktiv** und **Ausgeschieden** einrichten.</span><span class="sxs-lookup"><span data-stu-id="64e70-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="64e70-107">Anforderungslebenszyklusstatus sind mit Anlagenlebenszyklusstatus verknüpft.</span><span class="sxs-lookup"><span data-stu-id="64e70-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="64e70-108">Wenn Sie eine Anforderung in einen neuen Anforderungslebenszyklusstatus ändern, wird die Anlage, die der Anforderung zugeordnet ist, in einen neuen Anlagenlebenszyklusstatus geändert.</span><span class="sxs-lookup"><span data-stu-id="64e70-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="64e70-109">Wenn beispielsweise der Lebenszyklusstatus einer Anforderung in **Zugang** geändert wird, wird der Lebenszyklusstaus der zugeordneten Anlage in den Lebenszyklusstatus geändert, der im Feld **Eingehender Lebenszyklusstatus** im Inforegister **Anlagenlebenszyklusstatus** der Seite **Anlagenlebenszyklusstatus-Modelle** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="64e70-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="64e70-110">Anlagenlebenszyklusstatus können in Anlagenlebenszyklusmodellen eingerichtet werden, in denen Sie die erforderlichen Lebenszyklusstatus für unterschiedliche Arten von Anlagen definieren können.</span><span class="sxs-lookup"><span data-stu-id="64e70-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="64e70-111">Sie richten zunächst Lebenszyklusstatus ein.</span><span class="sxs-lookup"><span data-stu-id="64e70-111">You first set up lifecycle states.</span></span> <span data-ttu-id="64e70-112">Dann erstellen Sie ein Lebenszyklusmodell und wählen Lebenszyklusstatus dafür aus.</span><span class="sxs-lookup"><span data-stu-id="64e70-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="64e70-113">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Lebenszyklusstatus** aus.</span><span class="sxs-lookup"><span data-stu-id="64e70-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="64e70-114">Wählen Sie **Neu** aus, um einen neuen Anlagenlebenszyklusstatus zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64e70-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="64e70-115">Geben Sie im Feld **Lebenszyklusstatus** eine Kennung für den Lebenszyklusstatus ein.</span><span class="sxs-lookup"><span data-stu-id="64e70-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="64e70-116">Geben Sie im Feld **Name** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="64e70-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="64e70-117">Das Feld **Lebenszyklusmodelle** zeigt die Anzahl von Anlagenlebenszyklusmodellen an, die diesen Anlagenlebenszyklusstatus verwenden.</span><span class="sxs-lookup"><span data-stu-id="64e70-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="64e70-118">Legen Sie für die Option **Aktiv** den Wert **Ja** fest, wenn dieser Lebenszyklusstatus ein aktiver Lebenszyklusstatus sein soll (das heißt, wenn Arbeitsaufträge für Anlagen erstellt werden können, die in diesem Lebenszyklusstatus sind).</span><span class="sxs-lookup"><span data-stu-id="64e70-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="64e70-119">Legen Sie für die Option **Offene Kalenderpositionen löschen** den Wert **Ja** fest, wenn offene Anlagen-Kalenderpositionen, die den Anlagenlebenszyklusstatus **Erstellt** haben, gelöscht werden sollen, wenn sie in diesem Lebenszyklusstatus sind.</span><span class="sxs-lookup"><span data-stu-id="64e70-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="64e70-120">Diese Einstellung ist hilfreich, wenn Sie alle offenen Wartungspläne bereinigen möchten, die nicht mehr für die Anlage relevant sind (die Anlage ist beispielsweise nicht mehr aktiv).</span><span class="sxs-lookup"><span data-stu-id="64e70-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="64e70-121">Anlagenlebenszyklusstatus, Anlagenlebenszyklusmodelle und Anlagentypen stehen in Beziehung.</span><span class="sxs-lookup"><span data-stu-id="64e70-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="64e70-122">Sie werden auf die gleiche Weise wie Arbeitsauftrags-Lebenszyklusstatus, Arbeitsauftrags-Lebenszyklusmodelle und Arbeitsauftragstypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="64e70-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="64e70-123">Nachdem Sie die erforderlichen Anlagenlebenszyklusstatus erstellt haben, können Sie Lebenszyklusstatus in den Anlagenlebenszyklusmodellen einrichten.</span><span class="sxs-lookup"><span data-stu-id="64e70-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="64e70-124">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Lebenszyklusmodelle** aus.</span><span class="sxs-lookup"><span data-stu-id="64e70-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="64e70-125">Wählen Sie **Neu** aus, um ein neues Anlagenlebenszyklusmodell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64e70-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="64e70-126">Geben Sie im Feld **Lebenszyklusmodell** eine Kennung für das Lebenszyklusmodell ein.</span><span class="sxs-lookup"><span data-stu-id="64e70-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="64e70-127">Geben Sie im Feld **Name** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="64e70-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="64e70-128">Das Feld **Lebenszyklusstatus** zeigt die Anzahl der Lebenszyklusstatus an, die im Anlagenlebenszyklusmodell ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="64e70-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="64e70-129">Das Feld **Anlagentypen** zeigt die Anzahl von Anlagentypen an, die im Lebenszyklusmodell verwandt werden.</span><span class="sxs-lookup"><span data-stu-id="64e70-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="64e70-130">Wählen Sie auf dem Inforegister **Lebenszyklusstatus** die Anlagenlebenszyklusstatus aus, die in das Anlagenlebenszyklusmodell einbezogen werden sollen:</span><span class="sxs-lookup"><span data-stu-id="64e70-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="64e70-131">Um einen Lebenszyklusstatus für das Modell zu verwenden, wählen Sie ihn im Bereich **Verbleibende Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts ![Nach-Rechts-Pfeil](media/15-setup-for-objects.png), um ihn in den Bereich **Ausgewählte Lebenszyklusstatus** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="64e70-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="64e70-132">Um alle verfügbaren Lebenszyklusstatus im Modell zu verwenden, wählen Sie die Schaltfläche **Alle verfügbaren Lebenszyklusstatus** ![Alle verfügbaren Lebenszyklusstatus](media/20-setup-for-objects.png) aus.</span><span class="sxs-lookup"><span data-stu-id="64e70-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="64e70-133">Alle Lebenszyklusstatus werden in den Bereich **Ausgewählte Lebenszyklusstatus** verschoben.</span><span class="sxs-lookup"><span data-stu-id="64e70-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="64e70-134">Um einen Lebenszyklusstatus aus dem Modell zu entfernen, wählen Sie ihn im Bereich **Ausgewählte Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach links ![Nach-Links-Pfeil](media/16-setup-for-objects.png), um ihn in den Bereich **Verbleibende Lebenszyklusstatus** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="64e70-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="64e70-135">Wählen Sie **Lebenszyklusstatusaktualisierungen**, um festzulegen, welche Anlagenlebenszyklusstatus einem ausgewählten Lebenszyklusstatus folgen können.</span><span class="sxs-lookup"><span data-stu-id="64e70-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="64e70-136">Verwenden Sie das Inforegister **Anlagenstatus**, wenn Sie Anlagen behandelt, die Sie zwecks Reparatur erhalten.</span><span class="sxs-lookup"><span data-stu-id="64e70-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="64e70-137">Im Abschnitt **Ein-/ausgehend** können Sie Anlagenlebenszyklusstatus auswählen, um den Workflow einer Anlage anzugeben, die Sie zwecks Reparatur erhalten.</span><span class="sxs-lookup"><span data-stu-id="64e70-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="64e70-138">Wenn Sie Kunden oder Abteilungen Anlagenausleihen anbieten, wählen Sie im Abschnitt **Ausleihe** die Lebenszyklusstatus für Anlagenausleihen aus.</span><span class="sxs-lookup"><span data-stu-id="64e70-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
