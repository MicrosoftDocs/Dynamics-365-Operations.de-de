---
title: Artikelkonsolidierung – Auslastung von Lagerplatz
description: Dieses Thema enthält Informationen zu Funktionen, mit denen Lagerverwalter die volumetrische Auslastung von Standorten im gesamten Lager problemlos anzeigen und filtern können. Manager können direkt auf der Seite „Positionskonsolidierung“ Standorte auswählen und Lagerumlagerungsarbeiten erstellen, um Artikel zu konsolidieren und so den Lagerraum besser zu nutzen.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429028"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="2e148-104">Artikelkonsolidierung – Auslastung von Lagerplatz</span><span class="sxs-lookup"><span data-stu-id="2e148-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e148-105">Dieses Thema enthält Informationen zu Funktionen, mit denen Lagerverwalter die volumetrische Auslastung von Standorten im gesamten Lager problemlos anzeigen und filtern können.</span><span class="sxs-lookup"><span data-stu-id="2e148-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="2e148-106">Manager können direkt auf der Seite **Positionskonsolidierung** Standorte auswählen und Lagerumlagerungsarbeiten erstellen, um Artikel zu konsolidieren und so den Lagerraum besser zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="2e148-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="2e148-107">Aktivieren der Funktionen</span><span class="sxs-lookup"><span data-stu-id="2e148-107">Turn on the features</span></span>

<span data-ttu-id="2e148-108">Bevor Sie die in diesem Thema beschriebenen Funktionen verwenden können, müssen Sie sie in Ihrem System aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2e148-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="2e148-109">Administratoren können im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktionen überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2e148-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="2e148-110">Aktivieren Sie beide folgenden Funktionen in der Reihenfolge, in der sie aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2e148-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="2e148-111">(Beide Funktionen sind für das Modul **Lagerortverwaltung** vorgesehen.)</span><span class="sxs-lookup"><span data-stu-id="2e148-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="2e148-112">Status des Lagerplatzes an einem Lagerort</span><span class="sxs-lookup"><span data-stu-id="2e148-112">Warehouse location status</span></span>
2. <span data-ttu-id="2e148-113">Nutzung von Lagerplatz für Positionskonsolidierung</span><span class="sxs-lookup"><span data-stu-id="2e148-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="2e148-114">Status des Lagerplatzes an einem Lagerort</span><span class="sxs-lookup"><span data-stu-id="2e148-114">Warehouse location status</span></span>

<span data-ttu-id="2e148-115">Mit der Funktion *Status des Lagerplatzes an einem Lagerort* werden der Seite **Lagerplätze** vier neue Felder hinzugefügt, um zusätzliche Informationen zum aktuellen Status des Standorts zu verfolgen:</span><span class="sxs-lookup"><span data-stu-id="2e148-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="2e148-116">**Artikelnummer** – Der Artikel, der sich derzeit am Lagerplatz befindet.</span><span class="sxs-lookup"><span data-stu-id="2e148-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="2e148-117">Wenn der Lagerplatz mehrere Artikel enthält, ist dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="2e148-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="2e148-118">**Datum und Uhrzeit der letzten Aktivität** – Der Zeitstempel der letzten Lagertransaktion, die für den Lagerplatz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e148-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="2e148-119">**Fälligkeitsdatum** – Das Datum, an dem der Bestand am Lagerplatz in den Lagerort gebracht wurde.</span><span class="sxs-lookup"><span data-stu-id="2e148-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="2e148-120">Dieses Datum wird anhand des Fälligkeitsdatums des Kennzeichens berechnet.</span><span class="sxs-lookup"><span data-stu-id="2e148-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="2e148-121">Obwohl dieses Datum für Lagerplätze, die mit einem Kennzeichen versehen sind, genau ist, gilt dies möglicherweise nicht für Lagerplätze, die nicht mit einem Kennzeichen versehen sind.</span><span class="sxs-lookup"><span data-stu-id="2e148-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="2e148-122">**Lagerplatzstatus** – Der Status des Lagerplatzes.</span><span class="sxs-lookup"><span data-stu-id="2e148-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="2e148-123">Vier Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="2e148-123">Four values are available:</span></span>

    - <span data-ttu-id="2e148-124">**Unbestimmt** – Das Lagerplatzprofil verfolgt den Status nicht nach.</span><span class="sxs-lookup"><span data-stu-id="2e148-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="2e148-125">Daher ist der aktuelle Status unbekannt.</span><span class="sxs-lookup"><span data-stu-id="2e148-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="2e148-126">**Leer** – Derzeit befindet sich kein Bestand am Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="2e148-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="2e148-127">**Kommissionierung** – Ausgehende Transaktionen wurden für den Lagerplatz ausgeführt, nachdem er zuletzt leer war.</span><span class="sxs-lookup"><span data-stu-id="2e148-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="2e148-128">**Lager** – Nur eingehende Transaktionen wurden ausgeführt, da der Lagerplatz zuletzt leer war.</span><span class="sxs-lookup"><span data-stu-id="2e148-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="2e148-129">In diesen Feldern erhalten Lagerverwalter einen besseren Überblick über den Status der Lagerplätze am Lagerort.</span><span class="sxs-lookup"><span data-stu-id="2e148-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="2e148-130">Sie ermöglichen auch erweiterte Berichterstellung und Filterung.</span><span class="sxs-lookup"><span data-stu-id="2e148-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="2e148-131">Einrichten von Artikelkonsolidierung und Auslastung von Lagerplatz</span><span class="sxs-lookup"><span data-stu-id="2e148-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="2e148-132">In diesem Abschnitt wird beschrieben, wie Sie Ihr System auf die Verwendung der Artikelkonsolidierung und Auslastung von Lagerplatz vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="2e148-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="2e148-133">Die Verfahren verwenden Beispielwerte aus den Standarddemodaten.</span><span class="sxs-lookup"><span data-stu-id="2e148-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="2e148-134">Wenn Sie das Beispielszenario durcharbeiten möchten, das später in diesem Thema bereitgestellt wird, wählen Sie die juristische Person **USMF** aus (die die Standarddemodaten enthält) und erstellen Sie jeden Datensatz, der in diesem Abschnitt beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2e148-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="2e148-135">Wenn Sie das Beispielszenario nicht durcharbeiten möchten, können die hier angegebenen Werte als Beispiele für die Einrichtungstypen betrachtet werden, die Sie zur Verwendung der Funktionen ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="2e148-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="2e148-136">Freigegebenes Produkt</span><span class="sxs-lookup"><span data-stu-id="2e148-136">Released product</span></span>

1. <span data-ttu-id="2e148-137">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="2e148-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2e148-138">Wählen Sie im Feld **Artikelnummer** die Option *M9201* aus und öffnen Sie die Detailseite.</span><span class="sxs-lookup"><span data-stu-id="2e148-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="2e148-139">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** **Physische Dimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="2e148-140">Wählen Sie auf der Seite **Physische Dimensionen** im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="2e148-141">Dem Raster wird eine neue Zeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2e148-141">A new line is added to the grid.</span></span> <span data-ttu-id="2e148-142">Das Feld **Artikelnummer** ist voreingestellt.</span><span class="sxs-lookup"><span data-stu-id="2e148-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="2e148-143">Wählen Sie im Feld **Einheit** die Option *ea* aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="2e148-144">Die verbleibenden Felder in der Zeile werden automatisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2e148-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="2e148-145">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2e148-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="2e148-146">Lagerortprofil</span><span class="sxs-lookup"><span data-stu-id="2e148-146">Location profile</span></span>

1. <span data-ttu-id="2e148-147">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="2e148-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="2e148-148">Wählen Sie in der Liste der Lagerplatzprofile **BODEN-05** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="2e148-149">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2e148-150">Stellen Sie im Inforegister **Allgemeines** sicher, dass beide folgenden Optionen auf *Ja* eingestellt sind:</span><span class="sxs-lookup"><span data-stu-id="2e148-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="2e148-151">Artikel am Lagerplatz aktivieren</span><span class="sxs-lookup"><span data-stu-id="2e148-151">Enable item in location</span></span>
    - <span data-ttu-id="2e148-152">Lagerplatzstatus aktivieren</span><span class="sxs-lookup"><span data-stu-id="2e148-152">Enable location status</span></span>

1. <span data-ttu-id="2e148-153">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2e148-154">Wenn die Optionen **Artikel an Lagerplatz aktivieren** und **Lagerplatzstatus aktivieren** bereits auf *Ja*  eingestellt, fahren Sie mit den Anweisungen zum Einrichten des Inforegisters **Dimensionen** in Schritt 10 fort.</span><span class="sxs-lookup"><span data-stu-id="2e148-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="2e148-155">Wenn die Optionen nicht bereits auf *Ja* eingestellt waren, müssen Sie eine Konsistenzprüfung für das Modul **Lagerortverwaltung** durchführen, nachdem Sie sie manuell eingestellt haben.</span><span class="sxs-lookup"><span data-stu-id="2e148-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="2e148-156">Fahren Sie in diesem Fall mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="2e148-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="2e148-157">Um die Konsistenzprüfung durchzuführen, gehen Sie zu **Systemadministration \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**.</span><span class="sxs-lookup"><span data-stu-id="2e148-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="2e148-158">Legen Sie im Dialogfeld **Konsistenzprüfung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2e148-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2e148-159">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="2e148-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="2e148-160">**Überprüfen/Beheben:** *Überprüfen*</span><span class="sxs-lookup"><span data-stu-id="2e148-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="2e148-161">**Startdatum:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="2e148-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="2e148-162">**Konsistenzprüfung des Status des Lagerplatzes an einem Lagerort:** Aktivieren Sie dieses Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="2e148-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="2e148-163">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e148-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="2e148-164">Sie erhalten eine Benachrichtigung, wenn die Konsistenzprüfung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2e148-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="2e148-165">Öffnen Sie das [Aktionszentrum](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications), um die Nachricht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2e148-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="2e148-166">Wählen Sie **Meldungsdetails**, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2e148-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="2e148-167">Wenn die Meldung für die Konsistenzprüfung „Falsche Standortstatusinformationen für Standort XXXX in Lagerort XX gefunden“ lautet, müssen Sie die Konsistenzprüfung erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e148-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="2e148-168">Stellen Sie diesmal das Feld **Überprüfen/Beheben** auf *Fehler beheben* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="2e148-169">Zeigen Sie die Nachrichten an, um sicherzustellen, dass keine Fehler gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="2e148-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="2e148-170">Sie müssen nun die Einrichtung des Lagerplatzprofils abschließen.</span><span class="sxs-lookup"><span data-stu-id="2e148-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="2e148-171">Gehen Sie zurück zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatzprofile**, wählen Sie das Lagerplatzprofil **BODEN-05** und dann im Aktionsbereich die Option **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2e148-172">Legen Sie im Inforegister **Dimensionen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2e148-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2e148-173">**Volumennutzung in Prozent:** *100*</span><span class="sxs-lookup"><span data-stu-id="2e148-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="2e148-174">**Volumetrische Methode für den Lagerort-Standort:** *Lagerplatzvolumen verwenden*</span><span class="sxs-lookup"><span data-stu-id="2e148-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="2e148-175">**Tatsächliche Höhe des Lagerplatzes:** *10*</span><span class="sxs-lookup"><span data-stu-id="2e148-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="2e148-176">**Tatsächliche Breite des Lagerplatzes:** *10*</span><span class="sxs-lookup"><span data-stu-id="2e148-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="2e148-177">**Tatsächliche Tiefe des Lagerplatzes:** *10*</span><span class="sxs-lookup"><span data-stu-id="2e148-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="2e148-178">**Höchstgewicht:** *100*</span><span class="sxs-lookup"><span data-stu-id="2e148-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="2e148-179">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="2e148-180">Menüelemente des mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="2e148-180">Mobile device menu items</span></span>

1. <span data-ttu-id="2e148-181">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="2e148-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2e148-182">Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt zum Sortieren zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e148-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="2e148-183">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2e148-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="2e148-184">**Name des Menüelements:** *Anpassen in*</span><span class="sxs-lookup"><span data-stu-id="2e148-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="2e148-185">**Titel:** *Anpassen in*</span><span class="sxs-lookup"><span data-stu-id="2e148-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="2e148-186">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="2e148-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="2e148-187">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="2e148-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="2e148-188">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2e148-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2e148-189">**Arbeitserstellungsprozess:** *Anpassung in*</span><span class="sxs-lookup"><span data-stu-id="2e148-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="2e148-190">**Lagerregulierungstypen:** *Anpassen in*</span><span class="sxs-lookup"><span data-stu-id="2e148-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="2e148-191">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="2e148-192">Menü für mobiles Gerät</span><span class="sxs-lookup"><span data-stu-id="2e148-192">Mobile device menu</span></span>

1. <span data-ttu-id="2e148-193">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="2e148-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="2e148-194">Wählen Sie in der Liste der Menüs **Lager** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="2e148-195">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2e148-196">Suchen und wählen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den Menüpunkt **Anpassen in** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="2e148-197">Wählen Sie die rechte Pfeiltaste, um **Anpassen in** zur Liste **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="2e148-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="2e148-198">Auf diese Weise fügen Sie dem ausgewählten Menü den neuen Menüpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e148-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="2e148-199">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="2e148-200">Bewegungstypen</span><span class="sxs-lookup"><span data-stu-id="2e148-200">Movement types</span></span>

1. <span data-ttu-id="2e148-201">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Bestand \> Bewegungstypen**.</span><span class="sxs-lookup"><span data-stu-id="2e148-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="2e148-202">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2e148-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2e148-203">**Bewegungstypcode:** *KONSOLIDIEREN*</span><span class="sxs-lookup"><span data-stu-id="2e148-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="2e148-204">**Beschreibung:** *Lagerplätze konsolidieren*</span><span class="sxs-lookup"><span data-stu-id="2e148-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="2e148-205">**Arbeitsklassen-ID:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="2e148-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="2e148-206">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e148-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2e148-207">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="2e148-207">Example scenario</span></span>

<span data-ttu-id="2e148-208">Im folgenden Szenario wird die Lagerort-App auf einem mobilen Gerät verwendet, um eine Bestandsaufnahme *Anpassung in* an zwei Standorten im Lagerort durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="2e148-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="2e148-209">Lagerbestand zu Lagerplätzen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="2e148-209">Add inventory to locations</span></span>

1. <span data-ttu-id="2e148-210">Melden Sie sich beim mobilen Gerät als Benutzer an, der für den Lagerort *51* eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="2e148-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="2e148-211">Gehen Sie zu **Bestand \> Anpassen in**.</span><span class="sxs-lookup"><span data-stu-id="2e148-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="2e148-212">Sie geben nun die erste Lagerplatzanpassung ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="2e148-213">Wählen Sie in der Aufgabe **Anpassung in** den Ort aus, für den die Bestandsanpassung vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="2e148-214">Wählen Sie im Feld **LOC** *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="2e148-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="2e148-215">Bestätigen Sie den Lagerplatz</span><span class="sxs-lookup"><span data-stu-id="2e148-215">Confirm the location.</span></span>
1. <span data-ttu-id="2e148-216">Erstellen Sie eine Kennzeichen-ID für den Artikel, der dem Lagerplatz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2e148-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="2e148-217">Im Feld **LP** geben Sie *LP00101* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="2e148-218">Bestätigen Sie das Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2e148-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="2e148-219">Geben Sie den Artikel ein, der dem Kennzeichen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="2e148-220">Im Feld **ITEM** geben Sie *M9201* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="2e148-221">Bestätigen Sie den Artikel.</span><span class="sxs-lookup"><span data-stu-id="2e148-221">Confirm the item.</span></span>
1. <span data-ttu-id="2e148-222">Geben Sie die Menge des Artikels ein, der dem Kennzeichen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="2e148-223">Geben Sie im Feld **QTY** den Wert *10* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="2e148-224">Bestätigen Sie die Menge.</span><span class="sxs-lookup"><span data-stu-id="2e148-224">Confirm the quantity.</span></span>

    <span data-ttu-id="2e148-225">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="2e148-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="2e148-226">Sie geben nun die zweite Lagerplatzanpassung ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="2e148-227">Wählen Sie in der Aufgabe **Anpassung in** den Ort aus, für den die Bestandsanpassung vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="2e148-228">Wählen Sie im Feld **LOC** *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="2e148-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="2e148-229">Bestätigen des Lagerplatzes</span><span class="sxs-lookup"><span data-stu-id="2e148-229">Confirm the location.</span></span>
1. <span data-ttu-id="2e148-230">Erstellen Sie eine Kennzeichen-ID für den Artikel, der dem Lagerplatz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2e148-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="2e148-231">Im Feld **LP** geben Sie *LP00201* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="2e148-232">Bestätigen Sie das Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2e148-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="2e148-233">Geben Sie den Artikel ein, der dem Kennzeichen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="2e148-234">Im Feld **ITEM** geben Sie *M9201* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="2e148-235">Bestätigen Sie den Artikel.</span><span class="sxs-lookup"><span data-stu-id="2e148-235">Confirm the item.</span></span>
1. <span data-ttu-id="2e148-236">Geben Sie die Menge des Artikels ein, der dem Kennzeichen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="2e148-237">Geben Sie im Feld **QTY** den Wert *15* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="2e148-238">Bestätigen Sie die Menge.</span><span class="sxs-lookup"><span data-stu-id="2e148-238">Confirm the quantity.</span></span>

    <span data-ttu-id="2e148-239">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="2e148-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2e148-240">Wählen Sie die Menüschaltfläche (manchmal auch als Hamburger oder Hamburgerschaltfläche bezeichnet) und dann **Abbrechen** aus, um die Aufgabe **Anpassung in** zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2e148-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="2e148-241">Lagerplätze konsolidieren</span><span class="sxs-lookup"><span data-stu-id="2e148-241">Consolidate locations</span></span>

1. <span data-ttu-id="2e148-242">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Artikelkonsolidierung**.</span><span class="sxs-lookup"><span data-stu-id="2e148-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="2e148-243">Wählen Sie in der Kopfzeile ein Lager aus, für das die Konsolidierung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e148-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="2e148-244">Im Feld **Lagerort** geben Sie *51* ein.</span><span class="sxs-lookup"><span data-stu-id="2e148-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="2e148-245">Für jeden Ort, an dem der Artikel *M9201* angepasst wurde, wird ein Datensatz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e148-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="2e148-246">In der Spalte **Nutzung in Prozent** wird die volumetrische Auslastung jedes Lagerplatzes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e148-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="2e148-247">Um den Bestand zu konsolidieren, wählen Sie alle Lagerplätze aus, die konsolidiert werden müssen, und wählen Sie dann im Aktionsbereich die Option **Bestand konsolidieren**.</span><span class="sxs-lookup"><span data-stu-id="2e148-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="2e148-248">Geben Sie im Dialogfeld **Bestand konsolidieren** den Lagerplatz und den Bewegungstyp an, die zum Erstellen der Arbeit für die Lagerumlagerung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e148-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="2e148-249">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2e148-249">Set the following values:</span></span>

    - <span data-ttu-id="2e148-250">**Lagerplatz:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="2e148-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="2e148-251">**Bewegungstypcode:** *KONSOLIDIEREN*</span><span class="sxs-lookup"><span data-stu-id="2e148-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="2e148-252">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e148-252">Select **OK**.</span></span>
1. <span data-ttu-id="2e148-253">Sie erhalten eine Informationsnachricht, die die erstellte Umlagerungsarbeit zeigt.</span><span class="sxs-lookup"><span data-stu-id="2e148-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="2e148-254">Notieren Sie die Umlagerungsarbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="2e148-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="2e148-255">Umlagerungsarbeit anzeigen</span><span class="sxs-lookup"><span data-stu-id="2e148-255">View movement work</span></span>

1. <span data-ttu-id="2e148-256">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="2e148-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="2e148-257">Zeigen Sie die erstellte Arbeit an.</span><span class="sxs-lookup"><span data-stu-id="2e148-257">View the work that was created.</span></span> <span data-ttu-id="2e148-258">Verwenden Sie die Umlagerungsarbeits-ID aus der Bestandskonsolidierung, um das Arbeitsraster zu filtern oder zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="2e148-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="2e148-259">In diesem Szenario wurde ein vorhandener Lagerplatz mit Bestand als Standort für die Bestandskonsolidierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e148-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="2e148-260">Daher wurde nur eine Arbeits-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e148-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="2e148-261">Das System erstellt eine Arbeits-ID für jede Bewegung, die abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="2e148-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="2e148-262">Wenn Sie einen Lagerplatz angeben, der bereits Bestand enthält, wird nur eine Arbeits-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e148-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="2e148-263">Wenn Sie einen neuen Lagerplatz angeben, werden zwei Arbeits-IDs erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e148-263">If you specify a new location, two work IDs are created.</span></span>
