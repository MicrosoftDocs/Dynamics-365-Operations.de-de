---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 5. Oktober 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 5. Oktober 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 10/05/2021
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
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 206c7f590b495278b7899271db0e83b3a4da3edc
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641429"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 5. Oktober 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu sind, geändert wurden oder demnächst erscheinen.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4485.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Plattformupdate 10.0.21 (45) | -- | [Plattform-Updates für Version 10.0.21 von Finance and Operations-Apps (Oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Möglicherweise aktualisieren wir dieses Thema, um Fehlerkorrekturen einzubeziehen, die es in den Build geschafft haben, nachdem dieses Thema ursprünglich veröffentlicht wurde.

| Problemnummer | Problem | Beschreibung |
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
| Plattformupdate 10.0.22 (46) | Der Roll-out des Plattform-Updates 10.0.22 wird voraussichtlich mit dem Service-Release am 1. November 2021 beginnen. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.22 von Finance and Operations-Apps (November 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Siehe auch

[Neuerungen und Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]