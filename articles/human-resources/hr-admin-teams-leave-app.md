---
title: Human Resources-App in Teams
description: Dieser Artikel enthält Informationen zur Microsoft Dynamics 365 Human Resources-App in Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d29802bdf3411c93f20d710e1f26e541e5022d57
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812185"
---
# <a name="human-resources-app-in-teams"></a>Human Resources-App in Teams


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Mitarbeiter schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen. Mitarbeiter können mit einem Bot interagieren, um Informationen anzufordern. Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen. Darüber hinaus können sie Personen Informationen über bevorstehende arbeitsfreie Zeit in Teams und Chats außerhalb der Human Resources-App senden.

![Bot für Abwesenheiten der Human Resources-App in Teams.](./media/hr-teams-leave-app-bot.png)

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“.](./media/hr-teams-leave-app-timeoff-tab.png)

![Urlaubsantragskarte in Human Resources.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installieren und einrichten

Sie finden die App Dynamics 365 Human Resources im Teams-Store. Weitere Informationen zum Installieren der Teams-App finden Sie unter [Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md).

Informationen zum Verwalten von App-Berechtigungen in Teams finden Sie unter [App-Berechtigungsrichtlinien in Microsoft Teams verwalten](/MicrosoftTeams/teams-app-permission-policies).

Wenn Sie möchten, dass Ihre Benutzer den Urlaubs- und Abwesenheitskalender in der App sehen können, müssen Sie die Funktion **Abwesenheits- und Urlaubskalender in Teams** in der Funktionsverwaltung aktivieren. Weitere Informationen zum Aktivieren von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

## <a name="update-app"></a>App aktualisieren
>[!NOTE]
> Ab dem 20. Dezember 2021 werden die im Microsoft Mandant gehosteten Bot-Dienste der Human Resources App außer Betrieb genommen. Es gibt keine Auswirkungen für eine aktuelle Erweiterung (Version 1.1.5), die zur Installation verfügbar ist. Die größte Auswirkung wird die veraltete Erweiterung (Version 1.1.4) haben. Der Chatbot wird in dieser Version nicht mehr funktionieren. Die Registerkarte **Time-off** funktioniert weiterhin in beiden Erweiterungen.

Bei Version 1.1.4 reagiert der Chatbot nicht mehr auf Nachrichten. Zum Beispiel **Anmelden**, **Salden anzeigen** und **Abwesenheit sehen**. Die App muss manuell auf die neueste Version aktualisiert werden. Weitere Informationen finden Sie unter [Aktualisierung von Apps in Microsoft Teams](/MicrosoftTeams/apps-update-experience).

Um auf die Version 1.1.5 zu aktualisieren, führen Sie diese Schritte aus:
1. Gehen Sie in Microsoft Teams zu **Apps**.
2. Suchen Sie die App **Human Resources**.
3. Wählen Sie **Upgrade**.

Sie können die Version der App Human Resources entweder auf der Registerkarte **Über** oder im Abschnitt **Persönliche App** überprüfen. 

![Registerkarte Human Resources **Über**.](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Aktivieren von Benachrichtigungen für die Human Resources-App in Teams

Wenn Sie möchten, dass Benutzer in der Teams App Benachrichtigungen über Abwesenheitsanträge erhalten, müssen Sie in Dynamics 365 Human Resources Benachrichtigungen aktivieren.

>[!NOTE]
>Nur Benutzer, die in Teams angemeldet sind und die Dynamics 365 Human Resources Teams App verwenden, erhalten Benachrichtigungen.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie **Links** aus.

3. Wählen Sie unter **Einrichtung** **Systemparameter** aus.

4. Legen Sie auf der **Allgemeines**-Registerkarte **Benachrichtigungen für Teams-App aktivieren** auf **Ja** fest.

   ![Aktivieren von Teams-App-Benachrichtigungen in Systemparametern.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Um Teams-Benachrichtigungen für alle Benutzer zu aktivieren, wählen Sie in der Eingabeaufforderung **Ja** aus.

   ![Aktivieren von Teams-Benachrichtigungen für alle Benutzer.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Ein- und Ausschalten von Teams-Benachrichtigungen für einzelne Benutzer

Nachdem Sie die Benachrichtigungen für die Dynamics 365 Human Resources Teams App aktiviert haben, können Sie die Benachrichtigungen für einzelne Benutzer ein- oder ausschalten.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie **Links** aus.

3. Wählen Sie unter **Benutzer** **Benutzeroptionen** aus.

4. Wählen Sie die Registerkarte **Workflow** aus.

5. Legen Sie **Benachrichtigungen für die Teams-App aktivieren** auf **Ja** fest, um Benachrichtigungen für den Benutzer zu aktivieren oder auf **Nein**, um Benachrichtigungen für den Benutzer zu deaktivieren.

   ![Aktivieren von Teams-App-Benachrichtigungen auf der Registerkarte „Benutzeroptionen-Workflow“.](./media/hr-admin-teams-leave-app-notifications.png)

6. Wählen Sie **Speichern** aus.

## <a name="supported-languages"></a>Unterstützte Sprachen

Die Dynamics 365 Human Resources App in Teams unterstützt die folgenden Sprachen:

| Gebietsschema-ID | Sprache |
| --- | --- |
| de-DE | Deutsch (Deutschland) |
| es-ES | Spanisch (Spanien) |
| es-MX | Spanisch (Mexiko) |
| fr-CA | Französisch (Kanada) |
| fr-FR | Französisch (Frankreich) |
| it-IT | Italienisch (Italien) |
| nl-NL | Niederländisch (Niederlande) |
| pt-BR | Portugiesisch (Brasilien) |
| tr-TR | Türkisch (Türkei) |
| zh-CN | Chinesisch (vereinfacht) |

## <a name="notes"></a>Notizen

Die folgenden Artikel sind für zukünftige Versionen vorgesehen:

| Arbeitsaufgabe | Status |
| --- | --- |
| Der Saldo ist falsch, wenn arbeitsfreie Zeit für ein zukünftiges Datum eingereicht wird. | Es ist noch keine Planungsfunktion verfügbar. Der Saldo wird für das aktuelle Datum angezeigt. |
| Eine **Wird überprüft**-Anforderung kann nicht abgebrochen werden. | Diese Funktion wird derzeit nicht unterstützt und wird in einer zukünftigen Version hinzugefügt. |
| Die Saldoinformationen werden ab heute berechnet. | Das System zeigt derzeit keine Salden ab dem Abgrenzungszeitraum an, auch wenn dies auf der Seite **Urlaub- und Abwesenheitsparameter** konfiguriert ist. |

## <a name="troubleshooting"></a>Problembehandlung

Wenn ein Benutzer Probleme beim Anmelden oder Verwenden der Human Resources Teams-App hat, befolgen Sie diese Anweisungen zur Problembehandlung. Wenn Sie nach der Problembehandlung immer noch Probleme haben, wenden Sie sich an den Support. Weitere Informationen erhalten Sie über den [Support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Stellen Sie sicher, dass die Human Resources-Anwendung in Teams auf dem neuesten Stand ist
Wenn Probleme mit der Human Resources-App in Teams auftreten, müssen Sie bestätigen, dass Sie die neueste Version ausführen. Die unterstützte Mindestversion ist 1.1.5. Anweisungen zum Aktualisieren einer Teams-Anwendung finden Sie unter [Teams-Dokumentation](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Sie können sich nicht in Teams bei der Human Resources-App anmelden

Wenn ein Benutzer Sie kontaktiert, weil er sich nicht bei der App anmelden kann, überprüfen Sie, ob er einen zugehörigen Mitarbeiterdatensatz in Human Resources hat.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Fehler beim Genehmigen von Urlaubsanträgen in der Human Resources-App in Teams

Wenn ein Benutzer einen Fehler erhält, während er versucht, Abwesenheitsanträge in der Teams App zu genehmigen, versuchen Sie die folgenden Schritte zur Fehlerbehebung:

1. Stellen Sie sicher, dass das Teamkonto dasselbe ist, das sie für den Zugriff auf die Personalverwaltung verwenden.

2. Stellen Sie sicher, dass sie ein gültiger Genehmiger für die Anforderung sind, indem Sie die Workflow-Einstellungen auf Urlaubsgenehmigung überprüfen. Weitere Informationen zu Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Genehmiger von Abwesenheiten erhalten keine Teams-Chat-Nachrichten, um Abwesenheitsanträge zu genehmigen

1. Stellen Sie sicher, dass Benachrichtigungen für die Umgebung und den Benutzer aktiviert sind. Weitere Informationen finden Sie unter [Benachrichtigungen für die Human Resources App in Teams aktivieren](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) und [Benachrichtigungen von Teams für einzelne Benutzer ein- oder ausschalten](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Stellen Sie sicher, dass die Benutzer auf der Registerkarte **Chats** mit denselben Anmeldeinformationen angemeldet sind, die sie für die Genehmigung von Urlaubsanträgen verwenden. Verwenden Sie die Nachrichten „Abmelden“ und dann „Anmelden“, um sich mit den richtigen Anmeldeinformationen anzumelden.

3. Wenn das Problem weiterhin besteht, überprüfen Sie als Systemadministrator den Status des Batchauftrags für das **Geschäftsereignissesystem**. Wenn es sich in einer **Warte-** oder **Ausführungsphase** befindet, schauen Sie in ein paar Minuten wieder nach. Wenn der Status unverändert bleibt, protokollieren Sie ein Support-Ticket, sodass unser Team helfen kann, das Problem zu beheben.

## <a name="privacy-notice"></a>Datenschutzhinweis

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen. Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet. Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/). Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso). Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft.

Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt. Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf. Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden. 

Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet. Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid und Azure Cosmos DB

Bei Verwendung der Dynamics 365 Human Resources-App in Microsoft Teams fließen möglicherweise bestimmte Kundendaten außerhalb der geografischen Region, in welcher der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.

Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams. Diese Daten können bis zu 24 Stunden in Microsoft Azure Event Grid gespeichert werden und werden in den USA verarbeitet, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet. Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Während der Konversation mit dem Chat-Bot in der Human Resources-App wird der Konversationsinhalt möglicherweise in Azure Cosmos DB gespeichert und an Microsoft Teams übertragen. Diese Daten können in Azure Cosmos DB bis zu 24 Stunden lang gespeichert und außerhalb der geografischen Region verarbeitet werden, in der der Human Resources-Service Ihres Mandanten bereitgestellt wird, werden während des Transports und in Ruhe verschlüsselt und von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet. Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Um den Zugriff auf die Human Resources-App in Microsoft Teams für Ihre Organisation oder Benutzer in Ihrer Organisation zu beschränken, finden Sie unter Informationen unter [Verwalten von App-Berechtigungsrichtlinien in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Siehe auch 

[Microsoft Teams herunterladen und installieren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-Hilfecenter](https://support.office.com/teams)</br>
[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
