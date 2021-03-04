---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (03. September 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 3. September 2020 neu sind oder geändert wurden.
author: Darinkramer
manager: tfehr
ms.date: 9/03/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ddffff18e1d6d16bd5a5f7e7021f9a34651307fa
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527457"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (3. September 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3504. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).

Weitere Informationen zu bevorstehenden Funktionen in Human Resources finden Sie unter [Übersicht über Dynamics 365 Human Resources 2019 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Weitere Informationen zum Aktualisierungsprozess für Human Resources finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>In dieser Version

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Neues Raster für Finanzdimensionen und Dialogmuster in der gesamten Personalabteilung (469495)

Das neue Muster für Finanzdimensionen ist jetzt in folgenden Bereichen verfügbar:

- Positionsaktionen (Formular: **HcmPositionActionDetail**)
- Lohn- und Einkommenscodes (Formular: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Einträge werden nicht im Urlaubskalender des Unternehmens angezeigt, wenn die Verbesserungen des Urlaubs- und Abwesenheitskalenders nicht aktiviert sind (484406)

Diese Version behebt ein Problem, bei dem Urlaubseinträge nicht im Urlaubskalender des Unternehmens angezeigt werden. Dieses Problem tritt nur auf, wenn die Funktionsverwaltungsoption **Verbesserungen des Urlaubs- und Abwesenheitskalenders** nicht aktiviert ist.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity-Problem (467597)

Diese Version behebt ein Problem mit der **BenefitsPlanEmployee**-Entität. Beim Importieren von Mitarbeiterbeitritten werden der **Abdeckungscode** und der **Plantypcode** jetzt richtig eingestellt. Dieses Problem führte dazu, dass Mitarbeitervorteilspläne in den Formularen **Arbeitskraft-Vorteilsplan** und **Offene Beitritte** in Self-Service für Mitarbeiter falsch angezeigt werden.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Elektronische Datei 1094-C gibt fehlenden Buchstaben in XML aus (435190)

Diese Änderung behebt ein Problem mit der 1094-C-Ausgabedatei, bei der ein Zeichen fehlt, das beim Senden an das IRS benötigt wird.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Tabelle mit variablen Vergütungen für Mitarbeiter, die dem Formular für feste Vergütungen zugeordnet ist (476117)

Diese Änderung richtet die Felder für feste Vergütung am Formular für feste Vergütung aus. Felder für variable Vergütung sind jetzt nur mit dem Formular für variable Vergütung verfügbar.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Urlaubsanträge sind vor der Aufnahme zulässig, wenn dieser Urlaubstyp ein negatives Mindestguthaben aufweist (469917)

Diese Änderung verbietet die Eingabe von Urlaubsanträgen vor der Aufnahme in den Plan, selbst wenn die Aufnahme ein negatives Mindestguthaben aufweist. Sie können Anfragen nur eingeben oder einreichen, wenn der Plan aktiv ist.

### <a name="document-templates-dont-download-457279"></a>Dokumentvorlagen werden nicht heruntergeladen (457279)

Mit dieser Änderung können Sie jetzt alle Dokumentvorlagen herunterladen. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Daten werden als Spaltenüberschriften anstelle von Zeilen für das Feld Lohnsatz im Vergütungsplanbericht angezeigt(476077)

Der Analysebericht zeigt jetzt die richtigen Informationen für **Lohnsatz** an.

## <a name="in-preview"></a>Vorschau

### <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie hier:

- [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 1
- [Human Resources-App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in der Dokumentation für Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-App in Teams-Vorschaufunktonen
 
-  **Benachrichtigungen**: Antragssteller und Genehmigende von Anforderungen arbeitsfreier Zeit werden in der Human Resources-App in Teams benachrichtigt. Genehmigende Personen können Freistellungsanträge genehmigen oder ablehnen. Einreicher werden benachrichtigt, wenn die Anfrage genehmigt oder abgelehnt wurde. Weitere Informationen finden Sie hier:
   - [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 2
   - [Aktivieren von Benachrichtigungen für die Human Resources-App in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in der Dokumentation für Human Resources
   - [Aktivieren oder Deaktivieren von Team-Benachrichtigungen für einzelne Benutzer](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in der Dokumentation für Human Resources
   - [Teams-Benachrichtigungen](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in der Dokumentation für Human Resources
   - [Anzeigen den Urlaubskalenders Ihres Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in der Dokumentation für Human Resources
 
- **Manager-Kalender für arbeitsfreie Zeit**: Manager können die genehmigte und ausstehende arbeitsfreie Zeit für ihre direkten Berichte in einer Kalenderansicht anzeigen. Diese Ansicht bietet ein einfaches Verständnis dafür, wann ihre Teammitglieder nicht arbeiten. Weitere Informationen finden Sie hier:
   - [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 2
   - [Anzeigen den Urlaubskalenders Ihres Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in der Dokumentation für Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente (477004)

Eine neue Option ist jetzt verfügbar, um die **Mir zugewiesene Arbeitselemente**-Liste in der rechten Spalte des Dashboards zu positionieren. Mit dieser Änderung werden alle Arbeitselemente und Aufgabenlisten im selben Bereich angezeigt. Aktivieren Sie diese Funktion durch Einschalten von **Vorschau – Verbesserungen der Workflow-Erfahrung** in der Funktionsverwaltung. Weitere Informationen zur Aktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

Diese Funktion fördert auch die Workflow-Optionen, die in den Formularen für Personalaktionen angezeigt werden. Workflow-Optionen werden auch über das Aktion-Inforegister für den schnellen Zugriff angezeigt. Weitere Informationen finden Sie hier: 

- [Verbesserung der Workflow-Erfahrung in Organisation und Personalverwaltung](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) im Plan der Dynamics 365 2020 Versionswelle 2

![Mir zugewiesene Arbeitsaufgaben](./media/hr-workflow-work-items-assigned-to-me.png)

![Schneller Zugriff auf Workflow-Elemente](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Bald verfügbar

### <a name="checklist-entities-included-in-common-data-service"></a>In Common Data Service enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Common Data Service verfügbar sein.

### <a name="benefits-management-reason-codes"></a>Ursachencodes für die Vergütungsverwaltung

Ursachencodes für das Vergütungsverwaltung werden in Kürze mit vorhandenen Ursachencodes in der Human Resources kombiniert. Wenn Sie in der Vergütungsverwaltung Ursachencodes mit mehr als 15 Zeichen erstellt haben, müssen Sie den Namen des Ursachencodes im Vergütungsverwaltungsformular **Ursachencodes** auf maximal 15 Zeichen ändern. Nachdem Sie den Namen aktualisiert haben, wird der Ursachencode unter dem vorhandenen Ursachencodeformular in der Personalverwaltung angezeigt. Diese Änderung wird in Zukunft verfügbar sein und sich nicht auf vorhandene Funktionen auswirken.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]