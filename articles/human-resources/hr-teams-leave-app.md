---
title: Urlaubsanträge in Teams verwalten
description: In diesem Thema wird beschrieben, wie Sie arbeitsfreie Zeit in der Dynamics 365 Human Resources-App in Microsoft Teams beantragen.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428827"
---
# <a name="manage-leave-requests-in-teams"></a>Urlaubsanträge in Teams verwalten

[!include [banner](includes/preview-feature.md)]

Mit der Microsoft Dynamics 365 Human Resources-App in Microsoft Teams können Sie schnell arbeitsfreie Zeit beantragen und Informationen zu Salden arbeitsfreier Zeiten in Microsoft Teams anzeigen. Sie können mit einem Bot interagieren, um Informationen anzufordern. Die Registerkarte **Arbeitsfreie Zeit** enthält detailliertere Informationen.

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

> [!WARNING]
> Die App unterstützt derzeit die Sicherheitsrolle „Systemadministrator“ nicht und zeigt eine Fehlermeldung an, wenn Sie sich mit einem Systemadministratorkonto anmelden. Wählen Sie auf der Registerkarte **Einstellungen** die Schaltfläche **Konten wechseln** aus, und melden Sie sich dann mit einem Benutzerkonto an, dem keine Systemadministratorrechte zugewiesen sind, um sich mit einem anderen Konto anzumelden.
 
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
 
Nachdem Sie eine Urlaubsanforderung gestartet haben, können Sie die Tage direkt auf der Karte anpassen oder **Details bearbeiten** auswählen, um der Anforderung zusätzliche Informationen hinzuzufügen.

![Human Resources-App für Abwesenheiten in Teams – Anforderung bearbeiten](./media/hr-teams-leave-app-bot-edit.png)
 
Wenn Sie die Informationen eingegeben haben, geben Sie **Absenden** ein, um sie zur Genehmigung einzureichen. Sie können auch **Als Entwurf speichern** eingeben, um später darauf zurückzukommen.

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
   
## <a name="privacy-notice"></a>Datenschutzhinweis

Mit dem Bot von Dynamics 365 Human Resources in Microsoft Teams werden die Texteingaben des Benutzers analysiert, um die zugrunde liegende Abfrage/Absicht zu verstehen. Die Eingabe des Benutzers, z. B. „Suchkonto Contoso“ wird an einen Cognitive Service von Microsoft mit dem Namen „Language Understanding Intelligent Service“ (LUIS) weitergeleitet. Weitere Informationen zu LUIS finden Sie  [hier](https://www.luis.ai/). Der LUIS-Dienst unterscheidet oder versteht die Absicht der Benutzereingabe (in diesem Fall besteht die Absicht darin, Informationen zu suchen) und die Zielentität (in diesem Fall ist die beabsichtigte Entität ein Konto mit dem Namen Contoso). Diese Informationen werden dann an das [Azure-Bot-Framework](https://azure.microsoft.com/services/bot-service/)  von Microsoft weitergegeben, das mit Daten aus Dynamics 365 Human Resources interagiert und die gewünschten Informationen für die Benutzerabfrage abruft. 

Wenn Sie den Bot installieren und den Zugriff für die Verwendung des Bots erlauben, stimmen Sie zu, dass der LUIS-Dienst und das Azure Bot Framework die Absicht hinter der Eingabe verarbeiten können, was zu einer verbesserten Benutzerumgebung für Unterhaltungen führt. Der LUIS-Dienst und das Azure Bot Framework weisen im Vergleich zu Dynamics 365 Human Resources möglicherweise unterschiedliche Konformitätsstufen auf. Während der LUIS-Dienst nur auf die Benutzerabfragen zugreifen kann und nicht für die Verbindung mit den Dynamics 365 Human Resources-Daten oder dem Konto des Benutzers ausgelegt ist, könnte ein Benutzer des Bots von Dynamics 365 Human Resources freiwillig eine Abfrage mit Debitorendaten, personenbezogenen Daten oder anderen Daten eingeben, und solche Abfrageinhalte könnten an den LUIS-Dienst und das Azure Bot Framework gesendet werden. 

Der Inhalt der Abfragen und Nachrichten des Benutzers wird maximal 30 Tage im LUIS-System gespeichert, im Ruhezustand verschlüsselt und nicht für Schulungen oder die Verbesserung von Dienstleistungen verwendet. Weitere Informationen zu Cognitive Services findne Sie  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Wechseln Sie zum [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/), um Administratoreinstellungen für Apps in Microsoft Teams zu verwalten. 

## <a name="see-also"></a>Siehe auch

[Microsoft Teams herunterladen und installieren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-Hilfecenter](https://support.office.com/teams)</br>
[Human Resources-App in Teams](hr-admin-teams-leave-app.md)
