---
title: Zuteilung von Zeitfenstern für Lagerort
description: Dieser Artikel enthält Informationen zur Zuteilung von Zeitfenstern für den Lagerort. Mit der Zuteilung von Zeitfenstern für den Lagerort können Sie die Nachfrage nach Artikeln und Maßeinheiten aus Bestellungen mit dem Status „Bestellt“, „Reserviert“ oder „Freigegeben“ konsolidieren. Es hilft Lagerverwaltern, Entnahmeorte intelligent zu planen, bevor sie Aufträge für den Lagerort freigeben und Kommissionierarbeiten erstellen.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993752"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="39bb1-105">Zuteilung von Zeitfenstern für Lagerort</span><span class="sxs-lookup"><span data-stu-id="39bb1-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39bb1-106">Es stehen mehrere Funktionen für Lagerorte zur Verfügung, um Lagerleiter bei der intelligenten Planung von Lagerplätzen zu unterstützen, bevor sie Aufträge an das Lager freigeben und Entnahmearbeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="39bb1-107">Mit der Funktion *Lagerorteinteilung* können Sie die Nachfrage nach Elementen und Maßeinheiten von Aufträgen konsolidieren, die den Status *Bestellt*, *Reserviert* oder *Freigegeben* haben.</span><span class="sxs-lookup"><span data-stu-id="39bb1-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="39bb1-108">Der generierte Bedarf kann dann auf Lagerplätze angewendet werden, die für die Kommissionierung verwendet werden, basierend auf Menge, Einheit, physischen Dimensionen, festen Lagerplätzen und mehr.</span><span class="sxs-lookup"><span data-stu-id="39bb1-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="39bb1-109">Nachdem der Plan für die Zuteilung von Zeitfenstern erstellt wurde, können Wiederbeschaffungsarbeiten erstellt werden, um die entsprechende Menge an Bestand an jeden Lagerplatz zu bringen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="39bb1-110">Mit der Funktion *Lagerplätze für Transportaufträge* können Lagerort-Verwalter Wiederbeschaffung betreiben, basierend auf der Nachfrage von Transportaufträgen, die noch nicht für das Lager freigegeben sind.</span><span class="sxs-lookup"><span data-stu-id="39bb1-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="39bb1-111">Sie stellt sicher, dass die Lagerorte alle Elemente enthalten, die für die Transportaufträge benötigt werden, nachdem sie für das Lager freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="39bb1-112">Diese Funktion setzt voraus, dass Sie auch die Funktion *Lagerorte einlagern* einschalten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="39bb1-113">Die Funktion *Erweiterung der Lagerort-Zuweisung* fügt eine Option für die Vorlagenzeilen hinzu, die von der Funktion *Lagerort-Zuweisung* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="39bb1-114">Die Option ermöglicht es dem System, den vorhandenen Bestand an einem Lagerplatz zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="39bb1-115">Daher werden möglicherweise weniger Wiederbeschaffungen für die Platzierung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="39bb1-116">Die Funktion *Erweiterung der Lagerort-Zuweisung* erfordert, dass Sie auch die Funktion *Lagerort-Zuweisung* einschalten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="39bb1-117">Sie kann optional zusammen mit der Funktion *Lagerort-Zuteilung für Transportaufträge* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="39bb1-118">Einschalten der Funktionen für den Lagerort</span><span class="sxs-lookup"><span data-stu-id="39bb1-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="39bb1-119">Bevor Sie diese Funktionen verwenden können, müssen sie in Ihrem System eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="39bb1-120">Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktionen überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39bb1-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="39bb1-121">Schalten Sie die folgenden Funktionen je nach Bedarf ein:</span><span class="sxs-lookup"><span data-stu-id="39bb1-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="39bb1-122">Lagerortzeitrahmen-Funktion</span><span class="sxs-lookup"><span data-stu-id="39bb1-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="39bb1-123">Lagerort Einlagerung für Transportaufträge</span><span class="sxs-lookup"><span data-stu-id="39bb1-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="39bb1-124">Die Funktion *Lagerort-Zuteilung* muss vor dieser Funktion eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="39bb1-125">Erweiterungen für die Lagerort-Zuweisung (Zuteilung von Zeitfenstern )</span><span class="sxs-lookup"><span data-stu-id="39bb1-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="39bb1-126">Die Funktion *Lagerort-Zuteilung* muss vor dieser Funktion eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="39bb1-127">Zuteilung von Zeitfenstern für den Lagerort einrichten</span><span class="sxs-lookup"><span data-stu-id="39bb1-127">Set up warehouse slotting</span></span>

<span data-ttu-id="39bb1-128">Um die Lagerort-Zuteilung zu verwenden, müssen Sie die folgenden Elemente in Ihrem System festlegen:</span><span class="sxs-lookup"><span data-stu-id="39bb1-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="39bb1-129">Maßeinheitsebenen für die Zuteilung von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="39bb1-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="39bb1-130">Richtliniencodes</span><span class="sxs-lookup"><span data-stu-id="39bb1-130">Directive codes</span></span>
- <span data-ttu-id="39bb1-131">Vorlagen für die Zuteilung von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="39bb1-131">Slotting templates</span></span>
- <span data-ttu-id="39bb1-132">Lagerplatzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="39bb1-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="39bb1-133">Maßeinheitsstufen für Zuteilung von Zeitfenstern erstellen</span><span class="sxs-lookup"><span data-stu-id="39bb1-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="39bb1-134">Mithilfe von Maßeinheitsstufen können mehrere Maßeinheiten zum Zwecke der Zuteilung von Zeitfenstern zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="39bb1-135">Wenn beispielsweise mehrere Kistengrößen aus demselben Kistenauswahlbereich ausgewählt werden, kann für alle Größen eine Stufe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="39bb1-136">**Für jede Maßeinheit, die Teil der Stufe sein soll, muss eine Position erstellt werden.**</span><span class="sxs-lookup"><span data-stu-id="39bb1-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="39bb1-137">Gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Maßeinheitsstufen für Zuteilung von Zeitfenstern**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="39bb1-138">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-138">Select **New**.</span></span>
1. <span data-ttu-id="39bb1-139">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="39bb1-140">**Maßeinheitsstufe:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="39bb1-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="39bb1-141">**Beschreibung:** *Jede Kistenpalette*</span><span class="sxs-lookup"><span data-stu-id="39bb1-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="39bb1-142">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-142">Select **Save**.</span></span>
1. <span data-ttu-id="39bb1-143">Wählen Sie im Inforegister **Maßeinheiten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="39bb1-144">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-145">**Einheit:** *Kiste*</span><span class="sxs-lookup"><span data-stu-id="39bb1-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="39bb1-146">**Beschreibung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="39bb1-147">Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="39bb1-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="39bb1-148">**Einheitenklasse:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="39bb1-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="39bb1-149">Wählen Sie **Neu** aus, um dem Raster eine zweite Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="39bb1-150">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-151">**Einheit:** *ea*</span><span class="sxs-lookup"><span data-stu-id="39bb1-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="39bb1-152">**Beschreibung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="39bb1-153">Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="39bb1-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="39bb1-154">**Einheitenklasse:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="39bb1-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="39bb1-155">Wählen Sie **Neu** aus, um dem Raster eine dritte Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="39bb1-156">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-157">**Einheit:** *PL*</span><span class="sxs-lookup"><span data-stu-id="39bb1-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="39bb1-158">**Beschreibung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="39bb1-159">Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="39bb1-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="39bb1-160">**Einheitenklasse:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="39bb1-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="39bb1-161">Wählen Sie **Speichern** aus, um die Stufe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="39bb1-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="39bb1-162">Richtliniencode für Zuteilung von Zeitfenstern erstellen</span><span class="sxs-lookup"><span data-stu-id="39bb1-162">Create a directive code for slotting</span></span>

<span data-ttu-id="39bb1-163">Sie müssen den Richtliniencode auswählen, der einer Vorlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39bb1-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="39bb1-164">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Richtliniencodes**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="39bb1-165">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="39bb1-166">Geben Sie im Feld **Richtliniencode** *Zuteilung von Zeitfenstern* ein.</span><span class="sxs-lookup"><span data-stu-id="39bb1-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="39bb1-167">Geben Sie im Feld **Richtlinienbeschreibung** *Zuteilung von Zeitfenstern* ein.</span><span class="sxs-lookup"><span data-stu-id="39bb1-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="39bb1-168">Vorlagen für Zuteilung von Zeitfenstern einrichten</span><span class="sxs-lookup"><span data-stu-id="39bb1-168">Set up slotting templates</span></span>

<span data-ttu-id="39bb1-169">Jede Vorlage für die Zuteilung von Zeitfenstern steuert, wie der Bestand den Lagerplätzen für einen bestimmten Lagerort zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="39bb1-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="39bb1-170">Jede Vorlage muss eine Position für jede Spezifikation für die Zuteilung von Zeitfenstern enthalten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="39bb1-171">Verwenden Sie die in diesem Abschnitt beschriebenen Verfahren, um Vorlagen für die Zuteilung von Zeitfenstern einzurichten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="39bb1-172">Gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Vorlagen für Zuteilung von Zeitfenstern**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="39bb1-173">Wählen Sie **Neu** aus, um eine Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-173">Select **New** to create a template.</span></span>

<span data-ttu-id="39bb1-174">Als Nächstes müssen Sie den Vorlagenkopf, die Spezifikationen für die Zuteilung von Zeitfenstern und die Lagerplatzrichtlinien einrichten, wie in den folgenden Unterabschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="39bb1-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="39bb1-175">Das Einrichten der Lageraufteilung für Transportaufträge ähnelt dem Einrichten der Lageraufteilung für Verkaufsaufträge, aber das Feld **Auftragsart** ist auf *Transportaufträge* anstelle von *Verkaufsauftrag* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="39bb1-176">Festlegen der Kopfzeile für eine Vorlage für die Zuteilung von Zeitfenstern von Verkaufsaufträgen</span><span class="sxs-lookup"><span data-stu-id="39bb1-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="39bb1-177">Legen Sie in der Kopfzeile der Vorlage die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="39bb1-178">**Vorlage für die Zuteilung von Zeitfenstern:** _61_</span><span class="sxs-lookup"><span data-stu-id="39bb1-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="39bb1-179">**Beschreibung:** _61_</span><span class="sxs-lookup"><span data-stu-id="39bb1-179">**Description:** _61_</span></span>
    - <span data-ttu-id="39bb1-180">**Bedarfstyp:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="39bb1-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="39bb1-181">Derzeit sind *Verkaufsaufträge* und *Transferaufträge* die einzigen Bedarfsarten, die unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="39bb1-182">Sie können *Transportaufträge* nur auswählen, wenn die Funktion *Lagerort Zuteilung von Zeitfenstern für Transportaufträge* eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="39bb1-183">**Bedarfsstrategie:** _Bestellt_</span><span class="sxs-lookup"><span data-stu-id="39bb1-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="39bb1-184">In diesem Feld stehen folgende Werte zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="39bb1-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="39bb1-185">**Bestellt** – Die volle Bestellmenge auf dem Auftrag sollte als Bedarf betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="39bb1-186">**Reserviert** – Nur die reservierten (physischen und bestellten) Auftragspositionsmengen sollten als Bedarf betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="39bb1-187">**Freigegeben** - Die freigegebene Menge soll als Bedarf betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="39bb1-188">**Lagerort:** _61_</span><span class="sxs-lookup"><span data-stu-id="39bb1-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="39bb1-189">**Wellenbedarf die Nutzung nicht reservierter Mengen gestatten:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="39bb1-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="39bb1-190">Sie können auch eine Abfrage angeben, um den Umfang des ausgewerteten Bedarfs einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="39bb1-191">Spezifikationen für Zuteilung von Zeitfenstern für jede Vorlage einrichten</span><span class="sxs-lookup"><span data-stu-id="39bb1-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="39bb1-192">Führen Sie für jede Verkaufsauftragsvorlage, die Sie erstellen, die folgenden Schritte aus, um eine Zeile für jede Zuteilung von Zeitfenstern-Spezifikation hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="39bb1-193">Wählen Sie im Inforegister **Vorlagendetails für Zuteilung von Zeitfenstern** die Option **Neu** aus, um eine Vorlagenposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="39bb1-194">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-195">**Sequenz:** _1_</span><span class="sxs-lookup"><span data-stu-id="39bb1-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="39bb1-196">**Beschreibung:** _Fester Lagerplatz_</span><span class="sxs-lookup"><span data-stu-id="39bb1-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="39bb1-197">**Mindestmenge:** _1_</span><span class="sxs-lookup"><span data-stu-id="39bb1-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="39bb1-198">Dieses Feld definiert die Mindestbedarfsmenge, die für die Position erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="39bb1-199">**Höchstmenge:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="39bb1-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="39bb1-200">Dieses Feld definiert die Höchstbedarfsmenge, die für die Position gültig ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="39bb1-201">**Einheit:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="39bb1-202">Dieses Feld definiert die Maßeinheit, auf die sich die minimalen und maximalen Mengen beziehen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="39bb1-203">**Maßeinheitsstufe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="39bb1-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="39bb1-204">Dieses Feld definiert die Bedarfsmaßeinheiten, die für die Position gültig sind.</span><span class="sxs-lookup"><span data-stu-id="39bb1-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="39bb1-205">(Weitere Informationen erhalten Sie im Abschnitt [Maßeinheitsstufen für Zuteilung von Zeitfenstern einrichten](#unit-tiers) weiter oben in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="39bb1-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="39bb1-206">**Kriterien für Zuteilung von Zeitfenstern zuweisen:** _Menge betrachten_</span><span class="sxs-lookup"><span data-stu-id="39bb1-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="39bb1-207">In diesem Feld stehen folgende Werte zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="39bb1-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="39bb1-208">**Angenommen leer** – Dieses System sollte davon ausgehen, dass alle Lagerplätze im Kommissionierbereich leer sind, und diese Lagerplätze nicht auf Bestand prüfen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="39bb1-209">**Menge betrachten** – Das System sollte die Lagerplätze im Kommissionierbereich auf Bestand überprüfen und alle Lagerplätze überspringen, die nicht leer sind.</span><span class="sxs-lookup"><span data-stu-id="39bb1-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="39bb1-210">**Bestandsmäßig berücksichtigen** - Das System sollte prüfen, ob irgendein Ziellagerplatz nicht reservierte Mengen für das Element in der Bedarfszeile enthält.</span><span class="sxs-lookup"><span data-stu-id="39bb1-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="39bb1-211">Wenn die Menge groß genug ist, um mindestens eine Einheit der Bedarfszeile zu befriedigen, wird der generierte Zuteilung von Zeitfenstern-Plan-Datensatz um die verfügbare Menge reduziert.</span><span class="sxs-lookup"><span data-stu-id="39bb1-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="39bb1-212">Wenn der Bedarf z. B. 10 Kisten beträgt und eine Kiste vorrätig ist, beträgt der lokalisierte Bedarf neun Kisten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="39bb1-213">Wenn der Bedarf 10 Fälle beträgt und jeweils ein Fall vorhanden ist, beträgt der geortete Bedarf 10 Fälle.</span><span class="sxs-lookup"><span data-stu-id="39bb1-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="39bb1-214">Dieser Wert ist nur verfügbar, wenn die Funktion *Erweiterungen für die Lagerort-Zuweisung* eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="39bb1-215">**Richtliniencode:** _Zuteilung von Zeitfenstern_</span><span class="sxs-lookup"><span data-stu-id="39bb1-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="39bb1-216">Dieses Feld definiert die Lagerplatzrichtlinie, mit der der Kommissionierort der Wiederbeschaffungsarbeiten ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="39bb1-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="39bb1-217">**Überlauflagerplatz:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="39bb1-218">Dieses Feld definiert den Lagerplatz, an den der Bestand eingelagert wird, wenn bei der Verarbeitung der Position kein Lagerplatz für die Menge gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="39bb1-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="39bb1-219">**Pause zulassen:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="39bb1-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="39bb1-220">Wenn diese Option auf *Ja* festgelegt ist, wenn die Zuteilung von Zeitfenstern für Bedarf nicht möglich ist, werden Bewegungsarbeiten erstellt, um Bestand von Lagerplätzen zu entfernen, an denen Bestand vorhanden ist, an denen jedoch keine Zuteilung von Zeitfenstern durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="39bb1-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="39bb1-221">Die Vorlage wird dann erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-221">The template is then run again.</span></span> <span data-ttu-id="39bb1-222">Dieses Mal wird der Bestand an den Lagerplätzen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="39bb1-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="39bb1-223">Diese Funktionalität funktioniert am besten, wenn das Feld **Kriterien für Zuteilung von Zeitfenstern zuweisen** auf _Menge betrachten_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="39bb1-224">**Feste Lagerplatznutzung:** _Nur feste Lagerplätze für das Produkt_</span><span class="sxs-lookup"><span data-stu-id="39bb1-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="39bb1-225">In diesem Feld stehen folgende Werte zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="39bb1-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="39bb1-226">**Feste und nicht feste Lagerplätze** – Das System sollte nicht darauf beschränkt sein, nur feste Lagerplätze zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="39bb1-227">**Nur feste Lagerplätze für das Produkt** – Das System sollte nur an Lagerplätze eingesetzt werden, die feste Lagerplätze für das Produkt sind.</span><span class="sxs-lookup"><span data-stu-id="39bb1-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="39bb1-228">**Nur feste Lagerplätze für die Produktvariante** – Das System sollte nur an Lagerplätze eingesetzt werden, die feste Lagerplätze für die Produktvariante sind.</span><span class="sxs-lookup"><span data-stu-id="39bb1-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="39bb1-229">Wenn die Slot-Vorlage mindestens eine Zeile enthält, in der das Feld **Slot-Zuordnungskriterien** auf *Vorhandenes berücksichtigen* festgelegt ist, sind für keine Zeile in der Vorlage mehr Aufschläge erlaubt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="39bb1-230">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-230">Select **Save**.</span></span>
1. <span data-ttu-id="39bb1-231">Wählen Sie **Neu** aus, um eine zweite Vorlagenposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="39bb1-232">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-233">**Sequenz:** _2_</span><span class="sxs-lookup"><span data-stu-id="39bb1-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="39bb1-234">**Beschreibung:** _Sonstige_</span><span class="sxs-lookup"><span data-stu-id="39bb1-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="39bb1-235">**Mindestmenge:** _1_</span><span class="sxs-lookup"><span data-stu-id="39bb1-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="39bb1-236">**Höchstmenge:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="39bb1-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="39bb1-237">**Einheit:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="39bb1-238">**Maßeinheitsstufe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="39bb1-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="39bb1-239">**Kriterien für Zuteilung von Zeitfenstern zuweisen:** _Menge betrachten_</span><span class="sxs-lookup"><span data-stu-id="39bb1-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="39bb1-240">**Richtliniencode:** _Zuteilung von Zeitfenstern_</span><span class="sxs-lookup"><span data-stu-id="39bb1-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="39bb1-241">**Überlauflagerplatz:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="39bb1-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="39bb1-242">**Pause zulassen:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="39bb1-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="39bb1-243">**Feste Lagerplätze nutzen:** _Feste und nicht feste Lagerplätze_</span><span class="sxs-lookup"><span data-stu-id="39bb1-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="39bb1-244">In der Abfrage für die zweite Position geben Sie nun die Kriterien an, anhand derer bestimmt wird, an welchen Lagerplätzen die Zuteilung von Zeitfenstern für den Bestand für diese Position möglich ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="39bb1-245">Wählen Sie die Position aus, in der das Feld **Sequenz** auf *2* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="39bb1-246">Wählen Sie **Abfrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="39bb1-247">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="39bb1-248">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-249">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="39bb1-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="39bb1-250">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="39bb1-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="39bb1-251">**Feld:** *Lagerortprofilkennung*</span><span class="sxs-lookup"><span data-stu-id="39bb1-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="39bb1-252">**Kriterien:** *Pick-06* (Wählen Sie das doppelte Pluszeichen \[**++**\] im Feld, um die Liste zu erweitern, und wählen Sie dann *Pick-06* - *Kommissionierstelle 6*.)</span><span class="sxs-lookup"><span data-stu-id="39bb1-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="39bb1-253">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="39bb1-254">Lagerplatzrichtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="39bb1-254">Set up location directives</span></span>

<span data-ttu-id="39bb1-255">Es muss mindestens eine Lagerplatzrichtlinie eingerichtet werden, um die Zuteilung von Zeitfenstern für Entnahmen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="39bb1-256">Verwenden Sie die Verfahren in diesem Abschnitt, um eine neue *Wiederbeschaffungslagerplatzrichtlinie* für die Zuteilung von Zeitfenstern für Entnahmen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="39bb1-257">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="39bb1-258">Wählen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Wiederbeschaffung* aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="39bb1-259">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="39bb1-260">Geben Sie in der Kopfzeile für die neue Lagerplatzrichtlinie im Feld **Name** *61 Zuteilung von Zeitfenstern für Entnahmen* ein.</span><span class="sxs-lookup"><span data-stu-id="39bb1-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="39bb1-261">Übernehmen Sie im Feld **Sequenznummer** den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="39bb1-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="39bb1-262">Inforegister „Lagerplatzrichtlinien“ konfigurieren</span><span class="sxs-lookup"><span data-stu-id="39bb1-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="39bb1-263">Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="39bb1-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="39bb1-264">Akzeptieren Sie die Standardwerte für alle anderen Felder.</span><span class="sxs-lookup"><span data-stu-id="39bb1-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="39bb1-265">**Arbeitstyp:** _Entnahme_</span><span class="sxs-lookup"><span data-stu-id="39bb1-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="39bb1-266">**Standort:** _6_</span><span class="sxs-lookup"><span data-stu-id="39bb1-266">**Site:** _6_</span></span>
    - <span data-ttu-id="39bb1-267">**Lagerort:** _61_</span><span class="sxs-lookup"><span data-stu-id="39bb1-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="39bb1-268">**Richtliniencode:** _Zuteilung von Zeitfenstern_</span><span class="sxs-lookup"><span data-stu-id="39bb1-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="39bb1-269">Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="39bb1-270">Inforegister „Positionen“ konfigurieren</span><span class="sxs-lookup"><span data-stu-id="39bb1-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="39bb1-271">Klicken Sie im Inforegister **Positionen** auf **Neu**, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="39bb1-272">Legen Sie die folgenden Werte für die neue Position fest.</span><span class="sxs-lookup"><span data-stu-id="39bb1-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="39bb1-273">**Von Menge:** _0_</span><span class="sxs-lookup"><span data-stu-id="39bb1-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="39bb1-274">**Bis Menge:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="39bb1-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="39bb1-275">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="39bb1-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="39bb1-276">Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="39bb1-277">Inforegister „Lagerplatzrichtlinienaktivitäten“ konfigurieren</span><span class="sxs-lookup"><span data-stu-id="39bb1-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="39bb1-278">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="39bb1-279">Legen Sie die folgenden Werte für die neue Position fest.</span><span class="sxs-lookup"><span data-stu-id="39bb1-279">On the new line, set the following values.</span></span> <span data-ttu-id="39bb1-280">Akzeptieren Sie die Standardwerte für alle anderen Felder.</span><span class="sxs-lookup"><span data-stu-id="39bb1-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="39bb1-281">**Sequenznummer:** Akzeptieren Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="39bb1-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="39bb1-282">**Name:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="39bb1-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="39bb1-283">**Strategie:** _Keine_</span><span class="sxs-lookup"><span data-stu-id="39bb1-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="39bb1-284">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="39bb1-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="39bb1-285">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="39bb1-286">Abfrage bearbeiten</span><span class="sxs-lookup"><span data-stu-id="39bb1-286">Edit the query</span></span>

1. <span data-ttu-id="39bb1-287">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="39bb1-288">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="39bb1-289">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-290">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="39bb1-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="39bb1-291">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="39bb1-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="39bb1-292">**Feld:** *Zonen-ID*</span><span class="sxs-lookup"><span data-stu-id="39bb1-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="39bb1-293">**Kriterien:** *Bulk* (Wählen Sie das doppelte Pluszeichen \[**++**\] im Feld, um die Liste zu erweitern, und wählen Sie dann *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="39bb1-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="39bb1-294">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="39bb1-295">Szenario</span><span class="sxs-lookup"><span data-stu-id="39bb1-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="39bb1-296">Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="39bb1-296">Set up the scenario</span></span>

<span data-ttu-id="39bb1-297">Verwenden Sie für dieses Szenario die integrierten Beispieldaten und erstellen Sie die in diesem Abschnitt beschriebenen Datensätze.</span><span class="sxs-lookup"><span data-stu-id="39bb1-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="39bb1-298">USMF-Beispieldaten verwenden</span><span class="sxs-lookup"><span data-stu-id="39bb1-298">Use the USMF sample data</span></span>

<span data-ttu-id="39bb1-299">Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="39bb1-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="39bb1-300">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="39bb1-301">Bedarf erstellen</span><span class="sxs-lookup"><span data-stu-id="39bb1-301">Create demand</span></span>

<span data-ttu-id="39bb1-302">Befolgen Sie diese Schritte, um den Bedarf zu erstellen, auf den Sie die Zuteilung von Zeitfenstern anwenden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="39bb1-303">Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="39bb1-304">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="39bb1-305">Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** _US-007_ aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="39bb1-306">Im Feld **Lagerort** wählen Sie _61_ aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="39bb1-307">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-307">Select **OK**.</span></span>
1. <span data-ttu-id="39bb1-308">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="39bb1-308">The new sales order is opened.</span></span> <span data-ttu-id="39bb1-309">Er enthält eine leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="39bb1-310">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-311">**Artikel:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="39bb1-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="39bb1-312">**Menge** _20_</span><span class="sxs-lookup"><span data-stu-id="39bb1-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="39bb1-313">Wählen Sie **Position hinzufügen** aus, um eine neue Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="39bb1-314">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="39bb1-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="39bb1-315">**Menge** _8_</span><span class="sxs-lookup"><span data-stu-id="39bb1-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="39bb1-316">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-316">Select **Save**.</span></span>
1. <span data-ttu-id="39bb1-317">Wählen Sie **Neu** aus, um einen zweiten Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="39bb1-318">Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** _US-008_ aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="39bb1-319">Im Feld **Lagerort** wählen Sie _61_ aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="39bb1-320">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="39bb1-320">The new sales order is opened.</span></span> <span data-ttu-id="39bb1-321">Er enthält eine leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="39bb1-322">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="39bb1-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="39bb1-323">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="39bb1-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="39bb1-324">**Menge** _1_</span><span class="sxs-lookup"><span data-stu-id="39bb1-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="39bb1-325">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="39bb1-326">Typisches Szenario für Zuteilung von Zeitfenstern durchgehen</span><span class="sxs-lookup"><span data-stu-id="39bb1-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="39bb1-327">Nachdem alle erforderlichen Elemente vorhanden sind, wie im vorherigen Abschnitt beschrieben, können Sie die Funktion ausprobieren, indem Sie jede Übung in diesem Abschnitt durcharbeiten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="39bb1-328">Bedarf generieren</span><span class="sxs-lookup"><span data-stu-id="39bb1-328">Generate demand</span></span>

1. <span data-ttu-id="39bb1-329">Navigieren Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Vorlagen für Zuteilung von Zeitfenstern**, und wählen Sie die Vorlage für die Zuteilung von Zeitfenstern aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="39bb1-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="39bb1-330">Wählen Sie im Aktivitätsbereich **Bedarf generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="39bb1-331">Dieser Befehl wertet den gesamten Bedarf aus, der sich im System befindet und mit der Vorlagenabfrage für die Zuteilung von Zeitfenstern übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="39bb1-332">Der Gesamtbedarf aller Bestellungen wird dann in einer Position pro Menge/Maßeinheit zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="39bb1-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="39bb1-333">Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="39bb1-334">Bedarf an der Zuteilung von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="39bb1-334">Slotting demand</span></span>

<span data-ttu-id="39bb1-335">Die *Zuteilung von Zeitfenstern für den Bedarf* zeigt die Ergebnisse der Bedarfsgenerierung basierend auf dem Setup der Vorlage für die Zuteilung von Zeitfenstern.</span><span class="sxs-lookup"><span data-stu-id="39bb1-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="39bb1-336">Wählen Sie im Aktivitätsbereich **Zuteilung von Zeitfenstern für den Bedarf** aus, um die Ergebnisse aus dem Befehl **Bedarf generieren** zu sehen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="39bb1-337">Die Positionen in der Zuteilung von Zeitfenstern für den Bedarf können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="39bb1-338">Sie können eine Position löschen, eine neue Position hinzufügen oder die Positionsdetails bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="39bb1-339">Sie können den Bedarf manuell bearbeiten oder mithilfe der Datenverwaltung von einem externen System importieren.</span><span class="sxs-lookup"><span data-stu-id="39bb1-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="39bb1-340">Was auch immer in der Zuteilung von Zeitfenstern für den Bedarf enthalten ist, wird im nächsten Schritt verwendet, unabhängig davon, woher es stammt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="39bb1-341">Bedarf ermitteln</span><span class="sxs-lookup"><span data-stu-id="39bb1-341">Locate demand</span></span>

<span data-ttu-id="39bb1-342">Nachdem der Bedarf generiert wurde, müssen Sie den Befehl **Bedarf ermitteln** verwenden, um den *Plan für die Zuteilung von Zeitfenstern* zu generieren.</span><span class="sxs-lookup"><span data-stu-id="39bb1-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="39bb1-343">Wählen Sie im Aktivitätsbereich **Bedarf ermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="39bb1-344">Der Vorgang für die Zuteilung von Zeitfenstern läuft.</span><span class="sxs-lookup"><span data-stu-id="39bb1-344">The slotting process runs.</span></span> <span data-ttu-id="39bb1-345">Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="39bb1-346">Plan für die Zuteilung von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="39bb1-346">Slotting plan</span></span>

<span data-ttu-id="39bb1-347">Der Plan für die Zuteilung von Zeitfenstern zeigt den Lagerplatz, dem jeder Artikel/jede Menge zugewiesen wurde, ob ein Überlauf verwendet wurde, ob Pausenarbeiten erstellt wurden und welche Vorlagenposition verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="39bb1-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="39bb1-348">*Jeder Bedarf, für den keine Zuteilung von Zeitfenstern möglich ist, wird rot hervorgehoben.*</span><span class="sxs-lookup"><span data-stu-id="39bb1-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="39bb1-349">Wählen Sie im Aktivitätsbereich **Plan für die Zuteilung von Zeitfenstern** aus, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="39bb1-350">Die Prozesse **Bedarf generieren**, **Bedarf lokalisieren** und **Wiederbeschaffung ausführen** werden jetzt in einer Sandbox ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="39bb1-351">(Diese Prozesse sind im Aktivitätsbereich auf der Seite **Nachschubvorlagen** verfügbar).</span><span class="sxs-lookup"><span data-stu-id="39bb1-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="39bb1-352">Die Prozesse **Bedarf generieren**, **Bedarf lokalisieren** und **Nachschub ausführen** haben eine Sperre, um sicherzustellen, dass sie nicht gleichzeitig ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="39bb1-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="39bb1-353">Andernfalls könnten die verwendeten Daten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="39bb1-354">Die Prozesse **Nachschub generieren** und **Nachschub lokalisieren** zeigen eine Warnung an, wenn der Lauf keine Datensätze generiert hat oder wenn in den Datensätzen Informationen fehlen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="39bb1-355">Wenn Sie **Bedarfsplan** wählen, hat die Seite keine Schaltflächen **Neu**, **Bearbeiten** oder **Löschen** im Aktivitätsbereich, weil die Datenquelle nicht bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="39bb1-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="39bb1-356">Wenn Sie **Wiederbeschaffung ausführen** wählen, validiert das System die ausgewählte Slot-Vorlage und die Prozesse.</span><span class="sxs-lookup"><span data-stu-id="39bb1-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="39bb1-357">Wiederbeschaffung erstellen</span><span class="sxs-lookup"><span data-stu-id="39bb1-357">Create replenishment</span></span>

<span data-ttu-id="39bb1-358">Nachdem der Plan für die Zuteilung von Zeitfenstern erstellt wurde, müssen Sie *Wiederbeschaffungsarbeiten* basierend auf dem Plan erstellen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="39bb1-359">Wählen Sie im Aktivitätsbereich **Wiederbeschaffung ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="39bb1-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="39bb1-360">Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39bb1-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="39bb1-361">Diese Nachricht gibt die Anzahl der Header an, die für die Arbeits-Build-ID erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="39bb1-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="39bb1-362">Zu verwendende Lagerplatzrichtlinien werden anhand des Richtliniencodes identifiziert, der in jeder Vorlagenposition angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="39bb1-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="39bb1-363">Tipps</span><span class="sxs-lookup"><span data-stu-id="39bb1-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="39bb1-364">Automatische Zuteilung von Zeitfenstern einrichten</span><span class="sxs-lookup"><span data-stu-id="39bb1-364">Set up automatic slotting</span></span>

<span data-ttu-id="39bb1-365">Nachdem alle erforderlichen Elemente vorhanden sind, können Sie die Zuteilung von Zeitfenstern so einrichten, dass sie automatisch ausgeführt wird, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="39bb1-366">Wechseln Sie zu **Lagerortverwaltung \> Wiederbeschaffung \> Zuteilung von Zeitfenstern ausführen**.</span><span class="sxs-lookup"><span data-stu-id="39bb1-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="39bb1-367">Geben Sie die auszuführenden Schritte für die Zuteilung von Zeitfenstern an.</span><span class="sxs-lookup"><span data-stu-id="39bb1-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="39bb1-368">Wählen Sie einen oder mehrere der folgenden Schritte für die Zuteilung von Zeitfenstern aus:</span><span class="sxs-lookup"><span data-stu-id="39bb1-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="39bb1-369">Bedarf generieren</span><span class="sxs-lookup"><span data-stu-id="39bb1-369">Generate demand</span></span>
    - <span data-ttu-id="39bb1-370">Bedarf ermitteln</span><span class="sxs-lookup"><span data-stu-id="39bb1-370">Locate demand</span></span>
    - <span data-ttu-id="39bb1-371">Wiederbeschaffungsarbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="39bb1-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="39bb1-372">Die Schritte für die Zuteilung von Zeitfenstern sind progressiv.</span><span class="sxs-lookup"><span data-stu-id="39bb1-372">The slotting steps are progressive.</span></span> <span data-ttu-id="39bb1-373">Wenn Sie *Bedarf ermitteln* auswählen möchten, müssen Sie zuerst *Bedarf generieren* auswählen.</span><span class="sxs-lookup"><span data-stu-id="39bb1-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="39bb1-374">Geben Sie die zu verwendende Vorlage für die Zuteilung von Zeitfenstern an.</span><span class="sxs-lookup"><span data-stu-id="39bb1-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="39bb1-375">Stellen Sie die Serie so ein, dass sie automatisch ausgeführt wird, wenn Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="39bb1-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="39bb1-376">Richten Sie für die Übungen im Szenario **nicht** die automatische Zuteilung von Zeitfenstern ein.</span><span class="sxs-lookup"><span data-stu-id="39bb1-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
