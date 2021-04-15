---
title: Geplantes Crossdocking
description: In diesem Thema wird das erweiterte geplante Crossdocking beschrieben, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird. Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 49807c90c145eee55fae2d515fd19925eb2d944c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810413"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="d79f7-104">Geplantes Crossdocking</span><span class="sxs-lookup"><span data-stu-id="d79f7-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d79f7-105">In diesem Thema wird das erweiterte geplante Crossdocking beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d79f7-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="d79f7-106">Crossdocking ist ein Lagerortprozess, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d79f7-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="d79f7-107">Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.</span><span class="sxs-lookup"><span data-stu-id="d79f7-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="d79f7-108">Durch Crossdocking können Mitarbeiter eingehende Einlagerungen und ausgehende Kommissionierungen vom Lagerbestand überspringen, der bereits für eine ausgehende Bestellung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="d79f7-109">Daher wird die Häufigkeit, mit der der Lagerbestand berührt wird, nach Möglichkeit minimiert.</span><span class="sxs-lookup"><span data-stu-id="d79f7-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="d79f7-110">Da weniger Interaktion mit dem System besteht, wird außerdem die Zeit- und Platzersparnis im Lagerortfertigungsbereich erhöht.</span><span class="sxs-lookup"><span data-stu-id="d79f7-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="d79f7-111">Bevor Crossdocking ausgeführt werden kann, muss der Benutzer eine neue Crossdocking-Vorlage konfigurieren, in der die Bezugsquelle und andere Anforderungen für das Crossdocking angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d79f7-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="d79f7-112">Beim Erstellen der ausgehenden Bestellung muss die Position mit einer eingehenden Bestellung markiert werden, die denselben Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="d79f7-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="d79f7-113">Zum Zeitpunkt des Eingangs eingehender Bestellungen erkennt das Crossdocking-Setup automatisch den Bedarf an Crossdocking und erstellt die Bewegungsarbeit für die erforderliche Menge basierend auf dem Setup der Lagerplatzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d79f7-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="d79f7-114">Lagerbuchungen sind **nicht** unregistriert, wenn Crossdocking-Arbeiten abgebrochen werden, auch wenn die Einstellung für diese Funktion in den Lagerortverwaltungsparametern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="d79f7-115">Schalten Sie die Funktionen für das geplante Cross Docking ein</span><span class="sxs-lookup"><span data-stu-id="d79f7-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="d79f7-116">Wenn Ihr System nicht bereits die in diesem Thema beschriebenen Funktionen enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen in der folgenden Reihenfolge ein:</span><span class="sxs-lookup"><span data-stu-id="d79f7-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="d79f7-117">*Geplantes Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="d79f7-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="d79f7-118">*Crossdockingvorlagen mit Lagerplatzrichtlinien*</span><span class="sxs-lookup"><span data-stu-id="d79f7-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="d79f7-119">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d79f7-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="d79f7-120">Ladebuchungsmethoden erneut generieren</span><span class="sxs-lookup"><span data-stu-id="d79f7-120">Regenerate load posting methods</span></span>

<span data-ttu-id="d79f7-121">Das geplante Crossdocking wird als Ladebuchungsmethode implementiert.</span><span class="sxs-lookup"><span data-stu-id="d79f7-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="d79f7-122">Nachdem Sie die Funktion aktiviert haben, müssen Sie die Methoden erneut generieren.</span><span class="sxs-lookup"><span data-stu-id="d79f7-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="d79f7-123">Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Ladebuchungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="d79f7-124">Wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d79f7-125">Wenn die Regeneration abgeschlossen ist, sollte eine Methode mit **Methodenname** im Wert von *planCrossDocking* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d79f7-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="d79f7-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d79f7-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="d79f7-127">Crossdocking-Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="d79f7-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="d79f7-128">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Crossdocking-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="d79f7-129">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="d79f7-130">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="d79f7-131">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79f7-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="d79f7-132">Dieses Feld definiert die Reihenfolge, in der Vorlagen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="d79f7-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="d79f7-133">**Crossdocking-Vorlagen-ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="d79f7-134">**Beschreibung:** *Lagerort 51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="d79f7-135">**Richtlinien zur Bedarfsfreigabe:** *Vor dem Eingang der Lieferung*</span><span class="sxs-lookup"><span data-stu-id="d79f7-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="d79f7-136">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79f7-137">Das Setup im Inforegister **Planung** steuert, wie die Vorlage funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d79f7-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="d79f7-138">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-138">Set the following values:</span></span>

    - <span data-ttu-id="d79f7-139">**Bedarfsanforderungen:** *Keine*</span><span class="sxs-lookup"><span data-stu-id="d79f7-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="d79f7-140">Dieses Feld definiert die Anforderungen des Bedarfslagerbestands.</span><span class="sxs-lookup"><span data-stu-id="d79f7-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="d79f7-141">Wenn der Bedarf vor der Freigabe mit der Lieferung verknüpft werden muss, wählen Sie *Markierung* aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="d79f7-142">Wenn der Bedarf vor der Freigabe gegen die Lieferung reserviert werden muss, wählen Sie *Auftragsreservierung* aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="d79f7-143">**Lagerplatztyp:** *Versandorte*</span><span class="sxs-lookup"><span data-stu-id="d79f7-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="d79f7-144">In diesem Feld wird definiert, ob für die Crossdocking-Arbeit die Staging-/Ladeorte aus der Sendung oder ob Lagerplatzrichtlinien verwendet werden sollen, um eigene Staging-/Ladeorte zu finden.</span><span class="sxs-lookup"><span data-stu-id="d79f7-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="d79f7-145">**Arbeitsvorlage:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="d79f7-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="d79f7-146">Dieses Feld definiert die Arbeitsvorlage, die beim Erstellen von Crossdocking-Arbeiten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d79f7-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="d79f7-147">**Bei Eingang der Lieferung erneut validieren:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="d79f7-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="d79f7-148">Diese Option definiert, ob die Lieferung während des Eingangs erneut validiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d79f7-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="d79f7-149">Wenn diese Option auf *Ja* festgelegt ist, werden sowohl das maximale Zeitfenster als auch der Ablauftagebereich überprüft.</span><span class="sxs-lookup"><span data-stu-id="d79f7-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="d79f7-150">**Richtlinie Code** Lassen Sie dieses Feld leer</span><span class="sxs-lookup"><span data-stu-id="d79f7-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="d79f7-151">Mit dieser Option kann das System Lagerplatzrichtlinien verwenden, um den besten Lagerplatz zu bestimmen, an den der Bestand beim Cross-Docking gebracht werden soll.</span><span class="sxs-lookup"><span data-stu-id="d79f7-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="d79f7-152">Sie können sie festlegen, indem Sie jeder relevanten Cross-Docking-Vorlage einen Richtliniencode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="d79f7-153">Jeder Richtliniencode identifiziert eine eindeutige Lagerplatzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d79f7-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="d79f7-154">**Zeitfenster validieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d79f7-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="d79f7-155">Diese Option definiert, ob das maximale Zeitfenster ausgewertet werden soll, wenn eine Bezugsquelle ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d79f7-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="d79f7-156">Wenn diese Option auf *Ja* festgelegt ist, werden die Felder verfügbar, die sich auf das maximale und minimale Zeitfenster beziehen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="d79f7-157">**Maximales Zeitfenster:** *5*</span><span class="sxs-lookup"><span data-stu-id="d79f7-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="d79f7-158">Dieses Feld definiert den maximalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d79f7-159">**Maximale Zeitfenstereinheit:** *Tage*</span><span class="sxs-lookup"><span data-stu-id="d79f7-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d79f7-160">**Minimales Zeitfenster:** *0*</span><span class="sxs-lookup"><span data-stu-id="d79f7-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="d79f7-161">Dieses Feld definiert den minimalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d79f7-162">**Minimale Zeitfenstereinheit:** *Tage*</span><span class="sxs-lookup"><span data-stu-id="d79f7-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d79f7-163">**Ablauftagebereich:** *0*</span><span class="sxs-lookup"><span data-stu-id="d79f7-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="d79f7-164">*First Expiry First Out (FEFO)-Kriterien:* Dieses Feld definiert die maximale Anzahl von Tagen zwischen dem Ablaufdatum der ersten ablaufenden Charge, die sich derzeit im Lagerort befindet, und der Charge, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="d79f7-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="d79f7-165">Geben Sie im Inforegister **Bezugsquellen** die Liefertypen an, die für diese Vorlage gültig sind.</span><span class="sxs-lookup"><span data-stu-id="d79f7-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="d79f7-166">Wählen Sie **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d79f7-167">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79f7-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d79f7-168">**Bezugsquelle:** *Bestellung*</span><span class="sxs-lookup"><span data-stu-id="d79f7-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="d79f7-169">Eine Arbeitsklasse erstellen</span><span class="sxs-lookup"><span data-stu-id="d79f7-169">Create a work class</span></span>

1. <span data-ttu-id="d79f7-170">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d79f7-171">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsklasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="d79f7-172">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-172">Set the following values:</span></span>

    - <span data-ttu-id="d79f7-173">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79f7-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d79f7-174">**Beschreibung:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="d79f7-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="d79f7-175">**Arbeitsauftragstyp:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="d79f7-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="d79f7-176">Erstellen einer Arbeitsvorlage</span><span class="sxs-lookup"><span data-stu-id="d79f7-176">Create a work template</span></span>

1. <span data-ttu-id="d79f7-177">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d79f7-178">Legen Sie im Feld **Arbeitsauftragstyp** *Crossdocking* fest.</span><span class="sxs-lookup"><span data-stu-id="d79f7-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d79f7-179">Wählen Sie im Aktivitätsbereich **Neu** aus, um auf der Registerkarte **Übersicht** eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="d79f7-180">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-181">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79f7-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d79f7-182">**Arbeitsvorlage:** *51 Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="d79f7-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="d79f7-183">**Arbeitsvorlagenbeschreibung:** *51 Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="d79f7-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="d79f7-184">Wählen Sie **Speichern** aus, um das Inforegister **Arbeitsvorlagendetails** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d79f7-185">Wählen Sie im Inforegister **Arbeitsvorlagendetails** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79f7-186">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-187">**Arbeitstyp:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="d79f7-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d79f7-188">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79f7-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d79f7-189">Wählen Sie **Neu** aus, um eine weitere Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="d79f7-190">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="d79f7-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d79f7-191">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79f7-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d79f7-192">Wählen Sie **Speichern** aus, und bestätigen Sie, dass das Kontrollkästchen **Gültig** für die Vorlage *51 Crossdocking* ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="d79f7-193">Die Arbeitsklassen-IDs für die Arbeitstypen *Entnehmen* und *Einlagern* müssen gleich sein.</span><span class="sxs-lookup"><span data-stu-id="d79f7-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="d79f7-194">Lagerplatzrichtlinien erstellen</span><span class="sxs-lookup"><span data-stu-id="d79f7-194">Create location directives</span></span>

1. <span data-ttu-id="d79f7-195">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d79f7-196">Legen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Crossdocking* fest.</span><span class="sxs-lookup"><span data-stu-id="d79f7-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d79f7-197">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="d79f7-198">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79f7-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d79f7-199">**Name:** *51 Crossdocking einlagern*</span><span class="sxs-lookup"><span data-stu-id="d79f7-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="d79f7-200">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="d79f7-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d79f7-201">**Standort:** *5*</span><span class="sxs-lookup"><span data-stu-id="d79f7-201">**Site:** *5*</span></span>
    - <span data-ttu-id="d79f7-202">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79f7-203">Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d79f7-204">Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79f7-205">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-206">**Von Menge:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79f7-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d79f7-207">**Bis Menge:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d79f7-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="d79f7-208">Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d79f7-209">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79f7-210">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-211">**Name:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="d79f7-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="d79f7-212">**Feste Standortnutzung:** *Feste und nicht feste Lagerplätze*</span><span class="sxs-lookup"><span data-stu-id="d79f7-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="d79f7-213">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** in der Symbolleiste **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="d79f7-214">Wählen Sie **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="d79f7-215">Stellen Sie auf der Registerkarte **Bereich** sicher, dass die folgenden zwei Positionen konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="d79f7-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="d79f7-216">Position 1:</span><span class="sxs-lookup"><span data-stu-id="d79f7-216">Line 1:</span></span>

        - <span data-ttu-id="d79f7-217">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="d79f7-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d79f7-218">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="d79f7-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d79f7-219">**Feld:** *Lagerort*</span><span class="sxs-lookup"><span data-stu-id="d79f7-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="d79f7-220">**Kriterien:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="d79f7-221">Position 2:</span><span class="sxs-lookup"><span data-stu-id="d79f7-221">Line 2:</span></span>

        - <span data-ttu-id="d79f7-222">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="d79f7-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d79f7-223">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="d79f7-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d79f7-224">**Feld:** *Lagerplatz*</span><span class="sxs-lookup"><span data-stu-id="d79f7-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="d79f7-225">**Kriterien:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="d79f7-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="d79f7-226">Wählen Sie **OK** aus, um den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d79f7-227">Erstellen eines Menüelements für ein mobiles Geräts</span><span class="sxs-lookup"><span data-stu-id="d79f7-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d79f7-228">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d79f7-229">Wählen Sie in der Liste der Menüpunkte im linken Bereich die Option **Kaufeinlagerung** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="d79f7-230">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-230">Select **Edit**.</span></span>
1. <span data-ttu-id="d79f7-231">Wählen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79f7-232">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-233">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79f7-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d79f7-234">**Arbeitsauftragstyp:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="d79f7-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="d79f7-235">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d79f7-236">Szenario</span><span class="sxs-lookup"><span data-stu-id="d79f7-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d79f7-237">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="d79f7-237">Create a purchase order</span></span>

<span data-ttu-id="d79f7-238">Befolgen Sie diese Schritte, um eine Bestellung als Bezugsquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="d79f7-239">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d79f7-240">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d79f7-241">Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d79f7-242">**Kreditorenkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="d79f7-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d79f7-243">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79f7-244">Wählen Sie **OK** aus, und notieren Sie sich die Bestellnummer.</span><span class="sxs-lookup"><span data-stu-id="d79f7-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="d79f7-245">Im Inforegister **Bestellpositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d79f7-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d79f7-246">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-247">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="d79f7-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d79f7-248">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="d79f7-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="d79f7-249">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="d79f7-249">Create a sales order</span></span>

<span data-ttu-id="d79f7-250">Befolgen Sie diese Schritte, um einen Auftrag als Bedarfsquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="d79f7-251">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d79f7-252">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d79f7-253">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d79f7-254">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d79f7-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d79f7-255">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79f7-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79f7-256">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-256">Select **OK**.</span></span>
1. <span data-ttu-id="d79f7-257">Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d79f7-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d79f7-258">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="d79f7-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="d79f7-259">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="d79f7-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d79f7-260">**Menge** *3*</span><span class="sxs-lookup"><span data-stu-id="d79f7-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="d79f7-261">Geplantes Crossdocking erstellen</span><span class="sxs-lookup"><span data-stu-id="d79f7-261">Create planned cross-docking</span></span>

<span data-ttu-id="d79f7-262">Befolgen Sie diese Schritte, um das geplante Crossdocking aus dem Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="d79f7-263">Wählen Sie auf der Seite **Auftragsdetails** für den Auftrag, den Sie gerade erstellt haben, im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Aktivitäten** die Option **An Lager freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d79f7-264">Die Aktivität „An Lager freigeben“ erstellt eine Versand- und Ladeposition für die Auftragsposition und versucht, Lagerbestand zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="d79f7-265">Es wird eine Informationsnachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d79f7-265">You receive an informational message.</span></span> <span data-ttu-id="d79f7-266">Sie erhalten außerdem die folgende Warnmeldung: „Für Welle XXXX wurde keine Arbeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79f7-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="d79f7-267">Weitere Informationen finden Sie im Protokoll zum Arbeitserstellungsverlauf.“</span><span class="sxs-lookup"><span data-stu-id="d79f7-267">See the work creation history log for details."</span></span> <span data-ttu-id="d79f7-268">Dieses Verhalten wird erwartet, da sich kein Lagerbestand im Lagerort befindet.</span><span class="sxs-lookup"><span data-stu-id="d79f7-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="d79f7-269">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** die Option **Lieferdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="d79f7-270">Die Seite **Lieferdetails** wird angezeigt und zeigt die Lieferung, die für den Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d79f7-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="d79f7-271">Überprüfen Sie, ob im Inforegister **Ladungspositionen** das Feld **Geplante Crossdocking-Menge** auf *3* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="d79f7-272">Da im Lagerort kein Lagerbestand verfügbar war, aber innerhalb des in der Crossdocking-Vorlage definierten Zeitfensters eine gültige Bezugsquelle eintrifft, wurde die Crossdocking-Menge erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79f7-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="d79f7-273">Wählen Sie im Inforegister **Ladungspositionen** die Option **Geplantes Crossdocking** aus, um die Details des erstellten Crossdocking anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="d79f7-274">Crossdocking verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d79f7-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="d79f7-275">Bestelleingang mit der Warehouse Mobile App</span><span class="sxs-lookup"><span data-stu-id="d79f7-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="d79f7-276">Das System erhält die Menge von 5 aus der Bestellung an den Empfangsort und erstellt zwei Arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d79f7-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="d79f7-277">Die erste Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Crossdocking* und ist mit dem Auftrag verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d79f7-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="d79f7-278">Sie hat eine Menge von 3 und wird zum endgültigen Versandort geleitet, damit sie sofort versendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d79f7-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="d79f7-279">Die zweite Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Bestellungen* und ist mit der Bestellung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d79f7-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="d79f7-280">Sie hat die verbleibende Menge von 2, für die das Crossdocking nicht durchgeführt wurde und zur Einlagerung bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="d79f7-281">Melden Sie sich beim mobilen Gerät als ein Benutzer im Lagerort *51* an.</span><span class="sxs-lookup"><span data-stu-id="d79f7-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="d79f7-282">Gehen Sie zu **Eingehend \> Kaufempfang**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="d79f7-283">Geben Sie im Feld **PONum** Ihre Bestellnummer ein.</span><span class="sxs-lookup"><span data-stu-id="d79f7-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="d79f7-284">Geben Sie im Feld **Menge** den Wert *5* ein.</span><span class="sxs-lookup"><span data-stu-id="d79f7-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="d79f7-285">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-285">Select **OK**.</span></span>
1. <span data-ttu-id="d79f7-286">Legen Sie auf der nächsten Seite im Feld **Artikel** *A0001* fest.</span><span class="sxs-lookup"><span data-stu-id="d79f7-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="d79f7-287">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-287">Select **OK**.</span></span>
1. <span data-ttu-id="d79f7-288">Bestätigen Sie auf der nächsten Seite die Werte **PONum**, **Artikel** und **Menge**, indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="d79f7-289">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="d79f7-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d79f7-290">Wählen Sie **Abbrechen** aus, um zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d79f7-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="d79f7-291">Einlagerung zu Crossdocking und Bulk</span><span class="sxs-lookup"><span data-stu-id="d79f7-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="d79f7-292">Derzeit haben beide Arbeits-IDs das gleiche Zielkennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="d79f7-293">Um die nächsten Schritte ausführen zu können, müssen Sie die Arbeits-ID und die Zielkennzeichen-ID erhalten.</span><span class="sxs-lookup"><span data-stu-id="d79f7-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="d79f7-294">Sie können diese Informationen aus den Arbeitsdetails für die Bestellposition und die Auftragsposition abrufen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="d79f7-295">Alternativ können Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails** gehen und nach Arbeit filtern, wo der Wert von **Lagerort** *51* ist.</span><span class="sxs-lookup"><span data-stu-id="d79f7-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="d79f7-296">Gehen Sie auf dem mobilen Gerät zu **Eingehend \> Kaufeinlagerung**, und geben Sie das Zielkennzeichen von der Arbeit ein.</span><span class="sxs-lookup"><span data-stu-id="d79f7-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="d79f7-297">Geben Sie im Feld **ID** die Zielkennzeichen-ID aus den Arbeitsdetails ein.</span><span class="sxs-lookup"><span data-stu-id="d79f7-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="d79f7-298">Die Crossdocking-Auswahlseite zeigt den Kommissionierort (*RECV*), das Zielkennzeichen (*Kennzeichen*), den Artikel (*A0001*) und die Menge (*3*).</span><span class="sxs-lookup"><span data-stu-id="d79f7-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="d79f7-299">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-299">Select **OK**.</span></span>
1. <span data-ttu-id="d79f7-300">Geben Sie im Feld **Ziel-LP** ein Zielkennzeichen für die Kennzeichen-ID ein, die am Versandort eingelagert (Crossdocking) werden soll.</span><span class="sxs-lookup"><span data-stu-id="d79f7-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="d79f7-301">Sie können eine beliebige Kennzeichen-ID Ihrer Wahl auswählen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="d79f7-302">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-302">Select **OK**.</span></span>
1. <span data-ttu-id="d79f7-303">Geben Sie auf der nächsten Seite im Feld **ID** die Zielkennzeichen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="d79f7-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="d79f7-304">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-304">Select **OK**.</span></span>
1. <span data-ttu-id="d79f7-305">Bestätigen Sie die Arbeit zur Auswahl der verbleibenden Menge von 2, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d79f7-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="d79f7-306">Wählen Sie auf der nächsten Seite **Fertig** aus, um den Kommissioniervorgang zu beenden und den Einlagerungsprozess zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="d79f7-307">Die mobile App zeigt Ihnen den Lagerplatz und das Kennzeichen an, an dem Sie den Artikel ablegen möchten.</span><span class="sxs-lookup"><span data-stu-id="d79f7-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="d79f7-308">Bestätigen Sie den Bulk-Lagerplatz **Einlagern**, indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="d79f7-309">Bestätigen Sie auf der nächsten Seite das Crossdocking **Einlagern**, indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d79f7-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="d79f7-310">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="d79f7-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d79f7-311">Wählen Sie **Abbrechen** aus, um zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d79f7-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="d79f7-312">Die folgende Abbildung zeigt, wie die abgeschlossene Crossdocking-Arbeit in Microsoft Dynamics 365 Supply Chain Management aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="d79f7-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d79f7-313">![Crossdocking-Arbeit abgeschlossen](media/PlannedCrossDockingWork.png "Crossdocking-Arbeit abgeschlossen")</span><span class="sxs-lookup"><span data-stu-id="d79f7-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]