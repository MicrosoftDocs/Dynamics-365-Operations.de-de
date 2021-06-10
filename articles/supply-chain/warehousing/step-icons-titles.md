---
title: Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu
description: In diesem Thema wird beschrieben, wie Sie Schrittsymbole und -titel für neue oder angepasste Aufgabenabläufe für die mobile Warehouse Management-App zuweisen.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049363"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="524d6-103">Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu</span><span class="sxs-lookup"><span data-stu-id="524d6-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="524d6-104">In diesem Thema wird beschrieben, wie Sie Schrittsymbole und Schritttitel für neue oder angepasste Aufgabenabläufe für die mobile Warehouse Management Mobile App zuweisen.</span><span class="sxs-lookup"><span data-stu-id="524d6-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="524d6-105">Die folgenden Abbildungen zeigen, wie Schrittsymbole und -titel in der mobilen Warehouse Management-App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="524d6-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="524d6-106">![Beispiel für ein Schrittsymbol und einen Schritttitel in der mobilen Warehouse Management-App](media/step-icon-example.png "Beispiel für ein Schrittsymbol und einen Schritttitel in der mobilen Warehouse Management-App")</span><span class="sxs-lookup"><span data-stu-id="524d6-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="524d6-107">Diese Funktion in Ihrem System aktivieren</span><span class="sxs-lookup"><span data-stu-id="524d6-107">Turn on this feature in your system</span></span>

<span data-ttu-id="524d6-108">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="524d6-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="524d6-109">Admins können die Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="524d6-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="524d6-110">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="524d6-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="524d6-111">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="524d6-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="524d6-112">**Funktionsname:** *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App*</span><span class="sxs-lookup"><span data-stu-id="524d6-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="524d6-113">Standard-Schritt-IDs, Klassen und Symbole</span><span class="sxs-lookup"><span data-stu-id="524d6-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="524d6-114">Jeder Schritt in einem Aufgabenfluss wird durch eine Schritt-ID identifiziert, und jede Schritt-ID hat eine entsprechende Schrittklasse.</span><span class="sxs-lookup"><span data-stu-id="524d6-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="524d6-115">Das Schrittsymbol und der Titel werden in jeder Schrittklasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="524d6-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="524d6-116">Schritt-IDs und Schrittklassen</span><span class="sxs-lookup"><span data-stu-id="524d6-116">Step IDs and step classes</span></span>

<span data-ttu-id="524d6-117">In der folgenden Tabelle sind alle derzeit verfügbaren Schritt-IDs und die entsprechende Schrittklasse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="524d6-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="524d6-118">Der Steuerungsname des primären Eingabefelds wird als Schritt-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="524d6-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="524d6-119">Ein Beispiel, das zeigt, wie diese Schritt-IDs und Klassen verwendet werden, finden Sie in der Implementierung der `WHSMobileAppStepInfoBuilder.stepId()` Methode im Abschnitt unter [Beispiel: Weisen Sie Schrittsymbole und -titel für einen benutzerdefinierten Ablauf zu](#example) später in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="524d6-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="524d6-120">Schrittkennung</span><span class="sxs-lookup"><span data-stu-id="524d6-120">Step ID</span></span> | <span data-ttu-id="524d6-121">Schritt Klasse</span><span class="sxs-lookup"><span data-stu-id="524d6-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="524d6-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-122">BatchDisposition</span></span> | <span data-ttu-id="524d6-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="524d6-124">Spediteur</span><span class="sxs-lookup"><span data-stu-id="524d6-124">Carrier</span></span> | <span data-ttu-id="524d6-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="524d6-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="524d6-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-126">CatchWeight</span></span> | <span data-ttu-id="524d6-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="524d6-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="524d6-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="524d6-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="524d6-130">CatchWeightTag</span></span> | <span data-ttu-id="524d6-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="524d6-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="524d6-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="524d6-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="524d6-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="524d6-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="524d6-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="524d6-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="524d6-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="524d6-136">CheckDigit</span></span> | <span data-ttu-id="524d6-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="524d6-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="524d6-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="524d6-138">ClusterId</span></span> | <span data-ttu-id="524d6-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="524d6-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="524d6-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="524d6-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="524d6-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="524d6-142">ClusterPosition</span></span> | <span data-ttu-id="524d6-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="524d6-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="524d6-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="524d6-144">ConfigId</span></span> | <span data-ttu-id="524d6-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="524d6-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="524d6-146">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="524d6-146">Confirmation</span></span> | <span data-ttu-id="524d6-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="524d6-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="524d6-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="524d6-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="524d6-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="524d6-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="524d6-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="524d6-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="524d6-154">ContainerType</span></span> | <span data-ttu-id="524d6-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="524d6-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="524d6-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="524d6-156">CountingReasonCode</span></span> | <span data-ttu-id="524d6-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="524d6-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="524d6-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="524d6-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="524d6-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="524d6-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="524d6-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="524d6-160">CycleCountQty1</span></span> | <span data-ttu-id="524d6-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="524d6-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="524d6-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="524d6-162">CycleCountQty2</span></span> | <span data-ttu-id="524d6-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="524d6-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="524d6-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="524d6-164">CycleCountQty3</span></span> | <span data-ttu-id="524d6-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="524d6-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="524d6-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="524d6-166">CycleCountQty4</span></span> | <span data-ttu-id="524d6-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="524d6-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="524d6-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="524d6-168">Disposition</span></span> | <span data-ttu-id="524d6-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="524d6-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="524d6-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="524d6-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="524d6-172">DriverCheckInId</span></span> | <span data-ttu-id="524d6-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="524d6-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="524d6-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="524d6-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="524d6-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="524d6-176">DriverCheckOutId</span></span> | <span data-ttu-id="524d6-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="524d6-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="524d6-178">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="524d6-178">ExpDate</span></span> | <span data-ttu-id="524d6-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="524d6-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="524d6-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-180">FromBatchDisposition</span></span> | <span data-ttu-id="524d6-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="524d6-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="524d6-182">FromInventoryStatus</span></span> | <span data-ttu-id="524d6-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="524d6-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="524d6-184">Volle Menge</span><span class="sxs-lookup"><span data-stu-id="524d6-184">FullQty</span></span> | <span data-ttu-id="524d6-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="524d6-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="524d6-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="524d6-186">InboundPut</span></span> | <span data-ttu-id="524d6-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="524d6-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="524d6-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="524d6-188">InventBatchId</span></span> | <span data-ttu-id="524d6-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="524d6-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="524d6-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="524d6-190">InventColorId</span></span> | <span data-ttu-id="524d6-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="524d6-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="524d6-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-192">InventLocation</span></span> | <span data-ttu-id="524d6-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="524d6-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="524d6-194">InventLocationId</span></span> | <span data-ttu-id="524d6-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="524d6-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="524d6-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="524d6-196">InventSerialId</span></span> | <span data-ttu-id="524d6-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="524d6-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="524d6-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="524d6-198">InventSizeId</span></span> | <span data-ttu-id="524d6-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="524d6-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="524d6-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="524d6-200">InventStatusId</span></span> | <span data-ttu-id="524d6-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="524d6-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="524d6-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="524d6-202">InventStyleId</span></span> | <span data-ttu-id="524d6-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="524d6-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="524d6-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="524d6-204">InventVersionId</span></span> | <span data-ttu-id="524d6-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="524d6-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="524d6-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="524d6-206">ItemId</span></span> | <span data-ttu-id="524d6-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="524d6-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="524d6-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="524d6-208">ITMContainerID</span></span> | <span data-ttu-id="524d6-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="524d6-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="524d6-210">ITMShipmentID</span></span> | <span data-ttu-id="524d6-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="524d6-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="524d6-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="524d6-212">KanbanCardId</span></span> | <span data-ttu-id="524d6-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="524d6-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="524d6-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="524d6-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="524d6-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="524d6-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="524d6-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="524d6-216">KanbanOrCardId</span></span> | <span data-ttu-id="524d6-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="524d6-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="524d6-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-218">LicensePlateId</span></span> | <span data-ttu-id="524d6-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="524d6-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="524d6-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="524d6-220">LoadId</span></span> | <span data-ttu-id="524d6-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="524d6-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="524d6-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="524d6-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="524d6-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="524d6-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="524d6-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="524d6-224">LocOrLP</span></span> | <span data-ttu-id="524d6-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="524d6-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="524d6-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="524d6-226">LocOrLP_From</span></span> | <span data-ttu-id="524d6-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="524d6-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="524d6-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="524d6-228">LocOrLP_To</span></span> | <span data-ttu-id="524d6-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="524d6-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="524d6-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="524d6-230">LocOrLPCheck</span></span> | <span data-ttu-id="524d6-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="524d6-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="524d6-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-232">LocVerification</span></span> | <span data-ttu-id="524d6-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="524d6-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="524d6-234">LPAdjustIn</span></span> | <span data-ttu-id="524d6-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="524d6-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="524d6-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="524d6-236">LPBreakChildLP</span></span> | <span data-ttu-id="524d6-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="524d6-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="524d6-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="524d6-238">LPBreakParentLP</span></span> | <span data-ttu-id="524d6-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="524d6-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="524d6-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="524d6-240">LPBuildChildLP</span></span> | <span data-ttu-id="524d6-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="524d6-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="524d6-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="524d6-242">LPBuildParentLP</span></span> | <span data-ttu-id="524d6-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="524d6-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="524d6-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-244">LPVerification</span></span> | <span data-ttu-id="524d6-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="524d6-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-246">MergeContainerId</span></span> | <span data-ttu-id="524d6-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="524d6-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-248">MixedLPLineNum</span></span> | <span data-ttu-id="524d6-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="524d6-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="524d6-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="524d6-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="524d6-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="524d6-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="524d6-252">MovementConfirmCancel</span></span> | <span data-ttu-id="524d6-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="524d6-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="524d6-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-254">NewCaptureWeight</span></span> | <span data-ttu-id="524d6-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="524d6-256">Neuheit</span><span class="sxs-lookup"><span data-stu-id="524d6-256">NewQty</span></span> | <span data-ttu-id="524d6-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="524d6-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="524d6-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="524d6-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="524d6-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="524d6-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="524d6-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="524d6-260">OutboundPut</span></span> | <span data-ttu-id="524d6-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="524d6-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="524d6-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-262">OutboundWeight</span></span> | <span data-ttu-id="524d6-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="524d6-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-264">OverridePutNewLocation</span></span> | <span data-ttu-id="524d6-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="524d6-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="524d6-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="524d6-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-268">POLineNum</span></span> | <span data-ttu-id="524d6-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="524d6-270">Bestellnummer</span><span class="sxs-lookup"><span data-stu-id="524d6-270">PONum</span></span> | <span data-ttu-id="524d6-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="524d6-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="524d6-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="524d6-272">PositionFull</span></span> | <span data-ttu-id="524d6-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="524d6-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="524d6-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="524d6-274">PositionFullQty</span></span> | <span data-ttu-id="524d6-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="524d6-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="524d6-276">Konzentration</span><span class="sxs-lookup"><span data-stu-id="524d6-276">Potency</span></span> | <span data-ttu-id="524d6-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="524d6-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="524d6-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="524d6-278">PrinterName</span></span> | <span data-ttu-id="524d6-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="524d6-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="524d6-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="524d6-280">ProdId</span></span> | <span data-ttu-id="524d6-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="524d6-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="524d6-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="524d6-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="524d6-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-284">ProductConfirmation</span></span> | <span data-ttu-id="524d6-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="524d6-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="524d6-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="524d6-288">Einlagern</span><span class="sxs-lookup"><span data-stu-id="524d6-288">Put</span></span> | <span data-ttu-id="524d6-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="524d6-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="524d6-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="524d6-290">PutawayClusterId</span></span> | <span data-ttu-id="524d6-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="524d6-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="524d6-292">Mge</span><span class="sxs-lookup"><span data-stu-id="524d6-292">Qty</span></span> | <span data-ttu-id="524d6-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="524d6-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="524d6-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="524d6-294">QtyAdjust</span></span> | <span data-ttu-id="524d6-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="524d6-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="524d6-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="524d6-296">QtyShort</span></span> | <span data-ttu-id="524d6-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="524d6-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="524d6-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="524d6-298">QtyToConsume</span></span> | <span data-ttu-id="524d6-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="524d6-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="524d6-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="524d6-300">QtyToPick</span></span> | <span data-ttu-id="524d6-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="524d6-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="524d6-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="524d6-302">QtyToPut</span></span> | <span data-ttu-id="524d6-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="524d6-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="524d6-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="524d6-304">QtyToScrap</span></span> | <span data-ttu-id="524d6-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="524d6-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="524d6-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-306">QtyVerification</span></span> | <span data-ttu-id="524d6-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="524d6-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="524d6-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="524d6-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="524d6-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="524d6-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="524d6-310">ReasonString</span></span> | <span data-ttu-id="524d6-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="524d6-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="524d6-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="524d6-312">RecvLocationId</span></span> | <span data-ttu-id="524d6-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="524d6-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="524d6-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-314">RemoveContainerId</span></span> | <span data-ttu-id="524d6-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="524d6-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="524d6-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="524d6-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="524d6-318">RMANum</span></span> | <span data-ttu-id="524d6-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="524d6-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="524d6-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="524d6-320">ShortPickReason</span></span> | <span data-ttu-id="524d6-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="524d6-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="524d6-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="524d6-322">SortConOrLP</span></span> | <span data-ttu-id="524d6-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="524d6-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="524d6-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-324">SortLicensePlateId</span></span> | <span data-ttu-id="524d6-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="524d6-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="524d6-326">SortPositionId</span></span> | <span data-ttu-id="524d6-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="524d6-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="524d6-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-328">SortVerification</span></span> | <span data-ttu-id="524d6-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="524d6-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="524d6-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="524d6-330">StartLocationId</span></span> | <span data-ttu-id="524d6-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="524d6-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="524d6-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="524d6-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="524d6-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-334">TargetLicensePlateId</span></span> | <span data-ttu-id="524d6-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="524d6-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-336">TOLineNum</span></span> | <span data-ttu-id="524d6-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="524d6-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-338">ToLocation</span></span> | <span data-ttu-id="524d6-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="524d6-340">TONum</span><span class="sxs-lookup"><span data-stu-id="524d6-340">TONum</span></span> | <span data-ttu-id="524d6-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="524d6-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="524d6-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="524d6-342">ToWarehouse</span></span> | <span data-ttu-id="524d6-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="524d6-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="524d6-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="524d6-344">TransportLoadId</span></span> | <span data-ttu-id="524d6-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="524d6-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="524d6-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="524d6-346">WaveLabelId</span></span> | <span data-ttu-id="524d6-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="524d6-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="524d6-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="524d6-348">WaveLblQty</span></span> | <span data-ttu-id="524d6-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="524d6-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="524d6-350">Gewicht</span><span class="sxs-lookup"><span data-stu-id="524d6-350">Weight</span></span> | <span data-ttu-id="524d6-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="524d6-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="524d6-352">WeightToConsume</span></span> | <span data-ttu-id="524d6-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="524d6-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="524d6-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="524d6-354">WHSAdjustmentType</span></span> | <span data-ttu-id="524d6-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="524d6-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="524d6-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="524d6-356">WHSReceivingException</span></span> | <span data-ttu-id="524d6-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="524d6-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="524d6-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="524d6-358">WHSWorkException</span></span> | <span data-ttu-id="524d6-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="524d6-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="524d6-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="524d6-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="524d6-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="524d6-362">WMSLocationId</span></span> | <span data-ttu-id="524d6-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="524d6-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="524d6-364">WorkId</span></span> | <span data-ttu-id="524d6-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="524d6-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="524d6-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="524d6-366">WorkIdToCancel</span></span> | <span data-ttu-id="524d6-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="524d6-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="524d6-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="524d6-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="524d6-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="524d6-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="524d6-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="524d6-370">WorkPoolId</span></span> | <span data-ttu-id="524d6-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="524d6-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="524d6-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="524d6-372">ZoneId</span></span> | <span data-ttu-id="524d6-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="524d6-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="524d6-374">Verfügbare Schrittsymbole</span><span class="sxs-lookup"><span data-stu-id="524d6-374">Available step icons</span></span>

<span data-ttu-id="524d6-375">Das System enthält eine Sammlung von Standardschrittsymbolen, die Sie auch für Ihre benutzerdefinierten Schritte verwenden können.</span><span class="sxs-lookup"><span data-stu-id="524d6-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="524d6-376">Sie können derzeit keine benutzerdefinierten Schrittsymbole hochladen.</span><span class="sxs-lookup"><span data-stu-id="524d6-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="524d6-377">Daher müssen Sie immer eines der Standardschrittsymbole auswählen.</span><span class="sxs-lookup"><span data-stu-id="524d6-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="524d6-378">Die folgende Tabelle zeigt alle derzeit verfügbaren Standardschrittsymbole und ihren Namen.</span><span class="sxs-lookup"><span data-stu-id="524d6-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Über das Schrittsymbol"><br><span data-ttu-id="524d6-380">Info</span><span class="sxs-lookup"><span data-stu-id="524d6-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Fügen Sie ein Nummernschild- oder Artikelschritt-Symbol hinzu"><br><span data-ttu-id="524d6-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="524d6-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Chargendispositions-Schrittsymbol"><br><span data-ttu-id="524d6-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Symbol für den Schritt Träger"><br><span data-ttu-id="524d6-386">Spediteur</span><span class="sxs-lookup"><span data-stu-id="524d6-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Artikelgewicht Tag-Schrittsymbol"><br><span data-ttu-id="524d6-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="524d6-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Artikelgewicht Tag-Gewichtschrittsymbol"><br><span data-ttu-id="524d6-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Symbol für den Schritt Ziffernschritt überprüfen"><br><span data-ttu-id="524d6-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="524d6-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="ID-Schritt-Symbol ein- oder auschecken"><br><span data-ttu-id="524d6-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="524d6-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Symbol für den Schritt für untergeordnetes Kennzeichen"><br><span data-ttu-id="524d6-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="524d6-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Symbol für den Schritt für die Cluster-ID"><br><span data-ttu-id="524d6-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="524d6-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Symbol für den Schritt für die Cluster-Position"><br><span data-ttu-id="524d6-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="524d6-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Symbol für den Schritt für die Config-ID"><br><span data-ttu-id="524d6-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="524d6-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Symbol für den Schritt Feld konfigurieren"><br><span data-ttu-id="524d6-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="524d6-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con- oder LP-Schrittsymbol"><br><span data-ttu-id="524d6-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="524d6-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolidieren Sie vom Kennzeichen-ID-Schrittsymbol"><br><span data-ttu-id="524d6-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="524d6-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolidieren Sie zum Kennzeichen-ID-Schrittsymbol"><br><span data-ttu-id="524d6-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="524d6-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Schritttyp-Symbol für den Containertyp"><br><span data-ttu-id="524d6-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="524d6-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Symbol für den Schritt Zählen"><br><span data-ttu-id="524d6-414">Inventur</span><span class="sxs-lookup"><span data-stu-id="524d6-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Zählgrundsymbol Schritt Symbol"><br><span data-ttu-id="524d6-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="524d6-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Symbol für den Schritt für Herkunftslandcode"><br><span data-ttu-id="524d6-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="524d6-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Dispositions-Schrittsymbol"><br><span data-ttu-id="524d6-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="524d6-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Fertig Schritt Symbol"><br><span data-ttu-id="524d6-422">Fertig</span><span class="sxs-lookup"><span data-stu-id="524d6-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Symbol für Bestätigungsschritt zum Einckecken des Fahrers"><br><span data-ttu-id="524d6-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Symbol für den Schritt für das Einchecken der Fahrer-ID"><br><span data-ttu-id="524d6-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="524d6-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Symbol für den Schritt für das Auschecken der Fahrer-ID"><br><span data-ttu-id="524d6-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="524d6-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Ablaufdatum Schritt Symbol"><br><span data-ttu-id="524d6-430">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="524d6-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Symbol für den Schritt für das Feld"><br><span data-ttu-id="524d6-432">Feld</span><span class="sxs-lookup"><span data-stu-id="524d6-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Von Chargendispositions-Schrittsymbol"><br><span data-ttu-id="524d6-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="524d6-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Vom Inventarsstatus-Schrittsymbol"><br><span data-ttu-id="524d6-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="524d6-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Symbol für den Schritt für ID-Attribut"><br><span data-ttu-id="524d6-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="524d6-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Symbol für den Schritt für Inventar-Batch-ID"><br><span data-ttu-id="524d6-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="524d6-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Symbol für den Schritt für die Lagerfarb-ID"><br><span data-ttu-id="524d6-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="524d6-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Schritt-Symbol für Lagerstandort"><br><span data-ttu-id="524d6-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Symbol für den Schritt für Lager-Serien-ID"><br><span data-ttu-id="524d6-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="524d6-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Symbol für den Schritt für Lagergröße"><br><span data-ttu-id="524d6-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="524d6-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Symbol für den Schritt für die Lagerstatus-ID"><br><span data-ttu-id="524d6-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="524d6-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Symbol für den Schritt für Lagerstil-ID"><br><span data-ttu-id="524d6-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="524d6-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Inventarsversion ID_Schrittsymbol"><br><span data-ttu-id="524d6-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="524d6-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Symbol für den Schritt für die Artikel-ID"><br><span data-ttu-id="524d6-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="524d6-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Schritttyp-Symbol für den ITM-Containertyp"><br><span data-ttu-id="524d6-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="524d6-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Symbol für den Schritt für ITM-Lieferung"><br><span data-ttu-id="524d6-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="524d6-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban-Karten-ID-Schrittsymbol"><br><span data-ttu-id="524d6-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="524d6-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban oder Karten-ID-Schrittsymbol"><br><span data-ttu-id="524d6-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="524d6-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Symbol für den Schritt für Lizenz-Kennzeichen"><br><span data-ttu-id="524d6-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="524d6-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Symbol für den Schritt für die Lade-ID"><br><span data-ttu-id="524d6-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="524d6-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Schritt-ID für die Standortkennzeichenpositionierung"><br><span data-ttu-id="524d6-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="524d6-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Symbol für den Schritt für Standort oder Lizenzkennzeichen"><br><span data-ttu-id="524d6-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="524d6-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Standort oder Lizenzschild-Kontrollschritt-Symbol"><br><span data-ttu-id="524d6-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="524d6-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Symbol für den Schritt von Standort oder Lizenzkennzeichen"><br><span data-ttu-id="524d6-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="524d6-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Symbol für den Schritt für zu Standort oder Lizenzkennzeichen"><br><span data-ttu-id="524d6-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="524d6-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Symbol für den Schritt Langer Prozess abgeschlossen"><br><span data-ttu-id="524d6-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="524d6-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP-Pause übergeordnetes LP-Schrittsymbol"><br><span data-ttu-id="524d6-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="524d6-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Schritttyp-Symbol für das Zusammenführen der Container-ID"><br><span data-ttu-id="524d6-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Symbol für den Schritt für gemischte Lizenzkennzeichen-Zeilenzahlen"><br><span data-ttu-id="524d6-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Symbol für den Schritt des ausgehenden Gewichts"><br><span data-ttu-id="524d6-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="524d6-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Schritt Symbol für Besitzer"><br><span data-ttu-id="524d6-490">Eigentümer</span><span class="sxs-lookup"><span data-stu-id="524d6-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Symbol für den Schritt für übergeordnetes Kennzeichen"><br><span data-ttu-id="524d6-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="524d6-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Bitte bestätigen Sie das Schrittsymbol"><br><span data-ttu-id="524d6-494">Bitte bestätigen</span><span class="sxs-lookup"><span data-stu-id="524d6-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Symbol für den Schrittd für die Zeilenzahl der Bestellung"><br><span data-ttu-id="524d6-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Symbol für den Schrittd für die Zeilenzahl der Bestellungszahl"><br><span data-ttu-id="524d6-498">Bestellnummer</span><span class="sxs-lookup"><span data-stu-id="524d6-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Symbol für den Schritt für die vollständige Position"><br><span data-ttu-id="524d6-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="524d6-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Symbol für den Schritt für die Stärke"><br><span data-ttu-id="524d6-502">Konzentration</span><span class="sxs-lookup"><span data-stu-id="524d6-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Symbol für den Schritt für den Druckernamen"><br><span data-ttu-id="524d6-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="524d6-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Symbol für den Schritt für die Produktions-ID"><br><span data-ttu-id="524d6-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="524d6-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Symbol für den Produktbestätigungsschritt"><br><span data-ttu-id="524d6-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="524d6-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Symbol für den Positionierungsschritt"><br><span data-ttu-id="524d6-510">Einlagern</span><span class="sxs-lookup"><span data-stu-id="524d6-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Symbol für den Schritt Clustereinlagerungs-ID"><br><span data-ttu-id="524d6-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="524d6-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Symbol für Mengenschritt"><br><span data-ttu-id="524d6-514">Mge</span><span class="sxs-lookup"><span data-stu-id="524d6-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Symbold für Mengenanpassungsschritt"><br><span data-ttu-id="524d6-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="524d6-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Symbol für Kurz-Mengenschritt"><br><span data-ttu-id="524d6-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="524d6-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Symbol zu Mengen für Verbraucherschritt"><br><span data-ttu-id="524d6-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="524d6-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Symbol zu Mengen für Einlagerungsschritt"><br><span data-ttu-id="524d6-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="524d6-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Symbol zu Mengen für Verschrottungsschritt"><br><span data-ttu-id="524d6-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="524d6-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Symbol für den Mengenbestätigungsschritt"><br><span data-ttu-id="524d6-526">Mengenbestätigung</span><span class="sxs-lookup"><span data-stu-id="524d6-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Als fertiges Endschritt-Symbol melden"><br><span data-ttu-id="524d6-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="524d6-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Symbol für den Schritt für Standort-Empfangs-ID"><br><span data-ttu-id="524d6-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="524d6-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Schritttyp-Symbol für das Entfernen der Container-ID"><br><span data-ttu-id="524d6-532">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="524d6-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA-Nummernschritt-Symbol"><br><span data-ttu-id="524d6-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="524d6-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Wählen Sie das Bestellschritt-Symbol"><br><span data-ttu-id="524d6-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="524d6-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Kurzsymbol für Auswahlgrund"><br><span data-ttu-id="524d6-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="524d6-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Symbol für den Schritt für Positions-ID sortieren"><br><span data-ttu-id="524d6-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="524d6-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Symbol für den Schritt für Ziel-Ladungsträger-ID"><br><span data-ttu-id="524d6-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Zum Zeilennummernschrittsymbol"><br><span data-ttu-id="524d6-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="524d6-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Zu Schritt-Symbol Standort"><br><span data-ttu-id="524d6-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="524d6-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Zu Schrittsymbol Zahl"><br><span data-ttu-id="524d6-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="524d6-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Zu Schritt-Symbol Lagerort"><br><span data-ttu-id="524d6-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="524d6-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Symbol für den Schritt für Datentransportauslastungs-ID"><br><span data-ttu-id="524d6-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="524d6-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Symbol für den Schritt für Lieferanten-Chargen-ID"><br><span data-ttu-id="524d6-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="524d6-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Symbol für den Schritt für die Wellenbeschriftungs-ID"><br><span data-ttu-id="524d6-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="524d6-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Symbol für den Schritt für die Wellenbeschriftungsmenge"><br><span data-ttu-id="524d6-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="524d6-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Symbol für den Schritt des Gewichts"><br><span data-ttu-id="524d6-560">Gewicht</span><span class="sxs-lookup"><span data-stu-id="524d6-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Symbol für den Schritt für das erforderliche Gewicht"><br><span data-ttu-id="524d6-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="524d6-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Symbol für den Schritt für den WHS Anpassungstyp"><br><span data-ttu-id="524d6-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="524d6-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Symbol für den Schritt für den Empfang der WHS-Ausnahme"><br><span data-ttu-id="524d6-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="524d6-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Symbol für den Schritt für die WMS Standort-ID"><br><span data-ttu-id="524d6-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="524d6-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Symbol für den Schritt für die Arbeits-ID"><br><span data-ttu-id="524d6-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="524d6-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Symbol für den Schritt zum Abbrechen der Arbeits-ID"><br><span data-ttu-id="524d6-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="524d6-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Symbol für den Schritt für die Arbeits-Kennzeichnungs-ID"><br><span data-ttu-id="524d6-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="524d6-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Symbol für den Schritt für die Cluster-Einlagerungs-ID"><br><span data-ttu-id="524d6-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="524d6-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Schritt für das Symbol für den Arbeits-Pool"><br><span data-ttu-id="524d6-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="524d6-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Symbol für den Schritt für die Zonen-ID"><br><span data-ttu-id="524d6-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="524d6-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="524d6-581">Beispiel: Weisen Sie Schrittsymbole und -titel für einen benutzerdefinierten Ablauf zu</span><span class="sxs-lookup"><span data-stu-id="524d6-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="524d6-582">In diesem Beispiel wird erläutert, wie Sie Schrittsymbole und -titel für einen benutzerdefinierten Aufgabenablauf einrichten.</span><span class="sxs-lookup"><span data-stu-id="524d6-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="524d6-583">Das Szenario basiert auf einem Beispiel für einen benutzerdefinierten Aufgabenablauf, der im folgenden Blogbeitrag ausführlicher vorgestellt und untersucht wird: [ Anpassen der Mobile App Lager](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="524d6-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="524d6-584">Der Aufgabenfluss funktioniert folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="524d6-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="524d6-585">Die App zeigt eine Seite an, auf der der Mitarbeiter aufgefordert wird, eine Container-ID anzugeben (z. B. durch Scannen eines Barcodes).</span><span class="sxs-lookup"><span data-stu-id="524d6-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="524d6-586">Wenn die Container-ID gültig ist, öffnet die App eine neue Seite, auf der die Arbeitskraft zur Eingabe des Gewichts aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="524d6-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="524d6-587">(Wenn die Container-ID nicht gültig ist, kehrt die Arbeitskraft zur ersten Seite zurück.)</span><span class="sxs-lookup"><span data-stu-id="524d6-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="524d6-588">Wenn die Arbeitskraft ein gültiges Gewicht eingibt, speichert das System das Gewicht und die Arbeitskraft kehrt zur ersten Seite zurück.</span><span class="sxs-lookup"><span data-stu-id="524d6-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="524d6-589">Die folgende Abbildung zeigt diesen Aufgabenfluss.</span><span class="sxs-lookup"><span data-stu-id="524d6-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="524d6-590">![Aufgabenflussdiagramm](media/step-icons-example-task-flow.png "Aufgabenflussdiagramm")</span><span class="sxs-lookup"><span data-stu-id="524d6-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="524d6-591">Erstellen Sie eine Schrittklasse für die Containereingabeseite</span><span class="sxs-lookup"><span data-stu-id="524d6-591">Create a step class for the container input page</span></span>

<span data-ttu-id="524d6-592">Auf der Containereingabeseite kann der Mitarbeiter eine Container-ID scannen oder eingeben.</span><span class="sxs-lookup"><span data-stu-id="524d6-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="524d6-593">![Containereingabeseite](media/step-icons-example-container-input.png "Containereingabeseite")</span><span class="sxs-lookup"><span data-stu-id="524d6-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="524d6-594">Auf der Containereingabeseite lautet der Kontrollname des Eingabefelds `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="524d6-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="524d6-595">Weil dieser Kontrollname nicht in der [Liste der Schritt-IDs](#step-ids-classes) enthalten ist, finden Sie keinen vorhandenen Schritt, der darauf basiert.</span><span class="sxs-lookup"><span data-stu-id="524d6-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="524d6-596">Daher müssen Sie eine Schrittklasse erstellen, die den Schritt darstellt.</span><span class="sxs-lookup"><span data-stu-id="524d6-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="524d6-597">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="524d6-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="524d6-598">Die Kennung des Schrittsymbols wird im `defaultStepIcon` Klassenmitglied gespeichert und der Schritttitel wird im `defaultStepTitle` Klassenmitglied gespeichert.</span><span class="sxs-lookup"><span data-stu-id="524d6-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="524d6-599">Um ein Schrittsymbol zuzuweisen, setzen Sie `defaultStepIcon` zu einer der Symbol-IDs, die im Abschnitt [Verfügbare Schrittsymbole](#step-icons) weiter oben in diesem Thema aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="524d6-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="524d6-600">Verwenden Sie ein Standard- oder benutzerdefiniertes Schrittsymbol und einen Titel für die Gewichtseingabe</span><span class="sxs-lookup"><span data-stu-id="524d6-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="524d6-601">Auf der Seite zur Gewichtseingabe kann der Mitarbeiter ein Gewicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="524d6-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="524d6-602">![Gewichtseingabeseite](media/step-icons-example-weight-input.png "Gewichtseingabeseite")</span><span class="sxs-lookup"><span data-stu-id="524d6-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="524d6-603">Auf der Gewichtseingabeseite lautet der Kontrollname des Eingabefelds `Weight`, der in der [Liste der Schritt-IDs](#step-ids-classes) ist.</span><span class="sxs-lookup"><span data-stu-id="524d6-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="524d6-604">Wenn das Schrittsymbol und der Titel, die in der `WHSMobileAppStepWeight` Klasse definiert sind, akzeptabel sind, müssen Sie für diesen Schritt nichts ändern.</span><span class="sxs-lookup"><span data-stu-id="524d6-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="524d6-605">Wenn Sie für diesen Schritt jedoch lieber ein anderes Symbol oder einen anderen Titel verwenden möchten, können Sie entweder die `stepId()` Methode oder die `stepInfo()` Methode in der Builder-Klasse überschreiben.</span><span class="sxs-lookup"><span data-stu-id="524d6-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="524d6-606">Jeder Aufgabenfluss verfügt über einen eigenen Builder für Schrittinformationen.</span><span class="sxs-lookup"><span data-stu-id="524d6-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="524d6-607">Überschreiben Sie die stepId () -Methode</span><span class="sxs-lookup"><span data-stu-id="524d6-607">Override the stepId() method</span></span>

<span data-ttu-id="524d6-608">Das folgende Beispiel zeigt eine Möglichkeit, wie Sie eine Builder-Klasse ändern können, indem Sie die `stepId()` Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="524d6-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="524d6-609">Anschließend erstellen Sie eine Schrittklasse für den `NewWeight` Schritt.</span><span class="sxs-lookup"><span data-stu-id="524d6-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="524d6-610">Der Code sollte dem Code für das `ContainerId` Beispiel ähneln, das weiter oben in diesem Thema gezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="524d6-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="524d6-611">Überschreiben Sie die stepInfo () -Methode</span><span class="sxs-lookup"><span data-stu-id="524d6-611">Override the stepInfo() method</span></span>

<span data-ttu-id="524d6-612">Das folgende Beispiel zeigt eine Möglichkeit, wie Sie eine Builder-Klasse ändern können, indem Sie die `stepInfo()` Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="524d6-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="524d6-613">Sie konstruieren dann ein `WHSMobileAppStepInfo` Objekt und legen das Symbol und/oder den Titel direkt fest.</span><span class="sxs-lookup"><span data-stu-id="524d6-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="524d6-614">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="524d6-614">Additional resources</span></span>

- [<span data-ttu-id="524d6-615">Mobile Lagerortsverwaltungs-App installieren und verbinden</span><span class="sxs-lookup"><span data-stu-id="524d6-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="524d6-616">Benutzereinstellungen für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="524d6-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
