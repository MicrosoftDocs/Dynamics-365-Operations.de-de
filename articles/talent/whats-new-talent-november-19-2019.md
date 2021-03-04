---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (19. November 2019)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Talent neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527143"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (19. November 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Talent sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2621. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Plattformupdate 31 für Finance and Operations Apps

Weitere Informationen finden Sie unter [Vorschau der Funktionen im Plattformupdate 31 für Finance and Operations-Apps (Januar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Arbeitsbereich Feature-Management (383856)

Der Arbeitsbereich **Funktionsverwaltung** bietet eine Liste der in jedem Release ausgelieferten Features. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen. Weitere Informationen zur Feature-Verwaltung finden Sie unter [Feature-Verwaltung Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich **Feature-Management** sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.
 
Manchmal ist ein integrales Feature standardmäßig eingeschaltet und kann nicht deaktiviert werden (z.B. das **Feature-Management** Arbeitsbereich).
 
Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich **Feature-Management** zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Meldung erscheint, wenn für eine Position (382887) eine abgebrochene Aktion vorliegt.

Die folgende Meldung erscheint nicht mehr, wenn Sie eine bestimmte Position auswählen und eine abgebrochene Aktion ist alles, was für die Position verfügbar ist: **Es wird eine unvollständige Aktion für die Position xxxxxxxx** durchgeführt.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>In der Lernanalyse zeigen der Kurstyp und der Status falsche Daten an (381151).

Die Veröffentlichung dieser Woche aktualisierte die Lernanalyse, um **Kurstyp** und **Status** korrekt anzuzeigen.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Die Personalnummer sollte im Formularbanner Neuer Mitarbeiter (383832) angezeigt werden.

Im Formular **Neuer Mitarbeiter** wird die **Personalnummer** nun im Banner zur schnellen Orientierung angezeigt.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Das Startdatum der Position bestimmt den Job-Datensatz, der beim Abrufen einer Vergütungsstufe während der Einstellung verwendet werden soll (350361).

In dieser Version bestimmt das **Startdatum der Vergütung** die dem neuen Job zugeordnete Stufe.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Benutzerdefinierte Auswahllistenfelder in der Positionstabelle werden nicht mit Common Data Service synchronisiert (387503).

Mit diesem Release werden Kommissionierlistenpositionen nun mit Common Data Service synchronisiert.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Die Adresseinheit des Arbeiters synchronisiert sich beim Importieren neuer Daten nicht mit Common Data Service (349673).

In der aktuellen Version werden die Adressdaten nun beim Einlesen neuer Daten mit Common Data Service synchronisiert.

## <a name="in-preview"></a>Vorschau

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.


[!INCLUDE[footer-include](../includes/footer-banner.md)]