---
title: Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind
description: Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301304"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="4ecda-103">Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind</span><span class="sxs-lookup"><span data-stu-id="4ecda-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="4ecda-104">Fehlercode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="4ecda-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="4ecda-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="4ecda-105">Symptoms</span></span>

<span data-ttu-id="4ecda-106">Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="4ecda-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4ecda-107">Einige der Artikel, die für Ladung %1 benötigt werden, sind noch nicht entnommen und zum endgültigen Versandort verschoben worden.</span><span class="sxs-lookup"><span data-stu-id="4ecda-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="4ecda-108">Daher können Sie die Sendung für die Ladung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4ecda-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="4ecda-109">Cause</span></span>

<span data-ttu-id="4ecda-110">Die Ladung oder Sendung kann in ihrem aktuellen Status nicht bestätigt werden, weil eine der folgenden Bedingungen vorliegen könnte:</span><span class="sxs-lookup"><span data-stu-id="4ecda-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="4ecda-111">Die zugehörige Arbeit wurde noch nicht entnommen und an den endgültigen Versandort gebracht.</span><span class="sxs-lookup"><span data-stu-id="4ecda-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="4ecda-112">Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein.</span><span class="sxs-lookup"><span data-stu-id="4ecda-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="4ecda-113">Die Lagerplatzrichtlinie wurde mit dem Packplatz als endgültigem Versandort konfiguriert, während Sie die Wave-Template-Containerisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ecda-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="4ecda-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="4ecda-114">Resolution</span></span>

<span data-ttu-id="4ecda-115">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Versandbestätigung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="4ecda-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="4ecda-116">Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="4ecda-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="4ecda-117">Überprüfen Sie Ihre Ladungs-Zeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="4ecda-118">Stornieren Sie die Arbeits-IDs, die mit dem Verpackungsort als endgültigem Versandort erstellt wurden, konfigurieren Sie die Lagerplatzrichtlinie neu und geben Sie die Ladung erneut frei.</span><span class="sxs-lookup"><span data-stu-id="4ecda-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="4ecda-119">Überprüfen Sie die Zeilen Ihrer Ladung und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="4ecda-120">Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="4ecda-121">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4ecda-122">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ecda-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4ecda-123">Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.</span><span class="sxs-lookup"><span data-stu-id="4ecda-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="4ecda-124">Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="4ecda-125">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="4ecda-126">Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4ecda-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="4ecda-127">Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="4ecda-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="4ecda-128">Stornieren Sie die Arbeits-IDs, die mit dem Verpackungsort als endgültigem Versandort erstellt wurden, konfigurieren Sie die Lagerplatzrichtlinie neu und geben Sie die Ladung erneut frei</span><span class="sxs-lookup"><span data-stu-id="4ecda-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="4ecda-129">Gehen Sie wie folgt vor, um die Arbeits-IDs zu stornieren, die den Packort als endgültigen Lagerplatz mit automatischer Containerisierung haben.</span><span class="sxs-lookup"><span data-stu-id="4ecda-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="4ecda-130">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="4ecda-131">Der Dialog **Arbeit stornieren** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4ecda-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="4ecda-132">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="4ecda-133">Die ausgewählte Arbeits-ID muss einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* haben.</span><span class="sxs-lookup"><span data-stu-id="4ecda-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="4ecda-134">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4ecda-134">Select **OK**.</span></span>
1. <span data-ttu-id="4ecda-135">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="4ecda-136">Wiederholen Sie diesen Vorgang für die anderen Arbeits-IDs nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="4ecda-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="4ecda-137">Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="4ecda-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="4ecda-138">Gehen Sie wie folgt vor, um die Lagerplatzrichtlinie so umzukonfigurieren, dass sie nicht den Verpackungsplatz als endgültigen Versandort verwendet, wenn die automatische Containerisierung für die Wellenvorlage festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4ecda-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="4ecda-139">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4ecda-140">Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.</span><span class="sxs-lookup"><span data-stu-id="4ecda-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="4ecda-141">Wählen Sie die Lagerplatzrichtlinie aus, die Sie für die automatisierte Containerisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ecda-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="4ecda-142">Wählen Sie in der Symbolleiste **Aktionen der Lagerplatzrichtlinie** Inforegister **Abfrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="4ecda-143">Suchen Sie im Abfrage-Editor-Dialog auf der Registerkarte **Bereich** die Zeile, in der **Feld** auf *Lagerplatzprofil* festgelegt ist, und stellen Sie sicher, dass das Feld **Kriterien** für diese Zeile nicht auf ein Lagerplatzprofil festgelegt ist, das einen **Lagerplatztyp** von *Verpackung* hat.</span><span class="sxs-lookup"><span data-stu-id="4ecda-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="4ecda-144">Passen Sie das Feld **Kriterien** an, um den endgültigen PUT-Lagerplatz zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="4ecda-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="4ecda-145">Gehen Sie wie folgt vor, um die Ladung erneut freizugeben und Arbeits-IDs mit dem korrekten endgültigen Versandort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ecda-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="4ecda-146">Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="4ecda-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="4ecda-147">Suchen Sie im Bereich **Ladungen** die Ladung, die freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="4ecda-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="4ecda-148">Wählen Sie in der Symbolleiste des Bereichs **Ladungen** die Option **Freigeben \> Freigabe an Lagerort**, um die ausgewählte Ladung an den Lagerort freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4ecda-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="4ecda-149">Wiederholen Sie diesen Vorgang für die anderen Ladungen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="4ecda-149">Repeat this procedure for the other loads as needed.</span></span>
