---
title: Human Resources-App in Teams
description: Dieses Thema enthält Informationen zur Microsoft Dynamics 365 Human Resources-App in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776307"
---
# <a name="human-resources-app-in-teams"></a>Human Resources-App in Teams

[!include [banner](includes/preview-feature.md)]

Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Mitarbeiter schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen. Mitarbeiter können mit einem Bot interagieren, um Informationen anzufordern. Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen.

![Bot für Abwesenheiten der Human Resources-App in Teams](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources-App für Abwesenheiten in Teams – Registerkarte „Arbeitsfreie Zeit“](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Installieren und einrichten

Sie finden die Human Resources-App im Teams Store. Weitere Informationen zum Installieren der Teams-App finden Sie unter [Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md).

Informationen zum Verwalten von App-Berechtigungen in Teams finden Sie unter [App-Berechtigungsrichtlinien in Microsoft Teams verwalten](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Aktivieren von Benachrichtigungen für die Human Resources-App in Teams

Wenn Benutzer Benachrichtigungen über Urlaubsanträge in der Teams-App erhalten sollen, müssen Sie Benachrichtigungen in Human Resources aktivieren.

>[!NOTE]
>Nur Benutzer, die bei Teams angemeldet sind und die App Human Resources Teams verwenden, erhalten Benachrichtigungen.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie **Links** aus.

3. Wählen Sie unter **Einrichtung** **Systemparameter** aus.

4. Legen Sie auf der **Allgemeines**-Registerkarte **Benachrichtigungen für Teams-App aktivieren** auf **Ja** fest.

   ![Aktivieren von Teams-App-Benachrichtigungen in Systemparametern](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Um Teams-Benachrichtigungen für alle Benutzer zu aktivieren, wählen Sie in der Eingabeaufforderung **Ja** aus.

   ![Aktivieren von Teams-Benachrichtigungen für alle Benutzer](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Ein- und Ausschalten von Teams-Benachrichtigungen für einzelne Benutzer

Nachdem Sie Benachrichtigungen für die Human Resources Teams-App aktiviert haben, können Sie Benachrichtigungen für einzelne Benutzer aktivieren oder deaktivieren.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie **Links** aus.

3. Wählen Sie unter **Benutzer** **Benutzeroptionen** aus.

4. Wählen Sie die Registerkarte **Workflow** aus.

5. Legen Sie **Benachrichtigungen für die Teams-App aktivieren** auf **Ja** fest, um Benachrichtigungen für den Benutzer zu aktivieren oder auf **Nein**, um Benachrichtigungen für den Benutzer zu deaktivieren.

   ![Aktivieren von Teams-App-Benachrichtigungen auf der Registerkarte „Benutzeroptionen-Workflow“](./media/hr-admin-teams-leave-app-notifications.png)

6. Wählen Sie **Speichern** aus.

## <a name="known-issues"></a>Bekannte Probleme

| Abgang | Status |
| --- | --- |
| Das horizontale Scrollen funktioniert nicht bei Android-Smartphones | Horizontales Scrollen ist auf iOS‑ oder Desktop-Geräten kein Problem. Wir arbeiten an einer Lösung für Android. |
| Fehler: Es gibt ein Problem beim Finden einer Umgebung, zu der eine Verbindung hergestellt werden kann. | Möglicherweise wird dieser Fehler auch dann angezeigt, wenn Sie überprüft haben, dass der Benutzer auf eine oder mehrere Personalumgebungen zugreifen kann. Zudem werden möglicherweise nicht alle von Ihnen erwarteten Umgebungen angezeigt. Löschen Sie den Benutzer und importieren Sie ihn erneut, um das Problem zu beheben. |
| Der Saldo ist falsch, wenn arbeitsfreie Zeit für ein zukünftiges Datum eingereicht wird. | Es ist noch keine Planungsfunktion verfügbar. Der Saldo wird für das aktuelle Datum angezeigt. |
| Eine **Wird überprüft**-Anforderung kann nicht abgebrochen werden. | Diese Funktion wird derzeit nicht unterstützt und wird in einer zukünftigen Version hinzugefügt. |
| Die Saldoinformationen werden ab heute berechnet. | Das System zeigt derzeit keine Salden ab dem Abgrenzungszeitraum an, auch wenn dies in den Urlaub- und Abwesenheitsparameter konfiguriert ist. |

## <a name="privacy-notice"></a>Datenschutzhinweis

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen. Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet. Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/). Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso). Diese Informationen werden dann an das  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft. 

Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt. Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf. Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden. 

Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet. Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten.

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azure Event Grid und Microsoft Teams

Bei Verwendung der Benachrichtigungsfunktion für die Dynamics 365 Human Resources-App in Teams fließen bestimmte Kundendaten außerhalb der geografischen Region, in der der Human Resources-Dienst Ihres Mandanten bereitgestellt wird. Dynamics 365 Human Resources überträgt die Urlaubsantrags- und Workflow-Aufgabendetails des Mitarbeiters an Microsoft Azure Event Grid und Microsoft Teams. Diese Daten können bis zu 24 Stunden gespeichert und in den USA verarbeitet werden, werden während des Transports und als Daten in Ruhe verschlüsselt und werden von Microsoft oder seinen untergeordneten verarbeitenden Betrieben nicht für Schulungen oder Serviceverbesserungen verwendet.

## <a name="see-also"></a>Siehe auch 

[Microsoft Teams herunterladen und installieren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-Hilfecenter](https://support.office.com/teams)</br>
[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md)

