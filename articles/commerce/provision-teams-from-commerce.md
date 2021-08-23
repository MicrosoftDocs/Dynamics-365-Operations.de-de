---
title: Microsoft Teams aus Dynamics 365 Commerce bereitstellen
description: In diesem Thema wird Sie Microsoft Teams durch die Verwendung von Organisationsdaten aus Dynamics 365 Commerce bereitstellen.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 715b18acb10edebafe60805393cbc16c5be513ef3605cf7a575ff98362443bb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766432"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Microsoft Teams aus Dynamics 365 Commerce bereitstellen

[!include [banner](includes/banner.md)]

In diesem Thema wird Sie Microsoft Teams durch die Verwendung von Organisationsdaten aus Dynamics 365 Commerce bereitstellen.

Dynamics 365 Commerce bietet eine einfache Möglichkeit, Teams bereitzustellen, wenn Sie dort noch keine Teams für Ihre Einzelhandelsgeschäfte eingerichtet haben. Indem Sie genau definierte Informationen aus Commerce nutzen, die Sie in Teams verwenden möchten, können Sie Ihren Filialmitarbeitern den Einstieg in Teams erleichtern. Diese Informationen umfassen die Organisationshierarchie, Geschäftsnamen, Mitarbeiterinformationen und Azure Active Directory-Konten (Azure AD). 

Der Prozess der Bereitstellung von Teams besteht aus zwei Hauptschritten:

1. Erstellen Sie in Teams ein Team für jedes Einzelhandelsgeschäft und fügen Sie Filialmitarbeiter als Mitglieder des entsprechenden Teams hinzu. Wenn ein Mitarbeiter mit mehr als einem Einzelhandelsgeschäft verbunden ist, spiegelt die Teammitgliedschaft diese Tatsache wider. Ein Kommunikationsteam, dem Regionalmanager als Mitglieder angehören, wird erstellt, um die Veröffentlichung von Aufgaben aus Teams zu unterstützen.
1. Laden Sie Ihre Organisationshierarchie von Commerce in Teams hoch.

## <a name="provision-teams-in-commerce-headquarters"></a>Teams in der Commerce-Zentralverwaltung bereitstellen

Bevor Sie Microsoft Teams bereitstellen führen Sie die folgenden Aufgaben aus:

- Bestätigen Sie, dass alle Regionalmanager zu Kommunikationsmanagern ernannt wurden.
- Stellen Sie sicher, dass das Azure-Konto jedes Filialleiters und Worker mit dem Arbeitsdatensatz dieses Managers oder Workers in der Commerce-Zentralverwaltung verknüpft ist.

Führen Sie die folgenden Schritte aus, um Teams in der Commerce-Zentralverwaltung bereitzustellen.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.
1. Wählen Sie im Aktivitätsbereich **Teams bereitstellen** aus. Ein Stapelverarbeitungsauftrag mit Namen **Teams bereitstellen** wird erstellt.
1. Gehen Sie zu **Systemadministration \> Anfragen \> Stapelverarbeitungsaufträge** und finden Sie den neuesten Auftrag mit der Beschreibung **Teams-Bereitstellung**. Warten Sie, bis dieser Auftrag ausgeführt wurde.

> [!TIP]
> Wenn keinem Ihrer Regionalmanager, Filialleiter und Geschäftsmitarbeiter eine Teams-Lizenz zugeordnet wurde, wird möglicherweise die folgende Fehlermeldung angezeigt: „Anwendbare Sku-Kategorien für den Benutzer konnten nicht abgerufen werden.“ Wählen Sie, um das Problem zu beheben, im Aktivitätsbereich **Teams und Mitglieder synchronisieren** aus.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Teams-Bereitstellung im Teams Admin Center überprüfen

Um die Microsoft Teams-Bereitstellung im Microsoft Teams Admin Center zu überprüfen, befolgen Sie diese Schritte.
    
1. Gehen Sie zum [Teams Admin Center](https://admin.teams.microsoft.com/) und melden Sie sich als Administrator Ihres E-Commerce-Mandanten an.
1. Wählen Sie im linken Navigationsbereich **Teams** aus, um es zu erweitern, und wählen Sie dann **Teams verwalten** aus.
1. Bestätigen Sie, dass für jedes Commerce-Einzelhandelsgeschäft ein Team erstellt wurde.
1. Wählen Sie ein Team aus und bestätigen Sie, dass Filialmitarbeiter als Mitglieder hinzugefügt wurden.
1. Wählen Sie im linken Navigationsbereich **Benutzer** aus und bestätigen Sie, dass alle Filialmitarbeiter in allen Filialen als Benutzer hinzugefügt wurden.

Die folgende Abbildung zeigt ein Beispiel für die Seite **Teams verwalten** im Team Admin Center.

![Beispiel für die Seite „Teams verwalten“ im Teams Admin Center.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Eine Commerce-Organisationshierarchie in Teams hochladen
    
Die Commerce-Organisationshierarchie kann in Microsoft Teams verwendet werden, um Aufgaben in allen oder ausgewählten Geschäften zu veröffentlichen, die dieselbe Hierarchiestruktur verwenden.

Um eine Commerce-Organisationshierarchie in Teams hochzuladen, folgen Sie diesen Schritten.
    
1. Gehen Sie in der Commerce-Zentralverwaltung zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams-Integrationskonfiguration**.
1. Wählen Sie **Adressierungshierarchie herunterladen** und dann **Einzelhandelsgeschäfte nach Regionen** aus, um die Organisationshierarchie als Datei mit kommagetrennten Werten (CSV-Datei) herunterzuladen.
1. Installieren Sie das Microsoft Teams PowerShell-Modul mithilfe der Schritte in [Microsoft Teams Power Shell installieren](/microsoftteams/teams-powershell-install).
1. Wenn Sie im Team PowerShell-Fenster dazu aufgefordert werden, melden Sie sich mit dem Administratorkonto für Ihren Azure AD-Mandanten an.
1. Befolgen Sie die Schritte in [Einrichten Ihrer Team-Adressierungshierarchie](/microsoftteams/set-up-your-team-hierarchy), um die CSV-Datei für die Adressierungshierarchie hochzuladen.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Sicherstellen, dass die Organisationshierarchie in Teams hochgeladen wurde

Um sicherzustellen, dass die Organisationshierarchie in Microsoft Teams hochzuladen, gehen Sie wie folgt vor.

1. Melden Sie sich in Teams als Kommunikationsmanager an.
1. Wählen Sie im linken Navigationsbereich **Aufgaben aus Planner** aus.
1. Erstellen Sie auf der Registerkarte **Veröffentlichte Listen** eine neue Liste mit einer Dummy-Aufgabe.
1. Wählen Sie **Veröffentlichen** aus. Die Organisationshierarchie sollte im Dialogfeld **Auswählen, an wen veröffentlicht werden soll** erscheinen wie im Beispiel in der folgenden Abbildung gezeigt.

![Beispiel für eine Organisationshierarchie im Dialogfeld „Auswählen, an wen veröffentlicht werden soll“.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren](enable-teams-integration.md)

[Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren](synchronize-tasks-teams-pos.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)