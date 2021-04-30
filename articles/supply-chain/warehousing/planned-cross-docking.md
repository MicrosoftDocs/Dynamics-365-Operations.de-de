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
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911247"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="2079b-104">Geplantes Crossdocking</span><span class="sxs-lookup"><span data-stu-id="2079b-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2079b-105">In diesem Thema wird das erweiterte geplante Crossdocking beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2079b-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="2079b-106">Crossdocking ist ein Lagerortprozess, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2079b-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="2079b-107">Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.</span><span class="sxs-lookup"><span data-stu-id="2079b-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="2079b-108">Durch Crossdocking können Mitarbeiter eingehende Einlagerungen und ausgehende Kommissionierungen vom Lagerbestand überspringen, der bereits für eine ausgehende Bestellung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="2079b-109">Daher wird die Häufigkeit, mit der der Lagerbestand berührt wird, nach Möglichkeit minimiert.</span><span class="sxs-lookup"><span data-stu-id="2079b-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="2079b-110">Da weniger Interaktion mit dem System besteht, wird außerdem die Zeit- und Platzersparnis im Lagerortfertigungsbereich erhöht.</span><span class="sxs-lookup"><span data-stu-id="2079b-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="2079b-111">Bevor Sie Crossdocking ausführen können, müssen Sie eine neue Crossdocking-Vorlage konfigurieren, in der die Bezugsquelle und andere Anforderungen für das Crossdocking angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2079b-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="2079b-112">Beim Erstellen der ausgehenden Bestellung muss die Position mit einer eingehenden Bestellung markiert werden, die denselben Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="2079b-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="2079b-113">Sie können das Feld „Richtliniencode“ in der Crossdocking-Vorlage auswählen, ähnlich wie Sie Wiederbeschaffungen und Bestellungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="2079b-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="2079b-114">Zum Zeitpunkt des Eingangs eingehender Bestellungen erkennt das Crossdocking-Setup automatisch den Bedarf an Crossdocking und erstellt die Bewegungsarbeit für die erforderliche Menge basierend auf dem Setup der Lagerplatzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2079b-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="2079b-115">Lagerbuchungen sind *nicht* unregistriert, wenn Crossdocking-Arbeiten abgebrochen werden, auch wenn die Einstellung für diese Funktion in den Lagerortverwaltungsparametern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="2079b-116">Schalten Sie die Funktionen für das geplante Cross Docking ein</span><span class="sxs-lookup"><span data-stu-id="2079b-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="2079b-117">Wenn Ihr System nicht bereits die in diesem Thema beschriebenen Funktionen enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen in der folgenden Reihenfolge ein:</span><span class="sxs-lookup"><span data-stu-id="2079b-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="2079b-118">*Geplantes Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2079b-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="2079b-119">*Crossdockingvorlagen mit Lagerplatzrichtlinien*</span><span class="sxs-lookup"><span data-stu-id="2079b-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="2079b-120">Diese Funktion aktiviert das **Richtliniencode**, das in der Crossdocking-Vorlage angegeben werden soll, ähnlich wie Sie Wiederaufbauvorlagen einrichten.</span><span class="sxs-lookup"><span data-stu-id="2079b-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="2079b-121">Durch Aktivieren dieser Funktion können Sie keinen Richtliniencode in die Crossdocking-Arbeitsvorlagenzeilen für die letzte *Einlagern*-Zeile.</span><span class="sxs-lookup"><span data-stu-id="2079b-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="2079b-122">Dies stellt sicher, dass der endgültige Einlagerungsort während der Arbeitserstellung bestimmt werden kann, bevor Arbeitsvorlagen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="2079b-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="2079b-123">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2079b-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="2079b-124">Ladebuchungsmethoden erneut generieren</span><span class="sxs-lookup"><span data-stu-id="2079b-124">Regenerate load posting methods</span></span>

<span data-ttu-id="2079b-125">Das geplante Crossdocking wird als Ladebuchungsmethode implementiert.</span><span class="sxs-lookup"><span data-stu-id="2079b-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="2079b-126">Nachdem Sie die Funktion aktiviert haben, müssen Sie die Methoden erneut generieren.</span><span class="sxs-lookup"><span data-stu-id="2079b-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="2079b-127">Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Ladebuchungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="2079b-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="2079b-128">Wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="2079b-129">Wenn die Regeneration abgeschlossen ist, sollte eine Methode mit **Methodenname** im Wert von *planCrossDocking* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2079b-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="2079b-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2079b-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="2079b-131">Crossdocking-Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="2079b-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="2079b-132">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Crossdocking-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="2079b-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="2079b-133">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2079b-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="2079b-134">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="2079b-135">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="2079b-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="2079b-136">Dieses Feld definiert die Reihenfolge, in der Vorlagen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="2079b-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="2079b-137">**Crossdocking-Vorlagen-ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="2079b-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="2079b-138">**Beschreibung:** *Lagerort 51*</span><span class="sxs-lookup"><span data-stu-id="2079b-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="2079b-139">**Richtlinien zur Bedarfsfreigabe:** *Vor dem Eingang der Lieferung*</span><span class="sxs-lookup"><span data-stu-id="2079b-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="2079b-140">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2079b-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2079b-141">Das Setup im Inforegister **Planung** steuert, wie die Vorlage funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2079b-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="2079b-142">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-142">Set the following values:</span></span>

    - <span data-ttu-id="2079b-143">**Bedarfsanforderungen:** *Keine*</span><span class="sxs-lookup"><span data-stu-id="2079b-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="2079b-144">Dieses Feld definiert die Anforderungen des Bedarfslagerbestands.</span><span class="sxs-lookup"><span data-stu-id="2079b-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="2079b-145">Wenn der Bedarf vor der Freigabe mit der Lieferung verknüpft werden muss, wählen Sie *Markierung* aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="2079b-146">Wenn der Bedarf vor der Freigabe gegen die Lieferung reserviert werden muss, wählen Sie *Auftragsreservierung* aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="2079b-147">**Lagerplatztyp:** *Versandorte*</span><span class="sxs-lookup"><span data-stu-id="2079b-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="2079b-148">In diesem Feld wird definiert, ob für die Crossdocking-Arbeit die Staging-/Ladeorte aus der Sendung oder ob Lagerplatzrichtlinien verwendet werden sollen, um eigene Staging-/Ladeorte zu finden.</span><span class="sxs-lookup"><span data-stu-id="2079b-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="2079b-149">**Arbeitsvorlage:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="2079b-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="2079b-150">Dieses Feld definiert die Arbeitsvorlage, die beim Erstellen von Crossdocking-Arbeiten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2079b-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="2079b-151">**Bei Eingang der Lieferung erneut validieren:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="2079b-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="2079b-152">Diese Option definiert, ob die Lieferung während des Eingangs erneut validiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2079b-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="2079b-153">Wenn diese Option auf *Ja* festgelegt ist, werden sowohl das maximale Zeitfenster als auch der Ablauftagebereich überprüft.</span><span class="sxs-lookup"><span data-stu-id="2079b-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="2079b-154">**Richtliniencode:** Lassen Sie dieses Feld leer</span><span class="sxs-lookup"><span data-stu-id="2079b-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="2079b-155">Diese Option wird durch die Funktion *Crossdockingvorlagen mit Lagerplatzrichtlinien* aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2079b-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="2079b-156">Das System benutzt Lagerplatzrichtlinien, um den besten Lagerplatz zu bestimmen, an den der Bestand beim Crossdocking gebracht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2079b-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="2079b-157">Sie können sie festlegen, indem Sie jeder relevanten Cross-Docking-Vorlage einen Richtliniencode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2079b-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="2079b-158">Beachten Sie, dass bei festgelegtem Richtliniencode das System die Lagerplatzrichtlinie nach dem Richtliniencode sucht, wenn Arbeit erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2079b-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="2079b-159">Auf diese Weise können Sie Lagerplatzrichtlinien einschränken, die für eine bestimmte Crossdockingvorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2079b-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="2079b-160">**Zeitfenster validieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="2079b-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="2079b-161">Diese Option definiert, ob das maximale Zeitfenster ausgewertet werden soll, wenn eine Bezugsquelle ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2079b-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="2079b-162">Wenn diese Option auf *Ja* festgelegt ist, werden die Felder verfügbar, die sich auf das maximale und minimale Zeitfenster beziehen.</span><span class="sxs-lookup"><span data-stu-id="2079b-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="2079b-163">**Maximales Zeitfenster:** *5*</span><span class="sxs-lookup"><span data-stu-id="2079b-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="2079b-164">Dieses Feld definiert den maximalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="2079b-165">**Maximale Zeitfenstereinheit:** *Tage*</span><span class="sxs-lookup"><span data-stu-id="2079b-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="2079b-166">**Minimales Zeitfenster:** *0*</span><span class="sxs-lookup"><span data-stu-id="2079b-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="2079b-167">Dieses Feld definiert den minimalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="2079b-168">**Minimale Zeitfenstereinheit:** *Tage*</span><span class="sxs-lookup"><span data-stu-id="2079b-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="2079b-169">**Ablauftagebereich:** *0*</span><span class="sxs-lookup"><span data-stu-id="2079b-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="2079b-170">*First Expiry First Out (FEFO)-Kriterien:* Dieses Feld definiert die maximale Anzahl von Tagen zwischen dem Ablaufdatum der ersten ablaufenden Charge, die sich derzeit im Lagerort befindet, und der Charge, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2079b-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="2079b-171">Geben Sie im Inforegister **Bezugsquellen** die Liefertypen an, die für diese Vorlage gültig sind.</span><span class="sxs-lookup"><span data-stu-id="2079b-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="2079b-172">Wählen Sie **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2079b-173">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="2079b-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2079b-174">**Bezugsquelle:** *Bestellung*</span><span class="sxs-lookup"><span data-stu-id="2079b-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="2079b-175">Eine Arbeitsklasse erstellen</span><span class="sxs-lookup"><span data-stu-id="2079b-175">Create a work class</span></span>

1. <span data-ttu-id="2079b-176">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="2079b-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="2079b-177">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsklasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2079b-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="2079b-178">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-178">Set the following values:</span></span>

    - <span data-ttu-id="2079b-179">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2079b-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="2079b-180">**Beschreibung:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2079b-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="2079b-181">**Arbeitsauftragstyp:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2079b-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="2079b-182">Erstellen einer Arbeitsvorlage</span><span class="sxs-lookup"><span data-stu-id="2079b-182">Create a work template</span></span>

1. <span data-ttu-id="2079b-183">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="2079b-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="2079b-184">Legen Sie im Feld **Arbeitsauftragstyp** *Crossdocking* fest.</span><span class="sxs-lookup"><span data-stu-id="2079b-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="2079b-185">Wählen Sie im Aktivitätsbereich **Neu** aus, um auf der Registerkarte **Übersicht** eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2079b-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="2079b-186">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2079b-187">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="2079b-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2079b-188">**Arbeitsvorlage:** *51 Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2079b-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="2079b-189">**Arbeitsvorlagenbeschreibung:** *51 Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2079b-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="2079b-190">Wählen Sie **Speichern** aus, um das Inforegister **Arbeitsvorlagendetails** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2079b-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="2079b-191">Wählen Sie im Inforegister **Arbeitsvorlagendetails** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2079b-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2079b-192">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2079b-193">**Arbeitstyp:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="2079b-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="2079b-194">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2079b-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="2079b-195">Wählen Sie **Neu** aus, um eine weitere Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="2079b-196">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="2079b-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2079b-197">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2079b-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="2079b-198">Wählen Sie **Speichern** aus, und bestätigen Sie, dass das Kontrollkästchen **Gültig** für die Vorlage *51 Crossdocking* ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="2079b-199">Die Arbeitsklassen-IDs für die Arbeitstypen *Entnehmen* und *Einlagern* müssen gleich sein.</span><span class="sxs-lookup"><span data-stu-id="2079b-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="2079b-200">Lagerplatzrichtlinien erstellen</span><span class="sxs-lookup"><span data-stu-id="2079b-200">Create location directives</span></span>

1. <span data-ttu-id="2079b-201">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="2079b-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2079b-202">Legen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Crossdocking* fest.</span><span class="sxs-lookup"><span data-stu-id="2079b-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="2079b-203">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="2079b-204">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="2079b-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2079b-205">**Name:** *51 Crossdocking einlagern*</span><span class="sxs-lookup"><span data-stu-id="2079b-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="2079b-206">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="2079b-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2079b-207">**Standort:** *5*</span><span class="sxs-lookup"><span data-stu-id="2079b-207">**Site:** *5*</span></span>
    - <span data-ttu-id="2079b-208">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2079b-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2079b-209">Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2079b-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="2079b-210">Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2079b-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2079b-211">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2079b-212">**Von Menge:** *1*</span><span class="sxs-lookup"><span data-stu-id="2079b-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="2079b-213">**Bis Menge:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="2079b-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="2079b-214">Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2079b-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2079b-215">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2079b-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2079b-216">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2079b-217">**Name:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="2079b-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="2079b-218">**Feste Standortnutzung:** *Feste und nicht feste Lagerplätze*</span><span class="sxs-lookup"><span data-stu-id="2079b-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="2079b-219">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** in der Symbolleiste **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2079b-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="2079b-220">Wählen Sie **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2079b-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="2079b-221">Stellen Sie auf der Registerkarte **Bereich** sicher, dass die folgenden zwei Positionen konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="2079b-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="2079b-222">Position 1:</span><span class="sxs-lookup"><span data-stu-id="2079b-222">Line 1:</span></span>

        - <span data-ttu-id="2079b-223">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2079b-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="2079b-224">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2079b-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="2079b-225">**Feld:** *Lagerort*</span><span class="sxs-lookup"><span data-stu-id="2079b-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="2079b-226">**Kriterien:** *51*</span><span class="sxs-lookup"><span data-stu-id="2079b-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="2079b-227">Position 2:</span><span class="sxs-lookup"><span data-stu-id="2079b-227">Line 2:</span></span>

        - <span data-ttu-id="2079b-228">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2079b-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="2079b-229">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="2079b-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="2079b-230">**Feld:** *Lagerplatz*</span><span class="sxs-lookup"><span data-stu-id="2079b-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="2079b-231">**Kriterien:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="2079b-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="2079b-232">Wählen Sie **OK** aus, um den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2079b-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="2079b-233">Erstellen eines Menüelements für ein mobiles Geräts</span><span class="sxs-lookup"><span data-stu-id="2079b-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="2079b-234">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="2079b-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2079b-235">Wählen Sie in der Liste der Menüpunkte im linken Bereich die Option **Kaufeinlagerung** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="2079b-236">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-236">Select **Edit**.</span></span>
1. <span data-ttu-id="2079b-237">Wählen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2079b-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2079b-238">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2079b-239">**Arbeitsklassen-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2079b-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="2079b-240">**Arbeitsauftragstyp:** *Crossdocking*</span><span class="sxs-lookup"><span data-stu-id="2079b-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="2079b-241">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="2079b-242">Szenario</span><span class="sxs-lookup"><span data-stu-id="2079b-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="2079b-243">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="2079b-243">Create a purchase order</span></span>

<span data-ttu-id="2079b-244">Befolgen Sie diese Schritte, um eine Bestellung als Bezugsquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2079b-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="2079b-245">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="2079b-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="2079b-246">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2079b-247">Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2079b-248">**Kreditorenkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="2079b-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="2079b-249">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2079b-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2079b-250">Wählen Sie **OK** aus, und notieren Sie sich die Bestellnummer.</span><span class="sxs-lookup"><span data-stu-id="2079b-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="2079b-251">Im Inforegister **Bestellpositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2079b-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="2079b-252">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="2079b-253">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="2079b-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2079b-254">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="2079b-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="2079b-255">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="2079b-255">Create a sales order</span></span>

<span data-ttu-id="2079b-256">Befolgen Sie diese Schritte, um einen Auftrag als Bedarfsquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2079b-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="2079b-257">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="2079b-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2079b-258">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2079b-259">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2079b-260">**Debitorenkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="2079b-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="2079b-261">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="2079b-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2079b-262">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2079b-262">Select **OK**.</span></span>
1. <span data-ttu-id="2079b-263">Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2079b-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2079b-264">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="2079b-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="2079b-265">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="2079b-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2079b-266">**Menge** *3*</span><span class="sxs-lookup"><span data-stu-id="2079b-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="2079b-267">Geplantes Crossdocking erstellen</span><span class="sxs-lookup"><span data-stu-id="2079b-267">Create planned cross-docking</span></span>

<span data-ttu-id="2079b-268">Befolgen Sie diese Schritte, um das geplante Crossdocking aus dem Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2079b-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="2079b-269">Wählen Sie auf der Seite **Auftragsdetails** für den Auftrag, den Sie gerade erstellt haben, im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Aktivitäten** die Option **An Lager freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2079b-270">Die Aktivität „An Lager freigeben“ erstellt eine Versand- und Ladeposition für die Auftragsposition und versucht, Lagerbestand zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2079b-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="2079b-271">Es wird eine Informationsnachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2079b-271">You receive an informational message.</span></span> <span data-ttu-id="2079b-272">Sie erhalten außerdem die folgende Warnmeldung: „Für Welle XXXX wurde keine Arbeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="2079b-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="2079b-273">Weitere Informationen finden Sie im Protokoll zum Arbeitserstellungsverlauf.“</span><span class="sxs-lookup"><span data-stu-id="2079b-273">See the work creation history log for details."</span></span> <span data-ttu-id="2079b-274">Dieses Verhalten wird erwartet, da sich kein Lagerbestand im Lagerort befindet.</span><span class="sxs-lookup"><span data-stu-id="2079b-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="2079b-275">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** die Option **Lieferdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="2079b-276">Die Seite **Lieferdetails** wird angezeigt und zeigt die Lieferung, die für den Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2079b-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="2079b-277">Überprüfen Sie, ob im Inforegister **Ladungspositionen** das Feld **Geplante Crossdocking-Menge** auf *3* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="2079b-278">Da im Lagerort kein Lagerbestand verfügbar war, aber innerhalb des in der Crossdocking-Vorlage definierten Zeitfensters eine gültige Bezugsquelle eintrifft, wurde die Crossdocking-Menge erstellt.</span><span class="sxs-lookup"><span data-stu-id="2079b-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="2079b-279">Wählen Sie im Inforegister **Ladungspositionen** die Option **Geplantes Crossdocking** aus, um die Details des erstellten Crossdocking anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2079b-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="2079b-280">Crossdocking verarbeiten</span><span class="sxs-lookup"><span data-stu-id="2079b-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="2079b-281">Bestelleingang mit der Warehouse Mobile App</span><span class="sxs-lookup"><span data-stu-id="2079b-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="2079b-282">Das System erhält die Menge von 5 aus der Bestellung an den Empfangsort und erstellt zwei Arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2079b-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="2079b-283">Die erste Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Crossdocking* und ist mit dem Auftrag verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2079b-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="2079b-284">Sie hat eine Menge von 3 und wird zum endgültigen Versandort geleitet, damit sie sofort versendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2079b-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="2079b-285">Die zweite Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Bestellungen* und ist mit der Bestellung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2079b-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="2079b-286">Sie hat die verbleibende Menge von 2, für die das Crossdocking nicht durchgeführt wurde und zur Einlagerung bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="2079b-287">Melden Sie sich beim mobilen Gerät als ein Benutzer im Lagerort *51* an.</span><span class="sxs-lookup"><span data-stu-id="2079b-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="2079b-288">Gehen Sie zu **Eingehend \> Kaufempfang**.</span><span class="sxs-lookup"><span data-stu-id="2079b-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="2079b-289">Geben Sie im Feld **PONum** Ihre Bestellnummer ein.</span><span class="sxs-lookup"><span data-stu-id="2079b-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="2079b-290">Geben Sie im Feld **Menge** den Wert *5* ein.</span><span class="sxs-lookup"><span data-stu-id="2079b-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="2079b-291">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2079b-291">Select **OK**.</span></span>
1. <span data-ttu-id="2079b-292">Legen Sie auf der nächsten Seite im Feld **Artikel** *A0001* fest.</span><span class="sxs-lookup"><span data-stu-id="2079b-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="2079b-293">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2079b-293">Select **OK**.</span></span>
1. <span data-ttu-id="2079b-294">Bestätigen Sie auf der nächsten Seite die Werte **PONum**, **Artikel** und **Menge**, indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2079b-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="2079b-295">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="2079b-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2079b-296">Wählen Sie **Abbrechen** aus, um zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2079b-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="2079b-297">Einlagerung zu Crossdocking und Bulk</span><span class="sxs-lookup"><span data-stu-id="2079b-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="2079b-298">Derzeit haben beide Arbeits-IDs das gleiche Zielkennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2079b-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="2079b-299">Um die nächsten Schritte ausführen zu können, müssen Sie die Arbeits-ID und die Zielkennzeichen-ID erhalten.</span><span class="sxs-lookup"><span data-stu-id="2079b-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="2079b-300">Sie können diese Informationen aus den Arbeitsdetails für die Bestellposition und die Auftragsposition abrufen.</span><span class="sxs-lookup"><span data-stu-id="2079b-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="2079b-301">Alternativ können Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails** gehen und nach Arbeit filtern, wo der Wert von **Lagerort** *51* ist.</span><span class="sxs-lookup"><span data-stu-id="2079b-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="2079b-302">Gehen Sie auf dem mobilen Gerät zu **Eingehend \> Kaufeinlagerung**, und geben Sie das Zielkennzeichen von der Arbeit ein.</span><span class="sxs-lookup"><span data-stu-id="2079b-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="2079b-303">Geben Sie im Feld **ID** die Zielkennzeichen-ID aus den Arbeitsdetails ein.</span><span class="sxs-lookup"><span data-stu-id="2079b-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="2079b-304">Die Crossdocking-Auswahlseite zeigt den Kommissionierort (*RECV*), das Zielkennzeichen (*Kennzeichen*), den Artikel (*A0001*) und die Menge (*3*).</span><span class="sxs-lookup"><span data-stu-id="2079b-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="2079b-305">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2079b-305">Select **OK**.</span></span>
1. <span data-ttu-id="2079b-306">Geben Sie im Feld **Ziel-LP** ein Zielkennzeichen für die Kennzeichen-ID ein, die am Versandort eingelagert (Crossdocking) werden soll.</span><span class="sxs-lookup"><span data-stu-id="2079b-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="2079b-307">Sie können eine beliebige Kennzeichen-ID Ihrer Wahl auswählen.</span><span class="sxs-lookup"><span data-stu-id="2079b-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="2079b-308">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2079b-308">Select **OK**.</span></span>
1. <span data-ttu-id="2079b-309">Geben Sie auf der nächsten Seite im Feld **ID** die Zielkennzeichen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="2079b-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="2079b-310">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2079b-310">Select **OK**.</span></span>
1. <span data-ttu-id="2079b-311">Bestätigen Sie die Arbeit zur Auswahl der verbleibenden Menge von 2, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2079b-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="2079b-312">Wählen Sie auf der nächsten Seite **Fertig** aus, um den Kommissioniervorgang zu beenden und den Einlagerungsprozess zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="2079b-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="2079b-313">Die mobile App zeigt Ihnen den Lagerplatz und das Kennzeichen an, an dem Sie den Artikel ablegen möchten.</span><span class="sxs-lookup"><span data-stu-id="2079b-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="2079b-314">Bestätigen Sie den Bulk-Lagerplatz **Einlagern**, indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2079b-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="2079b-315">Bestätigen Sie auf der nächsten Seite das Crossdocking **Einlagern**, indem Sie **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2079b-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="2079b-316">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="2079b-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2079b-317">Wählen Sie **Abbrechen** aus, um zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2079b-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="2079b-318">Die folgende Abbildung zeigt, wie die abgeschlossene Crossdocking-Arbeit in Microsoft Dynamics 365 Supply Chain Management aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="2079b-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="2079b-319">![Crossdocking-Arbeit abgeschlossen](media/PlannedCrossDockingWork.png "Crossdocking-Arbeit abgeschlossen")</span><span class="sxs-lookup"><span data-stu-id="2079b-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]