---
title: Wellenvorlagengruppierung
description: Die Gruppierung von Wellenvorlagen ermöglicht es dem System, mithilfe von Wellenvorlagen-Setups anhand der von Ihnen definierten Kriterien zu bestimmen, wie freigegebene Positionen aufgeteilt und neuen oder vorhandenen Wellen zugewiesen werden sollen. Diese Funktion kann in Lagerorten nützlich sein, in denen Wellen nach bestimmten Kriterien erstellt werden, Manager jedoch Wellen lieber automatisch als manuell erstellen.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9cbc0b6655de740628bcf3709d250ac02238038b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015825"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="3ec39-104">Wellenvorlagengruppierung</span><span class="sxs-lookup"><span data-stu-id="3ec39-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ec39-105">Die Gruppierung von Wellenvorlagen ermöglicht es dem System, mithilfe von [Wellenvorlagen](tasks/configure-wave-processing.md)-Setups anhand der von Ihnen definierten Kriterien zu bestimmen, wie freigegebene Positionen aufgeteilt und neuen oder vorhandenen Wellen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="3ec39-106">Diese Funktion kann in Lagerorten nützlich sein, in denen Wellen nach bestimmten Kriterien erstellt werden, Manager jedoch Wellen lieber automatisch als manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="3ec39-107">Es ermöglicht dem System, jede neu freigegebene Lieferung der ersten Welle hinzuzufügen, die übereinstimmende Gruppierungsfeldwerte aufweist.</span><span class="sxs-lookup"><span data-stu-id="3ec39-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="3ec39-108">Wird keine Übereinstimmung gefunden, erstellt das System eine neue Welle für die neue Lieferung.</span><span class="sxs-lookup"><span data-stu-id="3ec39-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ec39-109">Die Wellenvorlagengruppierung wird für die Arbeitstypen *Produktionsrohmaterialentnahme* oder *Kanban-Entnahme* nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ec39-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="3ec39-110">Dies liegt daran, dass die Wellengruppierung auf Lieferungen basiert und diese Arbeitstypen keine Lieferungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ec39-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="3ec39-111">Funktion für Wellenvorlagengruppierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="3ec39-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="3ec39-112">Bevor Sie die Funktion *Wellenvorlagengruppierung* verwenden können, muss sie in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3ec39-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="3ec39-113">Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3ec39-114">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3ec39-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3ec39-115">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="3ec39-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3ec39-116">**Funktionsname:** *Wellenvorlagengruppierung*</span><span class="sxs-lookup"><span data-stu-id="3ec39-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="3ec39-117">Wellenvorlage für Wellenvorlagengruppierung festlegen</span><span class="sxs-lookup"><span data-stu-id="3ec39-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="3ec39-118">Um die Wellenvorlagengruppierung verfügbar zu machen, führen Sie die folgenden Schritte aus, um die [Wellenvorlage](tasks/configure-wave-processing.md) einzurichten.</span><span class="sxs-lookup"><span data-stu-id="3ec39-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="3ec39-119">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="3ec39-120">Wählen Sie im linken Bereich die einzurichtende Wellenvorlage aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="3ec39-121">Wenn Sie sich darauf vorbereiten, das Szenario später in diesem Thema mithilfe von Demodaten zu bearbeiten, wählen Sie die Vorlage **62 Versandstandard** aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="3ec39-122">Klicken Sie auf **Bearbeiten** , um die Seite in den Bearbeitungsmodus zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="3ec39-123">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3ec39-124">**Wellenerstellung automatisieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3ec39-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="3ec39-125">**Offenen Wellen zuweisen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3ec39-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="3ec39-126">**Welle bei Freigabe für Lagerort verarbeiten:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="3ec39-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="3ec39-127">Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um das Abfragedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="3ec39-128">Überprüfen Sie im Abfragedialogfeld auf der Registerkarte **Sortierung** die Sortierkriterien, und stellen Sie sicher, dass es eine Regel gibt, die das Feld enthält, mit dem Sie Ihre Wellen gruppieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3ec39-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="3ec39-129">Wenn Sie sich darauf vorbereiten, das Szenario mithilfe von Demodaten zu bearbeiten, fügen Sie eine Zeile mit den folgenden Werten hinzu:</span><span class="sxs-lookup"><span data-stu-id="3ec39-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="3ec39-130">**Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="3ec39-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="3ec39-131">**Abgeleitete Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="3ec39-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="3ec39-132">**Feld:** *Spediteur*</span><span class="sxs-lookup"><span data-stu-id="3ec39-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="3ec39-133">Nachdem Sie diesen Wert ausgewählt haben, wird möglicherweise die folgende Meldung angezeigt: „Das Spediteur-Feld ist kein Indexfeld.</span><span class="sxs-lookup"><span data-stu-id="3ec39-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="3ec39-134">Möchten Sie eine Sortierung hinzufügen?“</span><span class="sxs-lookup"><span data-stu-id="3ec39-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="3ec39-135">Wählen Sie **Ja** aus, um eine Sortierung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="3ec39-136">**Suchrichtung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="3ec39-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="3ec39-137">Wählen Sie **OK** aus, um Ihre Änderungen zu speichern und das Abfragedialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="3ec39-138">Wählen Sie im Aktivitätsbereich **Wellenvorlagengruppierung** aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="3ec39-139">Aktivieren Sie auf der Seite **Wellenvorlagengruppierung** das Kontrollkästchen **Gruppieren nach** für jede Zeile, mit der Sie Ihre Bestellpositionen nach Bedarf in Wellen gruppieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3ec39-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="3ec39-140">Wenn Sie sich darauf vorbereiten, das Szenario mithilfe von Demodaten zu bearbeiten, aktivieren Sie das Kontrollkästchen **Gruppieren nach** für die Zeile *Spediteur*.</span><span class="sxs-lookup"><span data-stu-id="3ec39-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="3ec39-141">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-141">Select **Save**.</span></span>
1. <span data-ttu-id="3ec39-142">Schließen Sie die Seite **Wellenvorlagengruppierung**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="3ec39-143">Wählen Sie **Speichern** aus, um die Vorlage zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3ec39-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="3ec39-144">Szenario</span><span class="sxs-lookup"><span data-stu-id="3ec39-144">Scenario</span></span>

<span data-ttu-id="3ec39-145">Dieser Abschnitt enthält ein Skript, mit dem Sie lernen können, was diese Funktion tut und wie Sie damit arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3ec39-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="3ec39-146">Beispieldaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="3ec39-146">Make sample data available</span></span>

<span data-ttu-id="3ec39-147">Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="3ec39-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="3ec39-148">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="3ec39-149">Sie können dieses Szenario auch als Anleitung zur Verwendung dieser Funktion nutzen, wenn Sie an einem Produktionssystem arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3ec39-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="3ec39-150">In diesem Fall müssen Sie jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3ec39-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="3ec39-151">Szenario: Wellenvorlagengruppierung</span><span class="sxs-lookup"><span data-stu-id="3ec39-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="3ec39-152">Dieses Szenario zeigt, wie mithilfe der Wellenvorlagengruppierung automatisch mehrere Wellen erstellt werden, basierend auf Gruppierungskriterien, die in einer Wellenvorlage definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3ec39-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="3ec39-153">In diesem Szenario wird die Wellenvorlage im System so eingerichtet, dass eine Welle pro Spediteur erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3ec39-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="3ec39-154">Bevor Sie beginnen, bereiten Sie Ihre Wellenvorlage wie im Abschnitt [Wellenvorlage für Wellenvorlagengruppierung festlegen](#set-up-template) weiter oben in diesem Thema beschrieben vor.</span><span class="sxs-lookup"><span data-stu-id="3ec39-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="3ec39-155">Wenn Sie für dieses Szenario mit Demodaten arbeiten, müssen Sie die in diesem Verfahren vorgeschlagenen Demodatenwerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ec39-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="3ec39-156">Dieses Setup gruppiert Ihre Wellen nach dem Spediteur, der für jeden Auftrag festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec39-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="3ec39-157">Auftrag 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="3ec39-157">Create sales order 1</span></span>

1. <span data-ttu-id="3ec39-158">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3ec39-159">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3ec39-160">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3ec39-161">Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-004* fest.</span><span class="sxs-lookup"><span data-stu-id="3ec39-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="3ec39-162">Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.</span><span class="sxs-lookup"><span data-stu-id="3ec39-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="3ec39-163">Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="3ec39-164">Der neue Auftrag wird in der Ansicht **Positionen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3ec39-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="3ec39-165">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="3ec39-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="3ec39-166">Wechseln Sie zur Ansicht **Kopfzeile**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3ec39-167">Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3ec39-168">**Spediteur:** *Luftfracht*</span><span class="sxs-lookup"><span data-stu-id="3ec39-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="3ec39-169">**Spediteur:** *Air*</span><span class="sxs-lookup"><span data-stu-id="3ec39-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="3ec39-170">Wechseln Sie zurück zur Ansicht **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="3ec39-171">Klicken Sie im Abschnitt **Auftragspositionen** auf **Position hinzufügen** , um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="3ec39-172">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3ec39-173">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="3ec39-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="3ec39-174">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="3ec39-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="3ec39-175">Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3ec39-176">Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3ec39-177">Schließen Sie die Seite **Reservierung** , um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3ec39-178">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** , in der Gruppe **Aktivitäten** , **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3ec39-179">Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3ec39-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3ec39-180">Notieren Sie sich die Wellen-ID-Nummer und die Lieferungs-ID-Nummern.</span><span class="sxs-lookup"><span data-stu-id="3ec39-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="3ec39-181">Welle anzeigen, die aus Auftrag 1 erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="3ec39-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="3ec39-182">Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3ec39-183">Wählen Sie die Wellen-ID aus, die aus dem Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec39-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="3ec39-184">Wählen Sie den Wellen-ID-Link aus, um die Wellendetailseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="3ec39-185">Beachten Sie, dass die Lieferung zum Inforegister **Wellenpositionen** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec39-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="3ec39-186">Auftrag 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="3ec39-186">Create sales order 2</span></span>

1. <span data-ttu-id="3ec39-187">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3ec39-188">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3ec39-189">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3ec39-190">Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-005* fest.</span><span class="sxs-lookup"><span data-stu-id="3ec39-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="3ec39-191">Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.</span><span class="sxs-lookup"><span data-stu-id="3ec39-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="3ec39-192">Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="3ec39-193">Der neue Auftrag wird in der Ansicht **Positionen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3ec39-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="3ec39-194">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="3ec39-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="3ec39-195">Wechseln Sie zur Ansicht **Kopfzeile**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3ec39-196">Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3ec39-197">**Spediteur:** *Blume bewegt sich*</span><span class="sxs-lookup"><span data-stu-id="3ec39-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="3ec39-198">**Spediteur:** *STD*</span><span class="sxs-lookup"><span data-stu-id="3ec39-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="3ec39-199">Wechseln Sie zurück zur Ansicht **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="3ec39-200">Klicken Sie im Abschnitt **Auftragspositionen** auf **Position hinzufügen** , um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="3ec39-201">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3ec39-202">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="3ec39-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3ec39-203">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="3ec39-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="3ec39-204">Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3ec39-205">Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3ec39-206">Schließen Sie die Seite **Reservierung** , um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3ec39-207">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** , in der Gruppe **Aktivitäten** , **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3ec39-208">Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3ec39-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3ec39-209">Notieren Sie sich die Wellen-ID-Nummer und die Lieferungs-ID-Nummern.</span><span class="sxs-lookup"><span data-stu-id="3ec39-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="3ec39-210">Beachten Sie, dass sich die Wellen-ID von der Wellen-ID des ersten Auftrags unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="3ec39-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="3ec39-211">Welle anzeigen, die aus Auftrag 2 erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="3ec39-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="3ec39-212">Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3ec39-213">Wählen Sie die Wellen-ID aus, die aus dem zweiten Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec39-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="3ec39-214">Wählen Sie den Wellen-ID-Link aus, um die Wellendetailseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="3ec39-215">Beachten Sie, dass die Lieferung zum Inforegister **Wellenpositionen** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec39-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="3ec39-216">Für diese Lieferung wurde eine neue Welle erstellt, da sie einen anderen Spediteur als der erste Auftrag verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ec39-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="3ec39-217">Auftrag 3 erstellen</span><span class="sxs-lookup"><span data-stu-id="3ec39-217">Create sales order 3</span></span>

1. <span data-ttu-id="3ec39-218">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3ec39-219">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3ec39-220">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3ec39-221">Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-006* fest.</span><span class="sxs-lookup"><span data-stu-id="3ec39-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="3ec39-222">Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.</span><span class="sxs-lookup"><span data-stu-id="3ec39-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="3ec39-223">Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="3ec39-224">Der neue Auftrag wird in der Ansicht **Positionen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3ec39-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="3ec39-225">Notieren Sie sich die Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="3ec39-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="3ec39-226">Wechseln Sie zur Ansicht **Kopfzeile**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3ec39-227">Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3ec39-228">**Spediteur:** *Luftfracht*</span><span class="sxs-lookup"><span data-stu-id="3ec39-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="3ec39-229">**Spediteur:** *Air*</span><span class="sxs-lookup"><span data-stu-id="3ec39-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="3ec39-230">Wechseln Sie zurück zur Ansicht **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="3ec39-231">Klicken Sie im Abschnitt **Auftragspositionen** auf **Position hinzufügen** , um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="3ec39-232">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="3ec39-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3ec39-233">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="3ec39-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3ec39-234">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="3ec39-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="3ec39-235">Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3ec39-236">Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3ec39-237">Schließen Sie die Seite **Reservierung** , um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3ec39-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3ec39-238">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** , in der Gruppe **Aktivitäten** , **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="3ec39-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3ec39-239">Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3ec39-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3ec39-240">Notieren Sie sich die Wellen-ID-Nummer und die Lieferungs-ID-Nummern.</span><span class="sxs-lookup"><span data-stu-id="3ec39-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="3ec39-241">Die Lieferung wurde der bestehenden Welle aus dem ersten Auftrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3ec39-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="3ec39-242">Welle für Aufträge 1 und 3 anzeigen</span><span class="sxs-lookup"><span data-stu-id="3ec39-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="3ec39-243">Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.</span><span class="sxs-lookup"><span data-stu-id="3ec39-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3ec39-244">Wählen Sie die Wellen-ID aus, die aus dem dritten Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec39-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="3ec39-245">Wählen Sie den Wellen-ID-Link aus, um die Wellendetailseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ec39-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="3ec39-246">Beachten Sie, dass die Lieferung zum Inforegister **Wellenpositionen** hinzugefügt wurde, zusammen mit der Lieferung für den ersten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="3ec39-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
