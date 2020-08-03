---
title: Arbeitspool für Arbeit ändern
description: In diesem Thema wird erläutert, wie Sie die Schaltfläche „Arbeitspool ändern“ für Arbeitsaufgaben verwenden können, um den Arbeitspool vorhandener Arbeit zu ändern.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33238b114f0939711163b19ae7af98be7c8d0744
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597540"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="1631f-103">Arbeitspool für Arbeit ändern</span><span class="sxs-lookup"><span data-stu-id="1631f-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1631f-104">Sie können Arbeitspools verwenden, um die Arbeit in Gruppen organisieren.</span><span class="sxs-lookup"><span data-stu-id="1631f-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="1631f-105">So können Sie beispielsweise einen Arbeitspool erstellen, um Arbeit zu klassifizieren, die an einem bestimmten Lagerort auftritt.</span><span class="sxs-lookup"><span data-stu-id="1631f-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="1631f-106">Die Funktion *Arbeitspool bei Arbeit ändern* fügt dem Aktionsbereich für Arbeitsaufgaben eine Schaltfläche **Arbeitspool ändern** hinzu.</span><span class="sxs-lookup"><span data-stu-id="1631f-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="1631f-107">Daher können Lagerverwalter den Arbeitspool vorhandener Arbeit problemlos ändern.</span><span class="sxs-lookup"><span data-stu-id="1631f-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="1631f-108">Mit dieser Funktion können Manager schnell auf Änderungen vor Ort im Lager reagieren und sie können sich leichter auf ändernde Situationen anpassen und Arbeit an einen anderen Arbeitspool übertragen.</span><span class="sxs-lookup"><span data-stu-id="1631f-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="1631f-109">Die Funktion „Arbeitspool bei Arbeit ändern“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="1631f-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="1631f-110">Bevor Sie mit der Einrichtung oder Verwendung dieser Funktion beginnen, müssen Sie sicherstellen, dass sie in Ihrem System verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1631f-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="1631f-111">Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1631f-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1631f-112">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="1631f-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1631f-113">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="1631f-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1631f-114">**Funktionsname:** *Arbeitspool bei Arbeit ändern*</span><span class="sxs-lookup"><span data-stu-id="1631f-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="1631f-115">Die Funktion „Arbeitspool bei Arbeit ändern“ einrichten</span><span class="sxs-lookup"><span data-stu-id="1631f-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="1631f-116">Um diese Funktion nutzen zu können, müssen einige Arbeitspools eingerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="1631f-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="1631f-117">Sie können Ihre Arbeitsvorlagen auch so einrichten, dass sie automatisch einen Pool zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1631f-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="1631f-118">Wenn Sie das weiter unten in diesem Thema enthaltene Beispielszenario durcharbeiten möchten, richten Sie Ihr System wie in diesem Abschnitt beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="1631f-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="1631f-119">Arbeitspools einrichten</span><span class="sxs-lookup"><span data-stu-id="1631f-119">Set up work pools</span></span>

<span data-ttu-id="1631f-120">Mit Arbeitspools können Sie Arbeitsaufgaben nach Typ organisieren.</span><span class="sxs-lookup"><span data-stu-id="1631f-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="1631f-121">Um mit der Funktion *Arbeitspool bei Arbeit ändern* zu arbeiten, müssen mindestens zwei Arbeitspools verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="1631f-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="1631f-122">Gehen Sie folgendermaßen vor, um Arbeitspools anzuzeigen und hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1631f-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="1631f-123">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitspools**.</span><span class="sxs-lookup"><span data-stu-id="1631f-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="1631f-124">Wenn Sie mit Demodaten aus dem Unternehmen **USMF** arbeiten und das Beispielszenario später in diesem Thema durcharbeiten werden, fügen Sie zwei Arbeitspools mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="1631f-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="1631f-125">Arbeitspool 1:</span><span class="sxs-lookup"><span data-stu-id="1631f-125">Work pool 1:</span></span>

        - <span data-ttu-id="1631f-126">**Arbeitspool-ID:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="1631f-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="1631f-127">**Beschreibung:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="1631f-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="1631f-128">Arbeitspool 2:</span><span class="sxs-lookup"><span data-stu-id="1631f-128">Work pool 2:</span></span>

        - <span data-ttu-id="1631f-129">**Arbeitspool-ID:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="1631f-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="1631f-130">**Beschreibung:** *Callcenter*</span><span class="sxs-lookup"><span data-stu-id="1631f-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="1631f-131">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="1631f-132">Arbeitsvorlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="1631f-132">Set up work templates</span></span>

<span data-ttu-id="1631f-133">Für jede Ihrer Arbeitsvorlagen können Sie nach Bedarf einen Standardarbeitspool festlegen.</span><span class="sxs-lookup"><span data-stu-id="1631f-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="1631f-134">Für jede relevante Vorlage weisen Sie in der Spalte **Arbeitspool-ID** einen Arbeitspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="1631f-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="1631f-135">In diesem Fall erben alle Arbeitsaufgaben, die mithilfe einer bestimmten Vorlage generiert werden, automatisch den zugewiesenen Arbeitspool.</span><span class="sxs-lookup"><span data-stu-id="1631f-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="1631f-136">Wenn Sie mit Demodaten aus dem Unternehmen **USMF** arbeiten und das Beispielszenario später in diesem Thema durcharbeiten werden, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="1631f-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="1631f-137">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="1631f-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1631f-138">Klicken Sie im Aktionsbereich auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="1631f-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="1631f-139">Bearbeiten Sie die Vorlage, indem Sie die folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="1631f-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="1631f-140">**Arbeitsvorlage:** *62 entnehmen für Paket*</span><span class="sxs-lookup"><span data-stu-id="1631f-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="1631f-141">**Arbeitspool-ID:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="1631f-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="1631f-142">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1631f-143">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="1631f-143">Example scenario</span></span>

<span data-ttu-id="1631f-144">Dieses Szenario zeigt, wie Sie den Stream der Verarbeitung für eine vorhandene Arbeitsaufgabe ändern, indem Sie dessen Arbeitspool ändern.</span><span class="sxs-lookup"><span data-stu-id="1631f-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="1631f-145">Es verwendet Demodaten aus dem Unternehmen **USMF** und die Einstellungen, die zuvor in diesem Thema vorgeschlagen wurden.</span><span class="sxs-lookup"><span data-stu-id="1631f-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="1631f-146">Einen Auftrag erstellen und ihn für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="1631f-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="1631f-147">Bestätigen Sie, dass genügend verfügbarer Lagerbestand für Artikel *A0001* und *A0002* im Lagerort *62* vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1631f-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="1631f-148">Gehen Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Bestandsliste** und bearbeiten Sie die Filter wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="1631f-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="1631f-149">Der Wert **Lagerort** beginnt mit *62*.</span><span class="sxs-lookup"><span data-stu-id="1631f-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="1631f-150">Der Wert **Artikelnummer** ist entweder *A001* oder *A002*.</span><span class="sxs-lookup"><span data-stu-id="1631f-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="1631f-151">Demodaten sollten jeweils eine Menge von 10 haben.</span><span class="sxs-lookup"><span data-stu-id="1631f-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="1631f-152">Als nächstes müssen Sie einen Auftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="1631f-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="1631f-153">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="1631f-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1631f-154">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1631f-155">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="1631f-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1631f-156">**Debitorenkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="1631f-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="1631f-157">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="1631f-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1631f-158">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1631f-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="1631f-159">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1631f-159">The new sales order is opened.</span></span> <span data-ttu-id="1631f-160">Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten.</span><span class="sxs-lookup"><span data-stu-id="1631f-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1631f-161">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="1631f-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="1631f-162">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="1631f-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1631f-163">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="1631f-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="1631f-164">Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="1631f-165">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="1631f-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1631f-166">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1631f-166">Close the page.</span></span>
1. <span data-ttu-id="1631f-167">Wählen Sie im Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus, um Ihrem Auftrag eine weitere Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1631f-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="1631f-168">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="1631f-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="1631f-169">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="1631f-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="1631f-170">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="1631f-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="1631f-171">Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="1631f-172">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="1631f-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1631f-173">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1631f-173">Close the page.</span></span>
1. <span data-ttu-id="1631f-174">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="1631f-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="1631f-175">Sie erhalten Informationsnachrichten mit der Wellen-ID und der Lieferungs-ID, die von der Freigabe erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1631f-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="1631f-176">Notieren Sie die Wellen-ID.</span><span class="sxs-lookup"><span data-stu-id="1631f-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="1631f-177">Die ausgehende Welle überprüfen</span><span class="sxs-lookup"><span data-stu-id="1631f-177">Review the outbound wave</span></span>

1. <span data-ttu-id="1631f-178">Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.</span><span class="sxs-lookup"><span data-stu-id="1631f-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="1631f-179">Suchen Sie im Raster nach der Wellen-ID, die von der Freigabe des Auftrags erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1631f-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="1631f-180">Wählen Sie die Wellen-ID aus, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1631f-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="1631f-181">Im Inforegister **Wellenpositionen** stellen Sie sicher, dass eine Lieferungs-ID für den Auftrag angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1631f-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="1631f-182">Wenn die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* in den Einstellungen für die Lieferungswellenvorlage festgelegt ist, müssen Sie die Welle manuell verarbeiten, indem Sie **Verarbeiten** aus der Registerkarte **Welle** im Aktionsbereich auswählen, um Arbeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1631f-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="1631f-183">Stellen Sie sicher, dass die Welle verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1631f-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="1631f-184">Diese Verarbeitung erstellt die erforderliche Arbeit.</span><span class="sxs-lookup"><span data-stu-id="1631f-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="1631f-185">Arbeitsdetails anzeigen und den Arbeitspool ändern</span><span class="sxs-lookup"><span data-stu-id="1631f-185">View work details and change the work pool</span></span>

<span data-ttu-id="1631f-186">Sie können die Seite **Arbeitsdetails** verwenden, um die erstellte Arbeit anzuzeigen und den Arbeitspool zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="1631f-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="1631f-187">Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="1631f-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="1631f-188">Wählen Sie die Zeile für die gerade erstellte Arbeit aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="1631f-189">Die Spalte **Auftragsnummer** zeigt die Auftragsnummer an.</span><span class="sxs-lookup"><span data-stu-id="1631f-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="1631f-190">Das Feld **Arbeitspool-ID** wird auf die Arbeitspool-ID festgelegt, die in der Arbeitsvorlage eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="1631f-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="1631f-191">Wenn Sie das Feld **Arbeitspool-ID** nicht sehen, fügen Sie die Spalte zum Raster hinzu und aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1631f-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="1631f-192">Um den Arbeitspool zu ändern, der der Arbeits-ID zugeordnet ist, wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Arbeitspool-ID** ändern aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="1631f-193">Im Dialogfeld **Arbeitspool ändern** im Inforegister **Parameter** im Feld **Arbeitspool-ID** wählen Sie *Callcenter* aus.</span><span class="sxs-lookup"><span data-stu-id="1631f-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="1631f-194">Wählen Sie **OK**, um Ihre Änderung zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="1631f-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="1631f-195">Beachten Sie, dass der Wert des Felds **Arbeitspool-ID** jetzt zu *Callcenter* geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1631f-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1631f-196">Wenn das Dialogfeld **Arbeitspool ändern** angezeigt wird, ist das Feld **Arbeitspool-ID** möglicherweise standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="1631f-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="1631f-197">Wenn das Feld leer ist, wenn Sie **OK** auswählen, um Änderungen zu übernehmen, entfernen Sie den Arbeitspool vollständig aus der Arbeit.</span><span class="sxs-lookup"><span data-stu-id="1631f-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="1631f-198">Zusätzlich zum Wechseln des Arbeitspools können Sie mit dieser Prozedur jeder Arbeitsaufgabe, die keinen hat, einen Arbeitspool hinzufügen oder einen Arbeitspool aus jeder Arbeitsaufgabe entfernen, die einen hat.</span><span class="sxs-lookup"><span data-stu-id="1631f-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
