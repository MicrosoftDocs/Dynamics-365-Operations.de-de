---
title: Geplantes Crossdocking
description: In diesem Thema wird das erweiterte geplante Crossdocking beschrieben, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird. Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017758"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="2061e-104">Geplantes Crossdocking</span><span class="sxs-lookup"><span data-stu-id="2061e-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2061e-105">In diesem Thema wird das erweiterte geplante Crossdocking beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2061e-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="2061e-106">Crossdocking ist ein Lagerortprozess, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2061e-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="2061e-107">Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.</span><span class="sxs-lookup"><span data-stu-id="2061e-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="2061e-108">Durch Crossdocking können Mitarbeiter eingehende Einlagerungen und ausgehende Kommissionierungen vom Lagerbestand überspringen, der bereits für eine ausgehende Bestellung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="2061e-109">Daher wird die Häufigkeit, mit der der Lagerbestand berührt wird, nach Möglichkeit minimiert.</span><span class="sxs-lookup"><span data-stu-id="2061e-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="2061e-110">Da weniger Interaktion mit dem System besteht, wird außerdem die Zeit- und Platzersparnis im Lagerortfertigungsbereich erhöht.</span><span class="sxs-lookup"><span data-stu-id="2061e-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="2061e-111">Bevor Crossdocking ausgeführt werden kann, muss der Benutzer eine neue Crossdocking-Vorlage konfigurieren, in der die Bezugsquelle und andere Anforderungen für das Crossdocking angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2061e-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="2061e-112">Beim Erstellen der ausgehenden Bestellung muss die Position mit einer eingehenden Bestellung markiert werden, die denselben Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="2061e-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="2061e-113">Zum Zeitpunkt des Eingangs eingehender Bestellungen erkennt das Crossdocking-Setup automatisch den Bedarf an Crossdocking und erstellt die Bewegungsarbeit für die erforderliche Menge basierend auf dem Setup der Lagerplatzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2061e-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="2061e-114">Lagerbuchungen sind **nicht** unregistriert, wenn Crossdocking-Arbeiten abgebrochen werden, auch wenn die Einstellung für diese Funktion in den Lagerortverwaltungsparametern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="2061e-115">Funktion für geplantes Crossdocking aktivieren</span><span class="sxs-lookup"><span data-stu-id="2061e-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="2061e-116">Bevor Sie das erweiterte geplante Crossdocking verwenden können, muss die Funktion in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="2061e-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="2061e-117">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2061e-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2061e-118">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="2061e-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2061e-119">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="2061e-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2061e-120">**Funktionsname:** *Geplantes Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2061e-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="2061e-121">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2061e-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="2061e-122">Ladebuchungsmethoden erneut generieren</span><span class="sxs-lookup"><span data-stu-id="2061e-122">Regenerate load posting methods</span></span>

<span data-ttu-id="2061e-123">Das geplante Crossdocking wird als Ladebuchungsmethode implementiert.</span><span class="sxs-lookup"><span data-stu-id="2061e-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="2061e-124">Nachdem Sie die Funktion aktiviert haben, müssen Sie die Methoden erneut generieren.</span><span class="sxs-lookup"><span data-stu-id="2061e-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="2061e-125">Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Ladebuchungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="2061e-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="2061e-126">Wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="2061e-127">Wenn die Regeneration abgeschlossen ist, sollte eine Methode mit **Methodenname** im Wert von *planCrossDocking* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2061e-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="2061e-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2061e-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="2061e-129">Crossdocking-Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="2061e-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="2061e-130">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Crossdocking-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="2061e-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="2061e-131">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2061e-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="2061e-132">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="2061e-133">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="2061e-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="2061e-134">Dieses Feld definiert die Reihenfolge, in der Vorlagen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="2061e-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="2061e-135">**Crossdocking-Vorlagen-ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="2061e-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="2061e-136">**Beschreibung:** *Lagerort 51*</span><span class="sxs-lookup"><span data-stu-id="2061e-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="2061e-137">**Richtlinien zur Bedarfsfreigabe:** *Vor dem Eingang der Lieferung*</span><span class="sxs-lookup"><span data-stu-id="2061e-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="2061e-138">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2061e-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2061e-139">Das Setup im Inforegister **Planung** steuert, wie die Vorlage funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2061e-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="2061e-140">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-140">Set the following values:</span></span>

    - <span data-ttu-id="2061e-141">**Bedarfsanforderungen:** *Keine*</span><span class="sxs-lookup"><span data-stu-id="2061e-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="2061e-142">Dieses Feld definiert die Anforderungen des Bedarfslagerbestands.</span><span class="sxs-lookup"><span data-stu-id="2061e-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="2061e-143">Wenn der Bedarf vor der Freigabe mit der Lieferung verknüpft werden muss, wählen Sie *Markierung* aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="2061e-144">Wenn der Bedarf vor der Freigabe gegen die Lieferung reserviert werden muss, wählen Sie *Auftragsreservierung* aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="2061e-145">**Lagerplatztyp:** *Versandorte*</span><span class="sxs-lookup"><span data-stu-id="2061e-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="2061e-146">In diesem Feld wird definiert, ob für die Crossdocking-Arbeit die Staging-/Ladeorte aus der Sendung oder ob Lagerplatzrichtlinien verwendet werden sollen, um eigene Staging-/Ladeorte zu finden.</span><span class="sxs-lookup"><span data-stu-id="2061e-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="2061e-147">**Arbeitsvorlage:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="2061e-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="2061e-148">Dieses Feld definiert die Arbeitsvorlage, die beim Erstellen von Crossdocking-Arbeiten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2061e-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="2061e-149">**Bei Eingang der Lieferung erneut validieren:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="2061e-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="2061e-150">Diese Option definiert, ob die Lieferung während des Eingangs erneut validiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2061e-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="2061e-151">Wenn diese Option auf *Ja* festgelegt ist, werden sowohl das maximale Zeitfenster als auch der Ablauftagebereich überprüft.</span><span class="sxs-lookup"><span data-stu-id="2061e-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="2061e-152">**Zeitfenster validieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="2061e-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="2061e-153">Diese Option definiert, ob das maximale Zeitfenster ausgewertet werden soll, wenn eine Bezugsquelle ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2061e-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="2061e-154">Wenn diese Option auf *Ja* festgelegt ist, werden die Felder verfügbar, die sich auf das maximale und minimale Zeitfenster beziehen.</span><span class="sxs-lookup"><span data-stu-id="2061e-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="2061e-155">**Maximales Zeitfenster:** *5*</span><span class="sxs-lookup"><span data-stu-id="2061e-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="2061e-156">Dieses Feld definiert den maximalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="2061e-157">**Maximale Zeitfenstereinheit:** *Tage*</span><span class="sxs-lookup"><span data-stu-id="2061e-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="2061e-158">**Minimales Zeitfenster:** *0*</span><span class="sxs-lookup"><span data-stu-id="2061e-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="2061e-159">Dieses Feld definiert den minimalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="2061e-160">**Minimale Zeitfenstereinheit:** *Tage*</span><span class="sxs-lookup"><span data-stu-id="2061e-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="2061e-161">**Ablauftagebereich:** *0*</span><span class="sxs-lookup"><span data-stu-id="2061e-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="2061e-162">*First Expiry First Out (FEFO)-Kriterien:* Dieses Feld definiert die maximale Anzahl von Tagen zwischen dem Ablaufdatum der ersten ablaufenden Charge, die sich derzeit im Lagerort befindet, und der Charge, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2061e-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="2061e-163">Geben Sie im Inforegister **Bezugsquellen** die Liefertypen an, die für diese Vorlage gültig sind.</span><span class="sxs-lookup"><span data-stu-id="2061e-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="2061e-164">Wählen Sie **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="2061e-165">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="2061e-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2061e-166">**Bezugsquelle:** *Bestellung*</span><span class="sxs-lookup"><span data-stu-id="2061e-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="2061e-167">Eine Arbeitsklasse erstellen</span><span class="sxs-lookup"><span data-stu-id="2061e-167">Create a work class</span></span>

1. <span data-ttu-id="2061e-168">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="2061e-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="2061e-169">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsklasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2061e-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="2061e-170">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-170">Set the following values:</span></span>

    - <span data-ttu-id="2061e-171">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2061e-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="2061e-172">**Beschreibung:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2061e-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="2061e-173">**Arbeitsauftragstyp:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2061e-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="2061e-174">Erstellen einer Arbeitsvorlage</span><span class="sxs-lookup"><span data-stu-id="2061e-174">Create a work template</span></span>

1. <span data-ttu-id="2061e-175">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="2061e-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="2061e-176">Legen Sie im Feld **Arbeitsauftragstyp** *Crossdocking* fest.</span><span class="sxs-lookup"><span data-stu-id="2061e-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="2061e-177">Wählen Sie im Aktivitätsbereich **Neu** aus, um auf der Registerkarte **Übersicht** eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2061e-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="2061e-178">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2061e-179">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="2061e-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2061e-180">**Arbeitsvorlage:** *51 Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2061e-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="2061e-181">**Arbeitsvorlagenbeschreibung:** *51 Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2061e-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="2061e-182">Wählen Sie **Speichern** aus, um das Inforegister **Arbeitsvorlagendetails** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2061e-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="2061e-183">Wählen Sie im Inforegister **Arbeitsvorlagendetails** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2061e-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2061e-184">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2061e-185">**Arbeitstyp:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="2061e-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="2061e-186">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2061e-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="2061e-187">Wählen Sie **Neu** aus, um eine weitere Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="2061e-188">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="2061e-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2061e-189">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2061e-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="2061e-190">Wählen Sie **Speichern** aus, und bestätigen Sie, dass das Kontrollkästchen **Gültig** für die Vorlage *51 Crossdocking* ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="2061e-191">Die Arbeitsklassen-IDs für die Arbeitstypen *Entnehmen* und *Einlagern* müssen gleich sein.</span><span class="sxs-lookup"><span data-stu-id="2061e-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="2061e-192">Lagerplatzrichtlinien erstellen</span><span class="sxs-lookup"><span data-stu-id="2061e-192">Create location directives</span></span>

1. <span data-ttu-id="2061e-193">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="2061e-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2061e-194">Legen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Crossdocking* fest.</span><span class="sxs-lookup"><span data-stu-id="2061e-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="2061e-195">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="2061e-196">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="2061e-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2061e-197">**Name:** *51 Crossdocking einlagern*</span><span class="sxs-lookup"><span data-stu-id="2061e-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="2061e-198">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="2061e-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2061e-199">**Standort:** *5*</span><span class="sxs-lookup"><span data-stu-id="2061e-199">**Site:** *5*</span></span>
    - <span data-ttu-id="2061e-200">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2061e-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2061e-201">Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2061e-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="2061e-202">Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2061e-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2061e-203">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2061e-204">**Von Menge:** *1*</span><span class="sxs-lookup"><span data-stu-id="2061e-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="2061e-205">**Bis Menge:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="2061e-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="2061e-206">Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2061e-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2061e-207">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2061e-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2061e-208">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2061e-209">**Name:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="2061e-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="2061e-210">**Feste Standortnutzung:** *Feste und nicht feste Lagerplätze*</span><span class="sxs-lookup"><span data-stu-id="2061e-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="2061e-211">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** in der Symbolleiste **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2061e-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="2061e-212">Wählen Sie **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2061e-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="2061e-213">Stellen Sie auf der Registerkarte **Bereich** sicher, dass die folgenden zwei Positionen konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="2061e-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="2061e-214">Position 1:</span><span class="sxs-lookup"><span data-stu-id="2061e-214">Line 1:</span></span>

        - <span data-ttu-id="2061e-215">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2061e-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="2061e-216">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2061e-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="2061e-217">**Feld:** *Lagerort*</span><span class="sxs-lookup"><span data-stu-id="2061e-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="2061e-218">**Kriterien:** *51*</span><span class="sxs-lookup"><span data-stu-id="2061e-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="2061e-219">Position 2:</span><span class="sxs-lookup"><span data-stu-id="2061e-219">Line 2:</span></span>

        - <span data-ttu-id="2061e-220">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2061e-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="2061e-221">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2061e-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="2061e-222">**Feld:** *Lagerplatz*</span><span class="sxs-lookup"><span data-stu-id="2061e-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="2061e-223">**Kriterien:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="2061e-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="2061e-224">Wählen Sie **OK** aus, um den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2061e-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="2061e-225">Erstellen eines Menüelements für ein mobiles Geräts</span><span class="sxs-lookup"><span data-stu-id="2061e-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="2061e-226">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="2061e-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2061e-227">Wählen Sie in der Liste der Menüpunkte im linken Bereich die Option **Kaufeinlagerung** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="2061e-228">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-228">Select **Edit**.</span></span>
1. <span data-ttu-id="2061e-229">Wählen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2061e-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2061e-230">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2061e-231">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2061e-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="2061e-232">**Arbeitsauftragstyp:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2061e-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="2061e-233">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="2061e-234">Szenario</span><span class="sxs-lookup"><span data-stu-id="2061e-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="2061e-235">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="2061e-235">Create a purchase order</span></span>

<span data-ttu-id="2061e-236">Befolgen Sie diese Schritte, um eine Bestellung als Bezugsquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2061e-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="2061e-237">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="2061e-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="2061e-238">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2061e-239">Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2061e-240">**Kreditorenkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="2061e-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="2061e-241">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2061e-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2061e-242">Wählen Sie **OK** aus, und notieren Sie sich die Bestellnummer.</span><span class="sxs-lookup"><span data-stu-id="2061e-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="2061e-243">Im Inforegister **Bestellpositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2061e-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="2061e-244">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="2061e-245">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="2061e-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2061e-246">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="2061e-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="2061e-247">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="2061e-247">Create a sales order</span></span>

<span data-ttu-id="2061e-248">Befolgen Sie diese Schritte, um einen Auftrag als Bedarfsquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2061e-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="2061e-249">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="2061e-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2061e-250">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2061e-251">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2061e-252">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="2061e-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="2061e-253">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2061e-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2061e-254">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2061e-254">Select **OK**.</span></span>
1. <span data-ttu-id="2061e-255">Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2061e-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2061e-256">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="2061e-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="2061e-257">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="2061e-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2061e-258">**Menge** *3*</span><span class="sxs-lookup"><span data-stu-id="2061e-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="2061e-259">Geplantes Crossdocking erstellen</span><span class="sxs-lookup"><span data-stu-id="2061e-259">Create planned cross-docking</span></span>

<span data-ttu-id="2061e-260">Befolgen Sie diese Schritte, um das geplante Crossdocking aus dem Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2061e-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="2061e-261">Wählen Sie auf der Seite **Auftragsdetails** für den Auftrag, den Sie gerade erstellt haben, im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Aktivitäten** die Option **An Lager freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2061e-262">Die Aktivität „An Lager freigeben“ erstellt eine Versand- und Ladeposition für die Auftragsposition und versucht, Lagerbestand zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2061e-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="2061e-263">Es wird eine Informationsnachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2061e-263">You receive an informational message.</span></span> <span data-ttu-id="2061e-264">Sie erhalten außerdem die folgende Warnmeldung: „Für Welle XXXX wurde keine Arbeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="2061e-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="2061e-265">Weitere Informationen finden Sie im Protokoll zum Arbeitserstellungsverlauf.“</span><span class="sxs-lookup"><span data-stu-id="2061e-265">See the work creation history log for details."</span></span> <span data-ttu-id="2061e-266">Dieses Verhalten wird erwartet, da sich kein Lagerbestand im Lagerort befindet.</span><span class="sxs-lookup"><span data-stu-id="2061e-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="2061e-267">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** die Option **Lieferdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="2061e-268">Die Seite **Lieferdetails** wird angezeigt und zeigt die Lieferung, die für den Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2061e-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="2061e-269">Überprüfen Sie, ob im Inforegister **Ladungspositionen** das Feld **Geplante Crossdocking-Menge** auf *3* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="2061e-270">Da im Lagerort kein Lagerbestand verfügbar war, aber innerhalb des in der Crossdocking-Vorlage definierten Zeitfensters eine gültige Bezugsquelle eintrifft, wurde die Crossdocking-Menge erstellt.</span><span class="sxs-lookup"><span data-stu-id="2061e-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="2061e-271">Wählen Sie im Inforegister **Ladungspositionen** die Option **Geplantes Crossdocking** aus, um die Details des erstellten Crossdocking anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2061e-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="2061e-272">Crossdocking verarbeiten</span><span class="sxs-lookup"><span data-stu-id="2061e-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="2061e-273">Bestelleingang mit der Warehouse Mobile App</span><span class="sxs-lookup"><span data-stu-id="2061e-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="2061e-274">Das System erhält die Menge von 5 aus der Bestellung an den Empfangsort und erstellt zwei Arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2061e-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="2061e-275">Die erste Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Crossdocking* und ist mit dem Auftrag verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2061e-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="2061e-276">Sie hat eine Menge von 3 und wird zum endgültigen Versandort geleitet, damit sie sofort versendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2061e-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="2061e-277">Die zweite Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Bestellungen* und ist mit der Bestellung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2061e-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="2061e-278">Sie hat die verbleibende Menge von 2, für die das Crossdocking nicht durchgeführt wurde und zur Einlagerung bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="2061e-279">Melden Sie sich beim mobilen Gerät als ein Benutzer im Lagerort *51* an.</span><span class="sxs-lookup"><span data-stu-id="2061e-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="2061e-280">Gehen Sie zu **Eingehend \> Kaufempfang**.</span><span class="sxs-lookup"><span data-stu-id="2061e-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="2061e-281">Geben Sie im Feld **PONum** Ihre Bestellnummer ein.</span><span class="sxs-lookup"><span data-stu-id="2061e-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="2061e-282">Geben Sie im Feld **Menge** den Wert *5* ein.</span><span class="sxs-lookup"><span data-stu-id="2061e-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="2061e-283">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2061e-283">Select **OK**.</span></span>
1. <span data-ttu-id="2061e-284">Legen Sie auf der nächsten Seite im Feld **Artikel** *A0001* fest.</span><span class="sxs-lookup"><span data-stu-id="2061e-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="2061e-285">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2061e-285">Select **OK**.</span></span>
1. <span data-ttu-id="2061e-286">Bestätigen Sie auf der nächsten Seite die Werte **PONum** , **Artikel** und **Menge** , indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2061e-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="2061e-287">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="2061e-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2061e-288">Wählen Sie **Abbrechen** aus, um zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2061e-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="2061e-289">Einlagerung zu Crossdocking und Bulk</span><span class="sxs-lookup"><span data-stu-id="2061e-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="2061e-290">Derzeit haben beide Arbeits-IDs das gleiche Zielkennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2061e-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="2061e-291">Um die nächsten Schritte ausführen zu können, müssen Sie die Arbeits-ID und die Zielkennzeichen-ID erhalten.</span><span class="sxs-lookup"><span data-stu-id="2061e-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="2061e-292">Sie können diese Informationen aus den Arbeitsdetails für die Bestellposition und die Auftragsposition abrufen.</span><span class="sxs-lookup"><span data-stu-id="2061e-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="2061e-293">Alternativ können Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails** gehen und nach Arbeit filtern, wo der Wert von **Lagerort** *51* ist.</span><span class="sxs-lookup"><span data-stu-id="2061e-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="2061e-294">Gehen Sie auf dem mobilen Gerät zu **Eingehend \> Kaufeinlagerung** , und geben Sie das Zielkennzeichen von der Arbeit ein.</span><span class="sxs-lookup"><span data-stu-id="2061e-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="2061e-295">Geben Sie im Feld **ID** die Zielkennzeichen-ID aus den Arbeitsdetails ein.</span><span class="sxs-lookup"><span data-stu-id="2061e-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="2061e-296">Die Crossdocking-Auswahlseite zeigt den Kommissionierort ( *RECV* ), das Zielkennzeichen ( *Kennzeichen* ), den Artikel ( *A0001* ) und die Menge ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="2061e-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="2061e-297">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2061e-297">Select **OK**.</span></span>
1. <span data-ttu-id="2061e-298">Geben Sie im Feld **Ziel-LP** ein Zielkennzeichen für die Kennzeichen-ID ein, die am Versandort eingelagert (Crossdocking) werden soll.</span><span class="sxs-lookup"><span data-stu-id="2061e-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="2061e-299">Sie können eine beliebige Kennzeichen-ID Ihrer Wahl auswählen.</span><span class="sxs-lookup"><span data-stu-id="2061e-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="2061e-300">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2061e-300">Select **OK**.</span></span>
1. <span data-ttu-id="2061e-301">Geben Sie auf der nächsten Seite im Feld **ID** die Zielkennzeichen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="2061e-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="2061e-302">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2061e-302">Select **OK**.</span></span>
1. <span data-ttu-id="2061e-303">Bestätigen Sie die Arbeit zur Auswahl der verbleibenden Menge von 2, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2061e-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="2061e-304">Wählen Sie auf der nächsten Seite **Fertig** aus, um den Kommissioniervorgang zu beenden und den Einlagerungsprozess zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="2061e-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="2061e-305">Die mobile App zeigt Ihnen den Lagerplatz und das Kennzeichen an, an dem Sie den Artikel ablegen möchten.</span><span class="sxs-lookup"><span data-stu-id="2061e-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="2061e-306">Bestätigen Sie den Bulk-Lagerplatz **Einlagern** , indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2061e-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="2061e-307">Bestätigen Sie auf der nächsten Seite das Crossdocking **Einlagern** , indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2061e-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="2061e-308">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="2061e-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2061e-309">Wählen Sie **Abbrechen** aus, um zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2061e-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="2061e-310">Die folgende Abbildung zeigt, wie die abgeschlossene Crossdocking-Arbeit in Microsoft Dynamics 365 Supply Chain Management aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="2061e-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="2061e-311">![Crossdocking-Arbeit abgeschlossen](media/PlannedCrossDockingWork.png "Crossdocking-Arbeit abgeschlossen")</span><span class="sxs-lookup"><span data-stu-id="2061e-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
