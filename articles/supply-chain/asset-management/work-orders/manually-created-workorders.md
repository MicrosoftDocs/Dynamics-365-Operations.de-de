---
title: Manuell erstellte Arbeitsaufträge
description: In diesem Thema wird erläutert, wie Sie im Anlagenmanagement Arbeitsaufträge manuell anlegen.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875671"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="faa3f-103">Manuell erstellte Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="faa3f-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="faa3f-104">Sie können Arbeitsaufträge auf zwei Arten manuell anlegen:</span><span class="sxs-lookup"><span data-stu-id="faa3f-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="faa3f-105">in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**</span><span class="sxs-lookup"><span data-stu-id="faa3f-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="faa3f-106">in **Alle Wartungsanforderungen** oder **Aktive Wartungsanforderungen** oder **Meine Wartungsanforderungen für Technische Standorte**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="faa3f-107">Arbeitsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="faa3f-107">Create work order</span></span>

1. <span data-ttu-id="faa3f-108">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="faa3f-109">Klicken Sie auf die Schaltfläche **Neu**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-109">Click the **New** button.</span></span>

3. <span data-ttu-id="faa3f-110">Wählen Sie in der Dropdown-Liste **Arbeitsauftrag erstellen** einen Arbeitsauftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="faa3f-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="faa3f-111">Wählen Sie bei Bedarf eine Beschreibung aus.</span><span class="sxs-lookup"><span data-stu-id="faa3f-111">If required, select a description.</span></span>

5. <span data-ttu-id="faa3f-112">Wählen Sie die Anlage für den Arbeitsauftrag sowie eine Wartungsauftragsart aus.</span><span class="sxs-lookup"><span data-stu-id="faa3f-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="faa3f-113">Wenn Sie eine Anlage auswählen, stehen Ihnen möglicherweise drei Registerkarten zur Verfügung: Die Registerkarte **Meine Anlagen** enthält Anlagen, die sich auf die Technischen Standorte beziehen, denen Sie (der im System angemeldete Mitarbeiter) zugeordnet werden können (eingerichtet unter [Wartungsarbeiter und Arbeitsgruppen](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="faa3f-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="faa3f-114">Wenn in [Wartungsarbeiter und Arbeitsgruppen](../setup-for-objects/workers-and-worker-groups.md) keine Technischen Standorte für einen Mitarbeiter eingerichtet sind, ist die Registerkarte **Meine Anlagen** nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="faa3f-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="faa3f-115">Die Registerkarte **Aktive Anlagen** enthält eine Liste aller Anlagen mit dem Anlagenlebenszyklusstatus „Aktiv“.</span><span class="sxs-lookup"><span data-stu-id="faa3f-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="faa3f-116">Die Registerkarte **Anlagenansicht** enthält eine Strukturansicht der funktionalen Standorte und Anlagen, die für diese Standorte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="faa3f-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="faa3f-117">Wählen Sie bei Bedarf **Wartungsauftragsartenvariante** und **Wechseln**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="faa3f-118">Bei Bedarf können Sie den Servicegrad des Arbeitsauftrags im Feld **Service Level** ändern.</span><span class="sxs-lookup"><span data-stu-id="faa3f-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="faa3f-119">Wählen Sie in den entsprechenden Feldern das erwartete Start- und Enddatum aus.</span><span class="sxs-lookup"><span data-stu-id="faa3f-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="faa3f-120">Klicken Sie auf **OK**, um einen neuen Arbeitsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="faa3f-121">Bearbeiten Sie den Arbeitsauftrag bei Bedarf unter **Alle Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="faa3f-122">Unter **Alle Arbeitsaufträge** können Sie in der Detailansicht mehrere Anlagen zu einem Arbeitsauftrag hinzufügen, indem Sie Zeilen zu den Wartungsaufträgen **Arbeitsauftrag** FastTab hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="faa3f-123">Auf einer Anlage können Sie nur die Wartungsjobtypen auswählen, die auf der für die Anlage ausgewählten Anlagenart definiert sind.</span><span class="sxs-lookup"><span data-stu-id="faa3f-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="faa3f-124">Wenn Sie einen Anlagenservicegrad oder einen Kritisch-Wert geändert haben, nachdem Sie sie für einen Arbeitsauftrag verwendet haben (siehe [Anlagen-Service-Level](../setup-for-objects/object-priorities.md) und [Anlagenkritiken](../setup-for-objects/object-criticalities.md)), wird der Servicegrad oder die Kritizität auf dem Arbeitsauftrag nicht entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="faa3f-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="faa3f-125">Der kritische Wert eines Arbeitsauftrags wird jedes Mal neu berechnet, wenn eine Arbeitsauftragszeile auf dem Arbeitsauftrag hinzugefügt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="faa3f-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="faa3f-126">Unter **Alle Arbeitsaufträge** Detailansicht > **Leiter** Ansicht > **Terminplan** FastTab können Sie in den Feldern **Verantwortliche Gruppe** oder **Verantwortliche** eine verantwortliche Wartungsgruppe oder einen verantwortlichen Instandhalter auswählen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="faa3f-127">Diese Einstellungen können geändert werden, solange der Arbeitsauftrag aktiv ist, z.B. wenn sich der Lebenszykluszustand des Arbeitsauftrags ändert.</span><span class="sxs-lookup"><span data-stu-id="faa3f-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="faa3f-128">Die automatische Auswahl bei der Erstellung von Arbeitsaufträgen basiert auf dem Setup in **Verantwortliche Wartungsmitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="faa3f-129">Wenn Sie Arbeitsaufträge hinzufügen oder entfernen, nachdem Sie einen Arbeitsauftrag angelegt haben, und das Feld **Verantwortliche Gruppe** und das Feld **Verantwortliche** bei der Aktualisierung des Arbeitsauftrags leer sind, sucht die Anlagenverwaltung nach einer möglichen Übereinstimmung im Setup-Formular für eine verantwortliche Wartungsmitarbeitergruppe oder einen verantwortlichen Wartungsmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="faa3f-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="faa3f-130">Wenn das Feld **Verantwortliche Gruppe** oder das Feld **Verantwortlicher** bei der Aktualisierung des Arbeitsauftrags bereits ausgefüllt ist, werden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="faa3f-131">Unter **Wartungsstatus** können Sie eine Kalkulation durchführen, um sich einen Überblick über die Auslastung der eingehenden und abgeschlossenen Arbeitsaufträge zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="faa3f-132">Verwenden Sie auf der **Zeilendetails** FastTab die Felder **Breite** und **Länge**, um geografische Koordinaten für die im Arbeitsauftrag ausgewählte Anlage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="faa3f-133">Zugehörigen Arbeitsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="faa3f-133">Create related work order</span></span>

<span data-ttu-id="faa3f-134">Sie können einen zugehörigen Arbeitsauftrag zu einem bestehenden Arbeitsauftrag anlegen, wenn Sie z.B. mit primären und sekundären Arbeitsaufträgen arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="faa3f-135">Ein neuer Arbeitsauftrag basiert auf einem Arbeitsauftrag aus einem bestehenden Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="faa3f-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="faa3f-136">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="faa3f-137">Wählen Sie den Arbeitsauftrag aus, für den Sie einen zugehörigen Arbeitsauftrag erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="faa3f-138">Klicken Sie auf **Verwandter Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="faa3f-139">Wählen Sie im Dropdown-Menü **Verwandter Arbeitsauftrag erstellen** im Feld **Verwandter Arbeitsauftrag** den Arbeitsauftrag aus, für den Sie einen entsprechenden Arbeitsauftrag erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="faa3f-140">Wählen Sie im Feld **Wartungsauftragsart** eine Wartungsauftragsart und ggf. eine zugehörige Variante der Wartungsauftragsart aus und handeln Sie in den Feldern **Wartungsauftragsart Variante** und **Wechseln**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="faa3f-141">Wenn dies der erste zugehörige Arbeitsauftrag ist, den Sie erstellen, klicken Sie auf den Auswahlknopf **Neuer Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="faa3f-142">Wählen Sie in den entsprechenden Feldern einen **Arbeitsauftragstyp** und eine **Beschreibung**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="faa3f-143">Ändern Sie bei Bedarf den Servicegrad des Arbeitsauftrags im Feld **Servegrad**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="faa3f-144">Fügen Sie die erwarteten Start- und Enddaten in die entsprechenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="faa3f-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="faa3f-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-145">Click **OK**.</span></span> <span data-ttu-id="faa3f-146">Der neue zugehörige Arbeitsauftrag wird in der Liste **Alle Arbeitsaufträge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="faa3f-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="faa3f-147">Wenn Sie einen zugehörigen Arbeitsauftrag auf einem Arbeitsauftrag anlegen, der bereits zugehörige Arbeitsaufträge hat, können Sie den Arbeitsauftrag zu einem bereits zugehörigen Arbeitsauftrag hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="faa3f-148">Dies geschieht durch Anklicken des Optionsschalters **Zu zugehörigem Arbeitsauftrag hinzufügen** in Schritt 6.</span><span class="sxs-lookup"><span data-stu-id="faa3f-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="faa3f-149">Dann wählen Sie den zugehörigen Arbeitsauftrag aus, dem Sie einen neuen Arbeitsauftrag hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="faa3f-150">Bearbeiten Sie bei Bedarf die Felder **Service Level**, **Erwarteter Start** und **Erwartetes Ende** und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="faa3f-151">Der Arbeitsauftrag wird zu dem bestehenden zugehörigen Arbeitsauftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="faa3f-151">The work order job is added to the existing related work order.</span></span>


![Abbildung 1](media/03-work-orders.png)

<span data-ttu-id="faa3f-153">**Hinweis:** Wenn Sie eine zugehörige Arbeitsauftragsmaske in **Anlagenmanagementparameter** > **Arbeitsaufträge**Link > **Verwandte Arbeitsauftragsmaske** eingerichtet haben, werden Arbeitsauftrags-IDs entsprechend dem Maskenaufbau erstellt.</span><span class="sxs-lookup"><span data-stu-id="faa3f-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="faa3f-154">Wenn keine zugehörige Arbeitsauftragsmaske eingerichtet ist, wird die nächste verfügbare Arbeitsauftrags-ID für zugehörige Arbeitsaufträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa3f-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="faa3f-155">Arbeitsauftrag kopieren</span><span class="sxs-lookup"><span data-stu-id="faa3f-155">Copy work order</span></span>

<span data-ttu-id="faa3f-156">Es ist möglich, schnell einen neuen Arbeitsauftrag aus einem bestehenden Arbeitsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="faa3f-157">Diese Art der Arbeit mit Arbeitsaufträgen unterscheidet sich von der Erstellung von Arbeitsaufträgen auf der Grundlage von Wartungsplänen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="faa3f-158">Dies ist z.B. sinnvoll, wenn Sie einen Arbeitsauftrag haben, der viele Arbeitsaufträge mit verschiedenen Aufträgen auf verschiedenen Anlagen enthält, die in regelmäßigen Abständen erledigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="faa3f-159">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="faa3f-160">Wählen Sie den Arbeitsauftrag aus, aus dem Sie Inhalte kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="faa3f-161">Klicken Sie auf **Arbeitsauftrag kopieren**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-161">Click **Copy work order**.</span></span> <span data-ttu-id="faa3f-162">Die Einrichtung des Arbeitsauftrags aus dem ausgewählten Arbeitsauftrag wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="faa3f-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="faa3f-163">Bei Bedarf können Sie einige der Felder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="faa3f-164">Klicken Sie auf **OK**, um den neuen Arbeitsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="faa3f-165">Bearbeiten Sie den Arbeitsauftrag bei Bedarf unter **Alle Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="faa3f-166">Wenn der neue Arbeitsauftrag erstellt wird, werden einige Informationen direkt aus dem bestehenden Arbeitsauftrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="faa3f-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="faa3f-167">Informationen zu Prognosen, Tools, Wartungschecklisten, Technischen Standorten, Adressen und Terminierung werden nicht kopiert, sondern aus dem aktuellen Setup im Anlagenmanagement initialisiert.</span><span class="sxs-lookup"><span data-stu-id="faa3f-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="faa3f-168">Das bedeutet, dass, wenn Änderungen an diesen Daten vom Zeitpunkt der Erstellung des ersten Arbeitsauftrags bis zum Zeitpunkt der Erstellung einer Kopie des Arbeitsauftrags vorgenommen wurden, diese Änderungen in den neuen Arbeitsauftrag aufgenommen werden, den Sie angelegt haben.</span><span class="sxs-lookup"><span data-stu-id="faa3f-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="faa3f-169">Beispiele sind Änderungen in den Prognosen oder aktualisierte Wartungschecklisten.</span><span class="sxs-lookup"><span data-stu-id="faa3f-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Abbildung 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="faa3f-171">Arbeitsauftrag basierend auf einer Wartungsanforderung anlegen</span><span class="sxs-lookup"><span data-stu-id="faa3f-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="faa3f-172">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Wartungsanforderungen** > **Alle Wartungsanforderungen** oder **Aktive Wartungsanforderungen**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="faa3f-173">Wählen Sie die Wartungsanforderung aus, für die Sie einen Arbeitsauftrag anlegen möchten, und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="faa3f-174">Klicken Sie unter **Alle Anfragen** auf **Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="faa3f-175">Füllen Sie das Dropdown-Menü **Arbeitsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="faa3f-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="faa3f-176">Wenn in der Wartungsanforderung ein Wartungsauftrag ausgewählt wurde, können Sie beim Anlegen des Arbeitsauftrags bei Bedarf einen anderen Wartungsauftragstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="faa3f-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="faa3f-177">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-177">Click **OK**.</span></span> <span data-ttu-id="faa3f-178">Sie erhalten eine Meldung, die Sie darüber informiert, dass der Arbeitsauftrag angelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="faa3f-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="faa3f-179">Wenn Sie sehen möchten, welche Arbeitsaufträge mit einer Wartungsanforderung verbunden sind, markieren Sie die Wartungsanforderung in den Listen **Alle Wartungsanforderungen** oder **Aktive Wartungsanforderungen** und klicken Sie auf die Schaltfläche **Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="faa3f-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Abbildung 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="faa3f-181">Arbeitsaufträge können auch automatisch erstellt werden, indem Wartungsplanjobs eingeplant werden, oder indem Wartungspläne oder Wartungsrunden auf einer Anlage „automatisch erstellt“ werden.</span><span class="sxs-lookup"><span data-stu-id="faa3f-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="faa3f-182">Arbeitsaufträge, die aus Wartungsanforderungen in **Wartungsplan** erstellt wurden, werden mit den in den Wartungsanforderungen ausgewählten Wartungsauftragsarten erstellt.</span><span class="sxs-lookup"><span data-stu-id="faa3f-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

