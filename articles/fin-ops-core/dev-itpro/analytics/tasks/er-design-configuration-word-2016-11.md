---
title: EB-Konfigurationen mit Excel-Vorlagen wiederverwenden, um Berichte im Word-Format zu erstellen
description: In diesem Thema wird beschrieben, wie Berichtsformate, die zum Generieren von Berichten als Excel-Arbeitsmappen entwickelt wurden, so konfiguriert werden können, dass Berichte als Word-Dokumente generiert werden.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 413be634e80b87781444e1c1445c78691f4b4b0b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944291"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="fe569-103">EB-Konfigurationen mit Excel-Vorlagen wiederverwenden, um Berichte im Word-Format zu erstellen</span><span class="sxs-lookup"><span data-stu-id="fe569-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe569-104">Um Berichte als Microsoft Word-Dokumente zu generieren, können Sie ein neues [EB-](../general-electronic-reporting.md)[Format](../general-electronic-reporting.md#FormatComponentOutbound) (elektronische Berichterstellung) [konfigurieren](../er-design-configuration-word.md).</span><span class="sxs-lookup"><span data-stu-id="fe569-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="fe569-105">Alternativ können Sie ein EB-Format wiederverwenden, das ursprünglich zum Generieren von Berichten als Excel-Arbeitsmappen entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe569-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="fe569-106">In diesem Fall müssen Sie die Excel-Vorlage durch eine Word-Vorlage ersetzen.</span><span class="sxs-lookup"><span data-stu-id="fe569-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="fe569-107">Die folgenden Verfahren zeigen, wie ein Benutzer in der Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung ein EB-Format konfigurieren kann, um Berichte als Word-Dateien zu generieren, indem er ein EB-Format wiederverwendet, das zum Generieren von Berichten als Excel-Dateien entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe569-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="fe569-108">Diese Prozeduren können im Unternehmen GBSI ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fe569-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fe569-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fe569-109">Prerequisites</span></span>

<span data-ttu-id="fe569-110">Um diese Prozeduren abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden [Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format](er-design-reports-openxml-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="fe569-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="fe569-111">Sie müssen auch die folgenden Vorlagen für den Beispielbericht herunterladen und lokal speichern:</span><span class="sxs-lookup"><span data-stu-id="fe569-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="fe569-112">Vorlage eines Zahlungsberichtes (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="fe569-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [<span data-ttu-id="fe569-113">Begrenzte Vorlage eines Zahlungsberichtes (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="fe569-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

<span data-ttu-id="fe569-114">Diese Prozeduren gelten für eine Funktion, die Dynamics 365 for Operations Version 1611 (November 2016) hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe569-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="fe569-115">Wählen Sie die vorhandene ER-Berichtskonfiguration aus</span><span class="sxs-lookup"><span data-stu-id="fe569-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="fe569-116">Wechseln Sie in Dynamics 365 Finance zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="fe569-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe569-117">Stellen Sie sicher, dass der Konfigurationsanbieter **Litware, Inc.** als **Aktiv** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fe569-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="fe569-118">Wenn dies nicht der Fall ist, befolgen Sie die Schritte im Aufgabenleitfaden [Erstellen von Konfigurationsanbietern und Markieren als aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fe569-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="fe569-119">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="fe569-120">Sie verwenden die vorhandene EB-Koniguration erneut, die entworfen wurde, um die Berichtsausgabe im OPENXML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="fe569-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="fe569-121">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **Beispiel-Arbeitsblattbericht** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe569-122">Die Entwurfsversion des ausgewählten EB-Formats kann im Inforegister **Versionen** bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="fe569-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="fe569-123">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-123">Select **Designer**.</span></span>
6. <span data-ttu-id="fe569-124">Beachten Sie auf der Seite **Format-Designer**, dass der Titel des Stammformatelements angibt, dass derzeit eine Excel-Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe569-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Auswählen der vorhandenen Konfiguration](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="fe569-126">Überprüfen der heruntergeladenen Word-Vorlage</span><span class="sxs-lookup"><span data-stu-id="fe569-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="fe569-127">Öffnen Sie in der Word-Desktopanwendung die Vorlagendatei **SampleVendPaymDocReport.docx**, die Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="fe569-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="fe569-128">Stellen Sie sicher, dass diese Vorlage nur das Layout des Dokuments beinhaltet, das Sie als EB-Ausgabe generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fe569-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Das Layout der Word-Vorlage in der Desktop-Anwendung](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="fe569-130">Ersetzen Sie die Excel-Vorlage durch die Word-Vorlage, und fügen Sie einen benutzerdefinierten XML-Teil hinzu</span><span class="sxs-lookup"><span data-stu-id="fe569-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="fe569-131">Aktuell wird das Excel-Dokument als Vorlage verwendet, um die Ausgabe im OPENXML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="fe569-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="fe569-132">Ersetzen Sie diese Vorlage durch die Word-Vorlagendatei SampleVendPaymDocReport.docx, die Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="fe569-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="fe569-133">Sie erweitern die Word-Vorlage auch durch Hinzufügen eines benutzerdefinierten XML-Teils.</span><span class="sxs-lookup"><span data-stu-id="fe569-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="fe569-134">Wählen Sie in Finance auf der Seite **Format-Designer** auf der Registerkarte **Format** die Option **Anhänge** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="fe569-135">Auf der Seite **Anhänge** wählen Sie **Löschen** aus, um die vorhandene Excel-Vorlage zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fe569-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="fe569-136">Wählen Sie **Ja** aus, um die Änderung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="fe569-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="fe569-137">Wählen Sie **Neu** \> **Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe569-138">Sie müssen einen Dokumenttyp auswählen, der in den EB-Parametern [konfiguriert wurde](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), um die Vorlagen von EB-Formatvorlagen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fe569-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="fe569-139">Wählen Sie **Durchsuchen** aus, und navigieren Sie dann zu der Datei **SampleVendPaymDocReport.docx**, die Sie zuvor heruntergeladen haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="fe569-140">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe569-140">Select **OK**.</span></span>
6. <span data-ttu-id="fe569-141">Schließen Sie die Seite **Anhänge**.</span><span class="sxs-lookup"><span data-stu-id="fe569-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="fe569-142">Auf der Seite **Format-Designer** im Feld **Vorlage** geben Sie die Datei **SampleVendPaymDocReport.docx** ein oder wählen sie aus, um diese Word-Vorlage anstelle der zuvor verwendeten Excel-Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe569-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="fe569-143">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-143">Select **Save**.</span></span>

    <span data-ttu-id="fe569-144">Zusätzlich zum Speichern von Konfigurationsänderungen, wird durch die Aktivität **Speichern** auch die angehängte Word-Vorlage aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fe569-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="fe569-145">Die hierarchische Struktur des entworfenen Formats wird dem zugeordneten Word-Dokument als neuer benutzerdefinierter XML-Abschnitt mit dem Namen **Bericht** angehängt.</span><span class="sxs-lookup"><span data-stu-id="fe569-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="fe569-146">Die angefügte Word-Vorlage enthält das Layout des Dokuments, das als EB-Ausgabe generiert wird, und auch die Struktur von Daten, die EB in diese Vorlage zur Laufzeit eingibt.</span><span class="sxs-lookup"><span data-stu-id="fe569-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="fe569-147">Beachten Sie, dass der Titel des Stammformatelements angibt, dass derzeit eine Word-Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe569-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Ersetzen der Excel-Vorlage durch die Word-Vorlage und Hinzufügen eines benutzerdefinierten XML-Teils](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="fe569-149">Auf der Registerkarte **Formate** wählen Sie **Anhänge** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="fe569-150">Sie können jetzt die Elemente des ausgewählten benutzerdefinierten XML-Teils **Bericht** den Inhaltssteuerelementen des Word-Dokuments zuordnen.</span><span class="sxs-lookup"><span data-stu-id="fe569-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="fe569-151">Wenn Sie mit dem Entwurf von Word-Dokumenten als Formulare vertraut sind, die [Inhaltssteuerelemente](/office/client-developer/word/content-controls-in-word) enthalten, die den Elementen von [benutzerdefinierten XML-Teilen](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) zugeordnet sind, führen Sie alle Schritte in der nächsten Prozedur aus, um das Dokument zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fe569-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="fe569-152">Weitere Informationen finden Sie unter [Erstellen von Formularen, die in Word ausgefüllt oder gedruckt werden können](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="fe569-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="fe569-153">Überspringen Sie anderenfalls die nächste Prozedur.</span><span class="sxs-lookup"><span data-stu-id="fe569-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="fe569-154">Ein Word-Dokument mit einem benutzerdefinierten XML-Teil erstellen und eine Datenzuordnung durchführen</span><span class="sxs-lookup"><span data-stu-id="fe569-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="fe569-155">In Finance wählen Sie auf der Seite **Anhänge** die Option **Öffnen** aus, um die ausgewählte Vorlage von Finance herunterzuladen und lokal als Word-Dokument zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fe569-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="fe569-156">Öffnen Sie in der Word-Desktopanwendung das gerade heruntergeladene Dokument.</span><span class="sxs-lookup"><span data-stu-id="fe569-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="fe569-157">Auf der Registerkarte **Entwickler** wählen Sie **XML-Zuordnungsbereich** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe569-158">Wenn die Registerkarte **Entwickler** nicht in der Menüleiste angezeigt wird, passen Sie die Menüleiste an, um sie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe569-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="fe569-159">Im Bereich **XML-Zuordnung** im Feld **Benutzerdefinierter XML-Teil** wählen Sie den benutzerdefinierten XML-Teil **Bericht** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="fe569-160">Sie können jetzt die Elemente des ausgewählten benutzerdefinierten XML-Teils **Bericht** und die Inhaltssteuerelemente des Word-Dokuments zuordnen.</span><span class="sxs-lookup"><span data-stu-id="fe569-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="fe569-161">Speichern Sie das aktualisierte Word-Dokument lokal unter **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="fe569-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="fe569-162">Überprüfen der Word-Vorlage, in der der benutzerdefinierte XML-Teil Inhaltssteuerelementen zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="fe569-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="fe569-163">Öffnen Sie in der Word-Desktopanwendung die Vorlagendatei **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="fe569-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="fe569-164">Stellen Sie sicher, dass diese Vorlage das Layout des Dokuments beinhaltet, das Sie als EB-Ausgabe generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fe569-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="fe569-165">Die Inhaltssteuerelemente, die als Platzhalter für Daten verwendet werden, die EB zur Laufzeit in diese Vorlage eingibt, basieren auf den Zuordnungen, die zwischen Elementen des benutzerdefinierten XML-Teils **Bericht** und den Inhaltssteuerelemente des Word-Dokuments konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="fe569-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Vorschau der Word-Vorlage in der Desktop-Anwendung](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="fe569-167">Hochladen der Word-Vorlage, in der der benutzerdefinierte XML-Teil Inhaltssteuerelementen zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="fe569-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="fe569-168">Wählen Sie in Finance auf der Seite **Anhänge** die Option **Löschen** aus, um die Word-Vorlage zu entfernen, die keine Zuordnungen zwischen Elementen des benutzerdefinierten XML-Teils **Bericht** und Inhaltssteuerelementen enthält.</span><span class="sxs-lookup"><span data-stu-id="fe569-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="fe569-169">Wählen Sie **Ja** aus, um die Änderung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="fe569-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="fe569-170">Wählen Sie **Neu** \> **Datei** aus, um eine neue Vorlagendatei hinzuzufügen, die Zuordnungen zwischen Elementen des benutzerdefinierten XML-Teils **Bericht** und Inhaltssteuerelementen enthält.</span><span class="sxs-lookup"><span data-stu-id="fe569-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe569-171">Sie müssen einen Dokumenttyp auswählen, der in den EB-Parametern [konfiguriert wurde](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), um die Vorlagen von EB-Formatvorlagen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fe569-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="fe569-172">Wählen Sie **Durchsuchen** aus, und navigieren Sie dann zu der Datei **SampleVendPaymDocReportBounded.docx**, die Sie heruntergeladen oder vorbereitet haben, indem Sie den Vorgang im Abschnitt [Ein Word-Dokument mit einem benutzerdefinierten XML-Teil erstellen und eine Datenzuordnung durchführen](#get-word-doc) abgeschlossen haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="fe569-173">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe569-173">Select **OK**.</span></span>
5. <span data-ttu-id="fe569-174">Schließen Sie die Seite **Anhänge**.</span><span class="sxs-lookup"><span data-stu-id="fe569-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="fe569-175">Auf der Seite **Format-Designer** im Feld **Vorlage** wählen Sie das Dokument aus, das Sie gerade heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="fe569-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="fe569-176">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-176">Select **Save**.</span></span>
8. <span data-ttu-id="fe569-177">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="fe569-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="fe569-178">Markieren des konfigurierten Formats als ausführbar</span><span class="sxs-lookup"><span data-stu-id="fe569-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="fe569-179">Um die Entwurfsversion des bearbeitbaren Formats auszuführen, müssen Sie sie [ausführbar](../er-quick-start2-customize-report.md#MarkFormatRunnable) machen.</span><span class="sxs-lookup"><span data-stu-id="fe569-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="fe569-180">In Finance wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** die Option **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="fe569-181">Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="fe569-182">Wählen Sie **Bearbeiten** aus, um die aktuelle Seite bei Bedarf bearbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="fe569-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="fe569-183">Für die aktuell ausgewählte Konfiguration **Beispiel-Arbeitsblattbericht** setzen Sie die Option **Entwurf ausführen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe569-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="fe569-184">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="fe569-185">Das Format ausführen, um eine Ausgabe im Word-Format zu erstellen</span><span class="sxs-lookup"><span data-stu-id="fe569-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="fe569-186">Wechseln Sie in Finance zu **Kreditorenkonten** \> **Zahlungen** \> **Zahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="fe569-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="fe569-187">Wählen Sie in einer zuvor eingegebenen Zahlungserfassung die Option aus **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="fe569-188">Auf der Seite **Kreditorenzahlungen** wählen Sie alle Zeilen im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="fe569-189">Wählen Sie **Zahlungsstatus** \> **Keiner** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-189">Select **Payment status** \> **None**.</span></span>

    ![Zahlrungen zur Verarbeitung auf der Seite „Kreditorenzahlungen“](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="fe569-191">Wählen Sie im Aktivitätsbereich **Zahlungen generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="fe569-192">Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fe569-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="fe569-193">Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="fe569-194">Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="fe569-195">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe569-195">Select **OK**.</span></span>

7. <span data-ttu-id="fe569-196">Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fe569-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="fe569-197">Die erstellte Ausgabe wird im Word-Format dargestellt und enthält die Details der verarbeiteten Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="fe569-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="fe569-198">Analysieren Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="fe569-198">Analyze the generated output.</span></span>

    ![Generierte Ausgabe im Word-Format](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="fe569-200">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe569-200">Additional resources</span></span>

- [<span data-ttu-id="fe569-201">Eine neue EB-Konfiguration zum Generieren von Berichten im Word-Format erstellen</span><span class="sxs-lookup"><span data-stu-id="fe569-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="fe569-202">Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER</span><span class="sxs-lookup"><span data-stu-id="fe569-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
