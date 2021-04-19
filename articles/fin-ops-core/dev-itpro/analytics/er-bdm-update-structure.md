---
title: Struktur einer Geschäftsdokumentvorlage aktualisieren
description: In diesem Thema wird erläutert, wie Sie die Struktur einer Geschäftsdokumentvorlage mithilfe der Funktion zur Verwaltung von Geschäftsdokumenten aktualisieren.
author: NickSelin
ms.date: 11/19/2020
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
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750483"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="2a115-103">Struktur einer Geschäftsdokumentvorlage aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2a115-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2a115-104">Im Bereich **Vorlagenstruktur** des Editors für Vorlagen zur [Verwaltung von Geschäftsdokumenten](er-business-document-management.md) können Sie eine Geschäftsdokumentvorlage durch das [Hinzufügen neuer Felder](er-bdm-add-field-to-excel-template.md) zu einer Vorlage in Microsoft Excel ändern.</span><span class="sxs-lookup"><span data-stu-id="2a115-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="2a115-105">Die Struktur der Vorlage wird dann in Dynamics 365 Finance automatisch aktualisiert, damit sie die Änderungen widerspiegelt, die Sie im Bereich **Vorlagenstruktur** vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="2a115-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="2a115-106">Sie können eine Vorlage auch mithilfe der Office 365-Onlinefunktion ändern.</span><span class="sxs-lookup"><span data-stu-id="2a115-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="2a115-107">Beispielsweise können Sie dem bearbeitbaren Arbeitsblatt ein neues benanntes Element, beispielsweise ein Bild oder eine Form, hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2a115-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="2a115-108">In diesem Fall wird die Struktur der Vorlage in Finance nicht automatisch aktualisiert und das von Ihnen hinzugefügte Element wird nicht im Bereich **Vorlagenstruktur** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a115-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="2a115-109">Aktualisieren Sie die Vorlagenstruktur in Finance manuell, indem Sie **Struktur aktualisieren** auf der Seite des Vorlagen-Editors auswählen.</span><span class="sxs-lookup"><span data-stu-id="2a115-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="2a115-110">Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das folgende Beispiel abschließen.</span><span class="sxs-lookup"><span data-stu-id="2a115-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="2a115-111">Beispiel: Struktur einer Geschäftsdokumentvorlage aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2a115-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="2a115-112">Dieses Beispiel zeigt, wie ein Systemadministrator die Struktur einer Geschäftsdokumentvorlage in Finance aktualisieren kann, nachdem die Vorlage in Office Online geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2a115-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="2a115-113">In den folgenden Abschnitten werden die damit verbundenen Schritte erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a115-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="2a115-114">Eine Geschäftsdokumentvorlage zur Bearbeitung vorbereiten</span><span class="sxs-lookup"><span data-stu-id="2a115-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="2a115-115">Führen Sie die folgenden Prozeduren in [Geschäftsdokumentverwaltung – Übersicht](er-business-document-management.md) aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="2a115-116">Parameter der elektronischen Berichterstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2a115-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="2a115-117">Importieren von ER-Lösungen</span><span class="sxs-lookup"><span data-stu-id="2a115-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="2a115-118">Aktivieren der Geschäftsdokumentverwaltung</span><span class="sxs-lookup"><span data-stu-id="2a115-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="2a115-119">Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2a115-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="2a115-120">Eine Geschäftsdokumentvorlage bearbeiten</span><span class="sxs-lookup"><span data-stu-id="2a115-120">Edit a business document template</span></span>

1. <span data-ttu-id="2a115-121">Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="2a115-122">Wählen Sie auf der Seite **Neue Vorlage erstellen** die Vorlage **Freitextrechnung (EB-Beispiel) (Excel)** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="2a115-123">Wählen Sie **Dokument erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-123">Select **Create document**.</span></span>
4. <span data-ttu-id="2a115-124">Geben Sie in das Feld **Titel** den Text **FTR-Beispiel Litware** ein.</span><span class="sxs-lookup"><span data-stu-id="2a115-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="2a115-125">Wählen Sie **OK** aus, um die neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2a115-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2a115-126">Wenn Sie sich noch nicht bei Office Online angemeldet haben, werden Sie [zur Anmeldeseite von Office 365 weitergeleitet](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="2a115-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="2a115-127">Um zu Ihrer Finance-Umgebung zurückzukehren, wählen Sie die Schaltfläche **Zurück** in Ihrem Browser aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="2a115-128">Die neue Vorlage wird zur Bearbeitung in der eingebetteten Excel Online-Steuerung auf der Seite des Vorlagen-Editors geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2a115-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="2a115-129">[![Verwenden des Arbeitsbereichs zur Geschäftsdokumentverwaltung, um mit der Bearbeitung einer Geschäftsdokumentvorlage zu beginnen](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="2a115-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="2a115-130">Aktuelle Struktur der bearbeitbaren Vorlage überprüfen</span><span class="sxs-lookup"><span data-stu-id="2a115-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="2a115-131">Wählen Sie in Excel Online im Menüband auf der Registerkarte **Ansicht** in der Gruppe **Anzeigen** die Option **Rasterlinien** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="2a115-132">Wählen Sie in der bearbeitbaren Vorlage das Rechteck über dem Vorlagentitel aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="2a115-133">Dieses Rechteck ist ein Bild mit dem Namen **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="2a115-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="2a115-134">Wenn der Bereich **Vorlagenstruktur** ausgeblendet ist, wählen Sie **Struktur anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="2a115-135">Erweitern Sie im Bereich **Vorlagenstruktur** die Struktur **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="2a115-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="2a115-136">Beachten Sie, dass in der Vorlagenstruktur in Finance das Element **rptHeaderCompLogo** als untergeordnetes Element von **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1** dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2a115-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="2a115-137">[![Verwenden des Arbeitsbereichs zur Verwaltung von Geschäftsdokumenten zum Überprüfen der aktuellen Struktur einer bearbeitbaren Vorlage](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="2a115-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="2a115-138">Struktur einer Geschäftsdokumentvorlage durch Löschen eines Bilds aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2a115-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="2a115-139">Wählen Sie in Excel Online in der bearbeitbaren Vorlage das Bild **rptHeaderCompLogo** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="2a115-140">Führen Sie einen der folgenden Schritte aus, um das ausgewählte Bild aus der bearbeitbaren Vorlage zu löschen:</span><span class="sxs-lookup"><span data-stu-id="2a115-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="2a115-141">Drücken Sie auf der Tastatur die **ENTF**-Taste.</span><span class="sxs-lookup"><span data-stu-id="2a115-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="2a115-142">Wählen Sie das Bild aus, halten Sie es gedrückt (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Ausschneiden** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2a115-143">Das Element **rptHeaderCompLogo** ist in der Vorlagenstruktur in Finance derzeit noch vorhanden, obwohl das Bild nicht mehr in der Excel-Vorlage enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2a115-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="2a115-144">Wählen Sie **Struktur aktualisieren** aus, um die Struktur der bearbeitbaren Vorlage in Excel und Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="2a115-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="2a115-145">Erweitern Sie im Bereich **Vorlagenstruktur** die Struktur **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="2a115-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="2a115-146">Beachten Sie, dass das Element **rptHeaderCompLogo** in der Vorlagenstruktur in Finance nicht mehr enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2a115-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="2a115-147">[![Verwenden des Arbeitsbereichs zur Geschäftsdokumentverwaltung, um ein Bild aus einer Geschäftsdokumentvorlage zu löschen](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="2a115-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="2a115-148">Struktur einer Geschäftsdokumentvorlage durch Hinzufügen eines Bilds aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2a115-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="2a115-149">Wählen Sie in Excel Online im Menüband auf der Registerkarte **Einfügen** in der Gruppe **Abbildungen** die Option **Bild** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="2a115-150">Wählen Sie **Datei auswählen** aus, navigieren Sie zu dem Bild, das Sie hinzufügen möchten, wählen Sie es aus und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="2a115-151">Wählen Sie **Einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="2a115-151">Select **Insert**.</span></span>
4. <span data-ttu-id="2a115-152">Verschieben Sie das neue Bild, bis es sich an der richtigen Stelle befindet.</span><span class="sxs-lookup"><span data-stu-id="2a115-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="2a115-153">Standardmäßig wird das Bild von Excel benannt.</span><span class="sxs-lookup"><span data-stu-id="2a115-153">By default, Excel names the picture.</span></span> <span data-ttu-id="2a115-154">Beispielsweise könnte das Bild den Namen **Bild 2** erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a115-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="2a115-155">Wählen Sie **Struktur aktualisieren** aus, um die Struktur der bearbeitbaren Vorlage in Excel und Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="2a115-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="2a115-156">Erweitern Sie im Bereich **Vorlagenstruktur** die Struktur **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="2a115-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="2a115-157">Beachten Sie, dass das neue Bild jetzt als ein Element in der Vorlagenstruktur in Finance enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2a115-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="2a115-158">[![Verwenden des Arbeitsbereichs zur Geschäftsdokumentverwaltung, um ein Bild zu einer Geschäftsdokumentvorlage hinzuzufügen](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="2a115-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="2a115-159">Zugehörige Links</span><span class="sxs-lookup"><span data-stu-id="2a115-159">Related links</span></span>

[<span data-ttu-id="2a115-160">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="2a115-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2a115-161">Geschäftsdokumentverwaltung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="2a115-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]