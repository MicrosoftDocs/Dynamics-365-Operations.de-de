---
title: Genehmigungsprozesse in einem Workflow konfigurieren
description: Verwenden Sie das folgende Verfahren, um die Eigenschaften des Genehmigungsprozesses zu konfigurieren.
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
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09d09464eae932bf9caf4f2ea38cbbb3b4f0162
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190211"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="0cebf-103">Genehmigungsprozesse in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0cebf-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cebf-104">Verwenden Sie das folgende Verfahren, um die Eigenschaften des Genehmigungsprozesses zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0cebf-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="0cebf-105">Klicken Sie zum Konfigurieren eines Genehmigungsprozesses im Workflow-Editor mit der rechten Maustaste auf das Genehmigungselement, und klicken Sie dann auf **Eigenschaften**, um das Formular **Eigenschaftens** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="0cebf-106">Benennen des Genehmigungsprozesses</span><span class="sxs-lookup"><span data-stu-id="0cebf-106">Name the approval process</span></span>

<span data-ttu-id="0cebf-107">Gehen Sie folgendermaßen vor, um einen Namen für den Genehmigungsprozess einzugeben.</span><span class="sxs-lookup"><span data-stu-id="0cebf-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="0cebf-108">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0cebf-109">Geben Sie im Feld **Name** einen eindeutigen Namen für den Genehmigungsprozess ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="0cebf-110">Angeben, wann das Dokument automatisch bearbeitet wird</span><span class="sxs-lookup"><span data-stu-id="0cebf-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="0cebf-111">Sie können festlegen, dass eine automatische Aktivität für das Dokument ausgeführt wird, wenn bestimmte Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="0cebf-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="0cebf-112">So können z. B. Spesenabrechnungen mit einem Gesamtbetrag unter 100 Euro automatisch genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="0cebf-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="0cebf-113">Gehen Sie folgendermaßen vor, um anzugeben, wann das Dokument automatisch bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0cebf-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="0cebf-114">Klicken Sie im linken Bereich auf **Automatische Aktivitäten**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="0cebf-115">Aktivieren Sie dieses Kontrollkästchen **Automatische Aktivitäten aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="0cebf-116">Klicken Sie auf **Bedingung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="0cebf-117">Geben Sie eine Bedingung ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-117">Enter a condition.</span></span>
5. <span data-ttu-id="0cebf-118">Geben Sie ggf. zusätzliche Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="0cebf-119">Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="0cebf-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="0cebf-120">Klicken Sie auf **Test**, um das Formular **Workflow-Bedingungen testen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="0cebf-121">Wählen Sie im Bereich **Bedingung überprüfen** des Formulars einen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="0cebf-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="0cebf-122">Klicken Sie auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-122">Click **Test**.</span></span> <span data-ttu-id="0cebf-123">Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="0cebf-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="0cebf-124">Klicken Sie auf **OK** oder **Abbrechen**, um zum Formular **Eigenschaften** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="0cebf-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="0cebf-125">Wählen Sie in der Liste **Aktivität für Auto-Vervollständigen** die Aktivität aus, die für das Dokument ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cebf-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="0cebf-126">Angeben, wann Benachrichtigungen gesendet werden</span><span class="sxs-lookup"><span data-stu-id="0cebf-126">Specify when notifications are sent</span></span>

<span data-ttu-id="0cebf-127">Sie können Benachrichtigungen an Personen senden, wenn ein Dokument genehmigt, abgelehnt, delegiert oder eskaliert wurde oder eine Änderung für das Dokument angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="0cebf-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="0cebf-128">Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cebf-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="0cebf-129">Klicken Sie im linken Bereich auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="0cebf-130">Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="0cebf-131">**Delegieren** – Wenn ein Dokument einem anderen Benutzer zur Genehmigung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="0cebf-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="0cebf-132">**Eskalieren** – Wenn der zugewiesene Benutzer das Dokument nicht innerhalb der vorgesehenen Zeit bearbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="0cebf-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="0cebf-133">**Genehmigen** – Wenn ein Dokument genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="0cebf-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="0cebf-134">**Ablehnen** – Wenn ein Dokument abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="0cebf-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="0cebf-135">**Änderung anfordern** – Wenn der zugewiesene Benutzer eine Änderung eines übermittelten Dokuments angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="0cebf-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="0cebf-136">Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="0cebf-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="0cebf-137">Klicken Sie auf die Registerkarte **Benachrichtigungstext**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="0cebf-138">Geben Sie im Textfeld den Text für die Benachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="0cebf-139">Zum Anpassen des Texts können Sie Platzhalter einfügen, die bei der Anzeige für Benutzer durch die entsprechenden Daten ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0cebf-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="0cebf-140">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="0cebf-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="0cebf-141">Klicken Sie im Textfeld auf die Position, an der der Platzhalter erscheinen soll.</span><span class="sxs-lookup"><span data-stu-id="0cebf-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="0cebf-142">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="0cebf-143">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="0cebf-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="0cebf-144">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-144">Click **Insert**.</span></span>

7. <span data-ttu-id="0cebf-145">Klicken Sie auf **Übersetzungen**, um Übersetzungen der Benachrichtigung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="0cebf-146">Führen Sie im angezeigten Formular die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0cebf-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="0cebf-147">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-147">Click **Add**.</span></span>
    2. <span data-ttu-id="0cebf-148">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="0cebf-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="0cebf-149">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="0cebf-150">Fügen Sie zum Personalisieren des Texts Platzhalter ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="0cebf-151">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-151">Click **Close**.</span></span>

8. <span data-ttu-id="0cebf-152">Klicken Sie auf die Registerkarte **Empfänger**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="0cebf-153">Geben Sie an, an wen die Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cebf-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="0cebf-154">Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 10 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="0cebf-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="0cebf-155">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="0cebf-155">Option</span></span></th>
    <th><span data-ttu-id="0cebf-156">Empfänger der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0cebf-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="0cebf-157">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="0cebf-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="0cebf-158"><strong>Teilnehmer</strong></span><span class="sxs-lookup"><span data-stu-id="0cebf-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="0cebf-159">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="0cebf-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="0cebf-160">Nachdem Sie <strong>Teilnehmer</strong> ausgewählt haben, klicken Sie auf die Registerkarte <strong>Rollenbasiert</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cebf-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="0cebf-161">Wählen Sie in der Liste <strong>Teilnehmertyp</strong> den Typ der Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="0cebf-162">Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="0cebf-163"><strong>Workflowbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="0cebf-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="0cebf-164">Benutzer, die am aktuellen Workflow teilnehmen</span><span class="sxs-lookup"><span data-stu-id="0cebf-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="0cebf-165">Nachdem Sie <strong>Workflow-Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Workflow-Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cebf-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="0cebf-166">Wählen Sie in der Liste <strong>Workflow-Benutzer</strong> einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="0cebf-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="0cebf-167"><strong>Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="0cebf-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="0cebf-168">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="0cebf-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="0cebf-169">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cebf-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="0cebf-170">Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cebf-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="0cebf-171">Wiederholen Sie die Schritte 3 bis 9 für jedes in Schritt 2 ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0cebf-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="0cebf-172">Festlegen einer letzten genehmigenden Person</span><span class="sxs-lookup"><span data-stu-id="0cebf-172">Specify a final approver</span></span>

<span data-ttu-id="0cebf-173">Eine letzte genehmigende Person sollte für Szenarios festgelegt werden, in denen die genehmigende Person die Person ist, die das Dokument zur Genehmigung übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="0cebf-173">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="0cebf-174">Gehen Sie zum Festlegen einer letzten genehmigenden Person folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="0cebf-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="0cebf-175">Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-175">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="0cebf-176">Aktivieren Sie das Kontrollkästchen **Letzter Genehmiger verwenden**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-176">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="0cebf-177">Wählen Sie in der Liste den Benutzer aus, der als letzte genehmigende Person fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="0cebf-177">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="0cebf-178">Festlegen einer Zeitgrenze</span><span class="sxs-lookup"><span data-stu-id="0cebf-178">Set a time limit</span></span>

<span data-ttu-id="0cebf-179">Gehen Sie folgendermaßen vor, wenn der Genehmigungsprozess in einer bestimmten Zeit abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-179">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="0cebf-180">Die in diesen Schritten ausgewählten Optionen setzen die Optionen außer Kraft, die Sie in den Bereichen **Zuweisung** und **Eskalation** jedes Genehmigungsschritts ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="0cebf-180">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="0cebf-181">Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-181">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="0cebf-182">Wählen Sie das Kontrollkästchen **Zeitgrenze für das Workflow** **element** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0cebf-182">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="0cebf-183">Legen Sie im Feld **Dauer** fest, wann der Genehmigungsprozess abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-183">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="0cebf-184">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="0cebf-184">Select one of the following options:</span></span>

    - <span data-ttu-id="0cebf-185">**Stunden** – Geben Sie die Anzahl der Stunden ein, in denen der Genehmigungsprozess abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-185">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="0cebf-186">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="0cebf-187">**Tage** – Geben Sie die Anzahl von Tagen ein, in denen der Genehmigungsprozess abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-187">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="0cebf-188">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="0cebf-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="0cebf-189">**Wochen** – Geben Sie die Anzahl von Wochen ein, in denen der Genehmigungsprozess abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-189">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="0cebf-190">**Monate** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Genehmigungsprozess abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-190">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="0cebf-191">Sie können z. B. angeben, dass der Genehmigungsprozess bis Freitag der dritten Woche des Monats abgeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="0cebf-191">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="0cebf-192">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Genehmigungsprozess abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cebf-192">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="0cebf-193">Sie können z. B. angeben, dass der Genehmigungsprozess bis Freitag der dritten Woche im Dezember abgeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="0cebf-193">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="0cebf-194">Wenn die Zeitgrenze überschritten wird, wird das Dokument automatisch bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="0cebf-194">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="0cebf-195">Wählen Sie in der Liste **Aktivität** die Aktivität aus, die vom System ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cebf-195">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="0cebf-196">Angeben der verfügbaren Aktivitäten für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="0cebf-196">Specify which actions are available to the user</span></span>

<span data-ttu-id="0cebf-197">Wenn ein Dokument einem Benutzer zur Genehmigung zugewiesen wird, muss der Benutzer das Dokument durch entsprechende Aktivitäten bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0cebf-197">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="0cebf-198">Gehen Sie folgendermaßen vor, um anzugeben, welche Aktivitäten der Benutzer für das übermittelte Dokument ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="0cebf-198">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="0cebf-199">Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="0cebf-199">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="0cebf-200">Aktivieren Sie das Kontrollkästchen **Genehmigen**, wenn der Benutzer das Dokument genehmigen kann.</span><span class="sxs-lookup"><span data-stu-id="0cebf-200">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="0cebf-201">Aktivieren Sie das Kontrollkästchen **Ablehnen**, wenn der Benutzer das Dokument ablehnen kann.</span><span class="sxs-lookup"><span data-stu-id="0cebf-201">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="0cebf-202">Aktivieren Sie das Kontrollkästchen **Änderung anfordern**, wenn der Benutzer Änderungen des Dokuments anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="0cebf-202">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="0cebf-203">Aktivieren Sie das Kontrollkästchen **Delegieren**, wenn der Benutzer das Dokument einem anderen Benutzer zur Genehmigung zuweisen kann.</span><span class="sxs-lookup"><span data-stu-id="0cebf-203">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="0cebf-204">Das Kontrollkästchen Aktionen von der Arbeitsliste in **Enterprise Portal** aktivieren ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0cebf-204">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="0cebf-205">Konfigurieren der Genehmigungsschritte</span><span class="sxs-lookup"><span data-stu-id="0cebf-205">Configure the approval steps</span></span>

<span data-ttu-id="0cebf-206">Ein Genehmigungsprozess besteht aus Genehmigungsschritten.</span><span class="sxs-lookup"><span data-stu-id="0cebf-206">An approval process consists of approval steps.</span></span> <span data-ttu-id="0cebf-207">Führen Sie die folgende Prozedur aus, um dem Genehmigungsprozess Schritte hinzuzufügen und die Schritte zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0cebf-207">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="0cebf-208">Doppelklicken Sie im Workflow-Editor auf den Genehmigungsprozess.</span><span class="sxs-lookup"><span data-stu-id="0cebf-208">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="0cebf-209">Im Workflow-Editor werden die Schritte des Genehmigungsprozesses angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0cebf-209">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="0cebf-210">Ziehen Sie zum Hinzufügen eines Genehmigungsschritts den Schritt aus dem Bereich **Workflow-Elemente** auf die Canvas.</span><span class="sxs-lookup"><span data-stu-id="0cebf-210">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="0cebf-211">Informationen zum Konfigurieren eines Genehmigungsschritts finden, finden Sie unter [Konfigurieren eines Genehmigungsschritts](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="0cebf-211">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
