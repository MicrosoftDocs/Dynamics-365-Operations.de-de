---
title: Power BI-Inhalt "Vergütung und Vorteile"
description: In diesem Thema wird der Power BI-Inhalt zu Vergütungen und Vorteilen beschrieben.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 96932c4ab32c004afb08fc9db2bf87bd5d5542d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174281"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Power BI-Inhalt "Vergütung und Vorteile"

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Power BI-Inhalt zu Vergütungen und Vorteilen beschrieben. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten sind
Nachdem Sie das Inhaltspaket mit Ihren Daten verbunden haben, zeigen die Berichte die Daten Ihrer Organisation an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Die Berichte, die im Paket enthalten sind, haben Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                     | Inhalt                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Vergütungs- und Benefits-Analyse. | Mitarbeiter mit Stunde- und Monatssalär nach Unternehmen, durchschnittlicher Stundenlohn, durchschnittlicher Lohn, Mitarbeiter nach Anstellungsart und Planregistrierung |
| Mitarbeitervergütungen          | Mitarbeiterregistrierung nach ausgewählten Vorteilen                                                                                               |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die Anwendungsdaten werden für die Berichte des Inhaltspakets „Vergütung und Vorteile“ verwendet. Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                            | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalendergegenkonten zu den Segmentberichten                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker |
| Workforce\_Company                | Unternehmen, nach denen Berichte gefiltert werden können                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_Compensation           | Lohnsatz und Häufigkeit im Zeitverlauf                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_CurrentCompensation    | Lohnsatz und Häufigkeit ab dem aktuellen Datum                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position |
| Workforce\_CurrentPosition        | Positionen nach dem aktuellen Datum, aufgerechtet nach Vollzeit (FTE), offen Positionen und offenen, zu besetzenden Positionen | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_Date                   | Tage, Wochen, Monate und Jahre                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | Geburtsdatum, Geschlecht, Familienstand und Nationalität                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_Employment             | Startdatum, Enddatum und Umbuchungsdatum                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_GeographicLocation     | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_Job                    | Funktion, Typ und Titel                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position |
| Workforce\_Performance            | Bewertung, Beschreibung und Bewertungsmodell                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_Position               | Abteilung, FTE, Position, Titel, Positionstyp                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Vorname, Nachname, vollständiger Name                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_Skill                  | Qualifikation, Fähigkeitstyp und Bewertung                                                                              | |
| Workforce\_TerminatedWorker       | Gesperrte Arbeitskräfte, Kündigungsdatum, Position, Titel und Aufgabenbereich                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Gültigkeitsdatum, Vergütungsoption, Vergütungsplan und Vergütungstyp                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_WorkerName             | Vorname, Nachname, vollständiger Name                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workforce\_WorkerTitle            | Titel- und Dienstalter                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend |
| Workorce\_WorkerTrend            | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |
