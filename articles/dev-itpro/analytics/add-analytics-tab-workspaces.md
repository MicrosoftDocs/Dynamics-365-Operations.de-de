---
title: "Über Power BI Embedded Analysen zu Arbeitsbereichen hinzufügen"
description: "Dieses Thema zeigt, wie Sie der Registerkarte Analysen eines Arbeitsbereichs einen Power BI-Bericht hinzufügen."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Platform, UnifiedOperations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e819aafbdf55fbc2a6dc996d275244de1e11d89b
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="a4a44-103">Über Power BI Embedded Analysen zu Arbeitsbereichen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a4a44-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a4a44-104">Diese Funktion wird in Dynamics 365 for Finance and Operations (Version 7.2 und höher) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4a44-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

# <a name="introduction"></a><span data-ttu-id="a4a44-105">Einführung</span><span class="sxs-lookup"><span data-stu-id="a4a44-105">Introduction</span></span>
<span data-ttu-id="a4a44-106">Dieses Thema zeigt, wie Sie der Registerkarte **Analysen** eines Arbeitsbereichs einen Microsoft Power BI-Bericht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="a4a44-107">Für das hier gezeigte Beispiel erweitern wir den Arbeitsbereich **Reservierungsverwaltung** in der Anwendung Flottenmanagement, um der Registerkarte **Analysen** einen analytischen Arbeitsbereich hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

# <a name="prerequisites"></a><span data-ttu-id="a4a44-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a4a44-108">Prerequisites</span></span>
+ <span data-ttu-id="a4a44-109">Zugriff auf eine Entwicklerumgebung mit Plattform-Update 8 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a4a44-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="a4a44-110">Einen Analysebericht (.pbix-Datei), der mit Microsoft Power BI Desktop erstellt wurde, und der ein Datenmodell verwendet, das von der Entitätsspeicher-Datenbank gespeist wird.</span><span class="sxs-lookup"><span data-stu-id="a4a44-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

# <a name="overview"></a><span data-ttu-id="a4a44-111">Überblick</span><span class="sxs-lookup"><span data-stu-id="a4a44-111">Overview</span></span>
<span data-ttu-id="a4a44-112">Egal, ob Sie einen vorhandenen Anwendungsarbeitsbereich erweitern oder einen eigenen neuen Arbeitsbereich anlegen, können Sie eingebettete analytische Ansichten nutzen, um informative und interaktive Ansichten Ihrer Geschäftsdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="a4a44-113">Der Prozess für das Hinzufügen einer Registerkarte mit analytischem Arbeitsbereich umfasst 4 Schritte.</span><span class="sxs-lookup"><span data-stu-id="a4a44-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="a4a44-114">Eine .pbix-Datei als Dynamics 365-Ressource hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="a4a44-115">Eine Registerkarte für einen analytischen Arbeitsbereich definieren.</span><span class="sxs-lookup"><span data-stu-id="a4a44-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="a4a44-116">Die .pbix-Ressource in die Registerkarte mit dem Arbeitsbereich einbetten.</span><span class="sxs-lookup"><span data-stu-id="a4a44-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="a4a44-117">Optional: Erweiterungen hinzufügen, um die Ansicht zu personalisieren.</span><span class="sxs-lookup"><span data-stu-id="a4a44-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="a4a44-118">Weitere Informationen zum Erstellen von analytischen Berichten finden Sie unter [Erste Schritte mit Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a4a44-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="a4a44-119">Diese Seite enthält wichtige Informationen, die Ihnen helfen, attraktive Lösungen für analytische Berichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

# <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="a4a44-120">Eine .pbix-Datei als Ressource hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a4a44-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="a4a44-121">Bevor Sie anfangen, müssen Sie den Power BI-Bericht erstellen oder erhalten, den Sie in den Arbeitsbereich einbetten wollen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="a4a44-122">Weitere Informationen zum Erstellen von analytischen Berichten finden Sie unter [Erste Schritte mit Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a4a44-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>
 
<span data-ttu-id="a4a44-123">Gehen Sie wie folgt vor, um eine .pbix-Datei als Visual Studio-Projektartefakt einzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="a4a44-124">Erstellen Sie ein neues Projekt im entsprechenden Modell.</span><span class="sxs-lookup"><span data-stu-id="a4a44-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="a4a44-125">Wählen Sie das Projekt im Projektmappen-Explorer aus, klicken Sie mit der rechten Maustaste und wählen Sie dann **Hinzufügen** > **Neues Element**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="a4a44-126">Wählen Sie im Dialogfeld **Neues Element hinzufügen** unter **Operations-Artefakte** die Vorlage **Ressource** aus.</span><span class="sxs-lookup"><span data-stu-id="a4a44-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="a4a44-127">Geben Sie einen Namen ein, der für die Referenzierung des Berichts in X++-Metadaten verwendet wird, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialogfeld Neues Element hinzufügen](media/analytical-workspace-add.png)

5. <span data-ttu-id="a4a44-129">Suchen Sie die .pbix-Datei, die die Definition des analytischen Berichts enthält, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Dialogfeld Auswählen einer Ressourcendatei](media/analytical-workspace-select-resource.png)
  
<span data-ttu-id="a4a44-131">Nachdem Sie die .pbix-Datei als Dynamics 365-Ressource hinzugefügt haben, können Sie die Berichte in Arbeitsbereiche einbetten und unter Verwendung von Menüeinträgen direkte Links hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

# <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="a4a44-132">Hinzufügen eines Registerkarten-Steuerelements zu einem Anwendungsarbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a4a44-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="a4a44-133">In diesem Beispiel erweitern wir den Arbeitsbereich **Reservierungsverwaltung** im Flottenmanagement-Modell, indem wir der Definition des Formulars **FMClerkWorkspace** die Registerkarte **Analysen** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>
 
<span data-ttu-id="a4a44-134">Die folgende Abbildung zeigt, wie das Formular **FMClerkWorkspace** im Designer in Microsoft Visual Studio aussieht.</span><span class="sxs-lookup"><span data-stu-id="a4a44-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Formular FMClerkWorkspace vor den Änderungen](media/analytical-workspace-definition-before.png)

<span data-ttu-id="a4a44-136">Gehen Sie wie folgt vor, um die Formulardefinition für den Arbeitsbereich **Reservierungsverwaltung** zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a4a44-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a4a44-137">Öffnen Sie den Formulardesigner, um die Designdefinition zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a4a44-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a4a44-138">In dieser Designdefinition wählen Sie das oberste Element aus, **Design | Muster: Arbeitsbereich operational**</span><span class="sxs-lookup"><span data-stu-id="a4a44-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="a4a44-139">Klicken Sie mit der rechten Maustaste und wählen Sie dann **Neu** > **Registerkarte**, um das neue Steuerelement **FormTabControl1** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="a4a44-140">Wählen Sie im Formulardesigner **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="a4a44-141">Klicken Sie mit der rechten Maustaste und wählen Sie dann **Neue Registerkartenseite**, um eine neue Registerkartenseite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="a4a44-142">Geben Sie der Registerkarte einen sprechenden Namen, wie beispielsweise **Arbeitsbereich**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="a4a44-143">Wählen Sie im Formulardesigner **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="a4a44-144">Klicken Sie mit der rechten Maustaste und wählen Sie dann **Neue Registerkartenseite**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="a4a44-145">Geben Sie der Registerkarte einen sprechenden Namen, wie beispielsweise **Analysen**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="a4a44-146">Wählen Sie im Formulardesigner **Analysen (Registerkartenseite)**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="a4a44-147">Setzen Sie die Legen Sie die **Überschrift**-Eigenschaft auf **Analysen**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="a4a44-148">Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie dann **Neu** > **Gruppe**, um ein neues Formulargruppensteuerelement hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="a4a44-149">Geben Sie der Formulargruppe einen sprechenden Namen, wie beispielsweise **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="a4a44-150">Wählen Sie im Formulardesigner **PanoramaBody (Registerkarte)** und ziehen Sie das Steuerelement auf die Registerkarte **Arbeitsbereich**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="a4a44-151">In dieser Designdefinition wählen Sie das oberste Element aus, **Design | Muster: Arbeitsbereich operational**</span><span class="sxs-lookup"><span data-stu-id="a4a44-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="a4a44-152">Klicken Sie mit der rechten Maustaste und wählen Sie dann **Muster entfernen**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="a4a44-153">Klicken Sie erneut mit der rechten Maustaste und wählen Sie dann **Muster hinzufügen** > **Arbeitsbereich mit Registerkarten**.</span><span class="sxs-lookup"><span data-stu-id="a4a44-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="a4a44-154">Führen Sie einen Build aus, um Ihre Änderungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-154">Perform a build to verify your changes.</span></span>
 
<span data-ttu-id="a4a44-155">Die folgende Abbildung zeigt, wie das Design nach Anwendung dieser Änderungen aussieht.</span><span class="sxs-lookup"><span data-stu-id="a4a44-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace nach den Änderungen](media/analytical-workspace-definition-after.png)

<span data-ttu-id="a4a44-157">Nachdem Sie die Steuerelemente für das Formular hinzugefügt haben, die für die Einbettung des Arbeitsbereichberichts verwendet werden, müssen Sie die Größe des übergeordneten Steuerelements definieren, sodass es zum Layout passt.</span><span class="sxs-lookup"><span data-stu-id="a4a44-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="a4a44-158">Standardmäßig werden die Seite **Filter** und die Seite **Registerkarte** auf dem Bericht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4a44-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="a4a44-159">Sie können die Sichtbarkeit dieser Steuerelemente jedoch abhängig vom Zielpublikum des Berichts abändern.</span><span class="sxs-lookup"><span data-stu-id="a4a44-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>
 
> [!NOTE]
> <span data-ttu-id="a4a44-160">Für eingebettete Arbeitsbereiche empfehlen wir, der Konsistenz halber Erweiterungen zu verwenden, um die Seiten **Filter** und **Registerkarte** auszublenden.</span><span class="sxs-lookup"><span data-stu-id="a4a44-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>
 
<span data-ttu-id="a4a44-161">Damit haben Sie die Aufgabe fertiggestellt, die Definition des Anwendungsformulars zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a4a44-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="a4a44-162">Weitere Informationen zur Verwendung von Erweiterungen für Anpassungen finden Sie in [Anpassung: Überlagerungen und Erweiterungen](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4a44-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="a4a44-163">Hinzufügen einer X++-Geschäftslogik, um ein Viewer-Steuerelement einzubetten</span><span class="sxs-lookup"><span data-stu-id="a4a44-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="a4a44-164">Gehen Sie wie folgt vor, um eine Geschäftslogik hinzuzufügen, die das Steuerelement für den Bericht-Viewer initialisiert, das in den Arbeitsbereich **Reservierungsverwaltung** eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="a4a44-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a4a44-165">Öffnen Sie den Formulardesigner **FMClerkWorkspace**, um die Designdefinition zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a4a44-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a4a44-166">Drücken Sie F7, um auf den Code hinter der Codedefinition zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="a4a44-167">Fügen Sie den folgenden X++-Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4a44-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="a4a44-168">Führen Sie einen Build aus, um Ihre Änderungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="a4a44-169">Damit haben Sie die Aufgabe abgeschlossen, die Geschäftslogik hinzuzufügen, mit der das eingebettete Steuerelement für den Bericht-Viewer initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a4a44-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="a4a44-170">Die folgende Abbildung zeigt, wie der Arbeitsbereich nach Anwendung dieser Änderungen aussieht.</span><span class="sxs-lookup"><span data-stu-id="a4a44-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![In den Arbeitsbereich eingebetteter Bericht](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="a4a44-172">Über die Registerkarten des Arbeitsbereichs unterhalb der Seitenüberschrift können Sie auf die vorhandene sofort ausgeführte Ansicht zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a4a44-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

# <a name="reference"></a><span data-ttu-id="a4a44-173">Referenz</span><span class="sxs-lookup"><span data-stu-id="a4a44-173">Reference</span></span>

## <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="a4a44-174">Die Methode PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="a4a44-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="a4a44-175">Dieser Abschnitt enthält Informationen über die Helferklasse, mit der ein Power BI-Bericht (.pbix-Ressource) in ein Formular-Gruppensteuerelement eingebettet wird.</span><span class="sxs-lookup"><span data-stu-id="a4a44-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

### <a name="syntax"></a><span data-ttu-id="a4a44-176">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4a44-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a><span data-ttu-id="a4a44-177">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a44-177">Parameters</span></span>

| <span data-ttu-id="a4a44-178">Name</span><span class="sxs-lookup"><span data-stu-id="a4a44-178">Name</span></span> | <span data-ttu-id="a4a44-179">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4a44-179">Description</span></span> |
|---|---|
| <span data-ttu-id="a4a44-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="a4a44-180">resourceName</span></span> | <span data-ttu-id="a4a44-181">Der Name der .pbix-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a4a44-181">The name of the .pbix resource.</span></span> |
| <span data-ttu-id="a4a44-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="a4a44-182">formGroupControl</span></span> | <span data-ttu-id="a4a44-183">Das Formular-Gruppensteuerelement, auf das das Power BI-Berichtssteuerelement angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4a44-183">The form group control to apply the Power BI report control to.</span></span> |
| <span data-ttu-id="a4a44-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="a4a44-184">defaultPageName</span></span> | <span data-ttu-id="a4a44-185">Der Standardseitenname.</span><span class="sxs-lookup"><span data-stu-id="a4a44-185">The default page name.</span></span> |
| <span data-ttu-id="a4a44-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="a4a44-186">showFilterPane</span></span> | <span data-ttu-id="a4a44-187">Ein boolescher Wert, der angibt, ob der Filterbereich angezeigt (**true**) oder ausgeblendet (**false**) werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4a44-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="a4a44-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="a4a44-188">showNavPane</span></span> | <span data-ttu-id="a4a44-189">Ein boolescher Wert, der angibt, ob der Navigationsbereich angezeigt (**true**) oder ausgeblendet (**false**) werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4a44-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="a4a44-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="a4a44-190">defaultFilters</span></span> | <span data-ttu-id="a4a44-191">Die Standardfilter für den Power BI-Bericht.</span><span class="sxs-lookup"><span data-stu-id="a4a44-191">The default filters for the Power BI report.</span></span> |

