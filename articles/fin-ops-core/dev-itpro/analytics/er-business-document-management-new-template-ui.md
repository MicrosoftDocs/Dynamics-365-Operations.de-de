---
title: Benutzeroberfläche im Stil von Microsoft Office für Dokumente in der Geschäftsdokumentverwaltung
description: Dieses Thema erklärt, wie die neue Benutzeroberfläche in der Geschäftsdokumentverwaltung-Funktion des Frameworks für elektronische Berichterstellung (EB) verwendet wird.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881035"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="70464-103">Benutzeroberfläche im Stil von Microsoft Office für Dokumente in der Geschäftsdokumentverwaltung</span><span class="sxs-lookup"><span data-stu-id="70464-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70464-104">Mit der Geschäftsdokumentverwaltung können geschäftliche Benutzer Geschäftsdokumentvorlagen mit einem Microsoft 365-Dienst oder der entsprechenden Microsoft Office-Desktopanwendung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="70464-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="70464-105">Bearbeitungen können Entwurfsänderungen oder neue Bereitstellungen umfassen. Benutzer können auch Platzhalter hinzufügen, um zusätzliche Daten aufzunehmen, ohne den Quellcode ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="70464-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="70464-106">Weitere Informationen zum Arbeiten mit der Geschäftsdokumentenverwaltung finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="70464-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="70464-107">Die neue Benutzeroberfläche ist übersichtlicher und benutzerfreundlicher.</span><span class="sxs-lookup"><span data-stu-id="70464-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="70464-108">Der **Geschäftsdokument**-Bereich zeigt nur die Vorlagen, die für den aktuellen Anbieter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="70464-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="70464-109">In der vorherigen Benutzeroberfläche wurden auf der Registerkarte **Vorlage** alle Vorlagen aufgelistet, die für Anbieter verfügbar waren.</span><span class="sxs-lookup"><span data-stu-id="70464-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="70464-110">Außerdem wurden alle Vorlagen angezeigt, die von Benutzern mit derselben Rolle erstellt und bearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="70464-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="70464-111">Sie können die Schaltfläche **Neues Dokument** verwenden, um eine Vorlage in einer Formatkonfiguration der elektronischen Berichtserstellung (EB) zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="70464-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="70464-112">Im Beispiel dieses Themas ist der Anbieter Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70464-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="70464-113">Alternativ können Sie eine Vorlage erstellen, indem Sie Ihre eigene Vorlage im Excel-Format hochladen.</span><span class="sxs-lookup"><span data-stu-id="70464-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="70464-114">Das Video zum Thema [ein neues Geschäftsdokument mit der Geschäftsdokumentverwaltung erstellen](https://youtu.be/gAIYl-mM_pw) (siehe oben) ist in der [Finance and Operations-Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) YouTube verfügbar.</span><span class="sxs-lookup"><span data-stu-id="70464-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="70464-115">Neue Benutzeroberfläche für die Geschäftsdokumentverwaltung zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="70464-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="70464-116">Um die neue Dokument-Benutzeroberfläche in der Geschäftsdokumentverwaltung zu verwenden, müssen Sie die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70464-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="70464-117">Befolgen Sie diese Schritte, um diese Funktion für alle juristischen Personen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70464-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="70464-118">Wählen Sie im Arbeitsbereich **Funktionsverwaltung** auf der Registerkarte **Alle** die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="70464-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="70464-119">Wählen Sie **Jetzt aktivieren** aus, um die ausgewählte Fähigkeit zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70464-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="70464-120">Aktualisieren Sie die Seite, um auf die neue Funktion zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="70464-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="70464-121">Vorlagen anderer Anbieter bearbeiten</span><span class="sxs-lookup"><span data-stu-id="70464-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="70464-122">Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.</span><span class="sxs-lookup"><span data-stu-id="70464-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbeitsbereich Geschäftsdokumentenverwaltung](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="70464-124">Wählen Sie in der Registerkarte **Auswählen** das Dokument aus, das als Vorlage verwendet werden soll, und wählen Sie **Dokument erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="70464-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialogfeld „Geschäftsdokumente“](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="70464-126">Ändern Sie im neuen Dialogfeld im Feld **Titel** den Titel nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="70464-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="70464-127">Der Titeltext wird zum Benennen der neuen ER-Formatkonfiguration verwendet, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70464-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="70464-128">Die Entwurfsversion dieser Konfiguration (**Debitoren-FTI-Bericht (GER) – Kopie**) enthält die bearbeitete Vorlage und wird verwendet, um dieses ER-Format für den aktuellen Benutzer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="70464-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="70464-129">Die ursprüngliche Vorlage von der Basis-ER-Formatkonfiguration wird verwendet, um dieses ER-Format für jeden anderen Benutzer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="70464-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="70464-130">Ändern Sie im Feld **Name** den Namen der ersten Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70464-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="70464-131">Aktualisieren Sie im Feld **Kommentar** die Anmerkungen für die Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70464-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="70464-132">Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="70464-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialogfeld zur Dokumentenerstellung](./media/BDM_overview_new_template3.png)

<span data-ttu-id="70464-134">Die Schaltfläche **Neues Dokument** wird verwendet, um eine Vorlage in einer ER-Formatkonfiguration zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="70464-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="70464-135">In diesem Beispiel ist der Anbieter Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70464-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="70464-136">Wenn Sie auf **Neues Dokument** klicken, sehen Sie alle Vorlagen, die sich im Besitz aktueller und anderer Anbieter befinden.</span><span class="sxs-lookup"><span data-stu-id="70464-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="70464-137">Nachdem Sie die Vorlage ausgewählt haben, wird sie zur Bearbeitung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="70464-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="70464-138">Die bearbeitete Vorlage wird dann in einer neuen ER-Formatkonfiguration gespeichert, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="70464-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="70464-139">Eine Vorlage hochladen, die ein vorhandenes Excel-Format verwendet</span><span class="sxs-lookup"><span data-stu-id="70464-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="70464-140">Gehen Sie wie folgt vor, um die erforderlichen Informationen bereitzustellen, bevor Sie eine Vorlage hochladen.</span><span class="sxs-lookup"><span data-stu-id="70464-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="70464-141">Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.</span><span class="sxs-lookup"><span data-stu-id="70464-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbeitsbereich Geschäftsdokumentenverwaltung](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="70464-143">Wählen Sie auf der Seite **Neue Vorlage erstellen** die Registerkarte **Hochladen**, dann die Registerkarte **Vorlage** und schließlich **Durchsuchen** aus, um die Excel-Datei zu finden und auszuwählen, die Sie als Vorlage verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="70464-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="70464-144">Im Abschnitt **Vorlage** werden die Felder **Titel** und **Beschreibung** automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="70464-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="70464-145">Sie geben den Namen und die Beschreibung der neuen EB-Formatkonfiguration an, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70464-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="70464-146">Sie können diese Felder bei Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="70464-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="70464-147">Im Abschnitt **Dokumenttyp** geben Sie im Feld **Name** den Typ des Geschäftsdokuments an.</span><span class="sxs-lookup"><span data-stu-id="70464-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="70464-148">Dieser Wert wird verwendet, um die richtige Datenquelle (d. h. die EB-Modellkonfiguration) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="70464-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Registerkarte „Vorlage“](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="70464-150">Wählen Sie auf der Registerkarte **Datenquelle** das Inforegister **Filter** und dann **Filter anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="70464-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="70464-151">Im Abschnitt **Datenquelle** wird das Feld **Name** automatisch ausgefüllt oder Sie können einen Wert manuell auswählen.</span><span class="sxs-lookup"><span data-stu-id="70464-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="70464-152">Mit dem Filter können Sie nach der entsprechenden Datenquelle nach Name, Beschreibung, Länder-/Regionscode und Geschäftsdokumenttyp filtern.</span><span class="sxs-lookup"><span data-stu-id="70464-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Registerkarte „Datenquelle“](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="70464-154">Das Inforegister **Filter** wird verwendet, um die richtige Datenquelle (d. h. die EB-Modellkonfiguration) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="70464-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="70464-155">Sie können alle Filterfelder bearbeiten, um die am besten geeignete Datenquelle für das Dokument zu finden, das Sie hochladen.</span><span class="sxs-lookup"><span data-stu-id="70464-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="70464-156">Die Bedingungen auf dem Inforegister **Filter** werden als **ODER**-Bedingungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="70464-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="70464-157">Auf der Registerkarte **Zuordnung** wählen Sie **Automatische Erkennung** aus.</span><span class="sxs-lookup"><span data-stu-id="70464-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="70464-158">Das Feld **Stammdefinition** wird automatisch ausgefüllt oder Sie können einen Wert manuell auswählen.</span><span class="sxs-lookup"><span data-stu-id="70464-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="70464-159">Diese Registerkarte zeigt die Endzuordnung für die Elemente aus der Vorlage und dem Modell.</span><span class="sxs-lookup"><span data-stu-id="70464-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Registerkarte „Zuordnung“](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="70464-161">Die Zuordnung im Abschnitt **Vorlagenstruktur** verwendet die vollständige Übereinstimmung der Beschriftungen oder Beschreibungen in der Datenquelle in der Sprache des Benutzers und im Zellennamen in der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="70464-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="70464-162">Wählen Sie **Dokument erstellen** aus, um zu bestätigen, dass Sie eine Vorlage erstellen und den Bearbeitungsprozess starten möchten.</span><span class="sxs-lookup"><span data-stu-id="70464-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="70464-163">Weitere Informationen finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="70464-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="70464-164">Wenn es in der elektronischen Berichterstellung keinen Anbieter gibt, können Sie einen erstellen.</span><span class="sxs-lookup"><span data-stu-id="70464-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="70464-165">Wenn es keinen aktiven Anbieter gibt, können Sie einen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70464-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="70464-166">Um einen Anbieter zu erstellen, ändern Sie den Namen des Anbieters im Feld **Name**, aktualisieren Sie die Internetadresse des neuen Anbieters im Feld **Internetadresse** und bestätigen Sie mit **OK**.</span><span class="sxs-lookup"><span data-stu-id="70464-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Einen neuen Anbieter in BDM erstellen](./media/bdm_create_provider.png)
    
- <span data-ttu-id="70464-168">Um einen vorhandenen Anbieter zu aktivieren, wählen Sie den Namen des Anbieters im Feld **Konfigurationsanbieter** aus und aktivieren Sie den Anbieter dann mit **OK**.</span><span class="sxs-lookup"><span data-stu-id="70464-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Einen Anbieter in BDM aktivieren](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="70464-170">Jede BDM-Vorlage verweist auf den Anbieter als Autor der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="70464-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="70464-171">Aus diesem Grund ist für die Vorlage ein aktiver Anbieter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="70464-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
