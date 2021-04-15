---
title: Bericht Lagerungsbericht mit Artikelpreisvergleich
description: Erfahren Sie, wie Sie einen Bericht über die Lagerung von Artikelpreisen erstellen und dann das Ergebnis durchsuchen und/oder exportieren können.
author: AndersGirke
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a9e05dd582ed1bd2c242d3eeb77ca61203706e11
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813218"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="c9bcc-103">Bericht Lagerungsbericht mit Artikelpreisvergleich</span><span class="sxs-lookup"><span data-stu-id="c9bcc-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9bcc-104">Dieses Thema erklärt, wie man einen Bericht **Lagerungsbericht mit Artikelpreisvergleich** ausführt und die Ausgabe digital zur Verfügung stellt, entweder als interaktive Seite in Dynamics 365 Supply Chain Management oder als exportiertes Dokument in einem von mehreren Formaten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="c9bcc-105">Wenn Sie den Bericht in Ihrem Browser anzeigen, werden die Spalten und Summenbilanzen je nach Ihrem konfigurierten Layout dynamisch angepasst.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="c9bcc-106">Sie können die Ergebnisse sortieren, filtern, die Daten aufschlüsseln und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="c9bcc-107">Die Berichtsergebnisse werden in der Dateneinheit **Artikelpreise vergleichen** gespeichert, mit der Sie die Ergebnisse filtern und in ein Format wie CSV oder Microsoft Excel exportieren können.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="c9bcc-108">Der Bericht **Lagerungsbericht mit Artikelpreisvergleich** ist in Fällen hilfreich, in denen die Ausgabe viele Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="c9bcc-109">Die Ausgabe enthält z.B. viele Zeilen, wenn Sie mehr als 40.000 Artikel mit einem ausstehenden Artikelpreis in der Kalkulationsversion haben.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="c9bcc-110">Aktivieren Sie die Speicherung der Vergleichspreise für Artikel</span><span class="sxs-lookup"><span data-stu-id="c9bcc-110">Enable compare item prices storage</span></span>

<span data-ttu-id="c9bcc-111">Bevor Sie diese Funktion nutzen können, müssen Sie sie auf Ihrem System aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="c9bcc-112">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie bei Bedarf aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="c9bcc-113">Hier wird die Funktion als aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="c9bcc-114">**Modul** - Kostenmanagement</span><span class="sxs-lookup"><span data-stu-id="c9bcc-114">**Module** - Cost management</span></span>
- <span data-ttu-id="c9bcc-115">**Funktionsname** - Vergleichen Sie die Lagerung von Artikelpreisen</span><span class="sxs-lookup"><span data-stu-id="c9bcc-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="c9bcc-116">Erstellen Sie einen Bericht zum Vergleich von Artikelpreisen für die Lagerung</span><span class="sxs-lookup"><span data-stu-id="c9bcc-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="c9bcc-117">Befolgen Sie diese Schritte, um einen **Lagerungsbericht mit Artikelpreisvergleich** Bericht zu erstellen und zu speichern:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="c9bcc-118">Gehen Sie zu **Kostenmanagement > Anfragen und Berichte > Berichte über vorher festgelegte Kosten > Lagerungsbericht mit Artikelpreisvergleich**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="c9bcc-119">Wählen Sie **Neu**, um den Bereich **Preisvergleiche Artikelpreise** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="c9bcc-120">Legen Sie die folgenden Optionen fest, um zu definieren, welche Preise in Ihrem Bericht verglichen werden sollen:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="c9bcc-121">Geben Sie im Bereich **Parameter** dem Bericht einen eindeutigen **Name** und verwenden Sie die Felder in den Abschnitten **Ausstehende Preise zum Vergleichen** und **Zum Vergleich verwendete Preise**, um festzulegen, welche Preise und Daten verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="c9bcc-122">Richten Sie in den Abschnitten **Einzubeziehende Datensätze** Filter und Einschränkungen ein, um zu definieren, welche Daten in den Bericht aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="c9bcc-123">Legen Sie auf der Registerkarte **Im Hintergrund ausführen** fest, wie, wann und mit welcher Häufigkeit Sie den Bericht erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="c9bcc-124">Dieser Bericht wird immer als Teil eines Batch-Jobs ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="c9bcc-125">Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und den Bereich zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="c9bcc-126">Nachdem der Batch-Job abgeschlossen ist, wird er auf der Seite **Lagerungsbericht mit Artikelpreisvergleich** aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="c9bcc-127">Möglicherweise müssen Sie die Seite aktualisieren, um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="c9bcc-128">Sehen Sie sich den Bericht „Lagerungsbericht mit Artikelpreisvergleich“ an.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="c9bcc-129">Nachdem Sie einen Bericht erstellt haben, können Sie ihn jederzeit wie folgt einsehen und untersuchen:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="c9bcc-130">Gehen Sie zu **Kostenmanagement > Anfragen und Berichte > Berichte über vorher festgelegte Kosten > Lagerungsbericht mit Artikelpreisvergleich**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="c9bcc-131">Wählen Sie einen Bericht aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-131">Select a report from the list.</span></span>

1. <span data-ttu-id="c9bcc-132">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-132">Do one of the following:</span></span>

    - <span data-ttu-id="c9bcc-133">Wählen Sie **Überblick**, um einen Überblick über Ihre Berichtsergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="c9bcc-134">Wählen Sie **Details anzeigen**, um eine detailliertere Ansicht Ihres Berichts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="c9bcc-135">Nachdem die ausgewählte Ansicht geöffnet wurde, können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="c9bcc-136">Wählen Sie fast eine beliebige Spaltenüberschrift, um die Tabelle nach den Werten in dieser Spalte zu sortieren oder zu filtern, wie bei den meisten Standardformularen im Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="c9bcc-137">Beachten Sie, dass Sie die Spalte **Nettoänderungspreis %** nicht sortieren oder filtern können, da es sich um ein berechnetes Feld handelt.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="c9bcc-138">Wählen Sie **Dimensionsanzeige**, um einen Bereich zu öffnen, in dem Sie wählen können, welche Dimensionsspalte in das Formular aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="c9bcc-139">Setzen Sie **Einstellung speichern** auf **Ja**, wenn Sie diese Einstellungen speichern möchten, damit sie beim nächsten Öffnen des Berichts erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="c9bcc-140">Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und den Bericht zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="c9bcc-141">Markieren Sie eine beliebige Zeile im Formular und wählen Sie dann **Details anzeigen**, um weitere Informationen über das ausgewählte Element zu sehen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="c9bcc-142">Von hier aus können Sie die Daten aufschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="c9bcc-143">Markieren Sie eine beliebige Zeile im Formular und wählen Sie dann **Vergleichsdiagramm anzeigen**, um eine interaktive grafische Darstellung Ihrer Ergebnisse in Bezug auf das ausgewählte Element zu sehen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="c9bcc-144">Sie können diese Ergebnisse untersuchen, indem Sie verschiedene grafische Elemente im Diagramm und in der Diagrammlegende auswählen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="c9bcc-145">Markieren Sie eine beliebige Zeile im Formular und wählen Sie dann **Berechnungsdetails anzeigen**, um weitere Informationen über Berechnungen in Bezug auf das ausgewählte Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="c9bcc-146">Von hier aus können Sie die Daten aufschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="c9bcc-147">Exportieren Sie den Bericht zum Vergleich der Artikelpreise für die Lagerung</span><span class="sxs-lookup"><span data-stu-id="c9bcc-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="c9bcc-148">Jeder Bericht, den Sie generieren, wird in der Dateneinheit **Postenpreise vergleichen** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="c9bcc-149">Sie können die Standarddatenverwaltungsfunktionen des Supply Chain Management verwenden, um Daten aus dieser Entität in jedes unterstützte Datenformat, einschließlich CSV oder Microsoft Excel, zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="c9bcc-150">Das folgende Beispiel zeigt, wie Sie einen Bericht **Lagerungsbericht mit Artikelpreisvergleich** exportieren können:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="c9bcc-151">Gehen Sie zu **Systemverwaltung > Arbeitsbereiche > Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="c9bcc-152">Wählen Sie die Schaltfläche **Export** im Abschnitt **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="c9bcc-153">Es öffnet sich die Seite **Export**, auf der Sie Ihren Export-Job einrichten können.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="c9bcc-154">Beginnen Sie, indem Sie Ihrem Job einen **Gruppenname** geben.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="c9bcc-155">Wählen Sie im Abschnitt **Ausgewählte Entitäten** die Option **Entität hinzufügen**, um ein Dialogfeld zu öffnen, in dem Sie die folgenden Optionen einstellen können:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="c9bcc-156">**Entitätsname** - Wählen Sie **Preisvergleich für Artikel**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="c9bcc-157">**Zieldatenformat** - Wählen Sie das Format, in das Sie exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="c9bcc-158">Wählen Sie **Hinzufügen**, um die neue Zeile hinzuzufügen, und wählen Sie dann **Schließen**, um das Dialogfenster zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="c9bcc-159">Normalerweise exportieren Sie jeweils nur einen Bericht.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="c9bcc-160">Richten Sie dazu einen **Filter** für die Zeile ein, die Sie gerade dem Fenster **Anfrage** hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="c9bcc-161">Auf diese Weise können Sie festlegen, welche Berichte aus dem Bereich **Preisvergleich von Artikeln** Sie in Ihren Export aufnehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="c9bcc-162">Legen Sie die folgenden Filteroptionen fest, um einen einzelnen Bericht zu exportieren:</span><span class="sxs-lookup"><span data-stu-id="c9bcc-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="c9bcc-163">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen**, um eine neue Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="c9bcc-164">Setzen Sie **Tabelle** auf **Preise für Artikel vergleichen**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="c9bcc-165">Setzen Sie **Ableitende Tabelle** auf **Artikelpreise vergleichen**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="c9bcc-166">Setzen Sie **Feld** auf das Feld, nach dem Sie filtern möchten.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="c9bcc-167">Normalerweise verwenden Sie **Ausführungsname** oder **Ausführungszeit**.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="c9bcc-168">Setzen Sie **Kriterien** auf den Wert aus dem von Ihnen gewählten Feld, nach dem Sie suchen wollen (entweder den Namen des Berichts oder die Zeit, zu der der Bericht generiert wurde).</span><span class="sxs-lookup"><span data-stu-id="c9bcc-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="c9bcc-169">Fügen Sie ggf. weitere Zeilen zur Tabelle **Bereich** hinzu, bis Sie den gesuchten Bericht eindeutig identifiziert haben.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="c9bcc-170">Wählen Sie **OK**, um Ihre Einstellungen zu speichern und zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="c9bcc-171">Wählen Sie **Speichern**, um Ihre Export-Einstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="c9bcc-172">Öffnen Sie die Registerkarte **Exportoptionen** und wählen Sie **Jetzt exportieren**, um die Exportdatei zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="c9bcc-173">Die Seite **Ausführungszusammenfassung** wird geöffnet, auf der Sie den Status Ihres Exportauftrags und eine Liste der exportierten Entitäten sehen können.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="c9bcc-174">Wählen Sie den Bereich **Preisvergleich für Artikel** Entität, die im Bereich **Verarbeitungsstatus der Entität** aufgelistet ist, und wählen Sie dann **Datei herunterladen**, um die von dieser Entität exportierten Daten herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="c9bcc-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="c9bcc-175">Weitere Informationen über die Verwendung der Datenverwaltung für den Datenexport finden Sie unter [Übersicht über Datenimport- und -exportjobs](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="c9bcc-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]