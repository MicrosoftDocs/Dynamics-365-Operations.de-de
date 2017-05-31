---
title: Power BI Inhalt Mitarbeiterkompetenzen und -entwicklung
description: "In diesem Thema wird der Dynamics 365 for Operations - Power BI Inhalt Mitarbeiterkompetenz und Entwicklung beschrieben Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 770a832efe8ee2da44d65670b1818be4fcf4bcc0
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI Inhalt Mitarbeiterkompetenzen und -entwicklung

[!include[banner](../includes/banner.md)]


In diesem Thema wird der Dynamics 365 for Operations - Power BI Inhalt Mitarbeiterkompetenz und Entwicklung beschrieben Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen auf das Inhaltspaket
--------------------------

Sie finden das  Mitarbeiterkompetenz und -entwicklungs-Inhaltspaket in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie Inhalte herunterladen und mit Ihrem Microsoft Dynamics 365 for Operations verbinden, finden Sie unter [Power Bi Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten sind
Nachdem Sie das Inhaltspaket mit Ihren Dynamics 365 for Operations Daten verbunden haben, zeigen das Dashboard und die Berichte Ihre Organisationsdaten an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Die Berichte, die im Paket enthalten sind, haben Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                            | Inhalt                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetenzen und Entwicklung, Analysen | Teammitgliedsfähigkeitstypen und Teammitgliedsqualifikationen nach Typ |
| Qualifikationsprofil                     | Qualifikationsprofil für den ausgewählten Mitarbeiter.                |
| Qualifikationsanalyse                    | Qualifikation nach Typ und Bewertung                              |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 for Operations-Daten werden für die Berichte im Mitarbeiterkompetenz und -entwicklungs-Inhaltspaket verwendet. Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                            | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalendergegenkonten zu den Segmentberichten                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | Unternehmen, nach denen Berichte gefiltert werden können                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | Lohnsatz und Häufigkeit im Zeitverlauf                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | Lohnsatz und Häufigkeit ab dem aktuellen Datum                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Positionen nach dem aktuellen Datum, aufgerechtet nach Vollzeit (FTE), offen Positionen und offenen, zu besetzenden Positionen | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | Tage, Wochen, Monate und Jahre                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | Geburtsdatum, Geschlecht, Familienstand und Nationalität                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | Startdatum, Enddatum und Umbuchungsdatum                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | Funktion, Typ und Titel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Wichtigkeit, Bewertung, Qualifikationen und Fähigkeiten                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | Bewertung, Beschreibung und Bewertungsmodell                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | Ebene, Berichtsebene und Qualifikation                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | Zertifiziert, Ebene, Datumsebene und Qualifikation                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Abteilung, FTE, Position, Titel, Positionstyp                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Vorname, Nachname, vollständiger Name                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | Qualifikation, Fähigkeitstyp und Bewertung                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | Gesperrte Arbeitskräfte, Kündigungsdatum, Position, Titel und Aufgabenbereich                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | Vorname, Nachname, vollständiger Name                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | Titel- und Dienstalter                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhaltspaket verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die  CompetenciesandDevelopment.pbix Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um das Inhaltspaket zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





