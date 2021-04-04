---
title: Steuerelemente für Word-Inhalte in generierten Berichten unterdrücken
description: In diesem Thema wird erläutert, wie Sie ein EB-Format (elektronische Berichterstellung) konfigurieren, um Berichte als Microsoft Word-Dateien zu generieren, in denen Inhaltssteuerelemente unterdrückt sind.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562117"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="804b5-103">Steuerelemente für Word-Inhalte in generierten Berichten unterdrücken</span><span class="sxs-lookup"><span data-stu-id="804b5-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="804b5-104">Um Berichte als Microsoft Word-Dokumente zu generieren, müssen Sie für diese eine Vorlage als Word-Dokument entwerfen.</span><span class="sxs-lookup"><span data-stu-id="804b5-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="804b5-105">Diese Vorlage muss Steuerelemente für Word-Inhalte als Platzhalter für Daten enthalten, die während der Laufzeit ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="804b5-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="804b5-106">Um das für Ihre Berichte als Vorlage erstellte Word-Dokument zu verwenden, können Sie eine neue [Lösung](er-quick-start1-new-solution.md) für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) [konfigurieren](er-design-configuration-word.md).</span><span class="sxs-lookup"><span data-stu-id="804b5-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="804b5-107">Die Lösung muss eine EB-[Konfiguration](general-electronic-reporting.md#Configuration) enthalten, die eine Komponente im EB-[Format](general-electronic-reporting.md#FormatComponentOutbound) aufweist.</span><span class="sxs-lookup"><span data-stu-id="804b5-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="804b5-108">Dieses EB-Format muss so konfiguriert sein, dass die entworfene Vorlage für die Berichtsgenerierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="804b5-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="804b5-109">In Dynamics 365 Finance Version 10.0.6 und höher können Sie Formeln in Ihrem EB-Format konfigurieren, um einige Word-Inhaltssteuerelemente in generierten Dokumenten zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="804b5-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="804b5-110">Die folgenden Schritten erläutern, wie ein Benutzer, der dem Systemadministrator oder der Rolle als funktionaler Berater für die elektronische Berichterstellung zugewiesen ist, ein EB-Format konfigurieren kann, das Berichte als Word-Dateien generiert und einige Inhaltssteuerelemente in den generierten Berichten unterdrückt, die mithilfe einer Word-Vorlage konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="804b5-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="804b5-111">Diese Schritte können im Unternehmen GBSI ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="804b5-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="804b5-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="804b5-112">Prerequisites</span></span>

<span data-ttu-id="804b5-113">Bevor Sie diese Schritte ausführen können, müssen Sie zuerst diejenigen in diesen Aufgabenleitfäden ausführen:</span><span class="sxs-lookup"><span data-stu-id="804b5-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="804b5-114">Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format</span><span class="sxs-lookup"><span data-stu-id="804b5-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="804b5-115">EB-Konfigurationen mit Excel-Vorlagen erneut verwenden, um Berichte im Word-Format zu generieren</span><span class="sxs-lookup"><span data-stu-id="804b5-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="804b5-116">Wenn Sie die Schritte dieser Aufgabenleitfäden ausführen, werden die folgenden Elemente vorbereitet:</span><span class="sxs-lookup"><span data-stu-id="804b5-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="804b5-117">ein EB-Format **Beispiel-Arbeitsblattbericht**, das zum Generieren eines Dokuments im Word-Format konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="804b5-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="804b5-118">eine [Entwurfsversion](general-electronic-reporting.md#component-versioning) des EB-Formats **Beispiel-Arbeitsblattbericht**, das als **Ausführbar** gekennzeichnet ist</span><span class="sxs-lookup"><span data-stu-id="804b5-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="804b5-119">eine **elektronische** Zahlungsmethode, die für die Verwendung des EB-Formats **Beispiel-Arbeitsblattbericht** zur Verarbeitung von Kreditorenzahlungen konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="804b5-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="804b5-120">Außerdem müssen Sie die folgende Vorlage für den Beispielbericht herunterladen und speichern:</span><span class="sxs-lookup"><span data-stu-id="804b5-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="804b5-121">Begrenzte Vorlage 2 eines Zahlungsberichtes (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="804b5-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="804b5-122">Überprüfen der heruntergeladenen Word-Vorlage</span><span class="sxs-lookup"><span data-stu-id="804b5-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="804b5-123">Öffnen Sie in der Word-Desktopanwendung die Vorlagendatei **SampleVendPaymDocReportBounded2.docx**, die Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="804b5-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="804b5-124">Stellen Sie sicher, dass die Vorlagendatei einen Zusammenfassungsabschnitt enthält, in dem die gesamten Zahlungsbeträge für jeden Währungscode angezeigt werden, der in den verarbeiteten Zahlungen erfüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="804b5-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="804b5-125">Der Zusammenfassungsabschnitt befindet sich in einer separaten Tabelle des Word-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="804b5-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="804b5-126">Die erste Zeile dieser Tabelle enthält die Überschriften der Tabellenspalten als Abschnittsüberschrift.</span><span class="sxs-lookup"><span data-stu-id="804b5-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="804b5-127">Die zweite Zeile dieser Tabelle enthält das Steuerelement für sich wiederholende Inhalte als Abschnittsdetails.</span><span class="sxs-lookup"><span data-stu-id="804b5-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="804b5-128">Dieses Inhaltssteuerelement ist dem Feld **SummaryLines** im benutzerdefinierten XML-Teil **Bericht** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="804b5-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="804b5-129">Basierend auf dieser Zuordnung ist das Inhaltssteuerelement dem Element **SummaryLines** des bearbeitbaren EB-Formats zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="804b5-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="804b5-130">Das sich wiederholende Inhaltssteuerelement wird durch den Schlüssel **SummaryLines** gekennzeichnet, der dem Feld des benutzerdefinierten XML-Teils entspricht, dem es zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="804b5-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Layout der Word-Vorlage](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="804b5-132">Wählen Sie die vorhandene ER-Berichtskonfiguration aus</span><span class="sxs-lookup"><span data-stu-id="804b5-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="804b5-133">Für die folgenden Schritte werden Sie die vorhandene EB-Konfiguration nutzen, die Sie konfiguriert haben, als Sie die Schritte in den zuvor genannten Aufgabenleitfäden ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="804b5-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="804b5-134">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="804b5-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="804b5-135">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="804b5-136">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur den Punkt **Zahlungsmodell**, und wählen Sie dann **Beispiel-Arbeitsblattbericht** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="804b5-137">Wählen Sie **Designer** aus, um die Entwurfsversion des ausgewählten EB-Formats zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="804b5-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="804b5-138">Die aktuelle Vorlage durch die neue Vorlage ersetzen</span><span class="sxs-lookup"><span data-stu-id="804b5-138">Replace the current template with the new template</span></span>

<span data-ttu-id="804b5-139">Aktuell wird die Datei „SampleVendPaymDocReportBounded.docx“ als Vorlage verwendet, um die Ausgabe im Word-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="804b5-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="804b5-140">In den folgenden Schritten werden Sie diese Word-Vorlage durch die neue Word-Vorlage „SampleVendPaymDocReportBounded2.docx“ ersetzen, die Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="804b5-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="804b5-141">Wählen Sie auf der Seite **Formatdesigner** die Option **Anhänge** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="804b5-142">Wählen Sie auf der Seite **Anhänge** die Option **Löschen** aus, um die vorhandene Vorlage zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="804b5-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="804b5-143">Wählen Sie **Ja** aus, um das Löschen zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="804b5-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="804b5-144">Wählen Sie **Neu** \> **Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="804b5-145">Wählen Sie **Durchsuchen** aus, navigieren Sie zu der Datei **SampleVendPaymDocReportBounded2.docx**, die Sie zuvor heruntergeladen haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="804b5-146">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="804b5-146">Select **OK**.</span></span>
7. <span data-ttu-id="804b5-147">Schließen Sie die Seite **Anhänge**.</span><span class="sxs-lookup"><span data-stu-id="804b5-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="804b5-148">Geben Sie auf der Seite **Formatdesigner** im Feld **Vorlage** die Datei **SampleVendPaymDocReportBounded2.docx** ein, oder wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="804b5-149">Das Format zum Erstellen der Word-Ausgabe ausführen</span><span class="sxs-lookup"><span data-stu-id="804b5-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="804b5-150">Rufen Sie **Kreditorenkonten** \> **Zahlungen** \> **Zahlungserfassung** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="804b5-151">Wählen Sie auf der Registerkarte **Liste** der Seite **Kreditorenzahlungen** alle Zahlungen aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="804b5-152">Wählen Sie **Zahlungsstatus** \> **Keiner** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="804b5-153">Wählen Sie **Zahlungen generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="804b5-154">Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="804b5-155">Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="804b5-156">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="804b5-156">Select **OK**.</span></span>
8. <span data-ttu-id="804b5-157">Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus, und analysieren Sie die generierte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="804b5-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Zahlrungen zur Verarbeitung auf der Seite „Kreditorenzahlungen“](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="804b5-159">Die Ausgabe wird im Word-Format dargestellt und enthält den Zusammenfassungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="804b5-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="804b5-160">Das bearbeitbare Format konfigurieren, um den Zusammenfassungsabschnitt zu unterdrücken</span><span class="sxs-lookup"><span data-stu-id="804b5-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="804b5-161">Wenn Sie den Zusammenfassungsabschnitt in einem generierten Dokument auf Anforderung eines Benutzers, der dieses EB-Format ausführt, unterdrücken möchten, müssen Sie das bearbeitbare EB-Format modifizieren.</span><span class="sxs-lookup"><span data-stu-id="804b5-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="804b5-162">Rufen Sie **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung** aus, und öffnen Sie zum Bearbeiten die Entwurfsversion des EB-Formats.</span><span class="sxs-lookup"><span data-stu-id="804b5-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="804b5-163">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="804b5-164">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur den Punkt **Zahlungsmodell** \> **Beispiel-Arbeitsblattbericht**.</span><span class="sxs-lookup"><span data-stu-id="804b5-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="804b5-165">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-165">Select **Designer**.</span></span>
5. <span data-ttu-id="804b5-166">Erweitern Sie auf der Seite **Formatdesigner** den Punkt **Word**, und wählen Sie **SummaryLines** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="804b5-167">Fügen Sie der Registerkarte **Zuordnung** eine neue Datenquelle hinzu, um den Benutzer während der Laufzeit zu fragen, ob der Zusammenfassungsabschnitt unterdrückt werden soll:</span><span class="sxs-lookup"><span data-stu-id="804b5-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="804b5-168">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="804b5-169">Wählen Sie im Dialogfeld **Datenquelle hinzufügen** die Option **Allgemein\Benutzereingabeparameter** aus, um das Dialogfeld **Datenquelleneigenschaften ‚Benutzereingabeparameter‛** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="804b5-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="804b5-170">Geben Sie im Feld **Name** **uipSuppress** ein.</span><span class="sxs-lookup"><span data-stu-id="804b5-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="804b5-171">Geben Sie im Feld **Beschriftung** **Zusammenfassungsabschnitt unterdrücken** ein.</span><span class="sxs-lookup"><span data-stu-id="804b5-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="804b5-172">Geben Sie im Feld **Name des Betriebsdatentyps** **NoYes** ein, oder wählen Sie dies aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="804b5-173">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="804b5-173">Select **OK**.</span></span>

7. <span data-ttu-id="804b5-174">Fügen Sie eine neue Datenquelle des Anwendungsenumerationstyps **NoYes** hinzu:</span><span class="sxs-lookup"><span data-stu-id="804b5-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="804b5-175">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="804b5-176">Wählen Sie im Dialogfeld **Datenquelle hinzufügen** die Option **Dynamics 365 for Operations\Enumeration** aus, um das Dialogfeld **Datenquelleneigenschaften ‚Enumeration‛** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="804b5-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="804b5-177">Geben Sie im Feld **Name** die Bezeichnung **enumNoYes** ein.</span><span class="sxs-lookup"><span data-stu-id="804b5-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="804b5-178">Geben Sie im Feld **Beschriftung** **Optionen unterdrücken** ein.</span><span class="sxs-lookup"><span data-stu-id="804b5-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="804b5-179">Geben Sie im Feld **Name des Betriebsdatentyps** **NoYes** ein, oder wählen Sie dies aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="804b5-180">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="804b5-180">Select **OK**.</span></span>

8. <span data-ttu-id="804b5-181">Konfigurieren Sie die Formel für das ausgewählte Formatelement **SummaryLines** so, dass angegeben wird, wann das dem ausgewählten Formatelement zugeordnete Word-Inhaltssteuerelement unterdrückt werden soll:</span><span class="sxs-lookup"><span data-stu-id="804b5-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="804b5-182">Wählen Sie auf der Registerkarte **Zuordnung** im Abschnitt **Entfernt** die Option **Bearbeiten** aus, um die Seite **[Formeldesigner](general-electronic-reporting-formula-designer.md)** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="804b5-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="804b5-183">Geben Sie im Feld **Formel** die Formel `uipSuppress = enumNoYes.Yes` ein.</span><span class="sxs-lookup"><span data-stu-id="804b5-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="804b5-184">Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.</span><span class="sxs-lookup"><span data-stu-id="804b5-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="804b5-185">Diese Formel wird auf ein generiertes Dokument angewendet, **nachdem alle anderen Formatelemente ausgeführt wurden**.</span><span class="sxs-lookup"><span data-stu-id="804b5-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="804b5-186">Zur Anwendung dieser Formel gibt es ein Word-Inhaltssteuerelement, das als für die Formel konfiguriertes Formatelement gekennzeichnet ist (**SummaryLines** in diesem Fall), in einem generierten Dokument.</span><span class="sxs-lookup"><span data-stu-id="804b5-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="804b5-187">Dieses Inhaltssteuerelement wird dann zusammen mit der Zeile in der Word-Tabelle, in der es enthalten ist, vollständig entfernt.</span><span class="sxs-lookup"><span data-stu-id="804b5-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="804b5-188">Die Detailzeile des Zusammenfassungsabschnitts wird aus dem generierten Dokument entfernt.</span><span class="sxs-lookup"><span data-stu-id="804b5-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="804b5-189">In der Entwurfsphase können Sie die **Entfernt**-Formel für ein Formatelement konfigurieren, obwohl kein Inhaltssteuerelement in der von Ihnen verwendeten Word-Vorlage eine Markierung enthält, die dem Namen eines Formatelements entspricht, für das die **Entfernt**-Eigenschaft konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="804b5-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="804b5-190">Wenn Sie das Format in der Entwurfsphase validieren, erhalten Sie eine [Warnung](er-components-inspections.md#i14) hinsichtlich dieser Inkonsistenz.</span><span class="sxs-lookup"><span data-stu-id="804b5-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="804b5-191">Während der Laufzeit wird eine Ausnahme ausgelöst, wenn kein Inhaltssteuerelement in der von Ihnen verwendeten Word-Vorlage eine Markierung enthält, die dem Namen eines Formatelements entspricht, für das die **Entfernt**-Eigenschaft konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="804b5-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="804b5-192">Setzen Sie auf der Registerkarte **Zuordnung** im Abschnitt **Entfernt** die Option **Mit übergeordnetem Element** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="804b5-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="804b5-193">Sie müssen diese Option auf **Ja** setzen, um die gesamte Word-Tabelle als übergeordnetes Objekt der Zeile, die die Details des Zusammenfassungsabschnitts enthält, zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="804b5-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="804b5-194">Wenn Sie diese Option auf **Nein** setzen, verbleibt die Abschnittsüberschriftenzeile im generierten Dokument.</span><span class="sxs-lookup"><span data-stu-id="804b5-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="804b5-195">Wählen Sie **Speichern** aus, um Ihre Änderungen im bearbeitbaren Format zu speichern.</span><span class="sxs-lookup"><span data-stu-id="804b5-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Die generierte Ausgabe im Word-Format](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="804b5-197">Das geänderte Format zum Erstellen der Word-Ausgabe ausführen</span><span class="sxs-lookup"><span data-stu-id="804b5-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="804b5-198">Rufen Sie **Kreditorenkonten** \> **Zahlungen** \> **Zahlungserfassung** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="804b5-199">Wählen Sie die erstellte Zahlungserfassung aus, und wählen Sie anschließend **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="804b5-200">Wählen Sie auf der Seite **Kreditorenzahlungen** alle Zeilen und anschließend **Zahlungsstatus** \> **Keiner** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="804b5-201">Wählen Sie **Zahlungen generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="804b5-202">Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="804b5-203">Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="804b5-204">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="804b5-204">Select **OK**.</span></span>
8. <span data-ttu-id="804b5-205">Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** im Feld **Zusammenfassungsabschnitt unterdrücken** die Option **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="804b5-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="804b5-206">Wählen Sie **OK** aus, und analysieren Sie die generierte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="804b5-206">Select **OK**, and analyze the generated output.</span></span>

    ![Generierte Ausgabe im Word-Format](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="804b5-208">Beachten Sie, dass die Ausgabe den Zusammenfassungsabschnitt nicht enthält, da er unterdrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="804b5-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="804b5-209">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="804b5-209">Additional resources</span></span>

- [<span data-ttu-id="804b5-210">Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format</span><span class="sxs-lookup"><span data-stu-id="804b5-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="804b5-211">ER-Konfigurationen zum Generieren von Berichten im Word-Format entwerfen</span><span class="sxs-lookup"><span data-stu-id="804b5-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="804b5-212">EB-Konfigurationen mit Excel-Vorlagen erneut verwenden, um Berichte im Word-Format zu generieren</span><span class="sxs-lookup"><span data-stu-id="804b5-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="804b5-213">Konfigurierte EB-Komponente überprüfen, um Laufzeitprobleme zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="804b5-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]