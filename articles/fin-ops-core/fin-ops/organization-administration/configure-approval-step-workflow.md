---
title: Genehmigungsschritte in einem Workflow konfigurieren
description: Dieses Thema erläutert, wie Sie die Eigenschaften eines Genehmigungsschritts konfigurieren können.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5bd5300a061e12ccabdea83c20863c95e15fe19
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124680"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="84157-103">Genehmigungsschritte in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="84157-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84157-104">Dieses Thema erläutert, wie Sie die Eigenschaften eines Genehmigungsschritts konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="84157-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="84157-105">Klicken Sie zum Konfigurieren eines Genehmigungsschritts im Workflow-Editor mit der rechten Maustaste auf den Genehmigungsschritt, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="84157-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="84157-106">Verwenden Sie dann die folgenden Verfahren, um die Eigenschaften des Genehmigungsschritts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="84157-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="84157-107">Benennen des Schritts</span><span class="sxs-lookup"><span data-stu-id="84157-107">Name the step</span></span>
<span data-ttu-id="84157-108">Gehen Sie folgendermaßen vor, um einen Namen für den Genehmigungsschritt einzugeben.</span><span class="sxs-lookup"><span data-stu-id="84157-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="84157-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="84157-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="84157-110">Geben Sie im Feld **Name** einen eindeutigen Namen für den Genehmigungsschritt ein.</span><span class="sxs-lookup"><span data-stu-id="84157-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="84157-111">Eingeben einer Betreffzeile und von Anweisungen</span><span class="sxs-lookup"><span data-stu-id="84157-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="84157-112">Sie müssen eine Betreffzeile und Anweisungen für Benutzer eingeben, die dem Genehmigungsschritt zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="84157-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="84157-113">Wenn Sie z. B. einen Genehmigungsschritt für Bestellanforderungen konfigurieren, werden dem Benutzer, der dem Schritt zugewiesen ist, die Betreffzeile und Anweisungen auf der Seite **Bestellanforderungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84157-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="84157-114">Die Betreffzeile wird in einer Statusleiste auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84157-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="84157-115">Der Benutzer kann nun auf das Symbol in der Statusleiste klicken, um die Anweisungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="84157-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="84157-116">Gehen Sie folgendermaßen vor, um eine Betreffzeile und Anweisungen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="84157-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="84157-117">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="84157-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="84157-118">Geben Sie im Feld **Betreff für die Arbeitsaufgabe** die Betreffzeile ein.</span><span class="sxs-lookup"><span data-stu-id="84157-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="84157-119">Zum Personalisieren der Betreffzeile können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="84157-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="84157-120">Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Betreffzeile Benutzern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="84157-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="84157-121">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="84157-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="84157-122">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="84157-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="84157-123">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="84157-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="84157-124">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="84157-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="84157-125">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="84157-125">Click **Insert**.</span></span>

4. <span data-ttu-id="84157-126">Führen Sie die folgenden Schritte aus, um Übersetzungen der Betreffzeile hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="84157-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="84157-127">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="84157-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="84157-128">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="84157-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="84157-129">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="84157-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="84157-130">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="84157-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="84157-131">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 3 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="84157-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="84157-132">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="84157-132">Click **Close**.</span></span>

5. <span data-ttu-id="84157-133">Geben Sie im Feld **Arbeitsaufgabenanweisungen** die Arbeitsanweisungen ein.</span><span class="sxs-lookup"><span data-stu-id="84157-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="84157-134">Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="84157-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="84157-135">Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt.</span><span class="sxs-lookup"><span data-stu-id="84157-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="84157-136">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="84157-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="84157-137">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="84157-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="84157-138">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="84157-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="84157-139">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="84157-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="84157-140">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="84157-140">Click **Insert**.</span></span>

7. <span data-ttu-id="84157-141">Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="84157-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="84157-142">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="84157-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="84157-143">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="84157-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="84157-144">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="84157-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="84157-145">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="84157-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="84157-146">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 6 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="84157-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="84157-147">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="84157-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="84157-148">Zuweisen des Genehmigungsschritts</span><span class="sxs-lookup"><span data-stu-id="84157-148">Assign the approval step</span></span>

<span data-ttu-id="84157-149">Gehen Sie folgendermaßen vor, um anzugeben, wem der Genehmigungsschritt zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="84157-150">Klicken Sie im linken Bereich auf **Zuweisung**.</span><span class="sxs-lookup"><span data-stu-id="84157-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="84157-151">Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 3 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="84157-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="84157-152">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="84157-152">Option</span></span></th>
    <th><span data-ttu-id="84157-153">Benutzer, denen der Genehmigungsschritt zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="84157-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="84157-154">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="84157-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="84157-155">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="84157-155">Participant</span></span></td>
    <td><span data-ttu-id="84157-156">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="84157-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84157-157">Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem der Schritt zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="84157-158">Wählen Sie in der Liste <strong>Teilnehmer</strong> den Typ der Gruppe oder der Rolle aus, dem der Schritt zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84157-159">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="84157-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="84157-160">Benutzer in einer bestimmten Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="84157-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84157-161">Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem der Schritt zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="84157-162">Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="84157-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="84157-163">Diese Namen stellen Benutzer dar, denen der Schritt zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="84157-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="84157-164">Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="84157-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="84157-165">Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="84157-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="84157-166">Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="84157-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="84157-167">Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="84157-168">Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich der Schritt zugewiesen werden soll:</span><span class="sxs-lookup"><span data-stu-id="84157-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="84157-169"><strong>Allen abgerufenen Benutzern zuordnen</strong> – Der Schritt wird allen Benutzern im Bereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="84157-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="84157-170"><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Der Schritt wird nur dem letzten Benutzer im Bereich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="84157-171"><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Der Schritt wird keinem Benutzer im Bereich zugewiesen, der eine bestimmte Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="84157-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="84157-172">Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="84157-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84157-173">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="84157-173">Workflow user</span></span></td>
    <td><span data-ttu-id="84157-174">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="84157-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="84157-175">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="84157-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84157-176">Benutzer</span><span class="sxs-lookup"><span data-stu-id="84157-176">User</span></span></td>
    <td><span data-ttu-id="84157-177">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="84157-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84157-178">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="84157-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="84157-179">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Systembenutzer.</span><span class="sxs-lookup"><span data-stu-id="84157-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="84157-180">Wählen Sie die Benutzer aus, um den Schritt zuzuweisen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="84157-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="84157-181">Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Bearbeiten oder Beantworten von Dokumenten zur Verfügung steht, die den Genehmigungsschritt erreichen.</span><span class="sxs-lookup"><span data-stu-id="84157-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="84157-182">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="84157-182">Select one of the following options:</span></span>

    - <span data-ttu-id="84157-183">**Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Beantworten hat.</span><span class="sxs-lookup"><span data-stu-id="84157-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="84157-184">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="84157-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84157-185">**Tage** – Geben Sie die Anzahl der Tage ein, die der Benutzer zum Beantworten hat.</span><span class="sxs-lookup"><span data-stu-id="84157-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="84157-186">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="84157-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84157-187">**Wochen** – Geben Sie die Anzahl der Wochen ein, die der Benutzer zum Beantworten hat.</span><span class="sxs-lookup"><span data-stu-id="84157-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="84157-188">**Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer antworten muss.</span><span class="sxs-lookup"><span data-stu-id="84157-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="84157-189">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats antworten soll.</span><span class="sxs-lookup"><span data-stu-id="84157-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="84157-190">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer antworten muss.</span><span class="sxs-lookup"><span data-stu-id="84157-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="84157-191">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember antworten soll.</span><span class="sxs-lookup"><span data-stu-id="84157-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="84157-192">Wenn der Benutzer das Dokument nicht innerhalb der vorgesehenen Zeit bearbeitet, ist das Dokument überfällig.</span><span class="sxs-lookup"><span data-stu-id="84157-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="84157-193">Ein überfälliges Dokument wird basierend auf den ausgewählten Optionen im Bereich **Eskalation** der Seite eskaliert.</span><span class="sxs-lookup"><span data-stu-id="84157-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="84157-194">Wenn Sie den Genehmigungsschritt mehreren Benutzern oder einer Gruppe von Benutzern zugewiesen haben, klicken Sie auf die Registerkarte **Vollendungsrichtlinie**, und wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="84157-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="84157-195">**Einzelne genehmigende Person** – Die Aktivität für das Dokument wird von der ersten antwortenden Person bestimmt.</span><span class="sxs-lookup"><span data-stu-id="84157-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="84157-196">Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht.</span><span class="sxs-lookup"><span data-stu-id="84157-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="84157-197">Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="84157-198">Falls Saskia die erste Person ist, die das Dokument beantwortet, wird ihre Aktivität für das Dokument übernommen.</span><span class="sxs-lookup"><span data-stu-id="84157-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="84157-199">Falls Saskia das Dokument ablehnt, wird es abgelehnt und an Steffen zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="84157-200">Wenn Saskia das Dokument genehmigt, wird es zur Genehmigung an Anne gesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Workflow mit Genehmigungsprozesses](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="84157-202">**Mehrheit der genehmigenden Personen** – Die Aktivität für das Dokument wird bei Antwort der Mehrheit der genehmigenden Personen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="84157-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="84157-203">Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht.</span><span class="sxs-lookup"><span data-stu-id="84157-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="84157-204">Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="84157-205">Falls Saskia und Jens die ersten beiden genehmigenden Personen sind, die antworten, wird ihre Aktivität für das Dokument übernommen.</span><span class="sxs-lookup"><span data-stu-id="84157-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="84157-206">Wird das Dokument von Saskia genehmigt, von Jens jedoch abgelehnt, wird es abgelehnt und an Steffen zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="84157-207">Wird das Dokument sowohl von Saskia als auch von Jens genehmigt, wird es zur Genehmigung an Anne gesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="84157-208">**Prozentsatz der Genehmiger** – Die Aktivität für das Dokument wird bei Antwort eines bestimmten Prozentsatzes der genehmigenden Personen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="84157-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="84157-209">Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht.</span><span class="sxs-lookup"><span data-stu-id="84157-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="84157-210">Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen, und Sie haben **50** als Prozentsatz eingegeben.</span><span class="sxs-lookup"><span data-stu-id="84157-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="84157-211">Falls Saskia und Jens die ersten beiden genehmigenden Personen sind, die antworten, wird ihre Aktivität für das Dokument übernommen, da sie die Anforderung von 50 Prozent der genehmigenden Personen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="84157-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="84157-212">Wird das Dokument von Saskia genehmigt, von Jens jedoch abgelehnt, wird es abgelehnt und an Steffen zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="84157-213">Wird das Dokument sowohl von Saskia als auch von Jens genehmigt, wird es zur Genehmigung an Anne gesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="84157-214">**Alle genehmigenden Personen** – Alle genehmigenden Personen müssen das Dokument genehmigen.</span><span class="sxs-lookup"><span data-stu-id="84157-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="84157-215">Andernfalls kann der Workflow nicht fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="84157-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="84157-216">Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht.</span><span class="sxs-lookup"><span data-stu-id="84157-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="84157-217">Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="84157-218">Wird das Dokument von Saskia und Jens genehmigt, von Bastian jedoch abgelehnt, wird es abgelehnt und an Steffen zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="84157-219">Wird das Dokument von Saskia, Jens und Bastian genehmigt, wird es zur Genehmigung an Anne gesendet.</span><span class="sxs-lookup"><span data-stu-id="84157-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="84157-220">Angeben, wann der Genehmigungsschritt erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="84157-220">Specify when the approval step is required</span></span>

<span data-ttu-id="84157-221">Sie können angeben, wann der Genehmigungsschritt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="84157-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="84157-222">Der Genehmigungsschritt kann immer oder nur dann erforderlich sein, wenn bestimmte Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="84157-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="84157-223">Der Genehmigungsschritt ist immer erforderlich</span><span class="sxs-lookup"><span data-stu-id="84157-223">The approval step is always required</span></span>

<span data-ttu-id="84157-224">Gehen Sie folgendermaßen vor, wenn der Genehmigungsschritt immer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="84157-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="84157-225">Klicken Sie im linken Bereich auf **Bedingung**.</span><span class="sxs-lookup"><span data-stu-id="84157-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="84157-226">Wählen Sie die Option **Diesen Schritt immer ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="84157-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="84157-227">Der Genehmigungsschritt ist unter bestimmten Bedingungen erforderlich</span><span class="sxs-lookup"><span data-stu-id="84157-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="84157-228">Der Genehmigungsschritt, den Sie konfigurieren, ist möglicherweise nur erforderlich, wenn bestimmte Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="84157-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="84157-229">Beispiel: Sie konfigurieren einen Genehmigungsschritt für einen Workflow für Bestellanforderungen und möchten, dass der Genehmigungsschritt nur dann ausgeführt wird, wenn die Bestellanforderung einen Betrag von 10.000 Euro überschreitet.</span><span class="sxs-lookup"><span data-stu-id="84157-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="84157-230">Gehen Sie folgendermaßen vor, um anzugeben, wann der Genehmigungsschritt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="84157-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="84157-231">Klicken Sie im linken Bereich auf **Bedingung**.</span><span class="sxs-lookup"><span data-stu-id="84157-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="84157-232">Wählen Sie die Option **Diesen Schritt nur ausführen, wenn folgende Bedingungen erfüllt sind** aus.</span><span class="sxs-lookup"><span data-stu-id="84157-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="84157-233">Geben Sie eine Bedingung ein.</span><span class="sxs-lookup"><span data-stu-id="84157-233">Enter a condition.</span></span>
4. <span data-ttu-id="84157-234">Geben Sie alle notwendigen zusätzlichen Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="84157-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="84157-235">Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="84157-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="84157-236">Klicken Sie auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="84157-236">Click **Test**.</span></span>
    2. <span data-ttu-id="84157-237">Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="84157-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="84157-238">Klicken Sie auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="84157-238">Click **Test**.</span></span> <span data-ttu-id="84157-239">Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="84157-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="84157-240">Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="84157-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="84157-241">Festlegen der Vorgehensweise für überfällige Dokumente</span><span class="sxs-lookup"><span data-stu-id="84157-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="84157-242">Wenn ein Benutzer ein Dokument nicht innerhalb der vorgesehenen Zeit bearbeitet, ist das Dokument überfällig.</span><span class="sxs-lookup"><span data-stu-id="84157-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="84157-243">Ein überfälliges Dokument kann eskaliert oder automatisch einem anderen Benutzer zur Genehmigung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="84157-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="84157-244">Führen Sie die folgenden Schritte aus, um das Dokument zu eskalieren, wenn es überfällig ist.</span><span class="sxs-lookup"><span data-stu-id="84157-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="84157-245">Klicken Sie im linken Bereich auf **Eskalation**.</span><span class="sxs-lookup"><span data-stu-id="84157-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="84157-246">Aktivieren Sie das Kontrollkästchen **Eskalationspfad verwenden**, um einen Eskalationspfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84157-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="84157-247">Das Dokument wird automatisch den im Eskalationspfad aufgeführten Benutzern zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="84157-248">Die folgende Tabelle stellt z. B. einen Eskalationspfad dar.</span><span class="sxs-lookup"><span data-stu-id="84157-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="84157-249">Sequenz</span><span class="sxs-lookup"><span data-stu-id="84157-249">Sequence</span></span> | <span data-ttu-id="84157-250">Eskalationspfad</span><span class="sxs-lookup"><span data-stu-id="84157-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="84157-251">1</span><span class="sxs-lookup"><span data-stu-id="84157-251">1</span></span>        | <span data-ttu-id="84157-252">Zuweisen zu: Doris</span><span class="sxs-lookup"><span data-stu-id="84157-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="84157-253">2</span><span class="sxs-lookup"><span data-stu-id="84157-253">2</span></span>        | <span data-ttu-id="84157-254">Zuweisen zu: Elke</span><span class="sxs-lookup"><span data-stu-id="84157-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="84157-255">3</span><span class="sxs-lookup"><span data-stu-id="84157-255">3</span></span>        | <span data-ttu-id="84157-256">Abschließende Aktivität: Ablehnen</span><span class="sxs-lookup"><span data-stu-id="84157-256">Final action: Reject</span></span> |

    <span data-ttu-id="84157-257">In diesem Beispiel wird das überfällige Dokument Doris zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="84157-258">Antwortet Doris nicht innerhalb der vorgesehenen Zeit, wird das Dokument Elke zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="84157-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="84157-259">Antwortet Elke nicht innerhalb der vorgesehenen Zeit, wird das Dokument abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="84157-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="84157-260">Klicken Sie auf **Eskalation hinzufügen**, um dem Eskalationspfad einen Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="84157-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="84157-261">Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 4 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="84157-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="84157-262">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="84157-262">Option</span></span></th>
    <th><span data-ttu-id="84157-263">Benutzer, denen das Dokument eskaliert wird</span><span class="sxs-lookup"><span data-stu-id="84157-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="84157-264">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="84157-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="84157-265">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="84157-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="84157-266">Benutzer in einer bestimmten Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="84157-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84157-267">Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, an den das Dokument eskaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="84157-268">Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="84157-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="84157-269">Diese Namen stellen Benutzer dar, an die das Dokument unter Umständen eskaliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="84157-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="84157-270">Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="84157-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="84157-271">Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="84157-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="84157-272">Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="84157-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="84157-273">Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84157-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="84157-274">Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, an welche Benutzer im Bereich das Dokument eskaliert werden soll:</span><span class="sxs-lookup"><span data-stu-id="84157-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="84157-275"><strong>Allen abgerufenen Benutzern zuordnen</strong> – Das Dokument wird an alle Benutzer im Bereich eskaliert.</span><span class="sxs-lookup"><span data-stu-id="84157-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="84157-276"><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Das Dokument wird nur an den letzten Benutzer im Bereich eskaliert.</span><span class="sxs-lookup"><span data-stu-id="84157-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="84157-277"><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Das Dokument wird an keinen Benutzer im Bereich eskaliert, der eine bestimmte Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="84157-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="84157-278">Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="84157-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84157-279">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="84157-279">Workflow user</span></span></td>
    <td><span data-ttu-id="84157-280">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="84157-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="84157-281">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="84157-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84157-282">Benutzer</span><span class="sxs-lookup"><span data-stu-id="84157-282">User</span></span></td>
    <td><span data-ttu-id="84157-283">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="84157-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84157-284">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="84157-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="84157-285">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="84157-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="84157-286">Wählen Sie die Benutzer aus, an die das Dokument eskaliert werden soll, und verschieben Sie diese Benutzer in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="84157-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="84157-287">Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Bearbeiten oder Beantworten von Dokumenten zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="84157-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="84157-288">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="84157-288">Select one of the following options:</span></span>

    - <span data-ttu-id="84157-289">**Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Beantworten hat.</span><span class="sxs-lookup"><span data-stu-id="84157-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="84157-290">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="84157-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84157-291">**Tage** – Geben Sie die Anzahl der Tage ein, die der Benutzer zum Beantworten hat.</span><span class="sxs-lookup"><span data-stu-id="84157-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="84157-292">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="84157-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84157-293">**Wochen** – Geben Sie die Anzahl der Wochen ein, die der Benutzer zum Beantworten hat.</span><span class="sxs-lookup"><span data-stu-id="84157-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="84157-294">**Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer antworten muss.</span><span class="sxs-lookup"><span data-stu-id="84157-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="84157-295">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats antworten soll.</span><span class="sxs-lookup"><span data-stu-id="84157-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="84157-296">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer antworten muss.</span><span class="sxs-lookup"><span data-stu-id="84157-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="84157-297">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember antworten soll.</span><span class="sxs-lookup"><span data-stu-id="84157-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="84157-298">Wiederholen Sie die Schritte 3 bis 4 für alle Benutzer, die dem Eskalationspfad hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="84157-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="84157-299">Sie können die Reihenfolge der Benutzer ändern.</span><span class="sxs-lookup"><span data-stu-id="84157-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="84157-300">Wenn die Benutzer im Eskalationspfad nicht innerhalb der vorgesehenen Zeit antworten, wird das Dokument automatisch bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="84157-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="84157-301">Um die vom System auszuführende Aktivität anzugeben, wählen Sie die Zeile **Aktivität** aus, klicken Sie dann auf die Registerkarte **Aktivität bei Beendigung** und wählen eine Aktivität aus.</span><span class="sxs-lookup"><span data-stu-id="84157-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
