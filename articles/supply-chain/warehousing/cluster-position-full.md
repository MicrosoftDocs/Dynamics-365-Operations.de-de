---
title: Clusterposition voll
description: Dieses Thema enthält Informationen zur Funktion Clusterposition voll. Diese Funktion bietet eine Alternative zur strengeren Durchsetzung von Arbeitsunterbrechungsregeln, wenn die Clusterkommissionierung verwendet wird, da sie eine größere Fehlerquote bei den volumetrischen Einschränkungen von Containern oder Behältern ermöglicht.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3610725815b35609ee98b69b367db2945bbf166a
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016170"
---
# <a name="cluster-position-full"></a><span data-ttu-id="00bc8-104">Clusterposition voll</span><span class="sxs-lookup"><span data-stu-id="00bc8-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00bc8-105">Die Funktion *Clusterposition voll* bietet eine Alternative zur strengeren Durchsetzung von Arbeitsunterbrechungsregeln, wenn die Clusterkommissionierung verwendet wird, da sie eine größere Fehlerquote bei den volumetrischen Einschränkungen von Containern oder Behältern ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="00bc8-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="00bc8-106">In einem allgemeinen Szenario passen nicht alle Elemente eines Arbeitsauftrags in einen ausgewählten Container.</span><span class="sxs-lookup"><span data-stu-id="00bc8-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="00bc8-107">Lagerarbeiter, die Cluster auswählen, haben in diesem Szenario nur wenige Optionen: Sie müssen entweder zu einem größeren Container wechseln oder mit ihrem Vorgesetzten zusammenarbeiten, um eine andere Lösung zu finden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="00bc8-108">Diese Funktion bietet die Möglichkeit, die Schaltfläche **Voll** auf einer der Arbeitseinheiten in einem Cluster auszuführen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="00bc8-109">In älteren Versionen war diese Option nur für die reguläre Kommissionierung verfügbar, nicht für die Clusterkommissionierung.</span><span class="sxs-lookup"><span data-stu-id="00bc8-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="00bc8-110">Diese Funktion unterscheidet sich jedoch von der Standard **Voll** -Schaltfläche, da die verbleibende Arbeit abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="00bc8-111">Es wird nicht vorgeschlagen, dass der Benutzer dem gleichen Cluster ein weiteres Lagerfach hinzufügt, und es wird nicht automatisch eine neue Arbeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="00bc8-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="00bc8-112">Aktivieren der Funktion Clusterposition voll</span><span class="sxs-lookup"><span data-stu-id="00bc8-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="00bc8-113">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="00bc8-114">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="00bc8-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="00bc8-115">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="00bc8-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="00bc8-116">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="00bc8-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="00bc8-117">**Name der Funktion:** *Clusterposition voll*</span><span class="sxs-lookup"><span data-stu-id="00bc8-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="00bc8-118">Setup</span><span class="sxs-lookup"><span data-stu-id="00bc8-118">Setup</span></span>

<span data-ttu-id="00bc8-119">Dieser Abschnitt enthält Richtlinien und ein Beispiel, das zeigt, wie Sie die *Clusterposition voll* -Funktion einrichten und verwenden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="00bc8-120">Beispieldaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="00bc8-120">Make sample data available</span></span>

<span data-ttu-id="00bc8-121">Um das [Beispielszenario](#example-scenario) mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="00bc8-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="00bc8-122">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="00bc8-123">Sie können dieses Beispielszenario auch als Anleitung zur Arbeit Sie an einem Produktionssystem mit dieser Funktion nutzen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="00bc8-124">In diesem Fall müssen Sie jedoch für alle hier beschriebene Einstellungen Ihre eigenen Werte einsetzen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="00bc8-125">Clusterprofile</span><span class="sxs-lookup"><span data-stu-id="00bc8-125">Cluster profiles</span></span>

<span data-ttu-id="00bc8-126">Sie müssen angeben, ob Cluster-IDs automatisch generiert werden, wie viele Positionen verwendet werden, wann Cluster beschädigt werden und wie die Entnahmearbeit sequenziert und überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="00bc8-127">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Clusterprofile**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="00bc8-128">Wählen Sie im Listenbereich den Datensatz **Cluster erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="00bc8-129">Bestätigen Sie im Inforegister **Allgemein** die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="00bc8-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="00bc8-130">**Cluster-ID generieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00bc8-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="00bc8-131">**Positionen aktivieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00bc8-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="00bc8-132">**Anzahl der Positionen:** *2*</span><span class="sxs-lookup"><span data-stu-id="00bc8-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="00bc8-133">**Positionsname:** *Numerisch*</span><span class="sxs-lookup"><span data-stu-id="00bc8-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="00bc8-134">**Cluster unterbrechen bei:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="00bc8-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="00bc8-135">**Sortierbestätigungstyp:** *Positionsscan*</span><span class="sxs-lookup"><span data-stu-id="00bc8-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="00bc8-136">In dem **Clustersortierung** -Inforegister.</span><span class="sxs-lookup"><span data-stu-id="00bc8-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="00bc8-137">Das Raster sollte leer sein (d.h. es sollte keine Positionen enthalten).</span><span class="sxs-lookup"><span data-stu-id="00bc8-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="00bc8-138">Arbeitsvorlagen</span><span class="sxs-lookup"><span data-stu-id="00bc8-138">Work templates</span></span>

<span data-ttu-id="00bc8-139">Sie müssen definieren, wie die Entnahmearbeit für Clusterkommissionierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="00bc8-140">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="00bc8-141">Stellen Sie oben auf der Seite das Feld **Arbeitsauftragstyp** auf *Aufträge*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="00bc8-142">Stellen Sie sicher, dass die folgenden Arbeitsvorlagen aus den Demodaten aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="00bc8-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="00bc8-143">Wenn sie nicht verfügbar sind, können Sie das Szenario nicht abschließen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="00bc8-144">61 SO Phase</span><span class="sxs-lookup"><span data-stu-id="00bc8-144">61 SO Stage</span></span>
    - <span data-ttu-id="00bc8-145">61 SO Clusterkommissionierung</span><span class="sxs-lookup"><span data-stu-id="00bc8-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="00bc8-146">Lagerplatzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="00bc8-146">Location directives</span></span>

<span data-ttu-id="00bc8-147">Sie müssen angeben, woher die Artikel kommissioniert wurden und wo sie platziert werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="00bc8-148">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="00bc8-149">Legen Sie in der Kopfzeile der Liste das Feld **Arbeitsauftragstyp** auf *Aufträge* fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="00bc8-150">Stellen Sie sicher, dass die folgenden Auftragsrichtlinien aus den Demodaten aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="00bc8-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="00bc8-151">Wenn sie nicht verfügbar sind, können Sie das Szenario nicht abschließen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="00bc8-152">61 Clusterkommissionierung</span><span class="sxs-lookup"><span data-stu-id="00bc8-152">61 Cluster pick</span></span>
    - <span data-ttu-id="00bc8-153">61 Kommissionierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="00bc8-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="00bc8-154">Menüelemente des mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="00bc8-154">Mobile device menu items</span></span>

<span data-ttu-id="00bc8-155">Sie müssen eine Menüoption des Mobilgeräts konfigurieren, um vorhandene Arbeit zu verwenden, die durch Clusterkommissionierung geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="00bc8-156">Im Menüpunkt des Mobilgeräts für die Clusterkommissionierung muss der **Arbeitsteilung zulassen** -Parameter eingeschaltet sein, und die Arbeiterklasse *SO Kommissionierung* muss hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="00bc8-157">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="00bc8-158">Wählen Sie im Listenbereich den Datensatz **Clusterkommissionierung erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="00bc8-159">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="00bc8-160">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="00bc8-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00bc8-161">**Geleitet von:** *Clusterkommissionierung*</span><span class="sxs-lookup"><span data-stu-id="00bc8-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="00bc8-162">**Kennzeichen generieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00bc8-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="00bc8-163">**Aufteilung der Arbeit zulassen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00bc8-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="00bc8-164">**Clusterprofil-ID:** *Cluster erstellen*</span><span class="sxs-lookup"><span data-stu-id="00bc8-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="00bc8-165">Akzeptieren Sie die Standardwerte für alle anderen Felder.</span><span class="sxs-lookup"><span data-stu-id="00bc8-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="00bc8-166">Fügen Sie im Inforegister **Arbeiterklassen** nach Bedarf die folgenden zwei Zeilen hinzu:</span><span class="sxs-lookup"><span data-stu-id="00bc8-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="00bc8-167">Zeile 1 (normalerweise in Demodaten vorhanden):</span><span class="sxs-lookup"><span data-stu-id="00bc8-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="00bc8-168">**Arbeitsklassenkennung:** *Vertrieb*</span><span class="sxs-lookup"><span data-stu-id="00bc8-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="00bc8-169">**Arbeitsauftragsart:** *Kundenaufträge*</span><span class="sxs-lookup"><span data-stu-id="00bc8-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="00bc8-170">Zeile 2 (wahrscheinlich nicht in Demodaten vorhanden):</span><span class="sxs-lookup"><span data-stu-id="00bc8-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="00bc8-171">**Arbeitsklassen-ID:** *SO Kommissionierung*</span><span class="sxs-lookup"><span data-stu-id="00bc8-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="00bc8-172">**Arbeitsauftragsart:** *Kundenaufträge*</span><span class="sxs-lookup"><span data-stu-id="00bc8-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="00bc8-173">Wechseln Sie im Aktionsbereich zu **Einrichtung der Arbeitsbestätigung**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="00bc8-174">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-174">Select **Edit**.</span></span>
1. <span data-ttu-id="00bc8-175">Geben Sie auf der Position im Raster die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="00bc8-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="00bc8-176">**Arbeitstyp:** - *Kommissionnieren*</span><span class="sxs-lookup"><span data-stu-id="00bc8-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="00bc8-177">**Produktbestätigung** - *Aktivieren Sie das Kontrollkästchen*</span><span class="sxs-lookup"><span data-stu-id="00bc8-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="00bc8-178">Wählen im Aktionsbereich **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="00bc8-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="00bc8-179">Entnahmearbeit erstellen</span><span class="sxs-lookup"><span data-stu-id="00bc8-179">Create picking work</span></span>

<span data-ttu-id="00bc8-180">Bevor Sie mit der Clusterkommissionierung beginnen können, müssen Sie ausgehende Arbeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="00bc8-181">Das zuvor erstellte Clusterprofil gibt zwei Clusterpositionen an.</span><span class="sxs-lookup"><span data-stu-id="00bc8-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="00bc8-182">Daher müssen mindestens zwei Arbeits-IDs für die Auftragskommissionierung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="00bc8-183">In diesem Szenario werden Transaktionen im Lager *61* ausgeführt und sie werden die Artikel *L0101* und *T0100* verwenden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-183">For this scenario, transactions will occur in warehouse *61* , and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="00bc8-184">Die Demodaten sollten über einen ausreichenden Bestand dieser Artikel verfügen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="00bc8-185">Stellen Sie sicher, dass Sie über genügend Bestand verfügen, um die Transaktionen abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="00bc8-186">Auftrag 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="00bc8-186">Create sales order 1</span></span>

1. <span data-ttu-id="00bc8-187">Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="00bc8-188">Wählen Sie **Neu** aus, um Auftrag 1 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="00bc8-189">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="00bc8-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="00bc8-190">**Debitorenkonto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="00bc8-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="00bc8-191">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="00bc8-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="00bc8-192">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-192">Select **OK**.</span></span>
1. <span data-ttu-id="00bc8-193">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="00bc8-193">The new sales order is opened.</span></span> <span data-ttu-id="00bc8-194">Fügen Sie im Inforegister **Auftragspositionen** eine Position mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="00bc8-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="00bc8-195">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="00bc8-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="00bc8-196">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="00bc8-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="00bc8-197">Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="00bc8-198">Fügen Sie im Inforegister **Auftragspositionen** eine zweite Position mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="00bc8-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="00bc8-199">**Artikelnummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="00bc8-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="00bc8-200">**Menge** *20*</span><span class="sxs-lookup"><span data-stu-id="00bc8-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="00bc8-201">Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="00bc8-202">Führen Sie für jede gerade hinzugefügte Position die folgenden Schritte aus, um Bestand zu reservieren:</span><span class="sxs-lookup"><span data-stu-id="00bc8-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="00bc8-203">Wählen Sie die zu reservierende Position aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="00bc8-204">Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="00bc8-205">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="00bc8-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="00bc8-206">Schließen Sie die Seite **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="00bc8-207">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="00bc8-208">Wenn die Freigabe abgeschlossen ist, erhalten Sie Informationsnachrichten mit der Wellen- und Lade-ID, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="00bc8-209">Auftrag 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="00bc8-209">Create sales order 2</span></span>

1. <span data-ttu-id="00bc8-210">Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="00bc8-211">Wählen Sie **Neu** aus, um Auftrag 2 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="00bc8-212">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="00bc8-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="00bc8-213">**Debitorenkonto:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="00bc8-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="00bc8-214">**Lagerort:** *61*</span><span class="sxs-lookup"><span data-stu-id="00bc8-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="00bc8-215">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-215">Select **OK**.</span></span>
1. <span data-ttu-id="00bc8-216">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="00bc8-216">The new sales order is opened.</span></span> <span data-ttu-id="00bc8-217">Fügen Sie im Inforegister **Auftragspositionen** eine Position mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="00bc8-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="00bc8-218">**Artikelnummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="00bc8-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="00bc8-219">**Menge** *20*</span><span class="sxs-lookup"><span data-stu-id="00bc8-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="00bc8-220">Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="00bc8-221">Fügen Sie im Inforegister **Auftragspositionen** eine zweite Position mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="00bc8-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="00bc8-222">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="00bc8-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="00bc8-223">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="00bc8-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="00bc8-224">Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="00bc8-225">Führen Sie für jede gerade hinzugefügte Position die folgenden Schritte aus, um Bestand zu reservieren:</span><span class="sxs-lookup"><span data-stu-id="00bc8-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="00bc8-226">Wählen Sie die zu reservierende Position aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="00bc8-227">Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="00bc8-228">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="00bc8-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="00bc8-229">Schließen Sie die Seite **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="00bc8-230">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="00bc8-231">Wenn die Freigabe abgeschlossen ist, erhalten Sie Informationsnachrichten mit der Wellen- und Lade-ID, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="00bc8-232">Arbeits-IDs und Kennzeichennummern abrufen</span><span class="sxs-lookup"><span data-stu-id="00bc8-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="00bc8-233">Es sollten zwei Arbeits-IDs erstellt worden sein, von denen jede zwei Kommissionierungspositionen hat.</span><span class="sxs-lookup"><span data-stu-id="00bc8-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="00bc8-234">Befolgen Sie diese Schritte, um die Arbeits-IDs und Kennzeichenzuordnungen zu finden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="00bc8-235">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="00bc8-236">Suchen Sie in dem **Übersicht** -Raster die **Bestellnummer** -Spalte für die beiden Aufträge, die Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="00bc8-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="00bc8-237">Notieren Sie sich für jeden Auftrag die entsprechende Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="00bc8-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="00bc8-238">Wählen Sie die Zeile für jeden Auftrag aus, um relevante Informationen in **Positionen** -Raster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="00bc8-239">Notieren Sie sich den Ort, an dem jeder Artikel ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="00bc8-240">Wechseln Sie zu **Bestandsverwaltung \> Anfragen und Berichte \> Bestandsliste**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="00bc8-241">Wählen Sie im Aktivitätsbereich **Dimensionen** aus, um das Dialogfeld **Dimensionsanzeige** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="00bc8-242">Stellen Sie sicher, dass die Kontrollkästchen **Kennzeichen** , **Warenhaus** , und **Artikelnummer** aktiviert sind und wählen Sie anschließend **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-242">Make sure that the **License plate** , **Warehouse** , and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="00bc8-243">Legen Sie im **Filter** -Bereich folgende Filter fest:</span><span class="sxs-lookup"><span data-stu-id="00bc8-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="00bc8-244">**Artikelnummer** – **ist eine von** – *L0101* und *T100*</span><span class="sxs-lookup"><span data-stu-id="00bc8-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="00bc8-245">**Warenhaus** – **beginnt mit** – *61*</span><span class="sxs-lookup"><span data-stu-id="00bc8-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="00bc8-246">Notieren Sie sich die angezeigten Werte für **Kennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="00bc8-247">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="00bc8-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="00bc8-248">Flow-Ausführung für mobile Geräte – Einrichtung der Arbeitsbestätigung für das Produkt</span><span class="sxs-lookup"><span data-stu-id="00bc8-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="00bc8-249">Melden Sie sich bei der Warehouse-App als ein Benutzer im Lagerort *61* an.</span><span class="sxs-lookup"><span data-stu-id="00bc8-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="00bc8-250">Wechseln Sie zu **Ausgehend \> Clusterkommissionierung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="00bc8-251">Die **AUFGABE: Arbeit dem Cluster zuweisen** -Seite erscheint.</span><span class="sxs-lookup"><span data-stu-id="00bc8-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="00bc8-252">Geben Sie die Arbeits-ID für Auftrag 1 ein, um sie der Clusterposition 1 zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="00bc8-253">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-254">Geben Sie die Arbeits-ID für Auftrag 2 ein, um sie der Clusterposition 2 zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="00bc8-255">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="00bc8-256">Die **AUFGABE: Clusterkommissionierung erstellen: Kommissionieren** -Seite erscheint und zeigt *Artikel L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="00bc8-257">Da das Clusterprofil die Anzahl der Positionen auf 2 festgelegt hat, leitet das System Sie automatisch zur ersten konsolidierten Auswahl weiter: zwei Paletten (PL) des Artikels *L0101*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="00bc8-258">Während der folgenden Schritte können Sie jederzeit die **Details** -Registerkarte auswählen, um zusätzliche Informationen zur Aufgabe anzuzeigen, z. B. den Kommissionierungsort.</span><span class="sxs-lookup"><span data-stu-id="00bc8-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="00bc8-259">Legen Sie das Feld **ARTIKEL** auf *L0101* fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="00bc8-260">Dies bestätigt die Artikelnummer, die für diesen Menüpunkt erforderlich ist (Sie haben dies zuvor durch Auswahl von **Einrichtung der Arbeitsbestätigung** auf der Seite **Mobilgerät-Menüpunkt** konfiguriert, als Sie diesen Menüpunkt erstellt haben).</span><span class="sxs-lookup"><span data-stu-id="00bc8-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="00bc8-261">Geben Sie die Kennzeichennummer ein, die dem Artikel an dem Lagerplatz zugeordnet ist, an dem es ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="00bc8-262">Sie werden zwei Paletten kommissionieren.</span><span class="sxs-lookup"><span data-stu-id="00bc8-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="00bc8-263">Stellen Sie das **LP** -Feld auf *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="00bc8-264">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="00bc8-265">Die **AUFGABE: Sortieren: Clusterkommissionierung erstellen** -Seite erscheint.</span><span class="sxs-lookup"><span data-stu-id="00bc8-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="00bc8-266">Hier sortieren Sie die beiden kommissionierten Paletten in eine Kommissionierposition.</span><span class="sxs-lookup"><span data-stu-id="00bc8-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="00bc8-267">Diese Position kann ein Behälter oder ein Container sein, mit dem der kommissionierte Bestand nach Auftrag getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="00bc8-268">Zeigen Sie die Details an, die für den Artikel ( *L0101* ) und die Menge ( *20* ea), die in Position 1 sortiert wird (für Auftrag 1), angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-268">View the details that are shown for the item ( *L0101* ) and quantity ( *20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="00bc8-269">Stellen Sie das **POSITION NA** -Feld auf *1*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="00bc8-270">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-271">Zeigen Sie die Details an, die für den Artikel ( *L0101* ) und die Menge ( *20* ea), die in Position 2 sortiert wird (für Auftrag 2), angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-271">View the details that are shown for the item ( *L0101* ) and quantity ( *20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="00bc8-272">Stellen Sie das **POSITION NA** -Feld auf *2*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="00bc8-273">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="00bc8-274">Die **AUFGABE: Clusterkommissionierung erstellen: Kommissionieren** -Seite erscheint und zeigt *Artikel T0100 7 ea*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="00bc8-275">In diesem Szenario kann Position 1 nicht die gesamte Menge der Artikel akzeptieren, die zur Erfüllung des Auftrags 1 kommissioniert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="00bc8-276">Eine Position muss als voll markiert sein.</span><span class="sxs-lookup"><span data-stu-id="00bc8-276">A position must be marked as full.</span></span> <span data-ttu-id="00bc8-277">In diesem Szenario kommissionieren Sie den zweiten Artikel teilweise.</span><span class="sxs-lookup"><span data-stu-id="00bc8-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="00bc8-278">Der zweite Artikel wird für Position 1 teilweise kommissioniert, und es wird neue Arbeit erstellt, um die verbleibende Menge zu kommissionieren, um die Bestellung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="00bc8-279">Wählen Sie die Menütaste (manchmal auch als Hamburger oder Hamburgertaste bezeichnet) und dann **Position voll** aus.</span><span class="sxs-lookup"><span data-stu-id="00bc8-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="00bc8-280">Identifizieren Sie die Position, die voll ist, und wählen Sie *1*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="00bc8-281">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-282">Geben Sie die Kommissionierungsmenge ein, die noch in Position 1 kommissioniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="00bc8-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="00bc8-283">Das System kann bestimmen, welche Artikelnummer kommissioniert wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="00bc8-284">Geben Sie *2* ein.</span><span class="sxs-lookup"><span data-stu-id="00bc8-284">Enter *2*.</span></span>
1. <span data-ttu-id="00bc8-285">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-286">Bestätigen Sie die Artikelnummer, um die Auswahl des verbleibenden Artikels in Position 2 abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="00bc8-287">Legen Sie das Feld **ARTIKEL** auf *T0100* fest.</span><span class="sxs-lookup"><span data-stu-id="00bc8-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="00bc8-288">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-289">Geben Sie das Kennzeichen ein, von dem der Artikel kommissioniert wird, indem Sie das **LP** -Feld auf *LPREPL04* festlegen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="00bc8-290">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-291">Zeigen Sie die Details an, die für den Artikel ( *T0100* ) und die Menge ( *2* ea), die in Position 2 sortiert wird (für Auftrag 2), angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-291">View the details that are shown for the item ( *T0100* ) and quantity ( *2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="00bc8-292">Stellen Sie das **POSITION NA** -Feld auf *2*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="00bc8-293">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="00bc8-294">Zeigen Sie die Details an, die für den Artikel ( *T0100* ) und die Menge ( *2* ea), die in Position 1 sortiert wird (für Auftrag 1), angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00bc8-294">View the details that are shown for the item ( *T0100* ) and quantity ( *2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="00bc8-295">Stellen Sie das **POSITION NA** -Feld auf *1*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="00bc8-296">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="00bc8-297">Die **AUFGABE: Clusterkommissionierung: Einlagern** -Seite erscheint.</span><span class="sxs-lookup"><span data-stu-id="00bc8-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="00bc8-298">In diesem Szenario wurde die Clusterkommissionierung abgeschlossen, und der Benutzer wird angewiesen, die ausgewählten Elemente von Position 1 und Position 2 an den Staging-Lagerplatz zu verschieben *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="00bc8-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="00bc8-299">Prüfen Sie die Informationen auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="00bc8-299">Review the information on the page.</span></span> <span data-ttu-id="00bc8-300">Sie zeigt, dass eine Gesamtmenge von *44* an den Staging-Lagerplatz gebracht wird.</span><span class="sxs-lookup"><span data-stu-id="00bc8-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="00bc8-301">Wählen Sie **OK** (Häkchensymbol).</span><span class="sxs-lookup"><span data-stu-id="00bc8-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="00bc8-302">Sie erhalten die Nachricht „Cluster abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="00bc8-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="00bc8-303">Sie können jetzt den **Verkaufsauswahl** -Menüpunkt verwenden, um die verbleibende Menge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="00bc8-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="00bc8-304">Sie können dann das **Verkaufsverladung** -Menüelement verwenden, um Artikel vom Staging-Lagerplatz zum Verladedock zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="00bc8-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
