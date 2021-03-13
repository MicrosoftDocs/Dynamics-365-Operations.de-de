---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (06. August 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 06. August 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f4a4de6cbed0a3ecb3e85782fac65d399731cf2
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129826"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources (06. August 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3444. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="platform-update-1001236-is-now-available"></a>Plattform-Update 10.0.12(36) ist jetzt verfügbar

Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.12 von Finance and Operations Apps (August 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF) Entitäten für das Leistungsmanagement
 
Leistungsverwaltungsentitäten geben frei. Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren. Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit. Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen. Weitere Informationen finden Sie hier:

- [Unterstützung für DMF-Entitäten](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) im Dynamics 365 2020 Veröffentlichungsplan Welle 1
- [Datenverwaltung – Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire erstellt einen Workflow für den Kauf und Verkauf von Urlaubsanträgen (446557)

Weitere Informationen finden Sie hier:

- [Mitarbeitern erlauben, Urlaub zu kaufen und zu verkaufen](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) im Dynamics 365 2020 Veröffentlichungsplan Welle 2
- [Kauf- und Verkaufsurlaubsrichtlinien verwalten](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Urlaub kaufen und verkaufen](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Postanschriften der Entität „Arbeitskraft-Postanschrift“ V2 hat Zugriff auf juristische Personen mit eingeschränktem Zugriff (459126)

Mit dieser Änderung wird die Entität **Arbeitskraft-Postanschrift V2** basierend auf dem Zugriff der juristischen Person, der dem Benutzer gewährt wird, eingeschränkt.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Der Workflow-E-Mail-Hyperlink kann keine relevanten Bewertungen öffnen (437398)

Wenn Sie den Platzhalter verwenden, um eine Leistungsüberprüfung im Überprüfungsworkflow zu öffnen, öffnet der in der E-Mail generierte Hyperlink jetzt den ausgewählten Datensatz.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Neue Entitäten für den Kauf und Verkauf von Urlaub(473180)

Datenverwaltungs-Framework-Entitäten stehen jetzt zum Kauf und Verkauf von Urlaub zur Verfügung. Weitere Informationen finden Sie unter [Datenverwaltung – Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Beim Anzeigen von Datensatzinformationen und Verwenden erweiterter Filter kann ein Benutzer auf die Datensätze anderer Mitarbeiter zugreifen (472490)

Mit dieser Änderung können Mitarbeiter-Self-Service-Benutzer nur dann auf ihre eigenen Datensätze zugreifen, wenn sie den Mitarbeiter-Self-Service verwenden. Durch das Anzeigen von Datensatzinformationen beim Ändern der Filteroption werden keine zusätzlichen Daten mehr angezeigt.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Zu den Personalführungsanalysen gehören Aufzeichnungen über ausgetretene Arbeitskräfte (382893)

Mit dieser Version umfassen Personalführungsanalysen nur noch aktive Arbeitskräfte. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Eine Lohnsteigerung für einen Mitarbeiter kann nicht verarbeitet werden (473125)

Mit dieser Änderung können Sie Lohnsteigerungen eingeben, wenn Sie das Datum des Inkrafttretens für die neue Lohnsteigerungen ändern.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Der Überprüfungsworkflow kann mehrmals gestartet werden (467541)

Mit dieser Änderung können Sie den Workflow für die Leistungsüberprüfung nur einmal starten. Der Status für den Manager zeigt nicht mehr die Option zum Starten der Überprüfung an.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Der Workflow für Urlaubsanträge endet fehlerhaft, wenn ein genehmigter Urlaubsantrag storniert wird (472063)

Wenn Sie in dieser Version einen genehmigten Urlaubsantrag stornieren, bleibt der Status des Antrags nicht mehr genehmigt, und der Workflow wird fortgesetzt.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Das System schlägt ausgetretene Mitarbeiter vor, wenn eine neue Überprüfung aus der Vorlage erstellt wird (460624)

Mit dieser Änderung sind ausgetretene Mitarbeiter länger verfügbar, wenn neue Überprüfungen aus einer Vorlage erstellt werden. Sie können keine Bewertungen für Mitarbeiter erstellen, die sich außerhalb der Daten ihrer Beschäftigung befinden.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Positionshierarchie Zirkelbezugserkennung (415879)

Mit dieser Änderung ist die Zirkelbezugserkennung der Positionshierarchie auf einen einzelnen Zeitpunkt beschränkt. Sie können die Zirkelbezugserkennung für verschiedene Daten ausführen, um zu überprüfen, dass die Berichtsstruktur keine Zirkelbezüge enthält.

## <a name="buy-and-sell-leave"></a>Urlaub kaufen und verkaufen 

Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können. Dieser Prozess wird häufig manuell verwaltet. Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung. Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen. Weitere Informationen finden Sie hier:

- [Mitarbeitern erlauben, Urlaub zu kaufen und zu verkaufen](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) im Dynamics 365 2020 Veröffentlichungsplan Welle 2
- [Kauf- und Verkaufsurlaubsrichtlinien verwalten](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Urlaub kaufen und verkaufen](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan

Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten. Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Urlaubsfälligkeitsrichtlinien Klarheit für den Fälligkeitsprozess. Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Anhänge zu Abwesenheitsfragen hinzufügen

Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung. Mitarbeiter können diese Anhänge jetzt hinzufügen. Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen. Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Ursachencode für Ansammlungsaussetzungen hinzufügen 

Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.

## <a name="carry-forward-rules"></a>Vortragungsregeln 

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen

Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen. Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein. Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.

## <a name="in-preview"></a>Vorschau

### <a name="mandatory-fields"></a>Pflichtfelder

Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder zu Pflichtfeldern machen. Diese Funktion erfordert **Gespeicherte Ansichten**. Weitere Informationen zu gespeicherten Ansichten finden Sie hier:

- [Gespeicherte Ansichten – allgemeine Verfügbarkeit](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) im Dynamics 365 2020 Veröffentlichungsplan Welle 2
- [Buildformulare, die gespeicherte Ansichten vollständig verwenden](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie hier:

- [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 1
- [Human Resources-App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-Entität verfügbar für Ansammlungsaussetzungen

Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.

## <a name="coming-soon"></a>Bald verfügbar

## <a name="checklist-entities-included-in-dataverse"></a>In Dataverse enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.

## <a name="known-issues"></a>Bekannte Probleme

Im Arbeitsbereich **Funktionsverwaltung** werden möglicherweise Funktionen angezeigt, die als Vorschaufunktionen deaktiviert sind, wenn sie allgemein verfügbar sind. Unten finden Sie eine Liste allgemein verfügbarer Funktionen, die einen falschen Status anzeigen. 

1.  Vergütungsverwaltung
2.  Anfragenverwaltung
3.  Datenbankprotokollierung (Überwachung)
4.  Urlaubsabgrenzung für ein einzelnes Unternehmen oder einen einzelnen Plan
5.  Abgrenzungsunterbrechung für Urlaub und Abwesenheit
6.  Ursachencode und Kommentar für Saldoanpassung
7.  Urlaub kaufen und verkaufen
8.  Urlaubs‑ und Abwesenheitskalender
9.  Vortragsregeln für Urlaub
10. Urlaubsabgrenzungsprüfung
11. Urlaubsabgrenzung löschen
12. Rundung für Urlaubsabgrenzungen
13. Mehrere Urlaubstypen für einen einzelnen Urlaubsplan konfigurieren
14. Erweiterungen zur Aktualisierung von arbeitsfreier Zeit
15. FTE des Mitarbeiters für Abgrenzungen verwenden
16. Ansicht für unternehmensübergreifende Vergütung
17. Leistungsbeurteilungen drucken
18. Feiertagsabgrenzungskorrekturen belassen

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)
