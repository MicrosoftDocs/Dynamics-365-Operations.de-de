---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (10. September 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 14e3482f366319851bed84b6cdd6135f0bcd1e80
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897331"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent (10. September 2019)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 for Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="candidate-e-mail-login"></a>Kandidaten-E-mail-Anmeldung

Kandidaten können nun jede E-Mail-Adresse verwenden, um ein Konto und eine Anmeldung bei einer Talent-Website mit Stellenangeboten zu erstellen, um sich auf Stellen zu bewerben und den Bewerbungsstatus zu suchen. Dies erfolgt zusätzlich zur Anmeldung an der Talent-Website mit Stellenangeboten über Sozialkonten oder die Organisationsanmeldeinformationen.

### <a name="job-activation-and-posting"></a>Stellenaktivierung und Buchung

Wir haben einige Änderungen an der Stellenaktivierung und Buchung vorgenommen. Sie müssen Stellen aktivieren, bevor Sie sie auf einer Talent-Website mit Stellenangeboten oder externen Stellenbörsen veröffentlichen, einschließlich LinkedIn oder Broadbean.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2482. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Sie können Vorschaufunktionen in der Sandbox- und Testumgebung aktivieren

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp Produktion oder Sandkasten ist. Die Instanzen vom Sandkasten Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp Sandkasten aktualisiert werden soll, wenden Sie sich an den Support, um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](./provisioning-talent.md).

### <a name="platform-update-29"></a>Plattformupdate 29

Zusätzliche Details zur Plattformaktualisierung 29 finden Sie unter [Vorschaufunktionen in Dynamics 365 for Finance and Operations Plattformaktualisierung 29 (Oktober 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Neue Stellenbasisentität verfügbar im Datenverwaltungsframework (347202)

Mit dieser Version wurde eine neue Basisstellenentität für das Importieren/Exportieren von Daten verfügbar gemacht. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Erweiterte Arbeitskraft-Sicherheitsrichtlinie zeigt falsche Positionen in der Positions-Hierarchie (354868)

Mit dieser Version werden Positionen nicht mehr als offen mit einer leeren Arbeitskraft angezeigt, wenn Benutzer eingeschränkten Zugriff haben.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Das Schließfeld des Stellenformulars wird in bestimmten Situationen nicht geschlossen (342467)

Diese Version enthält eine Änderung, die das Arbeitsformular zum Schließen in allen Szenarien zulässig macht.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Neuer Fall im Mitarbeiterdatensatz ist gesperrt für Personalverwaltungsmanagerrolle (337111 )

Mit dieser Änderung wird das Anfragemanagementformular nicht mehr gesperrt, sofern vom Mitarbeiterformular zugegriffen wird.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Das Beschäftigungsenddatum endet immer bis 23:59:59 (351492)

Mit dieser Änderung können Sie das Beschäftigungsdatum auf eine andere Zeit als 23:59 Uhr ändern, wenn ein Beschäftigungsverhältnis manuell beendet wird.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Festlegen des Ablaufdatums in einem Einkommenscode über die Datenverwaltung nicht möglich (336604)

In dieser Version können Sie Einkommenscodes einrichten, die durch die **PayrollWorkerPositionEarningCodeEntity**-Entität ablaufen.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Analytischer Bericht zur Mitarbeiterentwicklung zeigt keine Daten an (348737)

In der Version dieser Woche wurde die Analyse für Mitarbeiterfähigkeiten aktualisiert, um genaue Berichte bereitzustellen.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Einstellungsbedingungsdatum/-uhrzeit standardmäßig nicht am Beginn des Tages (349101)

Mit dieser Änderung liegt das Startdatum/Zeit jetzt am Tagesbeginn und Enddatum/Zeit am Tagesende.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Beim Ändern des Beschäftigungsenddatums auf dem Arbeitskraftaktivitätsformular wird ein Fehler angezeigt (354092) 

Diese Änderung behebt ein Problem beim Ändern der Beschäftigung als Teil der Arbeitskraftaktivität .

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Onboarding-Checklisten auf mehrere Unternehmen anwenden (338433)

Diese Version enthält nun die Möglichkeit, Checklisten für Mitarbeiter anzuwenden, die in anderen juristischen Entitäten angestellt sind als der angemeldeten juristischen Entität.

## <a name="in-preview"></a>Vorschau

### <a name="streamlined-employee-entry-and-navigation"></a>Fortschrittlicher Mitarbeitereintrag und ‑Navigation

Diese Funktionalität ist in der Sandboxumgebung verfügbar. Um diese Funktion zu aktivieren, navigieren Sie zu **> Systemverwaltung > Verknüpfung > Einstellungen > Systemparameter- > Vorschaufunktionen**. Wählen Sie **Verbessertes Arbeitskraftformular und Navigation** aus. Dies aktiviert diese Änderungen für alle Benutzer. Sie können diese Option jederzeit deaktivieren.

Weitere Informationen finden Sie unter [Fortschrittlicher Mitarbeitereintrag und -Navigation](./streamlined-employee-entry.md).
