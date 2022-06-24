---
title: Was ist neu oder geändert in Dynamics 365 Human Resources 22. Juni 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 22. Juni 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aacb605374d99a3c0bad3438c89e33a04a4d7faf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897776"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Was ist neu oder geändert in Dynamics 365 Human Resources 22. Juni 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4258.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Benutzer über die Funktion „Arbeitskräfte ohne Beschäftigung“ informieren – Wenn der erweiterte Zugriff aktiviert ist und die Funktion **Alle Arbeitskräfte ohne Beschäftigung anzeigen** in der Funktionsverwaltung deaktiviert ist, wird im Formular „Arbeitskräfte ohne Beschäftigung“ ein Banner angezeigt. Das Banner weist den Benutzer an, die Funktion **Alle Arbeitskräfte ohne Beschäftigung anzeigen** zu aktivieren. | Nicht zutreffend| [Arbeitskräfte ohne Beschäftigung](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Angepasste Feldunterstützung für die Berechtigungsregeln der Leistungsverwaltung | [Angepasste Feldunterstützung für die Verarbeitung von Berechtigungen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Berechtigungsregeln konfigurieren](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Überwachung von Urlaubsabgrenzungstransaktionen | Nicht zutreffend | [Überwachung von Urlaubsabgrenzungstransaktionen](hr-leave-and-absence-accrue.md)|
| Verbesserungen des Workflows für Urlaub und Abwesenheit | [Erweiterungen im Workflow für Abwesenheit und Urlaub](https://go.microsoft.com/fwlink/?linkid=2147528) | [Arbeitsfreie Zeit anfordern](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 583052 | Benutzer, die Feedback erhalten, können das erhaltene Feedback bearbeiten | Wenn ein Mitarbeiter, der Feedback zu einer Leistungserfassung erhält, **Externen Link hinzufügen** auswählt, wird das Formular bearbeitbar, was es dem Mitarbeiter erlaubt, das erhaltene Leistungsfeedback zu bearbeiten. |
| 522281 | Die Auswahl der Anzahl der Mitarbeiter auf den Kacheln der Vergütungsstruktur im Vergütungsmanagement führt zu falschen Ergebnissen| Beim Anzeigen von Detailinformationen zu den Vergütungsplänen aus dem Arbeitsbereich „Vergütung“ wird jetzt die korrekte Anzahl der Mitarbeiter angezeigt. |
| 580683 | Benutzer, die den Rollen Mitarbeiter und Manager zugeordnet sind, können keine Notizen anhängen oder eine Leistungserfassung aktualisieren | Benutzer, die den Rollen „Mitarbeiter“ und „Manager“ zugeordnet sind, können keine Notizen anhängen oder ein Leistungsjournal aktualisieren. Der Benutzer erhält die Fehlermeldung: „Datensatz im Journaleintrag „Leistung“ (HcmPerfJournal) kann nicht erstellt werden. Berechtigung der Sicherheitsrichtlinie verweigert.“ |
| 583077 | Das Geburtsdatum eines Mitarbeiters im Kalender der Firma Urlaub und Abwesenheit zeigt ein falsches Datum an | Die Benutzer können das korrekte Geburtsdatum der Mitarbeiter im Firmenkalender Urlaub und Abwesenheit anzeigen. |
| 586996 | Die Funktion zur unternehmensübergreifenden Urlaubsansicht führt dazu, dass die Salden leer sind, wenn der Zugriff auf eine einzelne Firma beschränkt ist | Die Benutzer können die zukünftigen Urlaubssalden der Mitarbeiter korrekt anzeigen, wenn die firmenübergreifende Urlaubsansicht aktiviert ist. |
| 581014 | Die Aktivierung der firmenübergreifenden Ansicht für Urlaub und Abwesenheit führt zu einem Fehler bei der Anzeige zukünftiger Salden | Es wurden Fehler behoben, wenn Benutzer die zukünftigen Urlaubssalden bei aktivierter firmenübergreifender Urlaubsansicht ansahen. |
| 509404 | Die Analyse des Abteilungspersonalbestands berücksichtigt nicht die Bewegung von Mitarbeitern zwischen Abteilungen. | Wenn ein Mitarbeiter von einer Abteilung in eine andere wechselt, spiegeln die Abteilungs-Headcount-Daten nicht die alte Abteilung wider, aus der der Mitarbeiter gewechselt ist, wenn das Positionsdetail im aktuellen Jahr verfallen ist. |
| 584851 | Die Flexibilitätsguthaben-Anteilsregel „Keine“ liefert nie ein Guthaben |Die Flex Credit Proration-Regel „Keine“ führte dazu, dass Mitarbeiter für den Leistungszeitraum keine Gutschrift erhielten, unabhängig davon, wann sie eingestellt wurden. Dies wurde behoben, so dass ein Mitarbeiter die volle Flex-Gutschrift erhält, wenn er vor Beginn des Leistungszeitraums eingestellt wird, und keine, wenn er nach Beginn des Zeitraums eingestellt wird. |
| 584897 | Das Duplizieren der Pflicht „Externe Basisfunktionalität verwenden“ führt zu einem Fehler | Beim Versuch, die Aufgabe „Externe Basisfunktionalität verwenden“ zu duplizieren, erhielt der Benutzer die Fehlermeldung „Das Objekt mit dem Bezeichner UserDefinedAppHostDialogView konnte nicht gefunden werden.“ |
| 575692 | Der Aufbau von Urlaub und Abwesenheit ist für schwebende Arbeitskräfte nicht verfügbar | Die Abgrenzung von Urlaub und Abwesenheit kann für zukünftige Mitarbeiter ausgeführt werden, wenn **Bereinigte Mitarbeiterentität** aktiviert ist. |
| 580110 | Das Hinzufügen einer Firma zur Gehaltsabrechnungsintegration setzt die Integration zurück, um alle Entitäten zu verwenden, auch wenn die Option festgelegt ist, das Projekt nicht zu aktualisieren | Wenn ein Debitor Entitäten entfernt oder das Datenprojekt für die Gehaltsabrechnungsintegration geändert hat und die Option festgelegt ist, um eine automatische Aktualisierung des Projekts zu verhindern, ignoriert das Hinzufügen einer neuen Firma zur Integration die Einstellung und aktualisiert das Projekt.  |
| 584518 |Performance-Problem bei der Verarbeitung von Enroll Benefits | Mit diesem Fehler wurden Leistungsprobleme bei der veralteten Leistungsanmeldung behoben. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Demnächst

| Funktion | Informationen |
| --- | --- |
| Plattformupdate 10.0.19 (43) | Das Plattform-Update 10.0.19 wird voraussichtlich mit dem Service-Release am 28. Juni 2021 ausgerollt. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.19 der Finanz- und Betriebs-Apps (Juni 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Umschalten der Anzeige von Betriebsjahren | Diese Funktion bietet die Möglichkeit, unterschiedliche Daten zur Berechnung der Dienstjahre zu verwenden, die im Formular **Bereinigte Mitarbeiterentität** und im Formular **Personen** angezeigt werden.  Dies wird in den Human Resources-Parametern verfügbar sein. |
|  Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Anhänge für bestimmte Urlaubsarten vorschreiben | Mit dieser Funktion können Admins das Hinzufügen von Anhängen beim Senden von Urlaubsanträgen für bestimmte Urlaubsarten vorschreiben. |
|  Konfigurieren von Einheiten pro Urlaubsart | Diese Funktion ermöglicht es Administratoren, Urlaubseinheiten (Stunden oder Tage) für jede Urlaubsart zu konfigurieren.  |
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
