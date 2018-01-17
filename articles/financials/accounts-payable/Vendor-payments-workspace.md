---
title: "Arbeitsbereich für Kreditorenzahlungen"
description: "Dieses Thema enthält Informationen zum Arbeitsbereich für Kreditorenzahlungen. Im Arbeitsbereich für Kreditorenzahlungen werden Informationen angezeigt, die zum Verarbeiten von Kreditorenzahlungen dienen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.assetid: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: fa8ddf52d34c3662e120509156ab0b343bb4cc16
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-payments-workspace"></a>Arbeitsbereich für Kreditorenzahlungen

[!include[banner](../includes/banner.md)]

Im Arbeitsbereich für **Kreditorenzahlungen** werden Informationen angezeigt, die zum Verarbeiten von Kreditorenzahlungen dienen. Der Arbeitsbereich umfasst eine Ansicht **meine Arbeit** und eine Seite **Analyse**. Die Ansicht **Meine Arbeit** zeigt zusammenfassende Kacheln, Lieferantentransaktionsrater und zugehörige Kreditoreninformationen. Die Seite **Analyse** verwendet die Funktionen von Microsoft Power BI, um grafische Elemente hinsichtlich der Lieferantenzahlungen anzuzeigen.

## <a name="my-work-view"></a>Ansicht "Meine Arbeit"

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die Kacheln im Abschnitt **Zusammenfassung** geben eine Übersicht des Status Ihrer Zahlungsinformationen. Sie können Zahlungserfassungen sehen, die noch nicht gebucht sind, Rechnungen, die überfällig sind, alle Kreditoren und gesperrte Kreditoren finden. Im Abschnitt **Zusammenfassung** können Sie einen neuen Zahlungslauf erstellen.

Die Informationen im Abschnitt **Zusammenfassung** sind für das Unternehmen, bei dem Sie angemeldet sind.

### <a name="vendor-transactions-grids"></a>Lieferantentransaktionsraster

Der Bereich **Kreditorenbuchungen** enthält Raster, die die Rechnungen anzeigen, die überfällig sind und Zahlungen, die noch nicht ausgeglichen sind. Im Raster **Rechnungen überfällig** können Sie die den Zahlungsverlauf für eine ausgewählte Rechnung anzeigen. Im Raster **Rechnungen nicht bezahlt** können Sie die den Zahlungsverlauf für eine ausgewählte Rechnung anzeigen und die Rechnung bezahlen.

Mitarbeiter für zentralisierte Zahlungen können einen Filter verwenden, der oben auf jedem Raster erscheint und ein Unternehmen auswählen. Das Raster wird dann gefiltert, so dass lediglich die Unternehmen angezeigt werden, die in der zentralisierten Organisationshierarchie definiert sind, und die der Mitarbeiter für die zentralisierte Zahlung sehen darf.

Mit der Registerkarte **Transaktionen suchen** im Abschnitt **Kreditorenbuchungen** können Sie nach einer Kreditorenbuchung suchen.

### <a name="related-information"></a>Zugehörige Informationen

Sie können den Bericht **Kreditorenfälligkeit** und **Zahlungsüberblick pro Datum** anzeigen, indem Sie die Links im Abschnitt **Zugehörige Informationen** des Arbeitsbereichs verwenden.

## <a name="analytics-page"></a>Analysenseite

Die Seite **Analyse** enthält wichtige Metrik, wie beispielsweise Kreditorenrechnungen, die überfällig sind und Kreditorenrechnungen, die fällig werden. Diese Seite enthält neun Berichtsseiten. Eine Seite enthält einen Überblick und die anderen acht Seiten enthalten Details zu Kreditorenkontenzahlungen.

Die folgende Tabelle enthält die Visualisierungen, die für jede Berichtsseite verfügbar ist.

| Berichtsseiten | Darstellung |
|-------------|---------------|
| Gebühren für Kreditorenzahlung anzeigen | <ul><li>Überfällige Rechnungen</li><li>Heute fällige Kreditorenrechnungen</li><li>Angewendete Rabatte und verlorene Rabatte</li><li>Fällig werdende Rechnungen nach Skontodatum</li><li>Fällig werdende Rechnungen nach Skontodatum</li><li>Zu spät bezahlte Rechnungen und pünktlich bezahlte Rechnungen</li><li>Workflow für Zuweisungen</li><li>Kreditoren-/Händlersaldo</li><li>Offene Rechnungen mit Zahlungssperre</li></ul> |
| Überfällige Rechnungen | <ul><li>Überfällige Rechnungen</li><li>Details überfälliger Kreditorenrechnungen</li><li>Summe offener Rechnungen</li><li>Überfällige Rechnungen nach Kreditorengruppe</li><li>Überfällige Rechnungen pro Unternehmen</li></ul> |
| Heute fällige Kreditorenrechnungen | <ul><li>Heute fällige Kreditorenrechnungen</li><li>Details von heute fälligen Rechnungen</li><li>Heute fällige Rechnungen pro Unternehmen</li><li>Heute fällige Rechnungen nach Kreditorengruppe</li></ul> |
| Angewendete Rabatte und verlorene Rabatte | <ul><li>Angewendete Rabatte und verlorener Rabatt</li><li>Details angewendeter Rabatte und verlorener Rabatt</li><li>Angewendete Rabatte und verlorener Rabatt nach Unternehmen</li><li>Angewendete Rabatte und verlorener Rabatt nach Kreditorengruppe</li></ul> |
| Rechnungen, die in der Zukunft fällig sind | <ul><li>Rechnungen, die in der Zukunft fällig sind</li><li>Details der Rechnungen, die in der Zukunft fällig sind</li><li>Rechnungen, die in der Zukunft fällig sind pro Unternehmen</li><li>Rechnungen, die in der Zukunft fällig sind nach Kreditorengruppe</li><li>Fällig werdende Rechnungen nach Skontodatum</li><li>Fällig werdende Rechnungen nach Skontodatum</li></ul> |
| Zu spät bezahlte Rechnungen | <ul><li>Nach dem Fälligkeitsdatum bezahlte Rechnungen</li><li>Details von nach dem Fälligkeitsdatum bezahlten Rechnungen</li><li>Details von nach dem Fälligkeitsdatum bezahlten Rechnungen pro Unternehmen</li><li>Details von nach dem Fälligkeitsdatum bezahlten Rechnungen pro Unternehmensgruppe</li><li>Zu spät bezahlte Rechnungen und pünktlich bezahlte Rechnungen</li></ul> |
| Zahlungsworkflow | <ul><li>Kreditorenzahlungsworkflowinstanzen</li><li>Kreditorenzahlungsworkflowinstanzen pro Genehmiger</li><li>Kreditorenzahlungsworkflowinstanzen pro Unternehmen</li><li>Durchschnittliche Tage im Arbeitsplan nach Genehmiger</li></ul> |
| Kreditoren-/Händlersaldo | <ul><li>Kreditoren-/Händlersaldo</li><li>Kreditoren-/Händlersaldo nach Unternehmen</li><li>Kreditoren-/Händlersaldo-Details</li></ul> |
| Rechnungen mit Zahlungssperre | <ul><li>Rechnungen mit Zahlungssperre</li><li>Rechnungen mit Zahlungssperre, Details</li><li>Rechnungen mit Zahlungssperre nach Unternehmen</li><li>Rechnungen mit Zahlungssperre nach Lieferantengruppe</li></ul> |

