---
title: Urlaubsanträge in Teams verwalten
description: In diesem Thema wird beschrieben, wie Sie arbeitsfreie Zeit in der Dynamics 365 Human Resources-App in Microsoft Teams beantragen.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3929992"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="75a26-103">Urlaubsanträge in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="75a26-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="75a26-104">Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Sie schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen.</span><span class="sxs-lookup"><span data-stu-id="75a26-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="75a26-105">Sie können mit einem Bot interagieren, um Informationen anzufordern und eine Urlaubsanfrage zu starten.</span><span class="sxs-lookup"><span data-stu-id="75a26-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="75a26-106">Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen.</span><span class="sxs-lookup"><span data-stu-id="75a26-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="75a26-107">Darüber hinaus können Sie Personen Informationen über Ihre bevorstehende arbeitsfreie Zeit in Teams und Chats außerhalb der Human Resources-App senden.</span><span class="sxs-lookup"><span data-stu-id="75a26-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="75a26-108">App installieren</span><span class="sxs-lookup"><span data-stu-id="75a26-108">Install the app</span></span>

<span data-ttu-id="75a26-109">Sie finden die Human Resources-App im Teams Store.</span><span class="sxs-lookup"><span data-stu-id="75a26-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="75a26-110">Wählen Sie in Microsoft Teams die drei Punkte aus.</span><span class="sxs-lookup"><span data-stu-id="75a26-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Ellipsen](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="75a26-112">Suchen Sie nach Dynamics 365 Human Resources, und wählen Sie dann die Kachel **Human Resources** aus.</span><span class="sxs-lookup"><span data-stu-id="75a26-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Kachel „Human Resources“](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="75a26-114">Wählen Sie die Schaltfläche **Hinzufügen** aus, um die App zu installieren.</span><span class="sxs-lookup"><span data-stu-id="75a26-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Installation](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="75a26-116">Wenn Sie nicht automatisch von der App angemeldet werden, wählen Sie die Registerkarte **Einstellungen** aus, um sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="75a26-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Einstellungen“](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="75a26-118">Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="75a26-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="75a26-119">Wenn Sie Zugriff auf mehrere Human Resources-Instanzen haben, können Sie auf der Registerkarte **Einstellungen** festlegen, zu welcher Umgebung Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="75a26-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="75a26-120">Die App unterstützt jetzt die Sicherheitsrolle des Systemadministrators.</span><span class="sxs-lookup"><span data-stu-id="75a26-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="75a26-121">Bot verwenden</span><span class="sxs-lookup"><span data-stu-id="75a26-121">Use the bot</span></span>

<span data-ttu-id="75a26-122">Nach der Installation der App wird eine Willkommensnachricht angezeigt, in der Sie über die Aktivitätstypen informiert werden, die der Bot in Ihrem Namen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="75a26-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Willkommensnachricht für Bot](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="75a26-124">Bei der ersten Interaktion mit dem Bot müssen Sie sich möglicherweise anmelden.</span><span class="sxs-lookup"><span data-stu-id="75a26-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="75a26-125">Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="75a26-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="75a26-126">Sie können den Bot bitten, die folgenden Aktionen durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="75a26-126">You can ask the bot to:</span></span>

- <span data-ttu-id="75a26-127">Informationen zum Freizeitguthaben für jeden Urlaubstyp anzeigen, für den Sie sich angemeldet haben</span><span class="sxs-lookup"><span data-stu-id="75a26-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Salden anzeigen](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="75a26-129">Zusätzliche Details zu einem bestimmten Urlaubstyp anzeigen</span><span class="sxs-lookup"><span data-stu-id="75a26-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Details anzeigen](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="75a26-131">Urlaubsanforderung für Sie starten</span><span class="sxs-lookup"><span data-stu-id="75a26-131">Start a leave request for you.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Urlaubsanforderung](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="75a26-133">Nachdem Sie einen Urlaubsantrag gestellt haben, können Sie die Tage direkt auf der Karte anpassen.</span><span class="sxs-lookup"><span data-stu-id="75a26-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Anforderung bearbeiten](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="75a26-135">Wenn Sie die Informationen eingegeben haben, wählen Sie **Absenden** aus, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="75a26-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="75a26-136">Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="75a26-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Anforderung senden](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="75a26-138">Urlaub in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="75a26-138">Manage your leave in Teams</span></span>

<span data-ttu-id="75a26-139">Auf der Registerkarte **Arbeitsfreie Zeit** können Sie Folgendes anzeigen:</span><span class="sxs-lookup"><span data-stu-id="75a26-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="75a26-140">Saldoinformationen für jeden Urlaubstyp anzeigen, für den Sie registriert sind</span><span class="sxs-lookup"><span data-stu-id="75a26-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="75a26-141">Anstehende Urlaubsanforderungen</span><span class="sxs-lookup"><span data-stu-id="75a26-141">Upcoming leave requests</span></span>

- <span data-ttu-id="75a26-142">Anforderungen von arbeitsfreier Zeit</span><span class="sxs-lookup"><span data-stu-id="75a26-142">Time-off requests</span></span>

- <span data-ttu-id="75a26-143">Urlaubsanforderungen entwerfen</span><span class="sxs-lookup"><span data-stu-id="75a26-143">Draft leave requests</span></span>

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="75a26-145">Neue Anforderung erstellen</span><span class="sxs-lookup"><span data-stu-id="75a26-145">Create a new request</span></span>

1. <span data-ttu-id="75a26-146">Wählen Sie **Neue Anforderung** aus, um eine neue Urlaubsanforderung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="75a26-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Neue Anforderung](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="75a26-148">Geben Sie den/die Tag(e) ein, den/die Sie sich frei nehmen möchten, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="75a26-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Arbeitsfreie Zeit hinzufügen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="75a26-150">Geben Sie gegebenenfalls einen Ursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="75a26-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="75a26-151">Geben Sie auch Kommentare ein, und fügen Sie Anhänge hinzu.</span><span class="sxs-lookup"><span data-stu-id="75a26-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="75a26-152">Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="75a26-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="75a26-153">Sie können auch **Als Entwurf speichern** eingeben, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="75a26-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="75a26-154">Entwurfsanforderungen verwalten</span><span class="sxs-lookup"><span data-stu-id="75a26-154">Manage draft requests</span></span>

1. <span data-ttu-id="75a26-155">Wählen Sie die Registerkarte **Entwürfe** aus.</span><span class="sxs-lookup"><span data-stu-id="75a26-155">Select the **Drafts** tab.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Entwürfe“](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="75a26-157">Wählen Sie den Stift aus, um die Anforderung zu bearbeiten, oder wählen Sie den Papierkorb aus, um die Anforderung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="75a26-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="75a26-158">Nehmen Sie die erforderlichen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="75a26-158">Make any necessary changes.</span></span> <span data-ttu-id="75a26-159">Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="75a26-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="75a26-160">Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="75a26-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – „Entwurf bearbeiten“](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="75a26-162">Antworten auf Teams-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="75a26-162">Respond to Teams notifications</span></span>

<span data-ttu-id="75a26-163">Wenn Sie oder ein Mitarbeiter, für den Sie Genehmiger sind, einen Urlaubsantrag stellen, erhalten Sie eine Benachrichtigung in der Human Resources-App in Teams.</span><span class="sxs-lookup"><span data-stu-id="75a26-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="75a26-164">Sie können die Benachrichtigung auswählen, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="75a26-164">You can select the notification to view it.</span></span> <span data-ttu-id="75a26-165">Benachrichtigungen werden auch im **Plaudern**-Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75a26-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="75a26-166">Wenn Sie ein Genehmiger sind, können Sie in der Benachrichtigung **Genehmigen** oder **Verweigern** auswählen.</span><span class="sxs-lookup"><span data-stu-id="75a26-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="75a26-167">Sie können auch eine optionale Nachricht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="75a26-167">You can also provide an optional message.</span></span>

![Urlaubsantragsbenachrichtigungen in der Human Resources-Teams-App](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="75a26-169">Informationen zu bevorstehender arbeitsfreier Zeit an Ihre Kollegen senden</span><span class="sxs-lookup"><span data-stu-id="75a26-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="75a26-170">Nachdem Sie die Human Resources-App für Teams installiert haben, können Sie Ihren Kollegen in Teams oder Chats problemlos Informationen zu Ihrer arbeitsfreien Zeit senden.</span><span class="sxs-lookup"><span data-stu-id="75a26-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="75a26-171">Wählen Sie in einem Team oder Chat in Teams die Schaltfläche Human Resources unter dem Chatfenster.</span><span class="sxs-lookup"><span data-stu-id="75a26-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Schaltfläche „Human Resources“ unter dem Chatfenster](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="75a26-173">Wählen Sie die Urlaubsanfrage aus, die Sie teilen möchten.</span><span class="sxs-lookup"><span data-stu-id="75a26-173">Select the leave request you want to share.</span></span> <span data-ttu-id="75a26-174">Wenn Sie einen Entwurf für einen Urlaubsantrag freigeben möchten, wählen Sie zuerst **Entwürfe**.</span><span class="sxs-lookup"><span data-stu-id="75a26-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Einen bevorstehenden Urlaubsantrag zum Teilen auswählen](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="75a26-176">Ihre Urlaubsanfrage wird im Chat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75a26-176">Your leave request will display in the chat.</span></span>

![Urlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="75a26-178">Wenn Sie einen Entwurfsantrag freigegeben haben, wird dieser als Entwurf angezeigt:</span><span class="sxs-lookup"><span data-stu-id="75a26-178">If you shared a draft request, it will display as a draft:</span></span>

![Entwurfsurlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="75a26-180">Urlaubskalender Ihres Teams anzeigen</span><span class="sxs-lookup"><span data-stu-id="75a26-180">View your team's leave calendar</span></span>

<span data-ttu-id="75a26-181">Wenn Sie ein Manager mit direkten Berichten sind, können Sie die genehmigte und ausstehende arbeitsfreie Zeit Ihres Teams anzeigen.</span><span class="sxs-lookup"><span data-stu-id="75a26-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="75a26-182">Wählen Sie in der Human Resources-App in Teams die Option aus **Arbeitsfreie Zeit** aus.</span><span class="sxs-lookup"><span data-stu-id="75a26-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="75a26-183">Wählen Sie **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="75a26-183">Select **Team calendar**.</span></span>

   ![Kalender in der Human Resources-Teams-App anzeigen](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="75a26-185">Der Kalender zeigt die genehmigte und ausstehende arbeitsfreie Zeit Ihrer direkten Berichte an.</span><span class="sxs-lookup"><span data-stu-id="75a26-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Kalender für arbeitsfreie Zeit in der Human Resources-Teams-App](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="75a26-187">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="75a26-187">Troubleshooting</span></span>

<span data-ttu-id="75a26-188">Wenn Sie Probleme beim Anmelden oder Verwenden der Human Resources Teams-App haben, befolgen Sie diese Anweisungen zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="75a26-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="75a26-189">Wenn Sie nach der Problembehandlung immer noch Probleme haben, wenden Sie sich an den Support.</span><span class="sxs-lookup"><span data-stu-id="75a26-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="75a26-190">Weitere Informationen erhalten Sie über den [Support](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="75a26-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="75a26-191">Sie können sich nicht in Teams bei der Human Resources-App anmelden</span><span class="sxs-lookup"><span data-stu-id="75a26-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="75a26-192">Wenn Sie sich nicht bei der App anmelden können, ist es möglich, dass das Konto, das Sie zur Anmeldung bei Microsoft Teams verwenden, keinem Mitarbeiterdatensatz in Dynamics 365 Human Resources zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75a26-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="75a26-193">Wenden Sie sich an Ihren Systemadministrator, um sicherzustellen, dass Ihr Mitarbeiterdatensatz korrekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75a26-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="75a26-194">Fehler beim Genehmigen von Urlaubsanträgen in der Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="75a26-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="75a26-195">Wenn Sie beim Versuch, Urlaubsanforderungen in der Teams-App zu genehmigen, eine Fehlermeldung erhalten, führen Sie die folgenden Schritte zur Problembehandlung aus:</span><span class="sxs-lookup"><span data-stu-id="75a26-195">If you receive an error when you're trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="75a26-196">Stellen Sie sicher, dass das Konto, mit dem Sie sich bei Microsoft Teams anmelden, dasselbe ist, mit dem Sie auf Dynamics 365 Human Resources zugreifen.</span><span class="sxs-lookup"><span data-stu-id="75a26-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="75a26-197">Stellen Sie sicher, dass Sie ein gültiger Genehmiger für die Anforderung sind, indem Sie die Workflow-Einstellungen auf Urlaubsgenehmigung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="75a26-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="75a26-198">Weitere Informationen zu Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="75a26-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="75a26-199">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="75a26-199">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="75a26-200">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="75a26-200">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="75a26-201">Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="75a26-201">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="75a26-202">Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="75a26-202">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="75a26-203">Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="75a26-203">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="75a26-204">Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso).</span><span class="sxs-lookup"><span data-stu-id="75a26-204">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="75a26-205">Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft.</span><span class="sxs-lookup"><span data-stu-id="75a26-205">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="75a26-206">Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt.</span><span class="sxs-lookup"><span data-stu-id="75a26-206">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="75a26-207">Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf.</span><span class="sxs-lookup"><span data-stu-id="75a26-207">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="75a26-208">Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="75a26-208">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="75a26-209">Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="75a26-209">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="75a26-210">Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="75a26-210">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="75a26-211">Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="75a26-211">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="75a26-212">Microsoft Teams, Azure Event Grid und Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="75a26-212">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="75a26-213">Bei Verwendung der Dynamics 365 Human Resources-App in Microsoft Teams fließen möglicherweise bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="75a26-213">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="75a26-214">Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="75a26-214">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="75a26-215">Diese Daten können bis zu 24 Stunden in Microsoft Azure Event Grid gespeichert werden und werden in den USA verarbeitet, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="75a26-215">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="75a26-216">Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="75a26-216">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="75a26-217">Während der Konversation mit dem Chat-Bot in der Human Resources-App wird der Konversationsinhalt möglicherweise in Azure Cosmos DB gespeichert und an Microsoft Teams übertragen.</span><span class="sxs-lookup"><span data-stu-id="75a26-217">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="75a26-218">Diese Daten können in Azure Cosmos DB bis zu 24 Stunden lang gespeichert und außerhalb der geografischen Region verarbeitet werden, in der der Human Resources-Service Ihres Mandanten bereitgestellt wird, werden während des Transports und in Ruhe verschlüsselt und von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="75a26-218">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="75a26-219">Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="75a26-219">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="75a26-220">Um den Zugriff auf die Human Resources-App in Microsoft Teams für Ihre Organisation oder Benutzer in Ihrer Organisation zu beschränken, finden Sie unter Informationen unter [Verwalten von App-Berechtigungsrichtlinien in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="75a26-220">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="75a26-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75a26-221">See also</span></span>

[<span data-ttu-id="75a26-222">Microsoft Teams herunterladen und installieren</span><span class="sxs-lookup"><span data-stu-id="75a26-222">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="75a26-223">Microsoft Teams-Hilfecenter</span><span class="sxs-lookup"><span data-stu-id="75a26-223">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="75a26-224">Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="75a26-224">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
