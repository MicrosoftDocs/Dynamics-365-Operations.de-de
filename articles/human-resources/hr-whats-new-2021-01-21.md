---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 21. Januar 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 21. Januar 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f1daf630d3a9354012db9b5b487d8a5ed11e0ed
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066699"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 21. Januar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3866.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Platform Update 10.0.16(40) | -- | [Plattform-Updates für Version 10.0.16 der Finanz- und Betriebs-Apps (Februar 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Erweiterte Workflow-Anforderungen und Genehmigungen | [Organisations- und Personalmanagement-Workflow wird verbessert](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Aktualisierungen der Einhaltung des ACA (Affordable Care Act) für Formular 1095-C, Formular 1095-B und elektronische Berichterstattung in veralteten Vorteilen | -- | -- | 
| Die Vorteilsverwaltung unterstützt jetzt die ACA-Einhaltungs-Berichterstattung für in den USA ansässige juristische Personen | -- | [ACA-Berichte in der Vorteilsverwaltung generieren](hr-benefits-management-aca-reports.md) |
| Die Vorteilsverwaltung verfügt nun über exponierte Entitäten für Vorteilssätze und doppelte Vorteilsstufen  | -- | -- |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 533079 | Navigationsfehler „Formular wurde falsch aufgerufen“, wenn wir versuchen, Abzüge zu betrachten. | Fehler beim Betrachten der Vorteilsabzüge mit Ansicht **Referenzdatum**. |
| 543641 | Postleitzahl nicht in elektronische Berichterstattung eingetragen.  | Es wurde ein interner Fehler behoben, bei dem die Postleitzahl nicht in elektronischen ACA-Berichten für die Vorteilsverwaltung angezeigt wurde, wenn das Dispositionsverfahren M bis Q ist. |
| 542815 | Der Bildschirm für den persönlichen Kontakt in der Mitarbeiter-Self-Service ermöglicht es den Mitarbeitern, die persönlichen Kontakte anderer zu sehen. | Es wurde ein Fehler behoben, bei dem das **Bearbeiten**-Formular für persönliche Kontakte beim Mitarbeiter-Self-Service die Abfrage nicht ausreichend einschränkt, um sicherzustellen, dass nur ein einziger persönlicher Kontakt abgerufen wird, sodass ein Benutzer Tastaturkürzel verwenden kann, um die Kontakte anderer Personen anzuzeigen. |
| 536157 | Die **Microsoft Dataverse-Integration**-Seite in der Systemadministration kann aufgrund des Aufrufs von IsVirtualEntityPackageInstalled () nicht geöffnet werden. | Ein Problem verhindert, dass die **Microsoft Dataverse-Integration**-Seite in Human Resources geladen wird. |
| 533079 | Navigationsfehler „Formular wurde falsch aufgerufen“, wenn wir versuchen, Abzüge zu betrachten. | Es wurde ein Fehler behoben, der im **Abzüge**-Formular für die Vorteilsverwaltung das **Referenzdatum** angezeigt wird. |
| 537264 | Das Inforegister **Persönliche Angaben** fehlt im Kandidatendatensatz. | Persönliche Informationen für den Kandidaten sind jetzt im Kandidatendatensatz verfügbar. |
| 537267 | **Berufserfahrung** wird nicht in internen Kandidatendatensätzen angezeigt. | Das Inforegister **Berufserfahrung** wird jetzt in internen Kandidatendatensätzen angezeigt. Zuvor, wenn der Kandidat intern war, wurde **Berufserfahrung** durch **Beschäftigungsverlauf** ersetzt. Dies ist der Beschäftigungsverlauf des Bewerbers innerhalb der Organisation. Beide sind anwendbar und müssen für interne Kandidaten angezeigt werden. |
| 537067 | **Darf den Arbeitgeber kontaktieren** wird nicht angezeigt. | Das **Darf den Arbeitgeber kontaktieren**-Steuerelement wurde dem **Berufserfahrung bearbeiten**-Bereich für einen Kandidatendatensatz hinzugefügt. |
| 525957 | **Kandidatenstatus** aktualisiert interne Kandidaten nicht, wenn die Übertragung abgeschlossen ist. | Wenn eine Übertragung abgeschlossen ist (die **Position ändern**- oder **Fortsetzen**-Schaltfläche auf der Seite **Arbeitskraft zu einer neuen Positionszuweisung übertragen** ausgewählt ist), muss sich der **Status** im Kandidatendatensatz auf **Angestellt** ändern. |
| 537051 | Währungssymbole für die indische Rupie und die türkische Lira werden nicht korrekt mit Dataverse synchronisiert | Symbole für die indische Rupie und die türkische Lira werden jetzt korrekt mit Dataverse synchronisiert. |
| 534846 | Rekrutierungstabellen müssen für die Datenverwaltung aktiviert sein. | Die neuen Tabellen, die für die Rekrutierung von Anfragen und Kandidaten erstellt wurden, sind jetzt für die Datenverwaltung aktiviert. Dadurch kann die Änderungsnachverfolgung für die Tabellen aktiviert werden, wodurch die OData-Änderungsnachverfolgung für die virtuellen Dataverse-Tabellen aktiviert wird. |
| 533474 | Korrigieren Sie den fehlenden Verweis auf Microsoft.SqlServer.XEvent.dll. | Ausnahmen beim Laden von Assemblys für Microsoft.SqlServer.XEvent.dll blockierten die Einrichtung virtueller Dataverse-Tabellen in einigen Umgebungen. |
| 481122 | Der **Personen**-Arbeitsbereich mit zurückgezogene Positionen. | Pensionierte Positionen wurden als offene Positionen im **Personen**-Arbeitsbereich angezeigt. Pensionierte Positionen werden nicht mehr angezeigt. | 
| 541978 | Fügen Sie der BaseWorker-Entität die primäre E-Mail-Adresse hinzu. | Durch diese Änderung wurde die primäre E-Mail-Adresse des Arbeitnehmers zu HcmWorkerBaseEntity hinzugefügt. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](./hr-admin-teams-leave-app.md)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Integration mit LinkedIn Talent Hub | [Integration mit LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [In LinkedIn Talent Hub integrieren](./hr-admin-integration-linkedin.md) |
| Unternehmensübergreifende Urlaubsansicht für Manager | [Unternehmensübergreifende Ansicht des Mitarbeiterurlaubs für Manager](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Urlaub- und Abwesenheitsparameter konfigurieren](./hr-leave-and-absence-parameters.md) |
|Zusätzliche Einblicke in Abwesenheitssalden| [Zusätzliche Einblicke in Abwesenheitssalden geben](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Mitarbeiter-Sonderurlaub verwalten](./hr-leave-and-absence-manage-employee-leave.md) |
| Manager können Personalbeschaffungsanträge für Positionen einreichen | [Manager können einen Personalbeschaffungsantrag für offene Positionen einreichen](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Einen Personalbeschaffungsantrag hinzufügen](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Verbessertes Kandidatenprofil in der Personalverwaltung | [Verbessertes Kandidatenprofil in der Personalverwaltung](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Ein Kandidatenprofil hinzufügen oder bearbeiten](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Vereinfachte Integration in Rekrutierungsanbieter aktivieren | [Vereinfachte Integration in Rekrutierungsanbieter aktivieren](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaten für Stelle anwerben](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Bald verfügbar
| Funktion | Detaildaten |
| --- | --- |
| E-Mail-Bestätigung für Vorteilsregistrierung | Diese Funktion bietet eine Option zum Senden einer Bestätigungs-E-Mail an Mitarbeiter, wenn sie sich aus der Umgebung zur Vorteilsregistrierung im Mitarbeiter-Self-Service abmelden. Weitere Informationen finden Sie unter [Vorteilsverwaltungsparameter pro Unternehmen konfigurieren](hr-benefits-setup-parameters-per-company.md). |
| Von einem Manager für seine Mitarbeiter eingegebene Qualifikationen können von einem Workflow automatisch genehmigt werden | Bald verfügbar. |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologie-Updates für Microsoft Dataverse

Gültig ab November 2020, Common Data Service wurde umbenannt in [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Siehe die [offizielle Ankündigung](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) im Power Apps-Blog, um mehr zu erfahren. In Verbindung mit dieser Namensänderung wurde manche Terminologie in Dataverse aktualisiert. Beispielsweise ist *Entität* jetzt *Tabelle* und *Feld* *Säule*. Weitere Informationen finden Sie unter [Terminologie-Aktualisierungen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

In dieser Version wurde Terminologie, die sich auf die Dynamics 365 Human Resources-Integration mit Dataverse bezieht, in der gesamten Anwendung aktualisiert, um diese Änderungen widerzuspiegeln. Zum Beispiel ist das **Common Data Service-Integration**-Formular jetzt **Microsoft Dataverse-Integration**.

Weitere Informationen zur Dynamics 365 Human Resources-Integration in Microsoft Dataverse finden Sie unter [Konfigurieren der Microsoft Dataverse-Integration](./hr-admin-integration-common-data-service.md) und [Konfigurieren virtueller Microsoft Dataverse-Tabellen](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2020 Versionswelle 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
