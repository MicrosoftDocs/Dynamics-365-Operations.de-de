---
title: Urlaubsanträge in Teams verwalten
description: In diesem Thema wird beschrieben, wie Sie arbeitsfreie Zeit in der Dynamics 365 Human Resources-App in Microsoft Teams beantragen.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097258"
---
# <a name="manage-leave-requests-in-teams"></a>Urlaubsanträge in Teams verwalten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Mit der Dynamics 365 Human Resources-App in Microsoft Teams können Sie schnell eine Auszeit beantragen und Ihre Informationen zum Zeitsaldo direkt in Microsoft Teams einsehen. Sie können mit einem Bot interagieren, um Informationen anzufordern und eine Urlaubsanfrage zu starten. Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen. Sie können auch in Teams und Chats außerhalb der Human Resources App Informationen über Ihre bevorstehende Auszeit an andere Personen senden.

## <a name="install-the-app"></a>App installieren

Sie finden die App Dynamics 365 Human Resources im Teams-Store.

1. Im Microsoft Teams navigieren Sie zur Liste der Apps.
 
2. Suchen Sie nach Dynamics 365 Human Resources, und wählen Sie dann die Kachel **Human Resources** aus.

3. Wählen Sie die Schaltfläche **Hinzufügen** aus, um die App zu installieren.

Wenn Sie nicht automatisch von der App angemeldet werden, wählen Sie die Registerkarte **Einstellungen** aus, um sich anzumelden.

> [!NOTE]
> Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen. 

Wenn Sie Zugriff auf mehrere Human Resources-Instanzen haben, können Sie auf der Registerkarte **Einstellungen** festlegen, zu welcher Umgebung Sie eine Verbindung herstellen möchten.

> [!NOTE]
> Die App unterstützt jetzt die Sicherheitsrolle des Systemadministrators.
 
## <a name="use-the-bot"></a>Bot verwenden

Nach der Installation der App wird eine Willkommensnachricht angezeigt, in der Sie über die Aktivitätstypen informiert werden, die der Bot in Ihrem Namen ausführen kann.

> [!NOTE]
> Bei der ersten Interaktion mit dem Bot müssen Sie sich möglicherweise anmelden. Wenn kein Anmeldedialogfeld angezeigt wird, überprüfen Sie die Einstellungen Ihres Browsers, um Popupfenster zuzulassen.

Sie können den Bot bitten, die folgenden Aktionen durchzuführen:

- Zeigen Sie Ihre aktuellen Urlaubsguthaben an. Senden Sie beispielsweise eine Nachricht mit dem Titel Urlaubssalden anzeigen.

- Urlaubsanforderung für Sie starten Senden Sie beispielsweise eine Nachricht mit der Aufschrift Nehmen Sie sich frei oder Ich möchte nächsten Donnerstag und Freitag Urlaub machen, um genauer zu sagen, ob Sie Urlaub für den Urlaubstyp beantragen möchten. 

  ![Starten Sie einen Urlaubsantrag im Teams-Chat](./media/hr-teams-leave-app-initiate.png)

- Der Chat-Bot wird einen Urlaubsantrag für Sie ausfüllen. Wählen Sie **Abwesenheitsantrag** und bearbeiten Sie die Details für Ihren Antrag.

   Wenn Sie Urlaubsanträge für mehrere Urlaubstypen zum selben Datum einreichen möchten, wählen Sie die Option **Tag teilen mit** aus dem Menü **Mehr Optionen**. 

   Wenn Sie einen halbtägigen Urlaub auswählen, während die Urlaubsantragseinheit in Tagen angegeben ist, können Sie angeben, ob Sie eine Freistellung für den ersten halben Tag oder den zweiten halben Tag beantragen möchten, indem Sie die Option **Halbtagesdefinition** aus dem Menü **Mehr Optionen** auswählen.
   
   ![Halbtagesdefinitionen](./media/HalfDayDefinitions.png)

- Wenn Sie mit der Bearbeitung der Details Ihres Urlaubsantrags fertig sind, wählen Sie **Senden**, um ihn zur Genehmigung zu senden.

  ![Urlaubsantrag senden](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Urlaub in Teams verwalten

Auf der Registerkarte **Arbeitsfreie Zeit** können Sie Folgendes anzeigen: 

- Saldoinformationen für jeden Urlaubstyp anzeigen, für den Sie registriert sind

- Anstehende Urlaubsanforderungen

- Anforderungen von arbeitsfreier Zeit

- Urlaubsanforderungen entwerfen
 
### <a name="create-a-new-request"></a>Neue Anforderung erstellen

1. Wählen Sie **Neue Anforderung** aus, um eine neue Urlaubsanforderung zu erstellen.

2. Geben Sie den/die Tag(e) ein, den/die Sie sich frei nehmen möchten, und wählen Sie dann **Hinzufügen** aus.

   ![Human Resources-App für Abwesenheiten in Teams – Arbeitsfreie Zeit hinzufügen](./media/TimeOffHours.png)

3. Geben Sie gegebenenfalls einen Ursachencode ein. Geben Sie auch Kommentare ein, und fügen Sie Anhänge hinzu.

4. Wenn Sie Urlaubsanträge für mehrere Urlaubstypen zum selben Datum einreichen möchten, wählen Sie die Option **Tag teilen mit** aus dem Menü **Mehr Optionen** aus.

5. Wählen Sie die Option **Halbtagesdefinition**, um anzugeben, ob Sie den ersten halben Tag oder den zweiten halben Tag frei beantragen möchten. Diese Option ist verfügbar, wenn die Urlaubsantragseinheit in Tagen angegeben ist und der angeforderte Betrag 0,5 Tage beträgt.

6. Wenn Sie die Informationen eingegeben haben, wählen Sie **Absenden**, um sie zur Genehmigung einzureichen. Sie können auch **Als Entwurf speichern** eingeben, um später darauf zurückzukommen.

### <a name="manage-draft-requests"></a>Entwurfsanforderungen verwalten

1. Wählen Sie die Registerkarte **Entwürfe** aus.

2. Wählen Sie den Stift aus, um die Anforderung zu bearbeiten, oder wählen Sie den Papierkorb aus, um die Anforderung zu löschen.

3. Nehmen Sie die erforderlichen Änderungen vor. Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen. Sie können auch **Als Entwurf speichern** auswählen, um später darauf zurückzukommen.
   
### <a name="respond-to-teams-notifications"></a>Antworten auf Teams-Benachrichtigungen

Wenn Sie oder ein Mitarbeiter, für den Sie Genehmiger sind, einen Urlaubsantrag stellen, erhalten Sie eine Benachrichtigung in der Human Resources-App in Teams. Sie können die Benachrichtigung auswählen, um sie anzuzeigen. Benachrichtigungen werden auch im **Plaudern**-Bereich angezeigt.

Wenn Sie ein Genehmiger sind, können Sie in der Benachrichtigung **Genehmigen** oder **Verweigern** auswählen. Sie können auch eine optionale Nachricht bereitstellen.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Informationen zu bevorstehender arbeitsfreier Zeit an Ihre Kollegen senden

Nachdem Sie die Human Resources-App für Teams installiert haben, können Sie Ihren Kollegen in Teams oder Chats problemlos Informationen zu Ihrer arbeitsfreien Zeit senden.

1. Wählen Sie in einem Team oder Chat in Teams die Schaltfläche Human Resources unter dem Chatfenster.

   ![Schaltfläche „Human Resources“ unter dem Chatfenster](./media/hr-teams-leave-app-chat-button.png)

2. Wählen Sie die Urlaubsanfrage aus, die Sie teilen möchten. Wenn Sie einen Entwurf für einen Urlaubsantrag freigeben möchten, wählen Sie zuerst **Entwürfe**.

Ihre Urlaubsanfrage wird im Chat angezeigt.

Wenn Sie einen Entwurfsantrag freigegeben haben, wird dieser als Entwurf angezeigt.

## <a name="view-your-teams-leave-calendar"></a>Urlaubskalender Ihres Teams anzeigen

Wenn Sie ein Manager mit direkten Berichten sind, können Sie die genehmigte und ausstehende arbeitsfreie Zeit Ihres Teams anzeigen.

1. Wählen Sie in der Human Resources-App in Teams die Option aus **Arbeitsfreie Zeit** aus.

2. Wählen Sie **Teamkalender**. Der Kalender zeigt die genehmigte und ausstehende arbeitsfreie Zeit Ihrer direkten Berichte an.

   > [!NOTE]
   > Wenn Sie den Team-Kalender nicht sehen können, bitten Sie Ihren Admin, ihn zu aktivieren. Weitere Informationen finden Sie unter [Installation und Einrichten](hr-admin-teams-leave-app.md#install-and-setup).

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

## <a name="troubleshooting"></a>Problembehandlung

Wenn Sie Probleme bei der Anmeldung oder Verwendung der Dynamics 365 Human Resources Teams App haben, versuchen Sie, diese Anweisungen zur Fehlerbehebung zu befolgen. Wenn Sie nach der Problembehandlung immer noch Probleme haben, wenden Sie sich an den Support. Weitere Informationen erhalten Sie über den [Support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Sie können sich nicht in Teams bei der Human Resources-App anmelden

Wenn Sie sich nicht bei der App anmelden können, ist es möglich, dass das Konto, das Sie zur Anmeldung bei Microsoft Teams verwenden, keinem Mitarbeiterdatensatz in Dynamics 365 Human Resources zugeordnet ist. Wenden Sie sich an Ihren Systemadministrator, um sicherzustellen, dass Ihr Mitarbeiterdatensatz korrekt zugeordnet ist.

### <a name="translations-dont-display-correctly"></a>Übersetzungen werden nicht korrekt angezeigt

Wenn die Übersetzungen nicht wie erwartet angezeigt werden, stellen Sie sicher, dass die Sprache, die Sie in Teams auswählen, mit der in Human Resources **Benutzeroptionen** ausgewählten Sprache übereinstimmt.

In Teams sehen Sie sich **App-Sprache** in **Einstellungen** an.

![Teams-Einstellungen](./media/hr-teams-leave-app-settings.png)

Wählen Sie in Human Resources **Einstellungen** und wählen Sie dann **Benutzeroptionen**. Stellen Sie sicher, dass das Feld **Sprache** mit dem Feld **App-Sprache** in Teams übereinstimmt.

![Human Resources Benutzeroptionen](./media/hr-teams-leave-app-user-options.png)

Wenn Sie immer noch Übersetzungsprobleme haben, lassen Sie es uns wissen. Informationen finden Sie unter [Unterstützung für Finance and Operations-Apps oder Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Fehler beim Genehmigen von Urlaubsanträgen in der Human Resources-App in Teams

Wenn Sie beim Versuch, Urlaubsanträge in der Teams-App zu genehmigen, eine Fehlermeldung erhalten, versuchen Sie es mit der folgenden Problembehandlung:

1. Stellen Sie sicher, dass das Konto, mit dem Sie sich bei Microsoft Teams anmelden, dasselbe ist, mit dem Sie auf Dynamics 365 Human Resources zugreifen.

2. Stellen Sie sicher, dass Sie ein gültiger Genehmiger für die Anforderung sind, indem Sie die Workflow-Einstellungen auf Urlaubsgenehmigung überprüfen. Weitere Informationen zu Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Genehmiger von Abwesenheiten erhalten keine Teams-Chat-Nachrichten, um Abwesenheitsanträge zu genehmigen

1. Stellen Sie sicher, dass Benachrichtigungen für die Umgebung und den Benutzer aktiviert sind. Weitere Informationen finden Sie unter [Benachrichtigungen für die Human Resources App in Teams aktivieren](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) und [Benachrichtigungen von Teams für einzelne Benutzer ein- oder ausschalten](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Stellen Sie sicher, dass die Benutzer auf der Registerkarte **Chats** mit denselben Anmeldeinformationen angemeldet sind, die sie für die Genehmigung von Urlaubsanträgen verwenden. Verwenden Sie die Nachrichten „Abmelden“ und dann „Anmelden“, um sich mit den richtigen Anmeldeinformationen anzumelden.

3. Wenn das Problem weiterhin besteht, überprüfen Sie als Systemadministrator den Status des Batchauftrags für das System Business Events. Wenn es sich in einer Warte- oder Ausführungsphase befindet, schauen Sie in ein paar Minuten noch einmal nach. Wenn der Status unverändert bleibt, protokollieren Sie ein Support-Ticket, damit unser Team das Problem beheben kann.

## <a name="known-accessibility-issues"></a>Bekannte Probleme mit den Eingabehilfen

In der Human Resources-App in Teams gibt es die folgenden Probleme mit den Eingabehilfen, an deren Behebung wir in zukünftigen Versionen arbeiten.

| Abgang | Problemumgehung oder Erklärung |
| --- | --- |
| Bei Zoomen auf 400 % auf dem Desktop werden einige der Aktionsschaltflächen ausgeblendet. | Sie sollten eine Bildschirmlupe verwenden, bis wir diese Zoomstufe unterstützen können. |
| Auf der Registerkarte **Arbeitsfreie Zeit** gibt das Voiceover eine Schaltfläche „Aktion“ an, wenn die Kopfzeile für das Raster für arbeitsfreie Zeit vorliest. | Die Kopfzeile und die Elemente im Raster sind nach Jahr gruppiert und können ausgeblendet werden. Das Voiceover interpretiert dies als umsetzbares Element, obwohl dies nicht der Fall ist. |
| In der Registerkarte **Arbeitsfreie Zeit** gibt es eine zusätzliche Wischgeste, wenn Sie zum **Ursachencode** in einem neuen Antrag navigieren. | Es gibt kein verstecktes Steuerelement, zu dem die Wischnavigation gelangen möchte. |
| Wenn Sie in der Registerkarte **Arbeitsfreie Zeit** wischen, während der Kalender geöffnet ist, befinden Sie sich außerhalb des Steuerelements, anstatt in einem neuen Antrag oder beim Bearbeiten eines Antrags ganz oben. | Wenn Sie **Zu heute gehen** erreichen, betrachten Sie dies als Ende des Steuerelements und wischen Sie in die entgegengesetzte Richtung, um wieder nach oben zu gelangen. |
| In der Registerkarte **Chat** springt der Fokus wieder nach oben, wenn Sie ein Datum eingeben, während Sie das Hilfsmittel oder die Tastaturnavigation verwenden. | Tippen Sie, bis Sie Ihren Eingabebereich wieder erreichen. |

## <a name="privacy-notice"></a>Datenschutzhinweis

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen. Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet. Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/). Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso). Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft. 

Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt. Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf. Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden. 

Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet. Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid und Azure Cosmos DB

Bei Verwendung der Dynamics 365 Human Resources-App in Microsoft Teams fließen möglicherweise bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird.

Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams. Diese Daten können bis zu 24 Stunden in Microsoft Azure Event Grid gespeichert werden und werden in den USA verarbeitet, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet. Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Während der Konversation mit dem Chat-Bot in der Human Resources-App wird der Konversationsinhalt möglicherweise in Azure Cosmos DB gespeichert und an Microsoft Teams übertragen. Diese Daten können in Azure Cosmos DB bis zu 24 Stunden lang gespeichert und außerhalb der geografischen Region verarbeitet werden, in der der Human Resources-Service Ihres Mandanten bereitgestellt wird, werden während des Transports und in Ruhe verschlüsselt und von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet. Um zu verstehen, wo Ihre Daten in Teams gespeichert sind, lesen Sie bitte: [Speicherort von Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Um den Zugriff auf die Human Resources-App in Microsoft Teams für Ihre Organisation oder Benutzer in Ihrer Organisation zu beschränken, finden Sie unter Informationen unter [Verwalten von App-Berechtigungsrichtlinien in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Siehe auch

[Microsoft Teams herunterladen und installieren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-Hilfecenter](https://support.office.com/teams)</br>
[Human Resources-App in Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
