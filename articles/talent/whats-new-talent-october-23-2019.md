---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (23. Oktober 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 27cb4a7c125cb2b330dff083c8ed0c1ee89c0e7e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528002"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (23. Oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2569. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Plattformupdate 30 für Finance and Operations Apps

Weitere Informationen finden Sie unter [Neues oder Änderungen im Plattformupdate 30 für Finance and Operations Apps (November 2019)](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Entfernen der Vorschaufunktion für Vorteile eines offenen Registrierungsprozesses

In Verbindung mit unserer Ankündigung im Blogbeitrag zum Thema [„Strategische Investitionen in Core HR steigern die operative Exzellenz“](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) entfernt Microsoft die Funktion für Vorteile eines offenen Registrierungsprozesses aus der öffentlichen Vorschau ab dem 18. Oktober 2019. Stattdessen werden neue Funktionen in der Zukunft verwendet. Der Produktionsgebrauch von Vorteilen eines offenen Registrierungsprozesses, der gerade in der öffentlichen Vorschau enthalten ist, wird nicht unterstützt.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Fehler bei der zweiten Auswahl des Landes/der im Arbeitskraftformular (350294)

In der Version dieser Woche wurde das Problem behoben, das auftrat wenn ein Land/eine Region im Formular **Arbeitskraft** ausgewählt wurde.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Als Finanzdimensionswerte wird standardmäßig das Kombinationsanzeigefeld verwendet, wenn „Keine manuellen Eingaben zulassen“ auf true festgelegt ist (340097)

Mit dieser Änderung zeigt das System ordnungsgemäß standardmäßig den Dimensionswert im Feld **Kombinationsanzeige** an, wenn Finanzdimensionen eingerichtet werden und die Option verwendet wird, manuelle Eingaben nicht zuzulassen.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Neue Beziehungstypen sollen zur Beziehungssuche im Formular der persönlichen Kontakten hinzugefügt werden (347691)

Diese Version enthält neue Funktionen, um neue Beziehungstypen in der Tabelle **Beziehungstypen** hinzuzufügen und diese Änderungen in der Beziehungssuche für persönliche Kontakte widerzuspiegeln.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Zusätzliche Listenwerte in benutzerdefinierten Feldern werden in Common Data Service nicht angezeigt (379599)

In der Version dieser Woche werden die neuen Kommissionierlistenwerte nun angezeigt, nachdem Änderungen der Entität angewendet wurden, wenn ein neuer Listenwert einem vorhandenen benutzerdefinierten Feld hinzufügt wird, das bereits mit Common Data Service synchronisiert wurde.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Auf der Seite „Einstellungsbedingungen“ werden die Einstellungsbedingungen aller Mitarbeiter angezeigt, nachdem „In Excel öffnen“ ausgewählt wurde (348073)

Ab dieser Version werden nur die Einstellungsbedingungen der ausgewählten Mitarbeiter in Excel geöffnet. Die gesamte Unternehmenssicherheit wird auch berücksichtigt.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Die Zuordnung zwischen der Ferieneinheit Arbeitskalender und der Einheit Arbeitskalender fehlt in Common Data Service (324178).

Diese Beziehung wurde in der Version hinzugefügt. Diese Änderung ermöglicht, dass Arbeitstage eines Mitarbeiters in PowerApps angezeigt werden. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Fehler bei Verwendung von Mitarbeiter-Self-Service-Workflow mit konfigurierbaren Hierarchien (370132)

In dieser Version ist besseres Messaging dazu verfügbar, wie Workflows mithilfe der konfigurierbaren Hierarchien konfiguriert werden. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>System ermöglicht das Erstellen neuer Positionen, bei denen das Datum „Für eine Zuweisung verfügbar“ vor dem Aktivierungsdatum liegt (340103)

Diese Änderung zeigt eine Warnung an, wenn das Datum **Für eine Zuweisung verfügbar** vor dem Datum **Aktivierung** der Position liegt.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.

### <a name="feature-management-workspace"></a>Arbeitsbereich für die Funktionsverwaltung

Funktionen werden in jeder Version hinzugefügt und aktualisiert. Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jeder Version geliefert wurden. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.

Weitere Informationen über die Änderungen, die in der Funktionsverwaltung enthalten sind, finden Sie unter [Überblick über die Funktionsverwaltung](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
