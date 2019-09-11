---
title: Arbeitsauftragspools
description: In diesem Thema wird beschrieben, wie Sie mit Arbeitsauftragspools im Anlagenmanagement arbeiten.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875673"
---
# <a name="work-order-pools"></a><span data-ttu-id="1357d-103">Arbeitsauftragspools</span><span class="sxs-lookup"><span data-stu-id="1357d-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="1357d-104">Mit Hilfe von Arbeitsauftragspools können Sie Arbeitsaufträge gruppieren, die etwas gemeinsam haben.</span><span class="sxs-lookup"><span data-stu-id="1357d-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="1357d-105">Sie können z.B. Arbeitsauftragspools anlegen für</span><span class="sxs-lookup"><span data-stu-id="1357d-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="1357d-106">Arbeitsteams, z.B. Wartungspersonal A, Wartungspersonal B</span><span class="sxs-lookup"><span data-stu-id="1357d-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="1357d-107">Fachkenntnisse, z.B. Elektriker oder Installateure</span><span class="sxs-lookup"><span data-stu-id="1357d-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="1357d-108">physische Standorte</span><span class="sxs-lookup"><span data-stu-id="1357d-108">physical locations</span></span>  

- <span data-ttu-id="1357d-109">Zeitpläne, z.B. Wochen oder andere Zeiträume</span><span class="sxs-lookup"><span data-stu-id="1357d-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="1357d-110">Bei Bedarf kann ein Arbeitsauftrag in mehreren Arbeitsauftragspools platziert werden.</span><span class="sxs-lookup"><span data-stu-id="1357d-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="1357d-111">Arbeitsauftragspool anlegen</span><span class="sxs-lookup"><span data-stu-id="1357d-111">Create work order pool</span></span>

<span data-ttu-id="1357d-112">Unter **Alle Auftragspools** oder **Aktive Auftragspools** können Sie sich einen Überblick über Ihre Auftragspools verschaffen und neue Pools anlegen.</span><span class="sxs-lookup"><span data-stu-id="1357d-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="1357d-113">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsauftragspools** > **Alle Auftragspools** oder **Aktive Auftragspools**.</span><span class="sxs-lookup"><span data-stu-id="1357d-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="1357d-114">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="1357d-114">Click **New**.</span></span>

3. <span data-ttu-id="1357d-115">Geben Sie in das Feld **Pool** eine Arbeitsauftragspool-ID und in das Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="1357d-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="1357d-116">Wählen Sie „Ja“ auf der Umschalttaste **Aktiv**, um anzuzeigen, dass der Arbeitsauftragspool aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="1357d-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="1357d-117">Wählen Sie „Ja“ auf der Schaltfläche **Arbeitsauftragsbeziehungen löschen**Umschalten, wenn Sie möchten, dass Arbeitsaufträge automatisch aus dem Arbeitsauftragspool entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1357d-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="1357d-118">Wählen Sie im Feld **Lebenszykluszustand löschen** den Lebenszykluszustand des Arbeitsauftrags aus.</span><span class="sxs-lookup"><span data-stu-id="1357d-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="1357d-119">So könnte beispielsweise der Lebenszykluszustand des Arbeitsauftrags für die Fertigstellung eines Arbeitsauftrags so eingestellt werden, dass er automatisch Beziehungen zu Arbeitsauftragspools löscht.</span><span class="sxs-lookup"><span data-stu-id="1357d-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="1357d-120">Sie können sofort mit dem Hinzufügen von Arbeitsaufträgen zu Ihrem Arbeitsauftragspool beginnen.</span><span class="sxs-lookup"><span data-stu-id="1357d-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="1357d-121">Klicken Sie auf der Seite **Arbeitsaufträge** FastTab auf **Zeile hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1357d-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="1357d-122">Wählen Sie einen Arbeitsauftrag im Feld **Arbeitsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="1357d-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="1357d-123">Die Bezugsfelder werden automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1357d-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="1357d-124">Wiederholen Sie die Schritte 7-8, wenn Sie weitere Arbeitsaufträge hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="1357d-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="1357d-125">Im Feld **Sortierreihenfolge** können Sie angeben, ob die Arbeitsaufträge in einer bestimmten Reihenfolge ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1357d-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="1357d-126">Fügen Sie die Nummern 1, 2, 3 usw. ein, um eine bestimmte Reihenfolge für die ausgewählten Arbeitsaufträge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1357d-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="1357d-127">Klicken Sie auf die Schaltfläche **Arbeitsaufträge**, um eine Liste aller im Arbeitsauftragspool enthaltenen Arbeitsaufträge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1357d-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="1357d-128">Klicken Sie auf die Schaltfläche **Kapazitätsbelastung**, um **Kapazitätsbelastung** zu öffnen, um die Kapazitätsbelastung für Wartungsplan, nicht geplante Arbeitsaufträge und geplante Arbeitsaufträge zu berechnen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1357d-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="1357d-129">Klicken Sie auf die Schaltfläche **Artikelprognose**, um **Artikelprognose** zu öffnen, um Prognosen für Artikel (Ersatzteile und andere benötigte Artikel) zu berechnen und anzuzeigen, die sich auf Wartungspläne, nicht geplante Arbeitsaufträge und geplante Arbeitsaufträge beziehen.</span><span class="sxs-lookup"><span data-stu-id="1357d-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="1357d-130">Klicken Sie auf die Schaltfläche **Bestellanforderung Arbeitsauftrag**, um die Liste **Bestellanforderung Arbeitsauftrag** zu öffnen, um eine Liste der Bestellanforderungen zu sehen, die sich auf die Arbeitsaufträge im Arbeitsauftragspool beziehen.</span><span class="sxs-lookup"><span data-stu-id="1357d-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="1357d-131">Klicken Sie auf die Schaltfläche **Arbeitsauftragsbestellung**, um die Liste **Arbeitsauftragsbestellung** zu öffnen und eine Liste der Bestellungen zu sehen, die sich auf die Arbeitsaufträge im Arbeitsauftragspool beziehen.</span><span class="sxs-lookup"><span data-stu-id="1357d-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="1357d-132">Wenn ein Arbeitsauftragspool für Ihre Arbeitsvorbereitung nicht mehr relevant ist, setzen Sie das Kontrollkästchen **Aktiv** für diesen Pool in der Listenansicht **Auftragspool** auf „Nein“.</span><span class="sxs-lookup"><span data-stu-id="1357d-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="1357d-133">Aktivieren Sie das Kontrollkästchen **Arbeitsauftragsbeziehungen löschen**, wenn Sie alle Arbeitsauftragszeilen löschen möchten, z.B. um einen leeren Pool zu erstellen, den Sie später für andere Arbeitsaufträge verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1357d-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="1357d-134">Denken Sie daran, das Kontrollkästchen **Arbeitsauftragsbeziehungen löschen** zu deaktivieren, wenn Sie den Arbeitsauftragspool zum späteren Anlegen neuer Arbeitsauftragsbeziehungen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="1357d-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Abbildung 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="1357d-136">Arbeitsauftrag zu einem Arbeitsauftragspool hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1357d-136">Add work order to a work order pool</span></span>

<span data-ttu-id="1357d-137">Wie im obigen Abschnitt beschrieben, können Sie beim Anlegen des Vorrats Arbeitsaufträge zu einem Arbeitsauftragspool hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1357d-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="1357d-138">Sie können einen Arbeitsauftrag auch aus einer der Listen **Alle Arbeitsaufträge** zu einem Arbeitsauftragspool hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1357d-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="1357d-139">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="1357d-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1357d-140">Wählen Sie den Arbeitsauftrag in der Liste aus und klicken Sie auf **Arbeitsauftragspool**.</span><span class="sxs-lookup"><span data-stu-id="1357d-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="1357d-141">Wählen Sie „Hinzufügen“ im Feld **Hinzufügen/Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="1357d-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="1357d-142">Wählen Sie den Arbeitsauftragspool im Feld **Pool** aus.</span><span class="sxs-lookup"><span data-stu-id="1357d-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="1357d-143">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1357d-143">Click **OK**.</span></span>

6. <span data-ttu-id="1357d-144">Nachdem Sie einen Arbeitsauftrag zu einem Arbeitsauftragspool hinzugefügt haben, wenn Sie den Arbeitsauftrag in einer bestimmten Reihenfolge im Pool platzieren möchten: Öffnen Sie eine der Listenseiten des Arbeitsauftragspools, wählen Sie den Pool aus und klicken Sie auf **Bearbeiten**, und passen Sie die Sortierreihenfolge der im Pool enthaltenen Arbeitsaufträge im Feld **Arbeitsauftragspool**Formular > **Arbeitsaufträge** FastTab > **Sortierauftrag** an.</span><span class="sxs-lookup"><span data-stu-id="1357d-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="1357d-145">Wenn Sie den ausgewählten Arbeitsauftrag aus einem Arbeitsauftragspool entfernen möchten, wählen Sie in Schritt 3 „Entfernen“.</span><span class="sxs-lookup"><span data-stu-id="1357d-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

