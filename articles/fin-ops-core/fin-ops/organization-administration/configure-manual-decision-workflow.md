---
title: Manuellen Entscheidungen in einem Workflow konfigurieren
description: Dieses Thema erläutert, wie Sie die Eigenschaften einer manuellen Entscheidung konfigurieren können.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 859e74b869fcf9b8a886f27f67f51bdf28819979
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698242"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="a2acd-103">Manuellen Entscheidungen in einem Workflow konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a2acd-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2acd-104">Dieses Thema erläutert, wie Sie die Eigenschaften einer manuellen Entscheidung konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="a2acd-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="a2acd-105">Klicken Sie zum Konfigurieren einer manuellen Entscheidung im Workflow-Editor mit der rechten Maustaste auf die manuelle Entscheidung, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a2acd-106">Verwenden Sie dann die folgenden Schritte aus, um die Eigenschaften der manuellen Entscheidung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a2acd-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="a2acd-107">Benennen der Entscheidung</span><span class="sxs-lookup"><span data-stu-id="a2acd-107">Name the decision</span></span>

<span data-ttu-id="a2acd-108">Gehen Sie folgendermaßen vor, um einen Namen für die manuelle Entscheidung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="a2acd-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a2acd-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die manuelle Entscheidung ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="a2acd-111">Eingeben einer Betreffzeile und von Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a2acd-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="a2acd-112">Sie müssen eine Betreffzeile und Anweisungen für Benutzer eingeben, die der manuellen Entscheidung zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a2acd-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="a2acd-113">Wenn Sie z. B. eine Entscheidung für Bestellanforderungen konfigurieren, werden dem Benutzer, der der Entscheidung zugewiesen ist, die Betreffzeile und Anweisungen auf der Seite **Bestellanforderungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="a2acd-114">Die Betreffzeile wird in einer Statusleiste auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="a2acd-115">Der Benutzer kann nun auf das Symbol in der Statusleiste klicken, um die Anweisungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="a2acd-116">Gehen Sie folgendermaßen vor, um eine Betreffzeile und Anweisungen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="a2acd-117">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a2acd-118">Geben Sie in der Registerkarte **Anweisungen** im Feld **Betreff für die Arbeitsaufgabe** die Betreffzeile ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="a2acd-119">Zum Personalisieren der Betreffzeile können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="a2acd-120">Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Betreffzeile Benutzern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a2acd-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="a2acd-121">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a2acd-122">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="a2acd-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a2acd-123">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a2acd-124">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a2acd-125">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-125">Click **Insert**.</span></span>

4. <span data-ttu-id="a2acd-126">Führen Sie die folgenden Schritte aus, um Übersetzungen der Betreffzeile hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="a2acd-127">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="a2acd-128">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a2acd-129">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a2acd-130">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a2acd-131">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 3 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="a2acd-132">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-132">Click **Close**.</span></span>

5. <span data-ttu-id="a2acd-133">Geben Sie im Feld **Arbeitsaufgabenanweisungen** die Arbeitsanweisungen ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="a2acd-134">Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="a2acd-135">Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="a2acd-136">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a2acd-137">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="a2acd-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a2acd-138">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a2acd-139">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a2acd-140">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-140">Click **Insert**.</span></span>

7. <span data-ttu-id="a2acd-141">Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="a2acd-142">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="a2acd-143">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a2acd-144">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a2acd-145">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a2acd-146">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 6 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="a2acd-147">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="a2acd-148">Angeben der möglichen Ergebnisse einer Entscheidung</span><span class="sxs-lookup"><span data-stu-id="a2acd-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="a2acd-149">Wenn ein Dokument einem Entscheidungsträger zugewiesen wird, wird dem Entscheidungsträger in der Regel eine Frage gestellt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="a2acd-150">Die Antwort auf diese Frage ist normalerweise **Ja** oder **Nein** oder **Wahr** oder **Falsch**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="a2acd-151">Gehen Sie folgendermaßen vor, um die möglichen Ergebnisse der manuellen Entscheidung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="a2acd-152">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a2acd-153">Geben Sie im Feld **Ergebnis 1** auf der Registerkarte **Ergebnisse** den Namen des Ergebnisses oder die Option ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="a2acd-154">Führen Sie die folgenden Schritte aus, um Übersetzungen von Ergebnissen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="a2acd-155">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="a2acd-156">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a2acd-157">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a2acd-158">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a2acd-159">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-159">Click **Close**.</span></span>

4. <span data-ttu-id="a2acd-160">Geben Sie im Feld **Ergebnis 2** den Namen des Ergebnisses oder die Option ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="a2acd-161">Führen Sie die folgenden Schritte aus, um Übersetzungen von Ergebnissen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="a2acd-162">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="a2acd-163">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a2acd-164">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a2acd-165">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a2acd-166">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a2acd-167">Angeben, wann Benachrichtigungen gesendet werden</span><span class="sxs-lookup"><span data-stu-id="a2acd-167">Specify when notifications are sent</span></span>

<span data-ttu-id="a2acd-168">Sie können Benachrichtigungen an Personen senden, wenn eine Entscheidung getroffen, delegiert oder eskaliert wurde.</span><span class="sxs-lookup"><span data-stu-id="a2acd-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="a2acd-169">Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="a2acd-170">Klicken Sie im linken Bereich auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="a2acd-171">Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="a2acd-172">**\[Auswahl 1\]** – Der zugewiesene Benutzer hat **\[Auswahl 1\]** gewählt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="a2acd-173">**\[Auswahl 2\]** – Der zugewiesene Benutzer hat **\[Auswahl 2\]** gewählt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="a2acd-174">**Delegieren** – Der zugewiesene Benutzer hat die Entscheidung einem anderen Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="a2acd-175">**Eskalieren** – Der zugewiesene Benutzer hat die Entscheidung nicht innerhalb der vorgesehenen Zeit getroffen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="a2acd-176">Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="a2acd-177">Geben Sie im Textfeld auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="a2acd-178">Zum Personalisieren der Benachrichtigung können Sie Platzhalter einfügen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="a2acd-179">Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Benachrichtigung Benutzern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a2acd-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="a2acd-180">Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a2acd-181">Klicken Sie im Textfeld die Position des Platzhalters an.</span><span class="sxs-lookup"><span data-stu-id="a2acd-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a2acd-182">Klicken Sie auf **Platzhalter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a2acd-183">Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a2acd-184">Klicken Sie auf **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-184">Click **Insert**.</span></span>

6. <span data-ttu-id="a2acd-185">Führen Sie die folgenden Schritte aus, um Übersetzungen von Benachrichtigungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="a2acd-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="a2acd-186">Klicken Sie auf **Übersetzungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="a2acd-187">Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a2acd-188">Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a2acd-189">Geben Sie den Text im Feld **Übersetzter Text** ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a2acd-190">Um den Text zu personalisieren, können Platzhalter, wie in Schritt 5 beschrieben, eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="a2acd-191">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-191">Click **Close**.</span></span>

7. <span data-ttu-id="a2acd-192">Auf der Registerkarte **Empfänger** geben Sie an, an wen die Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="a2acd-193">Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für diese Option aus, bevor Sie mit Schritt 8 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a2acd-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a2acd-194">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="a2acd-194">Option</span></span></th>
    <th><span data-ttu-id="a2acd-195">Empfänger der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a2acd-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="a2acd-196">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="a2acd-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a2acd-197">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="a2acd-197">Participant</span></span></td>
    <td><span data-ttu-id="a2acd-198">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="a2acd-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-199">Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Benachrichtigung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a2acd-200">Wählen Sie in der Liste <strong>Teilnehmer</strong> die aus, an die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-201">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-201">Workflow user</span></span></td>
    <td><span data-ttu-id="a2acd-202">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="a2acd-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a2acd-203">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-204">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-204">User</span></span></td>
    <td><span data-ttu-id="a2acd-205">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-206">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a2acd-207">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a2acd-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a2acd-208">Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="a2acd-209">Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a2acd-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="a2acd-210">Zuweisen einer Entscheidung</span><span class="sxs-lookup"><span data-stu-id="a2acd-210">Assign a decision</span></span>

<span data-ttu-id="a2acd-211">Gehen Sie folgendermaßen vor, um anzugeben, wem eine manuelle Aufgabe zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="a2acd-212">Klicken Sie im linken Bereich auf **Zuweisung**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="a2acd-213">Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 3 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a2acd-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a2acd-214">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="a2acd-214">Option</span></span></th>
    <th><span data-ttu-id="a2acd-215">Benutzer, denen die Entscheidung zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="a2acd-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="a2acd-216">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="a2acd-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a2acd-217">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="a2acd-217">Participant</span></span></td>
    <td><span data-ttu-id="a2acd-218">Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="a2acd-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-219">Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Entscheidung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="a2acd-220">Wählen Sie in der Liste <strong>Teilnehmer</strong> den Typ der Gruppe oder Rolle aus, dem die Entscheidung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-221">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="a2acd-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="a2acd-222">Benutzer in einer bestimmten Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="a2acd-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-223">Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem die Entscheidung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="a2acd-224">Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="a2acd-225">Diese Namen stellen Benutzer dar, denen die Entscheidung zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2acd-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="a2acd-226">Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="a2acd-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="a2acd-227">Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="a2acd-228">Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="a2acd-229">Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="a2acd-230">Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich die Entscheidung zugewiesen werden soll:</span><span class="sxs-lookup"><span data-stu-id="a2acd-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="a2acd-231"><strong>Allen abgerufenen Benutzern zuordnen</strong> – Die Entscheidung wird allen Benutzern im Bereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a2acd-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="a2acd-232"><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Die Entscheidung wird nur dem letzten Benutzer im Bereich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="a2acd-233"><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Die Entscheidung wird keinem Benutzer im Bereich zugewiesen, der eine bestimmte Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="a2acd-234">Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-235">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-235">Workflow user</span></span></td>
    <td><span data-ttu-id="a2acd-236">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="a2acd-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a2acd-237">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-238">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-238">User</span></span></td>
    <td><span data-ttu-id="a2acd-239">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-240">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a2acd-241">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a2acd-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a2acd-242">Wählen Sie die Benutzer aus, um die Entscheidung zuzuweisen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="a2acd-243">Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Treffen der Entscheidung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a2acd-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="a2acd-244">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="a2acd-244">Select one of the following options:</span></span>

    - <span data-ttu-id="a2acd-245">**Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Treffen der Entscheidung hat.</span><span class="sxs-lookup"><span data-stu-id="a2acd-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="a2acd-246">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a2acd-247">**Tage** – Geben Sie die Anzahl von Tagen ein, die der Benutzer zum Treffen der Entscheidung hat.</span><span class="sxs-lookup"><span data-stu-id="a2acd-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="a2acd-248">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a2acd-249">**Wochen** – Geben Sie die Anzahl von Wochen ein, die der Benutzer zum Treffen der Entscheidung hat.</span><span class="sxs-lookup"><span data-stu-id="a2acd-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="a2acd-250">**Monate** – Wählen Sie den Tag, und die Woche aus, bis zu dem der Benutzer die Entscheidung treffen muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="a2acd-251">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats die Entscheidung treffen soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a2acd-252">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer die Entscheidung treffen muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="a2acd-253">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember die Entscheidung treffen soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="a2acd-254">Wenn der Benutzer die Entscheidung nicht innerhalb der vorgesehenen Zeit trifft, ist die Entscheidung überfällig.</span><span class="sxs-lookup"><span data-stu-id="a2acd-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="a2acd-255">Eine überfällige Entscheidung wird basierend auf den ausgewählten Optionen im Bereich **Eskalation** der Seite eskaliert.</span><span class="sxs-lookup"><span data-stu-id="a2acd-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="a2acd-256">Festlegen der Vorgehensweise für überfällige Entscheidungen</span><span class="sxs-lookup"><span data-stu-id="a2acd-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="a2acd-257">Wenn der Benutzer die Entscheidung nicht innerhalb der vorgesehenen Zeit trifft, ist die Entscheidung überfällig.</span><span class="sxs-lookup"><span data-stu-id="a2acd-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="a2acd-258">Eine überfällige Entscheidung kann eskaliert oder automatisch einem anderen Benutzer zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="a2acd-259">Führen Sie die folgenden Schritte aus, um die Entscheidung zu eskalieren, wenn sie überfällig ist.</span><span class="sxs-lookup"><span data-stu-id="a2acd-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="a2acd-260">Klicken Sie im linken Bereich auf **Eskalation**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="a2acd-261">Aktivieren Sie das Kontrollkästchen **Eskalationspfad verwenden**, um einen Eskalationspfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="a2acd-262">Die Entscheidung wird automatisch den im Eskalationspfad aufgeführten Benutzern zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="a2acd-263">Die folgende Tabelle stellt z. B. einen Eskalationspfad dar.</span><span class="sxs-lookup"><span data-stu-id="a2acd-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="a2acd-264">Sequenz</span><span class="sxs-lookup"><span data-stu-id="a2acd-264">Sequence</span></span> | <span data-ttu-id="a2acd-265">Eskalationspfad</span><span class="sxs-lookup"><span data-stu-id="a2acd-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="a2acd-266">1</span><span class="sxs-lookup"><span data-stu-id="a2acd-266">1</span></span>        | <span data-ttu-id="a2acd-267">Zuweisen zu: Doris</span><span class="sxs-lookup"><span data-stu-id="a2acd-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="a2acd-268">2</span><span class="sxs-lookup"><span data-stu-id="a2acd-268">2</span></span>        | <span data-ttu-id="a2acd-269">Zuweisen zu: Elke</span><span class="sxs-lookup"><span data-stu-id="a2acd-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="a2acd-270">3</span><span class="sxs-lookup"><span data-stu-id="a2acd-270">3</span></span>        | <span data-ttu-id="a2acd-271">Abschließende Aktivität: \[Auswahl 1\]</span><span class="sxs-lookup"><span data-stu-id="a2acd-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="a2acd-272">In diesem Beispiel wird die überfällige Entscheidung Doris zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="a2acd-273">Trifft Doris die Entscheidung nicht innerhalb der vorgesehenen Zeit, wird die Entscheidung Elke zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="a2acd-274">Wenn Erin die Entscheidung nicht innerhalb der vorgesehenen Zeit trifft, wählt das System **\[Auswahl 1\]** als Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="a2acd-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="a2acd-275">Klicken Sie auf **Eskalation hinzufügen**, um dem Eskalationspfad einen Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="a2acd-276">Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für diese Option aus, bevor Sie mit Schritt 4 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a2acd-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a2acd-277">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="a2acd-277">Option</span></span></th>
    <th><span data-ttu-id="a2acd-278">Benutzer, denen die Entscheidung eskaliert wird</span><span class="sxs-lookup"><span data-stu-id="a2acd-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="a2acd-279">Zusätzliche Schritte</span><span class="sxs-lookup"><span data-stu-id="a2acd-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a2acd-280">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="a2acd-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="a2acd-281">Benutzer in einer bestimmten Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="a2acd-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-282">Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, an den die Entscheidung eskaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="a2acd-283">Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a2acd-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="a2acd-284">Diese Namen stellen Benutzer dar, denen die Entscheidung eskaliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2acd-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="a2acd-285">Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="a2acd-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="a2acd-286">Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="a2acd-287">Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="a2acd-288">Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="a2acd-289">Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, an welche Benutzer im Bereich die Entscheidung eskaliert werden soll:</span><span class="sxs-lookup"><span data-stu-id="a2acd-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="a2acd-290"><strong>Allen abgerufenen Benutzern zuordnen</strong> – Die Entscheidung wird an alle Benutzer im Bereich eskaliert.</span><span class="sxs-lookup"><span data-stu-id="a2acd-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="a2acd-291"><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Die Entscheidung wird nur an den letzten Benutzer im Bereich eskaliert.</span><span class="sxs-lookup"><span data-stu-id="a2acd-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="a2acd-292"><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Die Entscheidung wird keinem Benutzer im Bereich eskaliert, der eine bestimmte Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="a2acd-293">Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2acd-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-294">Workflowbenutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-294">Workflow user</span></span></td>
    <td><span data-ttu-id="a2acd-295">Benutzer im aktuellen Workflow</span><span class="sxs-lookup"><span data-stu-id="a2acd-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a2acd-296">Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="a2acd-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a2acd-297">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-297">User</span></span></td>
    <td><span data-ttu-id="a2acd-298">Bestimmte Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2acd-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a2acd-299">Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a2acd-300">Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a2acd-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a2acd-301">Wählen Sie die Benutzer aus, an die die Entscheidung eskaliert werden soll, und verschieben Sie diese Benutzer in die Liste <strong>Ausgewählte Benutzer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2acd-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="a2acd-302">Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Treffen der Entscheidung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a2acd-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="a2acd-303">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="a2acd-303">Select one of the following options:</span></span>

    - <span data-ttu-id="a2acd-304">**Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Treffen der Entscheidung hat.</span><span class="sxs-lookup"><span data-stu-id="a2acd-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="a2acd-305">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a2acd-306">**Tage** – Geben Sie die Anzahl von Tagen ein, die der Benutzer zum Treffen der Entscheidung hat.</span><span class="sxs-lookup"><span data-stu-id="a2acd-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="a2acd-307">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a2acd-308">**Wochen** – Geben Sie die Anzahl von Wochen ein, die der Benutzer zum Treffen der Entscheidung hat.</span><span class="sxs-lookup"><span data-stu-id="a2acd-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="a2acd-309">**Monate** – Wählen Sie den Tag, und die Woche aus, bis zu dem der Benutzer die Entscheidung treffen muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="a2acd-310">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats die Entscheidung treffen soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a2acd-311">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer die Entscheidung treffen muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="a2acd-312">Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember die Entscheidung treffen soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="a2acd-313">Wiederholen Sie die Schritte 3 bis 4 für alle Benutzer, die dem Eskalationspfad hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="a2acd-314">Sie können die Reihenfolge der Benutzer ändern.</span><span class="sxs-lookup"><span data-stu-id="a2acd-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="a2acd-315">Wenn die Benutzer im Eskalationspfad die Entscheidung nicht innerhalb der vorgesehenen Zeit treffen, wird die Entscheidung automatisch getroffen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="a2acd-316">Um die vom System auszuwählende Option anzugeben, wählen Sie die Zeile **Aktivität** aus, klicken Sie dann auf die Registerkarte **Aktivität bei Beendigung** und wählen eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="a2acd-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="a2acd-317">Festlegen einer Zeitgrenze</span><span class="sxs-lookup"><span data-stu-id="a2acd-317">Set a time limit</span></span>

<span data-ttu-id="a2acd-318">Gehen Sie folgendermaßen vor, wenn die Entscheidung in einer bestimmten Zeit getroffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="a2acd-319">Die hier ausgewählten Optionen setzen die Optionen außer Kraft, die Sie in den Bereichen **Zuweisung**und **Eskalation** der Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="a2acd-320">Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="a2acd-321">Aktivieren Sie das Kontrollkästchen **Zeitgrenze für das Workflowelement festlegen**.</span><span class="sxs-lookup"><span data-stu-id="a2acd-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="a2acd-322">Legen Sie im Feld **Dauer** fest, wann die Entscheidung getroffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="a2acd-323">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="a2acd-323">Select one of the following options:</span></span>

    - <span data-ttu-id="a2acd-324">**Stunden** – Geben Sie die Anzahl der Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="a2acd-325">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a2acd-326">**Tage** – Geben Sie die Anzahl von Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="a2acd-327">Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a2acd-328">**Wochen** – Geben Sie die Anzahl von Wochen ein.</span><span class="sxs-lookup"><span data-stu-id="a2acd-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="a2acd-329">**Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem die Entscheidung getroffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="a2acd-330">Sie können z. B. angeben, dass die Entscheidung bis Freitag der dritten Woche des Monats getroffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a2acd-331">**Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem die Entscheidung getroffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a2acd-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="a2acd-332">Sie können z. B. angeben, dass die Entscheidung bis Freitag der dritten Woche im Dezember getroffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="a2acd-333">Wenn die Zeitgrenze überschritten wird, wird die Entscheidung automatisch getroffen.</span><span class="sxs-lookup"><span data-stu-id="a2acd-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="a2acd-334">Wählen Sie in der Liste **Aktivität** die Option aus, die automatisch vom System ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2acd-334">In the **Action** list, select the option that the system should select.</span></span>
