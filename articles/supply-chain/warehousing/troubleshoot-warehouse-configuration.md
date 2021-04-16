---
title: Fehlerbehebung bei der Lagerort-Konfiguration
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Konfiguration von Microsoft Dynamics 365 Supply Chain Management auftreten können.
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
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814391"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="b672f-103">Fehlerbehebung bei der Lagerort-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b672f-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b672f-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Konfiguration von Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="b672f-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="b672f-105">Ich erhalte die folgende Fehlermeldung: „Der Ladungsträger oder Lagerplatz ist nicht gültig.“</span><span class="sxs-lookup"><span data-stu-id="b672f-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-106">Issue description</span></span>

<span data-ttu-id="b672f-107">Sie erhalten diese Fehlermeldung, wenn Sie einen Ladungsträger oder einen Lagerplatz scannen.</span><span class="sxs-lookup"><span data-stu-id="b672f-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-108">Issue resolution</span></span>

<span data-ttu-id="b672f-109">Stellen Sie sicher, dass die Ladungsträger-ID nicht durch etwas anderes reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="b672f-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="b672f-110">Dieses Problem trat früher auf, wenn der Wert, den ein Benutzer in der Warehouse Management Mobile App gescannt hat, sowohl ein gültiger Lagerplatz als auch eine gültige Ladungsträger-ID war.</span><span class="sxs-lookup"><span data-stu-id="b672f-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="b672f-111">Dieses Problem wurde jedoch in Version 10.0.11 behoben.</span><span class="sxs-lookup"><span data-stu-id="b672f-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="b672f-112">Ich erhalte die folgende Fehlermeldung: „Der Ladungsträger muss für diesen Lagerplatz angegeben werden.“</span><span class="sxs-lookup"><span data-stu-id="b672f-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-113">Issue description</span></span>

<span data-ttu-id="b672f-114">Sie erhalten diese Fehlermeldung, wenn Sie einen Transportauftrag unter Verwendung eines Lagers erstellen, das für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann nach Abschluss der Arbeit versuchen, die Sendung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="b672f-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-115">Issue resolution</span></span>

<span data-ttu-id="b672f-116">Das Feld **Standard-Eingangsort** ist für ein Transitlager des „von“-Lagers leer.</span><span class="sxs-lookup"><span data-stu-id="b672f-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="b672f-117">Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an.</span><span class="sxs-lookup"><span data-stu-id="b672f-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="b672f-118">Stellen Sie sicher, dass dieser Lagerplatz über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="b672f-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="b672f-119">Ich erhalte die folgende Fehlermeldung: „Sie können keine Arbeitsvorlagenzeile für Bestandsstatusänderung erstellen, da der Arbeitstyp nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b672f-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="b672f-120">Wählen Sie einen anderen Arbeitstyp.“</span><span class="sxs-lookup"><span data-stu-id="b672f-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-121">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-121">Issue description</span></span>

<span data-ttu-id="b672f-122">Für eine Arbeitsvorlage können Sie in der Spalte **Arbeitstyp** des Abschnitts **Arbeitsvorlagendetails** nicht *Bestandsstatusänderung* auswählen.</span><span class="sxs-lookup"><span data-stu-id="b672f-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-123">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-123">Issue resolution</span></span>

<span data-ttu-id="b672f-124">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="b672f-124">This behavior is by design.</span></span> <span data-ttu-id="b672f-125">Der Arbeitstyp *Bestandsstatusänderung* wird nur von Systemprozessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b672f-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="b672f-126">Er kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b672f-126">It can't be configured.</span></span> <span data-ttu-id="b672f-127">Da die Liste der Arbeitstypen als Aufzählung festgelegt ist, können die zusätzlichen Einträge nicht aus dem Dropdown-Menü **Arbeitstyp** herausgefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="b672f-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="b672f-128">Ich erhalte die folgende Fehlermeldung: „Die Menge ist für die Einheit 1% nicht gültig.“</span><span class="sxs-lookup"><span data-stu-id="b672f-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-129">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-129">Issue description</span></span>

<span data-ttu-id="b672f-130">Die Menge ist für die Einheit *ea* nicht gültig, wenn es Entnahmearbeiten gibt, die mehrere Ladungsträger an einem Lagerplatz haben.</span><span class="sxs-lookup"><span data-stu-id="b672f-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-131">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-131">Issue resolution</span></span>

<span data-ttu-id="b672f-132">Stellen Sie sicher, dass die Felder **Einheit Sequenz Gruppen-ID** und **Einheit Umrechnungen** auf dem freigegebenen Produkt oder der Produktvariante korrekt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b672f-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="b672f-133">Beachten Sie, dass die Fehlermeldung in Version 10.0.15 verbessert wurde (siehe [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="b672f-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="b672f-134">Die neue Fehlermeldung lautet: „Die Menge ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="b672f-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="b672f-135">Erwartet wird %1 %2.“</span><span class="sxs-lookup"><span data-stu-id="b672f-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="b672f-136">In Lagerplatzrichtlinien für das Einlagern von Verkaufsaufträgen wertet die Option „Mehrere SKU“ nicht mehrere Lagerplatzrichtlinien-Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="b672f-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-137">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-137">Issue description</span></span>

<span data-ttu-id="b672f-138">Lagerplatzrichtlinien der Arbeitsauftragsart *Verkaufsaufträge* und der Arbeitsauftragsart *Einlagern* werten nicht mehrere Lagerplatzrichtlinien-Aktionen aus, wenn die Option **Mehrere SKU** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b672f-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="b672f-139">Es wird nur die erste Aktion der Lagerplatzrichtlinie ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="b672f-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-140">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-140">Issue resolution</span></span>

<span data-ttu-id="b672f-141">Eine neue Funktion, *Alle Aktionen für Multi SKU Lagerplatzrichtlinien auswerten*, wurde in Version 10.0.15 hinzugefügt (siehe [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="b672f-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="b672f-142">Diese Funktion wertet alle Aktionen für Multi-SKU Lagerplatzrichtlinien aus.</span><span class="sxs-lookup"><span data-stu-id="b672f-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="b672f-143">Wenn Sie diese Funktion benötigen, verwenden Sie [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b672f-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="b672f-144">Ich kann mit der Warehouse Management Mobile App keine Teilkommissionierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="b672f-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-145">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-145">Issue description</span></span>

<span data-ttu-id="b672f-146">Bei Verkaufs- und Transportaufträgen können Sie keine Elemente überspringen und eine Teilkommissionierung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b672f-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-147">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-147">Issue resolution</span></span>

<span data-ttu-id="b672f-148">Legen Sie auf der Seite **Mobilgeräte-Menüelemente** für jeden Menüpunkt, der für die Bearbeitung von Verkaufsaufträgen oder Transportaufträgen eingerichtet ist, die Option **Arbeitsteilung zulassen** auf dem Inforegister **Allgemein** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="b672f-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="b672f-149">Wie kann ich eine Bestandsstatusänderung für Teilmengenarbeiten durchführen?</span><span class="sxs-lookup"><span data-stu-id="b672f-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-150">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-150">Issue description</span></span>

<span data-ttu-id="b672f-151">Sie möchten eine Bestandsstatusänderung für eine Teilmenge einer Charge durchführen.</span><span class="sxs-lookup"><span data-stu-id="b672f-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-152">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-152">Issue resolution</span></span>

<span data-ttu-id="b672f-153">Um den Arbeitskräften diese Änderung zu ermöglichen, können Sie einen Menüpunkt für die Warehouse Management Mobile App erstellen.</span><span class="sxs-lookup"><span data-stu-id="b672f-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="b672f-154">Erstellen (oder bearbeiten) Sie auf der Seite **Mobilgeräte-Menüpunkte** einen Menüpunkt, der die folgenden Einstellungen hat:</span><span class="sxs-lookup"><span data-stu-id="b672f-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="b672f-155">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="b672f-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="b672f-156">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="b672f-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="b672f-157">**Arbeitserstellungsprozess:** *Bewegung*</span><span class="sxs-lookup"><span data-stu-id="b672f-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="b672f-158">**Status des Bestands anzeigen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b672f-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="b672f-159">Sie können weitere Felder auf der Seite nach Bedarf festlegen.</span><span class="sxs-lookup"><span data-stu-id="b672f-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="b672f-160">Das Dock-Verwaltungsprofil eines Lagerplatz-Profils verhindert nicht, dass Bestandstypen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="b672f-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b672f-161">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="b672f-161">Issue description</span></span>

<span data-ttu-id="b672f-162">Sie verwenden *Sendungskonsolidierungsrichtlinien*.</span><span class="sxs-lookup"><span data-stu-id="b672f-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="b672f-163">Sie haben ein *Dock-Verwaltungsprofil* für ein *Standortprofil* festgelegt, aber wenn Arbeit erstellt wird, werden die Bestandstypen am endgültigen Lagerplatz gemischt.</span><span class="sxs-lookup"><span data-stu-id="b672f-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b672f-164">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="b672f-164">Issue resolution</span></span>

<span data-ttu-id="b672f-165">Dock-Verwaltungsprofile erfordern, dass die Arbeit im Voraus aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="b672f-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="b672f-166">Mit anderen Worten, das Dock-Verwaltungsprofil erwartet, dass ein Arbeitskopf nicht mehrere Lagerplätze einlagert.</span><span class="sxs-lookup"><span data-stu-id="b672f-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="b672f-167">Damit das Dock-Verwaltungsprofil die Vermischung von Beständen effektiv verwalten kann, muss eine Arbeitskopfunterbrechung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b672f-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="b672f-168">In diesem Beispiel ist unser Dock-Verwaltungsprofil so konfiguriert, dass **Bestandstypen, die nicht gemischt werden sollen** auf *Sendungs-ID* festgelegt ist, und wir werden eine Arbeitskopfunterbrechung dafür einrichten:</span><span class="sxs-lookup"><span data-stu-id="b672f-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="b672f-169">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="b672f-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b672f-170">Wählen Sie die **Arbeitsauftragsart**, die Sie bearbeiten wollen (z.B. *Einkaufsbestellungen*).</span><span class="sxs-lookup"><span data-stu-id="b672f-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="b672f-171">Wählen Sie die zu bearbeitende Arbeitsvorlage.</span><span class="sxs-lookup"><span data-stu-id="b672f-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="b672f-172">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b672f-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b672f-173">Öffnen Sie die Registerkarte **Sortierung** und fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="b672f-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="b672f-174">**Tabelle** - *Vorläufige Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="b672f-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="b672f-175">**Abgeleitete Tabelle** - *Zeitweilige Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="b672f-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="b672f-176">**Feld** - *Sendungs-ID*</span><span class="sxs-lookup"><span data-stu-id="b672f-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="b672f-177">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b672f-177">Select **OK**.</span></span>
1. <span data-ttu-id="b672f-178">Sie kehren auf die Seite **Arbeitsvorlagen** zurück.</span><span class="sxs-lookup"><span data-stu-id="b672f-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="b672f-179">Wählen Sie im Aktivitätsbereich **Arbeitskopfzeilenumbrüche** aus.</span><span class="sxs-lookup"><span data-stu-id="b672f-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="b672f-180">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b672f-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b672f-181">Aktivieren Sie das Kontrollkästchen, das mit dem **Feldname** *Shipment ID* verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b672f-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="b672f-182">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b672f-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
