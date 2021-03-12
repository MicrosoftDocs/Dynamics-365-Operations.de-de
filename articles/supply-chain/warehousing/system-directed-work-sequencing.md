---
title: Systemgeleitete Arbeitsabfolgen
description: Dieses Thema enthält Informationen zu systemgeleiteten Arbeitsabfolgen. Mit dieser Funktion können Sie die Arbeitsaufträge sortieren und filtern, die das System den Benutzern zur Ausführung vorlegt. Dies ist hilfreich in Szenarien, in denen zusätzliche Kriterien erforderlich sind, um den Lagerkommissioniervorgang voranzutreiben.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3811486a31d079cac7f7c27ea6323f16de4478d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970205"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="984f1-105">Systemgeleitete Arbeitsabfolgen</span><span class="sxs-lookup"><span data-stu-id="984f1-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="984f1-106">Mit systemgeleiteten Arbeitsabfolgen können Sie die Arbeitsaufträge sortieren und filtern, die das System den Benutzern zur Ausführung vorlegt.</span><span class="sxs-lookup"><span data-stu-id="984f1-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="984f1-107">Dies ist hilfreich in Szenarien, in denen zusätzliche Kriterien (z. B. Versandzeitpunkt, Kommissionierzone, Lagerplatzprofil oder eine Kombination verschiedener Kriterien) erforderlich sind, um den Lagerkommissioniervorgang voranzutreiben.</span><span class="sxs-lookup"><span data-stu-id="984f1-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="984f1-108">Diese Funktionalität erweitert die aktuelle systemgeleitete Kommissionierfunktion um eine systemgeleitete Abfragereihenfolge, in der Benutzer eine Sequenz und eine oder mehrere Abfragen einrichten können, die alle erstellten Arbeitsaufträge auswerten.</span><span class="sxs-lookup"><span data-stu-id="984f1-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="984f1-109">Es werden nur Arbeitsaufträge erfasst und angezeigt, die die Kriterien erfüllen, die im Setup des Menüpunkts für mobile Geräte angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="984f1-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="984f1-110">Daher ermöglicht diese Funktionalität eine weitere Optimierung der Lagerkommissioniervorgänge, indem Arbeitsaufträge identifiziert werden, die den angegebenen Kriterien entsprechen, sie dem richtigen Menüpunkt für mobile Geräte zugewiesen und sie dann einem Mitarbeiter basierend auf bestimmten Fähigkeiten, Kommissioniergeräten oder einer anderen Anforderung präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="984f1-111">Wenn unterschiedliche Kriterien erforderlich sind, müssen mehrere Menüpunkte für Mobilgeräte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="984f1-112">Funktion für organisationsweite systemgeleitete Arbeitsabfolgen aktivieren</span><span class="sxs-lookup"><span data-stu-id="984f1-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="984f1-113">Bevor Sie die Funktion für systemgeleitete Arbeitsabfolgen verwenden können, muss sie in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="984f1-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="984f1-114">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="984f1-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="984f1-115">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="984f1-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="984f1-116">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="984f1-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="984f1-117">**Funktionsname:** *Organisationsweite systemgeleitete Arbeitsabfolgen*</span><span class="sxs-lookup"><span data-stu-id="984f1-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="984f1-118">Einstellung</span><span class="sxs-lookup"><span data-stu-id="984f1-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="984f1-119">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="984f1-119">Make demo data available</span></span>

<span data-ttu-id="984f1-120">Um das Szenario mithilfe der in diesem Thema dargestellten Werte zu bearbeiten, müssen Sie auf einem System arbeiten, auf dem die Standarddemodaten installiert sind.</span><span class="sxs-lookup"><span data-stu-id="984f1-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="984f1-121">Außerdem müssen Sie die **USMF** juristische Person auswählen.</span><span class="sxs-lookup"><span data-stu-id="984f1-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="984f1-122">Das Szenario verwendet Lagerort *51* aus den Demodaten.</span><span class="sxs-lookup"><span data-stu-id="984f1-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="984f1-123">Bevor Sie die Aufträge für den Lagerort freigeben, stellen Sie sicher, dass die Kommissionierstellen über genügend Lagerbestand für alle Artikel in den Aufträgen verfügen.</span><span class="sxs-lookup"><span data-stu-id="984f1-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="984f1-124">Standard-USMF-Daten sollten dieses Szenario unterstützen.</span><span class="sxs-lookup"><span data-stu-id="984f1-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="984f1-125">Wenn Sie keine Demodaten verwenden, überprüfen Sie die Einstellung **Lagerplatzrichtlinie**, um zu erfahren, welche Kommissionierorte für die Auftragskommissionierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="984f1-126">Wenn Sie den Lagerbestand anpassen müssen, können Sie manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow verwenden.</span><span class="sxs-lookup"><span data-stu-id="984f1-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="984f1-127">Menüpunkt für mobiles Gerät einrichten</span><span class="sxs-lookup"><span data-stu-id="984f1-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="984f1-128">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="984f1-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="984f1-129">Wählen Sie in der Liste der Menüpunkte für mobile Geräte die Option **Verkaufsauswahl – System** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="984f1-130">Der gewünschte Menüpunkt sollte bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="984f1-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="984f1-131">Überprüfen Sie die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="984f1-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="984f1-132">Im Inforegister **Allgemein** sollte das Feld **Geleitet von** auf *Systemgeleitet* festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="984f1-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="984f1-133">Das Inforegister **Arbeitsklassen** sollte die folgenden Einstellungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="984f1-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="984f1-134">Arbeitsklassenkennung</span><span class="sxs-lookup"><span data-stu-id="984f1-134">Work class ID</span></span> | <span data-ttu-id="984f1-135">Arbeitsauftragstyp</span><span class="sxs-lookup"><span data-stu-id="984f1-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="984f1-136">Verk.</span><span class="sxs-lookup"><span data-stu-id="984f1-136">Sales</span></span> | <span data-ttu-id="984f1-137">Aufträge</span><span class="sxs-lookup"><span data-stu-id="984f1-137">Sales orders</span></span> |
        | <span data-ttu-id="984f1-138">SO-Entnahme</span><span class="sxs-lookup"><span data-stu-id="984f1-138">SO Pick</span></span> | <span data-ttu-id="984f1-139">Aufträge</span><span class="sxs-lookup"><span data-stu-id="984f1-139">Sales orders</span></span> |

1. <span data-ttu-id="984f1-140">Wählen Sie im Aktivitätsbereich **Systemgeleitete Arbeitsabfolgeabfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="984f1-141">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-141">Select **Edit**.</span></span>
1. <span data-ttu-id="984f1-142">Löschen Sie die vorhandene Position, und bestätigen Sie die Aktivität durch Auswahl von **Ja**.</span><span class="sxs-lookup"><span data-stu-id="984f1-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="984f1-143">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="984f1-144">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="984f1-145">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="984f1-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="984f1-146">**Beschreibungsfeld:** *Arbeitsmenge unter 20 und absteigend*</span><span class="sxs-lookup"><span data-stu-id="984f1-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="984f1-147">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-147">Select **Save**.</span></span>
1. <span data-ttu-id="984f1-148">Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus</span><span class="sxs-lookup"><span data-stu-id="984f1-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="984f1-149">Erweitern Sie auf der Registerkarte **Verknüpfungen** die Verknüpfungshierarchie, um die Tabelle **Arbeitspositionen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="984f1-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="984f1-150">Wählen Sie die Tabellenverknüpfung **Arbeitspositionen** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="984f1-151">**Tabellen-Join hinzufügen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="984f1-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="984f1-152">Suchen Sie in der angezeigten Liste die Zeile mit den folgenden Einstellungen, und wählen Sie sie aus:</span><span class="sxs-lookup"><span data-stu-id="984f1-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="984f1-153">**Verknüpfungsmodus:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="984f1-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="984f1-154">**Beziehung:** *Lagerplätze (Lagerplatz)*</span><span class="sxs-lookup"><span data-stu-id="984f1-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="984f1-155">Wählen Sie **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="984f1-155">Select **Select**.</span></span>

    <span data-ttu-id="984f1-156">Lagerplätze werden der Tabellenverknüpfung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="984f1-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="984f1-157">Wählen Sie auf der Registerkarte **Sortieren** die Option **Hinzufügen** aus, um eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="984f1-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="984f1-158">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="984f1-159">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="984f1-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="984f1-160">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="984f1-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="984f1-161">**Feld:** *Arbeitsmenge* (Wählen Sie im angezeigten Meldungsfeld die Option **Ja** aus, um diesem Feld eine Sortierung hinzuzufügen.)</span><span class="sxs-lookup"><span data-stu-id="984f1-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="984f1-162">**Suchrichtung:** *Absteigend*</span><span class="sxs-lookup"><span data-stu-id="984f1-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="984f1-163">Wählen Sie die Registerkarte **Bereich**.</span><span class="sxs-lookup"><span data-stu-id="984f1-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="984f1-164">Wenn nur bestimmte Arbeitskriterien in die Abfolge einbezogen werden sollen, können Sie diese auf der Registerkarte **Bereich** angeben. In diesem Beispiel möchten Sie nur Arbeiten einbeziehen, bei denen die Menge weniger als 20 EA beträgt (die niedrigste Maßeinheit).</span><span class="sxs-lookup"><span data-stu-id="984f1-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="984f1-165">Beachten Sie, dass einige Positionen bereits enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="984f1-165">Notice that some lines are already included.</span></span> <span data-ttu-id="984f1-166">Diese Positionen sollten nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="984f1-167">Wählen Sie **Hinzufügen** aus, um eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="984f1-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="984f1-168">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="984f1-169">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="984f1-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="984f1-170">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="984f1-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="984f1-171">**Feld:** *Bestandsarbeitsmenge*</span><span class="sxs-lookup"><span data-stu-id="984f1-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="984f1-172">**Kriterien:** *\<20* (weniger als 20)</span><span class="sxs-lookup"><span data-stu-id="984f1-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="984f1-173">Wählen Sie **Hinzufügen** aus, um eine weitere Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="984f1-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="984f1-174">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="984f1-175">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="984f1-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="984f1-176">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="984f1-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="984f1-177">**Feld:** *Arbeitstyp*</span><span class="sxs-lookup"><span data-stu-id="984f1-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="984f1-178">**Kriterien:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="984f1-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="984f1-179">Wählen Sie **Hinzufügen** aus, um eine weitere Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="984f1-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="984f1-180">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="984f1-181">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="984f1-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="984f1-182">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="984f1-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="984f1-183">**Feld:** *Lagerortprofilkennung*</span><span class="sxs-lookup"><span data-stu-id="984f1-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="984f1-184">**Kriterien:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="984f1-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="984f1-185">Stellen Sie sicher, dass das Ausrufezeichen (*!*) vor *STAGE* steht.</span><span class="sxs-lookup"><span data-stu-id="984f1-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="984f1-186">Wählen Sie **OK** aus, um die Abfrage zu speichern und zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="984f1-187">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-187">Select **Save**.</span></span>
1. <span data-ttu-id="984f1-188">Schließen Sie die Seite, um zur Seite **Menüpunkte für mobile Geräte** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="984f1-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="984f1-189">Dieses Setup definiert die Kriterien, anhand derer berechtigte Arbeiten dem Menüpunkt für mobile Geräte zugeführt werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="984f1-190">Wenn Sie der Abfrage weitere Kriterienpositionen hinzufügen, verwendet das System zuerst die Abfrageposition mit der niedrigsten Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="984f1-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="984f1-191">Mit anderen Worten, alle berechtigten Arbeiten für Sequenznummer 1 werden dem Benutzer zuerst präsentiert, und dann alle Arbeiten für Sequenznummer 2.</span><span class="sxs-lookup"><span data-stu-id="984f1-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="984f1-192">Wenn ein bestimmter Bereich und eine bestimmte Sortierung zusammen verwendet werden müssen, sollten sie daher in derselben systemgeleiteten Arbeitsabfolgeabfrage angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="984f1-193">Dieses Setup erfasst alle Arbeiten mit mindestens einer Position, in der die Menge weniger als 20 EA beträgt.</span><span class="sxs-lookup"><span data-stu-id="984f1-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="984f1-194">Wenn die Arbeit eine Position hat, in der die Menge genau 20 EA oder mehr als 20 EA beträgt, ist sie gültig, vorausgesetzt, sie hat auch mindestens eine Position, in der die Menge weniger als 20 EA beträgt.</span><span class="sxs-lookup"><span data-stu-id="984f1-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="984f1-195">Lagerplatzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="984f1-195">Location directives</span></span>

<span data-ttu-id="984f1-196">Wenn Sie Standard-Contoso-Daten verwenden, sind für die Abfrage der Lagerplatzrichtlinienaktivität keine Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="984f1-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="984f1-197">Erstellen Sie jedoch eine neue Lagerplatzrichtlinie, um sicherzustellen, dass die Lagerplatzrichtlinien die Artikel in den Aufträgen erfassen, wenn Sie die Funktion in einer Nicht-Contoso-Umgebung anwenden.</span><span class="sxs-lookup"><span data-stu-id="984f1-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="984f1-198">Führen Sie die folgenden Schritte aus, um die Einstellungen in der Demoumgebung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="984f1-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="984f1-199">Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="984f1-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="984f1-200">Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="984f1-201">Wählen Sie die Lagerplatzrichtlinie namens *51 Entnahme* aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="984f1-202">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Position für die Aktivität **Entnahme** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="984f1-203">Wählen Sie **Abfrage bearbeiten** über dem Raster aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="984f1-204">Überprüfen Sie die Abfrage **Bereich**.</span><span class="sxs-lookup"><span data-stu-id="984f1-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="984f1-205">Suchen Sie die Position, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="984f1-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="984f1-206">Stellen Sie sicher, dass das Feld **Kriterien** leer ist (d. h., es gibt keine Einschränkungen).</span><span class="sxs-lookup"><span data-stu-id="984f1-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="984f1-207">Szenario</span><span class="sxs-lookup"><span data-stu-id="984f1-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="984f1-208">Auftragskommissionierarbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="984f1-208">Create sales order picking work</span></span>

<span data-ttu-id="984f1-209">Bevor eine systemgeleitete Kommissionierung ausgeführt wird, sollten einige ausgehende Arbeiten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="984f1-210">In diesem Szenario erstellen Sie vier Aufträge, die auf den angegebenen systemgeleiteten Arbeitsabfolgeabfragen basieren.</span><span class="sxs-lookup"><span data-stu-id="984f1-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="984f1-211">Sie reservieren Lagerbestandsmengen für jeden Auftrag.</span><span class="sxs-lookup"><span data-stu-id="984f1-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="984f1-212">Deshalb kann reservierter Lagerbestand nicht für andere Aufträge aus dem Lagerort entnommen werden, es sei denn, die gesamte Lagerreservierung oder ein Teil davon wird storniert.</span><span class="sxs-lookup"><span data-stu-id="984f1-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="984f1-213">Anschließend geben Sie jeden Auftrag für den Lagerort frei, um die ausgehende Arbeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="984f1-214">Auftrag 1</span><span class="sxs-lookup"><span data-stu-id="984f1-214">Sales order 1</span></span>

1. <span data-ttu-id="984f1-215">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="984f1-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="984f1-216">Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 1 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="984f1-217">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="984f1-218">Legen Sie im Abschnitt **Kunde** das Feld **Kundenkonto** auf *US-004* fest.</span><span class="sxs-lookup"><span data-stu-id="984f1-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="984f1-219">Legen Sie im Abschnitt **Allgemein** das Feld **Lagerort** auf *51* fest.</span><span class="sxs-lookup"><span data-stu-id="984f1-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="984f1-220">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="984f1-221">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="984f1-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="984f1-222">Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="984f1-223">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="984f1-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="984f1-224">**Menge** *20*</span><span class="sxs-lookup"><span data-stu-id="984f1-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="984f1-225">Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="984f1-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="984f1-226">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um den Bestand zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="984f1-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="984f1-227">Schließen Sie die Seite **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="984f1-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="984f1-228">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**, um Arbeit für den Lagerort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="984f1-229">Sie erhalten Informationsnachrichten mit der Wellen-ID und den Lieferungs-IDs, die für den Auftrag erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="984f1-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="984f1-230">Auftrag 2</span><span class="sxs-lookup"><span data-stu-id="984f1-230">Sales order 2</span></span>

1. <span data-ttu-id="984f1-231">Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 2 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="984f1-232">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="984f1-233">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="984f1-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="984f1-234">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="984f1-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="984f1-235">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="984f1-236">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="984f1-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="984f1-237">Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="984f1-238">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="984f1-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="984f1-239">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="984f1-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="984f1-240">Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="984f1-241">**Artikelnummer:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="984f1-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="984f1-242">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="984f1-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="984f1-243">Reservieren Sie Lagerbestand für beide Positionen.</span><span class="sxs-lookup"><span data-stu-id="984f1-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="984f1-244">Geben Sie den Auftrag für den Lagerort frei.</span><span class="sxs-lookup"><span data-stu-id="984f1-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="984f1-245">Auftrag 3</span><span class="sxs-lookup"><span data-stu-id="984f1-245">Sales order 3</span></span>

1. <span data-ttu-id="984f1-246">Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 3 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="984f1-247">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="984f1-248">**Debitorenkonto:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="984f1-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="984f1-249">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="984f1-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="984f1-250">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="984f1-251">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="984f1-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="984f1-252">Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="984f1-253">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="984f1-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="984f1-254">**Menge** *7*</span><span class="sxs-lookup"><span data-stu-id="984f1-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="984f1-255">Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="984f1-256">**Artikelnummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="984f1-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="984f1-257">**Menge** *8*</span><span class="sxs-lookup"><span data-stu-id="984f1-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="984f1-258">Reservieren Sie Lagerbestand für beide Positionen.</span><span class="sxs-lookup"><span data-stu-id="984f1-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="984f1-259">Geben Sie den Auftrag für den Lagerort frei.</span><span class="sxs-lookup"><span data-stu-id="984f1-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="984f1-260">Auftrag 4</span><span class="sxs-lookup"><span data-stu-id="984f1-260">Sales order 4</span></span>

1. <span data-ttu-id="984f1-261">Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 4 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="984f1-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="984f1-262">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="984f1-263">**Debitorenkonto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="984f1-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="984f1-264">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="984f1-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="984f1-265">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="984f1-266">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="984f1-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="984f1-267">Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="984f1-268">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="984f1-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="984f1-269">**Menge** *25*</span><span class="sxs-lookup"><span data-stu-id="984f1-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="984f1-270">Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="984f1-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="984f1-271">**Artikelnummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="984f1-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="984f1-272">**Menge** *10*</span><span class="sxs-lookup"><span data-stu-id="984f1-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="984f1-273">Reservieren Sie Lagerbestand für beide Positionen.</span><span class="sxs-lookup"><span data-stu-id="984f1-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="984f1-274">Geben Sie den Auftrag für den Lagerort frei.</span><span class="sxs-lookup"><span data-stu-id="984f1-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="984f1-275">Arbeits-IDs für die erstellte Arbeit abrufen</span><span class="sxs-lookup"><span data-stu-id="984f1-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="984f1-276">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="984f1-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="984f1-277">Filtern Sie das Feld **Lagerort**, sodass nur Arbeit für den Lagerort *51* gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="984f1-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="984f1-278">Es sollten vier Arbeits-IDs erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="984f1-278">Four work IDs should have been created.</span></span> <span data-ttu-id="984f1-279">Notieren Sie sich die Arbeits-ID für jeden Auftrag.</span><span class="sxs-lookup"><span data-stu-id="984f1-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="984f1-280">Auftragskennung</span><span class="sxs-lookup"><span data-stu-id="984f1-280">Sales order ID</span></span> | <span data-ttu-id="984f1-281">Arbeitskennung</span><span class="sxs-lookup"><span data-stu-id="984f1-281">Work ID</span></span> | <span data-ttu-id="984f1-282">Arbeitsmenge</span><span class="sxs-lookup"><span data-stu-id="984f1-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="984f1-283">Auftrag 1</span><span class="sxs-lookup"><span data-stu-id="984f1-283">Sales Order 1</span></span> | <span data-ttu-id="984f1-284">Arbeits-ID 1</span><span class="sxs-lookup"><span data-stu-id="984f1-284">Work ID 1</span></span> | <span data-ttu-id="984f1-285">20 EA</span><span class="sxs-lookup"><span data-stu-id="984f1-285">20 ea</span></span> |
    | <span data-ttu-id="984f1-286">Auftrag 2</span><span class="sxs-lookup"><span data-stu-id="984f1-286">Sales Order 2</span></span> | <span data-ttu-id="984f1-287">Arbeits-ID 2</span><span class="sxs-lookup"><span data-stu-id="984f1-287">Work ID 2</span></span> | <span data-ttu-id="984f1-288">6 EA (Summe beider Positionen)</span><span class="sxs-lookup"><span data-stu-id="984f1-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="984f1-289">Auftrag 3</span><span class="sxs-lookup"><span data-stu-id="984f1-289">Sales Order 3</span></span> | <span data-ttu-id="984f1-290">Arbeits-ID 3</span><span class="sxs-lookup"><span data-stu-id="984f1-290">Work ID 3</span></span> | <span data-ttu-id="984f1-291">15 EA (Summe beider Positionen)</span><span class="sxs-lookup"><span data-stu-id="984f1-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="984f1-292">Auftrag 4</span><span class="sxs-lookup"><span data-stu-id="984f1-292">Sales Order 4</span></span> | <span data-ttu-id="984f1-293">Arbeits-ID 4</span><span class="sxs-lookup"><span data-stu-id="984f1-293">Work ID 4</span></span> | <span data-ttu-id="984f1-294">35 EA (Summe beider Positionen)</span><span class="sxs-lookup"><span data-stu-id="984f1-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="984f1-295">Stellen Sie vor dem Ausführen des Flows auf dem mobilen Gerät sicher, dass sich nur die gerade erstellte Arbeit im Status *Öffnen* für Lagerort *51* und den Arbeitsauftragstyp *Auftrag* befindet.</span><span class="sxs-lookup"><span data-stu-id="984f1-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="984f1-296">Andernfalls können die Testergebnisse variieren, da die systemgeleitete Kommissionierung alle berechtigten Arbeiten umfasst.</span><span class="sxs-lookup"><span data-stu-id="984f1-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="984f1-297">Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Ausgehend \> Offene Verkaufsarbeit**.</span><span class="sxs-lookup"><span data-stu-id="984f1-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="984f1-298">Filtern Sie im Raster **Offene Verkaufsarbeit** das Feld **Lagerort**, sodass nur Arbeit für den Lagerort *51* gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="984f1-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="984f1-299">Stellen Sie sicher, dass nur die vier zuvor erstellten Arbeits-IDs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="984f1-300">Schließen Sie die Seite **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="984f1-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="984f1-301">Flowausführung für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="984f1-301">Mobile device flow execution</span></span>

<span data-ttu-id="984f1-302">Basierend auf dem Setup versorgt das System die Benutzerarbeit, die von der höchsten Arbeitspositionsmenge zur niedrigsten sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="984f1-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="984f1-303">Die Menge in jeder Position beträgt weniger als 20 EA.</span><span class="sxs-lookup"><span data-stu-id="984f1-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="984f1-304">Denken Sie daran, dass dieses Setup alle Arbeiten mit mindestens einer Position erfasst, in der die Menge weniger als 20 EA beträgt.</span><span class="sxs-lookup"><span data-stu-id="984f1-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="984f1-305">Wenn die Arbeit eine andere Position hat, in der die Menge genau 20 EA oder mehr als 20 EA beträgt, ist sie daher auch gültig.</span><span class="sxs-lookup"><span data-stu-id="984f1-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="984f1-306">Mobile App</span><span class="sxs-lookup"><span data-stu-id="984f1-306">Mobile app</span></span>

1. <span data-ttu-id="984f1-307">Melden Sie sich bei der Warehouse-App als ein Benutzer im Lagerort *51* an.</span><span class="sxs-lookup"><span data-stu-id="984f1-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="984f1-308">Gehen Sie zu **Ausgehend \> Verkaufsauswahl – System**.</span><span class="sxs-lookup"><span data-stu-id="984f1-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="984f1-309">Der Auswahlschritt für die Arbeits-ID *4* wird vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="984f1-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="984f1-310">Diese Arbeits-ID wird aufgrund des Setups der systemgeleiteten Abfragereihenfolge zuerst angezeigt, in der Sie angegeben haben, dass die Arbeit basierend auf der absteigenden Arbeitspositionsmenge sequenziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="984f1-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="984f1-311">Vervollständigen Sie die erforderliche Entnahme und Einlagerung, um die Arbeits-ID zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="984f1-312">Als Nächstes wird Arbeits-ID *3* vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="984f1-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="984f1-313">Eine der Arbeitspositionen befindet sich als Nächstes in der Sequenz, basierend auf der Arbeitspositionsmenge.</span><span class="sxs-lookup"><span data-stu-id="984f1-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="984f1-314">Vervollständigen Sie die Entnahme und Einlagerung, um die Arbeits-ID zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="984f1-315">Als Nächstes wird Arbeits-ID *2* vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="984f1-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="984f1-316">Die Auswahlposition dieser Arbeit folgt als Nächstes in der Sequenz.</span><span class="sxs-lookup"><span data-stu-id="984f1-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="984f1-317">Vervollständigen Sie die Entnahme und Einlagerung, um die Arbeits-ID zu schließen.</span><span class="sxs-lookup"><span data-stu-id="984f1-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="984f1-318">Es sollten Ihnen keine weiteren Arbeiten vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="984f1-318">No further work should be presented to you.</span></span> <span data-ttu-id="984f1-319">Arbeits-ID *1* ist für diesen Menüpunkt für mobile Geräte nicht berechtigt, da in der Abfrage angegeben wird, dass Arbeitskopfzeilen nur berücksichtigt werden, wenn die Menge in den Arbeitspositionen weniger als 20 EA beträgt.</span><span class="sxs-lookup"><span data-stu-id="984f1-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="984f1-320">Tipps</span><span class="sxs-lookup"><span data-stu-id="984f1-320">Tips</span></span>

<span data-ttu-id="984f1-321">Die systemgeleiteten Arbeitsabfolgeabfragen sind *inklusive*.</span><span class="sxs-lookup"><span data-stu-id="984f1-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="984f1-322">Es ist wichtig, dass Sie sich bei einigen Setups an diese Tatsache erinnern.</span><span class="sxs-lookup"><span data-stu-id="984f1-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="984f1-323">Sie möchten beispielsweise, dass ein bestimmter Menüpunkt Arbeit nur dort verarbeitet, wo sich die Arbeitseinheit *EA* befindet, und Sie geben diese Einschränkung auf der Registerkarte **Bereich** der Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="984f1-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="984f1-324">In diesem Fall werden alle Arbeiten, bei denen für mindestens eine Arbeitsposition die Arbeitseinheit auf *EA* festgelegt ist, dem Arbeiter zugeführt.</span><span class="sxs-lookup"><span data-stu-id="984f1-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="984f1-325">Daher kann diese Arbeit auch Arbeiten umfassen, bei denen Arbeitspositionen eine andere Arbeitseinheit als *EA* haben (wie *Kiste* oder *Palette*).</span><span class="sxs-lookup"><span data-stu-id="984f1-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="984f1-326">Die Abfrage schließt nur Arbeiten aus, bei denen für keine Arbeitsposition die Arbeitseinheit auf *EA* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="984f1-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="984f1-327">Daher wurde im Beispiel aus diesem Szenario die Arbeits-ID *4* auch von der Abfrage erfasst.</span><span class="sxs-lookup"><span data-stu-id="984f1-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="984f1-328">Bei der Erstellung wurden zwei Positionen hinzugefügt: eine für 25 EA und eine für 10 EA.</span><span class="sxs-lookup"><span data-stu-id="984f1-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="984f1-329">Die Arbeit wurde dem Benutzer weiterhin präsentiert, da mindestens eine Arbeitsposition eine Menge von weniger als 20 EA aufweist.</span><span class="sxs-lookup"><span data-stu-id="984f1-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="984f1-330">Je nach Szenario können Sie dieses Verhalten mithilfe von Arbeitspausen verhindern.</span><span class="sxs-lookup"><span data-stu-id="984f1-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
