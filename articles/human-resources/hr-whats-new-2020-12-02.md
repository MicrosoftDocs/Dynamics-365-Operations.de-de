---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (2. Dezember 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources ab 2. Dezember 2020 neu sind oder geändert wurden.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e02586ad3e6b4428f2ba826851db6ebc3172bdf1760b483032f5159e7864a81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782658"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (2. Dezember 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3788.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Manager können Personalbeschaffungsanträge für Positionen einreichen | [Manager können einen Personalbeschaffungsantrag für offene Positionen einreichen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Einen Personalbeschaffungsantrag hinzufügen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Verbessertes Kandidatenprofil in der Personalverwaltung | [Verbessertes Kandidatenprofil in der Personalverwaltung](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ein Kandidatenprofil hinzufügen oder bearbeiten](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Vereinfachte Integration in Rekrutierungsanbieter aktivieren | [Vereinfachte Integration in Rekrutierungsanbieter aktivieren](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten für Stellen anwerben](./hr-personnel-recruit.md) |
| Benutzerdefinierte Links im Manager-Self-Service | [Benutzerdefinierte Links im Manager-Self-Service](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Benutzerdefinierte Links im Manager-Self-Service](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können dieses Thema aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.

| Problemnummer | Abgang | Beschreibung |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult sollte Datetime enthalten, die bei der Verarbeitung verwendet wurde. | Das Ergebnis der BenefitEligibity-Verarbeitung enthält jetzt den bisher fehlenden Datetime-Stempel für die letzte Verarbeitung. |
| 526903 | Die Vorteilsregistrierung funktioniert für Pläne mit Unterhaltsberechtigten nicht, wenn **Beauftragten automatisch auswählen** in **Freigegebene Human Resources-Parameter** aktiviert ist. | Das Problem, dass die Vorteilsregistrierung für Unterhaltsberechtigte nicht funktioniert, wenn die Option **Beauftragten automatisch auswählen** für Standardbeauftragte aktiviert ist, wurde behoben. |
| 521922 | Der Parameter **Abwesenheit ohne Detail zeigen** zeigt Details zu Abwesenheitsanträgen im Abwesenheitskalender des Teams an. | Der Urlaubstyp, die Urlaubstypfarbe und die Tagesdetails wurden im Abwesenheitskalender des Teams angezeigt, wenn **Abwesenheit ohne Detail zeigen** in den **Urlaubs- und Abwesenheitsparametern** auf **Ja** gesetzt wurde. Dies wurde behoben. Der Urlaubstyp wird nicht angezeigt und die Standardfarbe für den Urlaubstyp (dunkelblau) wird für alle Urlaubstypen im Abwesenheitskalender des Teams verwendet. |
| 527316 | Titeländerungen für Stellen-, Positions- und Arbeitskraftbenachrichtigungen werden nicht synchronisiert. | Früher war den Stellen-, Positions- und Arbeitskraftentitäten eine Titel-Relation hinzugefügt. Die Synchronisierung für diese Relation funktioniert für die Synchronisierung von Human Resources zu Dataverse, funktionierte aber nicht für Benachrichtigungen von Dataverse. Dies wurde behoben. |
| 512275 | Entfernen Sie die Farboptionen aus den **Urlaubs- und Abwesenheitsparametern**. | Nachdem die Farben für den Urlaubstyp definiert wurden, werden die Farboptionen in den **Urlaubs- und Abwesenheitsparametern** nicht mehr benötigt, sodass sie entfernt wurden. |
| 437112 | Irreführender Fehlermeldungstext während der Mitarbeiterpositionszuweisung. | Die Fehlermeldung wurde aktualisiert, wenn eine Arbeitskraft eingestellt und versucht wurde, die Arbeitskraft einer Position zuzuweisen, die nicht aktiv ist. Aktualisierte Nachricht **Die angegebene Position ist zum Startdatum der Beschäftigung nicht aktiv. Bitte überprüfen Sie die Dauer dieser Position.** |
| 527816 | Leistungsprobleme mit der Seite **Arbeitsfreie Zeit**. | Die Leistung auf der Seite **Arbeitsfreie Zeit** wurde verbessert. |
| 523158 | BenefitPeriodMigrationUpgrade und BenefitPlanMigrationUpgrade werden nicht ausgeführt. | Probleme mit den Vorteilsmigrationsaufträgen im Zusammenhang mit einer unsauberen Ausführung bei **Zeitraum** und **Plan** wurden behoben. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](./hr-admin-teams-leave-app.md)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Erweiterte Workflow-Anforderungen und Genehmigungen | [Organisations- und Personalmanagement-Workflow wird verbessert](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integration mit LinkedIn Talent Hub | [Integration mit LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [In LinkedIn Talent Hub integrieren](./hr-admin-integration-linkedin.md) |
|Unternehmensübergreifende Urlaubsansicht für Manager | [Unternehmensübergreifende Ansicht des Mitarbeiterurlaubs für Manager](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Urlaub- und Abwesenheitsparameter konfigurieren](./hr-leave-and-absence-parameters.md) |
|Zusätzliche Einblicke in Abwesenheitssalden| [Zusätzliche Einblicke in Abwesenheitssalden geben](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Mitarbeiter-Sonderurlaub verwalten](./hr-leave-and-absence-manage-employee-leave.md) |
| Manager können Personalbeschaffungsanträge für Positionen einreichen | [Manager können einen Personalbeschaffungsantrag für offene Positionen einreichen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Einen Personalbeschaffungsantrag hinzufügen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Verbessertes Kandidatenprofil in der Personalverwaltung | [Verbessertes Kandidatenprofil in der Personalverwaltung](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ein Kandidatenprofil hinzufügen oder bearbeiten](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Vereinfachte Integration in Rekrutierungsanbieter aktivieren | [Vereinfachte Integration in Rekrutierungsanbieter aktivieren](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten für Stellen anwerben](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Bald verfügbar

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2020 Versionswelle 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]