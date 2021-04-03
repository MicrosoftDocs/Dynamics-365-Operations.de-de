---
title: Rechnung für die Wartung von kundeneigenen Anlagen
description: In diesem Thema wird erläutert, wie Sie Wartungsarbeiten erstellen, verarbeiten und abrechnen, die an Anlagen durchgeführt werden, die Ihren Kunden gehören.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500453"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="5837a-103">Rechnung für die Wartung von kundeneigenen Anlagen</span><span class="sxs-lookup"><span data-stu-id="5837a-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="5837a-104">Mit der Funktion *Abrechnung von Arbeitsaufträgen* können Sie Wartungsarbeiten erstellen, verarbeiten und abrechnen, die an Anlagen durchgeführt werden, die Ihren Kunden gehören.</span><span class="sxs-lookup"><span data-stu-id="5837a-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="5837a-105">Mit dieser Funktion können folgende Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="5837a-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="5837a-106">Verbinden Sie Kunden mit den Anlagen, die sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="5837a-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="5837a-107">Wählen Sie einen Kunden aus, und zeigen Sie die Anlagen an, die der Kunde besitzt, wenn Sie einen Arbeitsauftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="5837a-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="5837a-108">Richten Sie für jeden Kunden ein übergeordnetes Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="5837a-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="5837a-109">Registrieren Sie Stunden, Artikel, Ausgaben und Gebühren für den Arbeitsauftrag und erstellen Sie später einen Rechnungsvorschlag für den Kunden.</span><span class="sxs-lookup"><span data-stu-id="5837a-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="5837a-110">Darüber hinaus bietet die Funktion die folgenden Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="5837a-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="5837a-111">Der Projektvertrag aus dem übergeordneten Projekt eines Kunden wird automatisch in das entsprechende Arbeitsauftragsprojekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="5837a-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="5837a-112">Die Anlagenverwaltung kann jetzt die Projekttransaktionsart *Gebühr* sowohl für Arbeitsauftragsprognosen als auch für Arbeitsauftragserfassungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5837a-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="5837a-113">Debitorenabrechnungsfunktion aktivieren</span><span class="sxs-lookup"><span data-stu-id="5837a-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="5837a-114">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5837a-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="5837a-115">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5837a-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="5837a-116">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5837a-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5837a-117">**Modul:** *Projektverwaltung und Buchhaltung*</span><span class="sxs-lookup"><span data-stu-id="5837a-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="5837a-118">**Funktionsname:** *Abrechnung von Arbeitsaufträgen*</span><span class="sxs-lookup"><span data-stu-id="5837a-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="5837a-119">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="5837a-119">Example scenario</span></span>

<span data-ttu-id="5837a-120">Um zu erfahren, wie diese Funktion funktioniert, arbeiten Sie das folgende Beispielszenario durch.</span><span class="sxs-lookup"><span data-stu-id="5837a-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="5837a-121">Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5837a-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="5837a-122">Sie müssen die juristische Person **USMF** auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="5837a-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="5837a-123">Sie können dieses Szenario auch als Anleitung zur Verwendung dieser Funktion nutzen, wenn Sie an einem Produktionssystem arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5837a-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="5837a-124">In diesem Fall müssen Sie jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5837a-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="5837a-125">Schritt 1: Erstellen Sie einen neuen Projektvertrag für den Kunden</span><span class="sxs-lookup"><span data-stu-id="5837a-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="5837a-126">Wechseln Sie zu **Projektverwaltung und Buchhaltung \> Projekte \> Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="5837a-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="5837a-127">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5837a-128">Legen Sie im Dialogfeld **Neuer Projektvertrag** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5837a-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5837a-129">**Name:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="5837a-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="5837a-130">**Finanzierungsart:** *Kunde*</span><span class="sxs-lookup"><span data-stu-id="5837a-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="5837a-131">**Finanzierungsquelle:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="5837a-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="5837a-132">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5837a-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="5837a-133">Schritt 2: Erstellen Sie einen übergeordneten Projektvertrag für den Kunden</span><span class="sxs-lookup"><span data-stu-id="5837a-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="5837a-134">Das übergeordnete Projekt, das Sie hier erstellen, wird verwendet, wenn Arbeitsaufträge für den Kunden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5837a-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="5837a-135">Wechseln Sie zu **Projektverwaltung und -verrechnung \> Projekte \> Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="5837a-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="5837a-136">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5837a-137">Legen Sie im Dialogfeld **Neues Projekt** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5837a-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5837a-138">**Projekttyp:** *Nach Aufwand*</span><span class="sxs-lookup"><span data-stu-id="5837a-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="5837a-139">**Projektname:** *Arbeitsaufträge von Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="5837a-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="5837a-140">**Projektgruppe:** *TM*</span><span class="sxs-lookup"><span data-stu-id="5837a-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="5837a-141">**Projektvertrags-ID:** *Pelikan Wholesales* (der Vertrag, den Sie zuvor erstellt haben)</span><span class="sxs-lookup"><span data-stu-id="5837a-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="5837a-142">**Startdatum:** Wählen Sie das heutige Datum aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="5837a-143">Wählen Sie **Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-143">Select **Create project**.</span></span>
1. <span data-ttu-id="5837a-144">Das neue Projekt wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5837a-144">The new project is opened.</span></span> <span data-ttu-id="5837a-145">Notieren Sie den Wert **Projekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="5837a-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="5837a-146">Sie müssen ihn später eingeben.</span><span class="sxs-lookup"><span data-stu-id="5837a-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="5837a-147">Schritt 3: Erstellen Sie einen neuen Arbeitsauftragstyp in der Anlagenverwaltung</span><span class="sxs-lookup"><span data-stu-id="5837a-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="5837a-148">Gehen Sie zu **Anlagenverwaltung \> Einstellungen \> Arbeitsauftrag \> Arbeitsauftragsarten**.</span><span class="sxs-lookup"><span data-stu-id="5837a-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="5837a-149">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5837a-150">Der Liste wird ein neuer Datensatz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5837a-150">A new record is added to the list.</span></span> <span data-ttu-id="5837a-151">Stellen Sie dafür die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="5837a-151">Set the following values for it:</span></span>

    - <span data-ttu-id="5837a-152">**Arbeitsauftragstyp:** *Service*</span><span class="sxs-lookup"><span data-stu-id="5837a-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="5837a-153">**Name:** *Servicearbeitsaufträge*</span><span class="sxs-lookup"><span data-stu-id="5837a-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="5837a-154">**Lebenszyklusstatus von Arbeitsaufträgen:** *Standard*</span><span class="sxs-lookup"><span data-stu-id="5837a-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="5837a-155">Schritt 4: Verknüpfen Sie das Kundenkonto mit dem übergeordneten Projekt</span><span class="sxs-lookup"><span data-stu-id="5837a-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="5837a-156">Sie müssen jetzt das Kundenkonto mit dem übergeordneten Projekt in den Projekteinstellungen in der Anlagenverwaltung verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5837a-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="5837a-157">Gehen Sie zu **Anlagenverwaltung \> Einstellungen \> Arbeitsaufträge \> Projekteinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="5837a-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="5837a-158">Wählen Sie auf der Registerkarte **Übergeordnetes Projekt** die Option **Hinzufügen** aus, um eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5837a-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="5837a-159">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="5837a-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5837a-160">**Kundenkonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="5837a-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="5837a-161">**Projekt-ID:** Geben Sie die Projekt-ID ein, die Sie zuvor notiert haben.</span><span class="sxs-lookup"><span data-stu-id="5837a-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="5837a-162">Schritt 5: Verknüpfen Sie die Projektgruppe und geben Sie sie in das Arbeitsauftragsprojekt ein</span><span class="sxs-lookup"><span data-stu-id="5837a-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="5837a-163">Sie sollten sich immer noch auf der Seite **Projekteinstellungen** befinden (**Anlagenverwaltung \> Einstellungen \> Arbeitsaufträge \> Projekteinstellungen**).</span><span class="sxs-lookup"><span data-stu-id="5837a-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="5837a-164">Wählen Sie auf der Registerkarte **Projektgruppe** die Option **Hinzufügen** aus, um eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5837a-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="5837a-165">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="5837a-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5837a-166">**Arbeitsauftragstyp:** *Service* (der Arbeitsauftragstyp, den Sie zuvor erstellt haben)</span><span class="sxs-lookup"><span data-stu-id="5837a-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="5837a-167">**Projektgruppe:** *TM*</span><span class="sxs-lookup"><span data-stu-id="5837a-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="5837a-168">Der Projektvertrag für das Arbeitsauftragsprojekt wird immer vom übergeordneten Projekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="5837a-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="5837a-169">Schritt 6: Verknüpfen Sie eine Anlage mit der Kunden-ID</span><span class="sxs-lookup"><span data-stu-id="5837a-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="5837a-170">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Aktive Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="5837a-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="5837a-171">Geben Sie im Feld **Filter** *VE-102* ein, und wählen Sie Filtern nach **Anlage** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="5837a-172">Wählen Sie die Anlage aus, um ihre Einstellungen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5837a-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="5837a-173">Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-013* (*Pelican Wholesales*) fest.</span><span class="sxs-lookup"><span data-stu-id="5837a-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="5837a-174">Das Feld **Name** wird automatisch in *Pelikan Wholesales* aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5837a-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="5837a-175">Schritt 7: Erstellen Sie einen neuen Arbeitsauftrag für die Anlage</span><span class="sxs-lookup"><span data-stu-id="5837a-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="5837a-176">Gehen Sie zu **Anlagenverwaltung \> Arbeitsaufträge \> Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="5837a-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="5837a-177">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5837a-178">Legen Sie im Dialogfeld **Arbeitsauftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5837a-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5837a-179">**Arbeitsauftragstyp:** *Service*</span><span class="sxs-lookup"><span data-stu-id="5837a-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="5837a-180">**Beschreibung:** *LKW reparieren*</span><span class="sxs-lookup"><span data-stu-id="5837a-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="5837a-181">**Kundenkonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="5837a-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="5837a-182">**Anlage:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="5837a-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="5837a-183">Die Suche zeigt nur Anlagen an, die mit dem ausgewählten Kundenkonto verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5837a-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="5837a-184">**Wartungsjobtyp:** *Reparatur*</span><span class="sxs-lookup"><span data-stu-id="5837a-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="5837a-185">**Art:** *Mechaniker*</span><span class="sxs-lookup"><span data-stu-id="5837a-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="5837a-186">**Servicelevel:** *4*</span><span class="sxs-lookup"><span data-stu-id="5837a-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="5837a-187">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5837a-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="5837a-188">Schritt 8: Überprüfen Sie den Arbeitsauftrag, und beginnen Sie mit der Arbeit</span><span class="sxs-lookup"><span data-stu-id="5837a-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="5837a-189">In diesem Abschnitt arbeiten Sie an dem Arbeitsauftrag, den Sie im vorherigen Abschnitt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5837a-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="5837a-190">Befolgen Sie diese Schritte, um zu überprüfen, ob das übergeordnete Projekt das Projekt *Arbeitsaufträge von Pelican Wholesales* ist:</span><span class="sxs-lookup"><span data-stu-id="5837a-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="5837a-191">Wählen Sie im Abschnitt **Wartungsaufträge für Arbeitsaufträge** eine Position aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="5837a-192">Überprüfen Sie auf dem Inforegister **Positionsdetails** den Wert **Projekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="5837a-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="5837a-193">Es sollte eine Zahl mit Bindestrich im Format *\<Parent-Project-ID\>-\<Project-ID\>* sein.</span><span class="sxs-lookup"><span data-stu-id="5837a-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="5837a-194">Dieser Wert ist ein Link.</span><span class="sxs-lookup"><span data-stu-id="5837a-194">This value is a link.</span></span>
    1. <span data-ttu-id="5837a-195">Wählen Sie den Projekt-ID-Link aus, um eine Seite zu öffnen, auf der Sie die Namen des übergeordneten Projekts und des Projekts anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="5837a-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="5837a-196">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Lebenszyklusstatus** die Option **Arbeitsauftragsstatus aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="5837a-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="5837a-197">Wählen Sie im Dialogfeld **Arbeitsauftragsstatus aktualisieren** in der Spalte **Auswählen** das Kontrollkästchen für die Zeile, in der das Feld **Lebenszyklusstatus** auf *In Bearbeitung* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5837a-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="5837a-198">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5837a-198">Select **OK**.</span></span>
1. <span data-ttu-id="5837a-199">Wählen Sie im Dialogfeld **Lebenszyklusstatus: In Bearbeitung** **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="5837a-200">Schritt 9: Buchen Sie die Stunden, die für den Arbeitsauftrag aufgewendet wurden, und erstellen Sie einen neuen Rechnungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="5837a-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="5837a-201">In diesem Abschnitt arbeiten Sie an dem Arbeitsauftrag, an dem Sie im vorherigen Abschnitt gearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="5837a-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="5837a-202">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Projekt** auf **Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="5837a-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="5837a-203">Die Seite **Arbeitsauftragserfassungen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5837a-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="5837a-204">Hier können Sie die Zeit registrieren, die Sie für den Arbeitsauftrag aufgewendet haben.</span><span class="sxs-lookup"><span data-stu-id="5837a-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="5837a-205">Wählen Sie auf dem Inforegister **Stunden** die Option **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="5837a-206">Stellen Sie in der neuen Zeile das Feld **Stunden** auf *4* ein.</span><span class="sxs-lookup"><span data-stu-id="5837a-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="5837a-207">Wählen Sie im Aktionsbereich **Erfassungen buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="5837a-208">Schließen Sie die Seite **Arbeitsauftragserfassungen**, um zum Arbeitsauftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5837a-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="5837a-209">Klicken Sie im Aktivitätsbereich auf die Registerkarte **Rechnungsstellung**, und wählen Sie **Neuer Rechnungsvorschlag** aus.</span><span class="sxs-lookup"><span data-stu-id="5837a-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="5837a-210">Aktivieren Sie im Dialogfeld **Rechnungsvorschlag erstellen** im Abschnitt **Projektbuchungen** das Kontrollkästchen **Auswählen** für jede Zeile, die Sie in Rechnung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="5837a-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="5837a-211">Wählen Sie **OK** aus, um das Dialogfeld zu schließen und den neuen Rechnungsvorschlag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5837a-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]