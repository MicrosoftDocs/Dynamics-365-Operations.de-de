---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (08. Juli 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 8. Juli 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14dfd925009cb2a9d40044e27f28521ff4d331b7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130396"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources (8. Juli 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3382. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="database-logging"></a>Datenbankprotokollierung

Mit der Datenbankprotokollierung können Sie festlegen, welche Tabellen und Felder überwacht werden sollen. Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen. Sie verwenden Datenbankprotokollierungsfunktionen, um diese Änderungen im Laufe der Zeit anzuzeigen. Weitere Informationen finden Sie unter [Konfigurieren und verwalten Sie die Datenbankprotokollierung](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Name des Mitarbeiter-Self-Service konfigurieren

In **Personalverwaltungsparameter** können Sie jetzt den Namen des Arbeitsbereichs **Mitarbeiter-Self-Service** zu **Self-Service** ändern. Weitere Informationen finden Sie unter [Mitarbeiter-Self-Service-Arbeitsbereichsname ändern](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Offener Beitrittszugriff der Vorteilsverwaltung außerhalb des Zeitraums

Dieses Release behebt einen Fehler, bei dem Mitarbeiter auf Vorteile des offenen Beitritts außerhalb des Beitrittszeitraums zugreifen konnten oder ohne ein Life-Ereignis. Wenn Sie den offenen Beitritt im Mitarbeiter-Self-Service demonstrieren möchten, müssen Sie die offenen Beitrittsdaten auf heute (oder früher) anpassen, um darauf zugreifen zu können. Sie können diese Einstellung unter **Vorteilsverwaltung > Regeln und Optionszeiträume** ändern.

## <a name="email-employee-enrollment-confirmation"></a>Mitarbeiterbeitrittsbestätigung per E-Mail senden

Sie können jetzt E-Mails an Mitarbeiter senden, nachdem diese ihre Vorteilsauswahl abgeschlossen haben. Sie können entweder eine Standardnachricht senden oder eine E-Mail-Vorlage der Organisation verwenden. Diese Einstellungen finden Sie unter **Personalverwaltungsparameter > Vorteilsverwaltung**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Die stornierte Abwesenheit wird in der kommenden arbeitsfreien Zeit weiterhin im Arbeitsbereich „Personen“ angezeigt (441358)

Stornierte Abwesenheit wird nicht mehr als bevorstehende arbeitsfreie Zeit auf den Urlaubskarten im Arbeitsbereich **Personen** angezeigt.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Die Abteilungsentitätseigenschaft in der Entität „PositionV2“ (456486) kann nicht verwendet werden

Sie können jetzt eine Abteilung hinzufügen, ohne eine doppelte Relation zu erstellen.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity sollte nur das berechnete Feld für Pensionspläne verwenden (459779)

Beim Exportieren der Entität **PayrollWorkerEnrolledBenefitDetailEntity** bestimmt der Export, ob sie ein berechnetes Feld basierend auf einer Ratentabelle verwenden oder das Feld **ContributionAmountCur** in der Sicherungstabelle verwenden soll. Die von der Datenentität verwendete Logik verwendet die Ratentabelle in Situationen, in denen die Anwendung dies normalerweise nicht tut. Diese Logik bewirkt, dass die Entitätsexporte einen Nullwert für diese Spalte zurückgeben, da keine Berechnungsratentabelle vorhanden ist und das Produkt dem Kunden nicht erlaubt, eine anzugeben.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Verwirrende Übersetzungen in tschechischer Sprache in Personalverwaltung und Mitarbeiter-Self-Service (400276)

Dieses Release korrigiert die Übersetzungen für **Unternehmensverzeichnis**, **Nächster angemeldeter Kurs**, **Stelle** und **Position**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>In der WorkCalendarEmployment-Tabelle sind die erstellten und geänderten Systemfelder nicht aktiviert (460171)

Erstellte und geänderte Systemfelder sind jetzt in der Tabelle **WorkCalendarEmployment** in der Personalverwaltung aktiviert.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Nullreferenzausnahme für Einstellung und Details für zukünftigen Mitarbeiter hinzufügen (455475)

Dieses Release korrigiert einen Fehler (Nullreferenz) in der optimierten Mitarbeitereingabe, wenn Sie einen Mitarbeiter mit der Option zum **Einstellen und Details hinzufügen** einstellen.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Änderungen in der Dataverse-Arbeitskraftentität spiegeln sich nicht in der Personalverwaltung wider (455652)

Änderungen an den folgenden Feldern in der Entität **Arbeitskraft** in Dataverse werden jetzt in der Personalverwaltung angezeigt:

- **Arbeitet von zu Hause aus**
- **Dienstalterdatum**
- **Jahrestag**
- **Ursprüngliches Einstellungsdatum**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Die korrekte Vergütungsstufe basiert nicht standardmäßig auf der Stelle, die der Position zugewiesenen ist (394136)

Mit dieser Änderung basieren die korrekten Vergütungsstufen-Standardwerte auf den Datensätzen **Datum des Inkrafttretens** für die **Positionsdetails** und das **Startdatum** der **Vergütungsplanzuordnung**.

## <a name="in-preview"></a>Vorschau

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

Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten. Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Urlaubsfälligkeitsrichtlinien Klarheit für den Fälligkeitsprozess. Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Anhänge zu Abwesenheitsfragen hinzufügen

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

## <a name="checklist-entities-included-in-dataverse"></a>In Dataverse enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)
