---
title: Human Resources-App in Teams
description: Dieses Thema enthält Informationen zur Microsoft Dynamics 365 Human Resources-App in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e714be06984f399235f0799ef077a92deae64d9e
ms.sourcegitcommit: b0aa724a18ab1fbb5a62925f048c54b2c676ebf4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "4476076"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="c4208-103">Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="c4208-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c4208-104">Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Mitarbeiter schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4208-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="c4208-105">Mitarbeiter können mit einem Bot interagieren, um Informationen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c4208-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="c4208-106">Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen.</span><span class="sxs-lookup"><span data-stu-id="c4208-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="c4208-107">Darüber hinaus können sie Personen Informationen über bevorstehende arbeitsfreie Zeit in Teams und Chats außerhalb der Human Resources-App senden.</span><span class="sxs-lookup"><span data-stu-id="c4208-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Bot für Abwesenheiten der Human Resources-App in Teams](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“](./media/hr-teams-leave-app-timeoff-tab.png)

![Urlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="c4208-111">Installieren und einrichten</span><span class="sxs-lookup"><span data-stu-id="c4208-111">Install and setup</span></span>

<span data-ttu-id="c4208-112">Sie finden die Human Resources-App im Teams Store.</span><span class="sxs-lookup"><span data-stu-id="c4208-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="c4208-113">Weitere Informationen zum Installieren der Teams-App finden Sie unter [Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="c4208-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="c4208-114">Informationen zum Verwalten von App-Berechtigungen in Teams finden Sie unter [App-Berechtigungsrichtlinien in Microsoft Teams verwalten](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="c4208-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="c4208-115">Aktivieren von Benachrichtigungen für die Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="c4208-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="c4208-116">Wenn Benutzer Benachrichtigungen über Urlaubsanträge in der Teams-App erhalten sollen, müssen Sie Benachrichtigungen in Human Resources aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c4208-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="c4208-117">Nur Benutzer, die bei Teams angemeldet sind und die App Human Resources Teams verwenden, erhalten Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c4208-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="c4208-118">Wählen Sie in Human Resources **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c4208-119">Wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-119">Select **Links**.</span></span>

3. <span data-ttu-id="c4208-120">Wählen Sie unter **Einrichtung** **Systemparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="c4208-121">Legen Sie auf der **Allgemeines**-Registerkarte **Benachrichtigungen für Teams-App aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="c4208-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivieren von Teams-App-Benachrichtigungen in Systemparametern](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="c4208-123">Um Teams-Benachrichtigungen für alle Benutzer zu aktivieren, wählen Sie in der Eingabeaufforderung **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivieren von Teams-Benachrichtigungen für alle Benutzer](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="c4208-125">Ein- und Ausschalten von Teams-Benachrichtigungen für einzelne Benutzer</span><span class="sxs-lookup"><span data-stu-id="c4208-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="c4208-126">Nachdem Sie Benachrichtigungen für die Human Resources Teams-App aktiviert haben, können Sie Benachrichtigungen für einzelne Benutzer aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c4208-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="c4208-127">Wählen Sie in Human Resources **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c4208-128">Wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-128">Select **Links**.</span></span>

3. <span data-ttu-id="c4208-129">Wählen Sie unter **Benutzer** **Benutzeroptionen** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="c4208-130">Wählen Sie die Registerkarte **Workflow** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="c4208-131">Legen Sie **Benachrichtigungen für die Teams-App aktivieren** auf **Ja** fest, um Benachrichtigungen für den Benutzer zu aktivieren oder auf **Nein**, um Benachrichtigungen für den Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c4208-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivieren von Teams-App-Benachrichtigungen auf der Registerkarte „Benutzeroptionen-Workflow“](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="c4208-133">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="c4208-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="c4208-134">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="c4208-134">Known issues</span></span>

| <span data-ttu-id="c4208-135">Abgang</span><span class="sxs-lookup"><span data-stu-id="c4208-135">Issue</span></span> | <span data-ttu-id="c4208-136">Status</span><span class="sxs-lookup"><span data-stu-id="c4208-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="c4208-137">Der Saldo ist falsch, wenn arbeitsfreie Zeit für ein zukünftiges Datum eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="c4208-137">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="c4208-138">Es ist noch keine Planungsfunktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4208-138">Forecasting isn't yet available.</span></span> <span data-ttu-id="c4208-139">Der Saldo wird für das aktuelle Datum angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4208-139">The balance displays for the current date.</span></span> |
| <span data-ttu-id="c4208-140">Eine **Wird überprüft**-Anforderung kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="c4208-140">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="c4208-141">Diese Funktion wird derzeit nicht unterstützt und wird in einer zukünftigen Version hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c4208-141">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="c4208-142">Die Saldoinformationen werden ab heute berechnet.</span><span class="sxs-lookup"><span data-stu-id="c4208-142">Balance information is calculated as of today.</span></span> | <span data-ttu-id="c4208-143">Das System zeigt derzeit keine Salden ab dem Abgrenzungszeitraum an, auch wenn dies in den Urlaub- und Abwesenheitsparameter konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="c4208-143">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="c4208-144">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="c4208-144">Troubleshooting</span></span>

<span data-ttu-id="c4208-145">Wenn ein Benutzer Probleme beim Anmelden oder Verwenden der Human Resources Teams-App hat, befolgen Sie diese Anweisungen zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="c4208-145">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="c4208-146">Wenn Sie nach der Problembehandlung immer noch Probleme haben, wenden Sie sich an den Support.</span><span class="sxs-lookup"><span data-stu-id="c4208-146">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="c4208-147">Weitere Informationen erhalten Sie über den [Support](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="c4208-147">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="c4208-148">Sie können sich nicht in Teams bei der Human Resources-App anmelden</span><span class="sxs-lookup"><span data-stu-id="c4208-148">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="c4208-149">Wenn ein Benutzer Sie kontaktiert, weil er sich nicht bei der App anmelden kann, überprüfen Sie, ob dem Benutzer ein Mitarbeiterdatensatz in der Personalverwaltung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c4208-149">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="c4208-150">Fehler beim Genehmigen von Urlaubsanträgen in der Human Resources-App in Teams</span><span class="sxs-lookup"><span data-stu-id="c4208-150">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="c4208-151">Wenn ein Benutzer beim Versuch, Urlaubsanforderungen in der Team-App zu genehmigen, eine Fehlermeldung erhält, führen Sie die folgenden Schritte zur Problembehandlung aus:</span><span class="sxs-lookup"><span data-stu-id="c4208-151">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="c4208-152">Stellen Sie sicher, dass das Teamkonto dasselbe ist, das sie für den Zugriff auf die Personalverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4208-152">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="c4208-153">Stellen Sie sicher, dass sie ein gültiger Genehmiger für die Anforderung sind, indem Sie die Workflow-Einstellungen auf Urlaubsgenehmigung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c4208-153">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="c4208-154">Weitere Informationen zu Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c4208-154">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c4208-155">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="c4208-155">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="c4208-156">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="c4208-156">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="c4208-157">Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="c4208-157">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="c4208-158">Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="c4208-158">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="c4208-159">Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="c4208-159">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="c4208-160">Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso).</span><span class="sxs-lookup"><span data-stu-id="c4208-160">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="c4208-161">Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft.</span><span class="sxs-lookup"><span data-stu-id="c4208-161">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="c4208-162">Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt.</span><span class="sxs-lookup"><span data-stu-id="c4208-162">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="c4208-163">Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf.</span><span class="sxs-lookup"><span data-stu-id="c4208-163">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c4208-164">Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4208-164">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="c4208-165">Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4208-165">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="c4208-166">Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="c4208-166">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="c4208-167">Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c4208-167">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="c4208-168">Microsoft Teams, Azure Event Grid und Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c4208-168">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="c4208-169">Bei Verwendung der Dynamics 365 Human Resources-App in Microsoft Teams fließen möglicherweise bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4208-169">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="c4208-170">Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c4208-170">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="c4208-171">Diese Daten können bis zu 24 Stunden in Microsoft Azure Event Grid gespeichert werden und werden in den USA verarbeitet, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4208-171">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="c4208-172">Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="c4208-172">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="c4208-173">Während der Konversation mit dem Chat-Bot in der Human Resources-App wird der Konversationsinhalt möglicherweise in Azure Cosmos DB gespeichert und an Microsoft Teams übertragen.</span><span class="sxs-lookup"><span data-stu-id="c4208-173">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="c4208-174">Diese Daten können in Azure Cosmos DB bis zu 24 Stunden lang gespeichert und außerhalb der geografischen Region verarbeitet werden, in der der Human Resources-Service Ihres Mandanten bereitgestellt wird, werden während des Transports und in Ruhe verschlüsselt und von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4208-174">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="c4208-175">Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="c4208-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="c4208-176">Um den Zugriff auf die Human Resources-App in Microsoft Teams für Ihre Organisation oder Benutzer in Ihrer Organisation zu beschränken, finden Sie unter Informationen unter [Verwalten von App-Berechtigungsrichtlinien in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="c4208-176">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="c4208-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4208-177">See also</span></span> 

[<span data-ttu-id="c4208-178">Microsoft Teams herunterladen und installieren</span><span class="sxs-lookup"><span data-stu-id="c4208-178">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="c4208-179">Microsoft Teams-Hilfecenter</span><span class="sxs-lookup"><span data-stu-id="c4208-179">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="c4208-180">Urlaubsanträge in Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="c4208-180">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

