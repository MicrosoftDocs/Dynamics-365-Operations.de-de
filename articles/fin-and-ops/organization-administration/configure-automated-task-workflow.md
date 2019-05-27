---
title: Konfigurieren von automatisierten Aufgaben in einem Workflow
description: Dieses Thema erläutert, wie Sie die Eigenschaften einer automatisierten Aufgabe konfigurieren können.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a9f37228beedafa085987668d5c89b06c6c9d61
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557404"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="a443b-103">Konfigurieren von automatisierten Aufgaben in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="a443b-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a443b-104">Dieses Thema erläutert, wie Sie die Eigenschaften einer automatisierten Aufgabe konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="a443b-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="a443b-105">Klicken Sie zum Konfigurieren einer automatisierten Aufgabe im Workflow-Editor mit der rechten Maustaste auf die Aufgabe, und klicken Sie dann auf **Eigenschaften**, umdie Seite **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a443b-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a443b-106">Verwenden Sie dann die folgenden Verfahren, um die Eigenschaften der automatisierten Aufgabe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a443b-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="a443b-107">Benennen der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a443b-107">Name the task</span></span>

<span data-ttu-id="a443b-108">Gehen Sie folgendermaßen vor, um einen Namen für die automatisierte Aufgabe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a443b-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="a443b-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a443b-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die Aufgabe ein.</span><span class="sxs-lookup"><span data-stu-id="a443b-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a443b-111">Angeben, wann Benachrichtigungen gesendet werden</span><span class="sxs-lookup"><span data-stu-id="a443b-111">Specify when notifications are sent</span></span>

<span data-ttu-id="a443b-112">Sie können Benachrichtigungen an Personen senden, wenn eine automatisierte Aufgabe ausgeführt oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="a443b-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="a443b-113">Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a443b-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="a443b-114">Klicken Sie im linken Bereich auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="a443b-115">Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a443b-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="a443b-116">**Ausführung** – Benachrichtigungen werden gesendet, wenn die Aufgabe ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a443b-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="a443b-117">**Abgebrochen** – Benachrichtigungen werden gesendet, wenn die Aufgabe abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="a443b-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="a443b-118">Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="a443b-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="a443b-119">Geben Sie im Textfeld auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="a443b-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="a443b-120">Zum Personalisieren der Benachrichtigung können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="a443b-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="a443b-121">Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Benachrichtigung Benutzern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a443b-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="a443b-122">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="a443b-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a443b-123">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="a443b-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a443b-124">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a443b-125">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="a443b-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a443b-126">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-126">Click **Insert**.</span></span>

6. <span data-ttu-id="a443b-127">Führen Sie die folgenden Schritte aus, um Übersetzungen von Benachrichtigungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="a443b-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="a443b-128">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="a443b-129">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a443b-130">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="a443b-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a443b-131">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="a443b-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a443b-132">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 5 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a443b-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="a443b-133">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a443b-133">Click **Close**.</span></span>

7. <span data-ttu-id="a443b-134">Auf der Registerkarte **Empfänger** geben Sie an, an wen die Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a443b-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="a443b-135">Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für diese Option aus, bevor Sie mit Schritt 8 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a443b-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a443b-136">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="a443b-136">Option</span></span></th>
    <th><span data-ttu-id="a443b-137">Empfänger der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a443b-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="a443b-138">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="a443b-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a443b-139">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="a443b-139">Participant</span></span></td>
    <td><span data-ttu-id="a443b-140">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="a443b-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a443b-141">Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Benachrichtigung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a443b-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a443b-142">Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a443b-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a443b-143">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="a443b-143">Workflow user</span></span></td>
    <td><span data-ttu-id="a443b-144">Benutzer, die am aktuellen Workflow teilnehmen</span><span class="sxs-lookup"><span data-stu-id="a443b-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a443b-145">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="a443b-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a443b-146">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a443b-146">User</span></span></td>
    <td><span data-ttu-id="a443b-147">Bestimmte Microsoft Dynamics 365 for Finance and Operations-Benutzer</span><span class="sxs-lookup"><span data-stu-id="a443b-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a443b-148">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a443b-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a443b-149">Die Liste <strong>Verfügbare Benutzer</strong> enthält die Liste aller Benutzer von Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a443b-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="a443b-150">Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a443b-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="a443b-151">Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a443b-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>
