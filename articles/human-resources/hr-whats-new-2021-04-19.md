---
title: Neuigkeiten oder Änderungen in Dynamics 365 Human Resources 19. April 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 19. April 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e46c5721853ebfe3b9d5955ca5f4e7a4ead570c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846299"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Neuigkeiten oder Änderungen in Dynamics 365 Human Resources 19. April 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4113.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Plattformupdate 10.0.17 (41) | -- | [Plattform-Updates für die Version 10.0.17 der Finanz- und Betriebs-Apps (April 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Unterstützung von angepassten Feldern in Formularen des Benefits Management | [Angepasste Feldunterstützung in der Leistungsverwaltung](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Vorteilsverwaltung – Übersicht](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 552164 | **Gespeicherte Ansicht** auf **Mitarbeiter-Self-Service > Kurse öffnen** funktioniert nicht für Kurse, die eine Agenda enthalten | Wenn eine gespeicherte Ansicht für offene Kurse (ESS) verwendet wird und einer der Kurse eine Agenda angehängt hat, dann zeigt die Ansicht nicht mehr mehrere Zeilen für diesen Kurs an |
| 560614 | **Leistungen > Optionen für Lebensereignisse** zeigen Diskrepanzen in der Tooltip-Dokumentation und im Code-Verhalten. | Aktualisierte Tooltips in **Lebensereignis-Optionen**, um das korrekte Verhalten anzuzeigen. |
| 560616 | **Leistungen > Lebensereignis-Optionen** sind im Leistungsplan für worker editierbar, aber Änderungen werden nicht beeinflusst. | Aktualisiertes Verhalten der Optionsschalter für Lebensereignisse zum Aktivieren oder Deaktivieren, basierend auf abhängigen Optionen, gemäß der Tooltip-Dokumentation. |
| 565054 | Der Inhalt der Liste **Arbeitskräfte ohne Beschäftigung** kann nicht angezeigt werden, wenn **Erweiterter Zugriff** eingeschaltet ist. | Diese Version behebt das Problem, bei dem, wenn **Erweiterter Zugriff** eingeschaltet war, nur Systemadministratoren den Inhalt der Liste **Arbeitskräfte ohne Beschäftigung** sehen konnten. Da es sich bei dieser Korrektur um eine Sicherheitsänderung handelt, müssen Sie sich in der Änderungsverwaltung für diese Funktion entscheiden. Sobald die Funktion eingeschaltet ist, sehen die Rollen, die Zugriff auf das Formular haben, den Inhalt, auch wenn der erweiterte Zugriff eingeschaltet ist. Für weitere Informationen, siehe [Arbeitskräfte ohne Beschäftigung](hr-personnel-workers-without-employment.md). |
| 570586 | Die Validierung von Abwesenheitsanträgen schlägt fehl, wenn das Arbeitsverhältnis vor der letzten Transaktion für diese Arbeitskraft in allen Urlaubsplänen endet. | Nach Beendigung eines Arbeitsverhältnisses schlägt die Validierung von Urlaubsanträgen nicht mehr aufgrund von Transaktionen des Mitarbeiters fehl.|
| 570783 | Das Aktivieren und Deaktivieren von firmenübergreifendem Urlaub in den gemeinsamen Parametern von Human Resources ändert, was Mitarbeiter, die in einer einzelnen Firma beschäftigt sind, in den Urlaubsanträgen sehen. | Mitarbeiter, die in einer einzigen Firma beschäftigt sind, sehen keine Änderungen bei der Beantragung von Freizeit, wenn der Parameter aktiviert oder deaktiviert ist. |
| 572343 | Der erforderliche Grundcode wird nicht angezeigt, wenn die Funktion „Firmenübergreifende Urlaubsansicht“ aktiviert ist. | Wenn die Funktion „Firmenübergreifender Urlaub“ eingeschaltet ist, wird der Grund jetzt wie erwartet angezeigt. |
| 573676 | Kann **Periode** nicht zu **Leistungsmanagement > Links > Leistungspläne** hinzufügen. | Es wurde ein Fehler behoben, bei dem **Periode** nicht auf dem bestehenden **Versorgungsplan** Formular hinzugefügt oder aktualisiert werden konnte. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Verbesserungen des Workflows für Urlaub und Abwesenheit | [Erweiterungen im Workflow für Abwesenheit und Urlaub](https://go.microsoft.com/fwlink/?linkid=2147528) | [Arbeitsfreie Zeit anfordern](hr-employee-self-service-request-time-off.md)|
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Bald verfügbar

| Funktion | Informationen |
| --- | --- |
| Von einem Manager für seine Mitarbeiter eingegebene Qualifikationen können von einem Workflow automatisch genehmigt werden | Bald verfügbar. |
| Plattformupdate 10.0.18 (42) | Das Plattform-Update 10.0.18 wird voraussichtlich mit dem Service-Release am 17. Mai 2021 ausgerollt. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.18 der Apps für Finanzen und Betrieb (Mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Unterstützung von angepassten Feldern in den Berechtigungsregeln von Benefits Management  | [Angepasste Feldunterstützung für die Verarbeitung von Berechtigungen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
