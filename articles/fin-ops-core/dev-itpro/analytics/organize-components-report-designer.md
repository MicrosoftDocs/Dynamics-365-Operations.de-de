---
title: Berichtskomponente im Berichts-Designer organisieren
description: In diesem Thema wird erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b55dcee00f571228ec1e933306d77d9edc12866
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092422"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="3178d-103">Organisieren von Berichtskomponenten im Berichtsdesigner</span><span class="sxs-lookup"><span data-stu-id="3178d-103">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3178d-104">Nachdem Sie Bausteine und generierte Berichte entworfen haben, ist es hilfreich, diese Objekte zu organisieren, sodass sie vom Benutzer leichter gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="3178d-104">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="3178d-105">Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3178d-105">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="3178d-106">Sie können Ordner, Berichte, Bausteine und andere Objekte im Berichtsdesigner umbenennen, um Ihre Dateien besser zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-106">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="3178d-107">Je nach Art des Objekts, das Sie umbenennen, müssen Sie möglicherweise Zuordnungen für das Objekt aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-107">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="3178d-108">Umbenennen eines Ordner oder Bausteins im Berichts-Designer</span><span class="sxs-lookup"><span data-stu-id="3178d-108">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="3178d-109">Im Berichts-Designer können Sie Ordner, Berichtsdefinitionen, Zeilendefinitionen, Spaltendefinitionen und Berichtsbaumstruktur-Definitionen umbenennen.</span><span class="sxs-lookup"><span data-stu-id="3178d-109">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="3178d-110">Umbenennen eines Ordners oder Bausteins im Berichts-Designer</span><span class="sxs-lookup"><span data-stu-id="3178d-110">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="3178d-111">Suchen Sie im Berichts-Designer im Navigationsbereich nach dem umzubenennenden Ordner oder Objekt.</span><span class="sxs-lookup"><span data-stu-id="3178d-111">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="3178d-112">Klicken Sie mit der rechten Maustaste auf den Ordner oder das Objekt, und klicken Sie dann auf **Umbenennen**.</span><span class="sxs-lookup"><span data-stu-id="3178d-112">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="3178d-113">Das Feld **Name** im Navigationsbereich ist nun verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3178d-113">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="3178d-114">Geben Sie einen neuen Namen ein, und drücken Sie die Eingabetaste.</span><span class="sxs-lookup"><span data-stu-id="3178d-114">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="3178d-115">Wenn der Baustein eine Zeilendefinition, eine Spaltendefinition oder eine Berichtstruktur-Definition ist, müssen Sie weitere Bausteine, die dem Artikel zugeordnet sind, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-115">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="3178d-116">Klicken Sie mit der rechten Maustaste auf den Baustein, den Sie in Schritt 3 umbenannt haben, wählen Sie **Zuordnungen**, und wählen Sie dann den Artikel in der Liste, um ihn zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-116">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="3178d-117">Wiederholen Sie Schritt 4, bis alle zugeordneten Artikel aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3178d-117">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="3178d-118">Erstellen und Verwalten von Berichtsgruppen</span><span class="sxs-lookup"><span data-stu-id="3178d-118">Create and manage report groups</span></span>
<span data-ttu-id="3178d-119">Sie können Berichtsdefinitionen gruppieren, um mehrere Berichte gleichzeitig zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-119">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="3178d-120">Zum Erstellen, Ändern, Löschen und Generieren von Berichtsgruppen müssen Sie die Designer- oder Administrator-Rolle haben.</span><span class="sxs-lookup"><span data-stu-id="3178d-120">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="3178d-121">Benutzer mit der Generator-Rolle können Berichtsgruppen generieren und anzeigen und die Benutzerberichtsdefinitions-Einstellungen für Berichtsgruppen ändern.</span><span class="sxs-lookup"><span data-stu-id="3178d-121">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="3178d-122">Erstellen einer Berichtsgruppe</span><span class="sxs-lookup"><span data-stu-id="3178d-122">Create a report group</span></span>

1. <span data-ttu-id="3178d-123">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="3178d-123">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3178d-124">Klicken Sie im Menü **Datei** auf **Neu** &gt; **Berichtsgruppe**, um eine neue Berichtsgruppe im Viewer-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="3178d-124">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="3178d-125">Klicken Sie alternativ auf die Schaltläche **Berichtsgruppe** ![Berichtsgruppe](media/report-group.gif "Berichtsgruppe") auf der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="3178d-125">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="3178d-126">Klicken Sie auf die Registerkarte **Gruppen-Bericht**. Um die Informationen zu den einzelnen Berichtsdefinitionen für die Generierung dieses Berichts zu überschreiben, aktivieren Sie das Kontrollkästchen **Überschreiben von Unternehmen**, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3178d-126">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="3178d-127">Die Felder Unternehmensname, Detailebene, vorläufige Einstellungen und Datumsinformationen werden automatisch ausgefüllt, aber Sie können Aktualisierungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3178d-127">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="3178d-128">Um mehrere Berichte zu generieren, die die Berichtswährung anzeigen, aktivieren Sie das Kontrollkästchen **Alle Berichtswährungen einschließen**.</span><span class="sxs-lookup"><span data-stu-id="3178d-128">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="3178d-129">Es sind mehrere Ansichten verfügbar, wenn Sie den Bericht anzeigen und auf die Schaltfläche **Währung** im Web-Viewer klicken.</span><span class="sxs-lookup"><span data-stu-id="3178d-129">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="3178d-130">Klicken Sie im Feld **Berichte in Gruppe** auf **Hinzufügen**, um die Berichte zu wählen, die in die Berichtsgruppe einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3178d-130">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="3178d-131">Um mehrere Berichte im Dialogfeld **Hinzufügen** auszuwählen, halten Sie STRG-Taste gedrückt, während Sie Berichte auswählen.</span><span class="sxs-lookup"><span data-stu-id="3178d-131">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="3178d-132">Wenn Sie die Berichtsauswahl abgeschlossen haben, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3178d-132">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="3178d-133">Klicken Sie auf **Datei** &gt; **Speichern**, um die neue Berichtsgruppe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3178d-133">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="3178d-134">Ändern einer Berichtsgruppe</span><span class="sxs-lookup"><span data-stu-id="3178d-134">Modify a report group</span></span>

1. <span data-ttu-id="3178d-135">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="3178d-135">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3178d-136">Doppelklicken Sie auf die zu ändernde Berichtsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3178d-136">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="3178d-137">Nehmen Sie auf der Registerkarte **Berichtsgruppe** die gewünschten Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="3178d-137">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="3178d-138">Klicken Sie im Menü **Datei** auf **Speichern**, um die geänderte Berichtsgruppe zu speichern. Alternativ klicken Sie auf die Schaltläche **Speichern** ![Speichern](media/save.gif "Speichern") in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="3178d-138">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="3178d-139">[Hinweis] Wenn Sie geplant haben, Berichte in Zeitabständen zu erstellen, können Sie diese Einstellungen überschreiben und einen Bericht sofort generieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-139">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="3178d-140">Generieren eines Berichtsgruppenberichts</span><span class="sxs-lookup"><span data-stu-id="3178d-140">Generate a report group report</span></span>

1. <span data-ttu-id="3178d-141">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="3178d-141">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3178d-142">Öffnen Sie die zu generierende Berichtsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3178d-142">Open the report group to generate.</span></span>
3. <span data-ttu-id="3178d-143">Klicken Sie auf die Schaltläche **Bericht generieren** ![Bericht generieren](media/generate-report.gif "Bericht generieren"), um Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-143">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="3178d-144">Löschen einer Berichtsgruppe</span><span class="sxs-lookup"><span data-stu-id="3178d-144">Delete a report group</span></span>

1. <span data-ttu-id="3178d-145">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="3178d-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3178d-146">Zum Löschen klicken Sie im Navigationsbereich mit der rechten Maustaste auf die Berichtsgruppe, und wählen Sie dann **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="3178d-146">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="3178d-147">Wenn eine Bestätigungsmeldung angezeigt wird, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3178d-147">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="3178d-148">Berichtsgruppen-Registerkartensteuerelement</span><span class="sxs-lookup"><span data-stu-id="3178d-148">Report Group tab controls</span></span>
<span data-ttu-id="3178d-149">In der folgenden Tabelle werden die Steuerelemente der Registerkarte **Berichtsgruppen** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3178d-149">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3178d-150">Steuerung</span><span class="sxs-lookup"><span data-stu-id="3178d-150">Control</span></span></th>
<th><span data-ttu-id="3178d-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3178d-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3178d-152">Überschreiben von Unternehmen, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="3178d-152">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="3178d-153">Aktivieren Sie dieses Kontrollkästchen, um einzelne Berichtsdefinitionen der Berichte in dieser Berichtsgruppe für die Generierung dieser Berichte zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3178d-153">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-154">Unternehmensname</span><span class="sxs-lookup"><span data-stu-id="3178d-154">Company name</span></span></td>
<td><span data-ttu-id="3178d-155">Wählen Sie das Unternehmen für die Berichte aus.</span><span class="sxs-lookup"><span data-stu-id="3178d-155">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-156">Detailebene</span><span class="sxs-lookup"><span data-stu-id="3178d-156">Detail level</span></span></td>
<td><span data-ttu-id="3178d-157">Spezifizieren Sie die für den Bericht gewünschte Detailstufe.</span><span class="sxs-lookup"><span data-stu-id="3178d-157">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="3178d-158"><strong>Financial</strong> − Ein übergeordneter Zusammenfassungsbericht.</span><span class="sxs-lookup"><span data-stu-id="3178d-158"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="3178d-159">Sie können keine Detailinformationen zu Konten und Dimensionen durchführen, ausgenommen derer, die Sie über die Berichtstruktur hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="3178d-159">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="3178d-160"><strong>Finanzen &amp; Konto</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Kontodetails enthält.</span><span class="sxs-lookup"><span data-stu-id="3178d-160"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="3178d-161"><strong>Finanzen, Konto &amp; Buchung</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Buchungsdetails enthält.</span><span class="sxs-lookup"><span data-stu-id="3178d-161"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-162">Vorläufig</span><span class="sxs-lookup"><span data-stu-id="3178d-162">Provisional</span></span></td>
<td><span data-ttu-id="3178d-163">Spezifizieren Sie die für den Bericht gewünschten Aktivitätstypen.</span><span class="sxs-lookup"><span data-stu-id="3178d-163">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="3178d-164"><strong>Nur gebuchte Aktivität</strong> − Enthält nur die Buchungen und Salden, die in den Finanzdaten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="3178d-164"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="3178d-165"><strong>Gebuchte und nicht gebuchte Aktivität</strong> − Enthält alle Buchungen und Salden, die in den Finanzdaten eingegeben und gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="3178d-165"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="3178d-166"><strong>Nur nicht gebuchte Aktivität</strong> − Enthält nur Buchungen, die in die Finanzdaten eingegeben, aber noch nicht gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="3178d-166"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-167">Alle Berichtswährungen einschließen</span><span class="sxs-lookup"><span data-stu-id="3178d-167">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="3178d-168">Alle zusätzlichen Berichtswährungen, die in Ihrem Microsoft Dynamics ERP-System konfiguriert sind, werden hier aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3178d-168">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="3178d-169">Wählen Sie dieses Kontrollkästchen aus, um zusätzliche Berichte in den angegebenen Währungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3178d-169">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="3178d-170">Sie können dann im Web-Viewer angezeigt werden, indem Sie auf die Schaltfläche <strong>Währung</strong> klicken und eine Währung auswählen.</span><span class="sxs-lookup"><span data-stu-id="3178d-170">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-171">Nicht mit Berichtsdefinition gespeicherte Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="3178d-171">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="3178d-172">Basisperiode</span><span class="sxs-lookup"><span data-stu-id="3178d-172">Base period</span></span></li>
<li><span data-ttu-id="3178d-173">Basisjahr</span><span class="sxs-lookup"><span data-stu-id="3178d-173">Base year</span></span></li>
<li><span data-ttu-id="3178d-174">Berücksichtigter Zeitraum</span><span class="sxs-lookup"><span data-stu-id="3178d-174">Period covered</span></span></li>
</ul>
<span data-ttu-id="3178d-175">Nur Einstellungen zum Standardbasiszeitraum werden mit der Berichtsdefinition gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3178d-175">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-176">Mit Berichtsdefinition gespeicherte Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="3178d-176">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="3178d-177">Berichtsdatum</span><span class="sxs-lookup"><span data-stu-id="3178d-177">Report date</span></span></li>
<li><span data-ttu-id="3178d-178">Standardbasiszeitraum</span><span class="sxs-lookup"><span data-stu-id="3178d-178">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="3178d-179">Berichte in Gruppe</span><span class="sxs-lookup"><span data-stu-id="3178d-179">Reports in group</span></span></td>
<td><span data-ttu-id="3178d-180">Fügen Sie Berichte in der Berichtsgruppe hinzu, entfernen Sie sie aus dieser oder sortieren Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="3178d-180">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="3178d-181">Doppelklicken Sie zum Hinzufügen von Berichtsdefinitionen zur Berichtsgruppe auf die Berichtsgruppe, um sie zu öffnen, und klicken Sie dann auf <strong>Hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="3178d-181">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="3178d-182">Wählen Sie die Berichte aus, die in die Berichtsgruppe eingefügt werden sollen, und klicken Sie dann auf <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="3178d-182">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="3178d-183">Wählen Sie zum Entfernen eines Berichts aus der Berichtsgruppe den Bericht aus, und klicken Sie dann auf <strong>Entfernen</strong>.</span><span class="sxs-lookup"><span data-stu-id="3178d-183">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="3178d-184">Um die Reihenfolge zu ändern, in der die Berichte generiert werden, wählen Sie einen Bericht in der Liste aus, und klicken anschließend auf <strong>Nach oben verschieben</strong> oder <strong>Nach unten verschieben</strong>.</span><span class="sxs-lookup"><span data-stu-id="3178d-184">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="3178d-185">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3178d-185">Additional resources</span></span>

[<span data-ttu-id="3178d-186">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="3178d-186">Financial reporting</span></span>](financial-reporting-intro.md)
