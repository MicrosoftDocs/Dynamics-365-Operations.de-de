---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (10. September 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
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
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304578"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (10. September 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.138.0**

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Gestatten Sie bestimmte Zeit auf Freizeitanforderungen (halbe Tage)

Wenn Urlaub und Abwesenheit eingerichtet wird, sodass Freizeit in Tagen übermittelt wird, können Sie jetzt auch eine Halbtagsdefinition aktivieren. Wenn Benutzer Freizeitanforderungen senden, können Sie angeben, ob diese die erste oder zweite Hälfte vom freiem Tag anfordern.

Standardmäßig ist diese Option deaktiviert. Damit Mitarbeiter die erste oder zweite Hälfte von freiem Tag anfordern können, müssen Sie diese Option im Bereich **Urlaub und Abwesenheit** im Bereich Personalverwaltungsparameter aktivieren.

Das Sicherheitsrecht für diese Funktion wird in den Personalverwaltungsparametern verwaltet.

## <a name="validation-of-leave-and-absence-entries"></a>Prüfung von Urlaub- und Abwesenheitseinträgen

Abhängig davon, wie der Urlaub konfiguriert wird, erhalten Mitarbeiter eine Warnung, wenn sie versuchen, eine Freizeitanforderung zu senden, die länger ist als ihr Arbeitstag. Das bedeutet, sie werden gewarnt, wenn Sie versuchen, mehr als einen ganzen Tag Urlaub an einem bestimmten Datum eingeben möchten.

Diese Prüfung ist immer deaktiviert. Immer wenn Mitarbeiter den Tagschwellenwert überschreiten, der definiert wird, erhalten diese eine Warnung in ihrer Freizeitanforderung.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Zusätzliche Felder für Bedingungsanweisungen in den Workflows

Weitere Felder wurden den Bedingungsanweisungen und den Platzhaltern für mehrere Workflows in Core HR hinzugefügt.

Die folgenden Felder wurden der Kompensation, Kündigung und den Übergangsworkflow hinzugefügt:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Position
- Gewerkschaft
- Abteilung
- PositionType
- CompLocation
- Titel
- Stelle
- JobType
- JobFamily
- JobFunction

Die folgenden Felder wurden den Workflowpositionen hinzugefügt:

- Position
- Gewerkschaft
- Abteilung
- PositionType
- CompLocation
- Titel
- Stelle
- JobType
- JobFamily
- JobFunction

Felder in den Bedingungsanweisungen und in den Platzhalter sind für alle Benutzer verfügbar, die den Zugriff haben, den oben genannten Workflow zu konfigurieren.

## <a name="navigation-to-attract-from-personnel-management"></a>Navigation zu Atract von der Personalführung

In Personalführung, wenn Attract nicht eingerichtet wurde, weist der Abschnitt **Kandidaten zum Anstellen** an, mit Attract zu beginnen, statt die Nachricht anzuzeigen, "Keinen Inhalt zum Anzeigen gefunden".

## <a name="other-changes"></a>Andere Änderungen

Diese Version enthält eine Reihe zusätzlicher Fehlerkorrekturen:

- Wenn ein Auftragnehmer angestellt wird, soll die Registerkarte **Kompensation** nicht auf der Anforderungs-/Aktionsseite verfügbar sein.
- Während der Anforderungskündigungsprozesses können Sie nicht fortfahren, bis alle erforderlichen Felder Daten enthalten.
- Sortierreihenfolgen und Datumsanzeigenprobleme auf der Personalführungsanalyse sind nicht behoben worden.
