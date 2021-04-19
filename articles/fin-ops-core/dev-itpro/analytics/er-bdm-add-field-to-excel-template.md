---
title: Hinzufügen neuer Felder zu einer Geschäftsdokumentvorlage in Microsoft Excel
description: In diesem Thema erfahren Sie, wie Sie mit der Funktion Geschäftsdokumentenverwaltung neue Felder zu einer Geschäftsdokumentvorlage in Microsoft Excel hinzufügen können.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 991fe4ea56a2726c5df835cfc90a390cef2d5df5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751129"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="7428a-103">Hinzufügen neuer Felder zu einer Geschäftsdokumentvorlage in Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="7428a-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7428a-104">Sie können einer Vorlage, die zur Generierung von Geschäftsdokumenten im Format Microsoft Excel verwendet wird, neue Felder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7428a-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="7428a-105">Diese Felder können als Platzhalter hinzugefügt werden, mit denen generierte Dokumente mit den erforderlichen Informationen aus der Anwendung gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="7428a-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="7428a-106">Für jedes Feld, das Sie hinzufügen, können Sie auch eine Bindung zu den Datenquellen angeben, um festzulegen, welche Anwendungsdaten in das Feld eingegeben werden, wenn die Vorlage zur Generierung von Geschäftsdokumenten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7428a-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="7428a-107">Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das Beispiel in diesem Thema abschließen.</span><span class="sxs-lookup"><span data-stu-id="7428a-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="7428a-108">Dieses Beispiel zeigt, wie Sie eine Vorlage aktualisieren, um die Felder in den generierten Freitext-Rechnungsformularen auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="7428a-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="7428a-109">Konfigurieren Sie die Geschäftsdokumentenverwaltung, um Vorlagen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7428a-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="7428a-110">Da die Geschäftsdokumentenverwaltung (BDM) auf dem [Überblick über die elektronische Berichterstattung (ER)](general-electronic-reporting.md) aufbaut, müssen Sie die erforderlichen ER- und BDM-Parameter konfigurieren, bevor Sie mit BDM arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="7428a-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="7428a-111">Melden Sie sich auf der Instanz von Microsoft Dynamics 365 Finance als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="7428a-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="7428a-112">Führen Sie die folgenden Schritte des Beispiels im Thema [Übersicht Geschäftsdokumentenverwaltung](er-business-document-management.md) aus:</span><span class="sxs-lookup"><span data-stu-id="7428a-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="7428a-113">ER-Parameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7428a-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="7428a-114">Schalten Sie BDM ein.</span><span class="sxs-lookup"><span data-stu-id="7428a-114">Turn on BDM.</span></span>

<span data-ttu-id="7428a-115">Sie können nun mit dem BDM beginnen, um Geschäftsdokumentvorlagen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7428a-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="7428a-116">Importieren von ER-Lösungen, die eine Vorlage enthalten</span><span class="sxs-lookup"><span data-stu-id="7428a-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="7428a-117">Das Beispiel in diesem Verfahren verwendet die offiziell veröffentlichte ER-Lösung.</span><span class="sxs-lookup"><span data-stu-id="7428a-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="7428a-118">Sie müssen die ER-Konfigurationen dieser Lösung in Ihre aktuelle Finanzinstanz importieren.</span><span class="sxs-lookup"><span data-stu-id="7428a-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="7428a-119">Die **Konfiguration der Freitextrechnung (Excel)** ER-Format dieser Lösung enthält die Geschäftsdokumentvorlage im Excel-Format, die mit dem BDM bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7428a-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="7428a-120">Importieren Sie die neueste Version dieser ER-Format-Konfiguration aus Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="7428a-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="7428a-121">Die entsprechenden ER-Datenmodell- und ER-Modellzuordnungskonfigurationen werden automatisch importiert.</span><span class="sxs-lookup"><span data-stu-id="7428a-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="7428a-122">Weitere Informationen zum Importieren von ER-Konfigurationen finden Sie unter [Verwaltung des Lebenszyklus der ER-Konfiguration](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="7428a-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS Shared Objektbibliothek Seite](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="7428a-124">Bearbeiten der ER-Lösungsvorlage</span><span class="sxs-lookup"><span data-stu-id="7428a-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="7428a-125">Melden Sie sich als Benutzer an, der Zugriff auf den Arbeitsbereich **Geschäftsdokumentenverwaltung** hat.</span><span class="sxs-lookup"><span data-stu-id="7428a-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="7428a-126">Öffnen Sie den Arbeitsbereich **Geschäftsdokumentenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="7428a-126">Open the **Business document management** workspace.</span></span>

    ![Arbeitsbereich Geschäftsdokumentenverwaltung](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="7428a-128">Wählen Sie im Raster die Vorlage **Freitextrechnung (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="7428a-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="7428a-129">Wählen Sie im rechten Bereich **Neue Vorlage**, um eine neue Vorlage zu erstellen, die auf der ausgewählten Vorlage basiert.</span><span class="sxs-lookup"><span data-stu-id="7428a-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="7428a-130">Geben Sie im Feld **Titel** als Titel der neuen Vorlage **Freitextrechnung (Excel) Contoso** ein.</span><span class="sxs-lookup"><span data-stu-id="7428a-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="7428a-131">Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="7428a-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="7428a-132">Die Seite mit dem Editor für BDM-Vorlagen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7428a-132">The BDM template editor page appears.</span></span> <span data-ttu-id="7428a-133">Mit Microsoft 365 können Sie die ausgewählte Vorlage online in der eingebetteten Steuerung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7428a-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM-Vorlagen-Editor-Seite](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="7428a-135">Hinzufügen der Bezeichnung für ein neues Feld zur Vorlage</span><span class="sxs-lookup"><span data-stu-id="7428a-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="7428a-136">Aktivieren Sie auf der Seite des BDM-Vorlageneditors, in der Excel-Leiste, auf der Registerkarte **Ansicht** die Kontrollkästchen **Überschriften und Rasterlinien** für die editierbare Excel-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="7428a-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Aktivierte Kontrollkästchen für Überschriften und Rasterlinien](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="7428a-138">Zellen auswählen **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="7428a-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="7428a-139">Wählen Sie in der Excel-Leiste auf der Registerkarte **Start** **Zusammenführen & Zentrieren**, um die ausgewählten Zellen zu einer neuen zusammengeführten **E8:F8** Zelle zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="7428a-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="7428a-140">Geben Sie in der zusammengeführten Zelle **E8:F8** **URL** ein.</span><span class="sxs-lookup"><span data-stu-id="7428a-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="7428a-141">Wählen Sie zusammengeführte Zelle **E7:F7**, wählen Sie **Formatkopie**, und wählen Sie dann zusammengeführte Zelle **E8:F8**, um sie genauso zu formatieren wie zusammengeführte Zelle **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="7428a-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Neue Feldbezeichnung in der Vorlage hinzugefügt](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="7428a-143">Formatieren Sie die Vorlage, um Platz für ein neues Feld zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="7428a-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="7428a-144">Wählen Sie auf der Seite des BDM-Vorlageneditors die zusammengeführte Zelle **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="7428a-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="7428a-145">Wählen Sie in der Excel-Leiste auf der Registerkarte **Start** **Zusammenführen & Zentrieren**, um die ausgewählten Zellen zu einer neuen zusammengeführten **G8:H8** Zelle zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="7428a-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="7428a-146">Wählen Sie zusammengeführte Zelle **G7:H7**, wählen Sie **Formatkopie**, und wählen Sie dann zusammengeführte Zelle **G8:H8**, um sie genauso zu formatieren wie zusammengeführte Zelle **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="7428a-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Platz für das neue Feld reserviert](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="7428a-148">Wählen Sie im Feld **Name** **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="7428a-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="7428a-149">Der Bereich **CompanyInfo** der aktuellen Excel-Vorlage enthält alle Felder, die verwendet werden, um den Kopf eines generierten Berichts mit den Details der aktuellen Firma als Verkäuferpartei zu füllen.</span><span class="sxs-lookup"><span data-stu-id="7428a-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![CompanyInfo Bereich ausgewählt](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="7428a-151">Ein neues Feld zur Vorlage hinzufügen</span><span class="sxs-lookup"><span data-stu-id="7428a-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="7428a-152">Wählen Sie auf der Seite **BDM-Vorlageneditor**, im Aktivitätsbereich **Format anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7428a-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="7428a-153">Wählen Sie im Bereich **Vorlagenstruktur** **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7428a-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7428a-154">Sie müssen den Abschnitt der Vorlage, den Sie als neues Feld verwenden möchten, anpassen.</span><span class="sxs-lookup"><span data-stu-id="7428a-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="7428a-155">Sie haben diese Anpassung bereits vorgenommen, indem Sie die zusammengeführte Zelle **G8:H8** formatiert haben.</span><span class="sxs-lookup"><span data-stu-id="7428a-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Hinzufügen eines neuen Feldes zur Vorlage](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="7428a-157">Wählen Sie **Excel\Zelle**, um ein neues Feld als Zelle in der Vorlage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7428a-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="7428a-158">Sie können **Excel\Bereich** wählen, wenn Sie der Vorlage einen neuen Bereich hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7428a-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="7428a-159">Der eingegebene Bereich kann mehrere Zellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7428a-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="7428a-160">Sie können diese Zellen später hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7428a-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="7428a-161">Beachten Sie, dass die Vorlagenkomponente **CompanyInfo** automatisch im Bereich **Vorlagenstruktur** ausgewählt wird, da sie die am besten geeignete übergeordnete Komponente in der aktuellen Vorlagenstruktur für das Feld ist, das Sie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7428a-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="7428a-162">Geben Sie im Feld **Excel-Bereich** **CompanyURL_Value** ein.</span><span class="sxs-lookup"><span data-stu-id="7428a-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="7428a-163">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7428a-163">Select **OK**.</span></span>

    ![CompanyURL_Wertfeld in der Vorlagenstruktur hinzugefügt](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="7428a-165">Wählen Sie im Bereich **Vorlagenstruktur** die Schaltfläche Ellipsis (...) und dann **Bindungen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="7428a-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Ausgewählte Bindungen anzeigen](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="7428a-167">Der Bereich **Vorlagenstruktur** zeigt nun die Datenquellen an, die im zugrunde liegenden ER-Format verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7428a-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="7428a-168">Wählen Sie **CompanyInfo_Value** als Feld, das Sie an eine Datenquelle des zugrunde liegenden ER-Formats binden möchten.</span><span class="sxs-lookup"><span data-stu-id="7428a-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="7428a-169">Erweitern Sie im Abschnitt **Datenquellen** des Bereichs **Vorlagenstruktur** **Modell \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="7428a-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="7428a-170">Wählen Sie unter **CompanyInfo** den Eintrag **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="7428a-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![WebsiteURI Artikel ausgewählt](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="7428a-172">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="7428a-172">Select **Bind**.</span></span>
11. <span data-ttu-id="7428a-173">Wählen Sie im Bereich **Vorlagenstruktur** **Speichern**, und schließen Sie dann die Seite des BDM-Vorlageneditors.</span><span class="sxs-lookup"><span data-stu-id="7428a-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="7428a-174">Im Arbeitsbereich **Geschäftsdokumentenmanagement** zeigt die Registerkarte **Vorlage** im rechten Bereich die aktualisierte Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="7428a-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="7428a-175">Beachten Sie im Raster, dass das Feld **Status** für die bearbeitete Vorlage in **Entwurf** geändert wurde und das Feld **Revision** nicht mehr leer ist.</span><span class="sxs-lookup"><span data-stu-id="7428a-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="7428a-176">Diese Änderungen zeigen an, dass der Prozess der Bearbeitung dieser Vorlage gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="7428a-176">These changes indicate that the process of editing this template has been started.</span></span>

![Bearbeitete Vorlage im Arbeitsbereich Geschäftsdokumentenmanagement](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="7428a-178">Überprüfen der Unternehmenseinstellungen</span><span class="sxs-lookup"><span data-stu-id="7428a-178">Review company settings</span></span>

1.  <span data-ttu-id="7428a-179">Gehen Sie zu **Organisationsverwaltung \> Organisationen \> Juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="7428a-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="7428a-180">Überprüfen Sie unter **Kontaktinformationen** Inforegister, ob die Firmen-URL eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7428a-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Firmen-URL, die auf der Seite Juristische Personen eingegeben wurde.](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="7428a-182">Generieren Sie Geschäftsdokumente, um die aktualisierte Vorlage zu testen.</span><span class="sxs-lookup"><span data-stu-id="7428a-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="7428a-183">Ändern Sie in der Anwendung die Firma auf **USMF** und gehen Sie zu **Forderung \> Rechnungen \> Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="7428a-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="7428a-184">Wählen Sie Rechnung **FTI-00000002**, und wählen Sie dann **Druckverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="7428a-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="7428a-185">Erweitern Sie im linken Bereich **Modul - Debitorenbuchhaltung \> Dokumente \> Freitextrechnung**.</span><span class="sxs-lookup"><span data-stu-id="7428a-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="7428a-186">Wählen Sie unter **Freitextrechnung** die Ebene **Originalbeleg**, um den Umfang der zu bearbeitenden Rechnungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7428a-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="7428a-187">Wählen Sie im rechten Bereich im Feld **Berichtsformat** die Vorlage **Freitextrechnung (Excel) Contoso** für die angegebene Dokumentebene.</span><span class="sxs-lookup"><span data-stu-id="7428a-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Freitextrechnung (Excel) Contoso-Vorlage ausgewählt](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="7428a-189">Drücken Sie **Esc**, um die aktuelle Seite zu schließen.</span><span class="sxs-lookup"><span data-stu-id="7428a-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="7428a-190">Wählen Sie **Drucken \> Ausgewählt**.</span><span class="sxs-lookup"><span data-stu-id="7428a-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="7428a-191">Laden Sie das generierte Dokument herunter und öffnen Sie es in Excel.</span><span class="sxs-lookup"><span data-stu-id="7428a-191">Download the generated document, and open it in Excel.</span></span>

    ![Freitextrechnung in Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="7428a-193">Die geänderte Vorlage wird verwendet, um den Freitextrechnungsbericht für den ausgewählten Artikel zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7428a-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="7428a-194">Um zu analysieren, wie sich Änderungen, die Sie an der Vorlage vornehmen, auf diesen Bericht auswirken, führen Sie den Bericht in einer Anwendungssitzung unmittelbar nach der Änderung der Vorlage in einer anderen Anwendungssitzung aus.</span><span class="sxs-lookup"><span data-stu-id="7428a-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="7428a-195">Zugehörige Links</span><span class="sxs-lookup"><span data-stu-id="7428a-195">Related links</span></span>

[<span data-ttu-id="7428a-196">Überblick über die elektronische Berichterstellung (Electronic reporting, ER)</span><span class="sxs-lookup"><span data-stu-id="7428a-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7428a-197">Geschäftsdokumentverwaltung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="7428a-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="7428a-198">Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format</span><span class="sxs-lookup"><span data-stu-id="7428a-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]