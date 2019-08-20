---
title: Kennzeichenbeschriftungs-Druck aktivieren
description: Durch diese Prozedur wird das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktiviert, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed74806e5e037570f3ed7f59725eed494c829d34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847266"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="ac495-103">Kennzeichenbeschriftungs-Druck aktivieren</span><span class="sxs-lookup"><span data-stu-id="ac495-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac495-104">Durch diese Prozedur wird das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktiviert, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="ac495-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="ac495-105">Sie können diese Prozedur im Demodatunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac495-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="ac495-106">Wenn Sie diese mithilfe Ihrer eigenen Daten ausgeführt haben, müssen Sie einen Nummernkreis für Kennzeichen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="ac495-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="ac495-107">Sie müssen einen Etikettendrucker einrichten, bevor Sie mit dieser Aufgabe beginnen.</span><span class="sxs-lookup"><span data-stu-id="ac495-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="ac495-108">Wechseln Sie zu "Organisationsverwaltung" > "Einrichtung" > "Netzwerkdrucker".</span><span class="sxs-lookup"><span data-stu-id="ac495-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="ac495-109">Klicken Sie im Aktivitätsbereich auf "Optionen" und klicken Sie dann auf die Routing-Agent-Installationsprogrammschaltfläche "Dokument herunterladen".</span><span class="sxs-lookup"><span data-stu-id="ac495-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="ac495-110">Führen Sie das Installationsprogramm aus und überprüfen Sie, ob Sie einen funktionierenden Netzwerkdrucker haben, der auf "Aktiv" festgelegt ist, bevor Sie mit der Prozedur fortfahren.</span><span class="sxs-lookup"><span data-stu-id="ac495-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="ac495-111">Das Präfix des Unternehmens GS1 einrichten</span><span class="sxs-lookup"><span data-stu-id="ac495-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="ac495-112">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".</span><span class="sxs-lookup"><span data-stu-id="ac495-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="ac495-113">Geben Sie im Feld GS1-Unternehmenspräfix die 7 Zahlen für Ihre GS1-Unternehmensnummer ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="ac495-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-114">Click Save.</span></span>
4. <span data-ttu-id="ac495-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="ac495-116">NVE-Kennzeichennummernkreis einrichten</span><span class="sxs-lookup"><span data-stu-id="ac495-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="ac495-117">Wechseln Sie zu "Organisationsverwaltung" > "Nummernkreise" > "Nummernkreise".</span><span class="sxs-lookup"><span data-stu-id="ac495-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="ac495-118">Wählen Sie im Feld "Bereich" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="ac495-119">Wählen Sie im Feld "Referenz" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="ac495-120">Geben Sie im Feld "Unternehmen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="ac495-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ac495-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ac495-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ac495-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ac495-123">Erweitern Sie den Abschnitt "Segmente".</span><span class="sxs-lookup"><span data-stu-id="ac495-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="ac495-124">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="ac495-124">Click Edit.</span></span>
9. <span data-ttu-id="ac495-125">In der Segmenttabelle wählen Sie die erste Zeile aus</span><span class="sxs-lookup"><span data-stu-id="ac495-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="ac495-126">Klicken Sie auf "Entfernen".</span><span class="sxs-lookup"><span data-stu-id="ac495-126">Click Remove.</span></span>
11. <span data-ttu-id="ac495-127">Klicken Sie auf "Entfernen".</span><span class="sxs-lookup"><span data-stu-id="ac495-127">Click Remove.</span></span>
12. <span data-ttu-id="ac495-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-128">Click Save.</span></span>
13. <span data-ttu-id="ac495-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="ac495-130">Erstellen des Dokumentarbeitsplan-Layouts</span><span class="sxs-lookup"><span data-stu-id="ac495-130">Create the document route layout</span></span>
1. <span data-ttu-id="ac495-131">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Dokumentrouting" > "Dokumentroutinglayouts".</span><span class="sxs-lookup"><span data-stu-id="ac495-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="ac495-132">Aktivieren Sie das NVE (SSCC)-Layout.</span><span class="sxs-lookup"><span data-stu-id="ac495-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="ac495-133">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ac495-133">Click New.</span></span>
3. <span data-ttu-id="ac495-134">Geben Sie im Feld "Layoutkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="ac495-135">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ac495-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ac495-137">Klicken Sie "Am Ende des Texts einfügen".</span><span class="sxs-lookup"><span data-stu-id="ac495-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="ac495-138">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-138">Click Save.</span></span>
8. <span data-ttu-id="ac495-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="ac495-140">Das Dokumentrouting einrichten</span><span class="sxs-lookup"><span data-stu-id="ac495-140">Set up the document routing</span></span>
1. <span data-ttu-id="ac495-141">Wechseln Sie zu "Lagerortverwaltung" > "Einrichten" > "Dokumentweiterleitung" > "Dokumentweiterleitung".</span><span class="sxs-lookup"><span data-stu-id="ac495-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="ac495-142">Wählen Sie im Feld "Arbeitsauftragstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="ac495-143">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="ac495-143">Click New.</span></span>
4. <span data-ttu-id="ac495-144">Geben Sie im Feld "Lagerort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="ac495-145">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="ac495-146">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="ac495-146">Click New.</span></span>
7. <span data-ttu-id="ac495-147">Geben Sie im Feld "Layoutkennung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="ac495-148">Geben Sie im Feld "Name" den Druckernamen ein, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ac495-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="ac495-149">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-149">Click Save.</span></span>
10. <span data-ttu-id="ac495-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="ac495-151">Menü für mobile Geräte erstellen</span><span class="sxs-lookup"><span data-stu-id="ac495-151">Create mobile device menu</span></span>
1. <span data-ttu-id="ac495-152">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menüoptionen für mobiles Gerät".</span><span class="sxs-lookup"><span data-stu-id="ac495-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="ac495-153">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ac495-153">Click New.</span></span>
3. <span data-ttu-id="ac495-154">Geben Sie im Feld "Menüoptionsname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="ac495-155">Geben Sie im Feld "Titel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="ac495-156">Wählen Sie im Feld "Modus" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="ac495-157">Wählen Sie "Ja" im Feld "Vorhandene Arbeit verwenden".</span><span class="sxs-lookup"><span data-stu-id="ac495-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="ac495-158">Wählen Sie "Ja" im Feld "Kennzeichen erzeugen" aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="ac495-159">Erweitern Sie den Abschnitt "Arbeitsklassen".</span><span class="sxs-lookup"><span data-stu-id="ac495-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="ac495-160">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ac495-160">Click New.</span></span>
10. <span data-ttu-id="ac495-161">Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ac495-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="ac495-162">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-162">Click Save.</span></span>
12. <span data-ttu-id="ac495-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-163">Close the page.</span></span>
13. <span data-ttu-id="ac495-164">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menü für mobiles Gerät".</span><span class="sxs-lookup"><span data-stu-id="ac495-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="ac495-165">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ac495-166">Wählen Sie in der Struktur "Wählen Sie in der Struktur die Menüoption aus, die Sie zuvor erstellt haben." aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="ac495-167">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac495-167">Click Edit.</span></span>
17. <span data-ttu-id="ac495-168">Klicken Sie auf den Pfeil, um die Menüoption dem Menü hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ac495-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="ac495-169">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-169">Click Save.</span></span>
19. <span data-ttu-id="ac495-170">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="ac495-171">Eine Arbeitsvorlage aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ac495-171">Update a work template</span></span>
1. <span data-ttu-id="ac495-172">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".</span><span class="sxs-lookup"><span data-stu-id="ac495-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="ac495-173">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ac495-174">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="ac495-174">Click Edit.</span></span>
4. <span data-ttu-id="ac495-175">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="ac495-175">Click New.</span></span>
5. <span data-ttu-id="ac495-176">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ac495-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ac495-177">Wählen Sie im Feld "Arbeitstyp" die Option "Drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="ac495-178">Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ac495-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="ac495-179">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ac495-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ac495-180">Klicken Sie auf "Nach oben verschieben".</span><span class="sxs-lookup"><span data-stu-id="ac495-180">Click Move up.</span></span>
10. <span data-ttu-id="ac495-181">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ac495-181">Click Save.</span></span>
11. <span data-ttu-id="ac495-182">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ac495-182">Close the page.</span></span>

