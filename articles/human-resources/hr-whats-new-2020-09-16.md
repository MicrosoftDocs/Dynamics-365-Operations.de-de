---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (16. September 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 16. September 2020 neu sind oder geändert wurden.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1386cca9fd39c2cf021e87fcc33da2bbda89630
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353589"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (16. September 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3557. Die Zahlen in Klammern neben einigen Funktionen beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>In dieser Version enthalten

-  [Gespeicherte Ansichten – allgemeine Verfügbarkeit](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Weitere Informationen finden Sie unter [Gespeicherte Ansichten](../fin-ops-core/fin-ops/get-started/saved-views.md). 

- Das **Aktionen positionieren**-Formular verfügt über ein aktualisiertes Dimensionsraster und einen neuen Dialog (469495).

- Wenn Sie **Den Zugriff auf Worker-Informationen beschränken** in **Erweiterter Zugriff** im **Gemeinsame Parameter für die Personalabteilung** auf Ja einstellen, werden in Leistungsformularen nur noch die entsprechenden Worker angezeigt (393384).

- Neue Kalenderoptionen für die Kalendererstellung in der **WorkCalendar**-Entität (477055):<br>- Standardendzeit<br>- Standardstartzeit<br>- Ist Freitag Arbeitstag<br>- Ist Montag Arbeitstag<br>- Ist Samstag Arbeitstag<br>- Ist Sonntag Arbeitstag<br>- Ist Donnerstag Arbeitstag<br>- Ist Dienstag Arbeitstag<br>- Ist Mittwoch Arbeitstag<br>- Arbeitskalenderurlaubs-ID

- Die **LeaveBankTransactionV1**-Entität enthält jetzt den Ursachencode (477823).

- Sie können jetzt Aufgabenaufzeichnungen speichern (492923).

- Daten werden nun erfolgreich von **HCMWorkerContactEntity** veröffentlicht (427620).

- Das Inforegister **Vergütung** wird jetzt im **Arbeitskraftaktionen**-Formular für den Auftragnehmer-Arbeitskrafttyp angezeigt (482494).

- Die Felder **Ebene** und **Plan** sind jetzt obligatorisch, wenn Sie **Feste Vergütung** festlegen. Eine Fehlermeldung wird angezeigt, wenn Sie diese Felder leer lassen (482497).

- Das **Typ des Plans**-Feld in **Vorteile** ist jetzt eine Dropdown-Liste (488768).

- Systemadministratoren erhalten jetzt eine Benachrichtigung, wenn ein benutzerdefiniertes Feld aus Human Resources gelöscht wird (481408).

- Während des Prozesses zum Beenden des Mitarbeiters verhält sich Human Resources wie erwartet und ändert das ausgewählte Unternehmen nicht, nachdem es scheinbar gesperrt wurde (479877). 

- Manager können durch Personalisierung keine Nummernspalte mehr hinzufügen (485317).

- Manager können den Datenbereichsfilter nicht mehr aus abgelaufenen Identifikationsnummern entfernen (485321).

- Wenn das **Berichtet an**-Feld leer ist, werden Positionsdetails weiterhin angezeigt, wenn Sie mit der Maus über die Position fahren (433328).

- Mitarbeiter können jetzt in Mitarbeiter-Self-Service Informationen zum Vorteilsplan anzeigen (481676) anzeigen.

- Mitarbeiter können jetzt alle registrierten Kurse sehen (429048).

- Sie können jetzt die Anzeigeoptionen für die **Berufszertifikate**-Seite einschränken. Sie können die Anzeigeoptionen nach Arbeitskraftstatus und nach Arbeitskrafttyp auf die aktuelle juristische Person beschränken (451501). 


## <a name="in-preview"></a>In Vorschau

### <a name="human-resources-app-in-teams"></a>Human Resources-App in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie hier:

- [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 1
- [Human Resources-App in Teams](./hr-admin-teams-leave-app.md) in der Dokumentation für Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-App in Teams-Vorschaufunktonen
 
-  **Benachrichtigungen**: Antragssteller und Genehmigende von Anforderungen arbeitsfreier Zeit werden in der Human Resources-App in Teams benachrichtigt. Genehmigende Personen können Freistellungsanträge genehmigen oder ablehnen. Einreicher werden benachrichtigt, wenn die Anfrage genehmigt oder abgelehnt wurde. Weitere Informationen finden Sie hier:
   - [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 2
   - [Aktivieren von Benachrichtigungen für die Human Resources-App in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in der Dokumentation für Human Resources
   - [Aktivieren oder Deaktivieren von Team-Benachrichtigungen für einzelne Benutzer](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in der Dokumentation für Human Resources
   - [Teams-Benachrichtigungen](./hr-teams-leave-app.md#respond-to-teams-notifications) in der Dokumentation für Human Resources
   - [Anzeigen den Urlaubskalenders Ihres Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in der Dokumentation für Human Resources
 
- **Manager-Kalender für arbeitsfreie Zeit**: Manager können die genehmigte und ausstehende arbeitsfreie Zeit für ihre direkten Berichte in einer Kalenderansicht anzeigen. Diese Ansicht bietet ein einfaches Verständnis dafür, wann ihre Teammitglieder nicht arbeiten. Weitere Informationen finden Sie hier:
   - [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 2
   - [Anzeigen den Urlaubskalenders Ihres Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in der Dokumentation für Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente (477004)

Eine neue Option ist jetzt verfügbar, um die **Mir zugewiesene Arbeitselemente**-Liste in der rechten Spalte des Dashboards zu positionieren. Mit dieser Änderung werden alle Arbeitselemente und Aufgabenlisten im selben Bereich angezeigt. Aktivieren Sie diese Funktion durch Einschalten von **Vorschau – Verbesserungen der Workflow-Erfahrung** in der Funktionsverwaltung. Weitere Informationen zur Aktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

Diese Funktion fördert auch die Workflow-Optionen, die in den Formularen für Personalaktionen angezeigt werden. Workflow-Optionen werden auch über das Aktion-Inforegister für den schnellen Zugriff angezeigt. Weitere Informationen finden Sie hier: 

- [Verbesserung der Workflow-Erfahrung in Organisation und Personalverwaltung](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) im Plan der Dynamics 365 2020 Versionswelle 2

![Mir zugewiesene Arbeitsaufgaben.](./media/hr-workflow-work-items-assigned-to-me.png)

![Schneller Zugriff auf Workflow-Elemente.](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Urlaubs- und Abwesenheitskalender

Diese Version enthält zusätzliche Kalenderoptionen für Urlaubs- und Abwesenheitskalender. Weitere Informationen finden Sie unter [Team- und Unternehmenskalender anzeigen](./hr-employee-self-service-calendar.md).

## <a name="coming-soon"></a>Bald verfügbar

### <a name="checklist-entities-included-in-dataverse"></a>In Dataverse enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.

### <a name="benefits-management-reason-codes"></a>Ursachencodes für die Vergütungsverwaltung

Ursachencodes für das Vergütungsverwaltung werden in Kürze mit vorhandenen Ursachencodes in der Human Resources kombiniert. Wenn Sie in der Vergütungsverwaltung Ursachencodes mit mehr als 15 Zeichen erstellt haben, müssen Sie den Namen des Ursachencodes im Vergütungsverwaltungsformular **Ursachencodes** auf maximal 15 Zeichen ändern. Nachdem Sie den Namen aktualisiert haben, wird der Ursachencode unter dem vorhandenen Ursachencodeformular in der Personalverwaltung angezeigt. Diese Änderung wird in Zukunft verfügbar sein und sich nicht auf vorhandene Funktionen auswirken.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
