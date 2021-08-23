---
title: Power BI-Inhalt zu Mitarbeiterkompetenzen und -entwicklung
description: In diesem Thema wird der Power BI-Inhalt zur Mitarbeiterkompetenzen und -entwicklung beschrieben.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 572f6bcfa202995d90080e1a31476122f7ec23d71214d5ff0dd44ed919859c57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726308"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI-Inhalt zu Mitarbeiterkompetenzen und -entwicklung

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Power BI-Inhalt zur Mitarbeiterkompetenzen und -entwicklung beschrieben. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten sind
Nachdem Sie das Inhaltspaket mit Ihren Daten verbunden haben, zeigen die Berichte die Daten Ihrer Organisation an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Die Berichte, die im Paket enthalten sind, haben Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                            | Inhalt                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetenzen und Entwicklung, Analysen | Teammitgliedsfähigkeitstypen und Teammitgliedsqualifikationen nach Typ |
| Qualifikationsprofil                     | Qualifikationsprofil für den ausgewählten Mitarbeiter.                |
| Qualifikationsanalyse                    | Qualifikation nach Typ und Bewertung                              |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Anwendungsdaten werden für die Berichte im „Mitarbeiterkompetenz und Entwicklung“-Inhaltspaket verwendet. Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                            | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalendergegenkonten zu den Segmentberichten                                                                          | |
| Workforce\_Company                | Unternehmen, nach denen Berichte gefiltert werden können                                                                             | |
| Workforce\_Compensation           | Lohnsatz und Häufigkeit im Zeitverlauf                                                                           | |
| Workforce\_CurrentCompensation    | Lohnsatz und Häufigkeit ab dem aktuellen Datum                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Positionen nach dem aktuellen Datum, aufgerechtet nach Vollzeit (FTE), offen Positionen und offenen, zu besetzenden Positionen | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Tage, Wochen, Monate und Jahre                                                                             | |
| Workforce\_Demographics           | Geburtsdatum, Geschlecht, Familienstand und Nationalität                                                   | |
| Workforce\_Employment             | Startdatum, Enddatum und Umbuchungsdatum                                                                  | |
| Workforce\_GeographicLocation     | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           | |
| Workforce\_Job                    | Funktion, Typ und Titel                                                                                  | |
| Workforce\_JobPreferredSkill      | Wichtigkeit, Bewertung, Qualifikationen und Fähigkeiten                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position |
| Workforce\_Performance            | Bewertung, Beschreibung und Bewertungsmodell                                                                      | |
| Workforce\_PersonSkill            | Ebene, Berichtsebene und Qualifikation                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Zertifiziert, Ebene, Datumsebene und Qualifikation                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Abteilung, FTE, Position, Titel, Positionstyp                                                        | |
| Workforce\_PositionTrend          | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Vorname, Nachname, vollständiger Name                                                                       | |
| Workforce\_Skill                  | Qualifikation, Fähigkeitstyp und Bewertung                                                                              | |
| Workforce\_TerminatedWorker       | Gesperrte Arbeitskräfte, Kündigungsdatum, Position, Titel und Aufgabenbereich                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Vorname, Nachname, vollständiger Name                                                                       | |
| Workforce\_WorkerTitle            | Titel- und Dienstalter                                                                                   | |
| Workorce\_WorkerTrend             | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]