---
title: Manuelle Aufgaben in einem Workflow konfigurieren
description: Dieses Thema erläutert, wie Sie die Eigenschaften einer manuellen Aufgabe konfigurieren können.
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
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492c49b1a3e8334bca401770c4c2db04e8892691
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124634"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="21142-103">Manuelle Aufgaben in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="21142-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21142-104">Dieses Thema erläutert, wie Sie die Eigenschaften einer manuellen Aufgabe konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="21142-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="21142-105">Klicken Sie zum Konfigurieren einer manuellen Aufgabe im Workflow-Editor mit der rechten Maustaste auf die Aufgabe, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="21142-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="21142-106">Verwenden Sie dann die folgenden Verfahren, um die Eigenschaften der manuellen Aufgabe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="21142-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="21142-107">Benennen der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="21142-107">Name the task</span></span>

<span data-ttu-id="21142-108">Gehen Sie folgendermaßen vor, um einen Namen für die manuelle Aufgabe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="21142-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="21142-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="21142-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die Aufgabe ein.</span><span class="sxs-lookup"><span data-stu-id="21142-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="21142-111">Eingeben einer Betreffzeile und von Anweisungen</span><span class="sxs-lookup"><span data-stu-id="21142-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="21142-112">Sie müssen eine Betreffzeile und Anweisungen für Benutzer eingeben, die der Aufgabe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="21142-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="21142-113">Wenn Sie z. B. eine Aufgabe für Bestellanforderungen konfigurieren, werden dem Benutzer, der dem Schritt zugewiesen ist, die Betreffzeile und Anweisungen auf der Seite **Bestellanforderungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21142-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="21142-114">Die Betreffzeile wird in einer Statusleiste auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21142-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="21142-115">Der Benutzer kann nun auf das Symbol in der Statusleiste klicken, um die Anweisungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="21142-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="21142-116">Gehen Sie folgendermaßen vor, um eine Betreffzeile und Anweisungen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="21142-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="21142-117">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="21142-118">Geben Sie im Feld **Betreff für die Arbeitsaufgabe** die Betreffzeile ein.</span><span class="sxs-lookup"><span data-stu-id="21142-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="21142-119">Zum Personalisieren der Betreffzeile können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="21142-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="21142-120">Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Betreffzeile Benutzern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="21142-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="21142-121">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="21142-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="21142-122">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="21142-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="21142-123">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="21142-124">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="21142-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="21142-125">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-125">Click **Insert**.</span></span>

4. <span data-ttu-id="21142-126">Führen Sie die folgenden Schritte aus, um Übersetzungen der Betreffzeile hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="21142-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="21142-127">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="21142-128">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="21142-129">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="21142-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="21142-130">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="21142-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="21142-131">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 3 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="21142-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="21142-132">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="21142-132">Click **Close**.</span></span>

5. <span data-ttu-id="21142-133">Geben Sie im Feld **Arbeitsaufgabenanweisungen** die Arbeitsanweisungen ein.</span><span class="sxs-lookup"><span data-stu-id="21142-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="21142-134">Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="21142-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="21142-135">Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt.</span><span class="sxs-lookup"><span data-stu-id="21142-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="21142-136">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="21142-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="21142-137">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="21142-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="21142-138">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="21142-139">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="21142-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="21142-140">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-140">Click **Insert**.</span></span>

7. <span data-ttu-id="21142-141">Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="21142-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="21142-142">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="21142-143">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="21142-144">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="21142-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="21142-145">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="21142-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="21142-146">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 6 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="21142-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="21142-147">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="21142-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="21142-148">Zuweisen der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="21142-148">Assign the task</span></span>

<span data-ttu-id="21142-149">Gehen Sie folgendermaßen vor, um anzugeben, wem die manuelle Aufgabe zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="21142-150">Klicken Sie im linken Bereich auf **Zuweisung**.</span><span class="sxs-lookup"><span data-stu-id="21142-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="21142-151">Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 3 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="21142-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="21142-152">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="21142-152">Option</span></span></th>
    <th><span data-ttu-id="21142-153">Benutzer, denen die Aufgabe zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="21142-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="21142-154">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="21142-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="21142-155">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="21142-155">Participant</span></span></td>
    <td><span data-ttu-id="21142-156">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="21142-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-157">Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Aufgabe zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="21142-158">Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, der die Aufgabe zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-159">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="21142-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="21142-160">Benutzer in einer bestimmten Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="21142-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-161">Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem die Aufgabe zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="21142-162">Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="21142-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="21142-163">Diese Namen stellen Benutzer dar, denen die Aufgabe zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="21142-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="21142-164">Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="21142-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="21142-165">Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="21142-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="21142-166">Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="21142-167">Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="21142-168">Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich die Aufgabe zugewiesen werden soll:</span><span class="sxs-lookup"><span data-stu-id="21142-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="21142-169"><strong>Allen abgerufenen Benutzern zuordnen</strong> – Die Aufgabe wird allen Benutzern im Bereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="21142-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="21142-170"><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Die Aufgabe wird nur dem letzten Benutzer im Bereich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21142-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="21142-171"><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Die Aufgabe wird keinem Benutzer im Bereich zugewiesen, der eine bestimmte Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="21142-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="21142-172">Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="21142-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-173">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="21142-173">Workflow user</span></span></td>
    <td><span data-ttu-id="21142-174">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="21142-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="21142-175">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="21142-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-176">Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-176">User</span></span></td>
    <td><span data-ttu-id="21142-177">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-178">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="21142-179">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="21142-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="21142-180">Wählen Sie die Benutzer aus, um die Aufgabe zuzuweisen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-181">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="21142-181">Queue</span></span></td>
    <td><span data-ttu-id="21142-182">Eine Warteschlange für Arbeitsaufgaben</span><span class="sxs-lookup"><span data-stu-id="21142-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-183">Nachdem Sie <strong>Warteschlange</strong> ausgewählt haben, klicken Sie auf die Registerkarte <strong>Warteschlangenbasiert</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="21142-184">Gehen Sie folgendermaßen vor, um die Aufgabe einer bestimmten Warteschlange zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="21142-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="21142-185">In der Liste <strong>Warteschlangentyp</strong> wählen Sie <strong>Warteschlangen für Arbeitsaufgaben</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="21142-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="21142-186">Wählen Sie in der Liste <strong>Warteschlangenname</strong> die Warteschlange aus.</span><span class="sxs-lookup"><span data-stu-id="21142-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="21142-187">Wenn mit einer bestimmten Bedingung festgelegt werden soll, welcher Warteschlange die Aufgabe zugewiesen wird, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="21142-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="21142-188">In der Liste <strong>Warteschlangentyp</strong> wählen Sie <strong>Bedingte Warteschlangen für Arbeitsaufgaben</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="21142-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="21142-189">Wählen Sie in der Liste <strong>Warteschlangenname</strong> <strong>Bedingte Warteschlange</strong>aus.</span><span class="sxs-lookup"><span data-stu-id="21142-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="21142-190">Diese Option wird nur für einige Workflows verwendet, wie z.B. Anfrageverwaltung.</span><span class="sxs-lookup"><span data-stu-id="21142-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="21142-191">Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Ausführen der Aufgabe zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="21142-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="21142-192">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="21142-192">Select one of the following options:</span></span>

    - <span data-ttu-id="21142-193">**Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Ausführen der Aufgabe hat.</span><span class="sxs-lookup"><span data-stu-id="21142-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="21142-194">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="21142-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="21142-195">**Tage** – Geben Sie die Anzahl von Tagen ein, die der Benutzer zum Ausführen der Aufgabe hat.</span><span class="sxs-lookup"><span data-stu-id="21142-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="21142-196">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="21142-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="21142-197">**Wochen** – Geben Sie die Anzahl von Wochen ein, die der Benutzer zum Ausführen der Aufgabe hat.</span><span class="sxs-lookup"><span data-stu-id="21142-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="21142-198">**Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer die Aufgabe ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="21142-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="21142-199">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats die Aufgabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="21142-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="21142-200">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer die Aufgabe ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="21142-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="21142-201">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember die Aufgabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="21142-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="21142-202">Wenn der Benutzer die Aufgabe nicht innerhalb der vorgesehenen Zeit ausführt, ist die Aufgabe überfällig.</span><span class="sxs-lookup"><span data-stu-id="21142-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="21142-203">Eine überfällige Aufgabe kann basierend auf den im Bereich **Eskalation** der Seite ausgewählten Optionen eskaliert werden.</span><span class="sxs-lookup"><span data-stu-id="21142-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="21142-204">Festlegen der Vorgehensweise für überfällige Aufgaben</span><span class="sxs-lookup"><span data-stu-id="21142-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="21142-205">Wenn ein Benutzer die manuelle Aufgabe nicht innerhalb der vorgesehenen Zeit ausführt, ist die Aufgabe überfällig.</span><span class="sxs-lookup"><span data-stu-id="21142-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="21142-206">Eine überfällige Aufgabe kann eskaliert oder automatisch einem anderen Benutzer zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="21142-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="21142-207">Führen Sie die folgenden Schritte aus, um die Aufgabe zu eskalieren, wenn sie überfällig ist.</span><span class="sxs-lookup"><span data-stu-id="21142-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="21142-208">Klicken Sie im linken Bereich auf **Eskalation**.</span><span class="sxs-lookup"><span data-stu-id="21142-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="21142-209">Aktivieren Sie das Kontrollkästchen **Eskalationspfad verwenden**, um einen Eskalationspfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="21142-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="21142-210">Die Aufgabe wird automatisch den im Eskalationspfad aufgeführten Benutzern zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21142-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="21142-211">Die folgende Tabelle stellt z. B. einen Eskalationspfad dar.</span><span class="sxs-lookup"><span data-stu-id="21142-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="21142-212">Sequenz</span><span class="sxs-lookup"><span data-stu-id="21142-212">Sequence</span></span> | <span data-ttu-id="21142-213">Eskalationspfad</span><span class="sxs-lookup"><span data-stu-id="21142-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="21142-214">1</span><span class="sxs-lookup"><span data-stu-id="21142-214">1</span></span>        | <span data-ttu-id="21142-215">Zuweisen zu: Doris</span><span class="sxs-lookup"><span data-stu-id="21142-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="21142-216">2</span><span class="sxs-lookup"><span data-stu-id="21142-216">2</span></span>        | <span data-ttu-id="21142-217">Zuweisen zu: Elke</span><span class="sxs-lookup"><span data-stu-id="21142-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="21142-218">3</span><span class="sxs-lookup"><span data-stu-id="21142-218">3</span></span>        | <span data-ttu-id="21142-219">Abschließende Aktivität: Ablehnen</span><span class="sxs-lookup"><span data-stu-id="21142-219">Final action: Reject</span></span> |

    <span data-ttu-id="21142-220">In diesem Beispiel wird die überfällige Aufgabe Doris zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21142-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="21142-221">Führt Doris die Aufgabe nicht innerhalb der vorgesehenen Zeit aus, wird die Aufgabe Elke zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21142-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="21142-222">Führt Elke die Aufgabe nicht innerhalb der vorgesehenen Zeit aus, wird das zur Verarbeitung übermittelte Dokument abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="21142-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="21142-223">Klicken Sie auf **Eskalation hinzufügen**, um dem Eskalationspfad einen Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="21142-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="21142-224">Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 4 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="21142-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="21142-225">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="21142-225">Option</span></span></th>
    <th><span data-ttu-id="21142-226">Benutzer, denen die Aufgabe eskaliert wird</span><span class="sxs-lookup"><span data-stu-id="21142-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="21142-227">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="21142-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="21142-228">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="21142-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="21142-229">Benutzer in einer bestimmten Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="21142-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-230">Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem die Aufgabe eskaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="21142-231">Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="21142-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="21142-232">Diese Namen stellen Benutzer dar, denen die Aufgabe eskaliert wird.</span><span class="sxs-lookup"><span data-stu-id="21142-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="21142-233">Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="21142-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="21142-234">Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="21142-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="21142-235">Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="21142-236">Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="21142-237">Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich die Aufgabe eskaliert werden soll:</span><span class="sxs-lookup"><span data-stu-id="21142-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="21142-238"><strong>Allen abgerufenen Benutzern zuordnen</strong> – Die Aufgabe wird allen Benutzern im Bereich eskaliert.</span><span class="sxs-lookup"><span data-stu-id="21142-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="21142-239"><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Die Aufgabe wird nur dem letzten Benutzer im Bereich eskaliert.</span><span class="sxs-lookup"><span data-stu-id="21142-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="21142-240"><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Diese Aufgabe wird keinem Benutzer im Bereich eskaliert, der eine bestimmte Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="21142-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="21142-241">Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="21142-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-242">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="21142-242">Workflow user</span></span></td>
    <td><span data-ttu-id="21142-243">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="21142-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="21142-244">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="21142-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-245">Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-245">User</span></span></td>
    <td><span data-ttu-id="21142-246">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-247">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="21142-248">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="21142-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="21142-249">Wählen Sie die Benutzer aus, um die Aufgabe zu eskalieren, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="21142-250">Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Ausführen der Aufgabe zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="21142-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="21142-251">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="21142-251">Select one of the following options:</span></span>

    - <span data-ttu-id="21142-252">**Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Ausführen der Aufgabe hat.</span><span class="sxs-lookup"><span data-stu-id="21142-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="21142-253">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="21142-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="21142-254">**Tage** – Geben Sie die Anzahl von Tagen ein, die der Benutzer zum Ausführen der Aufgabe hat.</span><span class="sxs-lookup"><span data-stu-id="21142-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="21142-255">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="21142-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="21142-256">**Wochen** – Geben Sie die Anzahl von Wochen ein, die der Benutzer zum Ausführen der Aufgabe hat.</span><span class="sxs-lookup"><span data-stu-id="21142-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="21142-257">**Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer die Aufgabe ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="21142-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="21142-258">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats die Aufgabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="21142-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="21142-259">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer die Aufgabe ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="21142-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="21142-260">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember die Aufgabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="21142-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="21142-261">Wiederholen Sie die Schritte 3 bis 4 für alle Benutzer, die dem Eskalationspfad hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="21142-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="21142-262">Sie können die Reihenfolge der Benutzer ändern.</span><span class="sxs-lookup"><span data-stu-id="21142-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="21142-263">Wenn die Benutzer im Eskalationspfad die Aufgabe nicht innerhalb der vorgesehenen Zeit ausführen, wird die Aufgabe automatisch bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="21142-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="21142-264">Um die vom System auszuführende Aktivität anzugeben, wählen Sie die Zeile **Aktivität** aus, klicken Sie dann auf die Registerkarte **Aktivität bei Beendigung** und wählen eine Aktivität aus.</span><span class="sxs-lookup"><span data-stu-id="21142-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="21142-265">Angeben, wann die Aufgabe automatisch bearbeitet wird</span><span class="sxs-lookup"><span data-stu-id="21142-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="21142-266">Sie können festlegen, dass unter bestimmten Bedingungen die manuelle Aufgabe automatisch bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="21142-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="21142-267">Angenommen, eine Aufgabe erfordert, dass ein Mitglied der für Spesenabrechnungen zuständigen Abteilung die zusammen mit einer Spesenabrechnung eingereichten Belege prüft.</span><span class="sxs-lookup"><span data-stu-id="21142-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="21142-268">Entsprechend den Unternehmensrichtlinien muss diese Aufgabe ausgeführt werden, wenn der Gesamtbetrag der Spesenabrechnung 100 Euro überschreitet.</span><span class="sxs-lookup"><span data-stu-id="21142-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="21142-269">In diesem Szenario können Sie das System zur automatischen Markierung der Aufgabe als **Abschließen** konfigurieren, wenn Gesamtbetrag < 100.</span><span class="sxs-lookup"><span data-stu-id="21142-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="21142-270">Gehen Sie folgendermaßen vor, um anzugeben, wann die manuelle Aufgabe automatisch bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="21142-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="21142-271">Klicken Sie im linken Bereich auf **Automatische Aktivitäten**.</span><span class="sxs-lookup"><span data-stu-id="21142-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="21142-272">Aktivieren Sie dieses Kontrollkästchen **Automatische Aktivitäten aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="21142-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="21142-273">Klicken Sie auf **Bedingung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="21142-274">Geben Sie eine Bedingung ein.</span><span class="sxs-lookup"><span data-stu-id="21142-274">Enter a condition.</span></span>
5. <span data-ttu-id="21142-275">Geben Sie alle notwendigen zusätzlichen Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="21142-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="21142-276">Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="21142-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="21142-277">Klicken Sie auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="21142-277">Click **Test**.</span></span>
    2. <span data-ttu-id="21142-278">Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="21142-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="21142-279">Klicken Sie auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="21142-279">Click **Test**.</span></span> <span data-ttu-id="21142-280">Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="21142-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="21142-281">Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="21142-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="21142-282">Wählen Sie in der Liste **Aktivität für AutoVervollständigen** die Aktivität aus, die für die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="21142-283">Angeben, wann Benachrichtigungen gesendet werden</span><span class="sxs-lookup"><span data-stu-id="21142-283">Specify when notifications are sent</span></span>

<span data-ttu-id="21142-284">Sie können Benachrichtigungen an Personen senden, wenn eine manuelle Aufgabe delegiert, eskaliert, abgeschlossen oder abgelehnt wurde oder eine Änderung für die Aufgabe angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="21142-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="21142-285">Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="21142-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="21142-286">Klicken Sie im linken Bereich auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="21142-287">Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen:</span><span class="sxs-lookup"><span data-stu-id="21142-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="21142-288">**Delegieren** – Die Aufgabe wurde einem anderen Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21142-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="21142-289">**Eskalieren** – Der zugewiesene Benutzer hat die Aufgabe nicht innerhalb der vorgesehenen Zeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21142-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="21142-290">**Abschließen** – Der zugewiesene Benutzer hat die Aufgabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21142-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="21142-291">**Ablehnen** – Der zugewiesene Benutzer hat das übermittelte Dokument abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="21142-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="21142-292">**Änderung anfordern** – Der zugewiesene Benutzer eine Änderung des übermittelten Dokuments angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="21142-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="21142-293">Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="21142-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="21142-294">Geben Sie im Textfeld auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="21142-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="21142-295">Zum Personalisieren der Benachrichtigung können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="21142-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="21142-296">Platzhalter werden durch die entsprechenden Informationen ersetzt, wenn die Benachrichtigung Benutzern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="21142-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="21142-297">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="21142-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="21142-298">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="21142-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="21142-299">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="21142-300">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="21142-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="21142-301">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-301">Click **Insert**.</span></span>

6. <span data-ttu-id="21142-302">Führen Sie die folgenden Schritte aus, um Übersetzungen von Benachrichtigungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="21142-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="21142-303">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="21142-304">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="21142-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="21142-305">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="21142-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="21142-306">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="21142-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="21142-307">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 5 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="21142-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="21142-308">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="21142-308">Click **Close**.</span></span>

7. <span data-ttu-id="21142-309">Auf der Registerkarte **Empfänger** geben Sie an, an wen die Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="21142-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="21142-310">Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für diese Option aus, bevor Sie mit Schritt 8 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="21142-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="21142-311">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="21142-311">Option</span></span></th>
    <th><span data-ttu-id="21142-312">Empfänger der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="21142-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="21142-313">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="21142-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="21142-314">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="21142-314">Participant</span></span></td>
    <td><span data-ttu-id="21142-315">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="21142-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-316">Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Benachrichtigung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="21142-317">Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="21142-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-318">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="21142-318">Workflow user</span></span></td>
    <td><span data-ttu-id="21142-319">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="21142-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="21142-320">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="21142-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="21142-321">Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-321">User</span></span></td>
    <td><span data-ttu-id="21142-322">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="21142-323">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="21142-324">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="21142-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="21142-325">Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="21142-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="21142-326">Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="21142-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="21142-327">Festlegen einer Zeitgrenze</span><span class="sxs-lookup"><span data-stu-id="21142-327">Set a time limit</span></span>

<span data-ttu-id="21142-328">Gehen Sie folgendermaßen vor, wenn die manuelle Aufgabe in einer bestimmten Zeit abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="21142-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="21142-329">Die hier ausgewählten Optionen setzen die Optionen außer Kraft, die Sie in den Bereichen **Zuweisung**und **Eskalation** der Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="21142-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="21142-330">Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="21142-331">Aktivieren Sie das Kontrollkästchen **Zeitgrenze für das Workflowelement festlegen**.</span><span class="sxs-lookup"><span data-stu-id="21142-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="21142-332">Legen Sie im Feld **Dauer** fest, wann die Aufgabe abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="21142-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="21142-333">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="21142-333">Select one of the following options:</span></span>

    - <span data-ttu-id="21142-334">**Stunden** – Geben Sie die Anzahl der Stunden ein, in denen die Aufgabe ausgeführt sein muss.</span><span class="sxs-lookup"><span data-stu-id="21142-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="21142-335">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="21142-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="21142-336">**Tage** – Geben Sie die Anzahl von Tagen ein, in denen die Aufgabe ausgeführt sein muss.</span><span class="sxs-lookup"><span data-stu-id="21142-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="21142-337">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="21142-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="21142-338">**Wochen** – Geben Sie die Anzahl von Wochen ein, in denen die Aufgabe ausgeführt sein muss.</span><span class="sxs-lookup"><span data-stu-id="21142-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="21142-339">**Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem die Aufgabe ausgeführt sein muss.</span><span class="sxs-lookup"><span data-stu-id="21142-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="21142-340">Sie können z. B. angeben, dass die Aufgabe bis Freitag der dritten Woche des Monats abgeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="21142-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="21142-341">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem die Aufgabe ausgeführt sein muss.</span><span class="sxs-lookup"><span data-stu-id="21142-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="21142-342">Sie können z. B. angeben, dass die Aufgabe bis Freitag der dritten Woche im Dezember ausgeführt sein soll.</span><span class="sxs-lookup"><span data-stu-id="21142-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="21142-343">Wenn die Zeitgrenze überschritten wird, wird die Aufgabe bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="21142-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="21142-344">Wählen Sie in der Liste **Aktivität** die Aktivität aus, die vom System ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21142-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="21142-345">Angeben der verfügbaren Aktivitäten für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="21142-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="21142-346">Wenn die manuelle Aufgabe einem Benutzer zugewiesen wird, muss der Benutzer die Aufgabe bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="21142-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="21142-347">Gehen Sie folgendermaßen vor, um anzugeben, welche Aktivitäten der Benutzer für die Aufgabe ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="21142-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="21142-348">Die verfügbaren Aktivitäten unterscheiden sich abhängig davon, wie die Aufgabe entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="21142-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="21142-349">Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="21142-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="21142-350">Aktivieren Sie das Kontrollkästchen **Abgeschlossen**, wenn der Benutzer in der Lage sein soll, die Aufgabe als **Abgeschlossen** zu markieren.</span><span class="sxs-lookup"><span data-stu-id="21142-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="21142-351">Aktivieren Sie das Kontrollkästchen **Ablehnen**, wenn der Benutzer in der Lage sein soll, das übermittelte Dokument abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="21142-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="21142-352">Aktivieren Sie das Kontrollkästchen **Änderung anfordern**, wenn der Benutzer in der Lage sein soll, Änderungen des übermittelten Dokuments anzufordern.</span><span class="sxs-lookup"><span data-stu-id="21142-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="21142-353">Aktivieren Sie das Kontrollkästchen **Delegieren**, wenn der Benutzer in der Lage sein soll, die Aufgabe einem anderen Benutzer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="21142-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="21142-354">Aktivieren Sie das Kontrollkästchen **Neu zuordnen**, wenn der Benutzer in der Lage sein soll, die Aufgabe einem anderen Benutzer in der Warteschlange für Arbeitsaufgaben neu zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="21142-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="21142-355">Aktivieren Sie das Kontrollkästchen **Freigeben**, wenn der Benutzer in der Lage sein soll, die Aufgabe der Warteschlange für Arbeitsaufgaben neu zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="21142-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="21142-356">Ein anderer Benutzer kann die Aufgabe anschließend ausführen.</span><span class="sxs-lookup"><span data-stu-id="21142-356">Another user can then complete the task.</span></span>
