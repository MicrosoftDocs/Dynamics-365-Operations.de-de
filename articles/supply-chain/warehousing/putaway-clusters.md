---
title: Clustereinlagerung
description: Einlagerungs-Cluster bieten eine Möglichkeit, mehrere Ladungsträger gleichzeitig zu entnehmen und diese dann an verschiedenen Lagerplätzen einzulagern. Sie können sehr nützlich für Einzelhandelsgeschäfte sein, bei denen Ladungsträger in der Regel keine vollen Paletten mit Bestand darstellen.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a330ddccbd17c92443232fc8488e36a59235773
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512329"
---
# <a name="putaway-clusters"></a><span data-ttu-id="cfe3d-104">Clustereinlagerung</span><span class="sxs-lookup"><span data-stu-id="cfe3d-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfe3d-105">Einlagerungs-Cluster bieten eine Möglichkeit, mehrere Ladungsträger gleichzeitig zu entnehmen und diese dann an verschiedenen Lagerplätzen einzulagern.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="cfe3d-106">Dieser Prozess wird oft als *Milchlauf* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="cfe3d-107">Clustereinlagerungen können sehr nützlich für Einzelhandelsgeschäfte sein, bei denen die Ladungsträger in der Regel keine vollen Paletten mit Bestand sind.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="cfe3d-108">Schalten Sie die Funktion Clustereinlagerung ein</span><span class="sxs-lookup"><span data-stu-id="cfe3d-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="cfe3d-109">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="cfe3d-110">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="cfe3d-111">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="cfe3d-112">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="cfe3d-113">**Funktionsname:** *Funktion Clustereinlagerung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="cfe3d-114">Einrichten für das Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="cfe3d-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="cfe3d-115">Clusterprofile</span><span class="sxs-lookup"><span data-stu-id="cfe3d-115">Cluster profiles</span></span>

<span data-ttu-id="cfe3d-116">Das Clustereinlagerungs-Profil bestimmt, wohin ein Element geht, basierend auf dem Lagerplatz, der dem Element zum Zeitpunkt des Eingangs zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="cfe3d-117">Wenn verschiedene Cluster benötigt werden, sollten verschiedene Clustereinlagerungen erstellt werden, eine für jeden Menüpunkt des mobilen Geräts.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="cfe3d-118">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Clusterprofile**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="cfe3d-119">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cfe3d-120">Legen Sie in der Ansicht **Kopfzeile** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="cfe3d-121">**Clustereinlagerungsprofil-ID:** *Clustereinlagerung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="cfe3d-122">**Name der Clustereinlagerungs-Profil-ID:** *Clustereinlagerung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="cfe3d-123">**Typ der Clustereinlagerung:** *Einlagerung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="cfe3d-124">**Sequenznummer:** Akzeptieren Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="cfe3d-125">Wählen Sie **Speichern**, um die erforderlichen Felder auf dem Inforegister **Allgemein** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="cfe3d-126">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="cfe3d-127">**Zeitpunkt der Cluster-Zuweisung:** *Beim Empfang*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="cfe3d-128">Dieses Feld legt fest, ob der eingelagerte Cluster sofort bei Eingang des Bestandes zugewiesen werden soll, oder ob er später sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="cfe3d-129">**Regel für Cluster-Zuweisung:** *Manuell*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="cfe3d-130">Dieses Feld legt fest, ob die Clusterzuordnung automatisch vom System oder manuell vom Benutzer bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="cfe3d-131">**Richtliniencode:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="cfe3d-132">**Clustereinlagerung lokalisieren:** *Empfang*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="cfe3d-133">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-133">The following values are available:</span></span>

        - <span data-ttu-id="cfe3d-134">**Empfang** - Ein Lagerplatz wird sofort beim Empfang gefunden.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="cfe3d-135">**Cluster schließen** - Ein Lagerplatz wird gefunden, wenn der Cluster geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="cfe3d-136">**Benutzergesteuert** - Ein Lagerplatz wird gefunden, wenn der Ladungsträger zum Einlagern aus dem Cluster entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="cfe3d-137">In diesem Fall wird kein Lagerplatz angegeben, wenn das Einlagerungswerk erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="cfe3d-138">Beim Einlagern selbst muss der Benutzer den Ladungsträger oder die Arbeits-ID scannen, um den Einlagerungsschritt zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="cfe3d-139">Das System findet dann den Lagerplatz wieder und sagt dem Benutzer, wo er die entnommene Menge einlagern soll.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="cfe3d-140">**Clustereinlagerung pro Benutzer:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="cfe3d-141">Dieses Feld legt fest, ob jeder Cluster pro Benutzer eindeutig sein soll, wenn Cluster automatisch zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="cfe3d-142">Es ist nur verfügbar, wenn das Feld **Cluster-Zuweisungsregel** auf *Automatisch* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="cfe3d-143">**Einheitsbeschränkung:** Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="cfe3d-144">Dieses Feld definiert die Einheit, die empfangen werden muss, damit das Profil gültig ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="cfe3d-145">Wenn es leer gelassen wird, sind alle Einheiten gültig.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="cfe3d-146">**Unterbrechung der Einheit:** *Einzelperson*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="cfe3d-147">Dieses Feld legt fest, ob beim Schließen eines Clusters der gesamte Bestand (unter Verwendung der Cluster-ID und des Kennzeichens) auf einen Ladungsträger konsolidiert werden soll und ob er als einzelner Ladungsträger oder getrennt auf den empfangenen Ladungsträgern eingelagert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="cfe3d-148">Dieses Feld ist nicht verfügbar, wenn das Feld **Clustereinlagerung einlagern** auf *Empfang* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="cfe3d-149">**Cluster bleibt als übergeordneter Ladungsträger bestehen:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="cfe3d-150">Wenn diese Option auf *Ja* festgelegt ist, wird die Cluster-ID nach dem Einlagern zu einem übergeordneten Ladungsträger, und alle Elemente auf der Cluster-ID werden mit diesem übergeordneten Ladungsträger verknüpft.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="cfe3d-151">Auf der Inforegister-Registerkarte **Clustereinlagerung** können Sie Kriterien für die Einlagerungssortierung definieren.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="cfe3d-152">Wählen Sie **Neu** in der Symbolleiste, um eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="cfe3d-153">**Sequenznummer:** Akzeptieren Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="cfe3d-154">**Feldname:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="cfe3d-155">Dieses Feld definiert das Feld, das diese Zeile als Sortierkriterium verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="cfe3d-156">**Sortierung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="cfe3d-157">Dieses Feld legt fest, ob die Sortierung in aufsteigender oder absteigender Reihenfolge erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="cfe3d-158">Wählen Sie auf dem Inforegister **Cluster-Arbeitsvorlage** die Option **Neu** in der Symbolleiste, um eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="cfe3d-159">**Arbeitsauftragstyp:** *Bestellungen*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="cfe3d-160">**Arbeitsvorlage:** *61 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="cfe3d-161">Wählen Sie im Aktivitätsbereich **Speichern** und wählen Sie dann **Abfrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="cfe3d-162">Wählen Sie im Dialogfeld **Clustereinlagerung** auf der Registerkarte **Bereich** die Option **Hinzufügen**, um der Abfrage eine zweite Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="cfe3d-163">Aktualisieren Sie dann die Zeilen der Abfrage wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="cfe3d-164">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cfe3d-164">Table</span></span> | <span data-ttu-id="cfe3d-165">Abgeleitete Tabelle</span><span class="sxs-lookup"><span data-stu-id="cfe3d-165">Derived table</span></span> | <span data-ttu-id="cfe3d-166">Feld</span><span class="sxs-lookup"><span data-stu-id="cfe3d-166">Field</span></span> | <span data-ttu-id="cfe3d-167">Kriterien</span><span class="sxs-lookup"><span data-stu-id="cfe3d-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="cfe3d-168">Arbeit</span><span class="sxs-lookup"><span data-stu-id="cfe3d-168">Work</span></span> | <span data-ttu-id="cfe3d-169">Arbeit</span><span class="sxs-lookup"><span data-stu-id="cfe3d-169">Work</span></span> | <span data-ttu-id="cfe3d-170">Lagerort</span><span class="sxs-lookup"><span data-stu-id="cfe3d-170">Warehouse</span></span> | <span data-ttu-id="cfe3d-171">*61*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-171">*61*</span></span> |
    | <span data-ttu-id="cfe3d-172">Arbeit</span><span class="sxs-lookup"><span data-stu-id="cfe3d-172">Work</span></span> | <span data-ttu-id="cfe3d-173">Arbeit</span><span class="sxs-lookup"><span data-stu-id="cfe3d-173">Work</span></span> | <span data-ttu-id="cfe3d-174">Arbeitskennung</span><span class="sxs-lookup"><span data-stu-id="cfe3d-174">Work ID</span></span> | <span data-ttu-id="cfe3d-175">Lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="cfe3d-176">Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="cfe3d-177">Wählen Sie im Aktivitätsbereich **Speichern**, und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfe3d-178">Felder im Clusterprofil, die abgeblendet erscheinen, wenn **Cluster-ID generieren** auf *Ja* festgelegt ist, sind nicht verfügbar und werden nicht berücksichtigt, wenn diese Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="cfe3d-179">Menüelemente des mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="cfe3d-179">Mobile device menu items</span></span>

<span data-ttu-id="cfe3d-180">Für diese Funktion sind zwei neue Menüelemente für mobile Geräte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="cfe3d-181">Der Menüpunkt **Cluster empfangen und sortieren** wird verwendet, um den empfangenen Bestand beim Empfang in ein Cluster für die Einlagerung zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="cfe3d-182">Der Menüpunkt **Clustereinlagerung** dient zum Einlagern des Clusters, nachdem er zugewiesen worden ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="cfe3d-183">Cluster empfangen und sortieren</span><span class="sxs-lookup"><span data-stu-id="cfe3d-183">Receive and sort cluster</span></span>

<span data-ttu-id="cfe3d-184">Erstellen Sie einen neuen Menüpunkt für mobile Geräte, um Bestände zu empfangen und in einen Cluster zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="cfe3d-185">Dieses Element erstellt einen Eingang nach dem Empfang von Bestand, was bedeutet, dass der Menüpunkt Empfangen für das Einlagern von Clustern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="cfe3d-186">Der Menüpunkt **Cluster empfangen und sortieren** kann mit den folgenden Empfangsmenüpunkten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="cfe3d-187">Bestellposition – Empfang</span><span class="sxs-lookup"><span data-stu-id="cfe3d-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="cfe3d-188">Bestellungsartikel – Empfang</span><span class="sxs-lookup"><span data-stu-id="cfe3d-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="cfe3d-189">Artikelempfang aus Ladung</span><span class="sxs-lookup"><span data-stu-id="cfe3d-189">Load item receiving</span></span>

1. <span data-ttu-id="cfe3d-190">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cfe3d-191">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cfe3d-192">Legen Sie in der Ansicht **Kopfzeile** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="cfe3d-193">**Name des Menüelements:** *Cluster empfangen und sortieren*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="cfe3d-194">**Titel:** *Clusters empfangen und sortieren*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="cfe3d-195">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="cfe3d-196">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="cfe3d-197">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="cfe3d-198">**Arbeitserstellungsprozess:** *Empfang von Elementen der Einkaufsbestellung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="cfe3d-199">**Kennzeichen generieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="cfe3d-200">**Clustereinlagerung zuweisen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="cfe3d-201">Die Option **Clustereinlagerung zuweisen** ist nur für die einstufige Aktivität *Arbeitserstellungsprozess* für den Empfang verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="cfe3d-202">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="cfe3d-203">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="cfe3d-204">Clustereinlagerung</span><span class="sxs-lookup"><span data-stu-id="cfe3d-204">Cluster putaway</span></span>

<span data-ttu-id="cfe3d-205">Erstellen Sie ein neues Menüelement für das Einlagern des Clusters, nachdem es zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="cfe3d-206">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cfe3d-207">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cfe3d-208">Legen Sie in der Ansicht **Kopfzeile** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="cfe3d-209">**Name des Menüelements:** *Clustereinlagerung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="cfe3d-210">**Titel:** *Clustereinlagerung*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="cfe3d-211">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="cfe3d-212">**Vorhandene Arbeit verwenden:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="cfe3d-213">Legen Sie im Inforegister **Allgemein** das Feld **Gerichtet durch** auf *Clustereinlagerung* fest.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="cfe3d-214">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="cfe3d-215">Legen Sie auf dem Inforegister **Arbeitsklassen** die gültige Arbeitsklasse für diesen Menüpunkt für mobile Geräte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="cfe3d-216">**Arbeitsklassen-ID:** *Kauf*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="cfe3d-217">**Arbeitsauftragstyp:** *Bestellungen*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="cfe3d-218">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="cfe3d-219">Menü für mobiles Gerät</span><span class="sxs-lookup"><span data-stu-id="cfe3d-219">Mobile device menu</span></span>

<span data-ttu-id="cfe3d-220">Fügen Sie die soeben erstellten Menüelemente in das Eingangsmenü der mobilen App ein.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="cfe3d-221">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="cfe3d-222">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="cfe3d-223">Wählen Sie in der Menüliste **Eingang**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="cfe3d-224">Suchen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den Eintrag **Cluster empfangen und sortieren** und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="cfe3d-225">Wählen Sie die rechte Pfeil-Schaltfläche, um das ausgewählte Element in die Liste **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="cfe3d-226">Verwenden Sie die Pfeil-nach-oben- oder Pfeil-nach-unten-Schaltfläche, um das Element an die gewünschte Position im Menü zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="cfe3d-227">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="cfe3d-228">Wiederholen Sie die Schritte 4 bis 7, um die restlichen Menüelemente hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="cfe3d-229">Cluster zuweisen</span><span class="sxs-lookup"><span data-stu-id="cfe3d-229">Assign cluster</span></span>
    - <span data-ttu-id="cfe3d-230">Clustereinlagerung</span><span class="sxs-lookup"><span data-stu-id="cfe3d-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="cfe3d-231">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="cfe3d-231">Example scenario</span></span>

<span data-ttu-id="cfe3d-232">Dieses Szenario simuliert die Clustereinlagerungs-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="cfe3d-233">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="cfe3d-233">Create a purchase order</span></span>

1. <span data-ttu-id="cfe3d-234">Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="cfe3d-235">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cfe3d-236">Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cfe3d-237">**Kreditorenkonto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="cfe3d-238">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="cfe3d-239">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-239">Select **OK**.</span></span>

    <span data-ttu-id="cfe3d-240">Die Seite **Alle Einkaufsbestellungen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="cfe3d-241">Fügen Sie auf der Seite **Alle Bestellungen** auf dem Inforegister **Bestellzeilen** mit der Schaltfläche **Zeile hinzufügen** die folgenden Zeilen hinzu:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="cfe3d-242">Einkaufsbestellung Zeile 1:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="cfe3d-243">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="cfe3d-244">**Menge** *10*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="cfe3d-245">Einkaufsbestellung Zeile 2:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="cfe3d-246">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="cfe3d-247">**Menge** *20*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="cfe3d-248">Einkaufsbestellung Zeile 3:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="cfe3d-249">**Artikelnummer:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="cfe3d-250">**Menge** *30*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="cfe3d-251">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="cfe3d-252">Notieren Sie sich die Bestellnummer.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="cfe3d-253">Bestand empfangen und auf dem mobilen Gerät einlagern</span><span class="sxs-lookup"><span data-stu-id="cfe3d-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="cfe3d-254">Bestand empfangen und in ein Cluster einsortieren</span><span class="sxs-lookup"><span data-stu-id="cfe3d-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="cfe3d-255">Melden Sie sich bei der Lagerort App als ein Benutzer an, der für Lagerort *61* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="cfe3d-256">Wählen Sie im Hauptmenü **Eingang**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="cfe3d-257">Wählen Sie im Menü **Eingang** die Option **Cluster empfangen und sortieren**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="cfe3d-258">Geben Sie im Feld **Ponum** die Nummer der Einkaufsbestellung ein.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="cfe3d-259">Wählen Sie **OK** (die Schaltfläche mit dem Häkchen).</span><span class="sxs-lookup"><span data-stu-id="cfe3d-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="cfe3d-260">Wählen Sie das Feld **Element**, geben Sie die Positionsnummer *A0001* ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="cfe3d-261">Wählen Sie das Feld **Anzahl**, geben Sie *10* mit Hilfe des Nummernblocks ein und wählen Sie dann die Schaltfläche mit dem Häkchen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="cfe3d-262">Auf der Aufgabenseite **Anzahl** wählen Sie **OK** (die Schaltfläche mit dem Häkchen), um die eingegebene Menge zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="cfe3d-263">Wählen Sie auf der Aufgabenseite **Element** **OK**, um zu bestätigen, dass das Element *A0001* eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="cfe3d-264">Wählen Sie das Feld **Cluster-ID** und geben Sie einen Wert ein, um eine ID für den Cluster zu vergeben, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="cfe3d-265">Die ID, die Sie hier eingeben, wird verwendet, wenn die beiden restlichen Elemente der Einkaufsbestellung eingehen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="cfe3d-266">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-266">Select **OK**.</span></span>

    <span data-ttu-id="cfe3d-267">Die Aufgabenseite **Ponum** erscheint und zeigt die Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="cfe3d-268">Element *A0001* ist nun auf dem Lagerplatz *RECV* eingegangen und der Cluster-ID zugeordnet, die Sie in Schritt 10 eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="cfe3d-269">Wiederholen Sie die Schritte 4 bis 11, um die restlichen zwei Elemente aus der Einkaufsbestellung zu empfangen und der Cluster-ID zuzuordnen:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="cfe3d-270">Eine Menge von *20* für Element *A0002*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="cfe3d-271">Eine Menge von *30* für das Element *M9215*</span><span class="sxs-lookup"><span data-stu-id="cfe3d-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="cfe3d-272">Schließen des Clusters</span><span class="sxs-lookup"><span data-stu-id="cfe3d-272">Close the cluster</span></span>

<span data-ttu-id="cfe3d-273">Bevor die Elemente des Clusters eingelagert werden können, muss der Cluster geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="cfe3d-274">Gehen Sie im Supply Chain Management auf **Lagerortverwaltung \> Arbeit \> Ausgang \> Arbeits-Cluster**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="cfe3d-275">Suchen Sie auf der Seite **Arbeitscluster** im Abschnitt **Arbeitscluster** im Feld **Cluster-ID** nach der Cluster-ID, die Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="cfe3d-276">Wenn der Cluster nicht angezeigt wird, wurde er möglicherweise bereits geschlossen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="cfe3d-277">Um festzustellen, ob der Cluster geschlossen wurde, aktivieren Sie das Kontrollkästchen **Geschlossene Arbeiten anzeigen** und suchen Sie nach der Cluster-ID, die Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="cfe3d-278">Folgen Sie dann diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="cfe3d-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="cfe3d-279">Wenn der Cluster geschlossen wurde, überspringen Sie die restlichen Schritte dieser Prozedur und fahren Sie mit der nächsten Prozedur fort, [Den Cluster einlagern](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="cfe3d-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="cfe3d-280">Wenn der Cluster nicht geschlossen wurde, folgen Sie den verbleibenden Schritten dieser Prozedur, um den Cluster manuell zu schließen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="cfe3d-281">Fahren Sie dann mit der nächsten Prozedur fort.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="cfe3d-282">Wählen Sie im Bereich **Arbeitscluster** die Cluster-ID, die Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="cfe3d-283">Wählen Sie im Aktivitätsbereich **Cluster schließen**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="cfe3d-284">Nachdem der Cluster geschlossen wurde, wird er nicht mehr im Bereich **Arbeitscluster** angezeigt (es sei denn, das Kontrollkästchen **Geschlossene Arbeit anzeigen** ist aktiviert).</span><span class="sxs-lookup"><span data-stu-id="cfe3d-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="cfe3d-285">Einlagern des Clusters</span><span class="sxs-lookup"><span data-stu-id="cfe3d-285">Put the cluster away</span></span>

1. <span data-ttu-id="cfe3d-286">Melden Sie sich bei der Lagerort App als ein Benutzer an, der für Lagerort *61* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="cfe3d-287">Wählen Sie im Hauptmenü **Eingang**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="cfe3d-288">Wählen Sie im Menü **Eingang** die Option **Clustereinlagerung**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="cfe3d-289">Wählen Sie **Cluster-ID**, und geben Sie die Cluster-ID ein, die Sie zuvor für den geschlossenen Cluster eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="cfe3d-290">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-290">Select **OK**.</span></span>

    <span data-ttu-id="cfe3d-291">Die Seite **Clustereinlagerung: Entnehmen** erscheint.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="cfe3d-292">Sie zeigt die Cluster-ID, den Lagerplatz, die Elemente (es wird der Wert *Mehrfach* angezeigt) und die Gesamtmenge im Cluster, die entnommen werden muss.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="cfe3d-293">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-293">Select **OK**.</span></span>

    <span data-ttu-id="cfe3d-294">Die Seite **Clustereinlagerung: Einlagern** erscheint.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="cfe3d-295">Die Anweisungen **Einlagern** identifizieren die Cluster-ID, den Lagerplatz, die Elemente, die Gesamtmenge und die Ladungsträger-IDs für die Elemente, die auf dem Cluster eingegangen sind.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="cfe3d-296">Sie haben die Standardoptionen, um diesen Schritt zu überschreiben oder zu übergehen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="cfe3d-297">![Clustereinlagerung: Seite einlagern](media/Cluster_putaway-Put.png "Clustereinlagerung: Seite einlagern")</span><span class="sxs-lookup"><span data-stu-id="cfe3d-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="cfe3d-298">Wählen Sie **OK**, um die Clustereinlagerung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="cfe3d-299">Es wird eine Meldung „Cluster abgeschlossen“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="cfe3d-300">Hinweise und Tipps</span><span class="sxs-lookup"><span data-stu-id="cfe3d-300">Notes and tips</span></span>

<span data-ttu-id="cfe3d-301">In Fällen, in denen die Cluster-ID zum übergeordneten Ladungsträger für eine verschachtelte Palette wird, wird die Einlagerungsposition automatisch angegeben, wenn die Cluster-ID gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="cfe3d-302">Es muss kein weiteres Ladungsträger-Kennzeichen gescannt werden, auch wenn die Kennzeichenerstellung auf manuell festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
