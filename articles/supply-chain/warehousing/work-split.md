---
title: Arbeitsaufteilung
description: Dieses Thema enthält Informationen über die Arbeitsteilungsfunktionalität. Mit dieser Funktionalität können Sie große Arbeitsaufträge in mehrere kleinere Arbeitsaufträge aufteilen, die Sie dann mehreren Lagerkräften zuweisen können. Auf diese Weise kann die gleiche Arbeit von mehreren Arbeitskräften gleichzeitig entnommen werden.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8a530f3887c3c66295177d480a8c486dd0984153
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965526"
---
# <a name="work-split"></a><span data-ttu-id="d4964-105">Arbeitsaufteilung</span><span class="sxs-lookup"><span data-stu-id="d4964-105">Work split</span></span>

<span data-ttu-id="d4964-106">Mit der Arbeitsaufteilungsfunktion können Sie große Arbeitsaufträge (d.h. Arbeitsaufträge, die mehrere Zeilen haben) in mehrere kleinere Arbeitsaufträge aufteilen, die Sie dann mehreren Lagermitarbeitern zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="d4964-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="d4964-107">Auf diese Weise kann die gleiche Arbeitserstellungsnummer von mehreren Arbeitskräften gleichzeitig entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="d4964-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4964-108">Sie können nur Arbeitsaufträge aufteilen, die einen Status von *Offen* oder *In Bearbeitung* haben.</span><span class="sxs-lookup"><span data-stu-id="d4964-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="d4964-109">Einschalten der Arbeitsaufteilungsfunktionalität</span><span class="sxs-lookup"><span data-stu-id="d4964-109">Turn on the work split functionality</span></span>

<span data-ttu-id="d4964-110">Bevor Sie die Arbeitsteilungsfunktionalität verwenden können, müssen Sie die Funktion und ihre voraussetzende Funktion in Ihrem System einschalten.</span><span class="sxs-lookup"><span data-stu-id="d4964-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="d4964-111">Administratoren können die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktionen zu prüfen und sie bei Bedarf einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="d4964-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="d4964-112">Schalten Sie zuerst die vorausgesetzte *Organisationsweite Arbeitssperre* Funktion ein, wenn sie nicht bereits eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d4964-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="d4964-113">Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d4964-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="d4964-114">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="d4964-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d4964-115">**Funktionsname:** *Organisationsweite Arbeitssperre*</span><span class="sxs-lookup"><span data-stu-id="d4964-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="d4964-116">Wenn diese Funktion aktiviert ist, wird nach dem Einschalten der Funktion automatisch ein Daten-Upgrade für alle juristischen Entitäten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4964-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="d4964-117">Als nächstes schalten Sie die Funktion *Arbeitsteilung* ein, die wie folgt aufgelistet ist:</span><span class="sxs-lookup"><span data-stu-id="d4964-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="d4964-118">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="d4964-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d4964-119">**Funktionsname:** *Arbeitsteilung*</span><span class="sxs-lookup"><span data-stu-id="d4964-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="d4964-120">Erweiterungen auf den Seiten Arbeitsdetails und Alle Arbeiten</span><span class="sxs-lookup"><span data-stu-id="d4964-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="d4964-121">Die Funktion *Arbeit teilen* fügt dem Reiter **Arbeit** im Aktivitätsbereich der Seiten **Arbeitsdetails** und **Alle Arbeiten** die folgenden beiden Schaltflächen hinzu:</span><span class="sxs-lookup"><span data-stu-id="d4964-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="d4964-122">**Arbeit aufteilen** - Die aktuelle Arbeits-ID in mehrere kleinere Arbeits-IDs aufteilen, die von separaten Arbeitskräften bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="d4964-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="d4964-123">**Arbeitsteilung abbrechen** - Bricht die Arbeitsteilung ab und stellt die Arbeit für die Verarbeitung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d4964-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="d4964-124">![Schaltflächen „Arbeit teilen“ und „Arbeitsteilung aufheben“](media/Work_split_buttons.png "Schaltflächen Arbeit teilen und Arbeitsteilung abbrechen")</span><span class="sxs-lookup"><span data-stu-id="d4964-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4964-125">Die Schaltfläche **Arbeitsteilung** ist nicht verfügbar, wenn eine der folgenden Bedingungen erfüllt ist:</span><span class="sxs-lookup"><span data-stu-id="d4964-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="d4964-126">Der Arbeitsstatus ist etwas anderes als *Offen* oder *In Bearbeitung*.</span><span class="sxs-lookup"><span data-stu-id="d4964-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="d4964-127">Eine Container-ID ist mit der Arbeits-ID verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d4964-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="d4964-128">(Ein Container kann nicht systematisch aufgeteilt werden, da dies physische Aktionen erfordert.)</span><span class="sxs-lookup"><span data-stu-id="d4964-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="d4964-129">Die Arbeit ist mit einem Cluster verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d4964-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="d4964-130">Der Typ des Arbeitsauftrags ist etwas anderes als einer der folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="d4964-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="d4964-131">Aufträge</span><span class="sxs-lookup"><span data-stu-id="d4964-131">Sales orders</span></span>
>    - <span data-ttu-id="d4964-132">Rohmaterialentnahme</span><span class="sxs-lookup"><span data-stu-id="d4964-132">Raw material picking</span></span>
>    - <span data-ttu-id="d4964-133">Umlagerungsproblem</span><span class="sxs-lookup"><span data-stu-id="d4964-133">Transfer issue</span></span>
>
> - <span data-ttu-id="d4964-134">Die Arbeit wird gerade von einem anderen Benutzer geteilt.</span><span class="sxs-lookup"><span data-stu-id="d4964-134">The work is currently being split by another user.</span></span> <span data-ttu-id="d4964-135">Wenn Sie versuchen, die Aufteilungsseite für Arbeiten zu öffnen, die bereits von einem anderen Benutzer aufgeteilt werden, erhalten Sie die folgende Fehlermeldung: „Die Arbeit mit der ID \#\#\#\# wird gerade geteilt.</span><span class="sxs-lookup"><span data-stu-id="d4964-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="d4964-136">Versuchen Sie es in ein paar Minuten erneut.</span><span class="sxs-lookup"><span data-stu-id="d4964-136">Retry in a few minutes.</span></span> <span data-ttu-id="d4964-137">Wenn Sie diese Meldung weiterhin erhalten, wenden Sie sich an einen Supervisor.“</span><span class="sxs-lookup"><span data-stu-id="d4964-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="d4964-138">Ein neuer Arbeitssperrungsgrund, *Arbeit teilen*, zeigt an, wenn die Arbeits-ID gerade geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="d4964-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="d4964-139">Er wird sowohl auf der Seite **Arbeit aufteilen** als auch in der Lagerort App angezeigt, wenn ein Benutzer versucht, die Arbeit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4964-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="d4964-140">Wenn Sperrgründe verwendet werden, wird der Name des Feldes **Blockierte Welle** von der Arbeits-ID in **Blockiert** geändert.</span><span class="sxs-lookup"><span data-stu-id="d4964-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="d4964-141">Initiieren einer Arbeitsteilung</span><span class="sxs-lookup"><span data-stu-id="d4964-141">Initiate a work split</span></span>

<span data-ttu-id="d4964-142">Die Funktion fügt eine neue Seite **Arbeit aufteilen** hinzu, mit der Benutzer Arbeitszeilen von der Arbeits-ID aus aufteilen können.</span><span class="sxs-lookup"><span data-stu-id="d4964-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="d4964-143">Wenn die Seite zum ersten Mal geöffnet wird, zeigt sie Zeilen an, die einen Arbeitsstatus von *Offen* haben und die für eine Aufteilung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d4964-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="d4964-144">Wählen Sie im Aktivitätsbereich **Arbeit aufteilen**, um die ausgewählte Arbeit zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4964-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="d4964-145">Gehen Sie folgendermaßen vor, um Arbeit zu teilen.</span><span class="sxs-lookup"><span data-stu-id="d4964-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="d4964-146">Öffnen Sie eine der folgenden Arbeitsseiten:</span><span class="sxs-lookup"><span data-stu-id="d4964-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="d4964-147">**Arbeitsdetails** (**Lagerortverwaltung \> Arbeit \> Arbeitsdetails**)</span><span class="sxs-lookup"><span data-stu-id="d4964-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="d4964-148">**Alle Arbeiten** (**Lagerortverwaltung \> Arbeit \> Alle Arbeiten**)</span><span class="sxs-lookup"><span data-stu-id="d4964-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="d4964-149">Wählen Sie im Raster eine Arbeits-ID aus, die aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4964-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="d4964-150">Das Feld **Arbeitsauftragstyp** muss auf einen der folgenden Werte festgelegt sein:</span><span class="sxs-lookup"><span data-stu-id="d4964-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="d4964-151">Aufträge</span><span class="sxs-lookup"><span data-stu-id="d4964-151">Sales orders</span></span>
    - <span data-ttu-id="d4964-152">Rohmaterialentnahme</span><span class="sxs-lookup"><span data-stu-id="d4964-152">Raw material picking</span></span>
    - <span data-ttu-id="d4964-153">Umlagerungsproblem</span><span class="sxs-lookup"><span data-stu-id="d4964-153">Transfer issue</span></span>

1. <span data-ttu-id="d4964-154">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Arbeit aufteilen**.</span><span class="sxs-lookup"><span data-stu-id="d4964-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="d4964-155">Die Seite **Arbeit teilen** erscheint und zeigt die Arbeitszeilen an, die offen sind und zum Teilen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d4964-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="d4964-156">Standardmäßig werden nur verfügbare Arbeitszeilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4964-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="d4964-157">Um alle Zeilen für die Arbeits-ID anzuzeigen (z. B. Zeilen, die eine Arbeitsart von *Einlagern* haben), aktivieren Sie das Kontrollkästchen **Alle Zeilen anzeigen** oberhalb des Rasters.</span><span class="sxs-lookup"><span data-stu-id="d4964-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="d4964-158">Die folgende Meldung wird angezeigt: „Benutzer können keine Zeilen der Arbeit bearbeiten, bis Sie die Aufteilung beenden und diese Seite schließen.“</span><span class="sxs-lookup"><span data-stu-id="d4964-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="d4964-159">Das Feld **Arbeitssperrgrund** für die aktuelle Arbeit wird auf *Arbeit teilen* festgelegt, und die Arbeit wird gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d4964-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="d4964-160">![Blockiergrund](media/Blocking_reason.png "Grund der Sperrung")</span><span class="sxs-lookup"><span data-stu-id="d4964-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="d4964-161">Wählen Sie die Zeilen aus, die aus der aktuellen Arbeits-ID entfernt und zu einer neuen Arbeits-ID hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4964-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="d4964-162">Folgende Ereignisse treten auf:</span><span class="sxs-lookup"><span data-stu-id="d4964-162">The following events occur:</span></span>

    - <span data-ttu-id="d4964-163">Wenn Sie die Arbeit teilen, werden die ausgewählte(n) Zeile(n) aus der ursprünglichen Arbeits-ID storniert und dann in eine neue Arbeits-ID kopiert.</span><span class="sxs-lookup"><span data-stu-id="d4964-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="d4964-164">Die vorhandene Struktur der Arbeitsvorlage und der Lagerplatz des Einlagerns (und auch zukünftiger Entnahme-/Einlagerungspaare) bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4964-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="d4964-165">Die Werte für die folgenden Felder der Arbeits-ID werden von der ursprünglichen Arbeit in die neue Arbeit kopiert:</span><span class="sxs-lookup"><span data-stu-id="d4964-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="d4964-166">Ladungskennung</span><span class="sxs-lookup"><span data-stu-id="d4964-166">Load ID</span></span>
        - <span data-ttu-id="d4964-167">Lieferungskennung</span><span class="sxs-lookup"><span data-stu-id="d4964-167">Shipment ID</span></span>
        - <span data-ttu-id="d4964-168">Arbeitsauftragstyp</span><span class="sxs-lookup"><span data-stu-id="d4964-168">Work order type</span></span>
        - <span data-ttu-id="d4964-169">Bestellnummer</span><span class="sxs-lookup"><span data-stu-id="d4964-169">Order number</span></span>
        - <span data-ttu-id="d4964-170">Standort</span><span class="sxs-lookup"><span data-stu-id="d4964-170">Site</span></span>
        - <span data-ttu-id="d4964-171">Lagerort</span><span class="sxs-lookup"><span data-stu-id="d4964-171">Warehouse</span></span>
        - <span data-ttu-id="d4964-172">Arbeitspriorität</span><span class="sxs-lookup"><span data-stu-id="d4964-172">Work priority</span></span>
        - <span data-ttu-id="d4964-173">Arbeitspoolkennung</span><span class="sxs-lookup"><span data-stu-id="d4964-173">Work pool ID</span></span>
        - <span data-ttu-id="d4964-174">Wellenkennung</span><span class="sxs-lookup"><span data-stu-id="d4964-174">Wave ID</span></span>
        - <span data-ttu-id="d4964-175">Arbeitserstellungsnummer</span><span class="sxs-lookup"><span data-stu-id="d4964-175">Work creation number</span></span>

    - <span data-ttu-id="d4964-176">Die folgenden Felder werden nicht in die neue Arbeits-ID kopiert:</span><span class="sxs-lookup"><span data-stu-id="d4964-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="d4964-177">**Arbeits-ID** - Eine neue Arbeits-ID wird aus der entsprechenden Sequenz der Nummer erzeugt.</span><span class="sxs-lookup"><span data-stu-id="d4964-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="d4964-178">**Arbeitsstatus** - Dieses Feld wird auf *Offen* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4964-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="d4964-179">**Gesperrt durch** - Dieses Feld ist zunächst auf leer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4964-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="d4964-180">**Ziel-Ladungsträger-ID** - Dieses Feld wird leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="d4964-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="d4964-181">**Erstelldatum und -uhrzeit** - Dieses Feld ist auf das aktuelle Datum und die aktuelle Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4964-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="d4964-182">**Blockierte Welle/eingefroren** - Dieses Feld wird für die ursprüngliche Arbeits-ID und die neue Arbeits-ID neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="d4964-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="d4964-183">Wählen Sie im Aktivitätsbereich **Arbeit aufteilen**.</span><span class="sxs-lookup"><span data-stu-id="d4964-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="d4964-184">Während die Arbeit geteilt wird, wird die folgende Meldung angezeigt: „Bearbeitungsvorgang - Arbeit teilen“.</span><span class="sxs-lookup"><span data-stu-id="d4964-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="d4964-185">Während diese Meldung sichtbar ist, können Sie den Vorgang abbrechen, indem Sie **Abbrechen** im Meldungsfeld wählen.</span><span class="sxs-lookup"><span data-stu-id="d4964-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="d4964-186">Wenn das Kontrollkästchen **Alle Zeilen anzeigen** deaktiviert ist, wird die Zeile, die abgespalten und abgebrochen wurde, nicht mehr im Raster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4964-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="d4964-187">Wenn das Kontrollkästchen aktiviert ist, sollten Sie sehen, dass sich der Wert des Feldes **Arbeitsstatus** für diese Zeile auf *Abgebrochen* geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d4964-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="d4964-188">Die folgende Meldung wird angezeigt, um anzuzeigen, dass die neue Arbeits-ID erstellt worden ist: „Arbeit \#\#\#\# wurde durch Abspaltung von der ursprünglichen Arbeit \#\#\#\# erstellt.“</span><span class="sxs-lookup"><span data-stu-id="d4964-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="d4964-189">Andere Zeilen der ursprünglichen Arbeits-ID (z. B. *Put*-Zeilen) werden nach Bedarf angepasst, um die Zeilen der Arbeit widerzuspiegeln, die eingelagert wurden.</span><span class="sxs-lookup"><span data-stu-id="d4964-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="d4964-190">Wenn zum Beispiel die ursprüngliche Arbeits-ID eine *Put*-Zeile für eine Menge von 15 hatte und *Pick*-Zeilen, die eine Gesamtmenge von 10 haben, eingelegt wurden, wird die neue *Put*-Menge auf der ursprünglichen Arbeits-ID jetzt 5 sein.</span><span class="sxs-lookup"><span data-stu-id="d4964-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="d4964-191">Die neue Arbeit wird nicht sofort einem Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d4964-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="d4964-192">Sie können sie aber bei Bedarf jetzt einem Benutzer zuweisen, indem Sie die Standardfunktionalität der Seite **Arbeitsdetails** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4964-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4964-193">Sie können nur Arbeits-IDs aufteilen, die zwei oder mehr verfügbare Arbeitszeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4964-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="d4964-194">Wenn Sie **Arbeit aufteilen** wählen, wenn nur eine Arbeitszeile vorhanden ist, erhalten Sie die folgende Fehlermeldung: „Mindestens eine Arbeitszeile muss auf der ursprünglichen Arbeit verbleiben.“</span><span class="sxs-lookup"><span data-stu-id="d4964-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="d4964-195">In diesem Fall wird keine Aufteilung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d4964-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="d4964-196">Beenden einer Arbeitsteilung</span><span class="sxs-lookup"><span data-stu-id="d4964-196">Finish a work split</span></span>

<span data-ttu-id="d4964-197">Um die Arbeitsteilung zu beenden, muss der Sperrgrund *Arbeitsteilung* aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="d4964-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="d4964-198">Es gibt zwei Möglichkeiten, diesen Schritt abzuschließen:</span><span class="sxs-lookup"><span data-stu-id="d4964-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="d4964-199">Der Benutzer, der die Arbeit aufteilt, schließt die Seite **Arbeit aufteilen**, indem er die Schaltfläche **Schließen** (**X**) in der oberen rechten Ecke wählt.</span><span class="sxs-lookup"><span data-stu-id="d4964-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="d4964-200">Wenn die Seite geschlossen wird, wird der *Arbeit teilen*-Blockiergrund entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4964-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="d4964-201">Der *Blockiert* Status dieser Arbeit wird neu berechnet und, wenn es keine verbleibenden Blockiergründe für diese Arbeit gibt, wird die Arbeit entsperrt.</span><span class="sxs-lookup"><span data-stu-id="d4964-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="d4964-202">Ein beliebiger Benutzer öffnet die Arbeits-ID und wählt die Schaltfläche **Arbeitsteilung aufheben** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="d4964-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="d4964-203">Der *Arbeitsteilung*-Blockiergrund wird entfernt und der *Blockiert*-Status dieser Arbeit wird neu berechnet, genau wie beim Schließen der **Arbeitsteilung**-Seite.</span><span class="sxs-lookup"><span data-stu-id="d4964-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="d4964-204">Nachdem der *Arbeit teilen*-Blockierungsgrund entfernt wurde, kann die Arbeit auf dem mobilen Gerät ausgeführt werden, vorausgesetzt, der **Blockiert**-Status wird auf der Arbeits-ID auf *Nein* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4964-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="d4964-205">Benutzersperrung auf der Lagerort App</span><span class="sxs-lookup"><span data-stu-id="d4964-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="d4964-206">Wenn Sie versuchen, mit der Lagerort App Entnahmearbeiten gegen eine Arbeits-ID laufen zu lassen, die geteilt wird, erhalten Sie folgende Fehlermeldung: „Die Arbeit mit der ID \#\#\#\# wird gerade geteilt.“</span><span class="sxs-lookup"><span data-stu-id="d4964-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="d4964-207">Wenn Sie diese Meldung erhalten, wählen Sie **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="d4964-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="d4964-208">Sie können dann mit der Bearbeitung anderer Arbeiten fortfahren.</span><span class="sxs-lookup"><span data-stu-id="d4964-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="d4964-209">Andere gesperrte Operationen</span><span class="sxs-lookup"><span data-stu-id="d4964-209">Other blocked operations</span></span>

<span data-ttu-id="d4964-210">Alle Operationen, die Arbeitszeilen, Arbeitsbestands-Transaktionen oder Wiederbeschaffungs-Verknüpfungen ändern, die sich auf Arbeit beziehen, die gerade geteilt wird, schlagen fehl, und die folgende Fehlermeldung wird angezeigt: „Die Arbeit mit der ID \#\#\#\# wird gerade geteilt.“</span><span class="sxs-lookup"><span data-stu-id="d4964-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
