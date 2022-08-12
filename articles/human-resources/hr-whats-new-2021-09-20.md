---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 20. September 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 20. September 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59f1b0e3c35d1dce045b4a3932d99fab398e5516
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069755"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 20. September 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4464.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md) |
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Für Zahlung bereit](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem | Description |
|---|---|---|
| 619774 | Das Bearbeiten der Adressbeschreibung wird nicht mit Dataverse in Echtzeit synchronisiert. | Beim Bearbeiten der Beschreibung für eine dresse der Arbeitskraft wird die aktualisierte Beschreibung nicht in Echtzeit mit Dataverse synchronisiert. Das Abonnement in der Tabelle **Logistikstandort** wurde aktualisiert, um ein Update zu senden. |
| 614603| Auf der Seite **Arbeitskraft** tritt ein Fehler auf, wenn der Parameter **Personalaktivitäten der Arbeitskraft** ist nicht ausgewählt. | Wenn Sie einen neuen Mitarbeiter einstellen oder zur Seite **Arbeitskraft** navigieren, wird der Fehler „Das Feld **Persönlicher Aktivitätstyp** muss ausgefüllt werden“ auch dann angezeigt, wenn die Option **Personalaktivitäten** deaktiviert ist. |
| 615367 | Die Registerkarte **Genehmigte Freizeit** zeigt eine Warnung an und wird falsch angezeigt. | Wenn die Urlaubseinheit auf **Tage** eingestellt ist, bevor die Funktion **Urlaubseinheiten pro Urlaubsart konfigurieren** aktiviert wird, zeigt die Registerkarte **Genehmigte Freizeit** eine ungültige Warnung und falsche Spalten an. |


## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen über das Ein- und Ausschalten von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Benutzerdefinierte Felder in Eligibility |[Angepasste Feldunterstützung für die Verarbeitung von Berechtigungen](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Verwenden von benutzerdefinierten Feldern in der Berechtigungsverarbeitung](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Vergütungsaufstellung |[Vergütungsaufstellung](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Vergütungsaufstellung](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Bekannte Probleme bei der Vergütungsaufstellung

| Problem | Beschreibung |
|---|---|
| Die Seite **Berichtsparameter** unter **Mitarbeiter-Self-Service** für die Vergütungsaufstellung ist nicht korrekt. | Wenn Sie zu **Vergütungsaufstellung** unter **Mitarbeiter-Self-Service** navigieren, zeigt die **Berichtsparameter** die Inforegister **Einzuschließende Datensätze** und **Im Hintergrund ausführen** an.  Diese müssen entfernt werden. |
| Geschlossene und zukünftige Perioden werden auf der Seite **Berichtsparameter** für die Vergütungsaufstellung angezeigt. | Wenn Sie zur Zielseite **Bericht zur Vergütungsaufstellung** navigieren, kann der Benutzer Vergütungsplanperioden auswählen, die geschlossen sind oder in der Zukunft liegen, was zu einer leeren Seite führt. In der Liste sollte nur die aktuelle Vergütungsplanperiode angezeigt werden. |
|Fehler beim Senden des Berichts per E-Mail über das GER-Berichtsziel. | Die Vergütungsaufstellung kann so eingestellt werden, dass E-Mail-Parameter innerhalb der Seite **GER-Berichtsziele** verwendet werden. Beim Abschließen der Einrichtung und Drucken des Berichts erhält der Benutzer einen Formatierungsfehler und die Vergütungsaufstellung wird nicht gesendet.|


## <a name="coming-soon"></a>Demnächst

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Informationen |
|---|---|
| Plattformupdate 10.0.21 (45) | Der Roll-out des Plattform-Updates 10.0.21 wird voraussichtlich mit dem Service-Release am 4. Oktober 2021 beginnen. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.21 der Finanz- und Betriebs-Apps (Oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Ansicht für erweiterte Berichtende für Leistungserfassungen | Diese Funktion wird beim nächsten Rollout standardmäßig aktiviert. |


## <a name="see-also"></a>Siehe auch

[Neuerungen und Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

