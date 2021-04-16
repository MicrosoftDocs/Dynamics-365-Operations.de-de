---
title: Wiederbeschaffung über Lagerplatzkapazität
description: Dieses Thema enthält Informationen zur Funktion „Wiederbeschaffung über Lagerplatzkapazität“. Mit dieser Funktion können alle für den Tag erforderlichen Wiederbeschaffungsarbeiten erstellt und die Verfügbarkeit dieser Wiederbeschaffungsarbeiten verwaltet werden, um sicherzustellen, dass am Kommissionierort weder der Lagerbestand ausgeht noch die Kapazität überschritten wird.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823238"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="bf375-104">Wiederbeschaffung über Lagerplatzkapazität</span><span class="sxs-lookup"><span data-stu-id="bf375-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf375-105">Einige Lagerorte mit hohem Volumen oder Platzmangel müssen an einem Tag mehr Mengen eines Artikels versenden, als in den Kommissionierort passen.</span><span class="sxs-lookup"><span data-stu-id="bf375-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="bf375-106">Mit der Funktion *Wiederbeschaffung über Lagerplatzkapazität* können alle für den Tag erforderlichen Wiederbeschaffungsarbeiten erstellt und die Verfügbarkeit dieser Wiederbeschaffungsarbeiten verwaltet werden, um sicherzustellen, dass am Kommissionierort weder der Lagerbestand ausgeht noch die Kapazität überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="bf375-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="bf375-107">Mit dieser Funktion können mehr Wiederbeschaffungsarbeiten erstellt werden, als in einen Lagerplatz passen, und es wird verhindert, dass Wiederbeschaffungsarbeiten abgeschlossen werden, wenn der Standort voll ist.</span><span class="sxs-lookup"><span data-stu-id="bf375-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="bf375-108">Wenn der Lagerbestand am Kommissionierort unter einen konfigurierbaren Schwellenwert fällt, werden mehr Wiederbeschaffungsarbeiten zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="bf375-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="bf375-109">Aktivieren der Funktion „Wiederbeschaffung über Lagerplatzkapazität“</span><span class="sxs-lookup"><span data-stu-id="bf375-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="bf375-110">Um diese Funktion verfügbar zu machen, aktivieren Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in dieser Reihenfolge):</span><span class="sxs-lookup"><span data-stu-id="bf375-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="bf375-111">Organisationsweite Arbeitssperrung</span><span class="sxs-lookup"><span data-stu-id="bf375-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="bf375-112">Wiederbeschaffung über Lagerplatzkapazität</span><span class="sxs-lookup"><span data-stu-id="bf375-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="bf375-113">Funktion für das Beispielszenario einrichten</span><span class="sxs-lookup"><span data-stu-id="bf375-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="bf375-114">Dieser Abschnitt enthält Richtlinien und ein Beispiel, das zeigt, wie Sie diese Funktion einrichten und Beispieldaten für das Beispielszenario vorbereiten, das später in diesem Thema bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf375-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="bf375-115">Beispieldaten aktivieren</span><span class="sxs-lookup"><span data-stu-id="bf375-115">Enable sample data</span></span>

<span data-ttu-id="bf375-116">Um das [Beispielszenario](#example-scenario) mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf375-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bf375-117">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="bf375-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="bf375-118">Lagerortprofil</span><span class="sxs-lookup"><span data-stu-id="bf375-118">Location profile</span></span>

<span data-ttu-id="bf375-119">Aktivieren Sie die Funktion „Wiederbeschaffung über Lagerplatzkapazität“ im Lagerplatzprofil.</span><span class="sxs-lookup"><span data-stu-id="bf375-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="bf375-120">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="bf375-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="bf375-121">Wählen Sie im linken Bereich **PICK-06** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="bf375-122">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bf375-123">Legen Sie im Inforegister **Wiederbeschaffung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="bf375-124">**Lagerplatzkapazität überschreiten:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="bf375-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="bf375-125">Bei Aktivierung wird zugelassen, dass die Maximalkapazität des Lagerplatzes durch Wiederbeschaffungsarbeit überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="bf375-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="bf375-126">Dies aktiviert auch andere Felder im Inforegister **Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="bf375-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="bf375-127">**Schwellenwerttyp für Arbeitsverfügbarkeit:** *Menge*</span><span class="sxs-lookup"><span data-stu-id="bf375-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="bf375-128">Dieses Feld definiert die Methode, mit der festgelegt wird, wann mehr Arbeit freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf375-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="bf375-129">Sie können die Freigabe entweder nach Menge oder nach Prozentsatz festlegen:</span><span class="sxs-lookup"><span data-stu-id="bf375-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="bf375-130">*Prozent* – Wählen Sie diese Option aus, um die Kapazität in Prozent zu verwenden, die auf Bestandsgrenzen oder Volumenmaßen basiert.</span><span class="sxs-lookup"><span data-stu-id="bf375-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="bf375-131">Durch Auswahl dieser Option wird das Feld **Überlaufprozentsatz** aktiviert und die beiden mengenbezogenen Felder **Überlaufmenge** und **Überlaufeinheit** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf375-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="bf375-132">Sie können diese Option verwenden, wenn die Kommissionierorte Volumenmaße verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf375-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="bf375-133">Wenn diese Option ausgewählt ist, legen Sie das Feld **Überlaufprozentsatz** auf den Prozentsatz fest, zu dem mehr Wiederbeschaffungsarbeiten zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="bf375-134">*Menge* – Wählen Sie diese Option aus, um einen bestimmten Mengenwert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf375-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="bf375-135">Durch Auswahl dieser Option wird das Feld **Überlaufprozentsatz** deaktiviert und die Felder **Überlaufmenge** und **Überlaufeinheit** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf375-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="bf375-136">Verwenden Sie diese Option, wenn Sie für die Lagerplätze, die aufgefüllt werden, keine Volumenmaße verwenden oder wenn Sie über konsistente Mengen verfügen, bei denen mehr Bestand an den Lagerplatz gebracht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf375-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="bf375-137">Wenn diese Option ausgewählt ist, legen Sie die Felder **Überlaufmenge** und **Überlaufeinheit** auf die Menge und Einheit fest, ab der weitere Wiederbeschaffungsarbeiten zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="bf375-138">**Überlaufmenge:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="bf375-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="bf375-139">Dieses Feld definiert die Menge, bei der der Lagerplatz überquillt.</span><span class="sxs-lookup"><span data-stu-id="bf375-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="bf375-140">Arbeit ist immer dann verfügbar, wenn die Summe der Bestandsmenge am Lagerplatz und der Arbeitsmenge unterhalb dieses Werts liegt.</span><span class="sxs-lookup"><span data-stu-id="bf375-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="bf375-141">Jede Wiederbeschaffungsarbeit über diesem Wert wird gesperrt und muss manuell entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="bf375-142">Lagerplatzbestandsgrenzen werden bei der Berechnung der Arbeitsmenge berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="bf375-143">**Überlaufeinheit:** *PL*</span><span class="sxs-lookup"><span data-stu-id="bf375-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="bf375-144">Dieses Feld definiert die Einheit, die der Überlaufmenge zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bf375-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="bf375-145">In diesem Fall werden mehr Wiederbeschaffungsarbeiten zur Verfügung gestellt, wenn der Lagerplatz auf 0,65 Paletten (PL) gesunken ist.</span><span class="sxs-lookup"><span data-stu-id="bf375-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="bf375-146">**Überlaufprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="bf375-146">**Overflow percentage**</span></span>

        <span data-ttu-id="bf375-147">Dieses Feld definiert den Prozentsatz, bei dem der Lagerplatz überquillt.</span><span class="sxs-lookup"><span data-stu-id="bf375-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="bf375-148">Arbeit ist immer dann verfügbar, wenn die Summe der Bestandsmenge am Lagerplatz und der Arbeitsmenge unterhalb dieses Prozentsatzes liegt.</span><span class="sxs-lookup"><span data-stu-id="bf375-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="bf375-149">Jeder Prozentsatz der Wiederbeschaffungsarbeitsmenge über diesem Wert wird gesperrt und muss manuell entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="bf375-150">Lagerplatzbestandsgrenzen werden bei der Berechnung des Prozentsatzes der Arbeitsmenge berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="bf375-151">Wenn keine Lagerplatzbestandsgrenzen definiert wurden, wird der Prozentsatz der Arbeitsmenge nach Volumen berechnet, wenn für das Lagerplatzprofil Volumenbeschränkungen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf375-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf375-152">Wenn Sie die Demodaten für die juristische Person **USMF** verwenden und zuvor die Funktion *Lagerplatzkennzeichenpositionierung* aktiviert haben, müssen Sie die Einstellung **Kennzeichenpositionierung aktivieren** für das Lagerplatzprofil **BULK-06** deaktivieren, um die mobilen Schritte im Beispielszenario abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="bf375-153">Wellenschrittcode</span><span class="sxs-lookup"><span data-stu-id="bf375-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="bf375-154">Um einen Wellenschrittcode wie hier beschrieben einzurichten, müssen Sie möglicherweise zuerst die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die Funktion namens *Organisationsweiter Wellenschrittcode* zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf375-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="bf375-155">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Wellen \> Wellenschrittcodes**.</span><span class="sxs-lookup"><span data-stu-id="bf375-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="bf375-156">Wählen Sie **Neu** aus, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="bf375-157">**Wellenschrittcode:** *Auffüllen*</span><span class="sxs-lookup"><span data-stu-id="bf375-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="bf375-158">**Wellenschrittbeschreibung:** *Wiederbeschaffung*</span><span class="sxs-lookup"><span data-stu-id="bf375-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="bf375-159">**Wellenschritttyp:** *Wiederbeschaffung*</span><span class="sxs-lookup"><span data-stu-id="bf375-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="bf375-160">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="bf375-161">Wiederbeschaffungsvorlage</span><span class="sxs-lookup"><span data-stu-id="bf375-161">Replenishment template</span></span>

<span data-ttu-id="bf375-162">Wiederbeschaffungsvorlagen sind eine Reihe von Regeln, die steuern, wann und wie ein Lagerplatz aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="bf375-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="bf375-163">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="bf375-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="bf375-164">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bf375-165">Wählen Sie im Abschnitt **Übersicht** die Position aus, in der das Feld **Wiederbeschaffungsvorlage** auf *Bedarfswiederbeschaffung* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bf375-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="bf375-166">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-166">Set the following values:</span></span>

    - <span data-ttu-id="bf375-167">**Wellenschrittcode:** *Auffüllen*</span><span class="sxs-lookup"><span data-stu-id="bf375-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="bf375-168">**Wellenbedarf die Nutzung nicht reservierter Mengen gestatten:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="bf375-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="bf375-169">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="bf375-170">Wellenvorlage</span><span class="sxs-lookup"><span data-stu-id="bf375-170">Wave template</span></span>

1. <span data-ttu-id="bf375-171">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="bf375-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="bf375-172">Legen Sie im linken Bereich im Feld **Wellenvorlagentyp** *Versand* fest.</span><span class="sxs-lookup"><span data-stu-id="bf375-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="bf375-173">Wählen Sie die Vorlage **61 Shipping** in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="bf375-174">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bf375-175">Legen Sie im Inforegister **Allgemein** die Option **Freigabe der Wiederbeschaffungsarbeit automatisieren** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="bf375-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="bf375-176">Legen Sie diese Option auf *Ja* fest, um bedarfsbasierte Wiederbeschaffungsarbeit zu erstellen und diese automatisch freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bf375-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="bf375-177">Sie müssen die Wiederbeschaffungswellenmethode der Wellenvorlage hinzufügen und eine Wiederbeschaffungsvorlage vom Typ **Wellenbedarf** erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf375-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="bf375-178">Richten Sie eine Wiederbeschaffungsvorlage auf der Seite **Wiederbeschaffungsvorlagen** ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="bf375-179">Um eine Wiederbeschaffungsvorlage einzurichten, müssen Sie der Wellenvorlage die Wiederbeschaffungsmethode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf375-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="bf375-180">Suchen Sie im Inforegister **Methoden** in der Spalte **Ausgewählte Methoden** die folgende Position:</span><span class="sxs-lookup"><span data-stu-id="bf375-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="bf375-181">**Methodenname:** *Auffüllen*</span><span class="sxs-lookup"><span data-stu-id="bf375-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="bf375-182">**Name:** *Wiederbeschaffung*</span><span class="sxs-lookup"><span data-stu-id="bf375-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="bf375-183">Legen Sie das Feld **Wellenschrittcode** für diese Position auf *Auffüllen* fest.</span><span class="sxs-lookup"><span data-stu-id="bf375-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="bf375-184">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="bf375-185">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="bf375-185">Example scenario</span></span>

<span data-ttu-id="bf375-186">Nachdem Sie alle zuvor beschriebenen Beispieldaten verfügbar gemacht und eingerichtet haben, können Sie dieses Szenario durcharbeiten, um die Funktion *Wiederbeschaffung über Lagerplatzkapazität* zu testen.</span><span class="sxs-lookup"><span data-stu-id="bf375-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="bf375-187">Bei den in diesem Szenario angezeigten Werten wird davon ausgegangen, dass Sie mit den Standarddemodaten arbeiten, die juristische Person **USMF** ausgewählt und die Beispieldatensätze vorbereitet haben, die weiter oben in diesem Thema beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="bf375-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="bf375-188">Dieses Szenario dient auch als Beispiel, das zeigt, wie die Funktion in einer Produktionseinstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf375-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="bf375-189">Wiederbeschaffungsarbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="bf375-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="bf375-190">Auftrag 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="bf375-190">Create sales order 1</span></span>

1. <span data-ttu-id="bf375-191">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="bf375-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="bf375-192">Wählen Sie im Aktivitätsbereich **Neu** aus, um ein Dialogfeld zum Erstellen eines neuen Auftrags zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf375-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="bf375-193">Legen Sie im Dialogfeld die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="bf375-194">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="bf375-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="bf375-195">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="bf375-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bf375-196">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bf375-197">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bf375-197">The new sales order is opened.</span></span> <span data-ttu-id="bf375-198">Er enthält eine neue leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="bf375-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bf375-199">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="bf375-200">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="bf375-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bf375-201">**Menge** *40*</span><span class="sxs-lookup"><span data-stu-id="bf375-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="bf375-202">Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="bf375-203">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="bf375-204">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bf375-204">Close the page.</span></span>
1. <span data-ttu-id="bf375-205">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="bf375-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bf375-206">Sie erhalten Informationsnachrichten mit den Wellen- und Lieferungs-IDs, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf375-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="bf375-207">Eine Wiederbeschaffungswelle wird ebenfalls erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf375-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="bf375-208">Sie erhalten außerdem eine Warnmeldung mit dem Titel „Die Arbeits-ID XXXX kann nicht entsperrt werden, da Wiederbeschaffungsarbeiten noch nicht abgeschlossen wurden.“.</span><span class="sxs-lookup"><span data-stu-id="bf375-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="bf375-209">Auftrag 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="bf375-209">Create sales order 2</span></span>

1. <span data-ttu-id="bf375-210">Wählen Sie auf der Seite **Alle Aufträge** im Aktivitätsbereich **Neu** aus, um ein Dialogfeld zum Erstellen eines neuen Auftrags zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf375-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="bf375-211">Legen Sie im Dialogfeld den folgenden Wert fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="bf375-212">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="bf375-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="bf375-213">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="bf375-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bf375-214">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bf375-215">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bf375-215">The new sales order is opened.</span></span> <span data-ttu-id="bf375-216">Er enthält eine neue leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="bf375-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bf375-217">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="bf375-218">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="bf375-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bf375-219">**Menge** *60*</span><span class="sxs-lookup"><span data-stu-id="bf375-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="bf375-220">Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="bf375-221">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="bf375-222">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bf375-222">Close the page.</span></span>
1. <span data-ttu-id="bf375-223">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="bf375-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bf375-224">Sie erhalten Informationsnachrichten mit den Wellen- und Lieferungs-IDs, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf375-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="bf375-225">Eine Wiederbeschaffungswelle wird ebenfalls erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf375-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="bf375-226">Sie erhalten außerdem eine Warnmeldung mit dem Titel „Die Arbeits-ID XXXX kann nicht entsperrt werden, da Wiederbeschaffungsarbeiten noch nicht abgeschlossen wurden.“.</span><span class="sxs-lookup"><span data-stu-id="bf375-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="bf375-227">Auftrag 3 erstellen</span><span class="sxs-lookup"><span data-stu-id="bf375-227">Create sales order 3</span></span>

1. <span data-ttu-id="bf375-228">Wählen Sie auf der Seite **Alle Aufträge** im Aktivitätsbereich **Neu** aus, um ein Dialogfeld zum Erstellen eines neuen Auftrags zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf375-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="bf375-229">Legen Sie im Dialogfeld die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="bf375-230">**Debitorenkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="bf375-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="bf375-231">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="bf375-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bf375-232">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bf375-233">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bf375-233">The new sales order is opened.</span></span> <span data-ttu-id="bf375-234">Er enthält eine neue leere Position im Inforegister **Auftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="bf375-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bf375-235">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="bf375-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="bf375-236">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="bf375-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bf375-237">**Menge** *30*</span><span class="sxs-lookup"><span data-stu-id="bf375-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="bf375-238">Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="bf375-239">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="bf375-240">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bf375-240">Close the page.</span></span>
1. <span data-ttu-id="bf375-241">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="bf375-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bf375-242">Sie erhalten Informationsnachrichten mit den Wellen- und Lieferungs-IDs, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf375-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="bf375-243">Eine Wiederbeschaffungswelle wird ebenfalls erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf375-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="bf375-244">Sie erhalten außerdem eine Warnmeldung mit dem Titel „Die Arbeits-ID XXXX kann nicht entsperrt werden, da Wiederbeschaffungsarbeiten noch nicht abgeschlossen wurden.“.</span><span class="sxs-lookup"><span data-stu-id="bf375-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="bf375-245">Arbeitsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="bf375-245">View work details</span></span>

1. <span data-ttu-id="bf375-246">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="bf375-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="bf375-247">Filtern Sie im Abschnitt **Übersicht** die Spalte **Lagerort** nach dem Lagerort *61*.</span><span class="sxs-lookup"><span data-stu-id="bf375-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="bf375-248">Es sollten sieben Arbeits-IDs für die drei Bedarfsaufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="bf375-249">Drei der sieben Arbeits-IDs haben einen **Arbeitsauftragstyp**-Wert von *Wiederbeschaffung* und vier haben einen **Arbeitsauftragstyp**-Wert von *Aufträge*.</span><span class="sxs-lookup"><span data-stu-id="bf375-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="bf375-250">Alle drei Arbeits-IDs mit einem **Arbeitsauftragstyp**-Wert von *Wiederbeschaffung* weisen dieselben *Entnehmen*- und *Einlagern*-Lagerplätze im Abschnitt **Positionen** auf:</span><span class="sxs-lookup"><span data-stu-id="bf375-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="bf375-251">**Entnehmen:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="bf375-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="bf375-252">**Einlagern:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="bf375-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="bf375-253">Für Auftrag 1 wurden zwei Arbeits-IDs erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf375-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="bf375-254">Notieren Sie sich die Arbeits-IDs für die Aufträge.</span><span class="sxs-lookup"><span data-stu-id="bf375-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="bf375-255">Abhängig von Ihren Bestandsmengen können die erstellten Arbeitsmengen geringfügig variieren.</span><span class="sxs-lookup"><span data-stu-id="bf375-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="bf375-256">Insgesamt sollten die erstellten Arbeitskopfzeilen jedoch mit diesem Szenariobeispiel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bf375-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="bf375-257">Bestandskennzeichen-ID</span><span class="sxs-lookup"><span data-stu-id="bf375-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="bf375-258">Später in diesem Szenario verwenden Sie die Warehouse Management Mobile App (oder einen Emulator), in der Sie das Kennzeichen identifizieren müssen, um die Kommissionier- und Wiederbeschaffungsszenarien abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-258">Later in this scenario, you will use the Warehouse Management mobile app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="bf375-259">Führen Sie die folgenden Schritte aus, um die Kennzeichen-IDs zu finden, die Sie später benötigen.</span><span class="sxs-lookup"><span data-stu-id="bf375-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="bf375-260">Wechseln Sie zu **Bestandsverwaltung \> Anfragen und Berichte \> Bestandsliste**.</span><span class="sxs-lookup"><span data-stu-id="bf375-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="bf375-261">Wählen Sie die Schaltfläche **Filter anzeigen** aus, um den Filterbereich zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf375-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="bf375-262">Geben Sie die folgenden Filterkriterien ein, um die Kennzeichen für das Szenario zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf375-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="bf375-263">Verwenden Sie den Filter *beginnt mit*.</span><span class="sxs-lookup"><span data-stu-id="bf375-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="bf375-264">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="bf375-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bf375-265">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="bf375-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bf375-266">Wählen Sie **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-266">Select **Apply**.</span></span>
1. <span data-ttu-id="bf375-267">Wählen Sie im Aktionsbereich **Dimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="bf375-268">Wählen Sie im Dialogfeld **Dimensionsanzeige** im Abschnitt **Lagerdimensionen** alle Werte aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="bf375-269">Wählen Sie im Abschnitt **Buchungen** **Artikelnummer** und **Menge \<\> 0** aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="bf375-270">Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="bf375-271">Das Raster **Bestand** zeigt die Kennzeichennummern für den Artikel *T0100* an jedem Lagerplatz an.</span><span class="sxs-lookup"><span data-stu-id="bf375-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="bf375-272">Notieren Sie sich das Kennzeichen eines jeden Lagerplatzes, da Sie diese Informationen später benötigen.</span><span class="sxs-lookup"><span data-stu-id="bf375-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="bf375-273">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bf375-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="bf375-274">Prozessschritte</span><span class="sxs-lookup"><span data-stu-id="bf375-274">Process steps</span></span>

<span data-ttu-id="bf375-275">Sie führen die Lagerplatzwiederbeschaffung für die ersten beiden Arbeits-IDs durch.</span><span class="sxs-lookup"><span data-stu-id="bf375-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="bf375-276">Die Arbeiten an der dritten Wiederbeschaffungsarbeit werden blockiert, bis der Lagerbestand am Kommissionierort den Schwellenwert unterschreitet.</span><span class="sxs-lookup"><span data-stu-id="bf375-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="bf375-277">Wiederbeschaffung</span><span class="sxs-lookup"><span data-stu-id="bf375-277">Replenishment</span></span>

1. <span data-ttu-id="bf375-278">Melden Sie sich bei der Warehouse Management Mobile App als ein Benutzer im Lagerort *61* an.</span><span class="sxs-lookup"><span data-stu-id="bf375-278">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="bf375-279">(Geben Sie *61* als Benutzer-ID und *1* als Passwort ein.)</span><span class="sxs-lookup"><span data-stu-id="bf375-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bf375-280">Gehen Sie zu **Lager \> Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="bf375-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="bf375-281">Sie werden aufgefordert, die erste Wiederbeschaffungsarbeit abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="bf375-282">Artikelnummer, -menge und -lagerplatz zur Entnahme werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="bf375-283">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bf375-284">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bf375-285">Das System generiert eine Zielkennzeichennummer für das neue Kennzeichen des entnommenen Artikels.</span><span class="sxs-lookup"><span data-stu-id="bf375-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="bf375-286">Wählen Sie **OK**, um den Wert zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="bf375-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="bf375-287">Es wird eine Einlagerungsarbeit angezeigt, die den Benutzer anweist, das Zielkennzeichen in den Wiederbeschaffungslagerplatz einzulagern.</span><span class="sxs-lookup"><span data-stu-id="bf375-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="bf375-288">Der *Einlagern*-Lagerplatz sollte **06A01R2S1B** lauten.</span><span class="sxs-lookup"><span data-stu-id="bf375-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="bf375-289">Bestätigen Sie die Einlagerungsdetails, und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="bf375-290">Sie erhalten die Meldung „Arbeit erledigt“ und die Details der nächsten Wiederbeschaffungsentnahmeaufgabe werden angezeigt: Artikelnummer, -menge und -lagerplatz zur Entnahme.</span><span class="sxs-lookup"><span data-stu-id="bf375-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="bf375-291">Der Kommissionierort ist derselbe wie der erste Wiederbeschaffungslagerplatz.</span><span class="sxs-lookup"><span data-stu-id="bf375-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="bf375-292">Daher hat das Kennzeichen dieselbe Kennzeichen-ID, die für die erste Wiederbeschaffungsarbeitsaufgabe verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf375-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="bf375-293">Wiederholen Sie die vorhergehenden Schritte, um die Wiederbeschaffungsarbeit für die zweite Arbeitsaufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="bf375-294">Die Menge und das Zielkennzeichen unterscheiden sich von der Menge und dem Zielkennzeichen für die erste Arbeitsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="bf375-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="bf375-295">Nach Abschluss der zweiten Wiederbeschaffungsarbeit erhalten Sie die Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf375-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bf375-296">Das mobile Gerät informiert Sie auch darüber, dass keine Arbeit verfügbar ist, obwohl noch einige Wiederbeschaffungsarbeiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bf375-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="bf375-297">Dieses Verhalten tritt auf, weil die Wiederbeschaffungsarbeit den Verfügbarkeitsstatus *Gehalten* aufweist und daher als **Gesperrt** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="bf375-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="bf375-298">Der Status *Gehalten* wurde ausgelöst, weil das Lagerplatzprofil für den Kommissionierstandort, dem die Arbeit zugewiesen ist, einen **Überlaufmenge**-Wert von *0,65 PL* aufweist.</span><span class="sxs-lookup"><span data-stu-id="bf375-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="bf375-299">Die beiden vorherigen Wiederbeschaffungsarbeitsaufgaben füllten den Lagerplatz fast bis zu seiner Überlaufgrenze für Artikel *T0100*.</span><span class="sxs-lookup"><span data-stu-id="bf375-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="bf375-300">(Die Einheitenumrechnung für den Artikel ist *1 PL = 100 EA*.) Daher würde die verbleibende Wiederbeschaffungsarbeit dazu führen, dass der Lagerplatz seine Überlaufgrenze überschreitet.</span><span class="sxs-lookup"><span data-stu-id="bf375-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="bf375-301">Solange nicht genügend Bestand vom Lagerplatz entnommen wurde, um es unter den Schwellenwert für die Arbeitsfreigabe im Menüelement für mobile Geräte zu bringen, bleibt diese Wiederbeschaffungsarbeit gesperrt.</span><span class="sxs-lookup"><span data-stu-id="bf375-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="bf375-302">Auftragsentnahme</span><span class="sxs-lookup"><span data-stu-id="bf375-302">Sales order pick</span></span>

<span data-ttu-id="bf375-303">Bevor die verbleibende Wiederbeschaffungsarbeitsaufgabe abgeschlossen werden kann, muss der Kommissionierort so weit vom Bestand geleert sein, dass die verbleibende Wiederbeschaffungsarbeit entsperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf375-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="bf375-304">Mit anderen Worten, die Summe aus der Menge des Lagerbestands am Lagerplatz und der Wiederbeschaffungsmenge darf den **Überlaufmenge**-Wert nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="bf375-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="bf375-305">Wenn diese Summe geringer ist als die Überlaufmenge, wird die verbleibende Wiederbeschaffungsarbeit entsperrt.</span><span class="sxs-lookup"><span data-stu-id="bf375-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="bf375-306">Melden Sie sich bei der Warehouse Management Mobile App als ein Benutzer im Lagerort *61* an.</span><span class="sxs-lookup"><span data-stu-id="bf375-306">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="bf375-307">(Geben Sie *61* als Benutzer-ID und *1* als Passwort ein.)</span><span class="sxs-lookup"><span data-stu-id="bf375-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bf375-308">Gehen Sie zu **Ausgehend \> Verkaufskommissionierung**.</span><span class="sxs-lookup"><span data-stu-id="bf375-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="bf375-309">Geben Sie die erste Arbeits-ID für Auftrag 1 ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="bf375-310">Auf der Seite **Arbeitsdetails** finden Sie in den Arbeits-IDs, die Sie zuvor notiert haben, Informationen zu Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="bf375-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="bf375-311">Die hier eingegebene Arbeits-ID generiert eine Kommissionierarbeit für eine Menge von 10 EA an zwei verschiedenen Lagerplätzen.</span><span class="sxs-lookup"><span data-stu-id="bf375-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="bf375-312">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-312">Select **OK**.</span></span>

    <span data-ttu-id="bf375-313">Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme für den ersten Lagerplatz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="bf375-314">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bf375-315">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bf375-316">Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme für den nächsten Lagerplatz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="bf375-317">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bf375-318">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bf375-319">Die Seite **Aufträge: Einlagern** weist Sie an, beide abgeschlossenen Kommissionierarbeiten an den ausgehenden Bereitstellungslagerplatz zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="bf375-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="bf375-320">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-320">Select **OK**.</span></span>

    <span data-ttu-id="bf375-321">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf375-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="bf375-322">Geben Sie die zweite Arbeits-ID für Auftrag 1 ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="bf375-323">Für diese Arbeits-ID gibt es nur eine Entnahmeaufgabe.</span><span class="sxs-lookup"><span data-stu-id="bf375-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="bf375-324">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-324">Select **OK**.</span></span>

    <span data-ttu-id="bf375-325">Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="bf375-326">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="bf375-327">Das von Ihnen angegebene Kennzeichen ist eines der vom System generierten Kennzeichen aus den Wiederbeschaffungsarbeitsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="bf375-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="bf375-328">Um sicherzustellen, dass Sie die richtige Kennzeichen-ID erfassen, überprüfen Sie auf der Seite **Bestandsliste** den Bestand für Artikel, Lagerplatz und Menge.</span><span class="sxs-lookup"><span data-stu-id="bf375-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="bf375-329">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="bf375-330">Bestätigen Sie die Anweisungen für die Einlagerungsaufgabe am ausgehenden Bereitstellungslagerplatz.</span><span class="sxs-lookup"><span data-stu-id="bf375-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="bf375-331">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-331">Select **OK**.</span></span>

    <span data-ttu-id="bf375-332">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf375-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="bf375-333">Auftrag 2 kann nicht kommissioniert werden, da die Wiederbeschaffungsaufgabe, mit der er verknüpft ist, nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bf375-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="bf375-334">Derzeit befindet sich am Kommissionierort noch eine Menge von 30 EA, und die Wiederbeschaffungsmenge für Auftrag 2 beträgt 60 EA.</span><span class="sxs-lookup"><span data-stu-id="bf375-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="bf375-335">Die Summe aus Lagerbestand und Wiederbeschaffungsbestand (90 EA) überschreitet die Überlaufmenge von 0,65 PL (oder 65 EA).</span><span class="sxs-lookup"><span data-stu-id="bf375-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="bf375-336">Bevor die Wiederbeschaffungsarbeit abgeschlossen werden kann, muss Auftrag 3 kommissioniert werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="bf375-337">Geben Sie die Arbeits-ID für Auftrag 3 ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="bf375-338">Für diese Arbeits-ID gibt es nur eine Entnahmeaufgabe.</span><span class="sxs-lookup"><span data-stu-id="bf375-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="bf375-339">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-339">Select **OK**.</span></span>

    <span data-ttu-id="bf375-340">Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="bf375-341">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="bf375-342">Das von Ihnen angegebene Kennzeichen ist eines der vom System generierten Kennzeichen aus den Wiederbeschaffungsarbeitsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="bf375-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="bf375-343">Um sicherzustellen, dass Sie die richtige Kennzeichen-ID erfassen, überprüfen Sie auf der Seite **Bestandsliste** den Bestand für Artikel, Lagerplatz und Menge.</span><span class="sxs-lookup"><span data-stu-id="bf375-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="bf375-344">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="bf375-345">Bestätigen Sie die Anweisungen für die Einlagerungsaufgabe am ausgehenden Bereitstellungslagerplatz.</span><span class="sxs-lookup"><span data-stu-id="bf375-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="bf375-346">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-346">Select **OK**.</span></span>

    <span data-ttu-id="bf375-347">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf375-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="bf375-348">Sobald die Summe der Bestandsmenge am Kommissionierort und der Wiederbeschaffungsmenge unter dem Schwellenwert liegt, können Sie die verbleibenden Wiederbeschaffungsarbeiten bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf375-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="bf375-349">Gehen Sie zur Seite **Arbeitsdetails** zurück, und beachten Sie, dass die Verfügbarkeit der Wiederbeschaffungsarbeit für den letzten Wiederbeschaffungsteil (für Auftrag 2) *Offen* lautet, weil jetzt genügend Platz am Lagerplatz vorhanden ist, um die Wiederbeschaffung zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="bf375-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="bf375-350">Sie können diese Wiederbeschaffungsarbeit jetzt über das mobile Gerät bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf375-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="bf375-351">Gehen Sie zu **Lager \> Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="bf375-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="bf375-352">Sie werden aufgefordert, die verbleibende Wiederbeschaffungsarbeit abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bf375-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="bf375-353">Artikelnummer, -menge und -lagerplatz zur Entnahme werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="bf375-354">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bf375-355">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bf375-356">Das System generiert eine Zielkennzeichennummer für das neue Kennzeichen des entnommenen Artikels.</span><span class="sxs-lookup"><span data-stu-id="bf375-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="bf375-357">Wählen Sie **OK**, um den Wert zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="bf375-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="bf375-358">Es wird eine Einlagerungsarbeit angezeigt, die den Benutzer anweist, das Zielkennzeichen in den Wiederbeschaffungslagerplatz einzulagern.</span><span class="sxs-lookup"><span data-stu-id="bf375-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="bf375-359">Der *Einlagern*-Lagerplatz sollte **06A01R2S1B** lauten.</span><span class="sxs-lookup"><span data-stu-id="bf375-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="bf375-360">Bestätigen Sie die Einlagerungsdetails, und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="bf375-361">Sie erhalten die Meldungen „Arbeit erledigt“ und „Keine Arbeit verfügbar“.</span><span class="sxs-lookup"><span data-stu-id="bf375-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="bf375-362">Sie können nun Auftrag 2 kommissionieren.</span><span class="sxs-lookup"><span data-stu-id="bf375-362">You can now pick sales order 2.</span></span> <span data-ttu-id="bf375-363">Er wurde entsperrt, als die mit dem Auftrag verknüpfte Wiederbeschaffungsarbeit abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bf375-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="bf375-364">Geben Sie die Arbeits-ID für Auftrag 2 ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="bf375-365">Für diese Arbeits-ID gibt es nur eine Entnahmeaufgabe.</span><span class="sxs-lookup"><span data-stu-id="bf375-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="bf375-366">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-366">Select **OK**.</span></span>

    <span data-ttu-id="bf375-367">Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf375-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="bf375-368">Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf375-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="bf375-369">Das von Ihnen angegebene Kennzeichen ist das vom System generierte Kennzeichen aus der Wiederbeschaffungsarbeitsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="bf375-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="bf375-370">Um sicherzustellen, dass Sie die richtige Kennzeichen-ID erfassen, überprüfen Sie auf der Seite **Bestandsliste** den Bestand für Artikel, Lagerplatz und Menge.</span><span class="sxs-lookup"><span data-stu-id="bf375-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="bf375-371">Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.</span><span class="sxs-lookup"><span data-stu-id="bf375-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="bf375-372">Bestätigen Sie die Anweisungen für die Einlagerungsaufgabe am ausgehenden Bereitstellungslagerplatz.</span><span class="sxs-lookup"><span data-stu-id="bf375-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="bf375-373">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf375-373">Select **OK**.</span></span>

    <span data-ttu-id="bf375-374">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf375-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="bf375-375">Hinweise und Tipps</span><span class="sxs-lookup"><span data-stu-id="bf375-375">Notes and tips</span></span>

- <span data-ttu-id="bf375-376">Diese Funktionalität funktioniert mit allen Typen der Wiederbeschaffung: Wellenbedarf, Min./Max., Ladungsbedarf und Zuteilung von Zeitfenstern.</span><span class="sxs-lookup"><span data-stu-id="bf375-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="bf375-377">Sie können die Verfügbarkeit der Wiederbeschaffungsarbeit für jede Arbeitskopfzeile aus der Seite **Arbeitsdetails** manuell überschreiben, wenn Sie wollen.</span><span class="sxs-lookup"><span data-stu-id="bf375-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="bf375-378">Wenn das System die Verfügbarkeit der Wiederbeschaffungsarbeiten festlegt, berücksichtigt es alle Bestände, die sich bereits am Lagerplatz befinden, bevor Arbeiten abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="bf375-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="bf375-379">Jeder Teil der Auftragsarbeit ist mit einer bestimmten Wiederbeschaffungsarbeit verknüpft.</span><span class="sxs-lookup"><span data-stu-id="bf375-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="bf375-380">Es gibt keine entsprechende Verfügbarkeitsfunktion für Verkaufsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf375-380">There is no corresponding sales work availability functionality.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]