---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (7. Februar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 07. Februar 2020 neu sind oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
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
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fac6e34db10efb047b4cb0fc3c7752330e5bcf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526943"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (7. Februar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.2835. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Beim Lernen in Analytics wird der Kurs nicht angezeigt, wenn das Klassenzimmer leer ist (388289)

Auf der Learning Analytics-Seite wird nun der Kurs angezeigt, wenn der Klassenraum leer ist.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Positionssuche berücksichtigt nicht die Zeitzone (405344)

Die Suche nach offenen Positionen berücksichtigt jetzt die Zeitzone, wenn überprüft wird, ob eine Position offen ist.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Die Ansicht für die Analyse des aktuellen Saldos wird nach Übermittlung von Abwesenheitsanträgen nicht mit dem korrekten aktuellen Urlaubssaldo aktualisiert (409756)

Der aktuelle Kontostand enthält jetzt die eingereichten Freizeitanträge.

## <a name="in-preview"></a>Vorschau

Die folgenden Vorschaufunktionen sind am 3. Februar 2020 verfügbar:

- **Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Vorschaufunktion für die Leistungsverwaltung** - Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über die Leistungsverwaltung](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Bald verfügbar

### <a name="platform-update-32"></a>Plattformupdate 32 

Das Plattform-Update 32 wird in Kürze verfügbar sein. [Weitere Informationen zu Platform Update 32 finden Sie hier](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-common-data-service-solution"></a>Aktualisierte Common Data Service Lösung

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]