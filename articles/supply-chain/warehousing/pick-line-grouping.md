---
title: Gruppierung von Kommissionierpositionen
description: In diesem Thema wird eine Übersicht über die Gruppierung von Kommissionierpositionen angezeigt.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ab8cdd7cad5420aca0de53e59220da9e230d411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234632"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="afbf4-103">Gruppierung von Kommissionierpositionen</span><span class="sxs-lookup"><span data-stu-id="afbf4-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afbf4-104">Die Gruppierung von Entnahmepositionen ermöglicht das Zusammenfassen mehrerer Arbeitspositionen mit demselben Artikel und Lagerplatz zu einer einzigen Entnahmeposition, die dem Benutzer auf einem Mobilgerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="afbf4-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="afbf4-105">Dadurch können Lagerarbeiter die effizientesten Anweisungen erhalten, wobei die erforderliche Trennung der Arbeitspositionen (für unterschiedliche Container, Aufträge usw.) weiterhin im System beibehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="afbf4-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="afbf4-106">Einschalten der Gruppierungsfunktion für Entnahmepositionen</span><span class="sxs-lookup"><span data-stu-id="afbf4-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="afbf4-107">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="afbf4-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="afbf4-108">Administratoren können den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie bei Bedarf einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="afbf4-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="afbf4-109">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="afbf4-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="afbf4-110">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="afbf4-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="afbf4-111">**Funktionsname:** *Gruppierung von Entnahmepositionen*</span><span class="sxs-lookup"><span data-stu-id="afbf4-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="afbf4-112">Gruppierung von Kommissionierpositionen einrichten</span><span class="sxs-lookup"><span data-stu-id="afbf4-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="afbf4-113">Erstellen eines Menüelements für ein mobiles Geräts</span><span class="sxs-lookup"><span data-stu-id="afbf4-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="afbf4-114">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="afbf4-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="afbf4-115">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="afbf4-116">Geben Sie im Feld **Menüelementname** den Text *Entnahmepositionen für Warengruppe* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="afbf4-117">Geben Sie im Feld **Titel** den Text *Entnahmepositionen für Warengruppe* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="afbf4-118">Dieser Titel wird im Menü des Mobilgeräts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="afbf4-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="afbf4-119">Wählen Sie im Feld **Modus** *Arbeit*.</span><span class="sxs-lookup"><span data-stu-id="afbf4-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="afbf4-120">Legen Sie die **Vorhandene Arbeit verwenden**-Option mit *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="afbf4-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="afbf4-121">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="afbf4-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="afbf4-122">Wählen Sie im Feld **Geleitet von** die Option *Benutzergesteuert* fest.</span><span class="sxs-lookup"><span data-stu-id="afbf4-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="afbf4-123">Legen Sie die Option **Ladungsträger generieren** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="afbf4-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="afbf4-124">Legen Sie die Option **Gruppenentnahme** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="afbf4-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="afbf4-125">Übernehmen Sie für alle verbleibenden Optionen die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="afbf4-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="afbf4-126">Befolgen Sie diese Schritte, um gültige Arbeitsklassen für den Menüpunkt für Mobilgeräte zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="afbf4-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="afbf4-127">Wählen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="afbf4-128">Wählen Sie im Feld **Arbeitsklassenkennung** entweder die Option *Verkäufe* oder *SO Entnahme* auswählen, je nachdem, welchen Lagerort Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="afbf4-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="afbf4-129">Wählen Sie für dieses Szenario *SO Entnahme* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="afbf4-130">Das Feld **Arbeitsauftragstyp** wird automatisch auf *Auftrag* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="afbf4-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="afbf4-131">Menü des mobilen Geräts einrichten</span><span class="sxs-lookup"><span data-stu-id="afbf4-131">Set up a mobile device menu</span></span>

<span data-ttu-id="afbf4-132">Führen Sie die folgenden Schritte aus, um den soeben erstellten Menüpunkt zum Menü **Ausgehend** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="afbf4-133">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="afbf4-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="afbf4-134">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="afbf4-135">Im Listenbereich werden alle vorhandenen Menüs für Mobilgeräte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="afbf4-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="afbf4-136">Wählen Sie in der Liste *Ausgehend* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="afbf4-137">Suchen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den von Ihnen erstellten Menüpunkt *Entnahmepositionen für Warengruppe* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="afbf4-138">Wählen Sie die Schaltfläche mit dem Pfeil nach rechts aus, um den Menüpunkt *Entnahmepositionen für Warengruppe* in die Liste **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="afbf4-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="afbf4-139">Verwenden Sie die Nach-oben- und Nach-unten-Pfeilschaltflächen, um den Menüpunkt an die gewünschte Position in der Menüstruktur zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="afbf4-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="afbf4-140">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="afbf4-141">Eine Arbeitsvorlage einrichten</span><span class="sxs-lookup"><span data-stu-id="afbf4-141">Set up a work template</span></span>

1. <span data-ttu-id="afbf4-142">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="afbf4-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="afbf4-143">Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="afbf4-144">Suchen Sie im Raster **Übersicht** nach der mit dieser Funktion zu verwendenden Arbeitsvorlage und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="afbf4-145">Wählen Sie für dieses Szenario die Vorlage *51 Entnahme zu Plattform* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="afbf4-146">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="afbf4-147">Wählen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortierung** die Option **Hinzufügen** aus und legen Sie dann für die neue Zeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="afbf4-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="afbf4-148">Wählen Sie in der Spalte **Tabelle** die Option *Temporäre Arbeitstransaktionen* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="afbf4-149">Wählen Sie in der Spalte **Abgeleitete Tabelle** die Option *Temporäre Arbeitstransaktionen* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="afbf4-150">Wählen Sie in der Spalte *Feld* die Option **Artikelnummer** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="afbf4-151">Wählen Sie in der Spalte **Suchrichtung** die Option *Aufsteigend* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="afbf4-152">Wählen Sie **OK** aus, um das Dialogfeld zu schließen und Ihre Auswahl zu speichern.</span><span class="sxs-lookup"><span data-stu-id="afbf4-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="afbf4-153">Die folgende Meldung wird angezeigt: „Gruppierung wird zurückgesetzt, fortfahren?“</span><span class="sxs-lookup"><span data-stu-id="afbf4-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="afbf4-154">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="afbf4-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afbf4-155">Damit die Funktion zum Gruppieren von Auswahlzeilen funktioniert, müssen die Arbeitszeilen nach Artikel-ID sortiert sein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="afbf4-156">Wenn Zeilen mit denselben Elementen nicht nacheinander sequenziert werden, werden sie nicht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="afbf4-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="afbf4-157">Beispiel</span><span class="sxs-lookup"><span data-stu-id="afbf4-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="afbf4-158">Entnahmearbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="afbf4-158">Create picking work</span></span>

<span data-ttu-id="afbf4-159">Bevor Sie die Gruppierung von Kommissionierpositionen einrichten können, müssen Sie geeignete ausgehende Arbeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="afbf4-160">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="afbf4-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="afbf4-161">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="afbf4-162">Wählen Sie im Feld **Kundenkonto** die Option *US-004* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="afbf4-163">Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagerort** die Option *51* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="afbf4-164">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="afbf4-164">Select **OK**.</span></span>
1. <span data-ttu-id="afbf4-165">Fügen Sie im Inforegister **Auftragspositionen** die folgenden sechs Positionen hinzu:</span><span class="sxs-lookup"><span data-stu-id="afbf4-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="afbf4-166">**Position 1:** Wählen Sie im Feld **Artikelnummer** die Option *M9200* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="afbf4-167">Geben Sie im Feld **Menge** den Wert *3* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="afbf4-168">**Position 2:** Wählen Sie im Feld **Artikelnummer** die Option *M9201* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="afbf4-169">Geben Sie im Feld **Menge** den Wert *3* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="afbf4-170">**Position 3:** Wählen Sie im Feld **Artikelnummer** die Option *M9202* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="afbf4-171">Geben Sie im Feld **Menge** den Wert *2* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="afbf4-172">**Position 4:** Wählen Sie im Feld **Artikelnummer** die Option *M9200* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="afbf4-173">Geben Sie im Feld **Menge** den Wert *1* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="afbf4-174">**Position 5:** Wählen Sie im Feld **Artikelnummer** die Option *M9200* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="afbf4-175">Geben Sie im Feld **Menge** den Wert *3* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="afbf4-176">**Position 6:** Wählen Sie im Feld **Artikelnummer** die Option *M9202* aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="afbf4-177">Geben Sie im Feld **Menge** den Wert *7* ein.</span><span class="sxs-lookup"><span data-stu-id="afbf4-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="afbf4-178">Hier ist eine Zusammenfassung der Gesamtmengen für jeden Artikel:</span><span class="sxs-lookup"><span data-stu-id="afbf4-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="afbf4-179">**Artikel M9200:** *7* Stück</span><span class="sxs-lookup"><span data-stu-id="afbf4-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="afbf4-180">**Artikel M9201:** *3* Stück</span><span class="sxs-lookup"><span data-stu-id="afbf4-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="afbf4-181">**Artikel M9202:** *9* Stück</span><span class="sxs-lookup"><span data-stu-id="afbf4-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="afbf4-182">Bevor Sie die Bestellungen an das Lager freigeben, müssen Sie sicherstellen, dass die Kommissionierstellen über genügend Lagerbestand für alle Artikel in allen Bestellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="afbf4-183">Überprüfen Sie die Einstellung **Standortrichtlinie**, um zu bestimmen, welche Kommissionierorte für die Kundenauftragskommissionierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afbf4-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="afbf4-184">Wenn Sie die Contoso-Demodatenumgebung für Lagerort *51* verwenden, bestätigen Sie, dass Bestand verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="afbf4-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="afbf4-185">Sie müssen jetzt den Bestand für jede Position reservieren.</span><span class="sxs-lookup"><span data-stu-id="afbf4-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="afbf4-186">Wählen Sie im Inforegister **Auftragspositionen** eine der Positionen aus, die reserviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="afbf4-187">Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="afbf4-188">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um die Reservierung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="afbf4-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="afbf4-189">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="afbf4-189">Then close the page.</span></span>
1. <span data-ttu-id="afbf4-190">Wiederholen Sie die Schritte 8 bis 10 für die verbleibenden Positionen, die reserviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="afbf4-191">Jetzt müssen Sie den Auftrag für den Lagerort freigeben.</span><span class="sxs-lookup"><span data-stu-id="afbf4-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="afbf4-192">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="afbf4-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="afbf4-193">Sie erhalten eine Nachricht, die besagt, dass eine Lieferung und eine Welle erstellt wurden und die Welle zur Ausführung in einem Stapel gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="afbf4-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="afbf4-194">Wenn die Welle und alle nachgelagerten Einzelvorgänge abgeschlossen wurden, wird für Arbeit mit sechs Positionen eine Arbeitskennung erstellt.</span><span class="sxs-lookup"><span data-stu-id="afbf4-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="afbf4-195">Die Zeilen sind nach Artikelnummer sortiert.</span><span class="sxs-lookup"><span data-stu-id="afbf4-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="afbf4-196">Wechseln Sie zu **Lagerverwaltung \> Arbeit \> Alle Arbeit**, um die erstellte Arbeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="afbf4-197">Notieren Sie sich den Wert von **Arbeitskennung**, da Sie ihn in der nächsten Prodzedur benötigen werden..</span><span class="sxs-lookup"><span data-stu-id="afbf4-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="afbf4-198">Initiieren einer Entnahme vom Mobilgerät aus</span><span class="sxs-lookup"><span data-stu-id="afbf4-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="afbf4-199">Melden Sie sich beim mobilen Gerät als Benutzer an, der für den Lagerort *51* eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="afbf4-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="afbf4-200">Wählen Sie auf dem Mobilgerät das Menü aus, das den neuen Menüpunkt für das mobile Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="afbf4-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="afbf4-201">Wählen Sie für dieses Szenario **Ausgehend** aus.</span><span class="sxs-lookup"><span data-stu-id="afbf4-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="afbf4-202">Wählen Sie das Menüelement **Entnahmepositionen für Warengruppe** aus, um die Entnahme zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="afbf4-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="afbf4-203">Geben Sie den Wert für **Arbeitskennung** ein, den Sie in der vorherigen Prozedur notiert haben.</span><span class="sxs-lookup"><span data-stu-id="afbf4-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="afbf4-204">Sie sollten einen Entnahmeschritt sehen, in dem alle Entnahmepositionen für den Artikel *M9200* gruppiert sind. Außerdem sollten Sie eine Anweisung zur Entnahme von *7* Stück von Artikel *M9200* erhalten.</span><span class="sxs-lookup"><span data-stu-id="afbf4-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="afbf4-205">Auf dem Mobilgerät wurde die Entnahmearbeit für die drei Entnahmearbeitspositionen zu einem Entnahmeschritt für den Anwender zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="afbf4-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="afbf4-206">Bestätigen Sie den Entnahmeschritt.</span><span class="sxs-lookup"><span data-stu-id="afbf4-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="afbf4-207">Wechseln Sie zur Arbeitsseite für die Arbeitskennung. Sie werden feststellen, dass alle drei Entnahmepositionen für Artikel *M9200* gleichzeitig geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="afbf4-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="afbf4-208">Wechseln Sie zurück zum Mobilgerät und fahren Sie mit der Entnahme fort.</span><span class="sxs-lookup"><span data-stu-id="afbf4-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="afbf4-209">Arbeitsposition 4 für Artikel *M9201* sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="afbf4-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="afbf4-210">Da der Auftrag nur eine Arbeitsposition enthielt, gibt es nichts zu aggregieren.</span><span class="sxs-lookup"><span data-stu-id="afbf4-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="afbf4-211">Bestätigen Sie den Entnahmeschritt.</span><span class="sxs-lookup"><span data-stu-id="afbf4-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="afbf4-212">Der letzte Entnahmeschritt auf dem Mobilgerät fasst die letzten beiden Entnahmepositionen aus dem Arbeitsauftrag zusammen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="afbf4-213">Führen Sie den Entnahmeschritt für *9* Stück von Artikel *M9202* durch.</span><span class="sxs-lookup"><span data-stu-id="afbf4-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="afbf4-214">Bestätigen Sie den Put-Schritt und alle weiteren Pick/Put-Paare, um die Arbeit abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="afbf4-215">Arbeitszeilen können nur dann gruppiert werden, wenn sie der Reihe nach vorliegen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="afbf4-216">Die folgende Funktionalität wird nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="afbf4-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="afbf4-217">Artikelgewichtsartikel</span><span class="sxs-lookup"><span data-stu-id="afbf4-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="afbf4-218">Wenn sich auf der Arbeit Catch-Weight-Artikel befinden, erhalten Sie eine Fehlermeldung, bevor Sie mit dem Kommissionieren beginnen.</span><span class="sxs-lookup"><span data-stu-id="afbf4-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="afbf4-219">Stückentnahme</span><span class="sxs-lookup"><span data-stu-id="afbf4-219">Piece picking</span></span>
>   - <span data-ttu-id="afbf4-220">Arbeitspositionen mit noch nicht abgeschlossenen Wiederbeschaffungsarbeiten</span><span class="sxs-lookup"><span data-stu-id="afbf4-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="afbf4-221">Zu hohe Entnahme</span><span class="sxs-lookup"><span data-stu-id="afbf4-221">Over-picking</span></span>
>   - <span data-ttu-id="afbf4-222">Artikelneuzuordnung für Entnahme mit unzureichender Menge</span><span class="sxs-lookup"><span data-stu-id="afbf4-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]