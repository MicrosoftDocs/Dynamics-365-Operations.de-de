---
title: Was ist neu oder geändert in Dynamics 365 Human Resources 23. August 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 23. August 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c9ee0206bd77a8a2ec42501d64e83077baef09
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441674"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Was ist neu oder geändert in Dynamics 365 Human Resources 23. August 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu sind, geändert wurden oder demnächst erscheinen.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4419.

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Möglicherweise aktualisieren wir dieses Thema, um Fehlerkorrekturen einzubeziehen, die es in den Build geschafft haben, nachdem dieses Thema ursprünglich veröffentlicht wurde.

| Problemnummer | Problem | Beschreibung |
| --- | --- | --- |
| 594066 | Kontaktinformationen können nicht gelöscht werden | Wenn Sie einen Datensatz mit Kontaktinformationen für einen Mitarbeiter löschen möchten, wird stattdessen ein anderer Datensatz mit Kontaktinformationen als der ausgewählte Datensatz gelöscht. |
| 611339 | Das Hinzufügen einer Personalisierung führt dazu, dass das Bankkonto den Filter ignoriert und den ersten Datensatz abruft | Das Hinzufügen einer Personalisierung führt dazu, dass die Bankkontoliste eine Personalisierungsabfrage ausführt, nachdem die Datenquellenabfrage ausgeführt wurde. Dies führt dazu, dass die Abfrage den obersten Datensatz abruft, unabhängig von der Arbeitskraft, für die die Details angezeigt werden. |
| 591806 | Aufgaben zum Onboarding-Fälligkeitsdatum werden falsch berechnet | Fälligkeitsdaten werden unter folgenden Bedingungen falsch berechnet: Die erstellten Checklisten verwenden einen Kalender mit einem erweiterten Zeitbereich (z. B. von 2005 bis 2050) und die Benutzereinstellungen verwenden eine andere Zeitzone als die Central Standard Time. |   
| 592749 | Urlaubssaldo im **Mitarbeiter-Self-Service** ist falsch angegeben | Wenn der Mitarbeiter in mehr als einer juristischen Person beschäftigt ist und die firmenübergreifende Urlaubsansicht aktiviert ist, ist der Urlaubssaldo möglicherweise falsch. |
| 603133 | Unerwartete Warnung beim Anfordern von Freizeit | Wenn Sie Freizeit anfordern und das Felder **Halber Tag** vor dem Feld **Betrag** ausfüllen, führt dies zu einer unerwarteten Warnung. |
| 606546 | Auswahlfeld in „Genehmigte Freizeit“ nicht sichtbar | Das Kontrollkästchen zum Auswählen mehrerer genehmigter Abwesenheitsanfragen war nicht sichtbar. |
| 597059 | Arbeitskraft nicht sichtbar in **Urlaubs‑ und Abwesenheitskalender des Unternehmens** | Eine Arbeitskraft ist im **Urlaubs‑ und Abwesenheitskalender des Unternehmens** nicht sichtbar, wenn der angewendete Datumsbereich einen Tag umfasst, für den ihr ein Urlaubsantrag verweigert wurde. |


## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen über das Ein- und Ausschalten von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|
| Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | In diesem Release aktualisieren wir die Ansicht des Arbeitsbereichs des Abwesenheitsmanagers. Weitere Informationen finden Sie unter [Rolle des Abwesenheitsmanagers konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Anhangsanforderung pro Urlaubsart konfigurieren | [Anhangsanforderung pro Urlaubsart konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Urlaubseinheiten pro Urlaubstyp konfigurieren | [Urlaubseinheiten pro Urlaubstyp konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Für Zahlung bereit](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Demnächst

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Informationen |
| --- | --- |
| Plattformupdate 10.0.21 (45) | Der Roll-out des Plattform-Updates 10.0.21 wird voraussichtlich mit dem Service-Release am 4. Oktober 2021 beginnen. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.21 von Finance and Operations-Apps (Oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Siehe auch

[Welche Neuerungen oder Änderungen bietet Human Resources?](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
