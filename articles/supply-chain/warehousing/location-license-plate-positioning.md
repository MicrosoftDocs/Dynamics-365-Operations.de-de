---
title: Standortkennzeichenpositionierung
description: Durch die Standortkennzeichenpositionierung können Sie sehen, wo sich ein Kennzeichen an einem Ort mit mehreren Paletten befindet, z. B. an einem Ort, an dem doppelt tiefe Palettenregale verwendet werden.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6810753c10d03999c38a6163687effd771076c15
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530051"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="b7692-103">Standortkennzeichenpositionierung</span><span class="sxs-lookup"><span data-stu-id="b7692-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7692-104">Durch die Standortkennzeichenpositionierung können Sie sehen, wo sich ein Kennzeichen an einem Ort mit mehreren Paletten befindet, z. B. an einem Ort, an dem doppelt tiefe Palettenregale verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7692-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="b7692-105">Die Funktion fügt jedem Kennzeichen, das an einem Lagerort abgelegt wird, eine Sequenznummer hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7692-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="b7692-106">Diese Sequenznummer wird verwendet, um die Kennzeichen am Lagerort zu bestellen.</span><span class="sxs-lookup"><span data-stu-id="b7692-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="b7692-107">Daher unterstützt die Funktion auf intelligente Weise Szenarien, in denen Kunden ein Schwerkraft-Regalsystem verwenden und zu Kommissionierzwecken wissen müssen, welches Kennzeichen nach vorne zeigt.</span><span class="sxs-lookup"><span data-stu-id="b7692-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="b7692-108">In diesem Thema wird ein Szenario vorgestellt, in dem gezeigt wird, wie die Funktion eingerichtet und verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7692-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="b7692-109">Funktion für Standortkennzeichenpositionierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="b7692-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="b7692-110">Bevor Sie die Standortkennzeichenpositionierung verwenden können, muss die Funktion in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="b7692-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="b7692-111">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b7692-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b7692-112">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="b7692-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b7692-113">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="b7692-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b7692-114">**Funktionsname:** *Standortkennzeichenpositionierung*</span><span class="sxs-lookup"><span data-stu-id="b7692-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b7692-115">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="b7692-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="b7692-116">Beispieldaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="b7692-116">Make sample data available</span></span>

<span data-ttu-id="b7692-117">Um dieses Szenario mit den hier vorgeschlagenen Werten zu bearbeiten, müssen Sie auf einem System arbeiten, auf dem Beispieldaten installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b7692-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="b7692-118">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="b7692-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="b7692-119">Funktion für dieses Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="b7692-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="b7692-120">Führen Sie die folgenden Schritte aus, um die Funktion *Standortkennzeichenpositionierung* für das in diesem Thema vorgestellte Szenario einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b7692-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="b7692-121">Lagerplatzprofile</span><span class="sxs-lookup"><span data-stu-id="b7692-121">Location profiles</span></span>

<span data-ttu-id="b7692-122">Die Funktion muss im Lagerplatzprofil für jeden Lagerplatz aktiviert sein, an dem sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7692-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="b7692-123">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="b7692-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b7692-124">Wählen Sie in der Liste der Lagerplatzprofile im linken Bereich **BULK-06** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="b7692-125">Im Inforegister **Allgemein** wurden zwei neue Optionen durch die Funktion hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7692-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="b7692-126">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b7692-126">Set the following values:</span></span>

    - <span data-ttu-id="b7692-127">**Kennzeichenposition aktivieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b7692-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="b7692-128">Wenn diese Option auf *Ja* eingestellt ist, wird die Kennzeichenposition für Kennzeichen am Lagerplatz beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b7692-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="b7692-129">**LP-Position des Mobilgeräts anzeigen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b7692-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="b7692-130">Wenn diese Option auf *Ja* eingestellt ist, wir die Kennzeichenposition den Benutzern mobiler Geräte während der Einstellung und Zählung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7692-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="b7692-131">Sie können die Einstellung dieser Option nur ändern, wenn die Funktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b7692-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="b7692-132">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="b7692-133">Lagerplatzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="b7692-133">Location directives</span></span>

1. <span data-ttu-id="b7692-134">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="b7692-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b7692-135">Stellen Sie im linken Bereich sicher, dass das Feld **Arbeitsauftragstyp** auf *Aufträge* eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="b7692-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="b7692-136">Wählen Sie in der Liste der Lagerplatzrichtlinien **61 SO Kommissionierreihenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="b7692-137">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b7692-138">Wählen Sie im Inforegister **Positionen** die Position mit einer **Sequenznummer** im Wert von *2* aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="b7692-139">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Position mit einem **Namen** im Wert von *Entnahme für weniger als Palette* (es sollte die einzige Position sein) aus, und ändern Sie den Wert ihrer **Sequenznummer** auf *2*.</span><span class="sxs-lookup"><span data-stu-id="b7692-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="b7692-140">Wählen Sie **Neu** oberhalb des Rasters aus, um eine Position für eine neue Lagerplatzrichtlinienaktivität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="b7692-141">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="b7692-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b7692-142">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="b7692-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b7692-143">**Name:** *Entnahmeposition 1*</span><span class="sxs-lookup"><span data-stu-id="b7692-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="b7692-144">Wählen Sie **Abfrage bearbeiten** über dem Gitter aus, während die neue Position noch ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b7692-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="b7692-145">Wählen Sie im Abfrageeditor die Registerkarte **Verknüpfungen** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="b7692-146">Erweitern Sie die Tabellenverknüpfung **Lagerplätze**, um die Verknüpfung zur Tabelle **Lagerungsdimensionen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7692-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="b7692-147">Erweitern Sie die Tabellenverknüpfung **Lagerungsdimensionen**, um die Verknüpfung zur Tabelle **Verfügbarer Lagerbestand** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7692-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="b7692-148">Wählen Sie **Lagerungsdimensionen** und dann **Tabellenverknüpfung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="b7692-149">Wählen Sie in der Liste der angezeigten Tabellen in der Spalte **Beziehung** die Option **Kennzeichen (Kennzeichen)** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="b7692-150">Wählen Sie dann **Auswählen** aus, um **Kennzeichen** zur Tabellenverknüpfung **Lagerungsdimensionen** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="b7692-151">Während **Kennzeichen** noch ausgewählt ist, wählen Sie **Tabellenverknüpfung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="b7692-152">Wählen Sie in der Liste der angezeigten Tabellen in der Spalte **Beziehung** die Option **Standortkennzeichenpositionierung (Kennzeichen)** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="b7692-153">Wählen Sie dann **Auswählen** aus, um **Standortkennzeichenpositionierung** zur Tabellenverknüpfung **Lagerungsdimensionen** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="b7692-154">![Tabellenverknüpfungen](media/LpTableJoin.png "Tabellenverknüpfungen")</span><span class="sxs-lookup"><span data-stu-id="b7692-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="b7692-155">Wählen Sie **OK** aus, um die aktualisierten verknüpften Tabellen zu bestätigen und den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b7692-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="b7692-156">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** erneut die Option **Abfrage bearbeiten** aus, um den Abfrageeditor erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b7692-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="b7692-157">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b7692-158">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="b7692-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b7692-159">**Tabelle:** *Standortkennzeichenpositionierung*</span><span class="sxs-lookup"><span data-stu-id="b7692-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="b7692-160">**Abgeleitete Tabelle:** *Standortkennzeichenpositionierung*</span><span class="sxs-lookup"><span data-stu-id="b7692-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="b7692-161">**Feld:** *LP-Position*</span><span class="sxs-lookup"><span data-stu-id="b7692-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="b7692-162">**Kriterien:** *1*</span><span class="sxs-lookup"><span data-stu-id="b7692-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="b7692-163">![Neuer Bereich](media/LpPositionCriteria.png "Neuer Bereich")</span><span class="sxs-lookup"><span data-stu-id="b7692-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="b7692-164">Wählen Sie **OK** aus, um Ihre Änderungen zu bestätigen und den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b7692-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="b7692-165">Beispieldaten für dieses Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="b7692-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="b7692-166">In diesem Szenario muss sich der Benutzer bei der Warehouse Mobile App anmelden, indem er einen Mitarbeiter verwendet, der für Warehouse *61* eingerichtet ist, um die Arbeit durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="b7692-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="b7692-167">Der Benutzer muss auch Transaktionen abschließen.</span><span class="sxs-lookup"><span data-stu-id="b7692-167">The user must also complete transactions.</span></span>

<span data-ttu-id="b7692-168">Weil mit der Funktion *Standortkennzeichenpositionierung* ein neuer Bezeichner für Kennzeichenpositionen an einem Lagerplatz hinzugefügt wird, müssen Sie zuerst einige Daten erstellen, um das Szenario zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b7692-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="b7692-169">Erste Lagerplatzinventur</span><span class="sxs-lookup"><span data-stu-id="b7692-169">Spot-count the first location</span></span>

1. <span data-ttu-id="b7692-170">Öffnen Sie die Warehouse Mobile App, und melden Sie sich bei Warehouse *61* an.</span><span class="sxs-lookup"><span data-stu-id="b7692-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="b7692-171">Gehen Sie zu **Lagerbestand \> Lagerplatzinventur**.</span><span class="sxs-lookup"><span data-stu-id="b7692-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="b7692-172">Legen Sie auf der Seite **Lagerplatzinventur** das Feld **Lagerplatz** auf *01A01R1S1B* fest.</span><span class="sxs-lookup"><span data-stu-id="b7692-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="b7692-173">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-173">Select **OK**.</span></span>

    <span data-ttu-id="b7692-174">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-174">The page shows the location that you entered.</span></span> <span data-ttu-id="b7692-175">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="b7692-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b7692-176">Wählen Sie **Aktualisieren** aus, um eine Zählung am Lagerplatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="b7692-177">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0001* ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="b7692-178">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-178">Select **OK**.</span></span>
1. <span data-ttu-id="b7692-179">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1001* (oder eine andere Kennzeichennummer Ihrer Wahl) ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="b7692-180">Die Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** zeigt **Kennzeichenposition 1** an.</span><span class="sxs-lookup"><span data-stu-id="b7692-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="b7692-181">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-181">Select **OK**.</span></span>

    <span data-ttu-id="b7692-182">Sie müssen nun die Menge des Artikels angeben, die auf dem Kennzeichen gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="b7692-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="b7692-183">Legen Sie das Feld **Menge** auf *10* fest.</span><span class="sxs-lookup"><span data-stu-id="b7692-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="b7692-184">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-184">Select **OK**.</span></span>

    <span data-ttu-id="b7692-185">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-185">The page shows the location that you entered.</span></span> <span data-ttu-id="b7692-186">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="b7692-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b7692-187">Wählen Sie **Aktualisieren** aus, um eine weitere Zählung am Lagerplatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="b7692-188">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0002* ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="b7692-189">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-189">Select **OK**.</span></span>
1. <span data-ttu-id="b7692-190">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1002* (oder eine andere Kennzeichennummer Ihrer Wahl, sofern sie von der zuvor angegebenen Kennzeichennummer abweicht) ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="b7692-191">Ändern Sie die Kennzeichenposition durch Einstellen des Felds **LP-Position** auf *2*.</span><span class="sxs-lookup"><span data-stu-id="b7692-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="b7692-192">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-192">Select **OK**.</span></span>
1. <span data-ttu-id="b7692-193">Geben Sie die Menge des Artikels an, die auf dem Kennzeichen gezählt wird, indem Sie das Feld **Menge** auf *10* festlegen.</span><span class="sxs-lookup"><span data-stu-id="b7692-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="b7692-194">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-194">Select **OK**.</span></span>

    <span data-ttu-id="b7692-195">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-195">The page shows the location that you entered.</span></span> <span data-ttu-id="b7692-196">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="b7692-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b7692-197">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-197">Select **OK**.</span></span>

<span data-ttu-id="b7692-198">Die Arbeit ist jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b7692-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="b7692-199">Zweite Lagerplatzinventur</span><span class="sxs-lookup"><span data-stu-id="b7692-199">Spot-count the second location</span></span>

1. <span data-ttu-id="b7692-200">Legen Sie auf der Seite **Lagerplatzinventur** das Feld **Lagerplatz** auf *01A01R1S2B* fest.</span><span class="sxs-lookup"><span data-stu-id="b7692-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="b7692-201">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-201">Select **OK**.</span></span>

    <span data-ttu-id="b7692-202">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-202">The page shows the location that you entered.</span></span> <span data-ttu-id="b7692-203">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="b7692-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b7692-204">Wählen Sie **Aktualisieren** aus, um eine Zählung am Lagerplatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="b7692-205">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0002* ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="b7692-206">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-206">Select **OK**.</span></span>
1. <span data-ttu-id="b7692-207">Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1003* (oder eine andere Kennzeichennummer Ihrer Wahl, sofern sie von den beiden im vorherigen Verfahren angegebenen Kennzeichennummern abweicht) ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="b7692-208">Die Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** zeigt **Kennzeichenposition 1** an.</span><span class="sxs-lookup"><span data-stu-id="b7692-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="b7692-209">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-209">Select **OK**.</span></span>
1. <span data-ttu-id="b7692-210">Geben Sie die Menge des Artikels an, die auf dem Kennzeichen gezählt wird, indem Sie das Feld **Menge** auf *10* festlegen.</span><span class="sxs-lookup"><span data-stu-id="b7692-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="b7692-211">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-211">Select **OK**.</span></span>

    <span data-ttu-id="b7692-212">Die Seite zeigt den Lagerplatz, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-212">The page shows the location that you entered.</span></span> <span data-ttu-id="b7692-213">Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="b7692-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b7692-214">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-214">Select **OK**.</span></span>

<span data-ttu-id="b7692-215">Die Arbeit ist jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b7692-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="b7692-216">Arbeitsdetails</span><span class="sxs-lookup"><span data-stu-id="b7692-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="b7692-217">Lagerplatzinventuren aus der mobilen App erstellen Zykluszählarbeit in Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b7692-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="b7692-218">Die Arbeit erfordert, dass die Zählungen akzeptiert werden, bevor sie in den Lagerbestand gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="b7692-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="b7692-219">Melden Sie sich bei Dynamics 365 Supply Chain Management an.</span><span class="sxs-lookup"><span data-stu-id="b7692-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="b7692-220">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="b7692-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b7692-221">Suchen Sie auf der Registerkarte **Überblick** nach Positionen mit den folgenden Werten:</span><span class="sxs-lookup"><span data-stu-id="b7692-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="b7692-222">**Arbeitsauftragstyp:** *Zykluszählung*</span><span class="sxs-lookup"><span data-stu-id="b7692-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="b7692-223">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="b7692-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b7692-224">**Arbeitsstatus:** *Überprüfung ausstehend*</span><span class="sxs-lookup"><span data-stu-id="b7692-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="b7692-225">Für diese Positionen sollten zwei Arbeits-IDs erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="b7692-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="b7692-226">Die Zählungen für diese beiden Arbeits-IDs müssen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7692-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="b7692-227">Wählen Sie im Raster die erste Arbeits-ID für den Arbeitsauftragstyp *Zykluszählung* aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="b7692-228">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Zykluszählung** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="b7692-229">Es werden zwei Positionen angezeigt, eine für jeden Artikel und jedes Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="b7692-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="b7692-230">Die Werte in den Feldern **Gezählte Menge**, **Lagerplatz**, **Kennzeichen** und **Artikel** sollten mit den Zähleinträgen übereinstimmen, die Sie auf dem mobilen Gerät erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="b7692-231">Wenn eines dieser Felder nicht sichtbar ist, wählen Sie im Aktivitätsbereich **Dimensionen anzeigen** aus, um sie dem Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7692-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="b7692-232">Wählen Sie beide Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-232">Select both lines.</span></span>
1. <span data-ttu-id="b7692-233">Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.</span><span class="sxs-lookup"><span data-stu-id="b7692-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="b7692-234">Sie erhalten eine Nachricht „Buchung – Erfassung“.</span><span class="sxs-lookup"><span data-stu-id="b7692-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="b7692-235">Wählen Sie **Nachrichtendetails** aus, um die gebuchte Erfassungsnummer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7692-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="b7692-236">Schließen Sie die Nachrichtendetails.</span><span class="sxs-lookup"><span data-stu-id="b7692-236">Close the message details.</span></span>
1. <span data-ttu-id="b7692-237">Aktualisieren Sie die Seite **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="b7692-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="b7692-238">Die erste Arbeits-ID wurde geschlossen und wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7692-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="b7692-239">Um geschlossene Arbeiten anzuzeigen, aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** über dem Raster.</span><span class="sxs-lookup"><span data-stu-id="b7692-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="b7692-240">Sie akzeptieren nun die Arbeit für das Kennzeichen im Lagerplatz *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="b7692-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="b7692-241">Wählen Sie auf der Registerkarte **Übersicht** die zweite Arbeits-ID für den Arbeitsauftragstyp *Zykluszählung* aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="b7692-242">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Zykluszählung** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="b7692-243">Für den Artikel und das Kennzeichen wird eine Position angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7692-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="b7692-244">Die Werte in den Feldern **Gezählte Menge**, **Lagerplatz**, **Kennzeichen** und **Artikel** sollten mit den Zähleinträgen übereinstimmen, die Sie auf dem mobilen Gerät erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b7692-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="b7692-245">Wählen Sie die Position aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-245">Select the line.</span></span>
1. <span data-ttu-id="b7692-246">Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.</span><span class="sxs-lookup"><span data-stu-id="b7692-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="b7692-247">Sie erhalten eine Nachricht „Buchung – Erfassung“.</span><span class="sxs-lookup"><span data-stu-id="b7692-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="b7692-248">Wählen Sie **Nachrichtendetails** aus, um die gebuchte Erfassungsnummer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7692-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="b7692-249">Schließen Sie die Nachrichtendetails.</span><span class="sxs-lookup"><span data-stu-id="b7692-249">Close the message details.</span></span>
1. <span data-ttu-id="b7692-250">Aktualisieren Sie die Seite **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="b7692-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="b7692-251">Die zweite Arbeits-ID wurde geschlossen und wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7692-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="b7692-252">Um geschlossene Arbeiten anzuzeigen, aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** über dem Raster.</span><span class="sxs-lookup"><span data-stu-id="b7692-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="b7692-253">Verfügbarer Lagerbestand nach Lagerplatz</span><span class="sxs-lookup"><span data-stu-id="b7692-253">On-hand by location</span></span>

1. <span data-ttu-id="b7692-254">Wechseln Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Verfügbarer Lagerbestand nach Lagerplatz**.</span><span class="sxs-lookup"><span data-stu-id="b7692-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="b7692-255">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b7692-255">Set the following values:</span></span>

    - <span data-ttu-id="b7692-256">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="b7692-256">**Site:** *6*</span></span>
    - <span data-ttu-id="b7692-257">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="b7692-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b7692-258">**Standortübergreifend aktualisieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b7692-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="b7692-259">Beachten Sie, dass der Lagerplatz *01A01R1S1B* zwei Kennzeichen hat:</span><span class="sxs-lookup"><span data-stu-id="b7692-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="b7692-260">**A0001**, bei dem das Feld **LP-Position** auf *1* festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="b7692-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="b7692-261">**A0002**, bei dem das Feld **LP-Position** auf *2* festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="b7692-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="b7692-262">Beachten Sie, dass der Lagerplatz *01A01R1S2B* ein Kennzeichen hat:</span><span class="sxs-lookup"><span data-stu-id="b7692-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="b7692-263">**A0002**, bei dem das Feld **LP-Position** auf *1* festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="b7692-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="b7692-264">Szenario für Aufträge</span><span class="sxs-lookup"><span data-stu-id="b7692-264">Sales order scenario</span></span>

<span data-ttu-id="b7692-265">Nun, da die Funktion *Standortkennzeichenpositionierung* eingerichtet und der Lagerbestand bereitgestellt wurde, müssen Sie einen Auftrag erstellen, um Kommissionierarbeiten zu generieren, die den Lagerarbeiter anweisen, Artikel *A0002* vom Lagerort zu kommissionieren, an dem sich die Paletten-ID an Position *1* befindet.</span><span class="sxs-lookup"><span data-stu-id="b7692-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="b7692-266">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="b7692-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b7692-267">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b7692-268">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b7692-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b7692-269">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b7692-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="b7692-270">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="b7692-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b7692-271">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7692-271">Select **OK**.</span></span>
1. <span data-ttu-id="b7692-272">Dem Raster im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7692-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b7692-273">Legen Sie die folgenden Werte für diese neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="b7692-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="b7692-274">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b7692-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="b7692-275">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="b7692-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b7692-276">Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b7692-277">Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um Lagerbestand für die Auftragsposition zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="b7692-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="b7692-278">Schließen Sie die Seite **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="b7692-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="b7692-279">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b7692-280">Sie erhalten eine Informationsnachricht mit der Wellen-ID und der Lieferungs-ID, die für den Auftrag erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b7692-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="b7692-281">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** über dem Raster die Option **Arbeitsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="b7692-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="b7692-282">Die Seite **Arbeit** wird angezeigt und zeigt die Arbeit, die für die Verkaufsposition erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7692-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="b7692-283">Notieren Sie sich die angezeigte Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="b7692-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="b7692-284">Verkaufsauswahlszenario</span><span class="sxs-lookup"><span data-stu-id="b7692-284">Sales picking scenario</span></span>

1. <span data-ttu-id="b7692-285">Öffnen Sie die mobile App, und melden Sie sich bei Warehouse *61* an.</span><span class="sxs-lookup"><span data-stu-id="b7692-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="b7692-286">Gehen Sie zu **Ausgehend \> Verkaufsauswahl**.</span><span class="sxs-lookup"><span data-stu-id="b7692-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="b7692-287">Wählen Sie auf der Seite **Arbeits-/Kennzeichen-ID scannen** das Feld **ID** aus, und geben Sie dann die Arbeits-ID aus der Verkaufsposition ein.</span><span class="sxs-lookup"><span data-stu-id="b7692-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="b7692-288">Beachten Sie, dass Sie bei der Kommissionierung angewiesen werden, den Artikel *A0002* vom Lagerplatz *01A01R1S2B* zu kommissionieren.</span><span class="sxs-lookup"><span data-stu-id="b7692-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="b7692-289">Sie erhalten diese Anweisung, weil sich Artikel *A0002* auf einem Kennzeichen befindet, das in Position *1* an diesem Lagerplatz ist.</span><span class="sxs-lookup"><span data-stu-id="b7692-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="b7692-290">![Lagerplatz Position 1](media/LocationLicensePlatePositioning.png "Lagerplatz Position 1")</span><span class="sxs-lookup"><span data-stu-id="b7692-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="b7692-291">Geben Sie die Kennzeichen-ID ein, die Sie für den Lagerplatz erstellt haben, und befolgen Sie die Anweisungen, um den Auftrag auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b7692-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
