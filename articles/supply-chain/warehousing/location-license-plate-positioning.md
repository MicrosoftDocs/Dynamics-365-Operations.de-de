---
title: Standortkennzeichenpositionierung
description: Durch die Standortkennzeichenpositionierung können Sie sehen, wo sich ein Kennzeichen an einem Ort mit mehreren Paletten befindet, z. B. an einem Ort, an dem doppelt tiefe Palettenregale verwendet werden.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: e5fd7a9a9703f9ab6802def0aac096e29aa04f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831385"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="27b37-103">Standortkennzeichenpositionierung</span><span class="sxs-lookup"><span data-stu-id="27b37-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27b37-104">Durch die Standortkennzeichenpositionierung können Sie sehen, wo sich ein Kennzeichen an einem Ort mit mehreren Paletten befindet, z. B. an einem Ort, an dem doppelt tiefe Palettenregale verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27b37-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="27b37-105">Die Funktion fügt jedem Kennzeichen, das an einem Lagerort abgelegt wird, eine Sequenznummer hinzu.</span><span class="sxs-lookup"><span data-stu-id="27b37-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="27b37-106">Diese Sequenznummer wird verwendet, um die Kennzeichen am Lagerort zu bestellen.</span><span class="sxs-lookup"><span data-stu-id="27b37-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="27b37-107">Daher unterstützt die Funktion auf intelligente Weise Szenarien, in denen Kunden ein Schwerkraft-Regalsystem verwenden und zu Kommissionierzwecken wissen müssen, welches Kennzeichen nach vorne zeigt.</span><span class="sxs-lookup"><span data-stu-id="27b37-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="27b37-108">In diesem Thema wird ein Szenario vorgestellt, in dem gezeigt wird, wie die Funktion eingerichtet und verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27b37-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="27b37-109">Funktion für Standortkennzeichenpositionierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="27b37-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="27b37-110">Bevor Sie die Standortkennzeichenpositionierung verwenden können, muss die Funktion in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="27b37-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="27b37-111">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27b37-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="27b37-112">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="27b37-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="27b37-113">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="27b37-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="27b37-114">**Funktionsname:** *Standortkennzeichenpositionierung*</span><span class="sxs-lookup"><span data-stu-id="27b37-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="27b37-115">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="27b37-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="27b37-116">Beispieldaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="27b37-116">Make sample data available</span></span>

<span data-ttu-id="27b37-117">Um dieses Szenario mit den hier vorgeschlagenen Werten zu bearbeiten, müssen Sie auf einem System arbeiten, auf dem Beispieldaten installiert sind.</span><span class="sxs-lookup"><span data-stu-id="27b37-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="27b37-118">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="27b37-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="27b37-119">Funktion für dieses Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="27b37-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="27b37-120">Führen Sie die folgenden Schritte aus, um die Funktion *Standortkennzeichenpositionierung* für das in diesem Thema vorgestellte Szenario einzurichten.</span><span class="sxs-lookup"><span data-stu-id="27b37-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="27b37-121">Lagerplatzprofile</span><span class="sxs-lookup"><span data-stu-id="27b37-121">Location profiles</span></span>

<span data-ttu-id="27b37-122">Die Funktion muss im Lagerplatzprofil für jeden Lagerplatz aktiviert sein, an dem sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27b37-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="27b37-123">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="27b37-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="27b37-124">Wählen Sie in der Liste der Lagerplatzprofile im linken Bereich **BULK-06** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="27b37-125">Im Inforegister **Allgemein** wurden zwei neue Optionen durch die Funktion hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="27b37-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="27b37-126">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="27b37-126">Set the following values:</span></span>

    - <span data-ttu-id="27b37-127">**Kennzeichenposition aktivieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="27b37-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="27b37-128">Wenn diese Option auf *Ja* eingestellt ist, wird die Kennzeichenposition für Kennzeichen am Lagerplatz beibehalten.</span><span class="sxs-lookup"><span data-stu-id="27b37-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="27b37-129">**LP-Position des Mobilgeräts anzeigen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="27b37-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="27b37-130">Wenn diese Option auf *Ja* eingestellt ist, wir die Kennzeichenposition den Benutzern mobiler Geräte während der Einstellung und Zählung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27b37-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="27b37-131">Sie können die Einstellung dieser Option nur ändern, wenn die Funktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27b37-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="27b37-132">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="27b37-133">Lagerplatzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="27b37-133">Location directives</span></span>

1. <span data-ttu-id="27b37-134">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="27b37-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="27b37-135">Stellen Sie im linken Bereich sicher, dass das Feld **Arbeitsauftragstyp** auf *Aufträge* eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="27b37-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="27b37-136">Wählen Sie in der Liste der Lagerplatzrichtlinien **61 SO Kommissionierreihenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="27b37-137">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="27b37-138">Wählen Sie im Inforegister **Positionen** die Position mit einer **Sequenznummer** im Wert von *2* aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="27b37-139">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Position mit einem **Namen** im Wert von *Entnahme für weniger als Palette* (es sollte die einzige Position sein) aus, und ändern Sie den Wert ihrer **Sequenznummer** auf *2*.</span><span class="sxs-lookup"><span data-stu-id="27b37-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="27b37-140">Wählen Sie **Neu** oberhalb des Rasters aus, um eine Position für eine neue Lagerplatzrichtlinienaktivität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="27b37-141">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="27b37-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27b37-142">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="27b37-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="27b37-143">**Name:** *Entnahmeposition 1*</span><span class="sxs-lookup"><span data-stu-id="27b37-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="27b37-144">Wählen Sie **Abfrage bearbeiten** über dem Gitter aus, während die neue Position noch ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="27b37-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="27b37-145">Wählen Sie im Abfrageeditor die Registerkarte **Verknüpfungen** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="27b37-146">Erweitern Sie die Tabellenverknüpfung **Lagerplätze**, um die Verknüpfung zur Tabelle **Lagerungsdimensionen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="27b37-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="27b37-147">Erweitern Sie die Tabellenverknüpfung **Lagerungsdimensionen**, um die Verknüpfung zur Tabelle **Verfügbarer Lagerbestand** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="27b37-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="27b37-148">Wählen Sie **Lagerungsdimensionen** und dann **Tabellenverknüpfung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="27b37-149">Wählen Sie in der Liste der angezeigten Tabellen in der Spalte **Beziehung** die Option **Kennzeichen (Kennzeichen)** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="27b37-150">Wählen Sie dann **Auswählen** aus, um **Kennzeichen** zur Tabellenverknüpfung **Lagerungsdimensionen** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="27b37-151">Während **Kennzeichen** noch ausgewählt ist, wählen Sie **Tabellenverknüpfung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="27b37-152">Wählen Sie in der Liste der angezeigten Tabellen in der Spalte **Beziehung** die Option **Standortkennzeichenpositionierung (Kennzeichen)** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="27b37-153">Wählen Sie dann **Auswählen** aus, um **Standortkennzeichenpositionierung** zur Tabellenverknüpfung **Lagerungsdimensionen** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="27b37-154">![Tabellenverknüpfungen](media/LpTableJoin.png "Tabellenverknüpfungen")</span><span class="sxs-lookup"><span data-stu-id="27b37-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="27b37-155">Wählen Sie **OK** aus, um die aktualisierten verknüpften Tabellen zu bestätigen und den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="27b37-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="27b37-156">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** erneut die Option **Abfrage bearbeiten** aus, um den Abfrageeditor erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="27b37-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="27b37-157">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="27b37-158">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="27b37-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27b37-159">**Tabelle:** *Standortkennzeichenpositionierung*</span><span class="sxs-lookup"><span data-stu-id="27b37-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="27b37-160">**Abgeleitete Tabelle:** *Standortkennzeichenpositionierung*</span><span class="sxs-lookup"><span data-stu-id="27b37-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="27b37-161">**Feld:** *LP-Position*</span><span class="sxs-lookup"><span data-stu-id="27b37-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="27b37-162">**Kriterien:** *1*</span><span class="sxs-lookup"><span data-stu-id="27b37-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="27b37-163">![Neuer Bereich](media/LpPositionCriteria.png "Neuer Bereich")</span><span class="sxs-lookup"><span data-stu-id="27b37-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="27b37-164">Wählen Sie **OK** aus, um Ihre Änderungen zu bestätigen und den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="27b37-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="27b37-165">Beispieldaten für dieses Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="27b37-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="27b37-166">In diesem Szenario muss sich der Benutzer bei der Warehouse Mobile App anmelden, indem er einen Mitarbeiter verwendet, der für Warehouse *61* eingerichtet ist, um die Arbeit durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="27b37-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="27b37-167">Der Benutzer muss auch Transaktionen abschließen.</span><span class="sxs-lookup"><span data-stu-id="27b37-167">The user must also complete transactions.</span></span>

<span data-ttu-id="27b37-168">Weil mit der Funktion *Standortkennzeichenpositionierung* ein neuer Bezeichner für Kennzeichenpositionen an einem Lagerplatz hinzugefügt wird, müssen Sie zuerst einige Daten erstellen, um das Szenario zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="27b37-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="27b37-169">Erste Lagerplatzinventur</span><span class="sxs-lookup"><span data-stu-id="27b37-169">Spot-count the first location</span></span>

1. <span data-ttu-id="27b37-170">Öffnen Sie die Warehouse Mobile App, und melden Sie sich bei Warehouse *61* an.</span><span class="sxs-lookup"><span data-stu-id="27b37-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="27b37-171">Gehen Sie zu **Lagerbestand \> Lagerplatzinventur**.</span><span class="sxs-lookup"><span data-stu-id="27b37-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="27b37-172">Legen Sie auf der Seite **Lagerplatzinventur** das Feld **Lagerplatz** auf *01A01R1S1B* fest.</span><span class="sxs-lookup"><span data-stu-id="27b37-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="27b37-173">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-173">Select **OK**.</span></span>

    <span data-ttu-id="27b37-174">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-174">The page shows the location that you entered.</span></span> <span data-ttu-id="27b37-175">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="27b37-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="27b37-176">Wählen Sie **Aktualisieren** aus, um eine Zählung am Lagerplatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="27b37-177">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0001* ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="27b37-178">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-178">Select **OK**.</span></span>
1. <span data-ttu-id="27b37-179">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1001* (oder eine andere Kennzeichennummer Ihrer Wahl) ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="27b37-180">Die Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** zeigt **Kennzeichenposition 1** an.</span><span class="sxs-lookup"><span data-stu-id="27b37-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="27b37-181">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-181">Select **OK**.</span></span>

    <span data-ttu-id="27b37-182">Sie müssen nun die Menge des Artikels angeben, die auf dem Kennzeichen gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="27b37-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="27b37-183">Legen Sie das Feld **Menge** auf *10* fest.</span><span class="sxs-lookup"><span data-stu-id="27b37-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="27b37-184">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-184">Select **OK**.</span></span>

    <span data-ttu-id="27b37-185">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-185">The page shows the location that you entered.</span></span> <span data-ttu-id="27b37-186">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="27b37-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="27b37-187">Wählen Sie **Aktualisieren** aus, um eine weitere Zählung am Lagerplatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="27b37-188">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0002* ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="27b37-189">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-189">Select **OK**.</span></span>
1. <span data-ttu-id="27b37-190">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1002* (oder eine andere Kennzeichennummer Ihrer Wahl, sofern sie von der zuvor angegebenen Kennzeichennummer abweicht) ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="27b37-191">Ändern Sie die Kennzeichenposition durch Einstellen des Felds **LP-Position** auf *2*.</span><span class="sxs-lookup"><span data-stu-id="27b37-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="27b37-192">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-192">Select **OK**.</span></span>
1. <span data-ttu-id="27b37-193">Geben Sie die Menge des Artikels an, die auf dem Kennzeichen gezählt wird, indem Sie das Feld **Menge** auf *10* festlegen.</span><span class="sxs-lookup"><span data-stu-id="27b37-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="27b37-194">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-194">Select **OK**.</span></span>

    <span data-ttu-id="27b37-195">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-195">The page shows the location that you entered.</span></span> <span data-ttu-id="27b37-196">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="27b37-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="27b37-197">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-197">Select **OK**.</span></span>

<span data-ttu-id="27b37-198">Die Arbeit ist jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="27b37-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="27b37-199">Zweite Lagerplatzinventur</span><span class="sxs-lookup"><span data-stu-id="27b37-199">Spot-count the second location</span></span>

1. <span data-ttu-id="27b37-200">Legen Sie auf der Seite **Lagerplatzinventur** das Feld **Lagerplatz** auf *01A01R1S2B* fest.</span><span class="sxs-lookup"><span data-stu-id="27b37-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="27b37-201">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-201">Select **OK**.</span></span>

    <span data-ttu-id="27b37-202">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-202">The page shows the location that you entered.</span></span> <span data-ttu-id="27b37-203">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="27b37-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="27b37-204">Wählen Sie **Aktualisieren** aus, um eine Zählung am Lagerplatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="27b37-205">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0002* ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="27b37-206">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-206">Select **OK**.</span></span>
1. <span data-ttu-id="27b37-207">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1003* (oder eine andere Kennzeichennummer Ihrer Wahl, sofern sie von den beiden im vorherigen Verfahren angegebenen Kennzeichennummern abweicht) ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="27b37-208">Die Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** zeigt **Kennzeichenposition 1** an.</span><span class="sxs-lookup"><span data-stu-id="27b37-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="27b37-209">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-209">Select **OK**.</span></span>
1. <span data-ttu-id="27b37-210">Geben Sie die Menge des Artikels an, die auf dem Kennzeichen gezählt wird, indem Sie das Feld **Menge** auf *10* festlegen.</span><span class="sxs-lookup"><span data-stu-id="27b37-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="27b37-211">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-211">Select **OK**.</span></span>

    <span data-ttu-id="27b37-212">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-212">The page shows the location that you entered.</span></span> <span data-ttu-id="27b37-213">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="27b37-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="27b37-214">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-214">Select **OK**.</span></span>

<span data-ttu-id="27b37-215">Die Arbeit ist jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="27b37-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="27b37-216">Arbeitsdetails</span><span class="sxs-lookup"><span data-stu-id="27b37-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="27b37-217">Lagerplatzinventuren aus der mobilen App erstellen Zykluszählarbeit in Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="27b37-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="27b37-218">Die Arbeit erfordert, dass die Zählungen akzeptiert werden, bevor sie in den Lagerbestand gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="27b37-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="27b37-219">Melden Sie sich bei Dynamics 365 Supply Chain Management an.</span><span class="sxs-lookup"><span data-stu-id="27b37-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="27b37-220">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="27b37-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="27b37-221">Suchen Sie auf der Registerkarte **Überblick** nach Positionen mit den folgenden Werten:</span><span class="sxs-lookup"><span data-stu-id="27b37-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="27b37-222">**Arbeitsauftragstyp:** *Zykluszählung*</span><span class="sxs-lookup"><span data-stu-id="27b37-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="27b37-223">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="27b37-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="27b37-224">**Arbeitsstatus:** *Überprüfung ausstehend*</span><span class="sxs-lookup"><span data-stu-id="27b37-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="27b37-225">Für diese Positionen sollten zwei Arbeits-IDs erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="27b37-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="27b37-226">Die Zählungen für diese beiden Arbeits-IDs müssen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="27b37-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="27b37-227">Wählen Sie im Raster die erste Arbeits-ID für den Arbeitsauftragstyp *Zykluszählung* aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="27b37-228">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Zykluszählung** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="27b37-229">Es werden zwei Positionen angezeigt, eine für jeden Artikel und jedes Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="27b37-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="27b37-230">Die Werte in den Feldern **Gezählte Menge**, **Lagerplatz**, **Kennzeichen** und **Artikel** sollten mit den Zähleinträgen übereinstimmen, die Sie auf dem mobilen Gerät erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="27b37-231">Wenn eines dieser Felder nicht sichtbar ist, wählen Sie im Aktivitätsbereich **Dimensionen anzeigen** aus, um sie dem Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27b37-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="27b37-232">Wählen Sie beide Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-232">Select both lines.</span></span>
1. <span data-ttu-id="27b37-233">Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.</span><span class="sxs-lookup"><span data-stu-id="27b37-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="27b37-234">Sie erhalten eine Nachricht „Buchung – Erfassung“.</span><span class="sxs-lookup"><span data-stu-id="27b37-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="27b37-235">Wählen Sie **Nachrichtendetails** aus, um die gebuchte Erfassungsnummer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="27b37-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="27b37-236">Schließen Sie die Nachrichtendetails.</span><span class="sxs-lookup"><span data-stu-id="27b37-236">Close the message details.</span></span>
1. <span data-ttu-id="27b37-237">Aktualisieren Sie die Seite **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="27b37-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="27b37-238">Die erste Arbeits-ID wurde geschlossen und wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27b37-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="27b37-239">Um geschlossene Arbeiten anzuzeigen, aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** über dem Raster.</span><span class="sxs-lookup"><span data-stu-id="27b37-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="27b37-240">Sie akzeptieren nun die Arbeit für das Kennzeichen im Lagerplatz *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="27b37-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="27b37-241">Wählen Sie auf der Registerkarte **Übersicht** die zweite Arbeits-ID für den Arbeitsauftragstyp *Zykluszählung* aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="27b37-242">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Zykluszählung** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="27b37-243">Für den Artikel und das Kennzeichen wird eine Position angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27b37-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="27b37-244">Die Werte in den Feldern **Gezählte Menge**, **Lagerplatz**, **Kennzeichen** und **Artikel** sollten mit den Zähleinträgen übereinstimmen, die Sie auf dem mobilen Gerät erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="27b37-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="27b37-245">Wählen Sie die Position aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-245">Select the line.</span></span>
1. <span data-ttu-id="27b37-246">Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.</span><span class="sxs-lookup"><span data-stu-id="27b37-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="27b37-247">Sie erhalten eine Nachricht „Buchung – Erfassung“.</span><span class="sxs-lookup"><span data-stu-id="27b37-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="27b37-248">Wählen Sie **Nachrichtendetails** aus, um die gebuchte Erfassungsnummer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="27b37-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="27b37-249">Schließen Sie die Nachrichtendetails.</span><span class="sxs-lookup"><span data-stu-id="27b37-249">Close the message details.</span></span>
1. <span data-ttu-id="27b37-250">Aktualisieren Sie die Seite **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="27b37-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="27b37-251">Die zweite Arbeits-ID wurde geschlossen und wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27b37-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="27b37-252">Um geschlossene Arbeiten anzuzeigen, aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** über dem Raster.</span><span class="sxs-lookup"><span data-stu-id="27b37-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="27b37-253">Verfügbarer Lagerbestand nach Lagerplatz</span><span class="sxs-lookup"><span data-stu-id="27b37-253">On-hand by location</span></span>

1. <span data-ttu-id="27b37-254">Wechseln Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Verfügbarer Lagerbestand nach Lagerplatz**.</span><span class="sxs-lookup"><span data-stu-id="27b37-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="27b37-255">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="27b37-255">Set the following values:</span></span>

    - <span data-ttu-id="27b37-256">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="27b37-256">**Site:** *6*</span></span>
    - <span data-ttu-id="27b37-257">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="27b37-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="27b37-258">**Standortübergreifend aktualisieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="27b37-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="27b37-259">Beachten Sie, dass der Lagerplatz *01A01R1S1B* zwei Kennzeichen hat:</span><span class="sxs-lookup"><span data-stu-id="27b37-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="27b37-260">**A0001**, bei dem das Feld **LP-Position** auf *1* festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="27b37-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="27b37-261">**A0002**, bei dem das Feld **LP-Position** auf *2* festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="27b37-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="27b37-262">Beachten Sie, dass der Lagerplatz *01A01R1S2B* ein Kennzeichen hat:</span><span class="sxs-lookup"><span data-stu-id="27b37-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="27b37-263">**A0002**, bei dem das Feld **LP-Position** auf *1* festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="27b37-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="27b37-264">Szenario für Aufträge</span><span class="sxs-lookup"><span data-stu-id="27b37-264">Sales order scenario</span></span>

<span data-ttu-id="27b37-265">Nun, da die Funktion *Standortkennzeichenpositionierung* eingerichtet und der Lagerbestand bereitgestellt wurde, müssen Sie einen Auftrag erstellen, um Kommissionierarbeiten zu generieren, die den Lagerarbeiter anweisen, Artikel *A0002* vom Lagerort zu kommissionieren, an dem sich die Paletten-ID an Position *1* befindet.</span><span class="sxs-lookup"><span data-stu-id="27b37-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="27b37-266">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="27b37-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="27b37-267">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="27b37-268">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="27b37-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="27b37-269">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="27b37-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="27b37-270">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="27b37-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="27b37-271">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27b37-271">Select **OK**.</span></span>
1. <span data-ttu-id="27b37-272">Dem Raster im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="27b37-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="27b37-273">Legen Sie die folgenden Werte für diese neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="27b37-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="27b37-274">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="27b37-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="27b37-275">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="27b37-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="27b37-276">Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="27b37-277">Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um Lagerbestand für die Auftragsposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="27b37-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="27b37-278">Schließen Sie die Seite **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="27b37-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="27b37-279">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="27b37-280">Sie erhalten eine Informationsnachricht mit der Wellen-ID und der Lieferungs-ID, die für den Auftrag erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="27b37-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="27b37-281">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** über dem Raster die Option **Arbeitsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="27b37-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="27b37-282">Die Seite **Arbeit** wird angezeigt und zeigt die Arbeit, die für die Verkaufsposition erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="27b37-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="27b37-283">Notieren Sie sich die angezeigte Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="27b37-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="27b37-284">Verkaufsauswahlszenario</span><span class="sxs-lookup"><span data-stu-id="27b37-284">Sales picking scenario</span></span>

1. <span data-ttu-id="27b37-285">Öffnen Sie die mobile App, und melden Sie sich bei Warehouse *61* an.</span><span class="sxs-lookup"><span data-stu-id="27b37-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="27b37-286">Gehen Sie zu **Ausgehend \> Verkaufsauswahl**.</span><span class="sxs-lookup"><span data-stu-id="27b37-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="27b37-287">Wählen Sie auf der Seite **Arbeits-/Kennzeichen-ID scannen** das Feld **ID** aus, und geben Sie dann die Arbeits-ID aus der Verkaufsposition ein.</span><span class="sxs-lookup"><span data-stu-id="27b37-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="27b37-288">Beachten Sie, dass Sie bei der Kommissionierung angewiesen werden, den Artikel *A0002* vom Lagerplatz *01A01R1S2B* zu kommissionieren.</span><span class="sxs-lookup"><span data-stu-id="27b37-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="27b37-289">Sie erhalten diese Anweisung, weil sich Artikel *A0002* auf einem Kennzeichen befindet, das in Position *1* an diesem Lagerplatz ist.</span><span class="sxs-lookup"><span data-stu-id="27b37-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="27b37-290">![Lagerplatz Position 1](media/LocationLicensePlatePositioning.png "Lagerplatz Position 1")</span><span class="sxs-lookup"><span data-stu-id="27b37-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="27b37-291">Geben Sie die Kennzeichen-ID ein, die Sie für den Lagerplatz erstellt haben, und befolgen Sie die Anweisungen, um den Auftrag auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="27b37-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]