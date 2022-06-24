---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources 26. Juli 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 26. Juli 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c7211135733f45a9841ae5a80607b01999d7c69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870928"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources 26. Juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4384.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Plattformupdate 10.0.20 | -- | [Plattform-Updates für die Version 10.0.20 der Finanz- und Betriebs-Apps (August 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 600422 | Die Prüfung der Lohnadresse zur Zahlungsbereitschaft schlägt fehl. | Die Überprüfung wurde aktualisiert, sodass nur noch eine Adresse des Typs „Wohnort für die Gehaltsabrechnung“ und nur eine Adresse des Typs „Arbeitsort für die Gehaltsabrechnung“ erforderlich sind. |
| 601226 | Datenintegrationsproblem: Das Exportprojekt für die Gehaltsabrechnungsintegration hat keine Option zum vollständigen Pushen | Die Integration der Gehaltsabrechnung in Ceridian DayForce erfolgte inkrementell anstelle eines vollständigen Pushs. Ceridian erfordert immer eine vollständige Aktualisierung. Dieses Problem ist jetzt behoben, die Entitäten im Datenexportprojekt werden nicht mehr auf inkrementelles Pushen umgestellt. |
| 602272 | Kacheln, die dem Employee-Self-Service-Arbeitsbereich hinzugefügt wurden, fehlen jetzt und Kacheln können nicht mehr hinzugefügt werden | Wir haben das Personalisierungsproblem für den Mitarbeiter Self Service behoben. Der Ansicht können neue Kacheln hinzugefügt werden und alle vorhandenen Personalisierungen sind für Benutzer sichtbar |
| 600711 | Auswahlfeld „Halbtagesdefinition“ für Ganztagesurlaubsanträge aktiviert | Dieses Problem ist jetzt behoben und das Feld für die Halbtagesdefinition wird nur aktiviert, wenn Mitarbeiter eine Urlaubsart mit aktivierter Halbtagsdefinition und einen halben Tag als Wert auswählen |
| 602208 | Abgrenzungssatzeinheiten zeigen Stunden statt Tage an | Dieses Problem ist jetzt behoben. Das Formular **Arbeitsfreie Zeit** die richtige Urlaubseinheit (Stunden oder Tage) für die Spalte **Abgrenzungssatz** an. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|
|  Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Mit dieser Version aktualisieren wir die Arbeitsbereichsansicht des Abwesenheitsmanagers. Weitere Informationen finden Sie unter [Rolle des Abwesenheitsmanagers konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Anhangsanforderung pro Urlaubsart konfigurieren | [Anhangsanforderung pro Urlaubsart konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Urlaubseinheiten pro Urlaubstyp konfigurieren | [Urlaubseinheiten pro Urlaubstyp konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Für Zahlung bereit](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Demnächst

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Welche Neuerungen oder Änderungen bietet Human Resources?](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
