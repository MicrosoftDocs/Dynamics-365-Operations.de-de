---
title: Neues Projekt erstellen
description: Dieser Artikel bietet Informationen dazu, wie ein neues Projekt erstellt wird.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760553"
---
# <a name="create-a-new-project"></a><span data-ttu-id="87dd8-103">Neues Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="87dd8-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87dd8-104">Führen Sie die folgenden Schritte aus, um ein neues Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="87dd8-105">Wählen Sie auf der Seite **Projektmanagement** **Neues Projekt** aus und geben Sie die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="87dd8-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="87dd8-106">**Projekttype:** Nach Aufwand</span><span class="sxs-lookup"><span data-stu-id="87dd8-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="87dd8-107">**Projektname:** XYZ Upgrade-Phase 2</span><span class="sxs-lookup"><span data-stu-id="87dd8-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="87dd8-108">**Projektgruppe:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="87dd8-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="87dd8-109">**Projektvertragskennung:** 00000002</span><span class="sxs-lookup"><span data-stu-id="87dd8-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="87dd8-110">Wählen Sie **Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="87dd8-111">Ressource zum Projekt zuweisen</span><span class="sxs-lookup"><span data-stu-id="87dd8-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="87dd8-112">Wählen Sie auf der Seite **Arbeitskräfte** in der Liste **Arbeitskräfte** den Datensatz für die Arbeitskraft aus, für die Sie zuvor Kompetenzen eingerichtet haben aus, und öffnen Sie den Arbeitskraftdatensatz.</span><span class="sxs-lookup"><span data-stu-id="87dd8-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="87dd8-113">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Projekt** in der Gruppe **Einrichten** **Projekte zuweisen** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="87dd8-114">Filtern Sie auf der Seite **Projektzuweisungen für Ressourcenüberprüfung** auf der Registerkarte **Projekte** im Feld **Fügen Sie das Projekt zu den ausgewählten Projekten hinzu** nach dem **XYZ Upgrade-Phase 2**-Projekt.</span><span class="sxs-lookup"><span data-stu-id="87dd8-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="87dd8-115">Wählen Sie im Bereich **Verbleibende Projekte** ein Projekt aus, und klicken Sie anschließend auf den Pfeil, um es dem Bereich **Ausgewählte Projekte** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="87dd8-116">Bei Bedarf können Sie auch Kategorien für eine Ressource zuweisen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="87dd8-117">Der Kategorietyp ist **Kosten** oder **Umsatzerlös**.</span><span class="sxs-lookup"><span data-stu-id="87dd8-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="87dd8-118">Der Kategorietyp wird von Ihrer Organisation festgelegt.</span><span class="sxs-lookup"><span data-stu-id="87dd8-118">The category type is determined by your organization.</span></span> <span data-ttu-id="87dd8-119">Wenn einer Ressource keine Kategorien zugewiesen sind, sucht Finance nach der Standardkategorie für Stundenpreise für die Kosten und den Umsatzerlös.</span><span class="sxs-lookup"><span data-stu-id="87dd8-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="87dd8-120">Einrichten von Projektressourcen und Rollenmerkmalen</span><span class="sxs-lookup"><span data-stu-id="87dd8-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="87dd8-121">Ein Projektmanager kann die Projektressourcenfunktionen verwenden, um die Rollen erstellen, die für das Projekt erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="87dd8-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="87dd8-122">Rollen können verwendet werden, wenn bestätigte Ressourcen während der Ressourcenreservierungen noch unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="87dd8-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="87dd8-123">Rollen können verwendet werden, um Ressourcen vorübergehend als geplante Ressourcen zu reservieren, um die Projektplanungsphasen fortsetzen zu können.</span><span class="sxs-lookup"><span data-stu-id="87dd8-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="87dd8-124">[![Beispiel einer Rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="87dd8-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="87dd8-125">**Szenario:** Contoso wurde für ein Aufwandsprojekt gebucht, das eine genehmigte Projektcharter hat.</span><span class="sxs-lookup"><span data-stu-id="87dd8-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="87dd8-126">Der Juniorprojektmanager arbeitet noch am Umfang des Projekts.</span><span class="sxs-lookup"><span data-stu-id="87dd8-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="87dd8-127">Der Ressourcen-Manager identifiziert derzeit zugewiesene Ressourcen, die reserviert für die Arbeit an dem neuen Projekt zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="87dd8-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="87dd8-128">Aufgrund der kritischen Natur des Projekts forderte der Projektträger einen Senior-Projektmanager als eine der Rollen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="87dd8-129">Der Ressourcen-Manager muss die neue Ressource erwerben und die Rolle im System definieren, falls der Juniorprojektmanager die Ressourceninformationen während der Projektplanung benötigt.</span><span class="sxs-lookup"><span data-stu-id="87dd8-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="87dd8-130">Die folgenden Schritte zeigen, wie der Ressourcen-Manager den Senior-Projektmanager einrichten und Ressourcenmerkmale zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="87dd8-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="87dd8-131">Später kann die Rolle verwendet werden, um für verfügbare Ressourcen zu finden, die die erforderlichen Ressourcenkompetenzen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="87dd8-132">Wählen Sie auf der Seite **Einstellungsrollen** **Neu** aus, und geben Sie die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="87dd8-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="87dd8-133">**Rollenkennung:** Senior Project Manager</span><span class="sxs-lookup"><span data-stu-id="87dd8-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="87dd8-134">**Beschreibung:** Senior Project Manager</span><span class="sxs-lookup"><span data-stu-id="87dd8-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="87dd8-135">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-135">Select **Create**.</span></span>
3. <span data-ttu-id="87dd8-136">Wählen Sie die Rolle für den **Senior-Projektmanager** aus und anschließend **Merkmale konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="87dd8-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="87dd8-137">Wählen Sie im Feld **Merkmalstyp** die Option **Qualifikation**.</span><span class="sxs-lookup"><span data-stu-id="87dd8-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="87dd8-138">Geben Sie im Feld **Verfügbare Merkmale** die Qualifikation ein, nach der gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="87dd8-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="87dd8-139">Wählen Sie im Feld **Merkmalstyp** die Option **Bescheinigung** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="87dd8-140">Geben Sie im **Verfügbare Merkmale**-Feld die Bescheinigung ein, die Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="87dd8-141">Projektressource zum Projekt zuweisen</span><span class="sxs-lookup"><span data-stu-id="87dd8-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="87dd8-142">Wählen Sie auf der Seite **Alle Projekte** das Projekt **XYZ Upgrade-Phase 2** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="87dd8-143">Klicken Sie auf der Registerkarte **Projektteam und Planung** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="87dd8-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="87dd8-144">Wählen Sie im Feld **Rolle** **Teammitglied** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="87dd8-145">Wählen Sie **Aus Kalender buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="87dd8-146">Klicken Sie auf der Seite **Ressourcenverfügbarkeit** auf **Einstellungen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="87dd8-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="87dd8-147">Geben Sie auf der **Ansichtseinstellungen anpassen**-Seite die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="87dd8-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="87dd8-148">**Format für Datumsbereichsansicht:** Tag</span><span class="sxs-lookup"><span data-stu-id="87dd8-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="87dd8-149">**Verfügbarkeitsbeschreibungen anzeigen**: Ja</span><span class="sxs-lookup"><span data-stu-id="87dd8-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="87dd8-150">**Verbleibende Kapazität anzeigen**: Ja</span><span class="sxs-lookup"><span data-stu-id="87dd8-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="87dd8-151">Wählen Sie in der Liste der Ressourcen eine Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="87dd8-152">Wählen Sie **Verbindlich buchen** und **Vollständige Kapazität** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="87dd8-153">Zuweisen einer Ressource zu einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="87dd8-153">Assign a resource to a default role</span></span>

<span data-ttu-id="87dd8-154">Um Projekt- und Ressourcen-Manager zu unterstützen, können Sie die zu einem Projekt reservierbaren Ressourcen detaillierter darstellen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="87dd8-155">Sie können eine standardmäßige Rolle zu einer vorhandenen Ressource oder zu einer neu abgerufenen Ressource zuordnen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="87dd8-156">Wenn Sie beispielsweise als Daniel eingestellt wurde, weist er Erfahrung und Fähigkeiten, um die der Business Analysten-Rolle ein.</span><span class="sxs-lookup"><span data-stu-id="87dd8-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="87dd8-157">Ressourcen-Manager Der zugewiesene Rolle diese als Daniels Standardrolle zu.</span><span class="sxs-lookup"><span data-stu-id="87dd8-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="87dd8-158">Daher ist Leiterin des Ressourcenmanagements Daniel einem Pool der Business Analysten hinzu, hinzufügen, die verfügbar sind, für Projekte zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="87dd8-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="87dd8-159">Während der Ressourcenreservierung können Projektmanager die Rollenressourcen filtern, die verfügbar sind, um an Projekten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="87dd8-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="87dd8-160">Sie können diese Informationen als als Kriterium verwenden, wenn sie Multikriterienentscheidungsanalysen für die Ressourcenerfüllung ausführen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="87dd8-161">Sie können andere Ressourcenmerkmale dem Filter für die Suche nach Ressourcen hinzufügen, die eine bestimmte Ausbildung, Qualifikationen und Erfahrungen für ein bestimmtes Projekt besitzen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="87dd8-162">**Szenario:** Ein genehmigtes Projekt wurde gestartet, und die Senior-Projektmanager wurde während der Projektplanungsphase als geplante Ressource reserviert.</span><span class="sxs-lookup"><span data-stu-id="87dd8-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="87dd8-163">Der Ressourcen-Manager hat nun eine Ressource abgerufen, um die Rolle Senio-Projektmanager zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="87dd8-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="87dd8-164">Wählen Sie auf der Seite **Ressourcenliste** **Daniel Goldschmidt** aus.</span><span class="sxs-lookup"><span data-stu-id="87dd8-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="87dd8-165">Wählen Sie auf der Seite **Ressourcenrolle** **Neu** aus, und geben Sie die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="87dd8-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="87dd8-166">**Gültigkeit:** Geben Sie das aktuelle Datum ein.</span><span class="sxs-lookup"><span data-stu-id="87dd8-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="87dd8-167">**Ablauf:** Geben Sie **Nie** ein.</span><span class="sxs-lookup"><span data-stu-id="87dd8-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="87dd8-168">**Rolle:** Geben Sie **Senior-Projektmanager** ein.</span><span class="sxs-lookup"><span data-stu-id="87dd8-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="87dd8-169">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="87dd8-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="87dd8-170">Fügen Sie auf der **Kompetenzen**-Registerkarte die **ProjectMgmt**-Qualifikation und die **PMP**-Bescheinigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="87dd8-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
