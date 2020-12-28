---
title: Fehlerbehebung bei der Lagerort-Konfiguration
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Konfiguration von Microsoft Dynamics 365 Supply Chain Management auftreten können.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646106"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="0f673-103">Fehlerbehebung bei der Lagerort-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0f673-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f673-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Konfiguration von Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="0f673-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="0f673-105">Ich erhalte die folgende Fehlermeldung: „Der Ladungsträger oder Lagerplatz ist nicht gültig.“</span><span class="sxs-lookup"><span data-stu-id="0f673-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-106">Issue description</span></span>

<span data-ttu-id="0f673-107">Sie erhalten diese Fehlermeldung, wenn Sie einen Ladungsträger oder einen Lagerplatz scannen.</span><span class="sxs-lookup"><span data-stu-id="0f673-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-108">Issue resolution</span></span>

<span data-ttu-id="0f673-109">Stellen Sie sicher, dass die Ladungsträger-ID nicht durch etwas anderes reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f673-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="0f673-110">Dieses Problem trat früher auf, wenn der Wert, den ein Benutzer in der Lagerort App gescannt hat, sowohl ein gültiger Lagerplatz als auch eine gültige Ladungsträger-ID war.</span><span class="sxs-lookup"><span data-stu-id="0f673-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="0f673-111">Dieses Problem wurde jedoch in Version 10.0.11 behoben.</span><span class="sxs-lookup"><span data-stu-id="0f673-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="0f673-112">Ich erhalte die folgende Fehlermeldung: „Der Ladungsträger muss für diesen Lagerplatz angegeben werden.“</span><span class="sxs-lookup"><span data-stu-id="0f673-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-113">Issue description</span></span>

<span data-ttu-id="0f673-114">Sie erhalten diese Fehlermeldung, wenn Sie einen Transportauftrag unter Verwendung eines Lagers erstellen, das für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann nach Abschluss der Arbeit versuchen, die Sendung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="0f673-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-115">Issue resolution</span></span>

<span data-ttu-id="0f673-116">Das Feld **Standard-Eingangsort** ist für ein Transitlager des „von“-Lagers leer.</span><span class="sxs-lookup"><span data-stu-id="0f673-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="0f673-117">Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an.</span><span class="sxs-lookup"><span data-stu-id="0f673-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="0f673-118">Stellen Sie sicher, dass dieser Lagerplatz über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="0f673-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="0f673-119">Ich erhalte die folgende Fehlermeldung: „Sie können keine Arbeitsvorlagenzeile für Bestandsstatusänderung erstellen, da der Arbeitstyp nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0f673-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="0f673-120">Wählen Sie einen anderen Arbeitstyp.“</span><span class="sxs-lookup"><span data-stu-id="0f673-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-121">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-121">Issue description</span></span>

<span data-ttu-id="0f673-122">Für eine Arbeitsvorlage können Sie in der Spalte **Arbeitstyp** des Abschnitts **Arbeitsvorlagendetails** nicht *Bestandsstatusänderung* auswählen.</span><span class="sxs-lookup"><span data-stu-id="0f673-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-123">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-123">Issue resolution</span></span>

<span data-ttu-id="0f673-124">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="0f673-124">This behavior is by design.</span></span> <span data-ttu-id="0f673-125">Der Arbeitstyp *Bestandsstatusänderung* wird nur von Systemprozessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f673-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="0f673-126">Er kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="0f673-126">It can't be configured.</span></span> <span data-ttu-id="0f673-127">Da die Liste der Arbeitstypen als Aufzählung festgelegt ist, können die zusätzlichen Einträge nicht aus dem Dropdown-Menü **Arbeitstyp** herausgefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="0f673-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="0f673-128">Ich erhalte die folgende Fehlermeldung: „Die Menge ist für die Einheit 1% nicht gültig.“</span><span class="sxs-lookup"><span data-stu-id="0f673-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-129">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-129">Issue description</span></span>

<span data-ttu-id="0f673-130">Die Menge ist für die Einheit *ea* nicht gültig, wenn es Entnahmearbeiten gibt, die mehrere Ladungsträger an einem Lagerplatz haben.</span><span class="sxs-lookup"><span data-stu-id="0f673-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-131">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-131">Issue resolution</span></span>

<span data-ttu-id="0f673-132">Stellen Sie sicher, dass die Felder **Einheit Sequenz Gruppen-ID** und **Einheit Umrechnungen** auf dem freigegebenen Produkt oder der Produktvariante korrekt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="0f673-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="0f673-133">Beachten Sie, dass die Fehlermeldung in Version 10.0.15 verbessert wurde (siehe [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="0f673-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="0f673-134">Die neue Fehlermeldung lautet: „Die Menge ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="0f673-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="0f673-135">Erwartet wird %1 %2.“</span><span class="sxs-lookup"><span data-stu-id="0f673-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="0f673-136">In Lagerplatzrichtlinien für das Einlagern von Verkaufsaufträgen wertet die Option „Mehrere SKU“ nicht mehrere Lagerplatzrichtlinien-Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="0f673-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-137">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-137">Issue description</span></span>

<span data-ttu-id="0f673-138">Lagerplatzrichtlinien der Arbeitsauftragsart *Verkaufsaufträge* und der Arbeitsauftragsart *Einlagern* werten nicht mehrere Lagerplatzrichtlinien-Aktionen aus, wenn die Option **Mehrere SKU** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="0f673-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="0f673-139">Es wird nur die erste Aktion der Lagerplatzrichtlinie ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="0f673-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-140">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-140">Issue resolution</span></span>

<span data-ttu-id="0f673-141">Eine neue Funktion, *Alle Aktionen für Multi SKU Lagerplatzrichtlinien auswerten*, wurde in Version 10.0.15 hinzugefügt (siehe [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="0f673-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="0f673-142">Diese Funktion wertet alle Aktionen für Multi-SKU Lagerplatzrichtlinien aus.</span><span class="sxs-lookup"><span data-stu-id="0f673-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="0f673-143">Wenn Sie diese Funktion benötigen, verwenden Sie [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0f673-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="0f673-144">Ich kann mit der Lagerort App keine Teilkommissionierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="0f673-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-145">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-145">Issue description</span></span>

<span data-ttu-id="0f673-146">Bei Verkaufs- und Transportaufträgen können Sie keine Elemente überspringen und eine Teilkommissionierung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0f673-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-147">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-147">Issue resolution</span></span>

<span data-ttu-id="0f673-148">Legen Sie auf der Seite **Mobilgeräte-Menüelemente** für jeden Menüpunkt, der für die Bearbeitung von Verkaufsaufträgen oder Transportaufträgen eingerichtet ist, die Option **Arbeitsteilung zulassen** auf dem Inforegister **Allgemein** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="0f673-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="0f673-149">Wie kann ich eine Bestandsstatusänderung für Teilmengenarbeiten durchführen?</span><span class="sxs-lookup"><span data-stu-id="0f673-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f673-150">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f673-150">Issue description</span></span>

<span data-ttu-id="0f673-151">Sie möchten eine Bestandsstatusänderung für eine Teilmenge einer Charge durchführen.</span><span class="sxs-lookup"><span data-stu-id="0f673-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f673-152">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="0f673-152">Issue resolution</span></span>

<span data-ttu-id="0f673-153">Um den Arbeitskräften diese Änderung zu ermöglichen, können Sie einen Menüpunkt für die Lagerort App erstellen.</span><span class="sxs-lookup"><span data-stu-id="0f673-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="0f673-154">Erstellen (oder bearbeiten) Sie auf der Seite **Mobilgeräte-Menüpunkte** einen Menüpunkt, der die folgenden Einstellungen hat:</span><span class="sxs-lookup"><span data-stu-id="0f673-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="0f673-155">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="0f673-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="0f673-156">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="0f673-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="0f673-157">**Arbeitserstellungsprozess:** *Bewegung*</span><span class="sxs-lookup"><span data-stu-id="0f673-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="0f673-158">**Status des Bestands anzeigen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="0f673-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="0f673-159">Sie können weitere Felder auf der Seite nach Bedarf festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f673-159">You can set other fields on the page as you require.</span></span>
