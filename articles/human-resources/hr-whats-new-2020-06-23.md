---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (25. Juni 2020)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Human Resources entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 6/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8d83268292ac65d62cbe8fa9a4c146bf4af36b50
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555026"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources (23. Juni 2020)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3347. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Wenn eine Registrierung für einen gekündigten Mitarbeiter abgelaufen ist, werden Urlaubstyp, Saldo und Betrag im Formular für die Urlaubsregistrierung (444867) gelöscht.

Die Werte unter **Urlaubstyp**, **Saldo** und **Betrag** werden jetzt beibehalten, anstatt bei dieser Auswahl gelöscht zu werden.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Falsch prognostizierter Saldo, wenn die neue Funktion (Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan) aktiviert ist (456553)

Der prognostizierte Saldo wird jetzt korrekt angezeigt, wenn diese Funktion aktiviert wurde.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Entitäten mit Beziehungen, die zu doppelten Navigationseigenschaften führen (456486)

Diese Version behebt ein Problem mit den Navigationseigenschaften (Beziehungen) mehrerer Entitäten. Doppelte Beziehungen werden erkannt. Diese Szenarien wurden alle korrigiert.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Unternehmensübergreifende Kommentare zur Leistungsbeurteilung (455536)

Unternehmensübergreifende Kommentare zu Leistungsbeurteilungen sind mit dieser Fehlerkorrektur jetzt sichtbar. Diese Änderung korrigiert die Ansicht der Kommentare des Prüfers, die in verschiedenen Unternehmen für dieselbe Leistungsbeurteilung eingegeben wurden.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Inkonsistenz bei der Anzeige von Vergütungsverwaltungsdaten (432562)

Die Self-Service-Übersicht für Manager bietet jetzt eine konsistente Ansicht der Vergütungsdaten. Abhängig davon, wie Sie zu den **Vergütungsdetails** eines Mitarbeiters navigieren, werden diese den Managern jetzt konsistent angezeigt.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Datum des Inkrafttretens des festen Vergütungsplans ist standardmäßig das heutige Datum (411994)

Das Startdatum der Vergütung basiert nun auf dem Startdatum der Position, die dem Mitarbeiter zugewiesen wurde.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>„Aktivieren Sie die Halbtagesdefinition“ im Formular für Urlaub und Abwesenheit ist beim Öffnen des Formulars deaktiviert (452607)

Mit dieser Änderung wird **Aktivieren Sie die Halbtagesdefinition** aktiviert, bis neue Urlaubstransaktionen existieren. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Veröffentlichung in HcmDiscussionEntity über Excel nicht möglich; Feldfehler TotalRatingScore (453899)

Sie können das Feld **TotalRatingScore** jetzt mit **HCMDiscussionEntity** im Excel-Arbeitsmappen-Designer aktualisieren.

## <a name="in-preview"></a>Vorschau

## <a name="database-logging"></a>Datenbankprotokollierung

Mit der Datenbankprotokollierung können Sie festlegen, welche Tabellen und Felder überwacht werden sollen. Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen. Sie verwenden Datenbankprotokollierungsfunktionen, um diese Änderungen im Laufe der Zeit anzuzeigen. Weitere Informationen finden Sie unter [Konfigurieren und verwalten Sie die Datenbankprotokollierung](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Pflichtfelder 

Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder jetzt zu Pflichtfeldern machen. Diese Funktion erfordert **Gespeicherte Ansichten**.

## <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie unter [Human Resources App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF) Entitäten für das Leistungsmanagement
 
Leistungsverwaltungsentitäten geben frei. Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren. Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit. Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.

## <a name="buy-and-sell-leave"></a>Urlaub kaufen und verkaufen 

Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können. Dieser Prozess wird häufig manuell verwaltet. Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung. Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen. Weitere Informationen finden Sie hier:

- [Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Urlaub kaufen und verkaufen](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan

Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten. Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Abgrenzungsrichtlinien Klarheit über den Abgrenzungsprozess. Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>Fügen Sie Anhänge zu Freizeitanfragen hinzu

Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung. Mitarbeiter können diese Anhänge jetzt hinzufügen. Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen. Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Ursachencode für Ansammlungsaussetzungen hinzufügen 

Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.

## <a name="carry-forward-rules"></a>Vortragungsregeln 

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen

Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen. Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein. Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-Entität verfügbar für Ansammlungsaussetzungen 

Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.

## <a name="coming-soon"></a>Bald verfügbar

## <a name="configure-the-name-of-employee-self-service"></a>Name des Mitarbeiter-Self-Service konfigurieren

Unter **Personalverwaltungsparameter** ist eine neue Option verfügbar, mit der der Name des Mitarbeiter-Self-Service-Arbeitsbereichs auf Self-Service aktualisiert werden kann.

## <a name="checklist-entities-included-in-common-data-service"></a>In Common Data Service enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Common Data Service verfügbar sein.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)