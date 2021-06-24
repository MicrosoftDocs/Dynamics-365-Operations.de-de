---
title: Geben Sie Fähigkeiten ein
description: Werke und Manager können Fähigkeiten in Dynamics 365 Human Resources eingeben.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193976"
---
# <a name="enter-skills"></a><span data-ttu-id="2d774-103">Geben Sie Fähigkeiten ein</span><span class="sxs-lookup"><span data-stu-id="2d774-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2d774-104">Sie können Zielqualifikationen oder tatsächliche Qualifikationen für Arbeitskräfte, Bewerber oder Kontakte in Dynamics 365 Human Resources eingeben.</span><span class="sxs-lookup"><span data-stu-id="2d774-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2d774-105">Eine Zielqualifikation ist eine Qualifikation, die eine Person plant zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="2d774-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="2d774-106">Eine tatsächliche Qualifikation ist eine Qualifikation, die eine Person derzeit hat.</span><span class="sxs-lookup"><span data-stu-id="2d774-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="2d774-107">Erstellen Sie einen Workflow, um Fähigkeiten automatisch zu genehmigen</span><span class="sxs-lookup"><span data-stu-id="2d774-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="2d774-108">Um Fähigkeiten einzugeben, ohne dass eine Genehmigung erforderlich ist, müssen Sie einen Workflow erstellen, um Fähigkeiten automatisch zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="2d774-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="2d774-109">Von Arbeitskräften eingegebene Fähigkeiten erfordern immer die Zustimmung des Managers.</span><span class="sxs-lookup"><span data-stu-id="2d774-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="2d774-110">Dieser Workflow genehmigt nur automatisch Fähigkeiten, die von Managern im Namen ihrer Mitarbeiter eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="2d774-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="2d774-111">Wählen Sie im Arbeitsbereich **Personalverwaltung** die Registerkarte **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="2d774-112">Unter **Einrichtung** wählen Sie **Personalressourcen-Workflows**.</span><span class="sxs-lookup"><span data-stu-id="2d774-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="2d774-113">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-113">Select **New**.</span></span>

4. <span data-ttu-id="2d774-114">In dem Bereich **Workflow erstellen** wählen Sie **Qualifikationen Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="2d774-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="2d774-115">[![Wählen Sie Workflow für Arbeitskräfte-Qualifikationen aus](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="2d774-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="2d774-116">In dem Dialog **Diese Datei öffnen?** wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="2d774-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="2d774-117">Geben Sie Ihre Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2d774-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="2d774-118">Wählen Sie im Workflow-Editor das Workflowelement **Qualifikationen genehmigen** und ziehen Sie es auf den Canvas.</span><span class="sxs-lookup"><span data-stu-id="2d774-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="2d774-119">[![Wählen Sie das Workflowelement Qualifikationen genehmigen aus](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="2d774-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="2d774-120">Verbinden Sie das Element **Start** mit dem Element **Qualifikationen genehmigen 1** und verbinden Sie dann das Element **Fähigkeiten genehmigen 1** mit dem Element **Ende**.</span><span class="sxs-lookup"><span data-stu-id="2d774-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="2d774-121">Möglicherweise müssen Sie nach unten scrollen, um das Element **Ende** zu sehen.</span><span class="sxs-lookup"><span data-stu-id="2d774-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="2d774-122">Sie können es näher an die anderen Elemente ziehen.</span><span class="sxs-lookup"><span data-stu-id="2d774-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="2d774-123">[![Workflow-Elemente verbinden](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="2d774-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="2d774-124">Doppelklicken Sie auf das Workflowelement **Qualifikationen 1 genehmigen** und klicken Sie dann mit der rechten Maustaste auf das Element **Schritt 1**.</span><span class="sxs-lookup"><span data-stu-id="2d774-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="2d774-125">Klicken Sie mit der rechten Maustaste auf das Element **Schritt 1**, und klicken Sie anschließend auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="2d774-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="2d774-126">In dem **Eigenschaften** Fenster wählen Sie **Bedingung** auf der linken Navigationsleiste.</span><span class="sxs-lookup"><span data-stu-id="2d774-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="2d774-127">Wählen Sie die Option **Diesen Schritt nur ausführen, wenn folgende Bedingungen erfüllt sind**.</span><span class="sxs-lookup"><span data-stu-id="2d774-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="2d774-128">Wählen Sie **Bedingung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2d774-128">Select **Add condition**.</span></span> <span data-ttu-id="2d774-129">Nach **Wo** wählen Sie **Self-Service-Fähigkeiten der Mitarbeiter** und dann **Mitarbeiter Self-Service-Fähigkeiten.Person**.</span><span class="sxs-lookup"><span data-stu-id="2d774-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="2d774-130">Nach **ist** wählen Sie **Feld** und dann **Benutzer-zu-Person-Beziehung.Person**.</span><span class="sxs-lookup"><span data-stu-id="2d774-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="2d774-131">[![Bedingung angeben](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="2d774-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="2d774-132">Wählen Sie **Zuweisung** auf der linken Navigationsleiste.</span><span class="sxs-lookup"><span data-stu-id="2d774-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="2d774-133">Auf der Registerkarte **Zuweisungstyp** wählen Sie **Hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="2d774-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="2d774-134">Auf der Registerkarte **Hierarchieauswahl** im Feld **Hierarchietyp:** wählen Sie **Führungshierarchie** aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="2d774-135">[![Geben Sie die Führungshierarchie an](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="2d774-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="2d774-136">Wählen Sie **Schließen** und wählen Sie **Workflow** im Canvas Breadcrumb, und wählen Sie dann **Speichern und schließen**.</span><span class="sxs-lookup"><span data-stu-id="2d774-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="2d774-137">Weitere Informationen über das Erstellen von Workflows finden Sie unter [Workflow-Systemübersicht](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2d774-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="2d774-138">Geben Sie Fähigkeiten für eine Arbeitskraft ein</span><span class="sxs-lookup"><span data-stu-id="2d774-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="2d774-139">Hier können Sie eine Arbeitskraft auswählen.</span><span class="sxs-lookup"><span data-stu-id="2d774-139">Select a worker.</span></span>

2. <span data-ttu-id="2d774-140">In der Aktionsleiste der Seite **Arbeitskraft** wählen Sie **Person** und dann **Qualifikationen**.</span><span class="sxs-lookup"><span data-stu-id="2d774-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="2d774-141">Auf der Seite **Qualifikationen** füllen Sie die folgenden Felder für jede Fertigkeit aus:</span><span class="sxs-lookup"><span data-stu-id="2d774-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="2d774-142">**Qualifikation**: Wählen Sie eine Qualifikation aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="2d774-143">**Ebenentyp**: Wählen Sie **Tatsächlich** für eine Qualifikation aus, die die Arbeitskraft bereits hat, oder wählen Sie **Ziel** für eine Qualifikation, auf die die Arbeitskraft hinarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2d774-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="2d774-144">**Ebene**: Wählen Sie eine Ebene für die Qualifikation der Arbeitskraft aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="2d774-145">**Ebenendatum**: Wählen Sie ein Datum im Kalender aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="2d774-146">**Prüfer**: Wählen Sie gegebenenfalls einen Prüfer aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="2d774-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="2d774-147">Sie können Ihre Suche filtern.</span><span class="sxs-lookup"><span data-stu-id="2d774-147">You can filter your search.</span></span>
   - <span data-ttu-id="2d774-148">**Anzahl Jahre Erfahrung**: Geben Sie Anzahl Jahre für die Erfahrung ein.</span><span class="sxs-lookup"><span data-stu-id="2d774-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="2d774-149">**Verifiziert**: Wenn die Fähigkeit überprüft wurde, aktivieren Sie das Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="2d774-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="2d774-150">**Geprüft von**: Geben Sie den Namen des Prüfers ein.</span><span class="sxs-lookup"><span data-stu-id="2d774-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="2d774-151">Wenn Sie mit der Eingabe von Qualifikationen fertig sind, wählen Sie **speichern**.</span><span class="sxs-lookup"><span data-stu-id="2d774-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d774-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d774-152">See also</span></span>

[<span data-ttu-id="2d774-153">Fähigkeiten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2d774-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="2d774-154">Qualifikationen aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="2d774-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]