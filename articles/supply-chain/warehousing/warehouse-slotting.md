---
title: Zuteilung von Zeitfenstern für Lagerort
description: Dieser Artikel enthält Informationen zur Zuteilung von Zeitfenstern für den Lagerort. Mit der Zuteilung von Zeitfenstern für den Lagerort können Sie die Nachfrage nach Artikeln und Maßeinheiten aus Bestellungen mit dem Status „Bestellt“, „Reserviert“ oder „Freigegeben“ konsolidieren. Es hilft Lagerverwaltern, Entnahmeorte intelligent zu planen, bevor sie Aufträge für den Lagerort freigeben und Kommissionierarbeiten erstellen.
author: mirzaab
manager: AnnBe
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
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d9080f192db0c59b4b4bc74468491e86ba0b7471
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530350"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="73ba8-105">Zuteilung von Zeitfenstern für Lagerort</span><span class="sxs-lookup"><span data-stu-id="73ba8-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73ba8-106">Mit der Zuteilung von Zeitfenstern für den Lagerort können Sie die Nachfrage nach Artikeln und Maßeinheiten aus Bestellungen mit dem Status *Bestellt*, *Reserviert* oder *Freigegeben* konsolidieren.</span><span class="sxs-lookup"><span data-stu-id="73ba8-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="73ba8-107">Der generierte Bedarf kann dann auf Lagerplätze angewendet werden, die für die Kommissionierung verwendet werden, basierend auf Menge, Einheit, physischen Dimensionen, festen Lagerplätzen und mehr.</span><span class="sxs-lookup"><span data-stu-id="73ba8-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="73ba8-108">Nachdem der Plan für die Zuteilung von Zeitfenstern erstellt wurde, können Wiederbeschaffungsarbeiten erstellt werden, um die entsprechende Menge an Bestand an jeden Lagerplatz zu bringen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="73ba8-109">Diese Funktion hilft Lagerverwaltern, Entnahmeorte intelligent zu planen, bevor sie Aufträge für den Lagerort freigeben und Kommissionierarbeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="73ba8-110">Funktion für Zuteilung von Zeitfenstern für den Lagerort aktivieren</span><span class="sxs-lookup"><span data-stu-id="73ba8-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="73ba8-111">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="73ba8-112">Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="73ba8-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="73ba8-113">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="73ba8-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="73ba8-114">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="73ba8-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="73ba8-115">**Funktionsname:** *Funktion für Zuteilung von Zeitfenstern für den Lagerort*</span><span class="sxs-lookup"><span data-stu-id="73ba8-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="73ba8-116">Zuteilung von Zeitfenstern für den Lagerort einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-116">Set up warehouse slotting</span></span>

<span data-ttu-id="73ba8-117">Um die Zuteilung von Zeitfenstern für den Lagerort zu verwenden, müssen Sie die folgenden Elemente in Ihrem System einrichten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="73ba8-118">Maßeinheitsstufen für Zuteilung von Zeitfenstern erstellen</span><span class="sxs-lookup"><span data-stu-id="73ba8-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="73ba8-119">Mithilfe von Maßeinheitsstufen können mehrere Maßeinheiten zum Zwecke der Zuteilung von Zeitfenstern zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="73ba8-120">Wenn beispielsweise mehrere Kistengrößen aus demselben Kistenauswahlbereich ausgewählt werden, kann für alle Größen eine Stufe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="73ba8-121">**Für jede Maßeinheit, die Teil der Stufe sein soll, muss eine Position erstellt werden.**</span><span class="sxs-lookup"><span data-stu-id="73ba8-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="73ba8-122">Gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Maßeinheitsstufen für Zuteilung von Zeitfenstern**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="73ba8-123">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-123">Select **New**.</span></span>
1. <span data-ttu-id="73ba8-124">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="73ba8-125">**Maßeinheitsstufe:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="73ba8-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="73ba8-126">**Beschreibung:** *Jede Kistenpalette*</span><span class="sxs-lookup"><span data-stu-id="73ba8-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="73ba8-127">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-127">Select **Save**.</span></span>
1. <span data-ttu-id="73ba8-128">Wählen Sie im Inforegister **Maßeinheiten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="73ba8-129">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-130">**Einheit:** *Kiste*</span><span class="sxs-lookup"><span data-stu-id="73ba8-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="73ba8-131">**Beschreibung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="73ba8-132">Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="73ba8-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="73ba8-133">**Einheitenklasse:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="73ba8-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="73ba8-134">Wählen Sie **Neu** aus, um dem Raster eine zweite Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="73ba8-135">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-136">**Einheit:** *ea*</span><span class="sxs-lookup"><span data-stu-id="73ba8-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="73ba8-137">**Beschreibung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="73ba8-138">Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="73ba8-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="73ba8-139">**Einheitenklasse:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="73ba8-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="73ba8-140">Wählen Sie **Neu** aus, um dem Raster eine dritte Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="73ba8-141">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-142">**Einheit:** *PL*</span><span class="sxs-lookup"><span data-stu-id="73ba8-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="73ba8-143">**Beschreibung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="73ba8-144">Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="73ba8-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="73ba8-145">**Einheitenklasse:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="73ba8-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="73ba8-146">Wählen Sie **Speichern** aus, um die Stufe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="73ba8-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="73ba8-147">Richtliniencode für Zuteilung von Zeitfenstern erstellen</span><span class="sxs-lookup"><span data-stu-id="73ba8-147">Create a directive code for slotting</span></span>

<span data-ttu-id="73ba8-148">Sie müssen den Richtliniencode auswählen, der einer Vorlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73ba8-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="73ba8-149">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Richtliniencodes**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="73ba8-150">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="73ba8-151">Geben Sie im Feld **Richtliniencode** *Zuteilung von Zeitfenstern* ein.</span><span class="sxs-lookup"><span data-stu-id="73ba8-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="73ba8-152">Geben Sie im Feld **Richtlinienbeschreibung** *Zuteilung von Zeitfenstern* ein.</span><span class="sxs-lookup"><span data-stu-id="73ba8-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="73ba8-153">Vorlagen für Zuteilung von Zeitfenstern einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-153">Set up slotting templates</span></span>

<span data-ttu-id="73ba8-154">Jede Vorlage für die Zuteilung von Zeitfenstern steuert, wie der Bestand den Lagerplätzen für einen bestimmten Lagerort zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="73ba8-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="73ba8-155">Jede Vorlage muss eine Position für jede Spezifikation für die Zuteilung von Zeitfenstern enthalten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="73ba8-156">Verwenden Sie die in diesem Abschnitt beschriebenen Verfahren, um Vorlagen für die Zuteilung von Zeitfenstern einzurichten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="73ba8-157">Gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Vorlagen für Zuteilung von Zeitfenstern**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="73ba8-158">Wählen Sie **Neu** aus, um eine Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-158">Select **New** to create a template.</span></span>

<span data-ttu-id="73ba8-159">Als Nächstes müssen Sie den Vorlagenkopf, die Spezifikationen für die Zuteilung von Zeitfenstern und die Lagerplatzrichtlinien einrichten, wie in den folgenden Unterabschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="73ba8-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="73ba8-160">Vorlagenkopf für Zuteilung von Zeitfenstern einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="73ba8-161">Legen Sie in der Kopfzeile der Vorlage die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="73ba8-162">**Vorlage für die Zuteilung von Zeitfenstern:** _61_</span><span class="sxs-lookup"><span data-stu-id="73ba8-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="73ba8-163">**Beschreibung:** _61_</span><span class="sxs-lookup"><span data-stu-id="73ba8-163">**Description:** _61_</span></span>
    - <span data-ttu-id="73ba8-164">**Bedarfstyp:** *Auftrag*</span><span class="sxs-lookup"><span data-stu-id="73ba8-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="73ba8-165">Derzeit wird nur der Bedarfstyp *Auftrag* unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="73ba8-166">**Bedarfsstrategie:** _Bestellt_</span><span class="sxs-lookup"><span data-stu-id="73ba8-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="73ba8-167">In diesem Feld stehen folgende Werte zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="73ba8-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="73ba8-168">**Bestellt** – Die volle Bestellmenge auf dem Auftrag sollte als Bedarf betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="73ba8-169">**Reserviert** – Nur die reservierten (physischen und bestellten) Auftragspositionsmengen sollten als Bedarf betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="73ba8-170">**Lagerort:** _61_</span><span class="sxs-lookup"><span data-stu-id="73ba8-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="73ba8-171">**Wellenbedarf die Nutzung nicht reservierter Mengen gestatten:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="73ba8-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="73ba8-172">Sie können auch eine Abfrage angeben, um den Umfang des ausgewerteten Bedarfs einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="73ba8-173">Spezifikationen für Zuteilung von Zeitfenstern für jede Vorlage einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="73ba8-174">Befolgen Sie diese Schritte für jede Vorlage, die Sie erstellen, um eine Position für jede Spezifikation für die Zuteilung von Zeitfenstern hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="73ba8-175">Wählen Sie im Inforegister **Vorlagendetails für Zuteilung von Zeitfenstern** die Option **Neu** aus, um eine Vorlagenposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="73ba8-176">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-177">**Sequenz:** _1_</span><span class="sxs-lookup"><span data-stu-id="73ba8-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="73ba8-178">**Beschreibung:** _Fester Lagerplatz_</span><span class="sxs-lookup"><span data-stu-id="73ba8-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="73ba8-179">**Mindestmenge:** _1_</span><span class="sxs-lookup"><span data-stu-id="73ba8-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="73ba8-180">Dieses Feld definiert die Mindestbedarfsmenge, die für die Position erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="73ba8-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="73ba8-181">**Höchstmenge:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="73ba8-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="73ba8-182">Dieses Feld definiert die Höchstbedarfsmenge, die für die Position gültig ist.</span><span class="sxs-lookup"><span data-stu-id="73ba8-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="73ba8-183">**Einheit:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="73ba8-184">Dieses Feld definiert die Maßeinheit, auf die sich die minimalen und maximalen Mengen beziehen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="73ba8-185">**Maßeinheitsstufe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="73ba8-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="73ba8-186">Dieses Feld definiert die Bedarfsmaßeinheiten, die für die Position gültig sind.</span><span class="sxs-lookup"><span data-stu-id="73ba8-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="73ba8-187">(Weitere Informationen erhalten Sie im Abschnitt [Maßeinheitsstufen für Zuteilung von Zeitfenstern einrichten](#unit-tiers) weiter oben in diesem Thema.)</span><span class="sxs-lookup"><span data-stu-id="73ba8-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="73ba8-188">**Kriterien für Zuteilung von Zeitfenstern zuweisen:** _Menge betrachten_</span><span class="sxs-lookup"><span data-stu-id="73ba8-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="73ba8-189">In diesem Feld stehen folgende Werte zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="73ba8-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="73ba8-190">**Angenommen leer** – Dieses System sollte davon ausgehen, dass alle Lagerplätze im Kommissionierbereich leer sind, und diese Lagerplätze nicht auf Bestand prüfen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="73ba8-191">**Menge betrachten** – Das System sollte die Lagerplätze im Kommissionierbereich auf Bestand überprüfen und alle Lagerplätze überspringen, die nicht leer sind.</span><span class="sxs-lookup"><span data-stu-id="73ba8-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="73ba8-192">**Richtliniencode:** _Zuteilung von Zeitfenstern_</span><span class="sxs-lookup"><span data-stu-id="73ba8-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="73ba8-193">Dieses Feld definiert die Lagerplatzrichtlinie, mit der der Kommissionierort der Wiederbeschaffungsarbeiten ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="73ba8-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="73ba8-194">**Überlauflagerplatz:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="73ba8-195">Dieses Feld definiert den Lagerplatz, an den der Bestand eingelagert wird, wenn bei der Verarbeitung der Position kein Lagerplatz für die Menge gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="73ba8-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="73ba8-196">**Pause zulassen:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="73ba8-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="73ba8-197">Wenn diese Option auf *Ja* festgelegt ist, wenn die Zuteilung von Zeitfenstern für Bedarf nicht möglich ist, werden Bewegungsarbeiten erstellt, um Bestand von Lagerplätzen zu entfernen, an denen Bestand vorhanden ist, an denen jedoch keine Zuteilung von Zeitfenstern durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="73ba8-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="73ba8-198">Die Vorlage wird dann erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-198">The template is then run again.</span></span> <span data-ttu-id="73ba8-199">Dieses Mal wird der Bestand an den Lagerplätzen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="73ba8-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="73ba8-200">Diese Funktionalität funktioniert am besten, wenn das Feld **Kriterien für Zuteilung von Zeitfenstern zuweisen** auf _Menge betrachten_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73ba8-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="73ba8-201">**Feste Lagerplatznutzung:** _Nur feste Lagerplätze für das Produkt_</span><span class="sxs-lookup"><span data-stu-id="73ba8-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="73ba8-202">In diesem Feld stehen folgende Werte zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="73ba8-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="73ba8-203">**Feste und nicht feste Lagerplätze** – Das System sollte nicht darauf beschränkt sein, nur feste Lagerplätze zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="73ba8-204">**Nur feste Lagerplätze für das Produkt** – Das System sollte nur an Lagerplätze eingesetzt werden, die feste Lagerplätze für das Produkt sind.</span><span class="sxs-lookup"><span data-stu-id="73ba8-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="73ba8-205">**Nur feste Lagerplätze für die Produktvariante** – Das System sollte nur an Lagerplätze eingesetzt werden, die feste Lagerplätze für die Produktvariante sind.</span><span class="sxs-lookup"><span data-stu-id="73ba8-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="73ba8-206">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-206">Select **Save**.</span></span>
1. <span data-ttu-id="73ba8-207">Wählen Sie **Neu** aus, um eine zweite Vorlagenposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="73ba8-208">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-209">**Sequenz:** _2_</span><span class="sxs-lookup"><span data-stu-id="73ba8-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="73ba8-210">**Beschreibung:** _Sonstige_</span><span class="sxs-lookup"><span data-stu-id="73ba8-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="73ba8-211">**Mindestmenge:** _1_</span><span class="sxs-lookup"><span data-stu-id="73ba8-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="73ba8-212">**Höchstmenge:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="73ba8-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="73ba8-213">**Einheit:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="73ba8-214">**Maßeinheitsstufe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="73ba8-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="73ba8-215">**Kriterien für Zuteilung von Zeitfenstern zuweisen:** _Menge betrachten_</span><span class="sxs-lookup"><span data-stu-id="73ba8-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="73ba8-216">**Richtliniencode:** _Zuteilung von Zeitfenstern_</span><span class="sxs-lookup"><span data-stu-id="73ba8-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="73ba8-217">**Überlauflagerplatz:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="73ba8-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="73ba8-218">**Pause zulassen:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="73ba8-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="73ba8-219">**Feste Lagerplätze nutzen:** _Feste und nicht feste Lagerplätze_</span><span class="sxs-lookup"><span data-stu-id="73ba8-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="73ba8-220">In der Abfrage für die zweite Position geben Sie nun die Kriterien an, anhand derer bestimmt wird, an welchen Lagerplätzen die Zuteilung von Zeitfenstern für den Bestand für diese Position möglich ist.</span><span class="sxs-lookup"><span data-stu-id="73ba8-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="73ba8-221">Wählen Sie die Position aus, in der das Feld **Sequenz** auf *2* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73ba8-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="73ba8-222">Wählen Sie **Abfrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="73ba8-223">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="73ba8-224">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-225">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="73ba8-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="73ba8-226">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="73ba8-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="73ba8-227">**Feld:** *Lagerortprofilkennung*</span><span class="sxs-lookup"><span data-stu-id="73ba8-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="73ba8-228">**Kriterien:** *Pick-06* (Wählen Sie das doppelte Pluszeichen \[**++**\] im Feld, um die Liste zu erweitern, und wählen Sie dann *Pick-06* - *Kommissionierstelle 6*.)</span><span class="sxs-lookup"><span data-stu-id="73ba8-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="73ba8-229">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="73ba8-230">Lagerplatzrichtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-230">Set up location directives</span></span>

<span data-ttu-id="73ba8-231">Es muss mindestens eine Lagerplatzrichtlinie eingerichtet werden, um die Zuteilung von Zeitfenstern für Entnahmen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="73ba8-232">Verwenden Sie die Verfahren in diesem Abschnitt, um eine neue *Wiederbeschaffungslagerplatzrichtlinie* für die Zuteilung von Zeitfenstern für Entnahmen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="73ba8-233">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="73ba8-234">Wählen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Wiederbeschaffung* aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="73ba8-235">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="73ba8-236">Geben Sie in der Kopfzeile für die neue Lagerplatzrichtlinie im Feld **Name** *61 Zuteilung von Zeitfenstern für Entnahmen* ein.</span><span class="sxs-lookup"><span data-stu-id="73ba8-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="73ba8-237">Inforegister „Lagerplatzrichtlinien“ konfigurieren</span><span class="sxs-lookup"><span data-stu-id="73ba8-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="73ba8-238">Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="73ba8-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="73ba8-239">Akzeptieren Sie die Standardwerte für alle anderen Felder.</span><span class="sxs-lookup"><span data-stu-id="73ba8-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="73ba8-240">**Arbeitstyp:** _Entnahme_</span><span class="sxs-lookup"><span data-stu-id="73ba8-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="73ba8-241">**Standort:** _6_</span><span class="sxs-lookup"><span data-stu-id="73ba8-241">**Site:** _6_</span></span>
    - <span data-ttu-id="73ba8-242">**Lagerort:** _61_</span><span class="sxs-lookup"><span data-stu-id="73ba8-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="73ba8-243">**Richtliniencode:** _Zuteilung von Zeitfenstern_</span><span class="sxs-lookup"><span data-stu-id="73ba8-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="73ba8-244">Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="73ba8-245">Inforegister „Positionen“ konfigurieren</span><span class="sxs-lookup"><span data-stu-id="73ba8-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="73ba8-246">Klicken Sie im Inforegister **Positionen** auf **Neu**, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="73ba8-247">Legen Sie die folgenden Werte für die neue Position fest.</span><span class="sxs-lookup"><span data-stu-id="73ba8-247">On the new line, set the following values.</span></span> <span data-ttu-id="73ba8-248">Akzeptieren Sie die Standardwerte für alle anderen Felder.</span><span class="sxs-lookup"><span data-stu-id="73ba8-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="73ba8-249">**Von Menge:** _0_</span><span class="sxs-lookup"><span data-stu-id="73ba8-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="73ba8-250">**Bis Menge:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="73ba8-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="73ba8-251">Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="73ba8-252">Inforegister „Lagerplatzrichtlinienaktivitäten“ konfigurieren</span><span class="sxs-lookup"><span data-stu-id="73ba8-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="73ba8-253">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="73ba8-254">Legen Sie die folgenden Werte für die neue Position fest.</span><span class="sxs-lookup"><span data-stu-id="73ba8-254">On the new line, set the following values.</span></span> <span data-ttu-id="73ba8-255">Akzeptieren Sie die Standardwerte für alle anderen Felder.</span><span class="sxs-lookup"><span data-stu-id="73ba8-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="73ba8-256">**Name:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="73ba8-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="73ba8-257">**Strategie:** _Keine_</span><span class="sxs-lookup"><span data-stu-id="73ba8-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="73ba8-258">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="73ba8-259">Abfrage bearbeiten</span><span class="sxs-lookup"><span data-stu-id="73ba8-259">Edit the query</span></span>

1. <span data-ttu-id="73ba8-260">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="73ba8-261">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="73ba8-262">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-263">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="73ba8-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="73ba8-264">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="73ba8-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="73ba8-265">**Feld:** *Zonen-ID*</span><span class="sxs-lookup"><span data-stu-id="73ba8-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="73ba8-266">**Kriterien:** *Bulk* (Wählen Sie das doppelte Pluszeichen \[**++**\] im Feld, um die Liste zu erweitern, und wählen Sie dann *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="73ba8-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="73ba8-267">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="73ba8-268">Szenario</span><span class="sxs-lookup"><span data-stu-id="73ba8-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="73ba8-269">Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-269">Set up the scenario</span></span>

<span data-ttu-id="73ba8-270">Verwenden Sie für dieses Szenario die integrierten Beispieldaten und erstellen Sie die in diesem Abschnitt beschriebenen Datensätze.</span><span class="sxs-lookup"><span data-stu-id="73ba8-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="73ba8-271">USMF-Beispieldaten verwenden</span><span class="sxs-lookup"><span data-stu-id="73ba8-271">Use the USMF sample data</span></span>

<span data-ttu-id="73ba8-272">Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="73ba8-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="73ba8-273">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="73ba8-274">Bedarf erstellen</span><span class="sxs-lookup"><span data-stu-id="73ba8-274">Create demand</span></span>

<span data-ttu-id="73ba8-275">Befolgen Sie diese Schritte, um den Bedarf zu erstellen, auf den Sie die Zuteilung von Zeitfenstern anwenden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="73ba8-276">Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="73ba8-277">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="73ba8-278">Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** _US-007_ aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="73ba8-279">Im Feld **Lagerort** wählen Sie _61_ aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="73ba8-280">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-280">Select **OK**.</span></span>
1. <span data-ttu-id="73ba8-281">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="73ba8-281">The new sales order is opened.</span></span> <span data-ttu-id="73ba8-282">Er enthält eine leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="73ba8-283">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-284">**Artikel:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="73ba8-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="73ba8-285">**Menge** _20_</span><span class="sxs-lookup"><span data-stu-id="73ba8-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="73ba8-286">Wählen Sie **Position hinzufügen** aus, um eine neue Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="73ba8-287">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="73ba8-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="73ba8-288">**Menge** _8_</span><span class="sxs-lookup"><span data-stu-id="73ba8-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="73ba8-289">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-289">Select **Save**.</span></span>
1. <span data-ttu-id="73ba8-290">Wählen Sie **Neu** aus, um einen zweiten Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="73ba8-291">Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** _US-008_ aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="73ba8-292">Im Feld **Lagerort** wählen Sie _61_ aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="73ba8-293">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="73ba8-293">The new sales order is opened.</span></span> <span data-ttu-id="73ba8-294">Er enthält eine leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="73ba8-295">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="73ba8-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="73ba8-296">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="73ba8-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="73ba8-297">**Menge** _1_</span><span class="sxs-lookup"><span data-stu-id="73ba8-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="73ba8-298">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="73ba8-299">Typisches Szenario für Zuteilung von Zeitfenstern durchgehen</span><span class="sxs-lookup"><span data-stu-id="73ba8-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="73ba8-300">Nachdem alle erforderlichen Elemente vorhanden sind, wie im vorherigen Abschnitt beschrieben, können Sie die Funktion ausprobieren, indem Sie jede Übung in diesem Abschnitt durcharbeiten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="73ba8-301">Bedarf generieren</span><span class="sxs-lookup"><span data-stu-id="73ba8-301">Generate demand</span></span>

1. <span data-ttu-id="73ba8-302">Navigieren Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Vorlagen für Zuteilung von Zeitfenstern**, und wählen Sie die Vorlage für die Zuteilung von Zeitfenstern aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="73ba8-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="73ba8-303">Wählen Sie im Aktivitätsbereich **Bedarf generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="73ba8-304">Dieser Befehl wertet den gesamten Bedarf aus, der sich im System befindet und mit der Vorlagenabfrage für die Zuteilung von Zeitfenstern übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="73ba8-305">Der Gesamtbedarf aller Bestellungen wird dann in einer Position pro Menge/Maßeinheit zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="73ba8-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="73ba8-306">Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="73ba8-307">Bedarf an der Zuteilung von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="73ba8-307">Slotting demand</span></span>

<span data-ttu-id="73ba8-308">Die *Zuteilung von Zeitfenstern für den Bedarf* zeigt die Ergebnisse der Bedarfsgenerierung basierend auf dem Setup der Vorlage für die Zuteilung von Zeitfenstern.</span><span class="sxs-lookup"><span data-stu-id="73ba8-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="73ba8-309">Wählen Sie im Aktivitätsbereich **Zuteilung von Zeitfenstern für den Bedarf** aus, um die Ergebnisse aus dem Befehl **Bedarf generieren** zu sehen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="73ba8-310">Die Positionen in der Zuteilung von Zeitfenstern für den Bedarf können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="73ba8-311">Sie können eine Position löschen, eine neue Position hinzufügen oder die Positionsdetails bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="73ba8-312">Sie können den Bedarf manuell bearbeiten oder mithilfe der Datenverwaltung von einem externen System importieren.</span><span class="sxs-lookup"><span data-stu-id="73ba8-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="73ba8-313">Was auch immer in der Zuteilung von Zeitfenstern für den Bedarf enthalten ist, wird im nächsten Schritt verwendet, unabhängig davon, woher es stammt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="73ba8-314">Bedarf ermitteln</span><span class="sxs-lookup"><span data-stu-id="73ba8-314">Locate demand</span></span>

<span data-ttu-id="73ba8-315">Nachdem der Bedarf generiert wurde, müssen Sie den Befehl **Bedarf ermitteln** verwenden, um den *Plan für die Zuteilung von Zeitfenstern* zu generieren.</span><span class="sxs-lookup"><span data-stu-id="73ba8-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="73ba8-316">Wählen Sie im Aktivitätsbereich **Bedarf ermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="73ba8-317">Der Vorgang für die Zuteilung von Zeitfenstern läuft.</span><span class="sxs-lookup"><span data-stu-id="73ba8-317">The slotting process runs.</span></span> <span data-ttu-id="73ba8-318">Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="73ba8-319">Plan für die Zuteilung von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="73ba8-319">Slotting plan</span></span>

<span data-ttu-id="73ba8-320">Der Plan für die Zuteilung von Zeitfenstern zeigt den Lagerplatz, dem jeder Artikel/jede Menge zugewiesen wurde, ob ein Überlauf verwendet wurde, ob Pausenarbeiten erstellt wurden und welche Vorlagenposition verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="73ba8-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="73ba8-321">**Jeder Bedarf, für den keine Zuteilung von Zeitfenstern möglich ist, wird rot hervorgehoben.**</span><span class="sxs-lookup"><span data-stu-id="73ba8-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="73ba8-322">Wählen Sie im Aktivitätsbereich **Plan für die Zuteilung von Zeitfenstern** aus, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="73ba8-323">Wiederbeschaffung erstellen</span><span class="sxs-lookup"><span data-stu-id="73ba8-323">Create replenishment</span></span>

<span data-ttu-id="73ba8-324">Nachdem der Plan für die Zuteilung von Zeitfenstern erstellt wurde, müssen Sie *Wiederbeschaffungsarbeiten* basierend auf dem Plan erstellen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="73ba8-325">Wählen Sie im Aktivitätsbereich **Wiederbeschaffung ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="73ba8-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="73ba8-326">Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73ba8-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="73ba8-327">Diese Nachricht gibt die Anzahl der Header an, die für die Arbeits-Build-ID erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="73ba8-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="73ba8-328">Zu verwendende Lagerplatzrichtlinien werden anhand des Richtliniencodes identifiziert, der in jeder Vorlagenposition angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="73ba8-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="73ba8-329">Tipps</span><span class="sxs-lookup"><span data-stu-id="73ba8-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="73ba8-330">Automatische Zuteilung von Zeitfenstern einrichten</span><span class="sxs-lookup"><span data-stu-id="73ba8-330">Set up automatic slotting</span></span>

<span data-ttu-id="73ba8-331">Nachdem alle erforderlichen Elemente vorhanden sind, können Sie die Zuteilung von Zeitfenstern so einrichten, dass sie automatisch ausgeführt wird, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="73ba8-332">Wechseln Sie zu **Lagerortverwaltung \> Wiederbeschaffung \> Zuteilung von Zeitfenstern ausführen**.</span><span class="sxs-lookup"><span data-stu-id="73ba8-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="73ba8-333">Geben Sie die auszuführenden Schritte für die Zuteilung von Zeitfenstern an.</span><span class="sxs-lookup"><span data-stu-id="73ba8-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="73ba8-334">Wählen Sie einen oder mehrere der folgenden Schritte für die Zuteilung von Zeitfenstern aus:</span><span class="sxs-lookup"><span data-stu-id="73ba8-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="73ba8-335">Bedarf generieren</span><span class="sxs-lookup"><span data-stu-id="73ba8-335">Generate demand</span></span>
    - <span data-ttu-id="73ba8-336">Bedarf ermitteln</span><span class="sxs-lookup"><span data-stu-id="73ba8-336">Locate demand</span></span>
    - <span data-ttu-id="73ba8-337">Wiederbeschaffungsarbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="73ba8-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="73ba8-338">Die Schritte für die Zuteilung von Zeitfenstern sind progressiv.</span><span class="sxs-lookup"><span data-stu-id="73ba8-338">The slotting steps are progressive.</span></span> <span data-ttu-id="73ba8-339">Wenn Sie *Bedarf ermitteln* auswählen möchten, müssen Sie zuerst *Bedarf generieren* auswählen.</span><span class="sxs-lookup"><span data-stu-id="73ba8-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="73ba8-340">Geben Sie die zu verwendende Vorlage für die Zuteilung von Zeitfenstern an.</span><span class="sxs-lookup"><span data-stu-id="73ba8-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="73ba8-341">Stellen Sie die Serie so ein, dass sie automatisch ausgeführt wird, wenn Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="73ba8-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="73ba8-342">Richten Sie für die Übungen im Szenario **nicht** die automatische Zuteilung von Zeitfenstern ein.</span><span class="sxs-lookup"><span data-stu-id="73ba8-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
