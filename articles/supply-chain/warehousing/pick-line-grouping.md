---
title: Gruppierung von Kommissionierpositionen
description: In diesem Thema wird eine Übersicht über die Gruppierung von Kommissionierpositionen angezeigt.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4b9cd7dac680c1691fb4c6dd4078f109254be784
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215595"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="1c7be-103">Gruppierung von Kommissionierpositionen</span><span class="sxs-lookup"><span data-stu-id="1c7be-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c7be-104">Bei der Kommissionierliniengruppierung können mehrere Arbeitslinien mit demselben Artikel und demselben Standort zu einer einzigen Kommissionierlinie zusammengefasst werden, die dem Benutzer auf einem mobilen Gerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c7be-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="1c7be-105">Daher können Lagerarbeiter die effizientesten Anweisungen erhalten, die möglich sind, aber die erforderliche Trennung der Arbeitslinien im System wird auch beibehalten (z. B. für verschiedene Container und Aufträge).</span><span class="sxs-lookup"><span data-stu-id="1c7be-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="1c7be-106">Gruppierung von Kommissionierpositionen einrichten</span><span class="sxs-lookup"><span data-stu-id="1c7be-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="1c7be-107">Erstellen eines Menüelements für ein mobiles Geräts</span><span class="sxs-lookup"><span data-stu-id="1c7be-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="1c7be-108">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüelemente für mobile Geräte**, und erstellen Sie ein neues Menüelement mit dem Namen **Entnahmepositionen für Warengruppe – Benutzergesteuert**.</span><span class="sxs-lookup"><span data-stu-id="1c7be-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="1c7be-109">Legen Sie unter **Menüoptionen für das mobile Gerät** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="1c7be-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="1c7be-110">Geben Sie im Feld **Menüelementname** die Option **Warenentnahme - Gruppenposition** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="1c7be-111">Geben Sie im Feld **Titel** die Option **Warenentnahme - Gruppenposition** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="1c7be-112">Wählen Sie im Feld **Modus** **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="1c7be-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="1c7be-113">Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="1c7be-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="1c7be-114">Legen Sie auf dem Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="1c7be-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="1c7be-115">Wählen Sie im Feld **Geleitet von** die Option **Benutzergesteuert** fest.</span><span class="sxs-lookup"><span data-stu-id="1c7be-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="1c7be-116">Legen Sie die Option **Ladungsträger generieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="1c7be-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="1c7be-117">Legen Sie die Option **Gruppenentnahme** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="1c7be-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="1c7be-118">Befolgen Sie im Inforegister **Arbeitsklassen** diese Schritte, um gültige Arbeitsklassen für den Menüpunkt für mobile Geräte zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="1c7be-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="1c7be-119">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-119">Select **New**.</span></span>
    2. <span data-ttu-id="1c7be-120">Wählen Sie im Feld **Arbeitsklassenkennung** die Option **Verkäufe** oder **SO Entnahme** aus, je nachdem, welchen Lagerort Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c7be-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="1c7be-121">Wählen Sie im Feld **Arbeitsauftragsart** **Arbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="1c7be-122">Menü des mobilen Geräts einrichten</span><span class="sxs-lookup"><span data-stu-id="1c7be-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="1c7be-123">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="1c7be-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="1c7be-124">Fügen Sie den soeben erstellten Menüeintrag zum gewünschten Menü hinzu.</span><span class="sxs-lookup"><span data-stu-id="1c7be-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="1c7be-125">Eine Arbeitsvorlage einrichten</span><span class="sxs-lookup"><span data-stu-id="1c7be-125">Set up a work template</span></span>

1. <span data-ttu-id="1c7be-126">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="1c7be-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1c7be-127">Suchen Sie die Arbeitsvorlage, die mit dieser Funktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c7be-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="1c7be-128">Wählen Sie für dieses Beispiel die standardmäßige Contoso-Arbeitsvorlage **51 Pick to stage** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="1c7be-129">Wählen Sie im Menü **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="1c7be-130">Wählen Sie auf der Registerkarte **Sortierung** die Option **Hinzufügen** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="1c7be-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="1c7be-131">Wählen Sie im Feld **Tabelle** die Option **Temporäre Arbeitstransaktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="1c7be-132">Wählen Sie im Feld **Abgeleitete Tabelle** die Option **Temporäre Arbeitstransaktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="1c7be-133">Wählen Sie im Feld **Feld** die Option **Artikelnummer** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="1c7be-134">Wählen Sie im Feld **Suchrichtung** die Option **Aufsteigend** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="1c7be-135">Damit die Funktion zum Gruppieren von Auswahlzeilen funktioniert, müssen die Arbeitszeilen nach Artikel-ID sortiert sein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="1c7be-136">Wenn Zeilen mit denselben Elementen nicht nacheinander sequenziert werden, werden sie nicht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="1c7be-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="1c7be-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1c7be-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="1c7be-138">Entnahmearbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="1c7be-138">Create picking work</span></span>

<span data-ttu-id="1c7be-139">Bevor Sie die Gruppierung von Kommissionierpositionen einrichten können, müssen Sie geeignete ausgehende Arbeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="1c7be-140">Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="1c7be-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="1c7be-141">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="1c7be-142">Wählen Sie im Feld **Debitorenkonto** einen Debitor aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="1c7be-143">Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagerort** die Option **51** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="1c7be-144">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-144">Then select **OK**.</span></span>
5. <span data-ttu-id="1c7be-145">Fügen Sie unter **Auftragspositionen** die folgenden sechs Zeilen hinzu:</span><span class="sxs-lookup"><span data-stu-id="1c7be-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="1c7be-146">**Position 1:** Wählen Sie im Feld **Artikelnummer** die Option **M9200** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="1c7be-147">Geben Sie im Feld **Menge** den Wert **3** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="1c7be-148">**Position 2:** Wählen Sie im Feld **Artikelnummer** die Option **M9201** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="1c7be-149">Geben Sie im Feld **Menge** den Wert **3** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="1c7be-150">**Position 3:** Wählen Sie im Feld **Artikelnummer** die Option **M9202** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="1c7be-151">Geben Sie im Feld **Menge** den Wert **2** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="1c7be-152">**Position 4:** Wählen Sie im Feld **Artikelnummer** die Option **M9200** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="1c7be-153">Geben Sie im Feld **Menge** den Wert **1** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="1c7be-154">**Position 5:** Wählen Sie im Feld **Artikelnummer** die Option **M9200** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="1c7be-155">Geben Sie im Feld **Menge** den Wert **3** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="1c7be-156">**Position 6:** Wählen Sie im Feld **Artikelnummer** die Option **M9202** aus.</span><span class="sxs-lookup"><span data-stu-id="1c7be-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="1c7be-157">Geben Sie im Feld **Menge** den Wert **7** ein.</span><span class="sxs-lookup"><span data-stu-id="1c7be-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="1c7be-158">Hier ist eine Zusammenfassung der Gesamtmengen für jeden Artikel:</span><span class="sxs-lookup"><span data-stu-id="1c7be-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="1c7be-159">**Artikel M9200:** 7 Stück</span><span class="sxs-lookup"><span data-stu-id="1c7be-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="1c7be-160">**Artikel M9201:** 3 Stück</span><span class="sxs-lookup"><span data-stu-id="1c7be-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="1c7be-161">**Artikel M9202:** 9 Stück</span><span class="sxs-lookup"><span data-stu-id="1c7be-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="1c7be-162">Bevor Sie die Bestellungen an das Lager freigeben, müssen Sie sicherstellen, dass die Kommissionierstellen über genügend Lagerbestand für alle Artikel in allen Bestellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="1c7be-163">Überprüfen Sie die Einstellung **Standortrichtlinie**, um zu bestimmen, welche Kommissionierorte für die Kundenauftragskommissionierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c7be-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="1c7be-164">Reservieren Sie das Inventar und geben Sie es an das Lager frei.</span><span class="sxs-lookup"><span data-stu-id="1c7be-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="1c7be-165">Eine Arbeitskennung mit sechs Zeilen wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c7be-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="1c7be-166">Die Zeilen sind nach Artikelnummer sortiert.</span><span class="sxs-lookup"><span data-stu-id="1c7be-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="1c7be-167">Den Ablauf für mobile Geräte ausführen</span><span class="sxs-lookup"><span data-stu-id="1c7be-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="1c7be-168">Wählen Sie auf dem Mobilgerät das Menü aus, das den neuen Menüpunkt für das mobile Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="1c7be-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="1c7be-169">Wählen Sie das Menüelement **Warenentnahme – Gruppenposition** aus, und initiieren Sie die Entnahme.</span><span class="sxs-lookup"><span data-stu-id="1c7be-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="1c7be-170">Nachdem Sie das Menü ausgewählt und die Arbeits-ID eingegeben haben, wird der Auswahlschritt angezeigt, in dem alle Auswahlzeilen für Artikel M9200 gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="1c7be-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="1c7be-171">Sie erhalten die Anweisung, jeweils 7 von Artikel M9200 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="1c7be-172">Bestätigen Sie den Entnahmeschritt.</span><span class="sxs-lookup"><span data-stu-id="1c7be-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="1c7be-173">Gehen Sie zum Mandantenbild der Ware in Arbeit und stellen Sie fest, dass alle drei Kommissionierzeilen für Position M9200 gleichzeitig geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="1c7be-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="1c7be-174">Arbeitslinie 4 wird vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="1c7be-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="1c7be-175">Bestätigen Sie den Entnahmeschritt.</span><span class="sxs-lookup"><span data-stu-id="1c7be-175">Confirm the pick step.</span></span>

    <span data-ttu-id="1c7be-176">Der letzte Entnahmeschritt auf dem Mobilgerät fasst die letzten beiden Entnahmepositionen aus dem Arbeitsauftrag zusammen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="1c7be-177">Führen Sie den Pick-Schritt für 9 Artikel M9202 durch.</span><span class="sxs-lookup"><span data-stu-id="1c7be-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="1c7be-178">Bestätigen Sie den Put-Schritt und alle weiteren Pick/Put-Paare, um die Arbeit abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="1c7be-179">Arbeitszeilen können nur dann gruppiert werden, wenn sie der Reihe nach vorliegen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="1c7be-180">Die folgende Funktionalität wird nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1c7be-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="1c7be-181">Artikelgewichtsartikel.</span><span class="sxs-lookup"><span data-stu-id="1c7be-181">Catch-weight items.</span></span> <span data-ttu-id="1c7be-182">Wenn sich auf der Arbeit Catch-Weight-Artikel befinden, erhalten Sie eine Fehlermeldung, bevor Sie mit dem Kommissionieren beginnen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="1c7be-183">Stückentnahme.</span><span class="sxs-lookup"><span data-stu-id="1c7be-183">Piece picking.</span></span>
>    - <span data-ttu-id="1c7be-184">Arbeitspositionen, für die noch Wiederbeschaffungsarbeiten durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1c7be-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="1c7be-185">Zu hohe Entnahme.</span><span class="sxs-lookup"><span data-stu-id="1c7be-185">Over-picking.</span></span>
