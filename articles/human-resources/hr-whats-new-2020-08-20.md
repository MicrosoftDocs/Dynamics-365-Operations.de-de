---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (20. August 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 20. August 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32535c1f93990306ffaa0a5d97b48d3e6fdda7d014ceeeb2552960cd08b4be6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775842"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources (20. August 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3478. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Bevorstehende und ausstehende Urlaubs- und Abwesenheitsinformationen auf Karten anzeigen im Arbeitsbereich „Personen“

Optionen für ausstehende und bevorstehende Urlaubsanträge sind jetzt auf den Urlaubs- und Abwesenheitskarten im Arbeitsbereich **Personen** verfügbar.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Das private Feld ist standardmäßig nicht „Ja“ für die Mitarbeiterrolle im Employee-Self-Service (477106)

Das Feld **Privat** ist jetzt standardmäßig **Ja**, wenn Mitarbeiter neue Adressdatensätze über die Seite **Persönliche Informationen** im Seite in Employee Self-Service hinzufügen. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Das Inforegister „Bewerber für die Einstellung“ in der Personalverwaltung zeigt eine falsche Anzahl von Bewerbern an (470110)

Die Seite **Personalverwaltung** zeigt jetzt genau die Anzahl der Bewerber an, die eingestellt werden sollen. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Krankheit für entlassenen Mitarbeiter kann nicht eingegeben werden, wenn die Abgrenzung auf Null festgelegt ist (446195)

Urlaubstransaktionen sind jetzt für Mitarbeiter zulässig, die in Zukunft gekündigt wurden, und die Abgrenzung wird auf Null gesetzt. Urlaubstransaktionen können bis zum Kündigungsdatum des Mitarbeiters eingegeben werden. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Durch Hinzufügen benutzerdefinierter Felder zum neuen Formular „Arbeitskraft“ werden die Felder im Aktionsbereich für „Urlaub verwalten“ deaktiviert (473314)

Optionen des Aktionsbereichs für das neue Formular **Arbeitskraft** in **Urlaub verwalten** wird nicht mehr deaktiviert, wenn dem neuen Formular **Arbeitskraft** benutzerdefinierte Felder hinzugefügt wurden.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Wenn das Feld „Urlaubskommentar“ obligatorisch ist, kann eine Urlaubsanforderung gesendet werden, wenn kein Kommentar eingegeben wird (473543)

Kommentarfelder können jetzt obligatorisch sein, und Urlaubsanforderungen berücksichtigen diese Einstellung. Pflichtfelder sind eine Vorschaufunktion.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-Entität verfügbar für Ansammlungsaussetzungen

Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.

## <a name="in-preview"></a>Vorschau

### <a name="mandatory-fields"></a>Pflichtfelder

Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder zu Pflichtfeldern machen. Diese Funktion erfordert **Gespeicherte Ansichten**. Weitere Informationen zu gespeicherten Ansichten finden Sie hier:

- [Gespeicherte Ansichten – allgemeine Verfügbarkeit](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) im Dynamics 365 2020 Veröffentlichungsplan Welle 2
- [Buildformulare, die gespeicherte Ansichten vollständig verwenden](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie hier:

- [Abwicklung von Urlaub und Abwesenheit von Mitarbeitern in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) im der Dynamics 365 2020 Veröffentlichungsplan Welle 1
- [Human Resources-App in Teams](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Bald verfügbar

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-App in Teams-Vorschaufunktonen
 
-  **Benachrichtigungen**: Antragssteller und Genehmigende von Anforderungen arbeitsfreier Zeit werden in der Human Resources-App in Teams benachrichtigt. Genehmigende Personen können Anforderungen arbeitsfreier Zeit genehmigen oder ablehnen und Antragsteller werden benachrichtigt, ob ihre Anforderung genehmigt oder abgelehnt wurde.
 
- **Manager-Kalender für arbeitsfreie Zeit**: Manager können die genehmigte und ausstehende arbeitsfreie Zeit für ihre direkten Berichte in einer Kalenderansicht anzeigen. Diese Ansicht bietet ein einfaches Verständnis dafür, wann ihre Teammitglieder nicht arbeiten.

### <a name="checklist-entities-included-in-dataverse"></a>In Dataverse enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.

## <a name="known-issues"></a>Bekannte Probleme

Im Arbeitsbereich **Funktionsverwaltung** werden möglicherweise Funktionen angezeigt, die als Vorschaufunktionen deaktiviert sind, wenn sie allgemein verfügbar sind. Unten finden Sie eine Liste allgemein verfügbarer Funktionen, die einen falschen Status anzeigen. 

- Vergütungsverwaltung
- Anfragenverwaltung
- Datenbankprotokollierung (Überwachung)
- Urlaubsabgrenzung für ein einzelnes Unternehmen oder einen einzelnen Plan
- Abgrenzungsunterbrechung für Urlaub und Abwesenheit
- Ursachencode und Kommentar für Saldoanpassung
- Urlaub kaufen und verkaufen
- Urlaubs‑ und Abwesenheitskalender
- Vortragsregeln für Urlaub
- Urlaubsabgrenzungsprüfung
- Urlaubsabgrenzung löschen
- Rundung für Urlaubsabgrenzungen
- Mehrere Urlaubstypen für einen einzelnen Urlaubsplan konfigurieren
- Erweiterungen zur Aktualisierung von arbeitsfreier Zeit
- FTE des Mitarbeiters für Abgrenzungen verwenden
- Ansicht für unternehmensübergreifende Vergütung
- Leistungsbeurteilungen drucken
- Feiertagsabgrenzungskorrekturen belassen

### <a name="benefit-plan-employee-entity"></a>Vorteilsplan-Mitarbeiterentität 

Wir haben kürzlich zwei Probleme in Bezug auf die Entität **BenefitsPlanEmployee** entdeckt. Beim Importieren von Mitarbeiterbeitritten werden der **Abdeckungscode** und der **Plantypcode** falsch eingestellt. Dieses Problem führt dazu, dass Mitarbeitervorteilspläne im Formular **Arbeitskraft-Vorteilsplan** sowie im Formular **Offene Beitritte** in Employee Self-Service falsch angezeigt werden. Dieses Problem kann sich auch auf die Fähigkeit des Mitarbeiters auswirken, Pläne im Employee Self-Service auszuwählen. Derzeit gibt es keine Problemumgehung. Wir behandeln dies als Fix mit hoher Priorität und werden den Fix mit unserer nächsten Version einführen.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]