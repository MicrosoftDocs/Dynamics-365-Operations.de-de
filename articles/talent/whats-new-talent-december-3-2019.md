---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (3. Dezember 2019)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Talent neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528692"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (3. Dezember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Talent sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2646. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Arbeitsbereich für die Funktionsverwaltung

Der Arbeitsbereich **Funktionsverwaltung** bietet eine Liste der in jedem Release ausgelieferten Features. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen. Weitere Informationen zur Feature-Verwaltung finden Sie unter [Feature-Verwaltung Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich **Feature-Management** sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.
 
Manchmal ist ein integrales Feature standardmäßig eingeschaltet und kann nicht deaktiviert werden (z.B. das **Feature-Management** Arbeitsbereich).
 
Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich **Feature-Management** zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Hinzufügen der automatischen Zeitplanung für die Bereinigung des Batchauftrags (332528)

Mit dieser Änderung wird die **Historie des Stapelverarbeitungsauftrags** jede Nacht ausgeführt und Elemente der Historie des Stapelverarbeitungsauftrags, die älter als 30 Tage sind, werden entfernt.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent reagiert nicht bei Arbeiteraktionen, wenn die Länge der Identifikationsnummer nicht mit dem Identifikationstyp übereinstimmt (390971)

Diese Version behebt das Problem, das aufgetreten ist, wenn die Länge der Identifikationsnummer nicht mit der Definition innerhalb des Identifikationstyps übereinstimmt. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Die feste Vergütung aktualisiert nicht die Ebene bei Änderungen an Positionsdetails (348085)

In der Veröffentlichung dieser Woche bestimmt das **Startdatum der Vergütung** den Auftrag, der der Position zum Zeitpunkt der Erstellung eines neuen Datensatzes für die feste Vergütung für einen Mitarbeiter zugeordnet wird.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Die Listen Arbeitskräfte, Mitarbeiter und Auftragnehmer zeigen den Arbeitertyp mit Beides an, obwohl er nur als Arbeitskraft oder Auftragnehmer (384473) angegeben sein sollte

Diese Änderung spiegelt die Art des eingegebenen Arbeitnehmers (Auftragnehmer oder Mitarbeiter) genau wider.

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>E-Mail-Benachrichtigungen für neue Einstellungsaktionen enthalten aufgrund von Sicherheitsrichtlinien keine Namensinformationen. (383402)

Diese Änderung korrigiert die Informationen, die in den Feldern „Vorname“ oder „Nachname“ in den Platzhaltern für den Workflow angezeigt werden, wenn die erweiterte Sicherheit aktiviert ist.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>System erlaubt zwei ganztägige Urlaubsanträge für denselben Tag (379284)

Mit dieser Änderung können Sie nicht zwei Urlaubsanträge für denselben Tag stellen. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Die Liste der Adressänderungen sollte nach dem Datum des Inkrafttretens sortiert sein (352798).

Mit dieser Änderung wird die Adressänderungsliste nun nach **Gültigkeitsdatum** sortiert.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Urlaubsanträge sollten das Löschen von Common Data Service aus Talent zulassen (376999)

Mit dieser Änderung können Entwürfe und stornierte Urlaubsanträge aus Common Data Service gelöscht und dann aus Talent entfernt werden.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Das Löschen von Verdienstcodes ist zulässig, wenn einem Mitarbeiter derselbe Verdienstcode zugewiesen wurde (371792).

In dieser Version müssen Sie zuerst den Verdienstcode vom Mitarbeiter entfernen, bevor Sie den Verdienstcode aus dem System löschen können.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Workflow für Beurlaubung und Abwesenheit mit zwei Genehmigungsstufen wird nicht abgeschlossen (391116)

Mit dieser Änderung werden die Arbeitsabläufe für Urlaub und Abwesenheit in allen Schritten fortgesetzt, wenn mehr als eine Genehmigungsstufe für die Anforderung konfiguriert ist.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Ausstellungsdatum wird bei Aktualisierung oder Eingabe in Talent nicht mit Common Data Service synchronisiert (397361)

Diese Änderung behebt ein Problem, bei dem das Ausstellungsdatum für die Datensätze **Personenidentifikation** nicht mit Common Data Service aus Talent synchronisiert werden konnte.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Hierarchie-Zirkelverweisfehler beim Zuweisen eines Managers zu einer Position (386659)

Diese Änderung behebt ein eindeutiges Szenario, in dem ein Zirkelverweisfehler auftritt, wenn einem neuen Manager eine Position zugewiesen wird.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service Entitäten, die nun benutzerdefinierte Felder unterstützen

Die folgenden Common Data Service-Entitäten unterstützen nun benutzerdefinierte Felder:

| Name | Entität |
| --- | --- |
| Bankkontoauszahlungen | cdm_bankaccountdisbursement |
| Vorteilsberechnungshäufigkeit | cdm_benefitcalculationfrequency |
| Berechnungshäufigkeit Lohnperiode für Vergütungen | cdm_benefitcalculationfrequencypayperiod |
| Vergütungsberechnungssatz | cdm_benefitcalculationrate |
| Vergütungsberechnungssatz-Detail | cdm_benefitcalculationratedetail |
| Vergütungsoption | cdm_benefitoption |
| Vergütungsplan | cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |
| Vergütungstyp | cdm_benefittype |
| Geschäftsprozesskalender | cdm_businessprocesscalendar |
| Zuweisung der Geschäftsprozessgruppe | cdm_businessprocessgroupassignment |
| Geschäftsprozessbibliothek-Aufgabengruppe | cdm_businessprocesslibrarytaskgroup |
| Geschäftsprozessphase | cdm_businessprocessstage |
| Kopfzeile der Prüflistenvorlage | cdm_businessprocesstemplateheader |
| Prüflistenvorlagen-Aufgabe | cdm_businessprocesstemplatetask |
| Firma | cdm_company |
| Plan mit fester Vergütung | cdm_compensationfixedplan |
| Vergütungsraster | cdm_compensationgrid |
| Vergütungsstufe | cdm_compensationlevel |
| Häufigkeit der Vergütungszahlung | cdm_compensationpayfrequency |
| Vergütungsreferenzpunkten einrichten | cdm_compensationreferencepointsetup |
| Vergütungsreferenzpunktzeile einrichten | cdm_compensationreferencepointsetupline |
| Vergütungsregion | cdm_compensationregion |
| Vergütungsstruktur | cdm_compensationstructure |
| Variabler Plan für Vergütung | cdm_compensationvariableplan |
| Variable Planstufe für Vergütung | cdm_compensationvariableplanlevel |
| Plantyp für variable Vergütung | cdm_compensationvariableplantype |
| Abteilung | cdm_department |
| Beschäftigung | cdm_employment |
| Nationalität | cdm_ethnicorigin |
| Ereignis für feste Vergütung | cdm_fixedcompensationevent |
| Auftrag | cdm_job |
| Stellenfunktion | cdm_jobfunction |
| Stellenposition | cdm_jobposition |
| Stellentyp | cdm_jobtype |
| Sprache | cdm_language |
| Bankgeschäft verlassen | cdm_leavebanktransaction |
| Urlaubsregistrierung | cdm_leaveenrollment |
| Urlaubsplan | cdm_leaveplan |
| Urlaubsantrag | cdm_leaverequest |
| Urlaubsantragdetail | cdm_leaverequestdetail |
| Urlaubstyp | cdm_leavetype |
| Ursachencode für Abwesenheitstyp | cdm_leavetypereasoncode |
| Lohnzyklus | cdm_paycycle |
| Lohnperiode | cdm_payperiod |
| Einkommenscode | cdm_payrollearningcode |
| Ausstellende Agentur für Personenidentifikation | cdm_personidentificationissuingagency |
| Positionstyp | cdm_positiontype |
| Arbeitskraftzuweisung für die Position | cdm_positionworkerassignmentmap |
| Ursachencode | cdm_reasoncode |
| Qualifikationstyp | cdm_skilltype |
| Steuerregion | cdm_taxregion |
| Übertragungsregel | cdm_vestingrule |
| Veteranenstatus | cdm_veteranstatus |
| Arbeitskalender | cdm_workcalendar |
| Arbeitskalendertag | cdm_workcalendarday |
| Arbeitskalenderurlaub |cdm_workcalendarholiday |
| Arbeitskalender-Datumsposition | cdm_workcalendarholidayline |
| Arbeitskalender-Zeitintervall | cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |
| Arbeitskraft | cdm_worker |
| Adresse Arbeitskraft | cdm_workeraddress |
| Arbeitskraftbankkonto | cdm_workerbankaccount |
| Feste Vergütung für Arbeitskraft | cdm_workerfixedcompensation |
| Persönliches Detail der Arbeitskraft | cdm_workerpersonaldetail |
| Personenidentifikationsnummer Arbeitskraft | cdm_workerpersonidentificationnumber |
| Personenidentifikationstyp Arbeitskraft | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Vorschau

Vorschaufunktionen werden nur in **Sandbox**-Umgebungen aktiviert.

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.


[!INCLUDE[footer-include](../includes/footer-banner.md)]