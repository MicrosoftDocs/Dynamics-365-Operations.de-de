---
title: Arbeitsauftragspools
description: In diesem Thema wird beschrieben, wie Sie mit Arbeitsauftragspools im Anlagenmanagement arbeiten.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626361"
---
# <a name="work-order-pools"></a><span data-ttu-id="e9add-103">Arbeitsauftragspools</span><span class="sxs-lookup"><span data-stu-id="e9add-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="e9add-104">Mit Hilfe von Arbeitsauftragspools können Sie Arbeitsaufträge gruppieren, die etwas gemeinsam haben.</span><span class="sxs-lookup"><span data-stu-id="e9add-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="e9add-105">Nachfolgend finden Sie einige Beispiele von Elementen, die Sie für Arbeitsauftragspools erstellen können:</span><span class="sxs-lookup"><span data-stu-id="e9add-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="e9add-106">Arbeitsteams, z.B. Wartungspersonal A oder Wartungspersonal B</span><span class="sxs-lookup"><span data-stu-id="e9add-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="e9add-107">Fachkenntnisse, z.B. Elektriker oder Installateure</span><span class="sxs-lookup"><span data-stu-id="e9add-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="e9add-108">Physische Standorte</span><span class="sxs-lookup"><span data-stu-id="e9add-108">Physical locations</span></span>  

- <span data-ttu-id="e9add-109">Zeitpläne, z.B. Wochen oder andere Zeiträume</span><span class="sxs-lookup"><span data-stu-id="e9add-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="e9add-110">Bei Bedarf können Sie einen Arbeitsauftrag in mehrere Arbeitsauftragspools einfügen.</span><span class="sxs-lookup"><span data-stu-id="e9add-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="e9add-111">Arbeitsauftragspool anlegen</span><span class="sxs-lookup"><span data-stu-id="e9add-111">Create a work order pool</span></span>

<span data-ttu-id="e9add-112">Auf der Listenseite **Alle Auftragspools** oder **Aktive Auftragspools** können Sie sich einen Überblick über Ihre Auftragspools verschaffen und neue Pools anlegen.</span><span class="sxs-lookup"><span data-stu-id="e9add-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="e9add-113">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsauftragspools** > **Alle Auftragspools** oder **Aktive Auftragspools**.</span><span class="sxs-lookup"><span data-stu-id="e9add-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="e9add-114">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e9add-114">Select **New**.</span></span>

3. <span data-ttu-id="e9add-115">Geben Sie im Feld **Pool** eine Kennung für den Arbeitsauftragspool ein.</span><span class="sxs-lookup"><span data-stu-id="e9add-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="e9add-116">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="e9add-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="e9add-117">Wählen Sie **Ja** für die Option **Aktiv**, um anzuzeigen, dass der Arbeitsauftragspool aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e9add-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="e9add-118">Wählen Sie **Ja** für die Option **Arbeitsauftragsbeziehungen löschen**, wenn Sie möchten, dass Arbeitsaufträge automatisch aus dem Arbeitsauftragspool entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e9add-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="e9add-119">Wählen Sie im Feld **Lebenszykluszustand löschen** den Lebenszykluszustand des Arbeitsauftrags aus.</span><span class="sxs-lookup"><span data-stu-id="e9add-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="e9add-120">So könnte beispielsweise der Lebenszykluszustand des Arbeitsauftrags für die Fertigstellung eines Arbeitsauftrags so eingestellt werden, dass er automatisch Beziehungen zu Arbeitsauftragspools löscht.</span><span class="sxs-lookup"><span data-stu-id="e9add-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="e9add-121">Sie können sofort mit dem Hinzufügen von Arbeitsaufträgen zu Ihrem Arbeitsauftragspool beginnen.</span><span class="sxs-lookup"><span data-stu-id="e9add-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="e9add-122">Wählen Sie auf dem Inforegister **Arbeitsaufträge** **Zeile hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e9add-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="e9add-123">Wählen Sie einen Arbeitsauftrag im Feld **Arbeitsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="e9add-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="e9add-124">Die Bezugsfelder werden automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e9add-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="e9add-125">Wiederholen Sie die Schritte 8 bis 9, um weitere Arbeitsaufträge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e9add-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="e9add-126">Wenn die Arbeitsaufträge, die von Ihnen hinzugefügt zugefügt wurden, in einer bestimmten Reihenfolge erfolgen sollen, können Sie im Feld **Sortierreihenfolge** die Nummern **1**, **2**, **3** usw. eingeben, um diese Reihenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e9add-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="e9add-127">Um eine Liste aller Arbeitsaufträge anzuzeigen, die im Arbeitsauftragspool enthalten sind, wählen Sie im Aktivitätsbereich auf dem Inforegister **Arbeitsauftragspool** in der Gruppe **Zugehörigen Arbeitsauftragspool anzeigen** **Arbeitsaufträge** aus, um die Listenseite **Alle Arbeitsaufträge** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9add-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="e9add-128">Um die Kapazitätsauslastung für den Wartungszeitplan, ungeplante und geplante Arbeitsaufträge zu berechnen, wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftragspool** in der Gruppe **Zugehörigen Arbeitsauftragspool anzeigen** **Kapazitätsauslastung** aus, um das Dialogfeld **Kapazitätsauslastung berechnen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9add-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="e9add-129">Um die Prognosen für Artikel (Ersatzteile und andere erforderliche Artikel) zu berechnen, die mit dem Wartungszeitplan, nicht geplanten Arbeitsaufträgen und geplanten Arbeitsaufträgen verbunden sind, wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftragspool** in der Gruppe **Zugehörigen Arbeitsauftragspool anzeigen** **Artikelplanung** aus, um das Dialogfeld **Artikelprognose berechnen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9add-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="e9add-130">Um eine Liste aller Bestellanforderungen anzuzeigen, die mit den Arbeitsaufträgen im Arbeitsauftragspool verbunden sind, wählen Sie im Aktivitätsbereich auf dem Inforegister **Arbeitsauftragspool** in der Gruppe **Beschaffung** **Arbeitsauftrag – Bestellanforderung** aus, um die Listenseite **Arbeitsauftrag – Bestellanforderung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9add-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="e9add-131">Um eine Liste aller Bestellungen anzuzeigen, die mit den Arbeitsaufträgen im Arbeitsauftragspool verbunden sind, wählen Sie im Aktivitätsbereich auf dem Inforegister **Arbeitsauftragspool** in der Gruppe **Beschaffung** **Arbeitsauftrag – Einkauf** aus, um die Listenseite **Arbeitsauftrag – Einkauf** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9add-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="e9add-132">Wenn ein Arbeitsauftragspool für Ihre Arbeitsvorbereitung nicht mehr relevant ist, setzen Sie die Option **Aktiv** für diesen Pool in der Listenansicht der Seite **Arbeitsauftragspool** auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="e9add-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="e9add-133">Um alle Arbeitsauftragspositionen zu löschen, setzen Sie die Option **Arbeitsauftragsbeziehungen löschen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e9add-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="e9add-134">Diese Option ist hilfreich, wenn Sie beispielsweise einen leeren Pool erstellen möchten, den Sie für andere Arbeitsaufträge später verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e9add-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="e9add-135">Denken Sie daran, die Option **Arbeitsauftragsbeziehungen löschen** auf **Nein** zu setzen, wenn Sie bereit sind, den Arbeitsauftragspool zum späteren Anlegen neuer Arbeitsauftragsbeziehungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9add-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="e9add-136">In der folgenden Abbildung wird ein Beispiel der Listenseite **Arbeitsauftragspool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9add-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Abbildung 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="e9add-138">Arbeitsauftrag zu einem Arbeitsauftragspool hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e9add-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="e9add-139">Wie im vorherigen Abschnitt beschrieben, können Sie beim Anlegen des Pools Arbeitsaufträge zu einem Arbeitsauftragspool hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e9add-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="e9add-140">Sie können Arbeitsaufträge einem Arbeitsauftragspool auf der Listenseite **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e9add-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="e9add-141">Wählen Sie den Arbeitsauftrag aus, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Verwalten** **Arbeitsauftragspool** aus.</span><span class="sxs-lookup"><span data-stu-id="e9add-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="e9add-142">Wählen Sie den Arbeitsauftrag in der Liste aus und klicken Sie auf **Arbeitsauftragspool**.</span><span class="sxs-lookup"><span data-stu-id="e9add-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="e9add-143">Im Dialogfeld **Arbeitsauftragspool verwalten** im Feld **Hinzufügen/Entfernen** wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="e9add-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="e9add-144">Wählen Sie den Arbeitsauftragspool im Feld **Pool** aus.</span><span class="sxs-lookup"><span data-stu-id="e9add-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="e9add-145">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9add-145">Select **OK**.</span></span>

6. <span data-ttu-id="e9add-146">Um den Arbeitsauftrag zu sperren, den Sie in einer bestimmten Reihenfolge im Arbeitsauftragspool hinzugefügt haben, wählen Sie auf der Listenseite **Alle Arbeitsauftragspools** oder **Aktive Arbeitsauftragspools** den Pool aus, und wählen Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e9add-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="e9add-147">Verwenden Sie anschließend auf der Seite **Arbeitsauftragspool** auf dem Inforegister **Arbeitsaufträge** das Feld **Sortierreihenfolge**, um die Sortierreihenfolge der Arbeitsaufträge anzupassen, die im Pool enthaltenen sind.</span><span class="sxs-lookup"><span data-stu-id="e9add-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="e9add-148">Wenn Sie einen Arbeitsauftrag aus einem Arbeitsauftragspool entfernen möchten, wiederholen Sie diese Schritte, aber wählen in Schritt 3 **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="e9add-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

