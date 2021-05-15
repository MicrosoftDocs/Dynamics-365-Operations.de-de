---
title: Urlaubsanträge in Teams verwalten
description: In diesem Thema wird beschrieben, wie Sie arbeitsfreie Zeit in der Dynamics 365 Human Resources-App in Microsoft Teams beantragen.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2ea495259ba29f302753991e260d5a8fa990322b
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953411"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="247b1-103">Urlaubsanträge in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="247b1-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="247b1-104">Mit der Dynamics 365 Human Resources-App in Microsoft Teams können Sie schnell eine Auszeit beantragen und Ihre Informationen zum Zeitsaldo direkt in Microsoft Teams einsehen.</span><span class="sxs-lookup"><span data-stu-id="247b1-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="247b1-105">Sie können mit einem Bot interagieren, um Informationen anzufordern und eine Urlaubsanfrage zu starten.</span><span class="sxs-lookup"><span data-stu-id="247b1-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="247b1-106">Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen.</span><span class="sxs-lookup"><span data-stu-id="247b1-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="247b1-107">Sie können auch in Teams und Chats außerhalb der Human Resources App Informationen über Ihre bevorstehende Auszeit an andere Personen senden.</span><span class="sxs-lookup"><span data-stu-id="247b1-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="247b1-108">App installieren</span><span class="sxs-lookup"><span data-stu-id="247b1-108">Install the app</span></span>

<span data-ttu-id="247b1-109">Sie finden die App Dynamics 365 Human Resources im Teams-Store.</span><span class="sxs-lookup"><span data-stu-id="247b1-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="247b1-110">Wählen Sie in Microsoft Teams die drei Punkte aus.</span><span class="sxs-lookup"><span data-stu-id="247b1-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Ellipsen](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="247b1-112">Suchen Sie nach Dynamics 365 Human Resources, und wählen Sie dann die Kachel **Human Resources** aus.</span><span class="sxs-lookup"><span data-stu-id="247b1-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Kachel „Human Resources“](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="247b1-114">Wählen Sie die Schaltfläche **Hinzufügen** aus, um die App zu installieren.</span><span class="sxs-lookup"><span data-stu-id="247b1-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Installation](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="247b1-116">Wenn Sie nicht automatisch von der App angemeldet werden, wählen Sie die Registerkarte **Einstellungen** aus, um sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="247b1-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Einstellungen“](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="247b1-118">Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="247b1-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="247b1-119">Wenn Sie Zugriff auf mehrere Human Resources-Instanzen haben, können Sie auf der Registerkarte **Einstellungen** festlegen, zu welcher Umgebung Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="247b1-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="247b1-120">Die App unterstützt jetzt die Sicherheitsrolle des Systemadministrators.</span><span class="sxs-lookup"><span data-stu-id="247b1-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="247b1-121">Bot verwenden</span><span class="sxs-lookup"><span data-stu-id="247b1-121">Use the bot</span></span>

<span data-ttu-id="247b1-122">Nach der Installation der App wird eine Willkommensnachricht angezeigt, in der Sie über die Aktivitätstypen informiert werden, die der Bot in Ihrem Namen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="247b1-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Willkommensnachricht für Bot](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="247b1-124">Bei der ersten Interaktion mit dem Bot müssen Sie sich möglicherweise anmelden.</span><span class="sxs-lookup"><span data-stu-id="247b1-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="247b1-125">Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="247b1-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="247b1-126">Sie können den Bot bitten, die folgenden Aktionen durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="247b1-126">You can ask the bot to:</span></span>

- <span data-ttu-id="247b1-127">Urlaubsanforderung für Sie starten</span><span class="sxs-lookup"><span data-stu-id="247b1-127">Start a leave request for you.</span></span>

  ![Starten Sie einen Urlaubsantrag im Teams-Chat](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="247b1-129">Der Chat-Bot wird einen Urlaubsantrag für Sie ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="247b1-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="247b1-130">Wählen Sie **Abwesenheitsantrag** und bearbeiten Sie die Details für Ihren Antrag.</span><span class="sxs-lookup"><span data-stu-id="247b1-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Details des Urlaubsantrags bearbeiten](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="247b1-132">Wenn Sie mit der Bearbeitung der Details Ihres Urlaubsantrags fertig sind, wählen Sie **Senden**, um ihn zur Genehmigung zu senden.</span><span class="sxs-lookup"><span data-stu-id="247b1-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Urlaubsantrag senden](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="247b1-134">Urlaub in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="247b1-134">Manage your leave in Teams</span></span>

<span data-ttu-id="247b1-135">Auf der Registerkarte **Arbeitsfreie Zeit** können Sie Folgendes anzeigen:</span><span class="sxs-lookup"><span data-stu-id="247b1-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="247b1-136">Saldoinformationen für jeden Urlaubstyp anzeigen, für den Sie registriert sind</span><span class="sxs-lookup"><span data-stu-id="247b1-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="247b1-137">Anstehende Urlaubsanforderungen</span><span class="sxs-lookup"><span data-stu-id="247b1-137">Upcoming leave requests</span></span>

- <span data-ttu-id="247b1-138">Anforderungen von arbeitsfreier Zeit</span><span class="sxs-lookup"><span data-stu-id="247b1-138">Time-off requests</span></span>

- <span data-ttu-id="247b1-139">Urlaubsanforderungen entwerfen</span><span class="sxs-lookup"><span data-stu-id="247b1-139">Draft leave requests</span></span>

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="247b1-141">Neue Anforderung erstellen</span><span class="sxs-lookup"><span data-stu-id="247b1-141">Create a new request</span></span>

1. <span data-ttu-id="247b1-142">Wählen Sie **Neue Anforderung** aus, um eine neue Urlaubsanforderung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="247b1-142">To create a new leave request, select **New request**.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Neue Anforderung](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="247b1-144">Geben Sie den/die Tag(e) ein, den/die Sie sich frei nehmen möchten, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="247b1-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Arbeitsfreie Zeit hinzufügen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="247b1-146">Geben Sie gegebenenfalls einen Ursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="247b1-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="247b1-147">Geben Sie auch Kommentare ein, und fügen Sie Anhänge hinzu.</span><span class="sxs-lookup"><span data-stu-id="247b1-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="247b1-148">Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="247b1-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="247b1-149">Sie können auch **Als Entwurf speichern** eingeben, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="247b1-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="247b1-150">Entwurfsanforderungen verwalten</span><span class="sxs-lookup"><span data-stu-id="247b1-150">Manage draft requests</span></span>

1. <span data-ttu-id="247b1-151">Wählen Sie die Registerkarte **Entwürfe** aus.</span><span class="sxs-lookup"><span data-stu-id="247b1-151">Select the **Drafts** tab.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Entwürfe“](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="247b1-153">Wählen Sie den Stift aus, um die Anforderung zu bearbeiten, oder wählen Sie den Papierkorb aus, um die Anforderung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="247b1-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="247b1-154">Nehmen Sie die erforderlichen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="247b1-154">Make any necessary changes.</span></span> <span data-ttu-id="247b1-155">Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="247b1-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="247b1-156">Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="247b1-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – „Entwurf bearbeiten“](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="247b1-158">Antworten auf Teams-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="247b1-158">Respond to Teams notifications</span></span>

<span data-ttu-id="247b1-159">Wenn Sie oder ein Mitarbeiter, für den Sie Genehmiger sind, einen Urlaubsantrag stellen, erhalten Sie eine Benachrichtigung in der Human Resources-App in Teams.</span><span class="sxs-lookup"><span data-stu-id="247b1-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="247b1-160">Sie können die Benachrichtigung auswählen, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="247b1-160">You can select the notification to view it.</span></span> <span data-ttu-id="247b1-161">Benachrichtigungen werden auch im **Plaudern**-Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="247b1-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="247b1-162">Wenn Sie ein Genehmiger sind, können Sie in der Benachrichtigung **Genehmigen** oder **Verweigern** auswählen.</span><span class="sxs-lookup"><span data-stu-id="247b1-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="247b1-163">Sie können auch eine optionale Nachricht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="247b1-163">You can also provide an optional message.</span></span>

![Urlaubsantragsbenachrichtigungen in der Human Resources-Teams-App](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="247b1-165">Informationen zu bevorstehender arbeitsfreier Zeit an Ihre Kollegen senden</span><span class="sxs-lookup"><span data-stu-id="247b1-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="247b1-166">Nachdem Sie die Human Resources-App für Teams installiert haben, können Sie Ihren Kollegen in Teams oder Chats problemlos Informationen zu Ihrer arbeitsfreien Zeit senden.</span><span class="sxs-lookup"><span data-stu-id="247b1-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="247b1-167">Wählen Sie in einem Team oder Chat in Teams die Schaltfläche Human Resources unter dem Chatfenster.</span><span class="sxs-lookup"><span data-stu-id="247b1-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Schaltfläche „Human Resources“ unter dem Chatfenster](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="247b1-169">Wählen Sie die Urlaubsanfrage aus, die Sie teilen möchten.</span><span class="sxs-lookup"><span data-stu-id="247b1-169">Select the leave request you want to share.</span></span> <span data-ttu-id="247b1-170">Wenn Sie einen Entwurf für einen Urlaubsantrag freigeben möchten, wählen Sie zuerst **Entwürfe**.</span><span class="sxs-lookup"><span data-stu-id="247b1-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Einen bevorstehenden Urlaubsantrag zum Teilen auswählen](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="247b1-172">Ihre Urlaubsanfrage wird im Chat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="247b1-172">Your leave request will display in the chat.</span></span>

![Urlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="247b1-174">Wenn Sie einen Entwurfsantrag freigegeben haben, wird dieser als Entwurf angezeigt:</span><span class="sxs-lookup"><span data-stu-id="247b1-174">If you shared a draft request, it will display as a draft:</span></span>

![Entwurfsurlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="247b1-176">Urlaubskalender Ihres Teams anzeigen</span><span class="sxs-lookup"><span data-stu-id="247b1-176">View your team's leave calendar</span></span>

<span data-ttu-id="247b1-177">Wenn Sie ein Manager mit direkten Berichten sind, können Sie die genehmigte und ausstehende arbeitsfreie Zeit Ihres Teams anzeigen.</span><span class="sxs-lookup"><span data-stu-id="247b1-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="247b1-178">Wählen Sie in der Human Resources-App in Teams die Option aus **Arbeitsfreie Zeit** aus.</span><span class="sxs-lookup"><span data-stu-id="247b1-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="247b1-179">Wählen Sie **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="247b1-179">Select **Team calendar**.</span></span> <span data-ttu-id="247b1-180">Der Kalender zeigt die genehmigte und ausstehende arbeitsfreie Zeit Ihrer direkten Berichte an.</span><span class="sxs-lookup"><span data-stu-id="247b1-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Kalender in der Human Resources-Teams-App anzeigen](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="247b1-182">Wenn Sie den Team-Kalender nicht sehen können, bitten Sie Ihren Admin, ihn zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="247b1-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="247b1-183">Weitere Informationen finden Sie unter [Installation und Einrichten](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="247b1-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="247b1-184">Unterstützte Sprachen</span><span class="sxs-lookup"><span data-stu-id="247b1-184">Supported languages</span></span>

<span data-ttu-id="247b1-185">Die Dynamics 365 Human Resources App in Teams unterstützt die folgenden Sprachen:</span><span class="sxs-lookup"><span data-stu-id="247b1-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="247b1-186">Gebietsschema-ID</span><span class="sxs-lookup"><span data-stu-id="247b1-186">Locale ID</span></span> | <span data-ttu-id="247b1-187">Sprache</span><span class="sxs-lookup"><span data-stu-id="247b1-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="247b1-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="247b1-188">de-DE</span></span> | <span data-ttu-id="247b1-189">Deutsch (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="247b1-189">German (Germany)</span></span> |
| <span data-ttu-id="247b1-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="247b1-190">es-ES</span></span> | <span data-ttu-id="247b1-191">Spanisch (Spanien)</span><span class="sxs-lookup"><span data-stu-id="247b1-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="247b1-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="247b1-192">es-MX</span></span> | <span data-ttu-id="247b1-193">Spanisch (Mexiko)</span><span class="sxs-lookup"><span data-stu-id="247b1-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="247b1-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="247b1-194">fr-CA</span></span> | <span data-ttu-id="247b1-195">Französisch (Kanada)</span><span class="sxs-lookup"><span data-stu-id="247b1-195">French (Canada)</span></span> |
| <span data-ttu-id="247b1-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="247b1-196">fr-FR</span></span> | <span data-ttu-id="247b1-197">Französisch (Frankreich)</span><span class="sxs-lookup"><span data-stu-id="247b1-197">French (France)</span></span> |
| <span data-ttu-id="247b1-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="247b1-198">it-IT</span></span> | <span data-ttu-id="247b1-199">Italienisch (Italien)</span><span class="sxs-lookup"><span data-stu-id="247b1-199">Italian (Italy)</span></span> |
| <span data-ttu-id="247b1-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="247b1-200">nl-NL</span></span> | <span data-ttu-id="247b1-201">Niederländisch (Niederlande)</span><span class="sxs-lookup"><span data-stu-id="247b1-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="247b1-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="247b1-202">pt-BR</span></span> | <span data-ttu-id="247b1-203">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="247b1-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="247b1-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="247b1-204">tr-TR</span></span> | <span data-ttu-id="247b1-205">Türkisch (Türkei)</span><span class="sxs-lookup"><span data-stu-id="247b1-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="247b1-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="247b1-206">zh-CN</span></span> | <span data-ttu-id="247b1-207">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="247b1-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="247b1-208">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="247b1-208">Troubleshooting</span></span>

<span data-ttu-id="247b1-209">Wenn Sie Probleme bei der Anmeldung oder Verwendung der Dynamics 365 Human Resources Teams App haben, versuchen Sie, diese Anweisungen zur Fehlerbehebung zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="247b1-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="247b1-210">Wenn Sie nach der Problembehandlung immer noch Probleme haben, wenden Sie sich an den Support.</span><span class="sxs-lookup"><span data-stu-id="247b1-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="247b1-211">Weitere Informationen erhalten Sie über den [Support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="247b1-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="247b1-212">Sie können sich nicht in Teams bei der Human Resources-App anmelden</span><span class="sxs-lookup"><span data-stu-id="247b1-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="247b1-213">Wenn Sie sich nicht bei der App anmelden können, ist es möglich, dass das Konto, das Sie zur Anmeldung bei Microsoft Teams verwenden, keinem Mitarbeiterdatensatz in Dynamics 365 Human Resources zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="247b1-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="247b1-214">Wenden Sie sich an Ihren Systemadministrator, um sicherzustellen, dass Ihr Mitarbeiterdatensatz korrekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="247b1-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="247b1-215">Übersetzungen werden nicht korrekt angezeigt</span><span class="sxs-lookup"><span data-stu-id="247b1-215">Translations don't display correctly</span></span>

<span data-ttu-id="247b1-216">Wenn die Übersetzungen nicht wie erwartet angezeigt werden, stellen Sie sicher, dass die Sprache, die Sie in Teams auswählen, mit der in Human Resources **Benutzeroptionen** ausgewählten Sprache übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="247b1-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="247b1-217">In Teams sehen Sie sich **App-Sprache** in **Einstellungen** an.</span><span class="sxs-lookup"><span data-stu-id="247b1-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams-Einstellungen](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="247b1-219">Wählen Sie in Human Resources **Einstellungen** und wählen Sie dann **Benutzeroptionen**.</span><span class="sxs-lookup"><span data-stu-id="247b1-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="247b1-220">Stellen Sie sicher, dass das Feld **Sprache** mit dem Feld **App-Sprache** in Teams übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="247b1-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Human Resources Benutzeroptionen](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="247b1-222">Wenn Sie immer noch Übersetzungsprobleme haben, lassen Sie es uns wissen.</span><span class="sxs-lookup"><span data-stu-id="247b1-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="247b1-223">Informationen finden Sie unter [Unterstützung für Finance and Operations-Apps oder Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="247b1-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="247b1-224">Fehler beim Genehmigen von Urlaubsanträgen in der Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="247b1-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="247b1-225">Wenn Sie beim Versuch, Urlaubsanträge in der Teams-App zu genehmigen, eine Fehlermeldung erhalten, versuchen Sie es mit der folgenden Problembehandlung:</span><span class="sxs-lookup"><span data-stu-id="247b1-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="247b1-226">Stellen Sie sicher, dass das Konto, mit dem Sie sich bei Microsoft Teams anmelden, dasselbe ist, mit dem Sie auf Dynamics 365 Human Resources zugreifen.</span><span class="sxs-lookup"><span data-stu-id="247b1-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="247b1-227">Stellen Sie sicher, dass Sie ein gültiger Genehmiger für die Anforderung sind, indem Sie die Workflow-Einstellungen auf Urlaubsgenehmigung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="247b1-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="247b1-228">Weitere Informationen zu Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="247b1-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="247b1-229">Genehmiger von Abwesenheiten erhalten keine Teams-Chat-Nachrichten, um Abwesenheitsanträge zu genehmigen</span><span class="sxs-lookup"><span data-stu-id="247b1-229">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="247b1-230">Stellen Sie sicher, dass Benachrichtigungen für die Umgebung und den Benutzer aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="247b1-230">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="247b1-231">Weitere Informationen finden Sie unter [Benachrichtigungen für die Human Resources App in Teams aktivieren](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) und [Benachrichtigungen von Teams für einzelne Benutzer ein- oder ausschalten](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="247b1-231">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="247b1-232">Stellen Sie sicher, dass die Benutzer auf der Registerkarte **Chats** mit denselben Anmeldeinformationen angemeldet sind, die sie für die Genehmigung von Urlaubsanträgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="247b1-232">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="247b1-233">Verwenden Sie die Nachrichten „Abmelden“ und dann „Anmelden“, um sich mit den richtigen Anmeldeinformationen anzumelden.</span><span class="sxs-lookup"><span data-stu-id="247b1-233">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="247b1-234">Wenn das Problem weiterhin besteht, überprüfen Sie als Systemadministrator den Status des Batchauftrags für das System Business Events.</span><span class="sxs-lookup"><span data-stu-id="247b1-234">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="247b1-235">Wenn es sich in einer Warte- oder Ausführungsphase befindet, schauen Sie in ein paar Minuten noch einmal nach.</span><span class="sxs-lookup"><span data-stu-id="247b1-235">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="247b1-236">Wenn der Status unverändert bleibt, protokollieren Sie ein Support-Ticket, damit unser Team das Problem beheben kann.</span><span class="sxs-lookup"><span data-stu-id="247b1-236">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="247b1-237">Bekannte Probleme mit den Eingabehilfen</span><span class="sxs-lookup"><span data-stu-id="247b1-237">Known accessibility issues</span></span>

<span data-ttu-id="247b1-238">In der Human Resources-App in Teams gibt es die folgenden Probleme mit den Eingabehilfen, an deren Behebung wir in zukünftigen Versionen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="247b1-238">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="247b1-239">Abgang</span><span class="sxs-lookup"><span data-stu-id="247b1-239">Issue</span></span> | <span data-ttu-id="247b1-240">Problemumgehung oder Erklärung</span><span class="sxs-lookup"><span data-stu-id="247b1-240">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="247b1-241">Bei Zoomen auf 400 % auf dem Desktop werden einige der Aktionsschaltflächen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="247b1-241">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="247b1-242">Sie sollten eine Bildschirmlupe verwenden, bis wir diese Zoomstufe unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="247b1-242">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="247b1-243">Auf der Registerkarte **Arbeitsfreie Zeit** gibt das Voiceover eine Schaltfläche „Aktion“ an, wenn die Kopfzeile für das Raster für arbeitsfreie Zeit vorliest.</span><span class="sxs-lookup"><span data-stu-id="247b1-243">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="247b1-244">Die Kopfzeile und die Elemente im Raster sind nach Jahr gruppiert und können ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="247b1-244">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="247b1-245">Das Voiceover interpretiert dies als umsetzbares Element, obwohl dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="247b1-245">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="247b1-246">In der Registerkarte **Arbeitsfreie Zeit** gibt es eine zusätzliche Wischgeste, wenn Sie zum **Ursachencode** in einem neuen Antrag navigieren.</span><span class="sxs-lookup"><span data-stu-id="247b1-246">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="247b1-247">Es gibt kein verstecktes Steuerelement, zu dem die Wischnavigation gelangen möchte.</span><span class="sxs-lookup"><span data-stu-id="247b1-247">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="247b1-248">Wenn Sie in der Registerkarte **Arbeitsfreie Zeit** wischen, während der Kalender geöffnet ist, befinden Sie sich außerhalb des Steuerelements, anstatt in einem neuen Antrag oder beim Bearbeiten eines Antrags ganz oben.</span><span class="sxs-lookup"><span data-stu-id="247b1-248">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="247b1-249">Wenn Sie **Zu heute gehen** erreichen, betrachten Sie dies als Ende des Steuerelements und wischen Sie in die entgegengesetzte Richtung, um wieder nach oben zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="247b1-249">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="247b1-250">In der Registerkarte **Chat** springt der Fokus wieder nach oben, wenn Sie ein Datum eingeben, während Sie das Hilfsmittel oder die Tastaturnavigation verwenden.</span><span class="sxs-lookup"><span data-stu-id="247b1-250">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="247b1-251">Tippen Sie, bis Sie Ihren Eingabebereich wieder erreichen.</span><span class="sxs-lookup"><span data-stu-id="247b1-251">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="247b1-252">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="247b1-252">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="247b1-253">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="247b1-253">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="247b1-254">Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="247b1-254">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="247b1-255">Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="247b1-255">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="247b1-256">Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="247b1-256">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="247b1-257">Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso).</span><span class="sxs-lookup"><span data-stu-id="247b1-257">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="247b1-258">Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft.</span><span class="sxs-lookup"><span data-stu-id="247b1-258">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="247b1-259">Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt.</span><span class="sxs-lookup"><span data-stu-id="247b1-259">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="247b1-260">Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf.</span><span class="sxs-lookup"><span data-stu-id="247b1-260">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="247b1-261">Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="247b1-261">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="247b1-262">Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="247b1-262">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="247b1-263">Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="247b1-263">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="247b1-264">Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="247b1-264">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="247b1-265">Microsoft Teams, Azure Event Grid und Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="247b1-265">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="247b1-266">Bei Verwendung der Dynamics 365 Human Resources-App in Microsoft Teams fließen möglicherweise bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="247b1-266">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="247b1-267">Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="247b1-267">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="247b1-268">Diese Daten können bis zu 24 Stunden in Microsoft Azure Event Grid gespeichert werden und werden in den USA verarbeitet, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="247b1-268">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="247b1-269">Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="247b1-269">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="247b1-270">Während der Konversation mit dem Chat-Bot in der Human Resources-App wird der Konversationsinhalt möglicherweise in Azure Cosmos DB gespeichert und an Microsoft Teams übertragen.</span><span class="sxs-lookup"><span data-stu-id="247b1-270">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="247b1-271">Diese Daten können in Azure Cosmos DB bis zu 24 Stunden lang gespeichert und außerhalb der geografischen Region verarbeitet werden, in der der Human Resources-Service Ihres Mandanten bereitgestellt wird, werden während des Transports und in Ruhe verschlüsselt und von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="247b1-271">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="247b1-272">Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="247b1-272">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="247b1-273">Um den Zugriff auf die Human Resources-App in Microsoft Teams für Ihre Organisation oder Benutzer in Ihrer Organisation zu beschränken, finden Sie unter Informationen unter [Verwalten von App-Berechtigungsrichtlinien in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="247b1-273">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="247b1-274">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="247b1-274">See also</span></span>

[<span data-ttu-id="247b1-275">Microsoft Teams herunterladen und installieren</span><span class="sxs-lookup"><span data-stu-id="247b1-275">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="247b1-276">Microsoft Teams-Hilfecenter</span><span class="sxs-lookup"><span data-stu-id="247b1-276">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="247b1-277">Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="247b1-277">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]