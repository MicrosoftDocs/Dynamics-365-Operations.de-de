---
title: Manuell erstellte Arbeitsaufträge
description: In diesem Thema wird erläutert, wie Sie im Anlagenmanagement Arbeitsaufträge manuell anlegen.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428520"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="80105-103">Manuell erstellte Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="80105-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="80105-104">Sie können Arbeitsaufträge auf zwei Arten manuell anlegen:</span><span class="sxs-lookup"><span data-stu-id="80105-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="80105-105">Auf der Seite **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**</span><span class="sxs-lookup"><span data-stu-id="80105-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="80105-106">Auf der Seite **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte**</span><span class="sxs-lookup"><span data-stu-id="80105-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="80105-107">Arbeitsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="80105-107">Create work order</span></span>

1. <span data-ttu-id="80105-108">Wählen Sie **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="80105-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-109">Select **New**.</span></span>

3. <span data-ttu-id="80105-110">Im Dialogfeld **Arbeitsauftrag erstellen** wählen Sie einen Arbeitsauftragstyp im Feld **Arbeitsauftragstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="80105-111">Wählen Sie bei Bedarf eine **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="80105-112">Wählen Sie im Feld **Anlage** die Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="80105-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="80105-113">Wenn Sie eine Anlage auswählen, sind möglicherweise drei Registerkarten im Dropdown **Anlage** verfügbar:</span><span class="sxs-lookup"><span data-stu-id="80105-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="80105-114">**Aktive Anlagen** – Diese Registerkarte enthält eine Liste aller Anlagen mit dem Anlagenlebenszyklusstatus „Aktiv“.</span><span class="sxs-lookup"><span data-stu-id="80105-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="80105-115">**Anlagenansicht** – Die Registerkarte enthält eine Strukturansicht der funktionalen Standorte und der Anlagen, die für diese Standorte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="80105-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="80105-116">**Meine Anlagen** – Diese Registerkarte enthält Anlagen, die den funktionalen Standorten zugeordnet werden, denen Sie (die am System angemeldete Arbeitskraft) möglicherweise zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="80105-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="80105-117">(Informationen zum Einrichten siehe [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).) Wenn keine funktionalen Standorte für eine Arbeitskraft unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md) eingerichtet werden, ist die Registerkarte **Meine Anlagen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="80105-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="80105-118">Wählen Sie im Feld **Wartungsauftragstyp** den Wartungsauftragstyp für den Wartungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="80105-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="80105-119">Wählen Sie bei Bedarf **Wartungsauftragsartenvariante** und **Wechseln**.</span><span class="sxs-lookup"><span data-stu-id="80105-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="80105-120">Bei Bedarf können Sie den Servicegrad des Arbeitsauftrags im Feld **Service Level** ändern.</span><span class="sxs-lookup"><span data-stu-id="80105-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="80105-121">Wählen Sie in den entsprechenden Feldern das **erwartete Startdatum**-und das **erwartete Enddatum** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="80105-122">Klicken Sie auf **OK**, um den Arbeitsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="80105-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="80105-123">Auf der Listenseite **Alle Arbeitsaufträge** können Sie den Arbeitsauftrag nach Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="80105-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="80105-124">Beachten Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="80105-124">Note the following points:</span></span>

- <span data-ttu-id="80105-125">In der Detailansicht auf der Listenseite **Alle Arbeitsaufträge** können Sie mehrere Anlagen zu einem Arbeitsauftrag hinzufügen, indem Sie Positionen zu den Wartungsaufträgen im Inforegister **Wartungsaufträge für Arbeitsaufträge** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="80105-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="80105-126">In einer Anlage können Sie nur die Wartungsauftragstypen auswählen, die für die für die Anlage ausgewählten Anlagenart definiert sind.</span><span class="sxs-lookup"><span data-stu-id="80105-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="80105-127">Wenn Sie einen Anlagenservicelevel oder eine Anlagenkritikalität ändern, nachdem Sie die Anlage für einen Arbeitsauftrag verwendet haben, wird der Servicelevel oder die Kritikalität für den Arbeitsauftrag nicht entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80105-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="80105-128">Weitere Informationen zu Service Levels und Kritikalitäten finden Sie unter [Asset Service Levels](../setup-for-objects/object-priorities.md) und [Asset Kritikalitätsarten](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="80105-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="80105-129">Die Kritikalität eines Arbeitsauftrags wird jedes Mal neu berechnet, wenn eine Arbeitsauftragseinzelvorgang zum Arbeitsauftrag hinzugefügt oder daraus gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="80105-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="80105-130">In der Detailansicht **Alle Arbeitsaufträge** > Ansicht **Leiter** > Inforegister **Terminplan** können Sie in den Feldern **Verantwortliche Gruppe** oder **Verantwortlich** eine verantwortliche Wartungsgruppe oder einen verantwortlichen Wartungsarbeiter auswählen.</span><span class="sxs-lookup"><span data-stu-id="80105-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="80105-131">Diese Einstellungen können geändert werden, während der Arbeitsauftrag aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="80105-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="80105-132">Sie können geändert werden, wenn sich der Arbeitsauftragslebenszyklusstatus ändert.</span><span class="sxs-lookup"><span data-stu-id="80105-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="80105-133">Die automatische Auswahl bei der Erstellung von Arbeitsaufträgen basiert auf dem Setup auf der Seite **Zuständige Wartungsarbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="80105-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="80105-134">Wenn Sie Arbeitsaufträge hinzufügen oder entfernen, nachdem Sie einen Arbeitsauftrag angelegt haben, und das Feld **Verantwortliche Gruppe** und das Feld **Verantwortlich** bei der Aktualisierung des Arbeitsauftrags leer sind, sucht die Anlagenverwaltung nach einer möglichen Übereinstimmung für eine verantwortliche Wartungsmitarbeitergruppe oder einen verantwortlichen Wartungsmitarbeiter auf der Einrichtungsseite.</span><span class="sxs-lookup"><span data-stu-id="80105-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="80105-135">Wenn das Feld **Verantwortliche Gruppe** oder das Feld **Verantwortlich** bei der Aktualisierung des Arbeitsauftrags bereits ausgefüllt ist, werden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="80105-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="80105-136">Weitere Informationen über verantwortliche Wartungsarbeiter und Wartungsarbeitergruppen finden Sie unter [Zuständige Wartungsarbeitskräfte](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="80105-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="80105-137">Auf der Seite [Wartungsstatus](../controlling-and-reporting/maintenance-status.md) können Sie eine Kalkulation durchführen, um sich einen Überblick über die Auslastung der eingehenden und abgeschlossenen Arbeitsaufträge zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="80105-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="80105-138">In der Detailansicht der Seite **Alle Arbeitsaufträge** auf dem Inforegister **Positionsdetails**, können Sie die Felder **Breite** und **Länge** verwenden, um geografische Koordinaten für die Anlage hinzuzufügen, die für den Arbeitsauftragseinzelvorgang aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80105-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="80105-139">Zugehörigen Arbeitsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="80105-139">Create related work order</span></span>

<span data-ttu-id="80105-140">Sie können einen Arbeitsauftrag erstellen, der zu einem vorhandenen Arbeitsauftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="80105-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="80105-141">Diese Funktion ist z. B. hilfreich, wenn Sie mit primären und sekundären Arbeitsaufträgen arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="80105-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="80105-142">Ein neuer Arbeitsauftrag basiert auf einem Arbeitsauftrag aus einem bestehenden Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="80105-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="80105-143">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="80105-144">Wählen Sie den zu erstellenden Arbeitsauftrag aus, für den ein zugehöriger Arbeitsauftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="80105-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="80105-145">Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Neu** die Option **Zugehöriger Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="80105-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="80105-146">Wählen Sie im Dialogfeld **Zugehörigen Arbeitsauftrag erstellen** im Feld **Arbeitsauftragseinzelvorgang** den Arbeitsauftragseinzelvorgang aus, für den Sie einen zugehörigen Arbeitsauftrag erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="80105-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="80105-147">Wählen Sie im Feld **Wartungsauftragstyp** den Wartungsauftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="80105-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="80105-148">Wählen Sie in den Feldern **Wartungsauftragstypvariante** und **Art** nach Bedarf die Variante und Art aus, die sich auf den Wartungsauftragstyp beziehen.</span><span class="sxs-lookup"><span data-stu-id="80105-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="80105-149">Wenn dieser Arbeitsauftrag der erste zugehörige Arbeitsauftrag ist, der für den ausgewählten Arbeitsauftrag erstellt wurde, gehen Sie gemäß den folgenden Schritten vor:</span><span class="sxs-lookup"><span data-stu-id="80105-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="80105-150">Wählen Sie die Option **Neuer Arbeitsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="80105-151">Wählen Sie im Feld **Arbeitsauftragstyp** einen Arbeitsauftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="80105-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="80105-152">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="80105-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="80105-153">Ändern Sie bei Bedarf die Leistungsebene des Arbeitsauftrags im Feld **Leistungsebene**.</span><span class="sxs-lookup"><span data-stu-id="80105-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="80105-154">Wählen Sie in den Feldern **Erwartetes Anfangsdatum** und **Erwartetes Enddatum** das erwartete Start- und Enddatum aus.</span><span class="sxs-lookup"><span data-stu-id="80105-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="80105-155">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="80105-155">Select **OK**.</span></span> <span data-ttu-id="80105-156">Der neue zugehörige Arbeitsauftrag wird in der Listenseite **Alle Arbeitsaufträge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80105-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="80105-157">Wenn der Arbeitsauftrag, für den Sie diesen zugehörigen Arbeitsauftrag erstellen, bereits zugehörige Arbeitsaufträge hat, führen Sie die folgenden Schritte aus, um einen Arbeitsauftragseinzelvorgang einem vorhandenen zugehörigen Arbeitsauftrag hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="80105-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="80105-158">Wählen Sie die Option **Zu zugehörigem Arbeitsauftrag hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="80105-159">Wähle Sie im Feld **Arbeitsauftrag** den zugehörigen Arbeitsauftrag aus, dem Sie einen neuen Arbeitsauftragseinzelvorgang hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="80105-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="80105-160">Ändern Sie bei Bedarf die Leistungsebene des Arbeitsauftrags im Feld **Leistungsebene**.</span><span class="sxs-lookup"><span data-stu-id="80105-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="80105-161">Ändern Sie in den Feldern **Erwartetes Anfangsdatum** und **Erwartetes Enddatum** das erwartete Start- und Enddatum nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="80105-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="80105-162">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="80105-162">Select **OK**.</span></span> <span data-ttu-id="80105-163">Der Arbeitsauftrag wird zu dem bestehenden zugehörigen Arbeitsauftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="80105-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="80105-164">Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Zugehörigen Arbeitsauftrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="80105-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Abbildung 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="80105-166">Wenn Sie eine zugehörige Arbeitsauftragsmaske unter **Anlagenverwaltungsparameter** > **Arbeitsaufträge** > **Verwandte Arbeitsauftragsmaske** eingerichtet haben, werden Arbeitsauftrags-IDs entsprechend dem Maskenaufbau erstellt.</span><span class="sxs-lookup"><span data-stu-id="80105-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="80105-167">Wenn keine zugehörige Arbeitsauftragsmaske eingerichtet ist, wird die nächste verfügbare Arbeitsauftrags-ID für zugehörige Arbeitsaufträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="80105-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="80105-168">Arbeitsauftrag kopieren</span><span class="sxs-lookup"><span data-stu-id="80105-168">Copy a work order</span></span>

<span data-ttu-id="80105-169">Es ist möglich, schnell einen neuen Arbeitsauftrag aus einem bestehenden Arbeitsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="80105-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="80105-170">Diese Art der Arbeit mit Arbeitsaufträgen unterscheidet sich von der Erstellung von Arbeitsaufträgen auf der Grundlage von [Wartungsplänen](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="80105-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="80105-171">Dies ist z.B. sinnvoll, wenn Sie ein Arbeitsauftrag viele Arbeitsaufträge enthält, und verschiedene Einzelvorgänge auf verschiedenen Anlagen in regelmäßigen Abständen erledigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80105-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="80105-172">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="80105-173">Wählen Sie den Arbeitsauftrag aus, aus dem Sie Inhalte kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="80105-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="80105-174">Wählen Sie im Aktivitätsbereich > Registerkarte **Arbeitsauftrag** > Gruppe **Neu** die Option **Arbeitsauftrag kopieren**.</span><span class="sxs-lookup"><span data-stu-id="80105-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="80105-175">Die Einrichtung des Arbeitsauftrags aus dem ausgewählten Arbeitsauftrag wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80105-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="80105-176">Bei Bedarf können Sie einige der Felder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="80105-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="80105-177">Wählen Sie **OK** aus, um den neuen Arbeitsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="80105-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="80105-178">Auf der Listenseite **Alle Arbeitsaufträge** können Sie den Arbeitsauftrag nach Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="80105-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="80105-179">Wenn der neue Arbeitsauftrag erstellt wird, werden einige Informationen direkt aus dem bestehenden Arbeitsauftrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="80105-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="80105-180">Informationen über Planungen, Werkzeuge, Wartungsprüflisten, funktionale Standorte, Adressen und Zeitplanung werden nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="80105-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="80105-181">Stattdessen werden sie über die aktuelle Einstellung in der Anlagenverwaltung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="80105-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="80105-182">Wenn diese Informationen zwischen dem Zeitpunkt geändert wurden, als erste Arbeitsauftrag erstellt wurde, und dem Zeitpunkt, zu dem Sie eine Kopie des Arbeitsauftrag erstellten, werden die Änderungen in den neuen Arbeitsauftrag einbezogen.</span><span class="sxs-lookup"><span data-stu-id="80105-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="80105-183">Beispiele umfassen Änderungen an den Prognosen und Aktualisierungen von Wartungsprüflisten.</span><span class="sxs-lookup"><span data-stu-id="80105-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="80105-184">In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Arbeitsauftrag kopieren** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80105-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Abbildung 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="80105-186">Arbeitsauftrag basierend auf einer Wartungsanforderung anlegen</span><span class="sxs-lookup"><span data-stu-id="80105-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="80105-187">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Wartungsanfragen** > **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="80105-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="80105-188">Wählen Sie die Wartungsanfrage aus, für die Sie einen Arbeitsauftrag anlegen möchten, und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="80105-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="80105-189">Wählen Sie im Aktivitätsbereich > Registerkarte **Wartungsanfrage** > Gruppe **Neu** die Option **Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="80105-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="80105-190">Im Dialogfeld **Arbeitsauftrag** können Sie die Felder festlegen.</span><span class="sxs-lookup"><span data-stu-id="80105-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="80105-191">Wenn in der Wartungsanfrage ein Wartungsauftrag ausgewählt wurde, können Sie beim Anlegen des Arbeitsauftrags bei Bedarf einen anderen Wartungsauftragstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="80105-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="80105-192">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="80105-192">Select **OK**.</span></span> <span data-ttu-id="80105-193">Die Nachricht informiert Sie darüber, dass ein Arbeitsauftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="80105-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="80105-194">Wenn Sie sehen möchten, welche Arbeitsaufträge mit einer Wartungsanfrage verbunden sind, markieren Sie die Wartungsanfrage auf der Listenseite **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen**.</span><span class="sxs-lookup"><span data-stu-id="80105-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="80105-195">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Wartungsanfrage** in der Gruppe **Ansicht** die Option **Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="80105-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="80105-196">In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Arbeitsauftrag erstellen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80105-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Abbildung 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="80105-198">Wenn Arbeitsaufträge automatisch erstellt werden sollen, können Sie Wartungsplanjobs planen oder festlegen, dass [Wartungspläne](../preventive-and-reactive-maintenance/maintenance-plans.md) oder [Wartungsrunden](../preventive-and-reactive-maintenance/maintenance-rounds.md) auf einer Anlage automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="80105-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="80105-199">Arbeitsaufträge, die aus Wartungsanfragen auf der Listenseite **Alle Wartungszeitpläne** erstellt wurden, weisen die in den Wartungsanfragen ausgewählten Wartungsauftragsarten auf.</span><span class="sxs-lookup"><span data-stu-id="80105-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

