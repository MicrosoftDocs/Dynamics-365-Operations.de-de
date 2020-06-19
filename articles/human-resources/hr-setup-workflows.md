---
title: Workflows zum Verwalten von Mitarbeiterinformationen verwenden
description: In diesem Artikel wird erläutert, wie die Sie Workflowfunktion für die Personalverwaltung verwenden können, um Mitarbeiterdaten zu verwalten. So können Sie beispielsweise einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, der gestartet wird, wenn Mitarbeiter Ihren Datensatz ändern.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 539f4c77244d2e5590e3994dedc0725e5a80093b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429173"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="62af6-104">Workflows zum Verwalten von Mitarbeiterinformationen verwenden</span><span class="sxs-lookup"><span data-stu-id="62af6-104">Use workflows to manage employee information</span></span>

<span data-ttu-id="62af6-105">In diesem Artikel wird erläutert, wie die Sie Workflowfunktion für die Personalverwaltung verwenden können, um Mitarbeiterdaten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="62af6-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="62af6-106">So können Sie beispielsweise einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, der gestartet wird, wenn Mitarbeiter Ihren Datensatz ändern.</span><span class="sxs-lookup"><span data-stu-id="62af6-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="62af6-107">Die Workflowfunktion für die Personalverwaltung beinhaltet zahlreiche Workflows zur Verwaltung von Personalverwaltungsaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="62af6-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="62af6-108">Darüber hinaus stehen zahlreiche Optionen zur Verfügung. So können Sie bestimmte Workflows ändern und einer Berichterstellungshierarchie zuordnen.</span><span class="sxs-lookup"><span data-stu-id="62af6-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="62af6-109">Workflows sind verfügbar, um die Verwaltung von Änderungen an mehreren Standardtypen der Mitarbeiterdaten zu unterstützten.</span><span class="sxs-lookup"><span data-stu-id="62af6-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="62af6-110">Sie können einen Workflow einer Position zuordnen.</span><span class="sxs-lookup"><span data-stu-id="62af6-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="62af6-111">Wenn Mitarbeiter dann ihren Datensatz ändern, wird ein Workflow gestartet, der eine Genehmigung erfordert, bevor die neuen Informationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="62af6-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="62af6-112">Workflows sind für die folgenden Informationsarten vordefiniert, damit Sie Änderungen effizient verwalten können und Ihre Mitarbeiterdaten immer korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="62af6-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="62af6-113">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="62af6-113">Identification numbers</span></span>
-   <span data-ttu-id="62af6-114">Kurse</span><span class="sxs-lookup"><span data-stu-id="62af6-114">Courses</span></span>
-   <span data-ttu-id="62af6-115">Ausbildung</span><span class="sxs-lookup"><span data-stu-id="62af6-115">Education</span></span>
-   <span data-ttu-id="62af6-116">Bild</span><span class="sxs-lookup"><span data-stu-id="62af6-116">Image</span></span>
-   <span data-ttu-id="62af6-117">Ausgeliehene Artikel</span><span class="sxs-lookup"><span data-stu-id="62af6-117">Loaned items</span></span>
-   <span data-ttu-id="62af6-118">Berufserfahrung</span><span class="sxs-lookup"><span data-stu-id="62af6-118">Professional experience</span></span>
-   <span data-ttu-id="62af6-119">Projekterfahrung</span><span class="sxs-lookup"><span data-stu-id="62af6-119">Project experience</span></span>
-   <span data-ttu-id="62af6-120">Qualifikationen</span><span class="sxs-lookup"><span data-stu-id="62af6-120">Skills</span></span>
-   <span data-ttu-id="62af6-121">Vertrauensposition</span><span class="sxs-lookup"><span data-stu-id="62af6-121">Positions of trust</span></span>
-   <span data-ttu-id="62af6-122">Personalverwaltungsaktivitäten</span><span class="sxs-lookup"><span data-stu-id="62af6-122">Human resources actions</span></span>
-   <span data-ttu-id="62af6-123">Kursregistrierung</span><span class="sxs-lookup"><span data-stu-id="62af6-123">Course registration</span></span>

<span data-ttu-id="62af6-124">Wenn Mitarbeiter eingestellt oder übertragen werden oder das Beschäftigungsverhältnis beendet wird, kann der Workflow einen Prüfprozess enthalten.</span><span class="sxs-lookup"><span data-stu-id="62af6-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="62af6-125">Auf diese Weise kann ein Dokument überarbeitet oder die Bedingungen für eine Aktivität als Teil des Workflows definiert werden.</span><span class="sxs-lookup"><span data-stu-id="62af6-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="62af6-126">Nach Abschluss des Prüfprozesses wird das Dokument oder die Aktivität abgeschlossen. Der Workflow wird dann zum Schritt der abschließenden Genehmigung verschoben.</span><span class="sxs-lookup"><span data-stu-id="62af6-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="62af6-127">Zuordnen eines Workflows zu einer Positionshierarchie</span><span class="sxs-lookup"><span data-stu-id="62af6-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="62af6-128">Sie können einen Workflow einer beliebigen Hierarchie zuordnen, die Sie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="62af6-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="62af6-129">Wird beispielsweise eine Position einer Matrixberichterstellungshierarchie zugeordnet, können Sie einen Workflow konfigurieren, der Ausgaben für ein bestimmtes Projekt an den Projektleiter weiterleitet und nicht an den Vorgesetzten des Mitarbeiters, der dieser Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="62af6-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="62af6-130">Zum Erstellen oder Ändern eines vorhandenen Workflows klicken Sie auf der Seite **Personalverwaltungsworkflow** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="62af6-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="62af6-131">Wählen Sie einen Workflow in der Liste aus, um den Workflowdesigner zu starten.</span><span class="sxs-lookup"><span data-stu-id="62af6-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="62af6-132">Sie können den Designer verwenden, um einen neuen Workflow zu erstellen oder die Schritte in einem vorhandenen Workflow zu ändern.</span><span class="sxs-lookup"><span data-stu-id="62af6-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="62af6-133">Wenn Sie einen vorhandenen Workflow ändern, werden die Änderungen als neue Version gespeichert.</span><span class="sxs-lookup"><span data-stu-id="62af6-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="62af6-134">Daher können Sie immer wieder zu einer früheren Version wechseln, falls notwendig.</span><span class="sxs-lookup"><span data-stu-id="62af6-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="62af6-135">Konfigurieren eines Personalverwaltungsworkflows</span><span class="sxs-lookup"><span data-stu-id="62af6-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="62af6-136">Um einen grundlegenden Workflow zu konfigurieren, der startet, wenn Mitarbeiter Änderungen an ihrer persönlichen Kennung fordern, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="62af6-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="62af6-137">Klicken Sie auf der Seite **Personalverwaltungsworkflows** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="62af6-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="62af6-138">Wählen Sie in der Liste der verfügbaren Workflows **Kennnummern** aus.</span><span class="sxs-lookup"><span data-stu-id="62af6-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="62af6-139">Klicken Sie auf **Ausführen**, um den Workflowdesigner zu starten, und geben Sie nach Aufforderung Ihren Benutzernamen und Ihr Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="62af6-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="62af6-140">Verschieben Sie das **Kennungsnummer genehmigen**-Element von der Liste der Workflowelemente in die Designercanvas.</span><span class="sxs-lookup"><span data-stu-id="62af6-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="62af6-141">Verbinden Sie das Genehmigungselement mit **Start** und **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="62af6-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="62af6-142">Doppelklicken Sie auf die Option für **Element genehmigen**, klicken Sie dann mit der rechten Maustaste, und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="62af6-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="62af6-143">Gehen Sie folgendermaßen vor, um Anweisungen für die Arbeitsaufgabe hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="62af6-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="62af6-144">Wählen Sie **Zuweisung** und anschließend **Hierarchie** unter dem Zuweisungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="62af6-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="62af6-145">Wählen Sie unter der **Hierarchie**-Auswahl die Option **Konfigurierbare Hierarchie** aus.</span><span class="sxs-lookup"><span data-stu-id="62af6-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="62af6-146">Fügen Sie eine Beendigungsbedingung hinzu, und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62af6-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="62af6-147">Führen Sie alle zusätzlichen Anweisungen zu Ende aus (es sollten keine zusätzlichen Warnungen vorhanden sein).</span><span class="sxs-lookup"><span data-stu-id="62af6-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="62af6-148">Klicken Sie auf **Speichern und schließen**.</span><span class="sxs-lookup"><span data-stu-id="62af6-148">Click **Save and close**.</span></span> <span data-ttu-id="62af6-149">Aktivieren Sie den neuen Workflow, wenn das Dialogfeld geöffnet wird, und wählen Sie **Als aktiv festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="62af6-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="62af6-150">Wechseln Sie zu **Personalverwaltung** &gt; **Positionen** &gt; **Hierarchietypen für die Position**.</span><span class="sxs-lookup"><span data-stu-id="62af6-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="62af6-151">Wählen Sie **Matrix** aus.</span><span class="sxs-lookup"><span data-stu-id="62af6-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="62af6-152">Fügen Sie den **Arbeitskraft-Kennungsnummer**-Workflow zur Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="62af6-152">Add the **Worker identification number** workflow to the list.</span></span>




