---
title: Fehlerbehebung bei Ladungserstellung und Sendungen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit der Ladungserstellung und den Sendungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e9964376a794661058da78152879d2142dd7ec51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828201"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="486b2-103">Fehlerbehebung bei Ladungserstellung und Sendungen</span><span class="sxs-lookup"><span data-stu-id="486b2-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="486b2-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit der Ladungserstellung und den Sendungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="486b2-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="486b2-105">Ich erhalte die folgende Fehlermeldung: „Sie können für diese Zeile keine Ladung erstellen, da sie Bestandsdimensionen enthält, die ungültig sind.“</span><span class="sxs-lookup"><span data-stu-id="486b2-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="486b2-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="486b2-106">Issue description</span></span>

<span data-ttu-id="486b2-107">Sie erhalten die folgende Fehlermeldung, wenn Sie versuchen, einen Rücklieferungs-Verkaufsauftrag an das Lagerort freizugeben:</span><span class="sxs-lookup"><span data-stu-id="486b2-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="486b2-108">Sie können keine Ladezeile für diese Auftragszeile erstellen, da sie Bestandsdimensionen enthält, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="486b2-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="486b2-109">Sie können sich nicht auf Bestandsdimensionen beziehen, die sich in der Reservierungshierarchie unterhalb der Dimension Lagerplatz befinden.</span><span class="sxs-lookup"><span data-stu-id="486b2-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="486b2-110">Entfernen Sie die ungültigen Dimensionen aus der Auftragszeile.</span><span class="sxs-lookup"><span data-stu-id="486b2-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="486b2-111">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="486b2-111">Issue resolution</span></span>

<span data-ttu-id="486b2-112">Leider unterstützt das Produkt keine Ladungsverarbeitung für einen Rückgabeprozess.</span><span class="sxs-lookup"><span data-stu-id="486b2-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="486b2-113">Daher können Sie den Verkaufsauftrag für die Rücklieferung nicht an das Lagerort freigeben.</span><span class="sxs-lookup"><span data-stu-id="486b2-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="486b2-114">Bei Verkaufsauftragstransaktionen können Sie nicht auf Bestandsdimensionen verweisen, die sich in der Reservierungshierarchie unterhalb der Dimension **Ort** befinden.</span><span class="sxs-lookup"><span data-stu-id="486b2-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="486b2-115">Die Lösung ist, die ungültigen Dimensionen aus der Auftragszeile zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="486b2-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="486b2-116">Ich erhalte die folgende Fehlermeldung: „Eine der Zeilen befindet sich bereits in einer Ladung.</span><span class="sxs-lookup"><span data-stu-id="486b2-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="486b2-117">Kann nicht an das Lagerort freigegeben werden.“</span><span class="sxs-lookup"><span data-stu-id="486b2-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="486b2-118">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="486b2-118">Issue description</span></span>

<span data-ttu-id="486b2-119">Wenn Sie Ladungen manuell erstellen oder den Prozess so festlegen, dass Ladungen bereits vor der Eingabe von Verkaufsauftragszeilen erstellt werden, wird davon ausgegangen, dass die anschließende Freigabe manuell erfolgt und dass der Arbeitsplan und die Einstufung aus der Ladung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="486b2-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="486b2-120">In einem anderen möglichen Szenario versuchen Sie, eine automatische Freigabe an das Lager durchzuführen, aber der Wellenprozess konnte keine Arbeit erstellen.</span><span class="sxs-lookup"><span data-stu-id="486b2-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="486b2-121">Daher wird noch eine offene Sendung oder Ladung erstellt.</span><span class="sxs-lookup"><span data-stu-id="486b2-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="486b2-122">Diese offene Sendung oder Ladung blockiert dann nachfolgende Versuche, den Auftrag automatisch freizugeben, bis Sie entweder die offene Sendung oder Ladung löschen oder die Welle manuell neu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="486b2-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="486b2-123">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="486b2-123">Issue resolution</span></span>

<span data-ttu-id="486b2-124">Sie können die Freigabe über die Seite Verkaufsauftrag oder die automatische Freigabe über die Seite Freigabe Verkaufsauftrag nur dann durchführen, wenn vor der Freigabe an das Lager keine Ladung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="486b2-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="486b2-125">Die Ladung wird automatisch erstellt, nachdem die Welle verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="486b2-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="486b2-126">Ich erhalte die folgende Fehlermeldung: „Die Lieferscheinkorrektur kann nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="486b2-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="486b2-127">Der Lieferschein enthält nur Elemente, die den Prozessen der Lagerortverwaltung unterliegen, da diese von der Lieferscheinkorrektur nicht unterstützt werden.“</span><span class="sxs-lookup"><span data-stu-id="486b2-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="486b2-128">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="486b2-128">Issue description</span></span>

<span data-ttu-id="486b2-129">Nachdem Sie einen Lieferschein gebucht haben, können Sie ihn nicht stornieren, da die Schaltfläche **Stornieren** nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="486b2-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="486b2-130">Sie können den Lieferschein auch nicht korrigieren.</span><span class="sxs-lookup"><span data-stu-id="486b2-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="486b2-131">Wenn Sie es versuchen, erhalten Sie diese Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="486b2-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="486b2-132">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="486b2-132">Issue resolution</span></span>

<span data-ttu-id="486b2-133">Um gebuchte Lieferscheine für Elemente zu korrigieren, die für die erweiterte Lagerortverwaltung (WMS) aktiviert sind, müssen Sie die Buchung aus der Ladung heraus vornehmen, nicht direkt aus dem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="486b2-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="486b2-134">Wie kann ich Arbeit aus ausgehenden Ladungen statt aus Wellen erstellen?</span><span class="sxs-lookup"><span data-stu-id="486b2-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="486b2-135">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="486b2-135">Issue description</span></span>

<span data-ttu-id="486b2-136">Hier ist eine Möglichkeit, dieses Problem zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="486b2-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="486b2-137">Erstellen Sie eine ausgehende Ladung mit Hilfe eines Verkaufsauftrags oder eines Transportauftrags.</span><span class="sxs-lookup"><span data-stu-id="486b2-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="486b2-138">Geben Sie die Ladung für den Lagerort frei.</span><span class="sxs-lookup"><span data-stu-id="486b2-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="486b2-139">Beachten Sie, dass noch keine Entnahmearbeiten erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="486b2-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="486b2-140">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="486b2-140">Issue resolution</span></span>

<span data-ttu-id="486b2-141">Wenn bei der Freigabe der Ladung sofort Arbeit erzeugt werden muss, müssen Sie die Wellenvorlage entsprechend konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="486b2-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="486b2-142">Legen Sie in der Wellenvorlage die folgenden Optionen auf *Ja* fest:</span><span class="sxs-lookup"><span data-stu-id="486b2-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="486b2-143">Wellenerstellung automatisieren</span><span class="sxs-lookup"><span data-stu-id="486b2-143">Automate wave creation</span></span>
- <span data-ttu-id="486b2-144">Welle bei Freigabe für Lagerort verarbeiten</span><span class="sxs-lookup"><span data-stu-id="486b2-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="486b2-145">Wellenfreigabe automatisieren</span><span class="sxs-lookup"><span data-stu-id="486b2-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="486b2-146">Ich kann eine teilweise ausgelieferte Ladung nicht wieder freigeben.</span><span class="sxs-lookup"><span data-stu-id="486b2-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="486b2-147">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="486b2-147">Issue description</span></span>

<span data-ttu-id="486b2-148">Sie können eine teilweise ausgelieferte Ladung nicht an das Lagerort freigeben.</span><span class="sxs-lookup"><span data-stu-id="486b2-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="486b2-149">Wenn Sie die Freigabe an das Lagerort durchführen, erscheint die Meldung „Vorgang abgeschlossen“, aber es passiert nichts, und es wird keine Arbeit für die verbleibende Menge erstellt.</span><span class="sxs-lookup"><span data-stu-id="486b2-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="486b2-150">Dieses Problem tritt auf, wenn Sie die Transportladungsfunktionalität verwenden und es eine unvollständige Reservierung gibt.</span><span class="sxs-lookup"><span data-stu-id="486b2-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="486b2-151">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="486b2-151">Issue resolution</span></span>

<span data-ttu-id="486b2-152">[KB-Problem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Teilweise versendete Ladungen können erneut versendet und verarbeitet werden“) ist in [Version 10.0.15](../get-started/whats-new-scm-10-0-15.md) behoben.</span><span class="sxs-lookup"><span data-stu-id="486b2-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]