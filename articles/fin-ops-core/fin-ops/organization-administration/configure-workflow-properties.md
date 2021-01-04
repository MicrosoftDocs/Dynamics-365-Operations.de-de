---
title: Konfigurieren von Workfloweigenschaften
description: Dieses Thema erläutert, wie Sie die verschiedenen Eigenschaften eines Workflows konfigurieren können.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693281"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="8cde5-103">Konfigurieren von Workfloweigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cde5-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cde5-104">Dieses Thema erläutert, wie Sie die verschiedenen Eigenschaften eines Workflows konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="8cde5-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="8cde5-105">Öffnen Sie zum Konfigurieren der Eigenschaften eines Workflows den Workflow im Workflow-Editor.</span><span class="sxs-lookup"><span data-stu-id="8cde5-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="8cde5-106">Klicken Sie auf die Canvas des Workflow-Editors und dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8cde5-107">Verwenden Sie dann die folgenden Prozeduren, um die verschiedenen Eigenschaften des Workflows zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8cde5-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="8cde5-108">Benennen des Workflows</span><span class="sxs-lookup"><span data-stu-id="8cde5-108">Name the workflow</span></span>

<span data-ttu-id="8cde5-109">Gehen Sie folgendermaßen vor, um einen Namen für den Workflow einzugeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="8cde5-110">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8cde5-111">Geben Sie im Feld **Name** einen eindeutigen Namen für den Workflow ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="8cde5-112">Wenn Sie für jedes Land bzw. jede Region, in dem/der Sie tätig sind, Workflows für Bestellanforderungen erstellen, kann der jeweilige Workflow beispielsweise **Bestellanforderungen Dänemark** oder **Bestellanforderungen Spanien** benannt werden.</span><span class="sxs-lookup"><span data-stu-id="8cde5-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="8cde5-113">Angeben des Workfloweigentümers</span><span class="sxs-lookup"><span data-stu-id="8cde5-113">Specify the workflow owner</span></span>

<span data-ttu-id="8cde5-114">Der Workfloweigentümer ist die Person, die den Workflow verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="8cde5-115">Gehen Sie folgendermaßen vor, um den Workfloweigentümer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="8cde5-116">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8cde5-117">Wählen Sie in der Liste **Eigentümer** den Namen der Person aus, die diesen Workflow verwalten soll.</span><span class="sxs-lookup"><span data-stu-id="8cde5-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="8cde5-118">Auswählen einer E-Mail-Vorlage</span><span class="sxs-lookup"><span data-stu-id="8cde5-118">Select an email template</span></span>

<span data-ttu-id="8cde5-119">Gehen Sie folgendermaßen vor, um die E-Mail-Vorlage auszuwählen, die zum Generieren von Benachrichtigungsmeldungen zu diesem Workflow verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cde5-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="8cde5-120">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8cde5-121">Wählen Sie in der Liste **E-Mail-Vorlagen für Workflowbenachrichtigungen** die Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="8cde5-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="8cde5-122">Eingeben von Anweisungen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="8cde5-122">Enter instructions for users</span></span>

<span data-ttu-id="8cde5-123">Sie können Benutzern, die Dokumente zur Verarbeitung und Genehmigung übermitteln, Anweisungen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="8cde5-124">Diese Benutzer werden auch als *Ersteller* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="8cde5-125">Sie erstellen beispielsweise einen Workflow für eine Bestellanforderung und geben Anweisungen ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="8cde5-126">Diese Anweisungen können von Benutzern angezeigt werden, die Bestellanforderungen auf der Seite **Bestellanforderungen** eingeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="8cde5-127">Der Ersteller klickt auf das Symbol in der Workflowstatusleiste, um Anweisungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="8cde5-128">Gehen Sie folgendermaßen vor, um Anweisungen für Benutzer einzugeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="8cde5-129">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8cde5-130">Geben Sie im Feld **Übermittlungsanweisungen** die Arbeitsanweisungen ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="8cde5-131">Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="8cde5-132">Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8cde5-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="8cde5-133">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="8cde5-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="8cde5-134">Wählen Sie das Feld **Übermittlungsanweisungen** aus, um festzulegen, wo der Platzhalter erscheinen soll.</span><span class="sxs-lookup"><span data-stu-id="8cde5-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8cde5-135">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8cde5-136">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="8cde5-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8cde5-137">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-137">Click **Insert**.</span></span>

4. <span data-ttu-id="8cde5-138">Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8cde5-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="8cde5-139">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="8cde5-140">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8cde5-141">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="8cde5-142">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8cde5-143">Zum Personalisieren des Texts können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8cde5-144">Anweisungen zum Eingeben eines Platzhalters finden Sie in Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="8cde5-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="8cde5-145">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="8cde5-146">Geben Sie an, wann dieser Workflow über Aktivierungsbedingungen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8cde5-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="8cde5-147">Sie können mehrere Workflows erstellen, die auf demselben Workflowtyp basieren.</span><span class="sxs-lookup"><span data-stu-id="8cde5-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="8cde5-148">Wenn mehrere Workflows vorhanden sind, die auf demselben Typ basieren, müssen Sie angeben, wann jeder Workflow mithilfe der Aktivierungsbedingungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cde5-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="8cde5-149">Wenn die Aktivierungsbedingungen nicht erfüllt sind, wird der Standardworkflow verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="8cde5-150">Wenn für einen Workflow-Typ nur eine Workflow-Konfiguration definiert ist, wird diese Workflow-Konfiguration unabhängig von den Aktivierungsbedingungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="8cde5-151">Sie können beispielsweise für jedes Land bzw. jede Region, in dem/der Sie tätig sind, einen Workflow für Bestellanforderungen erstellen, wie Bestellanforderungen Dänemark und Bestellanforderungen Spanien, mit den folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="8cde5-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="8cde5-152">"Bestellanforderungen Dänemark" wird verwendet, wenn: Land/Region = DK.</span><span class="sxs-lookup"><span data-stu-id="8cde5-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="8cde5-153">"Bestellanforderungen Spanien" wird verwendet, wenn: Land/Region = ES.</span><span class="sxs-lookup"><span data-stu-id="8cde5-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="8cde5-154">Gehen Sie folgendermaßen vor, um anzugeben, wann der von Ihnen konfigurierte Workflow verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cde5-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="8cde5-155">Klicken Sie im linken Bereich auf **Aktivierung**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="8cde5-156">Aktivieren Sie das Kontrollkästchen **Bedingungen für Ausführung des Workflows festlegen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="8cde5-157">Klicken Sie auf **Bedingung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="8cde5-158">Geben Sie eine Bedingung ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-158">Enter a condition.</span></span>
5. <span data-ttu-id="8cde5-159">Geben Sie alle notwendigen zusätzlichen Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="8cde5-160">Führen Sie den Workflow mit einigen Zieldatensätzen durch, um zu überprüfen, ob die Bedingung Datensätze korrekt einschließt und ausschließt.</span><span class="sxs-lookup"><span data-stu-id="8cde5-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="8cde5-161">Angeben, wann Benachrichtigungen gesendet werden</span><span class="sxs-lookup"><span data-stu-id="8cde5-161">Specify when notifications are sent</span></span>

<span data-ttu-id="8cde5-162">Wenn ein Dokument zur Verarbeitung übermittelt wird, wird eine Workflowinstanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="8cde5-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="8cde5-163">Benutzern können Benachrichtigungen gesendet werden, wenn auf diesem Workflow basierende Workflowinstanzen gestartet, abgeschlossen, beendet oder aufgrund eines Fehlers angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="8cde5-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="8cde5-164">Gehen Sie folgendermaßen vor, um anzugeben, wann Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cde5-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="8cde5-165">Klicken Sie im linken Bereich auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="8cde5-166">Aktivieren Sie das Kontrollkästchen für jedes Ereignis, das Benachrichtigungen auslösen soll:</span><span class="sxs-lookup"><span data-stu-id="8cde5-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="8cde5-167">**Gestartet** – Benachrichtigungen werden beim Start einer Workflowinstanz gesendet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="8cde5-168">**Beendet** – Benachrichtigungen werden gesendet, wenn eine Workflowinstanz aufgrund eines Fehlers beendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cde5-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="8cde5-169">**Abgeschlossen** – Benachrichtigungen werden beim Abschluss einer Workflowinstanz gesendet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="8cde5-170">**Nicht behebbar** – Benachrichtigungen werden gesendet, wenn eine Workflowinstanz aufgrund eines nicht behebbaren Fehlers beendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cde5-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="8cde5-171">**Beendet** – Benachrichtigungen werden beim Beenden einer Workflowinstanz gesendet.</span><span class="sxs-lookup"><span data-stu-id="8cde5-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="8cde5-172">Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="8cde5-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="8cde5-173">Geben Sie auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="8cde5-174">Zum Personalisieren des Texts können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8cde5-175">Platzhalter werden bei der Anzeige für Benutzer durch die entsprechenden Daten ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8cde5-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="8cde5-176">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="8cde5-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="8cde5-177">Klicken Sie in das Feld, um die Position des Platzhalters anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8cde5-178">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8cde5-179">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="8cde5-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8cde5-180">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="8cde5-181">Ein üblicherweise einzubeziehender **Benachrichtigungstext**-Platzhalter ist „Aktuelle Hinweise: %Workflow.Last note%“, der sämtliche Kommentare aus dem vorherigen Schritt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8cde5-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="8cde5-182">Führen Sie die folgenden Schritte aus, um Übersetzungen von Text hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8cde5-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="8cde5-183">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="8cde5-184">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="8cde5-185">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="8cde5-186">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8cde5-187">Zum Personalisieren des Texts können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8cde5-188">Anweisungen zum Eingeben eines Platzhalters finden Sie in Schritt 5.</span><span class="sxs-lookup"><span data-stu-id="8cde5-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="8cde5-189">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-189">Click **Close**.</span></span>

7. <span data-ttu-id="8cde5-190">Verwenden Sie auf der Registerkarte **Empfänger** die folgenden Optionen, um anzugeben, wer die Benachrichtigungen erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="8cde5-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8cde5-191">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="8cde5-191">Option</span></span></th>
    <th><span data-ttu-id="8cde5-192">Benachrichtigungen werden an diese Benutzer gesendet</span><span class="sxs-lookup"><span data-stu-id="8cde5-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="8cde5-193">Gehen Sie folgendermaßen vor, um Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="8cde5-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8cde5-194">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="8cde5-194">Participant</span></span></td>
    <td><span data-ttu-id="8cde5-195">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="8cde5-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8cde5-196">Klicken Sie auf der Registerkarte <strong>Empfänger</strong> auf <strong>Teilnehmer</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cde5-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="8cde5-197">Wählen Sie in der Liste <strong>Art von Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> die Art der Gruppe oder Rolle, an die die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="8cde5-198">Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8cde5-199">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="8cde5-199">Workflow user</span></span></td>
    <td><span data-ttu-id="8cde5-200">Benutzer, die an diesem Workflow teilnehmen</span><span class="sxs-lookup"><span data-stu-id="8cde5-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8cde5-201">Klicken Sie auf der Registerkarte <strong>Empfänger</strong> auf <strong>Workflowbenutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cde5-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="8cde5-202">Wählen Sie auf der Registerkarte <strong>Workflowbenutzer</strong> in der Liste <strong>Workflowbenutzer</strong>, einen Teilnehmer dieses Workflow aus.</span><span class="sxs-lookup"><span data-stu-id="8cde5-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8cde5-203">Benutzer</span><span class="sxs-lookup"><span data-stu-id="8cde5-203">User</span></span></td>
    <td><span data-ttu-id="8cde5-204">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="8cde5-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8cde5-205">Klicken Sie auf der Registerkarte <strong>Empfänger</strong> auf <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cde5-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="8cde5-206">Die Liste <strong>Verfügbare Benutzer</strong> auf der Registerkarte <strong>Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="8cde5-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8cde5-207">Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cde5-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="8cde5-208">Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8cde5-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="8cde5-209">Geben Sie Kommentare zu den Änderungen am Workflow ein</span><span class="sxs-lookup"><span data-stu-id="8cde5-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="8cde5-210">Gehen Sie folgendermaßen vor, um Kommentare zu den Änderungen am Workflow einzugeben.</span><span class="sxs-lookup"><span data-stu-id="8cde5-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="8cde5-211">Klicken Sie im linken Bereich auf **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="8cde5-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="8cde5-212">Geben Sie im Feld **Kommentare zum Workflow eingeben** Ihre Kommentare ein.</span><span class="sxs-lookup"><span data-stu-id="8cde5-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="8cde5-213">Prüfen Sie die Kommentare.</span><span class="sxs-lookup"><span data-stu-id="8cde5-213">Review your comments.</span></span> <span data-ttu-id="8cde5-214">Nach dem Hinzufügen von Kommentaren können diese nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8cde5-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="8cde5-215">Klicken Sie auf **Hinzufügen**, um Ihre Kommentare dem Bereich **Kommentarhistorie** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8cde5-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
