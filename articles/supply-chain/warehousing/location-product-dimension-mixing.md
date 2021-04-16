---
title: Lagerplatz-Produktdimensionsmischung
description: Dieses Thema enthält Informationen zur Lagerplatz-Produktdimensionsmischung. Diese Lagerplatzprofilfunktion hilft bei der Verbesserung der Standortverwaltung, wenn Produktvarianten oder Produkte mit Dimensionen verwendet werden, z. B. in der Modebranche. Hier können Sie entscheiden, ob Konfigurationen, Farben, Stile und Größen für ein bestimmtes Lagerplatzprofil gemischt werden können oder ob nur eine dieser Dimensionen oder eine Kombination davon an demselben Lagerplatz platziert werden kann.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 28f59052a74b6d8b263c7a8a8b6061f2c4b34c89
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831289"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="c091c-105">Lagerplatz-Produktdimensionsmischung</span><span class="sxs-lookup"><span data-stu-id="c091c-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c091c-106">Die Lagerplatz-Produktdimensionsmischung ist eine Lagerplatzprofilfunktion, die bei der Verbesserung der Standortverwaltung hilft, wenn Produktvarianten oder Produkte mit Dimensionen verwendet werden, z. B. in der Modebranche.</span><span class="sxs-lookup"><span data-stu-id="c091c-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="c091c-107">Hier können Sie entscheiden, ob Konfigurationen, Farben, Stile und Größen für ein bestimmtes Lagerplatzprofil gemischt werden können oder ob nur eine dieser Dimensionen oder eine Kombination davon an demselben Lagerplatz platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c091c-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="c091c-108">Funktion für Lagerplatz-Produktdimensionsmischung aktivieren</span><span class="sxs-lookup"><span data-stu-id="c091c-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="c091c-109">Bevor Sie die Lagerplatz-Produktdimensionsmischung verwenden können, muss die Funktion in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c091c-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="c091c-110">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c091c-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c091c-111">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="c091c-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c091c-112">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="c091c-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c091c-113">**Funktionsname:** *Lagerplatz-Produktdimensionsmischung*</span><span class="sxs-lookup"><span data-stu-id="c091c-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="c091c-114">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c091c-114">Setup</span></span>

<span data-ttu-id="c091c-115">Jedem Standort im Lagerort muss ein Lagerplatzprofil zugeordnet sein, das die Eigenschaften des Lagerplatzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c091c-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="c091c-116">Daher können alle Standorte, die dasselbe Lagerplatzprofil verwenden, die Produktdimensionsmischung nach dem Einrichten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c091c-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="c091c-117">Lagerplatzprofile konfigurieren, um Produktdimensionsmischung zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="c091c-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="c091c-118">Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="c091c-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="c091c-119">Wählen Sie in der Liste der Lagerplatzprofile **BULK** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="c091c-120">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c091c-121">Legen Sie im Inforegister **Allgemein** die Option **Spezifische Lagerplatz-Produktdimensionsmischung aktivieren** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="c091c-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c091c-122">Sie können diese Option nur dann auf *Ja* festlegen, wenn die Option **Gemischte Artikel zulassen** auf *Nein* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c091c-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="c091c-123">Legen Sie im Inforegister **Produktdimensionsmischung zulässig** die Option **Größe** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="c091c-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="c091c-124">In dem in diesem Thema beschriebenen Szenario kann das Mischen nur für Produkte mit unterschiedlichen Dimensionen der **Größe** durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c091c-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="c091c-125">Es stehen jedoch auch andere Optionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c091c-125">However, other options are also available.</span></span>
1. <span data-ttu-id="c091c-126">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="c091c-127">Einen neuen Produktmaster und Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="c091c-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="c091c-128">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**.</span><span class="sxs-lookup"><span data-stu-id="c091c-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="c091c-129">Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Produktmaster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c091c-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="c091c-130">Legen Sie im Dialogfeld **Neues Produkt** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c091c-131">**Produkttyp:** *Artikel*</span><span class="sxs-lookup"><span data-stu-id="c091c-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="c091c-132">**Produktuntertyp:** *Produktmaster*</span><span class="sxs-lookup"><span data-stu-id="c091c-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="c091c-133">**Produktnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="c091c-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="c091c-134">**Produktname:** *B0001 Größe*</span><span class="sxs-lookup"><span data-stu-id="c091c-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="c091c-135">**Produktdimensionsgruppe:** *Größe*</span><span class="sxs-lookup"><span data-stu-id="c091c-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="c091c-136">**Konfigurationstechnologie:** *Vordefinierte Variante*</span><span class="sxs-lookup"><span data-stu-id="c091c-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="c091c-137">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c091c-137">Select **OK**.</span></span>
1. <span data-ttu-id="c091c-138">Legen Sie auf der Seite **Produktdetails** im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c091c-139">**Varianten automatisch generieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="c091c-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="c091c-140">**Größengruppe:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="c091c-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="c091c-141">Um die vordefinierten Varianten anzuzeigen, wählen Sie im Aktivitätsbereich die Option **Produktvarianten** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="c091c-142">Die Seite **Produktvarianten** erscheint und zeigt eine Liste von Varianten aus der Konfiguration der Größengruppe.</span><span class="sxs-lookup"><span data-stu-id="c091c-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="c091c-143">Produkte für USMF-Unternehmen freigeben</span><span class="sxs-lookup"><span data-stu-id="c091c-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="c091c-144">Wählen Sie im Aktivitätsbereich **Produkte freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="c091c-145">Bestätigen Sie auf der Seite **Produkte zum Freigeben auswählen**, dass die Produktnummer *B0001* in der Liste ist, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="c091c-146">Wählen Sie **Weiter** aus, um die freizugebenden Produktvarianten zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c091c-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="c091c-147">Wählen Sie auf der Seite **Unternehmen für die Freigabe auswählen** die Option *USMF* und dann **Weiter** aus, um die Auswahl zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c091c-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="c091c-148">Wählen Sie auf der Seite **Auswahl bestätigen** die Option **Fertig** aus, um die Veröffentlichung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c091c-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="c091c-149">Sie erhalten die Nachricht „Vorgang abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="c091c-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="c091c-150">Freigegebenes Produkt in USMF-Unternehmen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c091c-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="c091c-151">Stellen Sie sicher, dass Sie beim **USMF**-Unternehmen angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="c091c-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="c091c-152">Gehen Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**, um die Erstellung des freigegebenen Produkts abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c091c-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="c091c-153">Suchen und wählen Sie die Artikelnummer *B0001* aus, um die Seite **Details für freigegebene Produkte** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c091c-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="c091c-154">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c091c-155">Stellen Sie im Inforegister **Allgemein** sicher, dass das Feld **Artikelmodellgruppe** auf *FIFO* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c091c-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="c091c-156">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Dimensionsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="c091c-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="c091c-157">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-157">Set the following values:</span></span>

    - <span data-ttu-id="c091c-158">**Lagerdimensionsgruppe:** *Lagerort*</span><span class="sxs-lookup"><span data-stu-id="c091c-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="c091c-159">**Rückverfolgungsangabengruppe:** *Keine*</span><span class="sxs-lookup"><span data-stu-id="c091c-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="c091c-160">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c091c-160">Select **OK**.</span></span>
1. <span data-ttu-id="c091c-161">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Reservierungshierarchie**.</span><span class="sxs-lookup"><span data-stu-id="c091c-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="c091c-162">Legen Sie das Feld **Reservierungshierarchie** auf *Standard* fest, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="c091c-163">Im Inforegister **Allgemein** im Abschnitt **Verwaltung** sehen Sie, dass Ihre Auswahl aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c091c-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="c091c-164">Geben Sie im Inforegister **Kauf** im Feld **Preis** den Wert *10* ein.</span><span class="sxs-lookup"><span data-stu-id="c091c-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="c091c-165">Geben Sie im Inforegister **Kosten verwalten** im Feld **Artikelgruppe** die Zeichenfolge *Audio* ein.</span><span class="sxs-lookup"><span data-stu-id="c091c-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="c091c-166">Geben Sie im Inforegister **Kauf** im Feld **Preis** den Wert *10* ein.</span><span class="sxs-lookup"><span data-stu-id="c091c-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="c091c-167">Geben Sie im Inforegister **Lagerort** im Feld **Einheitensequenzgruppen-ID** die Zeichenfolge *ea* ein.</span><span class="sxs-lookup"><span data-stu-id="c091c-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="c091c-168">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="c091c-169">Erstellen einer Lagerplatzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c091c-169">Create a location directive</span></span>

1. <span data-ttu-id="c091c-170">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="c091c-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c091c-171">Wählen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Bestellungen* aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="c091c-172">Wählen Sie in der Liste die Lagerplatzrichtlinie namens *24 PO Direkt* aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="c091c-173">Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c091c-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="c091c-174">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c091c-175">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="c091c-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="c091c-176">Die neue Position sollte sich vor der zuvor vorhandenen Position befinden.</span><span class="sxs-lookup"><span data-stu-id="c091c-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="c091c-177">Um die Änderung vorzunehmen, verwenden Sie die Schaltflächen **Nach oben** und **Nach unten** in der Symbolleiste, oder ändern Sie den Wert der **Sequenznummer** der vorhandenen Position zu *2*.</span><span class="sxs-lookup"><span data-stu-id="c091c-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="c091c-178">**Name:** *In BULK-Lagerplatzprofil einlagern*</span><span class="sxs-lookup"><span data-stu-id="c091c-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="c091c-179">**Feste Standortnutzung:** *Feste und nicht feste Lagerplätze*</span><span class="sxs-lookup"><span data-stu-id="c091c-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="c091c-180">**Negativen Lagerbestand zulassen:** *Kontrollkästchen deaktivieren (=Nein)*</span><span class="sxs-lookup"><span data-stu-id="c091c-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="c091c-181">**Charge aktiviert:** *Kontrollkästchen deaktivieren (=Nein)*</span><span class="sxs-lookup"><span data-stu-id="c091c-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="c091c-182">**Strategie:** *Keine*</span><span class="sxs-lookup"><span data-stu-id="c091c-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="c091c-183">Wählen Sie **Abfrage bearbeiten** über dem Gitter aus, während die neue Position noch ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c091c-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="c091c-184">Wählen Sie im Abfragedialogfeld auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c091c-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="c091c-185">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c091c-186">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="c091c-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="c091c-187">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="c091c-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="c091c-188">**Feld:** *Lagerortprofilkennung*</span><span class="sxs-lookup"><span data-stu-id="c091c-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="c091c-189">**Kriterien:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="c091c-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="c091c-190">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c091c-190">Select **OK**.</span></span>
1. <span data-ttu-id="c091c-191">Wählen Sie auf der Seite **Lagerplatzrichtlinien** im Aktivitätsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="c091c-192">Wenn Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** im Feld **Strategie** die Standortstrategie *Konsolidieren* verwenden, wird die Einrichtung des Inforegisters **Produktdimensionsmischung zulässig** in den **Lagerplatzprofilen** überschrieben, und Artikel werden an denselben Lagerplatz verschoben, auch wenn dieses Verhalten von der Einrichtung nicht zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="c091c-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="c091c-193">Erstellen eines Menüelements für ein mobiles Geräts</span><span class="sxs-lookup"><span data-stu-id="c091c-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="c091c-194">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="c091c-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c091c-195">Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt zum Sortieren zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c091c-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="c091c-196">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="c091c-197">**Name des Menüpunkts:** *PO-Positionsempfang*</span><span class="sxs-lookup"><span data-stu-id="c091c-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="c091c-198">**Titel:** *PO-Positionsempfang*</span><span class="sxs-lookup"><span data-stu-id="c091c-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="c091c-199">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="c091c-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c091c-200">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="c091c-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c091c-201">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c091c-202">**Arbeitserstellungsprozess:** *Bestellungspositionsempfang und Einlagerung*</span><span class="sxs-lookup"><span data-stu-id="c091c-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="c091c-203">**Kennzeichen generieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="c091c-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="c091c-204">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="c091c-205">Menü des mobilen Geräts konfigurieren</span><span class="sxs-lookup"><span data-stu-id="c091c-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="c091c-206">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="c091c-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c091c-207">Wählen Sie in der Liste der Menüs **Eingehend** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="c091c-208">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c091c-209">Suchen und wählen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den Menüpunkt **PO-Positionsempfang** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="c091c-210">Wählen Sie die Schaltfläche mit dem Pfeil nach Rechts aus, um den Menüpunkt **PO-Positionsempfang** in die Liste **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="c091c-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="c091c-211">Auf diese Weise fügen Sie dem ausgewählten Menü Ihren neuen Menüpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c091c-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="c091c-212">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="c091c-213">Szenario</span><span class="sxs-lookup"><span data-stu-id="c091c-213">Scenario</span></span>

<span data-ttu-id="c091c-214">Dieses Demoszenario zeigt, wie zwei verschiedene Produktvarianten an denselben Lagerplatz platziert werden können, wenn das Lagerplatzprofil keine gemischten Artikel zulässt, aber die Funktion *Lagerplatz-Produktdimensionsmischung* aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c091c-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="c091c-215">In diesem Fall verwenden Sie die Variante **Größe** als Kriterium.</span><span class="sxs-lookup"><span data-stu-id="c091c-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="c091c-216">Bevor Sie beginnen, stellen Sie sicher, dass sich im Lagerort *24* leere Lagerplätze befinden, die das *BULK*-Lagerplatzprofil verwenden.</span><span class="sxs-lookup"><span data-stu-id="c091c-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="c091c-217">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="c091c-217">Create a purchase order</span></span>

<span data-ttu-id="c091c-218">Sie erstellen eine Bestellung mit drei Positionen: zwei Positionen für dieselbe Produktnummer, jedoch unterschiedliche **Größe**-Varianten und eine dritte Position für ein anderes Produkt ohne Varianten.</span><span class="sxs-lookup"><span data-stu-id="c091c-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="c091c-219">Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="c091c-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="c091c-220">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c091c-221">Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c091c-222">**Kreditorenkonto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="c091c-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="c091c-223">**Lagerort:** *24*</span><span class="sxs-lookup"><span data-stu-id="c091c-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="c091c-224">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c091c-224">Select **OK**.</span></span>
1. <span data-ttu-id="c091c-225">Die Bestellung wird erstellt und im Inforegister **Bestellpositionen** wird eine neue Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c091c-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="c091c-226">Notieren Sie sich die Bestellnummer.</span><span class="sxs-lookup"><span data-stu-id="c091c-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="c091c-227">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c091c-228">**Artikelnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="c091c-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="c091c-229">**Größe** *L*</span><span class="sxs-lookup"><span data-stu-id="c091c-229">**Size** *L*</span></span>
    - <span data-ttu-id="c091c-230">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="c091c-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="c091c-231">Wählen Sie **Position hinzufügen** über dem Raster aus, um eine zweite Bestellposition hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="c091c-232">**Artikelnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="c091c-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="c091c-233">**Größe** *XL*</span><span class="sxs-lookup"><span data-stu-id="c091c-233">**Size** *XL*</span></span>
    - <span data-ttu-id="c091c-234">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="c091c-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="c091c-235">Wählen Sie **Position hinzufügen** aus, um eine dritte Bestellposition hinzuzufügen, und legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c091c-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="c091c-236">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="c091c-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="c091c-237">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="c091c-237">**Quantity:** *1*</span></span>

<span data-ttu-id="c091c-238">1. Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c091c-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="c091c-239">Bestellpositionen in der Warehouse Management Mobile App erhalten</span><span class="sxs-lookup"><span data-stu-id="c091c-239">Receive purchase order lines in the Warehouse Management mobile app</span></span>

1. <span data-ttu-id="c091c-240">Melden Sie sich bei der Warehouse Management Mobile App als Benutzer an, der für den Lagerort *24* aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c091c-240">Sign in to the Warehouse Management mobile app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="c091c-241">Wählen Sie das Menü **Eingehend**.</span><span class="sxs-lookup"><span data-stu-id="c091c-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="c091c-242">Wählen Sie **PO-Positionsempfang**.</span><span class="sxs-lookup"><span data-stu-id="c091c-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="c091c-243">Wählen Sie das Feld **PONUM**, und geben Sie dann die Bestellnummer ein.</span><span class="sxs-lookup"><span data-stu-id="c091c-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="c091c-244">Bestätigen Sie Ihre Eingabe, indem Sie auf die Schaltfläche zum Bestätigen (✔) unten auf der Seite klicken.</span><span class="sxs-lookup"><span data-stu-id="c091c-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="c091c-245">Geben Sie die Positionsnummer aus der Bestellung ein, die eingeht.</span><span class="sxs-lookup"><span data-stu-id="c091c-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="c091c-246">Wählen Sie das Feld **LINENUM**, und verwenden Sie dann das Nummernpad, um *1* einzugeben.</span><span class="sxs-lookup"><span data-stu-id="c091c-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="c091c-247">Bestätigen Sie Ihre Eingabe.</span><span class="sxs-lookup"><span data-stu-id="c091c-247">Confirm your entry.</span></span>
1. <span data-ttu-id="c091c-248">Geben Sie die zu empfangende Menge ein.</span><span class="sxs-lookup"><span data-stu-id="c091c-248">Enter the quantity to receive.</span></span> <span data-ttu-id="c091c-249">Wählen Sie zweimal das Pluszeichen (**+**) aus, um den Wert im Feld **Menge** auf *2* zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="c091c-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="c091c-250">Registrieren Sie Ihren Eintrag, indem Sie auf die Schaltfläche (✔) unten auf der Seite klicken, und bestätigen Sie Ihre Eingabe, indem Sie erneut auf die Schaltfläche (✔) klicken.</span><span class="sxs-lookup"><span data-stu-id="c091c-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="c091c-251">Zeigen Sie die Informationen auf der Seite **Bestellungen: Einlagern** an.</span><span class="sxs-lookup"><span data-stu-id="c091c-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="c091c-252">Diese Seite zeigt die Arbeit, die für die Einlagerung erstellt wurde (Arbeit 1).</span><span class="sxs-lookup"><span data-stu-id="c091c-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="c091c-253">Der Lagerplatz, an dem der empfangene Artikel weggelegt wird, das Kennzeichen, der Artikel, die Größe und die Menge der gerade erledigten Aufgabe **PO-Positionsempfang** werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c091c-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="c091c-254">Bestätigen Sie die Einlagerungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c091c-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="c091c-255">Wiederholen Sie die Schritte 4 bis 11 für die Bestellposition 2.</span><span class="sxs-lookup"><span data-stu-id="c091c-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="c091c-256">Geben Sie in Schritt 8 jedoch eine Menge von *1* an.</span><span class="sxs-lookup"><span data-stu-id="c091c-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="c091c-257">Neue Einlagerungsarbeiten (Arbeit 2) werden an demselben Lagerplatz wie Arbeit 1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="c091c-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="c091c-258">Wiederholen Sie erneut die Schritte 4 bis 11 für die Bestellposition 2.</span><span class="sxs-lookup"><span data-stu-id="c091c-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="c091c-259">Geben Sie in Schritt 8 die verbleibende Menge von *1* an.</span><span class="sxs-lookup"><span data-stu-id="c091c-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="c091c-260">Neue Einlagerungsarbeiten (Arbeit 3) werden an demselben Lagerplatz wie Arbeit 1 und Arbeit 2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="c091c-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="c091c-261">Dieses Verhalten tritt auf, weil die Lagerplatzrichtlinienstrategie *Konsolidieren* verwendet wird, und die Einrichtung im Inforegister **Produktdimensionsmischung zulässig** in den **Lagerplatzprofilen** *Bulk* ermöglicht die **Größe**-Variante, die an einem Lagerplatzprofil gemischt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c091c-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="c091c-262">Wiederholen Sie die Schritte 4 bis 11 für die Bestellposition 3.</span><span class="sxs-lookup"><span data-stu-id="c091c-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="c091c-263">Geben Sie in Schritt 8 eine Menge von *1* für Artikelnummer *A0001* an.</span><span class="sxs-lookup"><span data-stu-id="c091c-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="c091c-264">Neue Einlagerungsarbeiten (Arbeit 4) werden für einen anderen Lagerplatz als den erstellt, der für die Bestellpositionen 1 und 2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c091c-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="c091c-265">Dieses Verhalten tritt auf, weil das Lagerplatzprofil keine gemischten Produkte zulässt, jedoch gemischte Dimensionen desselben Produktmasters.</span><span class="sxs-lookup"><span data-stu-id="c091c-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="c091c-266">Wählen Sie die Menüschaltfläche oben auf der Seite (manchmal auch als Hamburger oder Hamburgerschaltfläche bezeichnet) und dann **Abbrechen** aus, um **PO-Positionsempfang** zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c091c-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="c091c-267">Sie können dieses Szenario wiederholen, diesmal jedoch **Größe** - *Nein* im Inforegister **Produktdimensionsmischung zulassen** in den **Lagerplatzprofilen** *BULK* festlegen, sodass keine der Produktdimensionen gemischt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c091c-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="c091c-268">In diesem Fall wird bei Erhalt der Bestellung jede Produktvariante an einen neuen Lagerplatz verschoben.</span><span class="sxs-lookup"><span data-stu-id="c091c-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]