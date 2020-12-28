---
title: Put-to-Wall - Put-to-Store
description: Dieses Thema enthält Informationen zu den Funktionen „Put-to-Wall - Put-to-Store“. Mit dieser Funktion können Sie Szenarien behandeln, in denen Sie ein Produkt basierend auf konfigurierbaren Kriterien in einem Prepack-Staging-Bereich konsolidieren müssen. Dies verkürzt die Kommissionierzeit, da es die Kommissionierung auf ein einzelnes Zielkennzeichen ermöglicht und mehr Put-Positionen als die Cluster-Kommissionierung verwenden kann.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429038"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="84ecf-105">Put-to-Wall - Put-to-Store</span><span class="sxs-lookup"><span data-stu-id="84ecf-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84ecf-106">Mit der Funktion *Put-to-Wall - Put-to-Store* können Sie Szenarien behandeln, in denen Sie ein Produkt basierend auf konfigurierbaren Kriterien in einem Prepack-Staging-Bereich konsolidieren müssen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="84ecf-107">Da diese Funktion die Kommissionierung auf einem einzelnen Zielkennzeichen ermöglicht und mehr Put-Positionen als die Cluster-Kommissionierung verwenden kann, profitieren Unternehmen, die an Geschäfte liefern oder kleine Artikel bearbeiten, von einer kürzeren Kommissionierzeit.</span><span class="sxs-lookup"><span data-stu-id="84ecf-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="84ecf-108">Der Workflow für diese Funktionalität leitet das ausgewählte Produkt an einen Sortierort zur Verteilung in verschiedene Arten von Containern.</span><span class="sxs-lookup"><span data-stu-id="84ecf-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="84ecf-109">Im Allgemeinen enthält jeder Sortierort mehrere Sortierpositionen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="84ecf-110">Jede Sortierposition wird gemäß den vom Geschäftsprozess festgelegten Kriterien zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="84ecf-111">Typische Kriterien sind das endgültige Ziel, die Lieferung oder die Auslastung.</span><span class="sxs-lookup"><span data-stu-id="84ecf-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="84ecf-112">Nachdem ein Produkt angekommen ist, wird es basierend auf der Menge, die der Bestellung, dem Bestimmungsort, der Sendung oder der Ladung zugeordnet ist, an jede Sortierposition verteilt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="84ecf-113">Wenn ein Container voll oder vollständig ist, wird er je nach Geschäftsprozess zur weiteren Bearbeitung an einen Bereitstellungsort oder einen Versandort verschoben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="84ecf-114">Auf diese Warehousing-Funktion wird auch mit anderen Namen verwiesen, z. B. Aufleuchten und Öffnen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="84ecf-115">Aktivieren der Funktion „Ausgangssortierung“</span><span class="sxs-lookup"><span data-stu-id="84ecf-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="84ecf-116">Bevor Sie die Funktion *Put-to-Wall - Put-to-Store* verwenden können, muss die *Ausgangssortierung* in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="84ecf-117">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="84ecf-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="84ecf-118">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="84ecf-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="84ecf-119">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="84ecf-120">**Funktionsname:** *Ausgangssortierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="84ecf-121">Die Funktion *Ausgangssortierung* kann in Verbindung mit der Funktion *Organisationsweiter Wellenschrittcode* verwendet werden, wenn sie eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="84ecf-122">Sie müssen diese Funktion auch aktivieren, wenn Sie vordefinierte Codes verwenden, die in Wellenschrittcodes eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="84ecf-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="84ecf-123">Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="84ecf-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="84ecf-124">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="84ecf-125">**Funktionsname:** *Organisationsweiter Wellenschrittcode*</span><span class="sxs-lookup"><span data-stu-id="84ecf-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="84ecf-126">Einstellung</span><span class="sxs-lookup"><span data-stu-id="84ecf-126">Setup</span></span>

<span data-ttu-id="84ecf-127">Für diese Demo werden Standard-Contoso-Daten und Lagerotz *62* verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="84ecf-128">Einige Ergänzungen, die später erwähnt werden, werden ebenfalls verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="84ecf-129">Lagerplatztyp</span><span class="sxs-lookup"><span data-stu-id="84ecf-129">Location type</span></span>

1. <span data-ttu-id="84ecf-130">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatztypen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="84ecf-131">Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Lagerplatztyp zum Sortieren zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="84ecf-132">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-132">Set the following values:</span></span>

    - <span data-ttu-id="84ecf-133">**Lagerplatztyp:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="84ecf-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="84ecf-134">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="84ecf-135">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="84ecf-136">Parameter für Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="84ecf-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="84ecf-137">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="84ecf-138">Geben Sie im Registerkarte **Allgemein** im Inforegister **Lagerplatztypen** das Feld **Lagerplatztyp für Sortierung** *SORT* ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="84ecf-139">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="84ecf-140">Lagerortprofil</span><span class="sxs-lookup"><span data-stu-id="84ecf-140">Location profile</span></span>

1. <span data-ttu-id="84ecf-141">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="84ecf-142">Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um ein Lagerplatzprofil für den Sortierort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="84ecf-143">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="84ecf-144">**Lagerortprofilkennung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-145">**Name:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="84ecf-146">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="84ecf-147">**Lagerplatzformat:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="84ecf-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="84ecf-148">**Lagerplatztyp:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="84ecf-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="84ecf-149">**Kennzeichenverfolgung verwenden:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="84ecf-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="84ecf-150">**Gemischte Artikel zulassen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="84ecf-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="84ecf-151">**Gemischte Bestandstatus zulassen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="84ecf-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="84ecf-152">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="84ecf-153">Lagerplätze</span><span class="sxs-lookup"><span data-stu-id="84ecf-153">Locations</span></span>

1. <span data-ttu-id="84ecf-154">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="84ecf-155">Löschen Sie das Kontrollkästchen **Prüfziffern für den Lagerplatz erstellen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="84ecf-156">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="84ecf-157">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="84ecf-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="84ecf-158">**Lagerplatz:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-159">**Lagerortprofilkennung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="84ecf-160">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="84ecf-161">Verpackungsprofile</span><span class="sxs-lookup"><span data-stu-id="84ecf-161">Packing profiles</span></span>

1. <span data-ttu-id="84ecf-162">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Verpackungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="84ecf-163">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="84ecf-164">**Verpackungsprofilkennung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-165">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-166">**Containerverpackungsrichtlinien:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="84ecf-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="84ecf-167">**Containerkennungsmodus:** *Auto*</span><span class="sxs-lookup"><span data-stu-id="84ecf-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="84ecf-168">**Containertyp:** *PALETTE 48X48*</span><span class="sxs-lookup"><span data-stu-id="84ecf-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="84ecf-169">**Container beim Schließen des Containers automatisch erstellen:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="84ecf-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="84ecf-170">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="84ecf-171">Wellenschrittcodes</span><span class="sxs-lookup"><span data-stu-id="84ecf-171">Wave step codes</span></span>

<span data-ttu-id="84ecf-172">Wenn Sie die Funktion *Organisationsweiter Wellenschrittcode* eingeschaltet haben, richten Sie den folgenden Code ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="84ecf-173">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="84ecf-174">Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="84ecf-175">**Wellenschrittcode:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-176">**Wellenschrittbeschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-177">**Wellenschritttyp:** *Vorlage sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="84ecf-178">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="84ecf-179">Vorlage für ausgehende Sortierung</span><span class="sxs-lookup"><span data-stu-id="84ecf-179">Outbound sorting template</span></span>

<span data-ttu-id="84ecf-180">Die Sortiervorlage steuert, ob Sortierpositionen erstellt werden, welche Kriterien verwendet werden und andere Attribute des Sortierprozesses.</span><span class="sxs-lookup"><span data-stu-id="84ecf-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="84ecf-181">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Vorlage für die Ausgangssortierung**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="84ecf-182">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Sortiervorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="84ecf-183">Legen Sie in der Kopfzeile der neuen Vorlage die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="84ecf-184">**ID der Vorlage für die Ausgangssortierung:** *Wellensortierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="84ecf-185">**Beschreibung:** *Wellensortierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="84ecf-186">**Sortiervorlagentyp:** *Wellenbedarf*</span><span class="sxs-lookup"><span data-stu-id="84ecf-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="84ecf-187">Dieses Feld definiert den Prozess, für den die Sortiervorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="84ecf-188">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="84ecf-188">The following values are available:</span></span>

        - <span data-ttu-id="84ecf-189">**Wellenbedarf** – Die Sortiervorlage wird für den Prozess *Put-to-Wall* verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="84ecf-190">Dieser Vorlagentyp wird zur Umgehung der Verpackungsstation und Verarbeitung des Bestands direkt aus der Welle verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="84ecf-191">Sie können diesen Typ nur verwenden, wenn die Wellenprozessmethode **Sortieren** in der Wellenvorlage enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="84ecf-192">**Container** – Die Sortiervorlage wird für den Prozess *Palettenerstellung nach dem Verpacken* verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="84ecf-193">Dieser Vorlagentyp wird zur Verarbeitung von Containern verwendet, die an dieser Packstation geschlossen werden und auf Paletten sortiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="84ecf-194">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="84ecf-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="84ecf-195">**Lagerplatz:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="84ecf-196">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="84ecf-197">**Sortierbestätigung:** *Positionsscan*</span><span class="sxs-lookup"><span data-stu-id="84ecf-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="84ecf-198">Dieses Feld definiert die Überprüfung, die während des Sortierens erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="84ecf-199">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="84ecf-199">The following values are available:</span></span>

        - <span data-ttu-id="84ecf-200">Keiner</span><span class="sxs-lookup"><span data-stu-id="84ecf-200">None</span></span>
        - <span data-ttu-id="84ecf-201">Ladungsträgerscan</span><span class="sxs-lookup"><span data-stu-id="84ecf-201">License plate scan</span></span>
        - <span data-ttu-id="84ecf-202">Positionsscan</span><span class="sxs-lookup"><span data-stu-id="84ecf-202">Position scan</span></span>

    - <span data-ttu-id="84ecf-203">**Arbeit bei Schließen der Position erstellen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="84ecf-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="84ecf-204">Wenn diese Option auf *Ja* eingestellt ist, wird Arbeit erstellt, wenn die Position geschlossen wird, um den Bestand zum endgültigen Versandlagerplatz umzulagern.</span><span class="sxs-lookup"><span data-stu-id="84ecf-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="84ecf-205">Ist sie auf *Nein* festgelegt, wird Lagerbestand sofort für den Auftrag entnommen, wenn die Position geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="84ecf-206">**Positionszuweisung:** *Manuell*</span><span class="sxs-lookup"><span data-stu-id="84ecf-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="84ecf-207">Dieses Feld definiert die Art der Positionszuweisung.</span><span class="sxs-lookup"><span data-stu-id="84ecf-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="84ecf-208">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="84ecf-208">The following values are available:</span></span>

        - <span data-ttu-id="84ecf-209">**Manuell** – Der Benutzer muss immer angeben, in welche Position der Bestand sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="84ecf-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="84ecf-210">**Automatisch** – Das System automatisch den Bestand an eine Position, sofern möglich, basierend auf den Sortiervorlagenunterbrechungen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="84ecf-211">**Sortierpositionskriterien zuweisen:** *Nur die leere Position verwenden*</span><span class="sxs-lookup"><span data-stu-id="84ecf-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="84ecf-212">Dieses Feld steuert, ob der Bestand, der auf Sortierungspositionen bereits vorhanden ist, berücksichtigt wird, wenn eine Position für den Bedarf zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="84ecf-213">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="84ecf-213">The following values are available:</span></span>

        - <span data-ttu-id="84ecf-214">**Nur die leere Position verwenden** – Positionen, denen bereits Bestand zugeordnet ist, werden berücksichtigt</span><span class="sxs-lookup"><span data-stu-id="84ecf-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="84ecf-215">**Position als leer annehmen** – Jeder Bestand, der sich bereits auf der Position befindet, wird bei der Zuordnung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="84ecf-216">Alle verfügbaren Positionen werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-216">All available positions will be used.</span></span>

    - <span data-ttu-id="84ecf-217">**Wellenschrittcode:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="84ecf-218">Wenn die Funktion *Organisationsweiter Wellenschrittcode* eingeschaltet ist, muss der Wellenschrittcode *Sortieren* auch in Wellenschrittcodes eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="84ecf-219">**Sortierposition automatisch schließen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="84ecf-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="84ecf-220">Wenn diese Option auf *Ja* eingestellt ist, wird die Sortierungsposition automatisch geschlossen, wenn alle Arbeiten in der Position abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="84ecf-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="84ecf-221">**Anzahl der Sortierpositionen:** *3*</span><span class="sxs-lookup"><span data-stu-id="84ecf-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="84ecf-222">Dieses Feld definiert die maximale Anzahl von Sortierpositionen, die das System erstellen wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="84ecf-223">**Sortierpositionspräfix:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="84ecf-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="84ecf-224">Dieses Feld definiert das Präfix, das das System vor der Positionsnummer zuweist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="84ecf-225">**Sortierposition automatisch packen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="84ecf-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="84ecf-226">Wenn diese Option auf *Ja* eingestellt ist, wird der Bestand für die Sortierungsposition in einen Container verpackt, wenn die Position geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="84ecf-227">**Verpackungsprofilkennung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="84ecf-228">Dieses Feld definiert das Verpackungsprofil, das verwendet wird, wenn die Sortierungsposition in einen Container verpackt wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="84ecf-229">Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um die Kriterien anzugeben, die für diese Sortiervorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="84ecf-230">Wählen Sie im Abfragedialogfeld auf der Registerkarte **Sortieren** die Option **Neu** aus, um eine Position hinzuzufügen und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="84ecf-231">**Tabelle:** *Ladungsdetails*</span><span class="sxs-lookup"><span data-stu-id="84ecf-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="84ecf-232">**Abgeleitete Tabelle:** *Ladungsdetails*</span><span class="sxs-lookup"><span data-stu-id="84ecf-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="84ecf-233">**Feld:** *Lieferungs-ID*</span><span class="sxs-lookup"><span data-stu-id="84ecf-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="84ecf-234">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="84ecf-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="84ecf-235">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-235">Select **OK**.</span></span>
1. <span data-ttu-id="84ecf-236">Möglicherweise erhalten Sie die folgende Meldung: „Gruppierung wird zurückgesetzt, fortfahren?“</span><span class="sxs-lookup"><span data-stu-id="84ecf-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="84ecf-237">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-237">Select **Yes**.</span></span>

    <span data-ttu-id="84ecf-238">Die Schaltfläche **Vorlagenunterbrechungen für Ausgangssortierung** im Aktivitätsbereich wird verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84ecf-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="84ecf-239">Wählen Sie im Aktivitätsbereich **Vorlagenunterbrechungen für Ausgangssortierung**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="84ecf-240">Aktivieren Sie das Kontrollkästchen **Gruppieren nach Feld**, um nach Lieferungs-ID zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="84ecf-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="84ecf-241">Diese Einstellung erstellt eine Sortierposition pro Sendung, die ein Container in der Welle ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="84ecf-242">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="84ecf-243">Wellenverarbeitungsmethoden</span><span class="sxs-lookup"><span data-stu-id="84ecf-243">Wave process methods</span></span>

1. <span data-ttu-id="84ecf-244">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="84ecf-245">Wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="84ecf-246">Die Methode **Sortieren** wird der Liste der verfügbaren Methoden hinzugefügt, und der Wellenvorlagentyp *Lieferung* ist dafür ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="84ecf-247">Wellenvorlagen</span><span class="sxs-lookup"><span data-stu-id="84ecf-247">Wave templates</span></span>

<span data-ttu-id="84ecf-248">Bearbeiten Sie die Wellenvorlage, die für die Sortierung der Wellenanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="84ecf-249">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="84ecf-250">Wählen Sie im Feld **Wellenvorlagentyp** *Versand* aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="84ecf-251">Wählen Sie die vorhandene Vorlage **Standard-62-Lieferung** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="84ecf-252">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="84ecf-253">Nehmen Sie im Inforegister **Allgemein** die folgenden Änderungen vor:</span><span class="sxs-lookup"><span data-stu-id="84ecf-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="84ecf-254">Legen Sie die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* fest.</span><span class="sxs-lookup"><span data-stu-id="84ecf-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="84ecf-255">Legen Sie die Option **Offenen Wellen zuweisen** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="84ecf-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="84ecf-256">Richten Sie im Inforegister **Methoden** die Methode **Sortieren** ein:</span><span class="sxs-lookup"><span data-stu-id="84ecf-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="84ecf-257">Wählen Sie im Raster **Verbleibende Methoden** **Sortieren** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="84ecf-258">Wählen Sie die Schaltfläche mit dem Pfeil nach rechts aus, um **Sortieren** in das Raster **Ausgewählte Methoden** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="84ecf-259">Wählen Sie im Raster **Ausgewählte Methoden** **Sortieren** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="84ecf-260">Legen Sie das Feld **Wellenschrittcode** auf *Sortieren* fest.</span><span class="sxs-lookup"><span data-stu-id="84ecf-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="84ecf-261">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="84ecf-262">Menüelemente des mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="84ecf-262">Mobile device menu items</span></span>

1. <span data-ttu-id="84ecf-263">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="84ecf-264">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="84ecf-265">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="84ecf-266">**Menüelementname:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-267">**Titel:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="84ecf-268">**Modus:** *Indirekt*</span><span class="sxs-lookup"><span data-stu-id="84ecf-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="84ecf-269">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="84ecf-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="84ecf-270">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="84ecf-271">**Aktivitätscode:** *Ausgangssortierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="84ecf-272">**Prozessleitfaden verwenden:** *Ja* (Standardwert)</span><span class="sxs-lookup"><span data-stu-id="84ecf-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="84ecf-273">**ID der Vorlage für die Ausgangssortierung:** *Wellensortierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="84ecf-274">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="84ecf-275">Menü für mobiles Gerät</span><span class="sxs-lookup"><span data-stu-id="84ecf-275">Mobile device menu</span></span>

1. <span data-ttu-id="84ecf-276">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="84ecf-277">Wählen Sie in der Liste der Menüs **Ausgehend** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="84ecf-278">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="84ecf-279">Suchen und wählen Sie inm Raster **Verfügbare Menüs und Menüpunkte** den Menüpunkt **Sortieren** aus, den Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="84ecf-280">Wählen Sie die rechte Pfeiltaste, um **Sortieren** zum Raster **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="84ecf-281">Auf diese Weise fügen Sie dem ausgewählten Menü den Menüpunkt **Ausgehend** hinzu.</span><span class="sxs-lookup"><span data-stu-id="84ecf-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="84ecf-282">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="84ecf-283">Lagerplatzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="84ecf-283">Location directives</span></span>

<span data-ttu-id="84ecf-284">Sie müssen Standortanweisungen erstellen, um die Arbeit zu steuern, die nach Abschluss der Sortierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="84ecf-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="84ecf-285">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="84ecf-286">Wählen Sie im Feld **Arbeitsauftragsart** *Sortierte Bestandsentnahme*.</span><span class="sxs-lookup"><span data-stu-id="84ecf-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="84ecf-287">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="84ecf-288">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="84ecf-289">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="84ecf-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="84ecf-290">**Name:** *Zu Frachttür bringen*</span><span class="sxs-lookup"><span data-stu-id="84ecf-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="84ecf-291">Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="84ecf-292">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="84ecf-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="84ecf-293">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="84ecf-293">**Site:** *6*</span></span>
    - <span data-ttu-id="84ecf-294">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="84ecf-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="84ecf-295">**Richtliniencode:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="84ecf-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="84ecf-296">**Mehrfach-SKU:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="84ecf-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="84ecf-297">Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="84ecf-298">Legen Sie im Inforegister **Positionen** die Option **Neu** aus und stellen Sie dann die folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="84ecf-299">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="84ecf-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="84ecf-300">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="84ecf-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="84ecf-301">**Von Menge:** *0*</span><span class="sxs-lookup"><span data-stu-id="84ecf-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="84ecf-302">**Bis Menge:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="84ecf-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="84ecf-303">Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="84ecf-304">Legen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und stellen Sie dann die folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="84ecf-305">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="84ecf-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="84ecf-306">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="84ecf-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="84ecf-307">**Name:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="84ecf-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="84ecf-308">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="84ecf-309">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="84ecf-310">Suchen Sie im Abfragedialogfeld auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="84ecf-311">Legen Sie das Feld **Kriterien** für diese Zeile auf *Baydoor* fest.</span><span class="sxs-lookup"><span data-stu-id="84ecf-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="84ecf-312">Wählen Sie **OK**, um die Bearbeitung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="84ecf-313">Arbeitsklassen</span><span class="sxs-lookup"><span data-stu-id="84ecf-313">Work classes</span></span>

1. <span data-ttu-id="84ecf-314">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="84ecf-315">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="84ecf-316">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="84ecf-317">**Arbeitsklassen-ID:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="84ecf-318">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="84ecf-319">**Arbeitsauftragstyp:** *Sortierte Bestandsentnahme*</span><span class="sxs-lookup"><span data-stu-id="84ecf-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="84ecf-320">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="84ecf-321">Arbeitsvorlagen</span><span class="sxs-lookup"><span data-stu-id="84ecf-321">Work templates</span></span>

1. <span data-ttu-id="84ecf-322">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="84ecf-323">Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="84ecf-324">Wählen Sie im Raster die Arbeitsvorlage **62 entnehmen für Paket** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="84ecf-325">Wählen Sie im Aktivitätsbereich **Arbeitskopfzeilenumbrüche** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="84ecf-326">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="84ecf-327">Löschen Sie in der Position, in der das Feld **Feldname** auf *Lieferungs-ID* gesetzt ist, das Kontrollkästchen **Nach diesem Feld gruppieren**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="84ecf-328">Wählen Sie **Speichern** und schließen Sie dann das Dialogfeld **Arbeitskopfzeilenumbrüche**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="84ecf-329">Wählen Sie im Feld **Arbeitsauftragsart** *Sortierte Bestandsentnahme*.</span><span class="sxs-lookup"><span data-stu-id="84ecf-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="84ecf-330">Wählen Sie **Neu** aus, um eine Arbeitsvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="84ecf-331">Legen Sie im Abschnitt **Übersicht** die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="84ecf-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="84ecf-332">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="84ecf-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="84ecf-333">**Arbeitsvorlage:** *Sortierte Kommissionierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="84ecf-334">**Arbeitsvorlagenbeschreibung:** *Sortierte Kommissionierung*</span><span class="sxs-lookup"><span data-stu-id="84ecf-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="84ecf-335">Wählen Sie **Speichern** aus, um den Abschnitt **Arbeitsvorlagendetails** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="84ecf-336">Im Abschnitt **Arbeitsvorlagendetails** erstellen Sie zwei Zeilen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="84ecf-337">Wählen Sie **Neu** aus, und legen Sie dann die folgenden Werte für Position 1 fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="84ecf-338">**Arbeitstyp:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="84ecf-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="84ecf-339">**Obligatorisch:** Ausgewählt (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="84ecf-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="84ecf-340">**Arbeitsklassen-ID:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="84ecf-341">Wählen Sie erneut **Neu** aus, und legen Sie dann die folgenden Werte für Position 2 fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="84ecf-342">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="84ecf-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="84ecf-343">**Obligatorisch:** Ausgewählt (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="84ecf-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="84ecf-344">**Arbeitsklassen-ID:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="84ecf-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="84ecf-345">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="84ecf-346">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="84ecf-346">Example scenario</span></span>

<span data-ttu-id="84ecf-347">Dieses Szenario simuliert eine Situation, in der das Lager kleine Artikel an Standorten lagert und diese vor dem Versand in Kartons verpacken muss und in denen die Funktionalität der Packstation nicht wirklich geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="84ecf-348">Mitarbeiter kommissionieren gleichzeitig Bestellungen für mehrere Kunden und unterschiedliche Adressen, um die Kommissioniergeschwindigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="84ecf-349">Nach Abschluss der Kommissionierung erreichen die Mitarbeiter den Sortierort, an dem die kommissionierten Artikel anhand der erforderlichen Kriterien in die richtige Box sortiert werden können.</span><span class="sxs-lookup"><span data-stu-id="84ecf-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="84ecf-350">In diesem Beispiel wird die Lieferungs-ID verwendet, um das richtige Feld zu bestimmen, da jede Lieferung eine andere Adresse hat.</span><span class="sxs-lookup"><span data-stu-id="84ecf-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="84ecf-351">Nachdem alle Artikel aus der Ladung verpackt und nach Versand sortiert wurden, werden die Kartons in den Bereitstellungsbereich gebracht und schließlich auf einen LKW verladen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="84ecf-352">Stellen Sie vor dem Starten des Szenarios sicher, dass alle Standard-Warehouse-Funktionen für Ihren Lagerort korrekt eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="84ecf-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="84ecf-353">Standard-Contoso-Lagerort *62* wird zu diesem Zweck verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ecf-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="84ecf-354">Die Standardkonfigurationen wurden außer den in den Einstellungen beschriebenen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="84ecf-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="84ecf-355">Bedarf erstellen</span><span class="sxs-lookup"><span data-stu-id="84ecf-355">Create demand</span></span>

<span data-ttu-id="84ecf-356">Bevor die Funktionalität demonstriert werden kann, müssen Sie eine Nachfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="84ecf-357">In diesem Szenario erstellen Sie drei Kundenaufträge für drei verschiedene Kunden, um verschiedene Lieferadressen zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="84ecf-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="84ecf-358">Auf diese Weise erstellen Sie drei separate Sendungen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="84ecf-359">Bevor Sie Aufträge und Lieferungen erstellen, müssen Sie sicherstellen, dass die Entnahmeorte über genügend Bestand für alle Artikel in den Aufträgen verfügen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="84ecf-360">Überprüfen Sie die Einstellungen der Standortrichtlinie, um die Kommissionierorte zu bestätigen, die für die Kundenauftragskommissionierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="84ecf-361">Wenn Sie den Lagerbestand anpassen müssen, können Sie manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow verwenden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="84ecf-362">Reservieren Sie dann den Bestand.</span><span class="sxs-lookup"><span data-stu-id="84ecf-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="84ecf-363">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="84ecf-364">Wählen Sie **Neu** aus, um einen Auftrag für Auftrag 1 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="84ecf-365">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="84ecf-366">**Kunde:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="84ecf-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="84ecf-367">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="84ecf-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84ecf-368">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-368">Select **OK**.</span></span>
1. <span data-ttu-id="84ecf-369">Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="84ecf-370">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-370">Set the following values:</span></span>

    - <span data-ttu-id="84ecf-371">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="84ecf-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="84ecf-372">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="84ecf-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="84ecf-373">Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="84ecf-374">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="84ecf-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="84ecf-375">**Menge** *10*</span><span class="sxs-lookup"><span data-stu-id="84ecf-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="84ecf-376">Wiederholen Sie die folgenden Schritte für jede Verkaufsposition in der Bestellung, um Bestand dafür zu reservieren:</span><span class="sxs-lookup"><span data-stu-id="84ecf-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="84ecf-377">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="84ecf-378">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="84ecf-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="84ecf-379">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-379">Select **Save**.</span></span>

1. <span data-ttu-id="84ecf-380">Wählen Sie **Neu** aus, um einen Auftrag für Auftrag 2 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="84ecf-381">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="84ecf-382">**Kunde:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="84ecf-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="84ecf-383">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="84ecf-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84ecf-384">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-384">Select **OK**.</span></span>
1. <span data-ttu-id="84ecf-385">Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="84ecf-386">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-386">Set the following values:</span></span>

    - <span data-ttu-id="84ecf-387">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="84ecf-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="84ecf-388">**Menge** *7*</span><span class="sxs-lookup"><span data-stu-id="84ecf-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="84ecf-389">Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="84ecf-390">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="84ecf-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="84ecf-391">**Menge** *3*</span><span class="sxs-lookup"><span data-stu-id="84ecf-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="84ecf-392">Wiederholen Sie die folgenden Schritte für jede Verkaufsposition in der Bestellung, um Bestand dafür zu reservieren:</span><span class="sxs-lookup"><span data-stu-id="84ecf-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="84ecf-393">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="84ecf-394">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="84ecf-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="84ecf-395">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-395">Select **Save**.</span></span>

1. <span data-ttu-id="84ecf-396">Wählen Sie **Neu** aus, um einen Auftrag für Auftrag 3 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="84ecf-397">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="84ecf-398">**Kunde:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="84ecf-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="84ecf-399">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="84ecf-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84ecf-400">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-400">Select **OK**.</span></span>
1. <span data-ttu-id="84ecf-401">Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="84ecf-402">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84ecf-402">Set the following values:</span></span>

    - <span data-ttu-id="84ecf-403">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="84ecf-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="84ecf-404">**Menge** *8*</span><span class="sxs-lookup"><span data-stu-id="84ecf-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="84ecf-405">Um Bestand für die Verkaufsposition zu reservieren, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="84ecf-406">Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="84ecf-407">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="84ecf-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="84ecf-408">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-408">Select **Save**.</span></span>

<span data-ttu-id="84ecf-409">Führen Sie die folgenden Schritte aus, um jeden Kundenauftrag an das Lager freizugeben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="84ecf-410">Es werden drei verschiedene Sendungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-410">Three different shipments will be created.</span></span> <span data-ttu-id="84ecf-411">Sie werden dann alle drei Sendungen zu einer neuen Welle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="84ecf-412">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="84ecf-413">Wählen Sie im Raster den ersten Kundenauftrag aus, den Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="84ecf-414">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="84ecf-415">Sie erhalten eine Informationsnachricht mit der Wellen-ID und der Lieferungs-ID, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="84ecf-416">Wiederholen Sie die vorherigen Schritte, um die Kundenaufträge 2 und 3 für das Lager freizugeben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="84ecf-417">Beachten Sie, dass die Informationsnachricht, die Sie erhalten, darauf hinweist, dass der Welle, die bei der Freigabe des Kundenauftrags 1 erstellt wurde, eine Sendung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="84ecf-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="84ecf-418">Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="84ecf-419">Wählen Sie die Wellen-ID, die von der Freigabe des Auftrags erstellt wurde, um die Seite **Wellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="84ecf-420">Diese Seite zeigt die Wellendetails.</span><span class="sxs-lookup"><span data-stu-id="84ecf-420">This page shows the wave details.</span></span> <span data-ttu-id="84ecf-421">Das Inforegister **Wellenpositionen** zeigt die Sendungen an, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="84ecf-422">Sie müssen jetzt Arbeit erstellen, um Artikel von den Kommissionierorten zum Sortierort zu bringen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="84ecf-423">Klicken Sie im Aktivitätsbereich auf **Verarbeiten**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="84ecf-424">Während der Wellenverarbeitung verwendet die Sortiermethode die Sortiervorlage, um den Bestand den Sortierpositionen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="84ecf-425">Nach Abschluss der Wellenverarbeitung erhalten Sie eine Informationsmeldung, die angibt, dass die Welle gebucht und Arbeit erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="84ecf-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="84ecf-426">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Zugehörige Informationen** auf **Arbeit**, um die Arbeit anzuzeigen, die für diese Welle erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="84ecf-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="84ecf-427">Notieren Sie die Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="84ecf-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="84ecf-428">Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Zuweisungen von Ausgangssortierpositionen**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="84ecf-429">In der linken Spalte können Sie die ausgehende Sortierposition anzeigen, die für jede Sendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="84ecf-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="84ecf-430">Im Inforegister **Sortierpositionskriterien** können Sie die Lieferungs-ID für diese Position anzeigen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="84ecf-431">Es wurde eine Arbeits-ID erstellt, um Bestand von den Kommissionierorten zum Sortierort zu bringen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="84ecf-432">Um die Arbeit abzuschließen, benötigen Sie die Arbeits-ID, die während der Wellenverarbeitung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="84ecf-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="84ecf-433">Kommissionierung von Kundenaufträgen zum Sortierort</span><span class="sxs-lookup"><span data-stu-id="84ecf-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="84ecf-434">Melden Sie sich bei der mobilen App als eine Arbeitskraft im Lagerort *62* an.</span><span class="sxs-lookup"><span data-stu-id="84ecf-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="84ecf-435">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="84ecf-436">Auf dem Menü **Ausgehend** wählen Sie **Verkaufsauswahl**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="84ecf-437">Wählen Sie das Feld **ID** aus, und geben Sie dann die Arbeits-ID aus der Wellenverarbeitung ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="84ecf-438">Bestätigen Sie Ihre Eingabe.</span><span class="sxs-lookup"><span data-stu-id="84ecf-438">Confirm your entry.</span></span>

    <span data-ttu-id="84ecf-439">Als Nächstes werden Sie aufgefordert, ein Zielkennzeichen (LP) einzugeben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="84ecf-440">Beachten Sie, dass Position 1 aus Kundenauftrag 1 ausgewählt und dem Zielkennzeichen hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="84ecf-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="84ecf-441">Die Artikelnummer, Menge, Artikelbeschreibung und der Kommissionierort werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="84ecf-442">Geben Sie in das Feld **Ziel-LP** eine Kennzeichennummer ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="84ecf-443">Sie wählen alle Positionen, die aus der verarbeiteten Welle erstellt wurden, auf demselben Zielkennzeichen aus.</span><span class="sxs-lookup"><span data-stu-id="84ecf-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="84ecf-444">Bestätigen Sie Ihre Eingabe.</span><span class="sxs-lookup"><span data-stu-id="84ecf-444">Confirm your entry.</span></span>

    <span data-ttu-id="84ecf-445">Die mobile App präsentiert nun eine Reihe von **Entnehmen**-Seiten, die Sie auf den Kommissionierort sowie auf den Artikel und die Menge verweisen, die kommissioniert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="84ecf-446">Nachdem der kommissionierte Artikel dem Kennzeichen hinzugefügt wurde, bestätigen Sie die Kommissionierarbeiten.</span><span class="sxs-lookup"><span data-stu-id="84ecf-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="84ecf-447">Die letzte Seite ist die Arbeit, um die ausgewählten Artikel an den Sortierort zu bringen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="84ecf-448">Bestätigen Sie die erste Entnahmearbeit.</span><span class="sxs-lookup"><span data-stu-id="84ecf-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="84ecf-449">Die nächste Entnahmearbeit wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-449">The next pick work is shown.</span></span> <span data-ttu-id="84ecf-450">Bestätigen Sie die Entnahme.</span><span class="sxs-lookup"><span data-stu-id="84ecf-450">Confirm the pick.</span></span>
1. <span data-ttu-id="84ecf-451">Bestätigen Sie dann die verbleibenden Kommissionierarbeiten.</span><span class="sxs-lookup"><span data-stu-id="84ecf-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="84ecf-452">Der letzte Schritt besteht darin, die Put-Arbeit abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-452">The last step is to complete the put work.</span></span> <span data-ttu-id="84ecf-453">Bestätigen Sie die Einlagerung an den Sortierort.</span><span class="sxs-lookup"><span data-stu-id="84ecf-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="84ecf-454">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="84ecf-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="84ecf-455">Verlassen Sie **Verkaufsauswahl** auf der mobilen App.</span><span class="sxs-lookup"><span data-stu-id="84ecf-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="84ecf-456">Sortieren/Put-to-Wall</span><span class="sxs-lookup"><span data-stu-id="84ecf-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="84ecf-457">Nachdem der gesamte Bestand an den Sortierort gebracht wurde, muss es an der richtigen Sortierposition sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="84ecf-458">Melden Sie sich bei der mobilen App an.</span><span class="sxs-lookup"><span data-stu-id="84ecf-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="84ecf-459">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="84ecf-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="84ecf-460">Wählen Sie im Menü **Ausgehend** **Sortieren** aus, um die Artikel zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="84ecf-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="84ecf-461">Geben Sie im Feld **LP/CON** das Zielkennzeichen der ausgewählten Kundenauftragsarbeit ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="84ecf-462">Bestätigen Sie Ihre Eingabe.</span><span class="sxs-lookup"><span data-stu-id="84ecf-462">Confirm your entry.</span></span>
1. <span data-ttu-id="84ecf-463">Geben Sie zuerst die zu sortierende Artikelnummer ein.</span><span class="sxs-lookup"><span data-stu-id="84ecf-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="84ecf-464">Das System bestimmt die erste Sortierposition, die angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84ecf-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="84ecf-465">Bestätigen Sie die Sortierposition.</span><span class="sxs-lookup"><span data-stu-id="84ecf-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="84ecf-466">Sie werden aufgefordert, der Sortierposition ein Kennzeichen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="84ecf-467">Wählen Sie das Feld **LP** aus, geben Sie ein Kennzeichen ein und bestätigen Sie Ihre Eingabe.</span><span class="sxs-lookup"><span data-stu-id="84ecf-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="84ecf-468">Da sich die Sortierposition auf die Lieferungs-ID bezieht, sortieren Sie die kommissionierten Artikel in ein Kennzeichen, das für die ausgehende Lieferung und den Kundenauftrag spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="84ecf-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="84ecf-469">Auf der nächsten Seite werden die Artikel-ID, die Menge, die Sortierpositions-ID sowie die Kennzeichen-IDs „von“ (Kommissionierung) und „bis“ (Sortierung) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="84ecf-470">Die Informationen auf dieser Seite weisen Sie an, den angegebenen Artikel und die angegebenen Mengen vom Kommissionierkennzeichen in das Sortierkennzeichen zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="84ecf-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="84ecf-471">Bestätigen Sie die Sortierposition.</span><span class="sxs-lookup"><span data-stu-id="84ecf-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="84ecf-472">Sortieren Sie die Artikel an der ersten Sortierposition.</span><span class="sxs-lookup"><span data-stu-id="84ecf-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="84ecf-473">Wenn Sie fertig sind, leitet Sie das System zur nächsten Sortierposition.</span><span class="sxs-lookup"><span data-stu-id="84ecf-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="84ecf-474">Wiederholen Sie diesen Vorgang für alle ausgewählten Positionen im Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="84ecf-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="84ecf-475">Sie sollten diesen Prozess auch verwenden, wenn mehrere Kommissionierzeilen dieselbe Artikelnummer haben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="84ecf-476">Wenn Sie diesen Vorgang für alle Artikel wiederholen, wertet das System die Kriterien des nächsten gescannten Artikel (Arbeitsposition) aus und bestimmt, an welche Sortierposition es verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="84ecf-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="84ecf-477">Sie werden automatisch angewiesen, den Artikel an die richtige Sortierposition zu bringen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="84ecf-478">Abhängig von der Bestätigungskonfiguration werden Sie auch angewiesen, diese Aktion durch Eingabe der Positionsnummer oder des Kennzeichens zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ecf-479">Wenn die automatische Sortierung aktiviert ist, ist kein manuelles Überschreiben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84ecf-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="84ecf-480">Wenn Sie fertig sind, öffnen Sie in Microsoft Dynamics 365 Supply Chain Management die Seite **Ausgehende Sortierungspositionszuweisungen**, um den Status der Positionen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="84ecf-481">Wenn Positionen automatisch geschlossen werden, wählen Sie **Geschlossene anzeigen**, um die geschlossenen Positionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="84ecf-482">Beachten Sie, dass Sortierpositionstransaktionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="84ecf-483">Der Artikel und die Menge, die über die Position verarbeitet wurden, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="84ecf-484">Wenn Sie die ausgehende Sortiervorlage einrichten, legen Sie die Option **Sortierposition automatisch schließen** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="84ecf-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="84ecf-485">Daher wird die Position automatisch geschlossen, nachdem der letzte erwartete Bestand darauf gelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="84ecf-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="84ecf-486">Die Sortierpositionen sind im Status **Geschlossen** und Arbeit wurde erstellt, um den sortierten Bestand zum Lagerplatz *Frachttür* zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="84ecf-487">Schließen Sie die Kommissionierarbeiten für sortierten Bestand ab, um den Bestand an den Versandort zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="84ecf-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="84ecf-488">Wenn der Bestand fertig ist, bestätigen Sie es für die Lieferung.</span><span class="sxs-lookup"><span data-stu-id="84ecf-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="84ecf-489">Damit die sortierte Bestandsauswahl korrekt verarbeitet werden kann, sollte ein Menüelement für mobile Geräte mit einer Arbeitsklassen-ID, in der das Feld **Arbeitsauftragstyp** auf *Sortierte Bestandsentnahme* festgelegt ist, für den Bewegungs- und Ladevorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="84ecf-490">Manuelles Schließen einer Position (optional)</span><span class="sxs-lookup"><span data-stu-id="84ecf-490">Manually close a position (optional)</span></span>

<span data-ttu-id="84ecf-491">Wenn Sortierpositionen manuell geschlossen werden sollen, muss die Option **Sortierposition automatisch schließen** für die Vorlage für die Ausgangssortierung auf *Nein* gesetzt sein und das Schließen muss erfolgen, bevor der Bestand in den Bereich der Frachttür gebracht werden kann.</span><span class="sxs-lookup"><span data-stu-id="84ecf-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="84ecf-492">Positionen können auf verschiedene Arten geschlossen werden:</span><span class="sxs-lookup"><span data-stu-id="84ecf-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="84ecf-493">Über die Warehouse-App:</span><span class="sxs-lookup"><span data-stu-id="84ecf-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="84ecf-494">Der Benutzer kann einen der Artikel scannen, die sich bereits an der Position befinden, und dann **Schließen** auswählen, um die Position zu schließen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="84ecf-495">Wenn der Benutzer einen Container sortiert, der bereits sortiert wurde, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="84ecf-496">Der Benutzer kann die Position jedoch weiterhin schließen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="84ecf-497">Über die Seite Microsoft Dynamics 365 Supply Chain Management **Ausgehende Sortierungspositionszuweisungen**:</span><span class="sxs-lookup"><span data-stu-id="84ecf-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="84ecf-498">Der Benutzer kann den ausgehenden Sortierpositionsdatensatz auswählen und dann im Aktionsbereich **Position schließen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="84ecf-499">Tipps</span><span class="sxs-lookup"><span data-stu-id="84ecf-499">Tips</span></span>

- <span data-ttu-id="84ecf-500">Artikel können nicht zwischen Positionen verschoben werden, nachdem sie einer zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="84ecf-501">Das System bewertet, wie viele von jedem Artikel an eine bestimmte Position gehen sollen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="84ecf-502">Die Sortiervorlage kann so konfiguriert werden, dass beim Schließen von Positionen automatisch Container erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="84ecf-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="84ecf-503">Dieser Ansatz erstellt eine Standard-Container-ID-Struktur, die auf dem angegebenen Verpackungsprofil basiert.</span><span class="sxs-lookup"><span data-stu-id="84ecf-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84ecf-504">Nachdem die Umlagerungsarbeit vom Sortierort aus erstellt wurde, dürfen Sie die Arbeit nicht abbrechen.</span><span class="sxs-lookup"><span data-stu-id="84ecf-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="84ecf-505">Andernfalls werden die Position und die darin enthaltenen Container aus dem System gelöscht und stehen nicht zur weiteren Verarbeitung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="84ecf-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="84ecf-506">Der Bestand wird ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="84ecf-506">The inventory will also be removed.</span></span>
