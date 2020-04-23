---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (18. Februar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077460"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (18. Februar 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.2903. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="platform-update-32"></a>Plattformupdate 32 

Plattform-Update 32 ist jetzt verfügbar. Weitere Informationen finden Sie unter [Was ist neu oder geändert in Plattform-Update 32 für Finance and Operations (Februar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Die Suchwerte werden bei der Änderung der Ansichtsoptionen in rationalisierter Mitarbeiterform gespeichert (383833)

Das neue Formular **Mitarbeiter** merkt sich jetzt Suchwerte, wenn Sie die Ansichtsoptionen ändern und Änderungen anwenden.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Vergütungsmanagement-Zusammenfassungskacheln in der Vorschaufunktion leiten in das falsche Formular um (401861)

Die Kacheln für die Verwaltung der festen und variablen Vergütung zeigen jetzt die richtigen Datensätze im neuen Formular **Arbeiter** an. Gilt nur für die rationalisierte Vorschaufunktion für Mitarbeiterformulare. Sie können diese Vorschaufunktion unter **Funktionsverwaltung** aktivieren. Weitere Informationen finden Sie unter [Funktionsverwaltung](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Leeres Statusfeld für einige Abwesenheitsantragssätze in Common Data Service (414915)

Diese Änderung korrigiert ein Problem in Common Data Service, wenn das Feld **Status** in einem Urlaubsantrag auf **Überprüfung** gesetzt ist. Die Common Data Service spiegelt nun den Status wider.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Qualifikationslückenanalyse nur für zugeordnete Stelle möglich (411390)

Sie können jetzt eine Analyse der Qualifikationslücke für jede in der Personalabteilung definierte Stelle durchführen.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Die Systemwährung wird in neuen Umgebungen nicht von Common Data Service mit der Personalabteilung synchronisiert (418011)

Die Systemwährung in Common Data Service kann nun mit der Personalabteilung synchronisiert werden.

## <a name="in-preview"></a>Vorschau

- [Vorschaufunktionen für Urlaub und Abwesenheit](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Vorschaufunktionen der Leistungsverwaltung](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Bald verfügbar

### <a name="updated-common-data-service-solution"></a>Aktualisierte Common Data Service-Lösung

Eine neue Common Data Service Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:

| Beschreibung | Änderung |
| ----------------------------------------- | --- |
| **Stelle/Position** Entitätsänderungen | **Kompensationsregion** hinzugefügt</br>**Finanzdimensionen** hinzugefügt |
| **Arbeitskraft** Entitätsänderungen | **Namensfolge** hinzugefügt</br>**Arbeitet von zu Hause** hinzugefügt</br>**Sprache** hinzugefügt</br>**Dienstalterdatum** hinzugefügt</br>**Jahrestag** hinzugefügt</br>**Ursprüngliches Einstellungsdatum** hinzugefügt |
| **Beschäftigung** Entitätsänderungen | **Finanzdimensionen** hinzugefügt</br>**Kündigungsgrund** hinzugefügt</br>**Kündigungsdatum** umbenannt von **Übergangsdatum**</br>**Probezeitdatum** hinzugefügt |
| **Arbeitskraftadresse** Entitätsänderungen | **Straße** hinzugefügt</br>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert |
| Neue variable Vergütung-Einrichtungsentitäten | **Plantyp für variable Vergütung**</br>**Plan für variable Vergütung**</br>**Übertragungsregeln**</br>**Variable Planstufe zur Vergütung** |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | **Arbeitkraftkalender-Entität** hinzugefügt |
| Neue **Lohnpositionsdetail** Entität | **Lohnpositionsdetail** hinzugefügt |
| Neue **Titel** Entität | **Titel** hinzugefügt. Die neue Einheit **Titel** wird in den Synchronisationsprozess zwischen Human Resources und Common Data Service einbezogen. Sie wird nicht zunächst von **Job-Position** oder **Job** Entitäten referenziert. |

## <a name="see-also"></a>Siehe auch

[Neuigkeiten oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)