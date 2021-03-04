---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (2. Dezember 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources ab 2. Dezember 2020 neu sind oder geändert wurden.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aba35563266d1149131124f489f89da61432bfb2
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669168"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (2. Dezember 2020)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3788.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Manager können Personalbeschaffungsanträge für Positionen einreichen | [Manager können einen Personalbeschaffungsantrag für offene Positionen einreichen](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Einen Personalbeschaffungsantrag hinzufügen](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Verbessertes Kandidatenprofil in der Personalverwaltung | [Verbessertes Kandidatenprofil in der Personalverwaltung](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ein Kandidatenprofil hinzufügen oder bearbeiten](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Vereinfachte Integration in Rekrutierungsanbieter aktivieren | [Vereinfachte Integration in Rekrutierungsanbieter aktivieren](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten für Stellen anwerben](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Benutzerdefinierte Links im Manager-Self-Service | [Benutzerdefinierte Links im Manager-Self-Service](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Benutzerdefinierte Links im Manager-Self-Service](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können dieses Thema aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.

| Problemnummer | Abgang | Beschreibung |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult sollte Datetime enthalten, die bei der Verarbeitung verwendet wurde. | Das Ergebnis der BenefitEligibity-Verarbeitung enthält jetzt den bisher fehlenden Datetime-Stempel für die letzte Verarbeitung. |
| 526903 | Die Vorteilsregistrierung funktioniert für Pläne mit Unterhaltsberechtigten nicht, wenn **Beauftragten automatisch auswählen** in **Freigegebene Human Resources-Parameter** aktiviert ist. | Das Problem, dass die Vorteilsregistrierung für Unterhaltsberechtigte nicht funktioniert, wenn die Option **Beauftragten automatisch auswählen** für Standardbeauftragte aktiviert ist, wurde behoben. |
| 521922 | Der Parameter **Abwesenheit ohne Detail zeigen** zeigt Details zu Abwesenheitsanträgen im Abwesenheitskalender des Teams an. | Der Urlaubstyp, die Urlaubstypfarbe und die Tagesdetails wurden im Abwesenheitskalender des Teams angezeigt, wenn **Abwesenheit ohne Detail zeigen** in den **Urlaubs- und Abwesenheitsparametern** auf **Ja** gesetzt wurde. Dies wurde behoben. Der Urlaubstyp wird nicht angezeigt und die Standardfarbe für den Urlaubstyp (dunkelblau) wird für alle Urlaubstypen im Abwesenheitskalender des Teams verwendet. |
| 527316 | Titeländerungen für Stellen-, Positions- und Arbeitskraftbenachrichtigungen werden nicht synchronisiert. | Früher war den Stellen-, Positions- und Arbeitskraftentitäten eine Titel-Relation hinzugefügt. Die Synchronisierung für diese Relation funktioniert für die Synchronisierung von Human Resources zu Common Data Service, funktionierte aber nicht für Benachrichtigungen von Common Data Service. Dies wurde behoben. |
| 512275 | Entfernen Sie die Farboptionen aus den **Urlaubs- und Abwesenheitsparametern**. | Nachdem die Farben für den Urlaubstyp definiert wurden, werden die Farboptionen in den **Urlaubs- und Abwesenheitsparametern** nicht mehr benötigt, sodass sie entfernt wurden. |
| 437112 | Irreführender Fehlermeldungstext während der Mitarbeiterpositionszuweisung. | Die Fehlermeldung wurde aktualisiert, wenn eine Arbeitskraft eingestellt und versucht wurde, die Arbeitskraft einer Position zuzuweisen, die nicht aktiv ist. Aktualisierte Nachricht **Die angegebene Position ist zum Startdatum der Beschäftigung nicht aktiv. Bitte überprüfen Sie die Dauer dieser Position.** |
| 527816 | Leistungsprobleme mit der Seite **Arbeitsfreie Zeit**. | Die Leistung auf der Seite **Arbeitsfreie Zeit** wurde verbessert. |
| 523158 | BenefitPeriodMigrationUpgrade und BenefitPlanMigrationUpgrade werden nicht ausgeführt. | Probleme mit den Vorteilsmigrationsaufträgen im Zusammenhang mit einer unsauberen Ausführung bei **Zeitraum** und **Plan** wurden behoben. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Erweiterte Workflow-Anforderungen und Genehmigungen | [Organisations- und Personalmanagement-Workflow wird verbessert](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integration mit LinkedIn Talent Hub | [Integration mit LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [In LinkedIn Talent Hub integrieren](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Unternehmensübergreifende Urlaubsansicht für Manager | [Unternehmensübergreifende Ansicht des Mitarbeiterurlaubs für Manager](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Urlaub- und Abwesenheitsparameter konfigurieren](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Zusätzliche Einblicke in Abwesenheitssalden| [Zusätzliche Einblicke in Abwesenheitssalden geben](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Mitarbeiter-Sonderurlaub verwalten](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Manager können Personalbeschaffungsanträge für Positionen einreichen | [Manager können einen Personalbeschaffungsantrag für offene Positionen einreichen](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Einen Personalbeschaffungsantrag hinzufügen](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Verbessertes Kandidatenprofil in der Personalverwaltung | [Verbessertes Kandidatenprofil in der Personalverwaltung](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ein Kandidatenprofil hinzufügen oder bearbeiten](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Vereinfachte Integration in Rekrutierungsanbieter aktivieren | [Vereinfachte Integration in Rekrutierungsanbieter aktivieren](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten für Stellen anwerben](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Bald verfügbar

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2020 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]