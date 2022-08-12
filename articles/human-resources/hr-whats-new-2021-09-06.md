---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 6. September 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 6. September 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 03f832a6a3a099c472b781f7e2258ac575127101
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069999"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 6. September 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4443.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | In diesem Release aktualisieren wir die Ansicht des Arbeitsbereichs des Abwesenheitsmanagers. Weitere Informationen finden Sie unter [Rolle des Abwesenheitsmanagers konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Anhangsanforderung pro Urlaubsart konfigurieren | [Anhangsanforderung pro Urlaubsart konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Urlaubseinheiten pro Urlaubstyp konfigurieren | [Urlaubseinheiten pro Urlaubstyp konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem | Description |
|---|---|---|
| 610128 | Fehler beim Veröffentlichen von Daten bei Verwendung der HcmDiscussionOverallCommentEntity | Wenn Daten aus einer Excel-Arbeitsmappe in der HcmDiscussionOverralCommentEntity-Entität veröffentlicht werden, tritt der folgende Fehler auf: „Datenquellendatensatz des Typs HcmTopicOverrall kann nicht gefunden werden.“ |
| 589073 | EEO-1-Bericht zählt „Nicht spezifisch“ und leere Werte für das Feld **Geschlecht** als den Wert „Weiblich“. | Wenn **Männlich** für das Feld **Geschlecht** nicht angegeben ist, generiert der EEO-1-Bericht den Standardwert **Weiblich**. |
| 589617 | Die Karte „Freizeitsalden“ sowie die Salden „Verfügbar zum Kaufen“ und „Verfügbar zum Verkaufen“ werden nicht angezeigt, wenn Benutzerrollen auf eine bestimmte juristische Person beschränkt sind. | Wenn der Benutzer (Mitarbeiterrolle) auf eine bestimmte juristische Person beschränkt ist, werden Salden auf der Karte **Freizeitsalden** und in den Feldern **Verfügbar zum Kaufen** und **Verfügbar zum Verkaufen** nicht korrekt angezeigt. |
| 604310 | Die Registerkarte „Abwesenheitsmanager“ sollte ausgeblendet werden, wenn dem Benutzer keine Abwesenheitshierarchie zugewiesen ist. | Für eine bestimmte juristische Person sollte die Registerkarte **Abwesenheitsmanager** im Self-Service-Portal ausgeblendet werden, es sei denn, der firmenübergreifende Parameter ist aktiviert und dem Benutzer ist mindestens eine Abwesenheitshierarchie zugeordnet. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen über das Ein- und Ausschalten von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md) |
| Arbeitsbereich „Vorteilsverwaltung“ | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Für Zahlung bereit](/dynamics365/human-resources/hr-compensation-payroll) |
| Benutzerdefinierte Felder in Eligibility |[Angepasste Feldunterstützung für die Verarbeitung von Berechtigungen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Verwenden von benutzerdefinierten Feldern in der Berechtigungsverarbeitung](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Demnächst

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Informationen |
|---|---|
| Plattformupdate 10.0.21 (45) | Der Roll-out des Plattform-Updates 10.0.21 wird voraussichtlich mit dem Service-Release am 4. Oktober 2021 beginnen. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.21 der Finanz- und Betriebs-Apps (Oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Vergütungsaufstellung | Leistungsnachweis zum Anzeigen der aktuellen Leistungsauswahl eines Mitarbeiters Weitere Informationen finden Sie unter [Leistungsnachweise](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) im Dokument „Veröffentlichungszyklus“. |

## <a name="see-also"></a>Siehe auch

[Welche Neuerungen oder Änderungen bietet Human Resources?](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

