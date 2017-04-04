---
title: Mitarbeiter-Kompetenzen und Entwicklungs-Energie BIinhalt
description: "In diesem Thema wird das Dynamics 365 - Mitarbeiter-Kompetenzen für Arbeitsgänge und Entwicklungs-Energie BIinhalt. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Mitarbeiter-Kompetenzen und Entwicklungs-Energie BIinhalt

In diesem Thema wird das Dynamics 365 - Mitarbeiter-Kompetenzen für Arbeitsgänge und Entwicklungs-Energie BIinhalt. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen des das Content Packs
--------------------------

Sie können das Inhaltstext Pack der Mitarbeiter- und der Entwicklung in der Bibliothek der kommenden Anlagen in den Microsoft Dynamics Lifecycle Services (LCS) suchen. Weitere Informationen dazu, wie das herunterlädt Inhaltstext Pack und es für Ihr Microsoft Dynamics 365 für Arbeitsgänge, Daten finden Sie in BIinhalt herstellt [Energie Kreditbriefen von Microsoft und von den Partnern]( power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten inhaltliche sind
Nachdem das Inhaltstext Pack für Ihr Dynamics 365 für Arbeitsgangsdaten verbunden wurde, zeigen die Berichte die Daten der Organisation an. Wenn Sie nicht Microsoft-Energie vor BI verwendet haben, können Sie dieser auf mehr zu erfahren [geführt, Seite für Leistung BI] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) erfahrend. Die Berichte, die im Paket enthalten inhaltliche werden, weisen den Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                            | Inhalt                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetenz-u. Entwicklungs-Analyse | Teammitgliedsfähigkeitstypen und Teammitgliedsqualifikationen nach Typ |
| Qualifikationsprofil                     | Fähigkeitsprofil für den ausgewählten Mitarbeiter                |
| Qualifikationsanalyse                    | Qualifikationen nach Typ und Bewertung                              |

Sie können die und die Kacheln Diagramme in diesen Erklärungen Stift und die Diagramme und die Kacheln das Dashboard filtern. Weitere Informationen dazu, wie und Energie Stift in finden Sie BI, gefiltert [Dient zum Erstellen und Konfigurieren eines Dashboard] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 für Arbeitsgangsdaten wird verwendet, um die Berichte im das Content Pack der Mitarbeiter- auszufüllen und der Entwicklung. Die folgende Tabelle enthält die von Entitäten, dass das Inhaltstext Pack auf Grundlage war.

| Entität                            | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_CalendarOffset Belegschaft         | Kalendergegenkonten zu den Segmentberichten                                                                          |                                                                                                                                                                                                                                                                                                         |
| \_Belegschafts Unternehmen                | Unternehmen, z von Berichten nach filtern                                                                             |                                                                                                                                                                                                                                                                                                         |
| \_Belegschafts Vergütung           | Lohnsatz und Häufigkeit im Zeitverlauf                                                                           |                                                                                                                                                                                                                                                                                                         |
| \_CurrentCompensation Belegschaft    | Lohnsatz und Häufigkeit ab dem aktuellen Datum                                                              | Belegschafts \_Demographie-Belegschafts\_\_Einzelvorgangs-Belegschafts Position Belegschafts\_Unternehmens-Belegschafts__ent_dict_PLACEHOLDER\_                                                                                                                                                                                            |
| \_CurrentPosition Belegschaft        | Positionen auf dem aktuellen Datum, entsprechenden ganztägig(FTE), den offen-zu-ausgefüllten den offenen Stellen und Positionen | Belegschafts \_\_Einzelvorgangs-Belegschafts Position                                                                                                                                                                                                                                                                      |
| \_CurrentWorker Belegschaft          | Arbeitskräfte vor dem aktuellen Datum und dem, die Dauer der Inventur Anwesenden                                                         | Belegschafts \_Leistungs-Belegschafts__ent_dict_PLACEHOLDER\_Belegschafts\_\_\_GeographicLocation\_WorkerName Belegschafts__ent_dict_PLACEHOLDER\_Belegschafts__ent_dict_PLACEHOLDER WorkerTitle\_\_Demographie-Belegschafts\_Einzelvorgangs-Belegschafts\_\_\_\_                     |
| \_Belegschafts Datum                   | Tagen, Wochen, Monaten und Jahre                                                                             |                                                                                                                                                                                                                                                                                                         |
| Belegschafts \_Demographie           | Geburtsdatum, Geschlecht, Familienstand Nationalität und                                                   |                                                                                                                                                                                                                                                                                                         |
| Belegschafts Beschäftigung \_             | Startdatum, Enddatum und Umbuchungsdatum                                                                  |                                                                                                                                                                                                                                                                                                         |
| \_GeographicLocation Belegschaft     | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           |                                                                                                                                                                                                                                                                                                         |
| \_Belegschafts Stelle                    | Funktion, Typ und Titel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| \_JobPreferredSkill Belegschaft      | Wichtigkeit, Bewertung, Qualifikationen und Fähigkeiten                                                                 | Belegschafts \_\_Qualifikations-Belegschafts Stelle                                                                                                                                                                                                                                                                         |
| \_PastPositionAssignment Belegschaft | Zuweisungsgrund, Startdatum, Enddatum und -Einzelvorgang                                                           | Belegschafts \_Datums-Belegschafts\_\_Einzelvorgangs-Belegschafts Position Belegschafts__ent_dict_PLACEHOLDER\_                                                                                                                                                                                                                            |
| \_Belegschafts Leistung            | Bewertung, Beschreibung und Bewertungsmodell                                                                      |                                                                                                                                                                                                                                                                                                         |
| \_PersonSkill Belegschaft            | Ebene, auf Berichtsebene Qualifikation und Datum                                                                               | \_Belegschafts Qualifikation                                                                                                                                                                                                                                                                                        |
| \_PersonSkillAnalysis Belegschaft    | Zertifiziertes, auf Berichtsebene, auf Berichtsebene Qualifikation und Datum                                                                    | Belegschafts-\_Belegschafts__ent_dict_PLACEHOLDER Qualifikation\_                                                                                                                                                                                                                                                                  |
| \_Belegschafts Position               | Abteilung, FTE, Position, Titel Positionstyp und                                                        |                                                                                                                                                                                                                                                                                                         |
| \_PositionTrend Belegschaft          | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Belegschafts \_Datums-Belegschafts\_\_Einzelvorgangs-Belegschafts Position Belegschafts__ent_dict_PLACEHOLDER\_                                                                                                                                                                                                                            |
| \_ReportsToWorkerName Belegschaft    | Vorname, Nachname und der Name                                                                       |                                                                                                                                                                                                                                                                                                         |
| \_Belegschafts Qualifikation                  | Qualifikation, Fähigkeitstyp und Bewertung                                                                              |                                                                                                                                                                                                                                                                                                         |
| \_TerminatedWorker Belegschaft       | Gesperrte Arbeitskräfte, Kündigungsdatum, Position, Titel und Aufgabenbereich                                             | Belegschafts \_Leistungs-Belegschafts__ent_dict_PLACEHOLDER\_Belegschafts\_\_\_GeographicLocation\_ReportsToWorkerName Belegschafts__ent_dict_PLACEHOLDER\_Belegschafts\_\_WorkerTitle Belegschafts\_Demographie-Belegschafts\_Beschäftigungs-Belegschafts\_\_\_\_ |
| \_WorkerName Belegschaft             | Vorname, Nachname und der Name                                                                       |                                                                                                                                                                                                                                                                                                         |
| \_WorkerTitle Belegschaft            | Titel- und Dienstalter                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce \_WorkerTrend             | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Belegschafts \_Leistungs-Belegschafts__ent_dict_PLACEHOLDER\_Belegschafts\_\_\_GeographicLocation\_ReportsToWorkerName Belegschafts__ent_dict_PLACEHOLDER\_Belegschafts\_\_WorkerTitle Belegschafts\_Demographie-Belegschafts\_\_Beschäftigungs-Belegschafts\_                     |

Diese wurden Entitäten verwendet, um berechnete Kennzahlen im - Datenmodell zu erstellen. Diese berechneten Kennzahlen, werden dann die Leistungskennzahlen (KPIs) und Berichten zu verwendet, die in das Content Pack verwendet werden. Wenn zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die CompetenciesandDevelopment.pbix-Datei der Kreditbriefe herunterladen und ändern. Diese Datei ist das Standarddatmodell, das verwendet wurde, um das Inhaltstext Pack zu erstellen. Wenn Sie die gewünschten Änderungen vorgenommen haben, können Sie ein organisatorisches Pack und ein zufriedenes Dashboard erstellen, die die Informationen enthalten, denen Sie Gäste hinzugefügt sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



