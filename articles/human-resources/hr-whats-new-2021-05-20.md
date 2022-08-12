---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 20. Mai 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 20. Mai 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36d490832edcef025cb24a06288eb021eb794bd9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068483"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 20. Mai 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4189.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Plattformupdate 10.0.18 (42) | -- | [Plattform-Updates für die Version 10.0.18 der Finanz- und Betriebs-Apps (Mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Personal-App für Microsoft Teams unterstützt jetzt Halbtagesdefinitionen und getielte Tages-Funktionen | -- | [Urlaubsanträge in Teams verwalten](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 583776 | Masseneinschreibungen von Mitarbeitern in Urlaubspläne verursachen einen doppelten Datensatzfehler | Dieser Fehler wurde mit der neuesten Version behoben, und die Registrierung von Massenurlaubsplänen sollte erfolgreich verarbeitet werden. |
| 582263 | Die Verarbeitung von Lebensereignissen kann nicht für alle Mitarbeiter gleichzeitig ausgeführt werden | Wenn das Feld **Arbeitskraft** für die Verarbeitung von Lebensereignissen leer bleibt, werden alle Mitarbeiter verarbeitet. |
| 558383 | Hauptbegünstigter nicht als 100% markiert, wenn der Standardbevollmächtigte nicht ausgewählt ist | Der Fehler wurde behoben, sodass der Benutzer nur das Umschalten des primären Begünstigten auswählen muss.|
| 509404 | Analyse der Abteilungsleiterzahl ohne Berücksichtigung der Bewegung von Mitarbeitern zwischen Abteilungen |Die Analyse wurde aktualisiert, um den Transfer von Mitarbeitern zwischen Abteilungen zu berücksichtigen|
| 579420 | Die Funktion zum Einfrieren von Spalten in Rastern sollte noch nicht verfügbar sein | Die Funktion **Einfrieren von Säulen in Rastern**, die in der Personalabteilung nicht verfügbar ist, wurde in der Funktionsverwaltung als verfügbar aufgeführt. Die Funktion wurde aus der Liste der zu aktivierenden Funktionen entfernt. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Unterstützung von angepassten Feldern in den Berechtigungsregeln von Benefits Management | [Angepasste Feldunterstützung für die Verarbeitung von Berechtigungen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Berechtigungsregeln konfigurieren](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Arbeitsbereich „Vorteilsverwaltung“ | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Verbesserungen des Workflows für Urlaub und Abwesenheit | [Erweiterungen im Workflow für Abwesenheit und Urlaub](https://go.microsoft.com/fwlink/?linkid=2147528) | [Arbeitsfreie Zeit anfordern](hr-employee-self-service-request-time-off.md)|
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|
| Überwachung von Urlaubsabgrenzungstransaktionen | - | [Überwachung von Urlaubsabgrenzungstransaktionen](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Demnächst

| Funktion | Informationen |
| --- | --- |
|  Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

