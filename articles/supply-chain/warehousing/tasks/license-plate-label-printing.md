---
title: Kennzeichenbeschriftungs-Druck aktivieren
description: In diesem Thema wird gezeigt, wie Sie das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktivieren, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a608e9a2356f9dd49bbec1bcbe5489af5931d44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830881"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="7f9ea-103">Kennzeichenbeschriftungs-Druck aktivieren</span><span class="sxs-lookup"><span data-stu-id="7f9ea-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f9ea-104">In diesem Thema wird gezeigt, wie Sie das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktivieren, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="7f9ea-105">Sie können diese Prozedur im Demodatunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="7f9ea-106">Wenn Sie diese mithilfe Ihrer eigenen Daten ausgeführt haben, müssen Sie einen Nummernkreis für Kennzeichen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="7f9ea-107">Sie müssen einen Etikettendrucker einrichten, bevor Sie mit dieser Aufgabe beginnen.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="7f9ea-108">Wechseln Sie zu "Organisationsverwaltung" > "Einrichtung" > "Netzwerkdrucker".</span><span class="sxs-lookup"><span data-stu-id="7f9ea-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="7f9ea-109">Klicken Sie im Aktivitätsbereich auf „Optionen“, und klicken Sie dann auf die Routing-Agent-Installationsprogrammschaltfläche „Dokument herunterladen“.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="7f9ea-110">Führen Sie das Installationsprogramm aus und überprüfen Sie, ob Sie einen funktionierenden Netzwerkdrucker haben, der auf "Aktiv" festgelegt ist, bevor Sie mit der Prozedur fortfahren.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="7f9ea-111">Das Präfix des Unternehmens GS1 einrichten</span><span class="sxs-lookup"><span data-stu-id="7f9ea-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="7f9ea-112">Gehen Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Parameter für Lagerortverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="7f9ea-113">Geben Sie im Feld **GS1-Unternehmenspräfix** die 7 Zahlen für Ihre GS1-Unternehmensnummer ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="7f9ea-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-114">Select **Save**.</span></span>
4. <span data-ttu-id="7f9ea-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="7f9ea-116">NVE-Kennzeichennummernkreis einrichten</span><span class="sxs-lookup"><span data-stu-id="7f9ea-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="7f9ea-117">Wechseln Sie zu **Navigationsbereich > Module > Organisationsverwaltung > Nummernkreise > Nummernkreise**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="7f9ea-118">Wählen Sie im Feld **Bereich** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="7f9ea-119">Wählen Sie im Feld **Referenz** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="7f9ea-120">Geben Sie im Feld **Unternehmen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="7f9ea-121">Erweitern Sie den Abschnitt **Segmente**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="7f9ea-122">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-122">Select **Edit**.</span></span>
7. <span data-ttu-id="7f9ea-123">In der Tabelle **Segmente** wählen Sie die erste Zeile aus</span><span class="sxs-lookup"><span data-stu-id="7f9ea-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="7f9ea-124">Wählen Sie **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-124">Select **Remove**.</span></span>
9. <span data-ttu-id="7f9ea-125">Wählen Sie **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-125">Select **Remove**.</span></span>
10. <span data-ttu-id="7f9ea-126">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-126">Select **Save**.</span></span>
11. <span data-ttu-id="7f9ea-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="7f9ea-128">Erstellen des Dokumentarbeitsplan-Layouts</span><span class="sxs-lookup"><span data-stu-id="7f9ea-128">Create the document route layout</span></span>
1. <span data-ttu-id="7f9ea-129">Wechseln Sie zu **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Dokumentrouting > Dokumentroutinglayouts**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="7f9ea-130">Aktivieren Sie das NVE (SSCC)-Layout.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="7f9ea-131">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-131">Select **New**.</span></span>
3. <span data-ttu-id="7f9ea-132">Geben Sie im Feld **Layoutkennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="7f9ea-133">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7f9ea-134">Wählen Sie **Am Ende des Texts einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="7f9ea-135">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-135">Select **Save**.</span></span>
7. <span data-ttu-id="7f9ea-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="7f9ea-137">Das Dokumentrouting einrichten</span><span class="sxs-lookup"><span data-stu-id="7f9ea-137">Set up the document routing</span></span>
1. <span data-ttu-id="7f9ea-138">Wechseln Sie zu **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Dokumentrouting > Dokumentrouting**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="7f9ea-139">Wählen Sie im Feld **Arbeitsauftragstyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="7f9ea-140">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-140">Select **New**.</span></span>
4. <span data-ttu-id="7f9ea-141">Geben Sie im Feld **Lagerort** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="7f9ea-142">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="7f9ea-143">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-143">Select **New**.</span></span>
7. <span data-ttu-id="7f9ea-144">Geben Sie im Feld **Layoutkennung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="7f9ea-145">Geben Sie im Feld **Name** den Druckernamen ein, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="7f9ea-146">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-146">Select **Save**.</span></span>
10. <span data-ttu-id="7f9ea-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="7f9ea-148">Menü für mobile Geräte erstellen</span><span class="sxs-lookup"><span data-stu-id="7f9ea-148">Create mobile device menu</span></span>
1. <span data-ttu-id="7f9ea-149">Gehen Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menüoptionen des mobilen Geräts**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="7f9ea-150">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-150">Select **New**.</span></span>
3. <span data-ttu-id="7f9ea-151">Geben Sie im Feld **Menüoptionsname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="7f9ea-152">Geben Sie im Feld **Titel** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="7f9ea-153">Wählen Sie im Feld **Modus** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="7f9ea-154">Wählen Sie **Ja** im Feld **Vorhandene Arbeit verwenden**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="7f9ea-155">Wählen Sie **Ja** im Feld **Kennzeichen erzeugen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="7f9ea-156">Erweitern Sie den Abschnitt **Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="7f9ea-157">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-157">Select **New**.</span></span>
10. <span data-ttu-id="7f9ea-158">Geben Sie im Feld **Arbeitsklassenkennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="7f9ea-159">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-159">Select **Save**.</span></span>
12. <span data-ttu-id="7f9ea-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-160">Close the page.</span></span>
13. <span data-ttu-id="7f9ea-161">Gehen Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menü des mobilen Geräts**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="7f9ea-162">Wählen Sie in der Struktur das Menüelement aus, das Sie vorher erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="7f9ea-163">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-163">Select **Edit**.</span></span>
16. <span data-ttu-id="7f9ea-164">Klicken Sie auf den Pfeil, um das Menüelement dem Menü hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="7f9ea-165">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-165">Select **Save**.</span></span>
18. <span data-ttu-id="7f9ea-166">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="7f9ea-167">Eine Arbeitsvorlage aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7f9ea-167">Update a work template</span></span>
1. <span data-ttu-id="7f9ea-168">Wechseln Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Arbeit > Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="7f9ea-169">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-169">Select **Edit**.</span></span>
3. <span data-ttu-id="7f9ea-170">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-170">Select **New**.</span></span>
4. <span data-ttu-id="7f9ea-171">Wählen Sie im Feld **Arbeitstyp** die Option **Drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="7f9ea-172">Geben Sie im Feld **Arbeitsklassenkennung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="7f9ea-173">Wählen Sie **Nach oben**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-173">Select **Move up**.</span></span>
7. <span data-ttu-id="7f9ea-174">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-174">Select **Save**.</span></span>
8. <span data-ttu-id="7f9ea-175">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f9ea-175">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]