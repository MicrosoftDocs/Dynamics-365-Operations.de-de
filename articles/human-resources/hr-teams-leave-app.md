---
title: Urlaubsanträge in Teams verwalten
description: In diesem Thema wird beschrieben, wie Sie arbeitsfreie Zeit in der Dynamics 365 Human Resources-App in Microsoft Teams beantragen.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766759"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="7c03e-103">Urlaubsanträge in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="7c03e-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7c03e-104">Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Sie schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="7c03e-105">Sie können mit einem Bot interagieren, um Informationen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="7c03e-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="7c03e-106">Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="7c03e-107">App installieren</span><span class="sxs-lookup"><span data-stu-id="7c03e-107">Install the app</span></span>

<span data-ttu-id="7c03e-108">Sie finden die Human Resources-App im Teams Store.</span><span class="sxs-lookup"><span data-stu-id="7c03e-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="7c03e-109">Wählen Sie in Microsoft Teams die drei Punkte aus.</span><span class="sxs-lookup"><span data-stu-id="7c03e-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Ellipsen](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="7c03e-111">Suchen Sie nach Dynamics 365 Human Resources, und wählen Sie dann die Kachel **Human Resources** aus.</span><span class="sxs-lookup"><span data-stu-id="7c03e-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Kachel „Human Resources“](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="7c03e-113">Wählen Sie die Schaltfläche **Hinzufügen** aus, um die App zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7c03e-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Installation](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="7c03e-115">Wenn Sie nicht automatisch von der App angemeldet werden, wählen Sie die Registerkarte **Einstellungen** aus, um sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="7c03e-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Einstellungen“](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="7c03e-117">Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="7c03e-118">Wenn Sie Zugriff auf mehrere Human Resources-Instanzen haben, können Sie auf der Registerkarte **Einstellungen** festlegen, zu welcher Umgebung Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7c03e-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="7c03e-119">Die App unterstützt derzeit die Sicherheitsrolle „Systemadministrator“ nicht und zeigt eine Fehlermeldung an, wenn Sie sich mit einem Systemadministratorkonto anmelden.</span><span class="sxs-lookup"><span data-stu-id="7c03e-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="7c03e-120">Wählen Sie auf der Registerkarte **Einstellungen** die Schaltfläche **Konten wechseln** aus, und melden Sie sich dann mit einem Benutzerkonto an, dem keine Systemadministratorrechte zugewiesen sind, um sich mit einem anderen Konto anzumelden.</span><span class="sxs-lookup"><span data-stu-id="7c03e-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="7c03e-121">Bot verwenden</span><span class="sxs-lookup"><span data-stu-id="7c03e-121">Use the bot</span></span>

<span data-ttu-id="7c03e-122">Nach der Installation der App wird eine Willkommensnachricht angezeigt, in der Sie über die Aktivitätstypen informiert werden, die der Bot in Ihrem Namen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="7c03e-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Willkommensnachricht für Bot](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="7c03e-124">Bei der ersten Interaktion mit dem Bot müssen Sie sich möglicherweise anmelden.</span><span class="sxs-lookup"><span data-stu-id="7c03e-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="7c03e-125">Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="7c03e-126">Sie können den Bot bitten, die folgenden Aktionen durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="7c03e-126">You can ask the bot to:</span></span>

- <span data-ttu-id="7c03e-127">Informationen zum Freizeitguthaben für jeden Urlaubstyp anzeigen, für den Sie sich angemeldet haben</span><span class="sxs-lookup"><span data-stu-id="7c03e-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Salden anzeigen](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="7c03e-129">Zusätzliche Details zu einem bestimmten Urlaubstyp anzeigen</span><span class="sxs-lookup"><span data-stu-id="7c03e-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Details anzeigen](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="7c03e-131">Urlaubsanforderung für Sie starten</span><span class="sxs-lookup"><span data-stu-id="7c03e-131">Start a leave request for you.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Urlaubsanforderung](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="7c03e-133">Nachdem Sie einen Urlaubsantrag gestellt haben, können Sie die Tage direkt auf der Karte anpassen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Anforderung bearbeiten](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="7c03e-135">Wenn Sie die Informationen eingegeben haben, wählen Sie **Absenden** aus, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="7c03e-136">Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources-App für Abwesenheiten in Teams – Anforderung senden](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="7c03e-138">Urlaub in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="7c03e-138">Manage your leave in Teams</span></span>

<span data-ttu-id="7c03e-139">Auf der Registerkarte **Arbeitsfreie Zeit** können Sie Folgendes anzeigen:</span><span class="sxs-lookup"><span data-stu-id="7c03e-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="7c03e-140">Saldoinformationen für jeden Urlaubstyp anzeigen, für den Sie registriert sind</span><span class="sxs-lookup"><span data-stu-id="7c03e-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="7c03e-141">Anstehende Urlaubsanforderungen</span><span class="sxs-lookup"><span data-stu-id="7c03e-141">Upcoming leave requests</span></span>

- <span data-ttu-id="7c03e-142">Anforderungen von arbeitsfreier Zeit</span><span class="sxs-lookup"><span data-stu-id="7c03e-142">Time-off requests</span></span>

- <span data-ttu-id="7c03e-143">Urlaubsanforderungen entwerfen</span><span class="sxs-lookup"><span data-stu-id="7c03e-143">Draft leave requests</span></span>

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="7c03e-145">Neue Anforderung erstellen</span><span class="sxs-lookup"><span data-stu-id="7c03e-145">Create a new request</span></span>

1. <span data-ttu-id="7c03e-146">Wählen Sie **Neue Anforderung** aus, um eine neue Urlaubsanforderung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Neue Anforderung](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="7c03e-148">Geben Sie den/die Tag(e) ein, den/die Sie sich frei nehmen möchten, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7c03e-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Arbeitsfreie Zeit hinzufügen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="7c03e-150">Geben Sie gegebenenfalls einen Ursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="7c03e-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="7c03e-151">Geben Sie auch Kommentare ein, und fügen Sie Anhänge hinzu.</span><span class="sxs-lookup"><span data-stu-id="7c03e-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="7c03e-152">Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="7c03e-153">Sie können auch **Als Entwurf speichern** eingeben, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="7c03e-154">Entwurfsanforderungen verwalten</span><span class="sxs-lookup"><span data-stu-id="7c03e-154">Manage draft requests</span></span>

1. <span data-ttu-id="7c03e-155">Wählen Sie die Registerkarte **Entwürfe** aus.</span><span class="sxs-lookup"><span data-stu-id="7c03e-155">Select the **Drafts** tab.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Entwürfe“](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="7c03e-157">Wählen Sie den Stift aus, um die Anforderung zu bearbeiten, oder wählen Sie den Papierkorb aus, um die Anforderung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="7c03e-158">Nehmen Sie die erforderlichen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="7c03e-158">Make any necessary changes.</span></span> <span data-ttu-id="7c03e-159">Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="7c03e-160">Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources-App für Abwesenheiten in Teams – „Entwurf bearbeiten“](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="7c03e-162">Teams-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7c03e-162">Teams notifications</span></span>

<span data-ttu-id="7c03e-163">Wenn Sie oder ein Mitarbeiter, für den Sie Genehmiger sind, einen Urlaubsantrag stellen, erhalten Sie eine Benachrichtigung in der Human Resources-App in Teams.</span><span class="sxs-lookup"><span data-stu-id="7c03e-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="7c03e-164">Sie können die Benachrichtigung auswählen, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-164">You can select the notification to view it.</span></span> <span data-ttu-id="7c03e-165">Benachrichtigungen werden auch im **Plaudern**-Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c03e-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="7c03e-166">Wenn Sie ein Genehmiger sind, können Sie in der Benachrichtigung **Genehmigen** oder **Verweigern** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="7c03e-167">Sie können auch eine optionale Nachricht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-167">You can also provide an optional message.</span></span>

![Urlaubsantragsbenachrichtigungen in der Human Resources-Teams-App](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="7c03e-169">Urlaubskalender Ihres Teams anzeigen</span><span class="sxs-lookup"><span data-stu-id="7c03e-169">View your team's leave calendar</span></span>

<span data-ttu-id="7c03e-170">Wenn Sie ein Manager mit direkten Berichten sind, können Sie die genehmigte und ausstehende arbeitsfreie Zeit Ihres Teams anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="7c03e-171">Wählen Sie in der Human Resources-App in Teams die Option aus **Arbeitsfreie Zeit** aus.</span><span class="sxs-lookup"><span data-stu-id="7c03e-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="7c03e-172">Wählen Sie **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="7c03e-172">Select **Team calendar**.</span></span>

   ![Kalender in der Human Resources-Teams-App anzeigen](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="7c03e-174">Der Kalender zeigt die genehmigte und ausstehende arbeitsfreie Zeit Ihrer direkten Berichte an.</span><span class="sxs-lookup"><span data-stu-id="7c03e-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Kalender für arbeitsfreie Zeit in der Human Resources-Teams-App](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="7c03e-176">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="7c03e-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="7c03e-177">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="7c03e-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="7c03e-178">Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="7c03e-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="7c03e-179">Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c03e-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="7c03e-180">Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="7c03e-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="7c03e-181">Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso).</span><span class="sxs-lookup"><span data-stu-id="7c03e-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="7c03e-182">Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft.</span><span class="sxs-lookup"><span data-stu-id="7c03e-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="7c03e-183">Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt.</span><span class="sxs-lookup"><span data-stu-id="7c03e-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="7c03e-184">Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf.</span><span class="sxs-lookup"><span data-stu-id="7c03e-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7c03e-185">Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c03e-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="7c03e-186">Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c03e-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="7c03e-187">Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="7c03e-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="7c03e-188">Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="7c03e-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="7c03e-189">Microsoft Azure Event Grid und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7c03e-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="7c03e-190">Bei Verwendung der Benachrichtigungsfunktion für die Dynamics 365 Human Resources-App in Teams fließen bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c03e-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="7c03e-191">Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7c03e-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="7c03e-192">Diese Daten können bis zu 24 Stunden gespeichert und in den USA verarbeitet werden, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c03e-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c03e-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c03e-193">See also</span></span>

[<span data-ttu-id="7c03e-194">Microsoft Teams herunterladen und installieren</span><span class="sxs-lookup"><span data-stu-id="7c03e-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="7c03e-195">Microsoft Teams-Hilfecenter</span><span class="sxs-lookup"><span data-stu-id="7c03e-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="7c03e-196">Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="7c03e-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
