---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 5. Oktober 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 5. Oktober 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba24afd16a471abb36a6f7bc9a8610acec374190
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067970"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 5. Oktober 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4485.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Plattformupdate 10.0.21 (45) | -- | [Plattform-Updates für die Version 10.0.21 der Finanz- und Betriebs-Apps (Oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem | Description |
|---|---|---|
| 598896 | Der Mitarbeiterbetrag wird erst angezeigt, nachdem der Mitarbeiter die Registrierung abgeschlossen hat | Auf der Seite **Mitarbeiter-Self-Service** wurde der Mitarbeiterbetrag für die Leistung nicht angezeigt. Auf der Seite **Vorteile-Self-Service** wird der Mitarbeiterbetrag nun angezeigt.  |
| 613440 | Daten von **Datenmanagement** können nicht exportiert werden | Beim Exportieren von Daten für ein Projekt in **Datenmanagement** schlägt der Export unerwartet fehl. |
| 618327 | Geschlossene und zukünftige Perioden werden auf der Seite **Berichtsparameter** für die Vergütungsaufstellung angezeigt | Wenn Sie zu **Vergütungsaufstellung** unter **Mitarbeiter-Self-Service** navigieren, zeigt die **Berichtsparameter** die Inforegister **Einzuschließende Datensätze** und **Im Hintergrund ausführen** an. Diese Abschnitte wurden entfernt.|
| 618326 | Eine nicht korrekte **Berichtsparameter**-Seite wird unter **Mitarbeiter-Self-Service** für die Vergütungsaufstellung angezeigt| Wenn Sie zur Zielseite **Bericht zur Vergütungsaufstellung** navigieren, konnte der Benutzer Vergütungsplanperioden auswählen, die geschlossen sind oder in der Zukunft liegen, was zu einer leeren Seite führt. In der Liste sollte nur die aktuelle Vergütungsplanperiode angezeigt werden. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen über das Ein- und Ausschalten von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Benutzerdefinierte Felder in Eligibility |[Angepasste Feldunterstützung für die Verarbeitung von Berechtigungen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Verwenden von benutzerdefinierten Feldern in der Berechtigungsverarbeitung](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Vergütungsaufstellung |[Vergütungsaufstellung](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Leistungsnachweis](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Bekannte Probleme bei der Vergütungsaufstellung

| Problem | Beschreibung |
|---|---|
|Fehler beim Senden des Berichts per E-Mail über das **GER-Berichtsziel** | Die Vergütungsaufstellung kann so eingestellt werden, dass die E-Mail-Parameter auf der Seite **GER-Berichtsziele** verwendet werden. Beim Abschließen der Einrichtung und Drucken des Berichts erhält der Benutzer einen Formatierungsfehler und die Vergütungsaufstellung wird nicht gesendet.|

## <a name="feature-management-changes"></a>Funktionsverwaltung – Änderungen

| Funktion | Beschreibung |
|---|---|
|Ansicht für erweiterte Berichte für Leistungserfassungen | Diese Funktion wird in diesem Release standardmäßig aktiviert. |

## <a name="coming-soon"></a>Demnächst

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Informationen |
|---|---|
| Plattformupdate 10.0.22 (46) | Der Roll-out des Plattform-Updates 10.0.22 wird voraussichtlich mit dem Service-Release am 1. November 2021 beginnen. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.22 der Finanz- und Betriebs-Apps (November 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Siehe auch

[Neuerungen und Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

