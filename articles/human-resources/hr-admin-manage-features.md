---
title: Funktionen verwalten
description: Erfahren Sie, wie Sie neue Funktionen in Dynamics 365 Human Resources aktivieren oder deaktivieren.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009117"
---
# <a name="manage-features"></a>Funktionen verwalten

Im Rahmen unseres kontinuierlichen Rollouts von neuen Funktionen für Microsoft Dynamics 365 Human Resources wollen wir unseren Kunden so schnell wie möglich neue Funktionen zur Verfügung stellen. Wir bieten Vorschaufunktionen, die fast bereit für die allgemeine Verfügbarkeit sind und ausgiebig getestet wurden. Wir sind nur auf der Suche nach einer letzten Runde von Kunden-Feedback und Validierung, bevor wir sie zur allgemeinen Verfügbarkeit veröffentlichen.

Weitere Informationen über neue Funktionen im Human Resources finden Sie unter [Neuerungen in Human Resources](hr-admin-whats-new.md) und [Dynamics 365 und Power Platform-Versionsveröffentlichungsplan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Der Arbeitsbereich **Funktionsverwaltung** bietet eine Liste der in jedem Release ausgelieferten Features. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen. Weitere Informationen zur Feature-Verwaltung finden Sie unter [Feature-Verwaltung Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich **Feature-Management** sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.

Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich **Feature-Management** zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

## <a name="enable-or-disable-preview-features"></a>Vorschaufunktionen aktivieren oder deaktivieren

Um auf Vorschaufunktionen zugreifen zu können, müssen Sie sie in Ihrer Umgebung zunächst aktivieren. Aktivieren oder Deaktivieren von Vorschaufunktionen ist umgebungsspezifisch.

> [!IMPORTANT]
> Vorschaufunktionen werden nur in **Sandbox**-Umgebungen aktiviert. Durch das Aktivieren der Vorschaufunktion aktivieren Sie Vorschaufunktionen für alle Benutzer in Ihrer Organisation, die sich in dieser Umgebung befinden. Wenn Sie die Vorschaufunktion deaktivieren, machen Sie sie für Ihre Benutzer unzugänglich. Die Vorschaufunktionen werden in Human Resources nur eingeschränkt unterstützt. Sie verwenden möglicherweise weniger Datenschutz‑ und Sicherheitsmaßnahmen und sind nicht in der Human Resources-Service-Level-Vereinbarung (SLA) enthalten. Sie sollten keine Vorschaufunktionen verwenden, um personenbezogene Daten (d. h. Informationen, die Sie identifizieren könnten) oder andere Daten zu verarbeiten, die gesetzlichen oder behördlichen Anforderungen unterliegen.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie die Kachel **Funktionsverwaltung**.

3. Um eine Vorschaufunktion zu aktivieren, wählen Sie sie aus der Liste aus und wählen Sie dann **Aktivieren**. Um eine Vorschaufunktion zu deaktivieren, wählen Sie sie aus der Liste aus und wählen Sie dann **Deaktivieren**.

## <a name="preview-feature-benefits-management"></a>Vorschaufunktion: Vorteilsverwaltung

Die Vorteilsverwaltung ist eine flexible Lösung, die eine Vielzahl von Vorteilsoptionen unterstützt und eine benutzerfreundliche Mitarbeitererfahrung bietet, die Ihre Angebote zeigt. Weitere Informationen zur Konfiguration und Verwendung der Vorteilsverwaltung finden Sie unter [Übersicht über die Vorteilsverwaltung](hr-benefits-management-overview.md).

Vorteilsverwaltung ersetzt die Funktionalität im Arbeitsbereich **Vorteile**. Wenn Sie die Vorschaufunktion für die Vorteilsverwaltung aktivieren, können Sie im Arbeitsbereich **Vorteile** nicht mehr auf die folgenden Formulare zugreifen:

- **Vergütungen**
- **Vergütungselemente**
- **Beitragsberechnungssätze**
- **Leistungsregistrierungsergebnisse**
- **Ergebnisse für Vergütungsablauf und -verlängerung**
- **Regeltypen für Vergütungsberechtigungsrichtlinien**
- **Vorteilsberechtigungsrichtlinien**
- **Berechtigungsereignisse**

Sie können die Informationen in diesen Formularen im schreibgeschützten Modus anzeigen. Wenn Sie die Informationen bearbeiten möchten, müssen Sie zuerst die Vorschaufunktion für die Vorteilsverwaltung deaktivieren.

### <a name="benefits-management-known-issues"></a>Bekannte Probleme bei der Vorteilsverwaltung

#### <a name="life-events"></a>Lebensereignisse

Bei der Verarbeitung von Lebensereignissen erhält der Benutzer eine Fehlermeldung:

Das Startdatum der Abdeckung muss zwischen *Beginn der Planperiode* und *Ende der Planperiode* liegen. 

Das Lebensereignis wird weiterhin wie erwartet verarbeitet.

#### <a name="eligibility-processing"></a>Verarbeitung von Berechtigungen

Wenn Sie die Berechtigung für Vorteile ausführen, die ein 1,5-faches Gehalt, einen Prozentsatz des Gehalts und ein Pauschalbetrag als Abdeckungsbetrag verwenden, muss das Datum der Vorteilsdetails auf das Mitarbeiterstartdatum in **Beschäftigungshistorie** festgelegt werden, mit geleisteten Arbeitsstunden, Zahlungshäufigkeit und jährlichem Vorteilsgehalt. Wenn für die Arbeitskraft eine feste Vergütung besteht, geben Sie die geleisteten Arbeitsstunden zusammen mit der Zahlungshäufigkeit ein und der jährliche Gehaltsbetrag wird berechnet. Wenn der Mitarbeiter fest angestellt ist, werden die geleisteten Arbeitsstunden nicht benötigt. Wir empfehlen, bei der Erstellung neuer Mitarbeiter zunächst eine feste Vergütung einzugeben. So aktualisieren Sie den Datensatz mit Vorteilsdetails: Navigieren Sie zu **Arbeitskraft > Beschäftigungshistorie > Beschäftigungsdetails**. Passen Sie das Datum an das Startdatum der Arbeitskraft an.

#### <a name="employee-self-service"></a>Mitarbeiter-Self-Service

Mitarbeiter können einen Plan auswählen, für den sie nicht qualifiziert sind, und auschecken. Beispiel: Eine Arbeitskraft hat keine Unterhaltsberechtigten, kann jedoch einen Krankenversicherungsplan mit einer Familienversicherungsoption auswählen.

Der Mitarbeiterbetrag wird bei der Aktualisierung des Abdeckungsbetrags für die Lebensversicherung nicht berechnet. Wenn einem Mitarbeiter beispielsweise eine Lebensversicherung angeboten wird, kann er bis zu 50.000 Euro Versicherungsschutz zu einem Preis von 0,36 Euro pro 1.000 Euro Versicherungsschutz auswählen.  Wenn der Mitarbeiter den Abdeckungsbetrag aktualisiert, bleiben die damit verbundenen Kosten des Mitarbeiters bei Null.

Bei einem Vorteilsplan, der nur eine einzige Auswahl dieses Plantyps zulässt, wird dem Benutzer eine Fehlermeldung angezeigt, wenn er versucht, nach Auswahl eines Plans auf einen Plan zu verzichten. Beispielsweise wählt ein Benutzer einen Krankenversicherungsplan aus und legt ihn in seinen Warenkorb. Der Benutzer wählt dann **Aufheben** für einen anderen Krankenversicherungsplan aus. Der Benutzer erhält eine Fehlermeldung.

## <a name="preview-features-in-leave-and-absence"></a>Vorschaufunktionen in Urlaub und Abwesenheit

Vorschaufunktionen in Urlaub und Abwesenheit enthalten:

- **Urlaubs‑ und Abwesenheitskalender** – die Parameter für Urlaub und Abwesenheit befinden sich nicht mehr unter **Personalverwaltungsparameter**, sondern auf einem neuen Bildschirm namens **Urlaubs‑ und Abwesenheitsparameter**. Der neue Bildschirm enthält eine neue Registerkarte **Kalender**. Diese Vorschau ermöglicht nur eine Teilmenge der Parameter. Sie können den neuen Bildschirm über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** aufrufen. Die Kalender beinhalten:
  - **Firmenkalender** – zeigt alle Freizeitanforderungen der Mitarbeiter an. Menschen mit der Rolle **Personalverwaltung** können auf diesen Kalender über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** zugreifen.
  - **Manager-Teamkalender** – zeigt alle Freizeitanforderungen von Mitarbeitern an. Manager können über die Registerkarte **Mein Team** im Mitarbeiter-Self-Service unter **Urlaub und Abwesenheit** auf den Kalender zugreifen. 

- **Urlaubs‑ und Abwesenheitskalender** – Urlaubstypen enthalten eine neue Option **Feiertag**, die in Verbindung mit dem Arbeitszeitkalender verwendet wird. Tage, die durch Feiertage und Schließungen definiert sind, werden jetzt als **Feiertag** bezeichnet, wenn Arbeitstage generiert werden. Bei der Verarbeitung von Rückstellungen werden die dem Kalender zugewiesenen Mitarbeiter angepasst, um die auf einen Arbeitstag fallenden Feiertage zu berücksichtigen.

- **Überwachen von Urlaubsrückstellung** – In einem neuen Bildschirm können Sie überprüfen, wann Rückstellungen verarbeitet und gelöscht wurden, sowohl von allen Mitarbeitern als auch von einzelnen Mitarbeitern. Sie können diesen neuen Bildschirm über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** aufrufen.

- **Löschen von Urlaubsrückstellung** – Sie können jetzt Rückstellungsdatensätze für bestimmte Urlaubspläne löschen. Sie können diese neue Option über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** aufrufen. Für einzelne Mitarbeiter erscheint diese Option in der Gruppierung **Urlaub und Abwesenheit** im Mitarbeiterprofil. 

- **Runden von Urlaubsrückstellung** – Neue Optionen für **Urlaubstyp** definieren, welche Rundungsart für die Rückstellung verwendet werden soll, sowie die Dezimalgenauigkeit der Rundung während des Rückstellungsprozesses. Bei der Verarbeitung von Rückstellungen werden Rundung und Genauigkeit auf die Rückstellungsdatensätze angewendet. 

- **Mehrere Urlaubstypen in einem einzigen Urlaubsplan konfigurieren** – In einer neuen Spalte im Urlaubsrückstellungsplan für Urlaubstypen können Sie mehrere Urlaubstypen in einem Urlaubs‑ und Abwesenheitsplan mit unterschiedlichen Rückstellungsplänen definieren. Der vorherige Feld **Urlaubstyp** wird entfernt. Bei der Mitarbeiterregistrierung werden die Salden für die Urlaubstypen jetzt in einer Tabelle angezeigt und nicht mehr oben auf dem Bildschirm.

  > [!IMPORTANT]
  > Sie können diese Funktion nicht deaktivieren, nachdem Sie sie aktiviert haben.

- **Vollzeitäquivalent (FTE) eines Mitarbeiters für die Rückstellung verwenden** – Eine neue Spalte im Urlaubsrückstellungsplan ermöglicht die Verwendung des FTE für die Rückstellung. Bei der Verarbeitung von Rückstellungen verwendet die Anwendung die primäre Position des Mitarbeiters und das definierte FTE, um den anteiligen Rückstellungsbetrag zu bestimmen.

  > [!NOTE]
  > Diese Funktion ist nur verfügbar, wenn Sie **Mehrere Urlaubstypen pro Urlaubsplan konfigurieren** aktivieren. 

## <a name="feedback"></a>Feedback

Wir möchten von Ihnen über Ihre Erfahrung mit Vorschaufunktionen hören. Wir empfehlen Ihnen, Ihr Feedback regelmäßig auf den folgenden Seiten zu veröffentlichen, wenn Sie diese oder andere Funktionen nutzen:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) - Diese Seite ist eine großartige Ressource, auf der Benutzer Anwendungsfälle diskutieren, Fragen stellen und Hilfe von der Community erhalten können.
- Teilen Sie uns mit, welche Funktionen Sie im Produkt sehen möchten und welche Änderungen Ihrer Meinung nach an bestehenden Funktionen vorgenommen werden sollten. Schlagen Sie Produktideen über [Ideen für Human Resources](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources) vor
    
Bitte geben Sie keine persönlichen Daten (Informationen, die Sie identifizieren könnten) in Ihre Feedback- oder Produktbewertungseinreichungen ein. Die gesammelten Informationen können weiter analysiert werden und werden nicht zur Beantwortung von Anfragen im Rahmen der geltenden Datenschutzgesetze verwendet. Personenbezogene Daten, die im Rahmen dieser Programme separat erfasst werden, unterliegen der [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Siehe auch

- [Neuerungen in Human Resources](hr-admin-whats-new.md)
- [Dynamics 365 und Power Platform-Versionsveröffentlichungsplan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)