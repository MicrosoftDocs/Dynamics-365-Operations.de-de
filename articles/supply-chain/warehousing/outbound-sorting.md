---
title: Ausgangssortierung
description: Dieser Artikel enthält Informationen zur Ausgangssortierung. Diese Funktion erleichtert die Handhabung kleiner Container und hilft Lagerarbeitern, die Palettenkapazität im LKW besser zu planen und zu organisieren.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 44807e8d9915652c1c9d365de47d594a0c4f90e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225954"
---
# <a name="outbound-sorting"></a><span data-ttu-id="5b523-104">Ausgangssortierung</span><span class="sxs-lookup"><span data-stu-id="5b523-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b523-105">Diese Funktion erleichtert die Handhabung kleiner Container und hilft Lagerarbeitern, die Palettenkapazität im LKW besser zu planen und zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="5b523-106">Wenn Sie die Ausgangssortierung verwenden, können Sie verpackte Container auf der richtigen Palette sortieren, nachdem sie an einer Verpackungsstation waren.</span><span class="sxs-lookup"><span data-stu-id="5b523-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="5b523-107">Sie können auch eine Packungshierarchie erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b523-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="5b523-108">Mit dieser Funktion können Sie Paletten aus Containern erstellen, die über die Verpackungsfunktion verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="5b523-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="5b523-109">Der Container wird nicht an den endgültigen Versandort gesendet, da er sich im ursprünglichen Verpackungsflow befindet.</span><span class="sxs-lookup"><span data-stu-id="5b523-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="5b523-110">Stattdessen können Mitarbeiter den Container schließen und an einen Lagerplatz für Sortiertypen verschieben.</span><span class="sxs-lookup"><span data-stu-id="5b523-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="5b523-111">Sie können dann Container nach Positionen sortieren, von denen jede ein Kennzeichen (LP) hat.</span><span class="sxs-lookup"><span data-stu-id="5b523-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="5b523-112">Nachdem die Container sortiert wurden, kann eine Arbeit erstellt werden, um das gesamte LP basierend auf den Standortanweisungen oder Ihren eigenen Anforderungen an das endgültige Versanddock oder die endgültigen Bühnenstandorte zu senden.</span><span class="sxs-lookup"><span data-stu-id="5b523-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="5b523-113">Darüber hinaus kann durch das Schließen der Sortierposition den Bestand sofort an den endgültigen Versandort verschoben und in die Bestellung aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="5b523-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="5b523-114">Aktivieren der Funktion „Ausgangssortierung“</span><span class="sxs-lookup"><span data-stu-id="5b523-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="5b523-115">Bevor Sie die Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5b523-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="5b523-116">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5b523-117">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="5b523-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5b523-118">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="5b523-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5b523-119">**Funktionsname:** *Ausgangssortierung*</span><span class="sxs-lookup"><span data-stu-id="5b523-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="5b523-120">Einstellung</span><span class="sxs-lookup"><span data-stu-id="5b523-120">Setup</span></span>

<span data-ttu-id="5b523-121">Für dieses Szenario müssen Sie standardmäßige **USMF**-Demodaten und Lager *62* verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b523-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="5b523-122">Sie müssen auch die in den folgenden Unterabschnitten beschriebenen Einstellungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="5b523-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="5b523-123">Richten Sie eine Wellenvorlage ein</span><span class="sxs-lookup"><span data-stu-id="5b523-123">Set up a wave template</span></span>

<span data-ttu-id="5b523-124">Durch diese Einstellungen wird die Welle automatisch verarbeitet und Arbeit erstellt, wenn eine Position an den Lagerort freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b523-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="5b523-125">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5b523-126">Wählen Sie in der Vorlagenliste **Lagerort 62**.</span><span class="sxs-lookup"><span data-stu-id="5b523-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="5b523-127">Stellen Sie im Inforegister **Allgemein** sicher, dass die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Ja* eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="5b523-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="5b523-128">Einrichten einer Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="5b523-128">Set up a worker</span></span>

<span data-ttu-id="5b523-129">Die Verpackungsstation gilt als Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="5b523-129">The packing station is considered a location.</span></span> <span data-ttu-id="5b523-130">Lagerarbeiter, die sich an der Verpackungsstation anmelden, sehen und bearbeiten nur Sendungen und Container, die an diesem bestimmten Verpackungsort geplant sind.</span><span class="sxs-lookup"><span data-stu-id="5b523-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="5b523-131">Ein Benutzer, der sich bei Microsoft Dynamics 365 anmeldet, muss als Arbeitskraft in der Lagerortverwaltung eingerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="5b523-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="5b523-132">Wenn der Name des Benutzers nicht in der Liste der Arbeitsbenutzer angezeigt wird, fügen Sie ihn wie folgt hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b523-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="5b523-133">Diese Schritte setzen voraus, dass der Benutzer bereits im System vorhanden ist und als Mitarbeiter oder Arbeitskraft im Modul **Personalverwaltung** zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="5b523-134">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.</span><span class="sxs-lookup"><span data-stu-id="5b523-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="5b523-135">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-135">Select **New**.</span></span>
1. <span data-ttu-id="5b523-136">Wählen Sie im Feld **Arbeitskraft** den Zielbenutzer in der Liste der Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="5b523-137">Wählen Sie **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-137">Select **Select**.</span></span>
1. <span data-ttu-id="5b523-138">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b523-139">Wählen Sie im Inforegister **Benutzer** **Neu** aus, um ein Konto für mobile Geräte zu erstellen und die folgenden Werte dafür festzulegen:</span><span class="sxs-lookup"><span data-stu-id="5b523-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="5b523-140">**Benutzer-ID:** Geben Sie eine eindeutige ID ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="5b523-141">**Benutzername:** Geben Sie einen Namen für die ID ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="5b523-142">**Standardlagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-143">**Menüname:** *Hauptseite*</span><span class="sxs-lookup"><span data-stu-id="5b523-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="5b523-144">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b523-145">Das Dialogfeld **Passwort festlegen** wird angezeigt, in dem Sie ein einfaches Kennwort erstellen können, mit dem sich der Benutzer bei der mobilen App anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="5b523-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="5b523-146">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-146">Set the following values:</span></span>

    - <span data-ttu-id="5b523-147">**Passwort:** Geben Sie ein einfaches Passwort ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="5b523-148">**Passwort bestätigen:** Geben Sie das gleiche Passwort erneut ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="5b523-149">**Kennwortzurücksetzung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5b523-149">Select **Set password**.</span></span>

    <span data-ttu-id="5b523-150">Eine Benachrichtigung im Aktionszentrum informiert Sie darüber, dass das Kennwort für den von Ihnen erstellten Benutzer festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="5b523-151">Erstellen eines Lagerplatztyps</span><span class="sxs-lookup"><span data-stu-id="5b523-151">Create a location type</span></span>

1. <span data-ttu-id="5b523-152">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatztypen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="5b523-153">Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Lagerplatztyp zu erstellen und die folgenden Werte dafür festzulegen:</span><span class="sxs-lookup"><span data-stu-id="5b523-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="5b523-154">**Lagerplatztyp:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="5b523-155">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="5b523-156">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="5b523-157">Parameter für Lagerortverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="5b523-158">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="5b523-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="5b523-159">Legen Sie im Registerkarte **Allgemein** im Inforegister **Lagerplatztypen** das Feld **Lagerplatztyp für Sortierung** auf *SORT* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="5b523-160">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="5b523-161">Lagerplatzprofil einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-161">Set up a location profile</span></span>

1. <span data-ttu-id="5b523-162">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="5b523-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="5b523-163">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-164">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="5b523-165">**Lagerortprofilkennung:** *Sortierung*</span><span class="sxs-lookup"><span data-stu-id="5b523-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="5b523-166">**Name:** *Sortierung*</span><span class="sxs-lookup"><span data-stu-id="5b523-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="5b523-167">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-168">**Lagerplatzformat:** *ASRB* (Gang-Regal-Regalboden-Lagerfach)</span><span class="sxs-lookup"><span data-stu-id="5b523-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="5b523-169">**Lagerplatztyp:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="5b523-170">**Kennzeichenverfolgung verwenden:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="5b523-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="5b523-171">**Gemischte Artikel zulassen:** *Ja* (Wenn Sie diese Option auf *Ja* setzen, wird die Option **Gemischte Bestandchargenoption zulassen** automatisch auf *Ja* gesetzt und kann nicht unabhängig geändert werden.)</span><span class="sxs-lookup"><span data-stu-id="5b523-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="5b523-172">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="5b523-173">Lagerplatz einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-173">Set up a location</span></span>

1. <span data-ttu-id="5b523-174">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**.</span><span class="sxs-lookup"><span data-stu-id="5b523-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="5b523-175">Löschen Sie in der Kopfzeile das Kontrollkästchen **Prüfziffern für den Lagerplatz erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="5b523-176">Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Lagerplatz zu erstellen und die folgenden Werte dafür festzulegen:</span><span class="sxs-lookup"><span data-stu-id="5b523-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="5b523-177">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-178">**Lagerplatz:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="5b523-179">**Lagerortprofilkennung:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="5b523-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="5b523-180">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="5b523-181">Einrichten einer Vorlage für die Ausgangssortierung</span><span class="sxs-lookup"><span data-stu-id="5b523-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="5b523-182">Die Vorlage für die Ausgangssortierung bestimmt, ob die Arbeit außerhalb des Sortierorts erstellt wird und ob die Sortierung manuell oder automatisch erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5b523-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="5b523-183">In diesem Szenario erstellen Sie eine Vorlage für die Ausgangssortierung, um Paletten nach der Verpackungsstation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b523-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="5b523-184">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Vorlage für die Ausgangssortierung**.</span><span class="sxs-lookup"><span data-stu-id="5b523-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="5b523-185">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-186">Legen Sie in der Kopfzeile der neuen Vorlage die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="5b523-187">**ID der Vorlage für die Ausgangssortierung:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="5b523-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="5b523-188">**Beschreibung:** *Automatische Arbeitserstellung*</span><span class="sxs-lookup"><span data-stu-id="5b523-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="5b523-189">**Vorlagentyp für Ausgangssortierung:** *Container*</span><span class="sxs-lookup"><span data-stu-id="5b523-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="5b523-190">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-191">**Lagerplatz:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="5b523-192">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-193">**Sortierbestätigung:** *Positionsscan*</span><span class="sxs-lookup"><span data-stu-id="5b523-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="5b523-194">**Arbeit bei Schließen der Position erstellen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="5b523-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="5b523-195">Wenn diese Option auf *Ja* eingestellt ist, wird Arbeit erstellt, wenn die Position geschlossen wird, um den Bestand zum endgültigen Versandlagerplatz umzulagern.</span><span class="sxs-lookup"><span data-stu-id="5b523-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="5b523-196">Ist sie auf *Nein* festgelegt, wird Lagerbestand sofort für den Auftrag entnommen, wenn die Position geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5b523-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="5b523-197">**Positionszuweisung:** *Automatisch*</span><span class="sxs-lookup"><span data-stu-id="5b523-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="5b523-198">Ist dieses Feld auf *Manuell* eingestellt, muss der Benutzer immer angeben, in welche Position der Bestand sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b523-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="5b523-199">Ist es auf *Automatisch* eingestellt, leitet das System automatisch den Bestand an eine Position, sofern möglich, basierend auf den Sortiervorlagenunterbrechungen.</span><span class="sxs-lookup"><span data-stu-id="5b523-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="5b523-200">Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** im Aktivitätsbereich verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5b523-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="5b523-201">Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus</span><span class="sxs-lookup"><span data-stu-id="5b523-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="5b523-202">Fügen Sie im Abfrage-Editor auf der Registerkarte **Sortieren** eine Position mit den folgenden Werten ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="5b523-203">**Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="5b523-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5b523-204">**Abgeleitete Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="5b523-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5b523-205">**Feld:** *Spediteur*</span><span class="sxs-lookup"><span data-stu-id="5b523-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="5b523-206">Wenn Sie diesen Wert ausgewählt haben, wird möglicherweise die folgende Meldung angezeigt: „Das Spediteur-Feld ist kein Indexfeld.</span><span class="sxs-lookup"><span data-stu-id="5b523-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="5b523-207">Möchten Sie eine Sortierung hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="5b523-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="5b523-208">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-208">Select **Yes**.</span></span>

    - <span data-ttu-id="5b523-209">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="5b523-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5b523-210">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-210">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-211">Möglicherweise erhalten Sie die folgende Meldung: „Gruppierung wird zurückgesetzt, fortfahren?“</span><span class="sxs-lookup"><span data-stu-id="5b523-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="5b523-212">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-212">Select **Yes**.</span></span>

    <span data-ttu-id="5b523-213">Die Schaltfläche **Vorlagenunterbrechungen für Ausgangssortierung** im Aktivitätsbereich wird verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5b523-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="5b523-214">Wählen Sie im Aktivitätsbereich **Vorlagenunterbrechungen für Ausgangssortierung**.</span><span class="sxs-lookup"><span data-stu-id="5b523-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="5b523-215">Legen Sie im Dialogfeld **Ausgehende Sortierkriterien** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5b523-216">**Name der Referenztabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="5b523-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="5b523-217">**Name des Referenzfelds:** *Spediteur*</span><span class="sxs-lookup"><span data-stu-id="5b523-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="5b523-218">**Gruppieren nach Feld:** Aktivieren Sie dieses Kontrollkästchen, um Sendungen nach Spedition zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="5b523-219">Wählen Sie **OK**, um Ihre Einstellungen zu speichern und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5b523-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="5b523-220">Einrichten von Containerverpackungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="5b523-220">Set up container packing policies</span></span>

1. <span data-ttu-id="5b523-221">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Container \> Containerverpackungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="5b523-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="5b523-222">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-223">Legen Sie in der Kopfzeile der neuen Richtlinie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="5b523-224">**Containerverpackungsrichtlinien:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="5b523-225">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="5b523-226">Legen Sie im Inforegister **Übersicht** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-227">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-228">**Standardlagerplatz für die Sortierung:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="5b523-229">**Gewichtseinheit:** *kg*</span><span class="sxs-lookup"><span data-stu-id="5b523-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="5b523-230">**Richtlinie zum Containerabschluss:** *Automatische Freigabe*</span><span class="sxs-lookup"><span data-stu-id="5b523-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="5b523-231">**Richtlinie zur Containerfreigabe:** *Container der ausgehenden Sortierposition zuweisen*</span><span class="sxs-lookup"><span data-stu-id="5b523-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="5b523-232">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="5b523-233">Richten Sie Verpackungsprofile ein</span><span class="sxs-lookup"><span data-stu-id="5b523-233">Set up packing profiles</span></span>

<span data-ttu-id="5b523-234">Erstellen Sie ein neues Verpackungsprofil, das zusammen mit der Sortierfunktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b523-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="5b523-235">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Verpackungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="5b523-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="5b523-236">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen und die folgenden Werte dafür festzulegen:</span><span class="sxs-lookup"><span data-stu-id="5b523-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="5b523-237">**Verpackungsprofilkennung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="5b523-238">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="5b523-239">**Containerverpackungsrichtlinien:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="5b523-240">**Containerkennungsmodus:** *Auto*</span><span class="sxs-lookup"><span data-stu-id="5b523-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="5b523-241">**Containertyp:** *Box-Groß*</span><span class="sxs-lookup"><span data-stu-id="5b523-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="5b523-242">**Container beim Schließen des Containers automatisch erstellen:** Gelöscht (= *Nein*)</span><span class="sxs-lookup"><span data-stu-id="5b523-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="5b523-243">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="5b523-244">Arbeitsklassen einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-244">Set up work classes</span></span>

<span data-ttu-id="5b523-245">Richten Sie eine Arbeitsklasse ein, die zusammen mit dem Sortieren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b523-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="5b523-246">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="5b523-247">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsklasse zum Sortieren zu erstellen und die folgenden Werte dafür festzulegen:</span><span class="sxs-lookup"><span data-stu-id="5b523-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="5b523-248">**Arbeitsklassen-ID:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="5b523-249">**Beschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="5b523-250">**Arbeitsauftragstyp:** *Sortierte Bestandsentnahme*</span><span class="sxs-lookup"><span data-stu-id="5b523-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="5b523-251">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="5b523-252">Menüpunkte für mobiles Gerät einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="5b523-253">Menüpunkt für neue Palette einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="5b523-254">Erstellen Sie einen Menüpunkt für mobile Geräte, um Paletten während des Sortierens zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b523-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="5b523-255">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="5b523-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5b523-256">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-257">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="5b523-258">**Name des Menüelements:** *Palettenerstellung*</span><span class="sxs-lookup"><span data-stu-id="5b523-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="5b523-259">**Titel:** *Palettenerstellung*</span><span class="sxs-lookup"><span data-stu-id="5b523-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="5b523-260">**Modus:** *Indirekt*</span><span class="sxs-lookup"><span data-stu-id="5b523-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="5b523-261">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="5b523-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="5b523-262">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-263">**Aktivitätscode:** *Ausgangssortierung*</span><span class="sxs-lookup"><span data-stu-id="5b523-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="5b523-264">Wenn dieses Feld auf *Ausgangssortierung* eingestellt ist, wird das Feld **ID der Vorlage für die Ausgangssortierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b523-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="5b523-265">**Prozessleitfaden verwenden:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="5b523-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="5b523-266">Wenn das Feld **Aktivitätscode** auf *Ausgangssortierung* festgelegt ist, wird diese Option automatisch auf *Ja* gesetzt.</span><span class="sxs-lookup"><span data-stu-id="5b523-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="5b523-267">**ID der Vorlage für die Ausgangssortierung:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="5b523-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="5b523-268">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="5b523-269">Menüpunkt für neue Ladung einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-269">Set up a new loading menu item</span></span>

<span data-ttu-id="5b523-270">Erstellen Sie als Nächstes ein Menüelement, mit dem Benutzer die sortierten Bestandselemente an den Versandort verschieben können.</span><span class="sxs-lookup"><span data-stu-id="5b523-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="5b523-271">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="5b523-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5b523-272">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-273">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="5b523-274">**Name des Menüelements:** *Aus Sortierung laden*</span><span class="sxs-lookup"><span data-stu-id="5b523-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="5b523-275">**Titel:** *Aus Sortierung laden*</span><span class="sxs-lookup"><span data-stu-id="5b523-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="5b523-276">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="5b523-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="5b523-277">**Vorhandene Arbeit verwenden:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="5b523-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="5b523-278">Legen Sie im Inforegister **Allgemein** das Feld **Geleitet von** auf *Benutzergeleitet* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="5b523-279">Legen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus und stellen Sie dann die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="5b523-280">**Arbeitsklassenkennung:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="5b523-281">**Arbeitsauftragstyp:** *Sortierte Bestandsentnahme*</span><span class="sxs-lookup"><span data-stu-id="5b523-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="5b523-282">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="5b523-283">Menü für mobiles Gerät einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-283">Set up the mobile device menu</span></span>

<span data-ttu-id="5b523-284">Sie müssen jetzt die neuen Menüelemente zum Menü des Mobilgeräts hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b523-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="5b523-285">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="5b523-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="5b523-286">Wählen Sie das Menü **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="5b523-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="5b523-287">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5b523-288">Suchen Sie in der Spalte **Verfügbare Menüs und Menüpunkte** und wählen Sie **Palettenerstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="5b523-289">Wählen Sie die rechte Pfeiltaste, um **Palettenerstellung** zur Spalte **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5b523-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="5b523-290">Verwenden Sie die Aufwärtspfeil- und Abwärtspfeiltasten, um die Menüoption **Palettenerstellung** an die gewünschte Position im Menü des Mobilgeräts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5b523-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="5b523-291">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-291">Select **Save**.</span></span>
1. <span data-ttu-id="5b523-292">Wiederholen Sie diesen Vorgang, um die Menüoption **Aus Sortierung laden** zum Menü **Ausgehend** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b523-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="5b523-293">Lagerplatzrichtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-293">Set up location directives</span></span>

<span data-ttu-id="5b523-294">*Lagerplatzrichtlinien* sind Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerumlagerung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="5b523-295">Sie müssen jetzt eine Regel erstellen, um die Sortierarbeit zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5b523-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="5b523-296">Einrichten einer Richtlinie für eine einzelne SKU</span><span class="sxs-lookup"><span data-stu-id="5b523-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="5b523-297">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="5b523-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="5b523-298">Ändern Sie im linken Bereich den Wert des Felds **Arbeitsauftragstyp** zu *Sortierte Bestandsentnahme*.</span><span class="sxs-lookup"><span data-stu-id="5b523-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="5b523-299">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-300">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="5b523-301">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5b523-302">**Name:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="5b523-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="5b523-303">Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-304">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="5b523-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5b523-305">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="5b523-305">**Site:** *6*</span></span>
    - <span data-ttu-id="5b523-306">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-307">**Mehrfach-SKU:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="5b523-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="5b523-308">Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5b523-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="5b523-309">Legen Sie im Inforegister **Positionen** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="5b523-310">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="5b523-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5b523-311">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5b523-312">**Von:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b523-312">**From:** *0*</span></span>
    - <span data-ttu-id="5b523-313">**An:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="5b523-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="5b523-314">Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5b523-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="5b523-315">Legen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="5b523-316">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="5b523-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5b523-317">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5b523-318">**Name:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="5b523-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="5b523-319">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-319">Select **Save**.</span></span>
1. <span data-ttu-id="5b523-320">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="5b523-321">Suchen Sie im Abfrageeditor auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b523-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="5b523-322">Legen Sie das Feld **Kriterien** für diese Zeile auf *Baydoor* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="5b523-323">Wählen Sie **OK** aus, um Ihre Einstellungen zu speichern und den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5b523-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="5b523-324">Einrichten einer Richtlinie für eine Mehrfach-SKU</span><span class="sxs-lookup"><span data-stu-id="5b523-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="5b523-325">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="5b523-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="5b523-326">Ändern Sie im linken Bereich den Wert des Felds **Arbeitsauftragstyp** zu *Sortierte Bestandsentnahme*.</span><span class="sxs-lookup"><span data-stu-id="5b523-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="5b523-327">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-328">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="5b523-329">**Sequenz:** *2*</span><span class="sxs-lookup"><span data-stu-id="5b523-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="5b523-330">**Name:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="5b523-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="5b523-331">Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-332">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="5b523-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5b523-333">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="5b523-333">**Site:** *6*</span></span>
    - <span data-ttu-id="5b523-334">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-335">**Mehrfach-SKU:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="5b523-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="5b523-336">Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5b523-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="5b523-337">Legen Sie im Inforegister **Positionen** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="5b523-338">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="5b523-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5b523-339">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5b523-340">**Von:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b523-340">**From:** *0*</span></span>
    - <span data-ttu-id="5b523-341">**An:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="5b523-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="5b523-342">Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5b523-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="5b523-343">Legen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="5b523-344">Übernehmen Sie für alle anderen Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="5b523-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5b523-345">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5b523-346">**Name:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="5b523-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="5b523-347">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-347">Select **Save**.</span></span>
1. <span data-ttu-id="5b523-348">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="5b523-349">Suchen Sie im Abfrageeditor auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b523-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="5b523-350">Legen Sie das Feld **Kriterien** für diese Zeile auf *Baydoor* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="5b523-351">Wählen Sie **OK** aus, um Ihre Einstellungen zu speichern und den Abfrageeditor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5b523-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="5b523-352">Arbeitsvorlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="5b523-352">Set up work templates</span></span>

1. <span data-ttu-id="5b523-353">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="5b523-354">Ändern Sie den Wert des Felds **Arbeitsauftragstyp** zu *Sortierte Bestandsentnahme*.</span><span class="sxs-lookup"><span data-stu-id="5b523-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="5b523-355">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b523-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="5b523-356">Legen Sie auf der Registerkarte **Überblick** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="5b523-357">**Sequenz:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5b523-358">**Arbeitsvorlage:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="5b523-359">**Arbeitsvorlagenbeschreibung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="5b523-360">Wählen Sie **Speichern** aus, um das Inforegister **Arbeitsvorlagendetails** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5b523-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="5b523-361">Wählen Sie im Inforegister **Arbeitsvorlagendetails** die Option **Neu** aus, um eine Zeile hinzuzufügen und dann die folgenden Werte dafür festzulegen:</span><span class="sxs-lookup"><span data-stu-id="5b523-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="5b523-362">**Arbeitstyp:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="5b523-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="5b523-363">**Arbeitsklassenkennung:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="5b523-364">Wählen Sie erneut **Neu** aus, um eine zweite Position hinzuzufügen, und legen Sie dann die folgenden Werte dafür fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="5b523-365">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="5b523-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5b523-366">**Arbeitsklassenkennung:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5b523-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="5b523-367">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="5b523-368">Szenario</span><span class="sxs-lookup"><span data-stu-id="5b523-368">Scenario</span></span>

<span data-ttu-id="5b523-369">Dieses Szenario simuliert eine Situation, in der verpackte Container je nach Spedition automatisch nach verschiedenen Positionen (Paletten) nach der Verpackungsstation sortiert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="5b523-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="5b523-370">Nachdem alle Artikel aus der Ladung verpackt und nach Adresse sortiert wurden, werden die Paletten zur Frachttür gebracht.</span><span class="sxs-lookup"><span data-stu-id="5b523-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="5b523-371">Aufträge und Kommissionierarbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="5b523-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="5b523-372">Auftrag 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="5b523-372">Create sales order 1</span></span>

1. <span data-ttu-id="5b523-373">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="5b523-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5b523-374">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-375">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5b523-376">**Debitorenkonto:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="5b523-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="5b523-377">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b523-378">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5b523-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="5b523-379">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5b523-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="5b523-380">Wechseln Sie zur Ansicht **Kopfzeile**.</span><span class="sxs-lookup"><span data-stu-id="5b523-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="5b523-381">Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="5b523-382">**Spediteur:** *Luftfracht*</span><span class="sxs-lookup"><span data-stu-id="5b523-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="5b523-383">**Spediteur:** *Air*</span><span class="sxs-lookup"><span data-stu-id="5b523-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="5b523-384">Wechseln Sie zur Ansicht **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="5b523-385">Auf dem Inforegister **Kundenauftragspositionen** wählen Sie **Zeile hinzufügen**, wenn eine neue Zeile nicht automatisch zum Raster hinzugefügt wird, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="5b523-386">Stellen Sie die folgenden Werte für die neue Bestellposition ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="5b523-387">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="5b523-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="5b523-388">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="5b523-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="5b523-389">Während die neue Auftragsposition weiterhin im Inforegister **Auftragspositionen** ausgewählt ist, wählen Sie im Menü **Bestand** über dem Raster **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5b523-390">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5b523-391">Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5b523-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5b523-392">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5b523-393">Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5b523-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5b523-394">Notieren Sie sich die Wellen-ID- und Lieferungs-ID-Nummern.</span><span class="sxs-lookup"><span data-stu-id="5b523-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="5b523-395">Auftrag 2</span><span class="sxs-lookup"><span data-stu-id="5b523-395">Sales order 2</span></span>

1. <span data-ttu-id="5b523-396">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="5b523-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5b523-397">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5b523-398">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5b523-399">**Debitorenkonto:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="5b523-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="5b523-400">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b523-401">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5b523-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5b523-402">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5b523-402">The new sales order is opened.</span></span> <span data-ttu-id="5b523-403">Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten.</span><span class="sxs-lookup"><span data-stu-id="5b523-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5b523-404">Stellen Sie die folgenden Werte für diese Bestellposition ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="5b523-405">**Artikel:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b523-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="5b523-406">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5b523-407">Im Inforegister **Zeilendetails** auf der Registerkarte **Lieferung** legen Sie das Feld **Lieferart** auf *Flowe-STD* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="5b523-408">Legen Sie im Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus und stellen Sie dann die folgenden Werte auf die zweite Auftragsposition ein:</span><span class="sxs-lookup"><span data-stu-id="5b523-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="5b523-409">**Artikel:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5b523-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="5b523-410">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5b523-411">Im Inforegister **Zeilendetails** auf der Registerkarte **Lieferung** ändern Sie den Wert des Felds **Lieferart** auf *Air C-Air* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="5b523-412">Wählen Sie im Inforegister **Auftragspositionen** die erste Auftragsposition aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="5b523-413">Wählen Siedann im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5b523-414">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5b523-415">Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5b523-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5b523-416">Wählen Sie im Inforegister **Auftragspositionen** die zweite Auftragsposition aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="5b523-417">Wählen Siedann im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5b523-418">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5b523-419">Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5b523-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5b523-420">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5b523-421">Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5b523-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5b523-422">Beachten Sie, dass zwei Wellen-ID-Nummern und zwei Lieferungs-ID-Nummern erstellt wurden, eine für jede Lieferart für die Auftragspositionen.</span><span class="sxs-lookup"><span data-stu-id="5b523-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="5b523-423">Arbeits-IDs aus den Arbeitsdetails abrufen</span><span class="sxs-lookup"><span data-stu-id="5b523-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="5b523-424">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="5b523-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="5b523-425">Die Seite zeigt die Arbeits-IDs, die aus Aufträgen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5b523-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="5b523-426">Verwenden Sie die Wellen-IDs und Lieferungs-IDs aus den von Ihnen erstellten Aufträgen, um die Arbeits-ID für jede Welle und Lieferung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5b523-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="5b523-427">Notieren Sie sich diese Arbeits-IDs, da Sie sie in den nächsten Schritten benötigen.</span><span class="sxs-lookup"><span data-stu-id="5b523-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="5b523-428">Beachten Sie, dass für den zweiten Auftrag zwei Arbeits-IDs erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5b523-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="5b523-429">Wenn verschiedene Artikel an verschiedenen Orten entnommen werden, werden separate Wort-IDs generiert.</span><span class="sxs-lookup"><span data-stu-id="5b523-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="5b523-430">Artikel für die Aufträge entnehmen</span><span class="sxs-lookup"><span data-stu-id="5b523-430">Pick items for the sales orders</span></span>

<span data-ttu-id="5b523-431">Schließen Sie die erstellte Arbeit ab, indem Sie die Artikel mit dem mobilen Gerät zur Verpackungsstation verschieben.</span><span class="sxs-lookup"><span data-stu-id="5b523-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="5b523-432">Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).</span><span class="sxs-lookup"><span data-stu-id="5b523-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5b523-433">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="5b523-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5b523-434">Auf dem Menü **Ausgehend** wählen Sie **Verkaufsauswahl**.</span><span class="sxs-lookup"><span data-stu-id="5b523-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="5b523-435">Geben Sie im Feld **ID** die Arbeits-ID ein, die für den Auftrag 1 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="5b523-436">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-436">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-437">Geben Sie auf dieser Seite **Aufträge – Entnehmen** eine Ziel-LP ein, die für Auftrag 1 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="5b523-438">Beachten Sie, dass Entnahmeort (*Bulk-001*), Artikel (*A0001*) und Menge (*2 Stk*) gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5b523-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="5b523-439">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-439">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-440">Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**.</span><span class="sxs-lookup"><span data-stu-id="5b523-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="5b523-441">Das Feld **Loc** sollte anzeigen, dass die ausgewählten Artikel an den Ort *Verpackung* gehen.</span><span class="sxs-lookup"><span data-stu-id="5b523-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="5b523-442">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-442">Select **OK**.</span></span>

    <span data-ttu-id="5b523-443">Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“ message, die angibt, dass die Arbeits-ID aus Auftrag 1 abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="5b523-444">Sie wählen nun Auftrag 2.</span><span class="sxs-lookup"><span data-stu-id="5b523-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="5b523-445">Geben Sie im Feld **ID** die Arbeits-ID ein, die für den Auftrag 2 erstellt wurde, bei der Position 1 den Artikel *A0001* aufweist.</span><span class="sxs-lookup"><span data-stu-id="5b523-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="5b523-446">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-446">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-447">Geben Sie auf der Seite **Aufträge – Entnehmen** eine Ziel-LP ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="5b523-448">Beachten Sie, dass Entnahmeort (*Bulk-001*), Artikel (*A0001*) und Menge (*1 Stk*) gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5b523-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="5b523-449">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-449">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-450">Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**.</span><span class="sxs-lookup"><span data-stu-id="5b523-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="5b523-451">Das Feld **Loc** sollte anzeigen, dass die ausgewählten Artikel an den Ort *Verpackung* gehen.</span><span class="sxs-lookup"><span data-stu-id="5b523-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="5b523-452">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-452">Select **OK**.</span></span>

    <span data-ttu-id="5b523-453">Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="5b523-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5b523-454">Diese Nachricht zeigt an, dass die Arbeits-ID aus Position 1 von Auftrag 2 abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="5b523-455">Geben Sie im Feld **ID** die Arbeits-ID ein, die für den Auftrag 2 erstellt wurde, bei der Position 2 den Artikel *A0002* aufweist.</span><span class="sxs-lookup"><span data-stu-id="5b523-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="5b523-456">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-456">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-457">Geben Sie auf der Seite **Aufträge – Entnehmen** eine Ziel-LP ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="5b523-458">Beachten Sie, dass Entnahmeort (*Bulk-002*), Artikel (*A0001*) und Menge (*1 Stk*) gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5b523-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="5b523-459">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-459">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-460">Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**.</span><span class="sxs-lookup"><span data-stu-id="5b523-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="5b523-461">Das Feld **Loc** sollte anzeigen, dass die ausgewählten Artikel an den Ort *Verpackung* gehen.</span><span class="sxs-lookup"><span data-stu-id="5b523-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="5b523-462">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-462">Select **OK**.</span></span>

    <span data-ttu-id="5b523-463">Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="5b523-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5b523-464">Diese Nachricht zeigt an, dass die Arbeits-ID aus Position 2 von Auftrag 2 abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="5b523-465">Aufträge in Container verpacken</span><span class="sxs-lookup"><span data-stu-id="5b523-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="5b523-466">Auftrag 1 in Container verpacken</span><span class="sxs-lookup"><span data-stu-id="5b523-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="5b523-467">Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Verpackung**.</span><span class="sxs-lookup"><span data-stu-id="5b523-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="5b523-468">Das Dialogfeld **Verpackungsstation auswählen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b523-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="5b523-469">Standardmäßig sollte das Feld **Arbeitskraft** auf den Namen der Arbeitskraft gesetzt werden, die Sie zuvor eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="5b523-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="5b523-470">Legen Sie die folgenden Werte fest, um Lieferungen und Container anzuzeigen und zu bearbeiten, die am jeweiligen Verpackungsort geplant sind:</span><span class="sxs-lookup"><span data-stu-id="5b523-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="5b523-471">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="5b523-471">**Site:** *6*</span></span>
    - <span data-ttu-id="5b523-472">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b523-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5b523-473">**Lagerplatz:** *Verpackung*</span><span class="sxs-lookup"><span data-stu-id="5b523-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="5b523-474">**Verpackungsprofilkennung:** *Sortieren*</span><span class="sxs-lookup"><span data-stu-id="5b523-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="5b523-475">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5b523-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5b523-476">Geben Sie auf der Seite **Verpackung** im Feld **Kennzeichen oder Lieferung** die Ziel-LP für Auftrag 1 ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="5b523-477">Drücken Sie dann die Taste **Tab** oder **Eingabe** auf Ihrer Tastatur, um das Feld zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="5b523-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="5b523-478">Wählen Sie im Aktivitätsbereich **Neuer Container** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5b523-479">Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5b523-480">Notieren Sie die Container-ID.</span><span class="sxs-lookup"><span data-stu-id="5b523-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5b523-481">Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-482">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5b523-483">**Bezeichner:** Artikel *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b523-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="5b523-484">Wählen Sie im Aktivitätsbereich **Container schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5b523-485">Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b523-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5b523-486">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-486">Select **OK**.</span></span> <span data-ttu-id="5b523-487">Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="5b523-488">Erstellen Sie einen zweiten Container, um den zweiten Artikel aus der LP für Auftrag 1 einem neuen Container hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b523-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="5b523-489">Wählen Sie im Aktivitätsbereich **Neuer Container** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5b523-490">Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5b523-491">Notieren Sie die Container-ID.</span><span class="sxs-lookup"><span data-stu-id="5b523-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5b523-492">Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-493">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5b523-494">**Bezeichner:** Artikel *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b523-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="5b523-495">Wählen Sie im Aktivitätsbereich **Container schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5b523-496">Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b523-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5b523-497">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-497">Select **OK**.</span></span> <span data-ttu-id="5b523-498">Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="5b523-499">Auftrag 2 in Container verpacken</span><span class="sxs-lookup"><span data-stu-id="5b523-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="5b523-500">Geben Sie auf der Seite **Verpackung** im Feld **Kennzeichen oder Lieferung** die Ziel-LP für Position 1 von Auftrag 1 ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="5b523-501">Drücken Sie dann die Taste **Tab** oder **Eingabe** auf Ihrer Tastatur, um das Feld zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="5b523-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="5b523-502">Wählen Sie im Aktivitätsbereich **Neuer Container** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5b523-503">Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5b523-504">Notieren Sie die Container-ID.</span><span class="sxs-lookup"><span data-stu-id="5b523-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5b523-505">Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-506">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5b523-507">**Bezeichner:** Artikel *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b523-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="5b523-508">Wählen Sie im Aktivitätsbereich **Container schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5b523-509">Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b523-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5b523-510">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-510">Select **OK**.</span></span> <span data-ttu-id="5b523-511">Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="5b523-512">Geben Sie im Feld **Kennzeichen oder Lieferung** die Ziel-LP für Position 2 von Auftrag 2 ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="5b523-513">Drücken Sie dann die Taste **Tab** oder **Eingabe** auf Ihrer Tastatur, um das Feld zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="5b523-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="5b523-514">Wählen Sie im Aktivitätsbereich **Neuer Container** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5b523-515">Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5b523-516">Notieren Sie die Container-ID.</span><span class="sxs-lookup"><span data-stu-id="5b523-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5b523-517">Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5b523-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5b523-518">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="5b523-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5b523-519">**Bezeichnerfeld:** Artikel *A0002*</span><span class="sxs-lookup"><span data-stu-id="5b523-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="5b523-520">Wählen Sie im Aktivitätsbereich **Container schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5b523-521">Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b523-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5b523-522">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-522">Select **OK**.</span></span> <span data-ttu-id="5b523-523">Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.</span><span class="sxs-lookup"><span data-stu-id="5b523-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="5b523-524">Um die Containerdetails anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Container** und suchen Sie nach den Container-IDs, die beim Packen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5b523-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="5b523-525">Container sortieren</span><span class="sxs-lookup"><span data-stu-id="5b523-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b523-526">Wenn Sie auf der mobilen App auf die Menüoption **Palettenerstellung** für die Ausgangssortierung zugreifen, wird eine Schaltfläche mit der Bezeichnung **Voll** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b523-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="5b523-527">*Verwenden Sie die Schaltfläche **Voll** nicht zum Sortieren oder Schließen der Position.*</span><span class="sxs-lookup"><span data-stu-id="5b523-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="5b523-528">Die Schaltfläche **Voll** ist standardmäßig verfügbar und kann nicht deaktiviert oder von der Seite entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5b523-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="5b523-529">Sie wird nicht für die Funktion *Ausgangssortierung* verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b523-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="5b523-530">Sortieren des ersten Containers</span><span class="sxs-lookup"><span data-stu-id="5b523-530">Sort the first container</span></span>

1. <span data-ttu-id="5b523-531">Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).</span><span class="sxs-lookup"><span data-stu-id="5b523-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5b523-532">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="5b523-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5b523-533">Auf dem Menü **Ausgehend** wählen Sie **Palettenerstellung**.</span><span class="sxs-lookup"><span data-stu-id="5b523-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="5b523-534">Geben Sie im Feld **LP/Con** die erste Container-ID ein, die dem Auftrag 1 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5b523-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="5b523-535">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-535">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-536">Da derzeit keine Sortierpositionen vorhanden sind, müssen Sie eine angeben.</span><span class="sxs-lookup"><span data-stu-id="5b523-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="5b523-537">Geben Sie im Feld **Sortierposition-ID** *SP01* ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="5b523-538">Weil derzeit keine LP mit der Sortierposition *SP01* verknüpft ist, müssen Sie eine angeben.</span><span class="sxs-lookup"><span data-stu-id="5b523-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="5b523-539">Im Feld **LP** geben Sie *PLP01* ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="5b523-540">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-540">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-541">Da die Überprüfung der Sortierposition aktiviert ist, müssen Sie die ID der Sortierposition erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="5b523-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="5b523-542">Geben Sie im Feld **Sortierposition-ID** *SP01* ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="5b523-543">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-543">Select **OK**.</span></span>

    <span data-ttu-id="5b523-544">Sie erhalten die Nachricht „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="5b523-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="5b523-545">Um die Sortierposition und die darin enthaltene LP anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Zuweisungen von Ausgangssortierpositionen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="5b523-546">Die Seite **Zuweisungen von Ausgangssortierpositionen** zeigt alle aktuell aktiven Sortierpositionen an.</span><span class="sxs-lookup"><span data-stu-id="5b523-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="5b523-547">Das Feld **Sortierpositionstransaktionen** zeigt die LP, die jeder Sortierposition zugeordnet ist, und die Container, die sich an der Sortierposition befinden.</span><span class="sxs-lookup"><span data-stu-id="5b523-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="5b523-548">Beachten Sie, dass derzeit eine Sortierposition vorhanden ist und dass das Inforegister **Sortierpositionskriterien** ein Kriterium von **Lieferung – Spedition – Luft**.</span><span class="sxs-lookup"><span data-stu-id="5b523-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="5b523-549">Übrige Container sortieren</span><span class="sxs-lookup"><span data-stu-id="5b523-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="5b523-550">Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).</span><span class="sxs-lookup"><span data-stu-id="5b523-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5b523-551">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="5b523-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5b523-552">Auf dem Menü **Ausgehend** wählen Sie **Palettenerstellung**.</span><span class="sxs-lookup"><span data-stu-id="5b523-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="5b523-553">Geben Sie im Feld **LP/Con** die zweite Container-ID ein, die dem Auftrag 1 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5b523-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="5b523-554">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-554">Select **OK**.</span></span> <span data-ttu-id="5b523-555">Da die Sortiervorlage so eingerichtet ist, dass sie automatisch sortiert wird und bereits eine Sortierposition mit übereinstimmenden Kriterien vorhanden ist, werden Sie automatisch zur richtigen Sortierposition weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="5b523-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="5b523-556">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-556">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-557">Bestätigen Sie die ID der Sortierposition, um anzuzeigen, dass sich der Bestand an der richtigen Stelle befindet.</span><span class="sxs-lookup"><span data-stu-id="5b523-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="5b523-558">Geben Sie im Feld **Sortierposition-ID** *SP01* ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="5b523-559">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-559">Select **OK**.</span></span>

    <span data-ttu-id="5b523-560">Die Arbeiten am zweiten Container aus Auftrag 1 sind abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="5b523-561">Sie sortieren nun die verbleibenden Container aus Auftrag 2.</span><span class="sxs-lookup"><span data-stu-id="5b523-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="5b523-562">Geben Sie im Feld **LP/Con** die Container-ID des Containers aus Auftrag 2 ein, der den Artikel *A0001* enthält.</span><span class="sxs-lookup"><span data-stu-id="5b523-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="5b523-563">Da sich die Spedition unterscheidet, werden Sie aufgefordert, eine neue Sortierposition einzugeben und dieser Position eine LP zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5b523-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="5b523-564">Verwenden Sie Sortierposition *SP02* und LP *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="5b523-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="5b523-565">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-565">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-566">Bestätigen Sie die Sortierposition durch Eingabe von *SP02* im Feld **Sortierposition-ID**.</span><span class="sxs-lookup"><span data-stu-id="5b523-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="5b523-567">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-567">Select **OK**.</span></span>

    <span data-ttu-id="5b523-568">Die Arbeiten am Container sind abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="5b523-569">Geben Sie im Feld **LP/Con** die Container-ID für die übrigen Container aus Auftrag 2 ein, der den Artikel *A0002* enthält.</span><span class="sxs-lookup"><span data-stu-id="5b523-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="5b523-570">Da der Spediteurservice mit dem Spediteurservice für Auftrag 1 identisch ist, zeigt das System die vorhandene Sortierposition mit Übereinstimmungskriterien an.</span><span class="sxs-lookup"><span data-stu-id="5b523-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="5b523-571">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-571">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-572">Bestätigen Sie die Sortierposition durch Eingabe von *SP01* im Feld **Sortierposition-ID**.</span><span class="sxs-lookup"><span data-stu-id="5b523-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="5b523-573">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-573">Select **OK**.</span></span>

    <span data-ttu-id="5b523-574">Die Arbeiten am Container sind abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="5b523-575">Schließen Sie die ausgehenden Sortierpositionen</span><span class="sxs-lookup"><span data-stu-id="5b523-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="5b523-576">Wenn der gesamte Bestand sortiert wurde, muss die Position geschlossen werden, bevor Arbeiten erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="5b523-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="5b523-577">Es werden sortierte Bestandsentnahmen erstellt, um den Bestand zur Frachttür zu bringen.</span><span class="sxs-lookup"><span data-stu-id="5b523-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="5b523-578">Eine Position vom Mobilgerät aus schließen</span><span class="sxs-lookup"><span data-stu-id="5b523-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="5b523-579">Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).</span><span class="sxs-lookup"><span data-stu-id="5b523-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5b523-580">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="5b523-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5b523-581">Auf dem Menü **Ausgehend** wählen Sie **Palettenerstellung**.</span><span class="sxs-lookup"><span data-stu-id="5b523-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="5b523-582">Geben Sie im Feld **LP/Con** eine Container-ID ein, die nach Sortierposition *SP01* sortiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5b523-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="5b523-583">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-583">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-584">Sie erhalten folgende Meldung: „Der Container ist bereits auf Position SP01 sortiert.</span><span class="sxs-lookup"><span data-stu-id="5b523-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="5b523-585">Diese Position schließen?“</span><span class="sxs-lookup"><span data-stu-id="5b523-585">Close the position?"</span></span> <span data-ttu-id="5b523-586">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-586">Select **Close**.</span></span>

    <span data-ttu-id="5b523-587">Die Arbeit ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="5b523-588">Eine Position aus ausgehenden Sortierpositionszuweisungen schließen</span><span class="sxs-lookup"><span data-stu-id="5b523-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="5b523-589">Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Zuweisungen von Ausgangssortierpositionen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="5b523-590">Wählen Sie in der linken Spalte **SP02**.</span><span class="sxs-lookup"><span data-stu-id="5b523-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="5b523-591">Diese Zeile für die ausgehende Sortierposition wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="5b523-592">Wählen Sie im Aktivitätsbereich **Position schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b523-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="5b523-593">Der Sortierpositionsdatensatz ist geschlossen und wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b523-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="5b523-594">Um alle geschlossenen Positionsdatensätze anzuzeigen, wählen Sie das Kontrollkästchen **Geschlossene anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="5b523-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="5b523-595">Sortierte Bestandsentnahme</span><span class="sxs-lookup"><span data-stu-id="5b523-595">Sorted inventory picking</span></span>

<span data-ttu-id="5b523-596">Sie müssen die sortierte Bestandsauswahl durchführen.</span><span class="sxs-lookup"><span data-stu-id="5b523-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="5b523-597">Wenn es fertig ist, wird der Bestand in den Kundenauftrag aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="5b523-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="5b523-598">Zu diesem Zeitpunkt gelten alle anderen Lagerprozesse.</span><span class="sxs-lookup"><span data-stu-id="5b523-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="5b523-599">Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).</span><span class="sxs-lookup"><span data-stu-id="5b523-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5b523-600">Auf dem Hauptmenü wählen Sie **Ausgehend**.</span><span class="sxs-lookup"><span data-stu-id="5b523-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5b523-601">Wählen Sie im Menü **Ausgehend** **Aus Sortierung laden**.</span><span class="sxs-lookup"><span data-stu-id="5b523-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="5b523-602">Geben Sie die Ziel-LP-ID von der ersten Sortierposition *SP01* aus ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="5b523-603">Legen Sie das Feld **ID** auf *PLP01* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="5b523-604">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-604">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-605">Die Seite **Sortierte Bestandentnahme: Entnehmen** zeigt die Entnahmearbeit, die ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5b523-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="5b523-606">Wählen Sie aus dem Lagerplatz *SORT* und Ziel-LP *PLP01*, die mehrere Artikel und eine Menge von *3* hat.</span><span class="sxs-lookup"><span data-stu-id="5b523-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="5b523-607">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-607">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-608">Die Seite **Sortierte Bestandentnahme: Einlagern** zeigt die Einlagerunsarbeit, die ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5b523-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="5b523-609">Lagern Sie im Lagerplatz *Frachttür* und Ziel-LP *PLP01*, die mehrere Artikel und eine Menge von *3* hat.</span><span class="sxs-lookup"><span data-stu-id="5b523-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="5b523-610">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-610">Select **OK**.</span></span>

    <span data-ttu-id="5b523-611">Die Arbeit ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-611">Work is completed.</span></span>

1. <span data-ttu-id="5b523-612">Geben Sie das Zielkennzeichen von der zweiten Sortierposition *SP02* aus ein.</span><span class="sxs-lookup"><span data-stu-id="5b523-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="5b523-613">Legen Sie das Feld **ID** auf *PLP02* fest.</span><span class="sxs-lookup"><span data-stu-id="5b523-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="5b523-614">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-614">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-615">Die Seite **Sortierte Bestandentnahme: Entnehmen** zeigt die Entnahmearbeit, die ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5b523-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="5b523-616">Wählen Sie aus dem Lagerplatz *SORT* und Ziel-LP *PLP02*, die mehrere Artikel und eine Menge von *1* hat.</span><span class="sxs-lookup"><span data-stu-id="5b523-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="5b523-617">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-617">Select **OK**.</span></span>
1. <span data-ttu-id="5b523-618">Die Seite **Sortierte Bestandentnahme: Einlagern** zeigt die Einlagerunsarbeit, die ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5b523-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="5b523-619">Lagern Sie im Lagerplatz *Frachttür* und Ziel-LP *PLP02*, die mehrere Artikel und eine Menge von *1* hat.</span><span class="sxs-lookup"><span data-stu-id="5b523-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="5b523-620">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b523-620">Select **OK**.</span></span>

    <span data-ttu-id="5b523-621">Die Arbeit ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5b523-621">Work is completed.</span></span>

<span data-ttu-id="5b523-622">Ab diesem Zeitpunkt gelten alle anderen Lagerprozesse.</span><span class="sxs-lookup"><span data-stu-id="5b523-622">From this point forward, all other warehouse processes apply.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]