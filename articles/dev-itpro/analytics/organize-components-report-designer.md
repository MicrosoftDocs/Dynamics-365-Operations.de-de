---
title: Organisieren von Berichtskomponenten im Berichtsdesigner
description: "Nachdem Sie Bausteine und generierte Berichte entworfen haben, ist es hilfreich, diese Objekte zu organisieren, sodass sie vom Benutzer leichter gefunden werden können. Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fade9e2acdb94daa6a908d949c578fd7ed439882
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="79d37-104">Organisieren von Berichtskomponenten im Berichtsdesigner</span><span class="sxs-lookup"><span data-stu-id="79d37-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="79d37-105">Nachdem Sie Bausteine und generierte Berichte entworfen haben, ist es hilfreich, diese Objekte zu organisieren, sodass sie vom Benutzer leichter gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="79d37-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="79d37-106">Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="79d37-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="79d37-107">Sie können Ordner, Berichte, Bausteine und andere Objekte im Berichtsdesigner umbenennen, um Ihre Dateien besser zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="79d37-108">Je nach Art des Objekts, das Sie umbenennen, müssen Sie möglicherweise Zuordnungen für das Objekt aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="79d37-109">Umbenennen eines Ordner oder Bausteins im Berichts-Designer</span><span class="sxs-lookup"><span data-stu-id="79d37-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="79d37-110">Im Berichts-Designer können Sie Ordner, Berichtsdefinitionen, Zeilendefinitionen, Spaltendefinitionen und Berichtsbaumstruktur-Definitionen umbenennen.</span><span class="sxs-lookup"><span data-stu-id="79d37-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="79d37-111">**Hinweis:** Beim Umbenennen eines Bausteins müssen Sie alle Berichtsdefinitionen, die in dem Baustein verwendet werden, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="79d37-112">Andernfalls kann kein neuer Bericht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="79d37-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="79d37-113">Umbenennen eines Ordner oder Bausteins im Berichts-Designer</span><span class="sxs-lookup"><span data-stu-id="79d37-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="79d37-114">Im Berichts-Designer verwenden Sie den Navigationsbereich, um den Ordner oder das Objekt zu suchen, den bzw. das Sie umbenennen möchten.</span><span class="sxs-lookup"><span data-stu-id="79d37-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="79d37-115">Klicken Sie mit der rechten Maustaste auf den Ordner oder das Objekt, und klicken Sie dann auf **Umbenennen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="79d37-116">Das Feld **Name** im Navigationsbereich ist nun verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79d37-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="79d37-117">Geben Sie einen neuen Namen ein, und drücken Sie die Eingabetaste.</span><span class="sxs-lookup"><span data-stu-id="79d37-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="79d37-118">Wenn der Baustein eine Zeilendefinition, eine Spaltendefinition oder eine Berichtstruktur-Definition ist, müssen Sie weitere Bausteine, die dem Artikel zugeordnet sind, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="79d37-119">Klicken Sie mit der rechten Maustaste auf den Baustein, den Sie in Schritt 3 umbenannt haben, wählen Sie **Zuordnungen**, und wählen Sie dann den Artikel in der Liste, um ihn zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="79d37-120">Wiederholen Sie Schritt 4, bis alle zugeordneten Artikel aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="79d37-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="79d37-121">Erstellen und Verwalten von Berichtsgruppen</span><span class="sxs-lookup"><span data-stu-id="79d37-121">Create and manage report groups</span></span>
<span data-ttu-id="79d37-122">Sie können Berichtsdefinitionen gruppieren, um mehrere Berichte gleichzeitig zu generieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="79d37-123">Zum Erstellen, Ändern, Löschen und Generieren von Berichtsgruppen müssen Sie die Designer- oder Administrator-Rolle haben.</span><span class="sxs-lookup"><span data-stu-id="79d37-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="79d37-124">Benutzer mit der Generator-Rolle können Berichtsgruppen generieren und anzeigen und die Benutzerberichtsdefinitions-Einstellungen für Berichtsgruppen ändern.</span><span class="sxs-lookup"><span data-stu-id="79d37-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="79d37-125">Erstellen einer Berichtsgruppe</span><span class="sxs-lookup"><span data-stu-id="79d37-125">Create a report group</span></span>

1.  <span data-ttu-id="79d37-126">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="79d37-127">Klicken Sie im Menü **Datei** auf **Neu** &gt; **Berichtsgruppe**, um eine neue Berichtsgruppe im Viewer-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="79d37-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="79d37-128">Klicken Sie alternativ auf die **Berichtsgruppe** -Schaltfläche ![Berichtsgruppe](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Berichtsgruppe") auf der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="79d37-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="79d37-129">Klicken Sie auf die Registerkarte **Berichtsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="79d37-129">Click the **Report Group** tab.</span></span> <span data-ttu-id="79d37-130">Um die Informationen zu den einzelnen Berichtsdefinitionen für die Generierung dieses Berichts zu überschreiben, aktivieren Sie das Kontrollkästchen **Überschreiben von Unternehmen, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-130">To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="79d37-131">Die Felder Unternehmensname, Detailebene, vorläufige Einstellungen und Datumsinformationen werden automatisch ausgefüllt, aber Sie können Aktualisierungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="79d37-131">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="79d37-132">Um mehrere Berichte zu generieren, die die Berichtswährung anzeigen, aktivieren Sie das Kontrollkästchen **Alle Berichtswährungen einschließen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-132">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="79d37-133">Es sind mehrere Ansichten verfügbar, wenn Sie den Bericht anzeigen und auf die Schaltfläche **Währung** im Web-Viewer klicken.</span><span class="sxs-lookup"><span data-stu-id="79d37-133">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="79d37-134">Klicken Sie im Feld **Berichte in Gruppe** auf **Hinzufügen**, um die Berichte zu wählen, die in die Berichtsgruppe einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79d37-134">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="79d37-135">Um mehrere Berichte im Dialogfeld **Hinzufügen** auszuwählen, halten Sie STRG-Taste gedrückt, während Sie Berichte auswählen.</span><span class="sxs-lookup"><span data-stu-id="79d37-135">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="79d37-136">Wenn Sie die Berichtsauswahl abgeschlossen haben, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="79d37-136">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="79d37-137">Klicken Sie auf **Datei** &gt; **Speichern**, um die neue Berichtsgruppe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="79d37-137">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="79d37-138">Ändern einer Berichtsgruppe</span><span class="sxs-lookup"><span data-stu-id="79d37-138">Modify a report group</span></span>

1.  <span data-ttu-id="79d37-139">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-139">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="79d37-140">Doppelklicken Sie auf die zu ändernde Berichtsgruppe.</span><span class="sxs-lookup"><span data-stu-id="79d37-140">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="79d37-141">Nehmen Sie auf der Registerkarte **Berichtsgruppe** die gewünschten Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="79d37-141">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="79d37-142">Klicken Sie im Menü **Datei** auf **Speichern**, um die geänderte Berichtsgruppe zu speichern. Alternativ klicken Sie auf die **Speichern**-Schaltfläche ![Speichern](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Speichern") in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="79d37-142">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="79d37-143">**Hinweis:** Wenn Sie geplant haben, Berichte in Zeitabständen zu erstellen, können Sie diese Einstellungen überschreiben und einen Bericht sofort generieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-143">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="79d37-144">Generieren eines Berichtsgruppenberichts</span><span class="sxs-lookup"><span data-stu-id="79d37-144">Generate a report group report</span></span>

1.  <span data-ttu-id="79d37-145">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="79d37-146">Öffnen Sie die zu generierende Berichtsgruppe.</span><span class="sxs-lookup"><span data-stu-id="79d37-146">Open the report group to generate.</span></span>
3.  <span data-ttu-id="79d37-147">Klicken Sie auf die **Bericht generieren** -Schaltfläche ![Bericht generieren](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Bericht generieren") zum Generieren von Berichten.</span><span class="sxs-lookup"><span data-stu-id="79d37-147">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="79d37-148">Löschen einer Berichtsgruppe</span><span class="sxs-lookup"><span data-stu-id="79d37-148">Delete a report group</span></span>

1.  <span data-ttu-id="79d37-149">Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="79d37-149">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="79d37-150">Zum Löschen klicken Sie im Navigationsbereich mit der rechten Maustaste auf die Berichtsgruppe, und wählen Sie dann **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="79d37-150">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="79d37-151">Wenn eine Bestätigungsmeldung angezeigt wird, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="79d37-151">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="79d37-152">Berichtsgruppen-Registerkartensteuerelement</span><span class="sxs-lookup"><span data-stu-id="79d37-152">Report Group tab controls</span></span>
<span data-ttu-id="79d37-153">In der folgenden Tabelle werden die Steuerelemente der Registerkarte **Berichtsgruppen** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="79d37-153">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79d37-154">Steuerung</span><span class="sxs-lookup"><span data-stu-id="79d37-154">Control</span></span></th>
<th><span data-ttu-id="79d37-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79d37-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79d37-156">Überschreiben von Unternehmen, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="79d37-156">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="79d37-157">Aktivieren Sie dieses Kontrollkästchen, um einzelne Berichtsdefinitionen der Berichte in dieser Berichtsgruppe für die Generierung dieser Berichte zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="79d37-157">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79d37-158">Unternehmensname</span><span class="sxs-lookup"><span data-stu-id="79d37-158">Company name</span></span></td>
<td><span data-ttu-id="79d37-159">Wählen Sie das Unternehmen für die Berichte aus.</span><span class="sxs-lookup"><span data-stu-id="79d37-159">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79d37-160">Detailebene</span><span class="sxs-lookup"><span data-stu-id="79d37-160">Detail level</span></span></td>
<td><span data-ttu-id="79d37-161">Spezifizieren Sie die für den Bericht gewünschte Detailstufe.</span><span class="sxs-lookup"><span data-stu-id="79d37-161">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="79d37-162"><strong>Finanzen</strong>− Eine Zusammenfassung auf hoher Ebene.</span><span class="sxs-lookup"><span data-stu-id="79d37-162"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="79d37-163">Sie können keine Detailinformationen zu Konten und Dimensionen durchführen, ausgenommen derer, die Sie über die Berichtstruktur hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="79d37-163">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="79d37-164"><strong>Finanzen &amp; Konto</strong>− Ein Bericht, der eine übergeordnete Zusammenfassung und Kontodetails enthält.</span><span class="sxs-lookup"><span data-stu-id="79d37-164"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="79d37-165"><strong>Finanzen, Konto &amp; Buchung</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Buchungsdetails enthält.</span><span class="sxs-lookup"><span data-stu-id="79d37-165"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79d37-166">Vorläufig</span><span class="sxs-lookup"><span data-stu-id="79d37-166">Provisional</span></span></td>
<td><span data-ttu-id="79d37-167">Spezifizieren Sie die für den Bericht gewünschten Aktivitätstypen.</span><span class="sxs-lookup"><span data-stu-id="79d37-167">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="79d37-168"><strong>Nur gebuchte Aktivität</strong> − Umfasst nur die Buchungen und Salden, die in den Finanzdaten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="79d37-168"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="79d37-169"><strong>Gebuchte und nicht gebuchte Aktivität</strong> − Umfasst alle Buchungen und Salden, die in den Finanzdaten eingegeben und gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="79d37-169"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="79d37-170"><strong>Nur nicht gebuchte Aktivität</strong> − Umfasst nur die Buchungen, die in den Finanzdaten eingegeben aber noch nicht gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="79d37-170"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79d37-171">Alle Berichtswährungen einschließen</span><span class="sxs-lookup"><span data-stu-id="79d37-171">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="79d37-172">Alle zusätzlichen Berichtswährungen, die in Ihrem Microsoft Dynamics ERP-System konfiguriert sind, werden hier aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="79d37-172">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="79d37-173">Wählen Sie dieses Kontrollkästchen aus, um zusätzliche Berichte in den angegebenen Währungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="79d37-173">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="79d37-174">Um diese Berichte im Web-Viewer anzuzeigen, klicken Sie auf die Schaltfläche <strong>Währung</strong> und wählen dann eine Währung aus.</span><span class="sxs-lookup"><span data-stu-id="79d37-174">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79d37-175">Nicht mit Berichtsdefinition gespeicherte Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="79d37-175">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="79d37-176">Basisperiode</span><span class="sxs-lookup"><span data-stu-id="79d37-176">Base period</span></span></li>
<li><span data-ttu-id="79d37-177">Basisjahr</span><span class="sxs-lookup"><span data-stu-id="79d37-177">Base year</span></span></li>
<li><span data-ttu-id="79d37-178">Berücksichtigter Zeitraum</span><span class="sxs-lookup"><span data-stu-id="79d37-178">Period covered</span></span></li>
</ul>
<span data-ttu-id="79d37-179">Nur Einstellungen zum Standardbasiszeitraum werden mit der Berichtsdefinition gespeichert.</span><span class="sxs-lookup"><span data-stu-id="79d37-179">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79d37-180">Mit Berichtsdefinition gespeicherte Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="79d37-180">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="79d37-181">Berichtsdatum</span><span class="sxs-lookup"><span data-stu-id="79d37-181">Report date</span></span></li>
<li><span data-ttu-id="79d37-182">Standardbasiszeitraum</span><span class="sxs-lookup"><span data-stu-id="79d37-182">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79d37-183">Berichte in Gruppe</span><span class="sxs-lookup"><span data-stu-id="79d37-183">Reports in group</span></span></td>
<td><span data-ttu-id="79d37-184">Fügen Sie Berichte in der Berichtsgruppe hinzu, entfernen Sie sie aus dieser oder sortieren Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="79d37-184">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="79d37-185">Um Berichtsdefinitionen zur Berichtsgruppe hinzuzufügen, doppelklicken Sie auf die Berichtsgruppe, um sie zu öffnen, und klicken dann auf <strong>Hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="79d37-185">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="79d37-186">Wählen Sie die in die Berichtsgruppe einzuschließenden Berichte, und klicken Sie auf <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="79d37-186">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="79d37-187">Zum Entfernen eines Berichts aus der Berichtsgruppe wählen Sie diesen aus und klicken dann auf <strong>Entfernen</strong>.</span><span class="sxs-lookup"><span data-stu-id="79d37-187">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="79d37-188">Um die Reihenfolge zu ändern, in der die Berichte generiert werden, wählen Sie einen Bericht in der Liste aus, und klicken anschließend auf <strong>Nach oben verschieben</strong> oder <strong>Nach unten verschieben</strong>.</span><span class="sxs-lookup"><span data-stu-id="79d37-188">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="79d37-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79d37-189">See also</span></span>
--------

[<span data-ttu-id="79d37-190">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="79d37-190">Financial reporting</span></span>](financial-reporting-intro.md)




