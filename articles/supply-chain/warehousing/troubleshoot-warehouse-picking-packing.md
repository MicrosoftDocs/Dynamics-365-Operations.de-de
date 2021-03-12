---
title: Fehlerbehebung beim Entnehmen und Verpacken
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die beim Entnehmen und Verpacken in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993930"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="59658-103">Fehlerbehebung beim Entnehmen und Verpacken</span><span class="sxs-lookup"><span data-stu-id="59658-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59658-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die beim Entnehmen und Verpacken in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="59658-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="59658-105">Ich erhalte die folgende Fehlermeldung: „Der Lagerplatz der Dimension kann nicht leer gelassen werden, wenn die Seriennummer der Dimension festgelegt ist.“</span><span class="sxs-lookup"><span data-stu-id="59658-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-106">Issue description</span></span>

<span data-ttu-id="59658-107">Sie erhalten diese Fehlermeldung, wenn Sie einen Transportauftrag für ein serielles Element erstellen, indem Sie ein Lagerort verwenden, der für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann, nachdem die Arbeit abgeschlossen ist, versuchen, die Sendung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="59658-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-108">Issue resolution</span></span>

<span data-ttu-id="59658-109">Das Feld **Standard-Eingangsort** ist für ein Transitlager des „von“-Lagers leer.</span><span class="sxs-lookup"><span data-stu-id="59658-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="59658-110">Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an.</span><span class="sxs-lookup"><span data-stu-id="59658-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="59658-111">Stellen Sie sicher, dass dieser Lagerplatz über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="59658-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="59658-112">Ich erhalte die folgende Fehlermeldung: „Ungültiger Ladungsträger“.</span><span class="sxs-lookup"><span data-stu-id="59658-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-113">Issue description</span></span>

<span data-ttu-id="59658-114">Sie erhalten diese Fehlermeldung in der Lagerort App, wenn Sie einen Ladungsträger ID scannen.</span><span class="sxs-lookup"><span data-stu-id="59658-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-115">Issue resolution</span></span>

<span data-ttu-id="59658-116">Vergewissern Sie sich, dass die Kennzeichen-ID in der Kennzeichentabelle vorhanden ist und dass die Elemente und Mengen auf dem Kennzeichen verfügbar sind (d.h. nicht gesperrt sind).</span><span class="sxs-lookup"><span data-stu-id="59658-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="59658-117">Ich erhalte die folgende Fehlermeldung: „Feld 'Lastgewicht'(=-%1) kann nur positive Zahlen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59658-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="59658-118">Die Aktualisierung wurde abgebrochen.“</span><span class="sxs-lookup"><span data-stu-id="59658-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-119">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-119">Issue description</span></span>

<span data-ttu-id="59658-120">Sie erhalten diese Fehlermeldung, wenn bei der Verarbeitung von Arbeit von Packplätzen zu Lagerplätzen oder von Lagerplätzen zu Andockplätzen offene Arbeit vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="59658-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-121">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-121">Issue resolution</span></span>

<span data-ttu-id="59658-122">Um dieses Problem zu beheben, gehen Sie zu **Systemadministration \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**, und führen Sie den Prozess für **Konsistenzprüfung für Lagerort-Lastgewicht** aus.</span><span class="sxs-lookup"><span data-stu-id="59658-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="59658-123">Ich erhalte die folgende Fehlermeldung: „Die Menge ist für die Einheit %1 nicht gültig.“</span><span class="sxs-lookup"><span data-stu-id="59658-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-124">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-124">Issue description</span></span>

<span data-ttu-id="59658-125">Sie erhalten diese Fehlermeldung, wenn Sie versuchen, eine *Gesplittete Entnahme* über mehrere Chargen hinweg durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="59658-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-126">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-126">Issue resolution</span></span>

<span data-ttu-id="59658-127">Die Arbeitskraft im Lager muss den Prozess *Kurzes Entnehmen* in der Lagerort App verwenden.</span><span class="sxs-lookup"><span data-stu-id="59658-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="59658-128">Wenn Sie versuchen, mehrere Chargen vom selben Lagerplatz zu entnehmen, können Sie auch die Option **Voll** in der Lagerort App verwenden.</span><span class="sxs-lookup"><span data-stu-id="59658-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="59658-129">Ich kann den Bestand nicht an einen Lagerplatz verschieben, der von Ladungsträgern kontrolliert wird.</span><span class="sxs-lookup"><span data-stu-id="59658-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-130">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-130">Issue description</span></span>

<span data-ttu-id="59658-131">Sie können die entnommenen Mengen einer Ladung nicht reduzieren.</span><span class="sxs-lookup"><span data-stu-id="59658-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-132">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-132">Issue resolution</span></span>

<span data-ttu-id="59658-133">In früheren Versionen können Sie die entnommenen Mengen auf einer Ladung nicht reduzieren.</span><span class="sxs-lookup"><span data-stu-id="59658-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="59658-134">Jetzt können Sie jedoch die Entnahme rückgängig machen und an einen Lagerplatz verschieben, der von einem Ladungsträger kontrolliert wird.</span><span class="sxs-lookup"><span data-stu-id="59658-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="59658-135">Sie müssen sowohl einen **Ort**-Wert als auch einen **Kennzeichen**-Wert für die Ladezeile auf der Seite **Kommissionierte Menge reduzieren** angeben.</span><span class="sxs-lookup"><span data-stu-id="59658-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="59658-136">Kann ich einen Lieferschein oder Verpackungsinhalt nach Lagerort drucken?</span><span class="sxs-lookup"><span data-stu-id="59658-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-137">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-137">Issue description</span></span>

<span data-ttu-id="59658-138">Sie möchten einen Lieferschein oder Packungsinhalt nach Lagerort oder Standort auf der Seite **Arbeitsprüfungsvorlage Zeilenaktualisierung** drucken.</span><span class="sxs-lookup"><span data-stu-id="59658-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-139">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-139">Issue resolution</span></span>

<span data-ttu-id="59658-140">Wenn Sie ein Dokument über die Einstellungen der Druckverwaltung ausdrucken, schränken Sie den Umfang (Standort/Lager) über die Druckverwaltung ein, anstatt durch die Auswahl von **Druckeinstellungen bearbeiten** auf der Seite **Work-Audit-Vorlage Zeilenaktualisierung**.</span><span class="sxs-lookup"><span data-stu-id="59658-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="59658-141">Ich kann einen Lieferschein nicht stornieren, nachdem er aus einem Verkaufsauftrag gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="59658-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-142">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-142">Issue description</span></span>

<span data-ttu-id="59658-143">Wenn Kommissionier- und Versandprozesse für WMS aktiviert sind, können Sie einen Lieferscheins nicht stornieren, nachdem er aus einem Verkaufsauftrag gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="59658-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-144">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-144">Issue resolution</span></span>

<span data-ttu-id="59658-145">Um gebuchte Lieferscheine für Artikel, die für WMS aktiviert sind, zu korrigieren, muss die Buchung aus der Ladung erfolgen, nicht aus dem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="59658-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="59658-146">Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="59658-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="59658-147">Im Allgemeinen kann ein Verkaufsauftrag, der durch Lagerortverwaltungsprozesse entnommen und versandt wurde, aus der Ladung oder dem Versand und dem Verkaufsauftragsbeleg selbst Lieferscheinaktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="59658-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="59658-148">Wenn Sie jedoch den Kundenauftrag vom Kundenauftragsbeleg aus Lieferscheinaktualisieren, kann die Stornierung des Lieferscheins immer noch nicht von der Ladung oder dem Kundenauftrag aus erfolgen.</span><span class="sxs-lookup"><span data-stu-id="59658-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="59658-149">Daher empfehlen wir Ihnen, die Lieferscheinbuchung aus der Ladung heraus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="59658-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="59658-150">In diesem Fall wird die Stornierung, die von der Ladung aus erfolgen muss, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="59658-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="59658-151">Ich erhalte die folgende Fehlermeldung: „Es kann nicht genügend Arbeit für den Cluster gefunden werden.“</span><span class="sxs-lookup"><span data-stu-id="59658-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59658-152">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="59658-152">Issue description</span></span>

<span data-ttu-id="59658-153">Wenn Sie den Prozess *Systemgesteuerte Cluster-Kommissionierung* verwenden und ein Cluster-Profil konfigurieren, bei dem z.B. 10 Positionen entnommen werden können, funktioniert der Prozess wie geplant, wenn genügend Arbeit vorhanden ist, um 10 Positionen zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="59658-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="59658-154">Wenn jedoch nur acht Positionen zu entnehmen sind, erhalten Sie diese Fehlermeldung, weil nicht genug Arbeit für einen Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="59658-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59658-155">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="59658-155">Issue resolution</span></span>

<span data-ttu-id="59658-156">Um dieses Problem zu beheben, bearbeiten Sie das Clusterprofil und legen Sie die Option **Positionen aktivieren** auf *Nein* fest.</span><span class="sxs-lookup"><span data-stu-id="59658-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
