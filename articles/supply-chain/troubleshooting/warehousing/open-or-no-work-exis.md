---
title: Sie können eine Sendung nicht bestätigen, weil Arbeiten unvollständig sind oder fehlen
description: Sie können eine Sendung nicht bestätigen, weil Arbeiten unvollständig sind oder fehlen
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123842"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="6eced-103">Sie können eine Sendung nicht bestätigen, weil Arbeiten unvollständig sind oder fehlen</span><span class="sxs-lookup"><span data-stu-id="6eced-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="6eced-104">Fehlercode: WAX515</span><span class="sxs-lookup"><span data-stu-id="6eced-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="6eced-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="6eced-105">Symptoms</span></span>

<span data-ttu-id="6eced-106">Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="6eced-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="6eced-107">Die Lieferung für die Ladung %1 konnte nicht überprüft werden, da sämtliche Arbeiten für die Ladung abgeschlossen sein müssen.</span><span class="sxs-lookup"><span data-stu-id="6eced-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="6eced-108">Daher können Sie die Sendung für die Ladung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6eced-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="6eced-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="6eced-109">Cause</span></span>

<span data-ttu-id="6eced-110">Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Versandbestätigung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6eced-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="6eced-111">Bevor Sie die Ladung bestätigen können, müssen zumindest einige Arbeiten für die Ladung vorhanden sein, und alle diese Arbeiten müssen einen Status von *Geschlossen* oder *Storniert* haben.</span><span class="sxs-lookup"><span data-stu-id="6eced-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="6eced-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="6eced-112">Resolution</span></span>

<span data-ttu-id="6eced-113">Prüfen Sie die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge für die Ladung oder den Transport, und stellen Sie sicher, dass alle zugehörigen Arbeiten abgeschlossen oder storniert wurden.</span><span class="sxs-lookup"><span data-stu-id="6eced-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="6eced-114">Sie können mit Sendungen und Ladungen auf mehreren Seiten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6eced-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="6eced-115">In den folgenden Unterabschnitten finden Sie einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="6eced-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="6eced-116">Alle Ladungen Seite</span><span class="sxs-lookup"><span data-stu-id="6eced-116">All loads page</span></span>

1. <span data-ttu-id="6eced-117">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="6eced-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6eced-118">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6eced-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="6eced-119">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="6eced-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="6eced-120">Untersuchen Sie den Status jeder Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="6eced-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="6eced-121">Verfolgen Sie jede Arbeits-ID nach, die nicht den Status *Geschlossen* oder *Storniert* hat.</span><span class="sxs-lookup"><span data-stu-id="6eced-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="6eced-122">Wenn jede Arbeits-ID den Status *Geschlossen* oder *Abgebrochen* hat, versuchen Sie erneut, die Sendung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6eced-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="6eced-123">Alle Sendungen Seite</span><span class="sxs-lookup"><span data-stu-id="6eced-123">All shipments page</span></span>

1. <span data-ttu-id="6eced-124">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="6eced-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="6eced-125">Wählen Sie die Sendung aus, die nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6eced-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="6eced-126">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Sendungen** in der Gruppe **Arbeit** die Option **Arbeitsdetails**.</span><span class="sxs-lookup"><span data-stu-id="6eced-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="6eced-127">Untersuchen Sie den Status jeder Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="6eced-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="6eced-128">Verfolgen Sie jede Arbeits-ID nach, die nicht den Status *Geschlossen* oder *Storniert* hat.</span><span class="sxs-lookup"><span data-stu-id="6eced-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="6eced-129">Wenn jede Arbeits-ID den Status *Geschlossen* oder *Abgebrochen* hat, versuchen Sie erneut, die Sendung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6eced-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="6eced-130">Seite „Alle Arbeiten</span><span class="sxs-lookup"><span data-stu-id="6eced-130">All work page</span></span>

1. <span data-ttu-id="6eced-131">Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Alle Arbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6eced-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="6eced-132">Wählen Sie die Arbeit für die Auftragsnummer, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6eced-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="6eced-133">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Sendung** in der Gruppe **Sendung** die Option **Sendung bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="6eced-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="6eced-134">Untersuchen Sie den Status jeder Arbeits-ID.</span><span class="sxs-lookup"><span data-stu-id="6eced-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="6eced-135">Verfolgen Sie jede Arbeits-ID nach, die nicht den Status *Geschlossen* oder *Storniert* hat.</span><span class="sxs-lookup"><span data-stu-id="6eced-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="6eced-136">Wenn jede Arbeits-ID den Status *Geschlossen* oder *Abgebrochen* hat, versuchen Sie erneut, die Sendung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6eced-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
