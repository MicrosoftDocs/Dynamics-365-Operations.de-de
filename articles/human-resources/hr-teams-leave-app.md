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
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828943"
---
# <a name="manage-leave-requests-in-teams"></a>Urlaubsanträge in Teams verwalten

[!include [banner](includes/preview-feature.md)]

Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Sie schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen. Sie können mit einem Bot interagieren, um Informationen anzufordern und eine Urlaubsanfrage zu starten. Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen. Darüber hinaus können Sie Personen Informationen über Ihre bevorstehende arbeitsfreie Zeit in Teams und Chats außerhalb der Human Resources-App senden.

## <a name="install-the-app"></a>App installieren

Sie finden die Human Resources-App im Teams Store.

1. Wählen Sie in Microsoft Teams die drei Punkte aus.

   ![Human Resources-App für Abwesenheiten in Teams – Ellipsen](./media/hr-teams-leave-app-ellipses.png)
 
2. Suchen Sie nach Dynamics 365 Human Resources, und wählen Sie dann die Kachel **Human Resources** aus.

   ![Human Resources-App für Abwesenheiten in Teams – Kachel „Human Resources“](./media/hr-teams-leave-app-human-resources-tile.png)

3. Wählen Sie die Schaltfläche **Hinzufügen** aus, um die App zu installieren.

   ![Human Resources-App für Abwesenheiten in Teams – Installation](./media/hr-teams-leave-app-in-store.png)

Wenn Sie nicht automatisch von der App angemeldet werden, wählen Sie die Registerkarte **Einstellungen** aus, um sich anzumelden.

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Einstellungen“](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen. 

Wenn Sie Zugriff auf mehrere Human Resources-Instanzen haben, können Sie auf der Registerkarte **Einstellungen** festlegen, zu welcher Umgebung Sie eine Verbindung herstellen möchten.

> [!NOTE]
> Die App unterstützt jetzt die Sicherheitsrolle des Systemadministrators.
 
## <a name="use-the-bot"></a>Bot verwenden

Nach der Installation der App wird eine Willkommensnachricht angezeigt, in der Sie über die Aktivitätstypen informiert werden, die der Bot in Ihrem Namen ausführen kann.

![Human Resources-App für Abwesenheiten in Teams – Willkommensnachricht für Bot](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Bei der ersten Interaktion mit dem Bot müssen Sie sich möglicherweise anmelden. Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.

Sie können den Bot bitten, die folgenden Aktionen durchzuführen:

- Informationen zum Freizeitguthaben für jeden Urlaubstyp anzeigen, für den Sie sich angemeldet haben

   ![Human Resources-App für Abwesenheiten in Teams – Salden anzeigen](./media/hr-teams-leave-app-bot-balances.png)
 
- Zusätzliche Details zu einem bestimmten Urlaubstyp anzeigen

   ![Human Resources-App für Abwesenheiten in Teams – Details anzeigen](./media/hr-teams-leave-app-bot-details.png)

- Urlaubsanforderung für Sie starten

   ![Human Resources-App für Abwesenheiten in Teams – Urlaubsanforderung](./media/hr-teams-leave-app-bot-request.png)
 
Nachdem Sie einen Urlaubsantrag gestellt haben, können Sie die Tage direkt auf der Karte anpassen.

![Human Resources-App für Abwesenheiten in Teams – Anforderung bearbeiten](./media/hr-teams-leave-app-bot-edit.png)
 
Wenn Sie die Informationen eingegeben haben, wählen Sie **Absenden** aus, um sie zur Genehmigung einzureichen. Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.

![Human Resources-App für Abwesenheiten in Teams – Anforderung senden](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Urlaub in Teams verwalten

Auf der Registerkarte **Arbeitsfreie Zeit** können Sie Folgendes anzeigen:

- Saldoinformationen für jeden Urlaubstyp anzeigen, für den Sie registriert sind

- Anstehende Urlaubsanforderungen

- Anforderungen von arbeitsfreier Zeit

- Urlaubsanforderungen entwerfen

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Neue Anforderung erstellen

1. Wählen Sie **Neue Anforderung** aus, um eine neue Urlaubsanforderung zu erstellen.

   ![Human Resources-App für Abwesenheiten in Teams – Neue Anforderung](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Geben Sie den/die Tag(e) ein, den/die Sie sich frei nehmen möchten, und wählen Sie dann **Hinzufügen** aus.

   ![Human Resources-App für Abwesenheiten in Teams – Arbeitsfreie Zeit hinzufügen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Geben Sie gegebenenfalls einen Ursachencode ein. Geben Sie auch Kommentare ein, und fügen Sie Anhänge hinzu.

4. Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen. Sie können auch **Als Entwurf speichern** eingeben, um später darauf zurückzukommen.

### <a name="manage-draft-requests"></a>Entwurfsanforderungen verwalten

1. Wählen Sie die Registerkarte **Entwürfe** aus.

   ![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Entwürfe“](./media/hr-teams-leave-app-drafts-tab.png)

2. Wählen Sie den Stift aus, um die Anforderung zu bearbeiten, oder wählen Sie den Papierkorb aus, um die Anforderung zu löschen.

3. Nehmen Sie die erforderlichen Änderungen vor. Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen. Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.

   ![Human Resources-App für Abwesenheiten in Teams – „Entwurf bearbeiten“](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>Antworten auf Teams-Benachrichtigungen

Wenn Sie oder ein Mitarbeiter, für den Sie Genehmiger sind, einen Urlaubsantrag stellen, erhalten Sie eine Benachrichtigung in der Human Resources-App in Teams. Sie können die Benachrichtigung auswählen, um sie anzuzeigen. Benachrichtigungen werden auch im **Plaudern**-Bereich angezeigt.

Wenn Sie ein Genehmiger sind, können Sie in der Benachrichtigung **Genehmigen** oder **Verweigern** auswählen. Sie können auch eine optionale Nachricht bereitstellen.

![Urlaubsantragsbenachrichtigungen in der Human Resources-Teams-App](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Informationen zu bevorstehender arbeitsfreier Zeit an Ihre Kollegen senden

Nachdem Sie die Human Resources-App für Teams installiert haben, können Sie Ihren Kollegen in Teams oder Chats problemlos Informationen zu Ihrer arbeitsfreien Zeit senden.

1. Wählen Sie in einem Team oder Chat in Teams die Schaltfläche Human Resources unter dem Chatfenster.

   ![Schaltfläche „Human Resources“ unter dem Chatfenster](./media/hr-teams-leave-app-chat-button.png)

2. Wählen Sie die Urlaubsanfrage aus, die Sie teilen möchten. Wenn Sie einen Entwurf für einen Urlaubsantrag freigeben möchten, wählen Sie zuerst **Entwürfe**.

   ![Einen bevorstehenden Urlaubsantrag zum Teilen auswählen](./media/hr-teams-leave-app-chat-search.png)

Ihre Urlaubsanfrage wird im Chat angezeigt.

![Urlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-card.png)

Wenn Sie einen Entwurfsantrag freigegeben haben, wird dieser als Entwurf angezeigt:

![Entwurfsurlaubsantragskarte in Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>Urlaubskalender Ihres Teams anzeigen

Wenn Sie ein Manager mit direkten Berichten sind, können Sie die genehmigte und ausstehende arbeitsfreie Zeit Ihres Teams anzeigen.

1. Wählen Sie in der Human Resources-App in Teams die Option aus **Arbeitsfreie Zeit** aus.

2. Wählen Sie **Teamkalender**.

   ![Kalender in der Human Resources-Teams-App anzeigen](./media/hr-teams-leave-app-view-calendar.png)

Der Kalender zeigt die genehmigte und ausstehende arbeitsfreie Zeit Ihrer direkten Berichte an.

![Kalender für arbeitsfreie Zeit in der Human Resources-Teams-App](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a>Datenschutzhinweis

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen. Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet. Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/). Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso). Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft. 

Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt. Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf. Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden. 

Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet. Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid und Azure Cosmos DB

Bei Verwendung der Dynamics 365 Human Resources-App in Microsoft Teams fließen möglicherweise bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.

Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams. Diese Daten können bis zu 24 Stunden in Microsoft Azure Event Grid gespeichert werden und werden in den USA verarbeitet, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet. Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Während der Konversation mit dem Chat-Bot in der Human Resources-App wird der Konversationsinhalt möglicherweise in Azure Cosmos DB gespeichert und an Microsoft Teams übertragen. Diese Daten können in Azure Cosmos DB bis zu 24 Stunden lang gespeichert und außerhalb der geografischen Region verarbeitet werden, in der der Human Resources-Service Ihres Mandanten bereitgestellt wird, werden während des Transports und in Ruhe verschlüsselt und von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet. Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Um den Zugriff auf die Human Resources-App in Microsoft Teams für Ihre Organisation oder Benutzer in Ihrer Organisation zu beschränken, finden Sie unter Informationen unter [Verwalten von App-Berechtigungsrichtlinien in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Siehe auch

[Microsoft Teams herunterladen und installieren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-Hilfecenter](https://support.office.com/teams)</br>
[Human Resources-App in Teams](hr-admin-teams-leave-app.md)
