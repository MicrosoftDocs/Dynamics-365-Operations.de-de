---
title: Organisatorischer Trainings-Energie BIinhalt
description: "In diesem Thema wird das Dynamics 365 - Trainings-Energie organisatorischer für Arbeitsgänge BIinhalt. Er zeigt, wie das Inhaltstext Pack zugreift und wird das - Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisatorischer Trainings-Energie BIinhalt

In diesem Thema wird das Dynamics 365 - Trainings-Energie organisatorischer für Arbeitsgänge BIinhalt. Er zeigt, wie das Inhaltstext Pack zugreift und wird das - Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen des das Content Packs
--------------------------

Sie können das Trainings organisatorischen Inhaltstext Pack des in der Bibliothek der kommenden Anlagen in den Microsoft Dynamics Lifecycle Services (LCS) suchen. Weitere Informationen dazu, wie das herunterlädt Inhaltstext Pack und es für Ihr Microsoft Dynamics 365 für Arbeitsgänge, Daten finden Sie in BIinhalt herstellt [Energie Kreditbriefen von Microsoft und von den Partnern]( power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten inhaltliche sind
Nachdem das Inhaltstext Pack für Ihr Dynamics 365 für Arbeitsgangsdaten verbunden wurde, zeigen die Berichte die Daten der Organisation an. Wenn Sie nicht Microsoft-Energie vor BI verwendet haben, können Sie dieser auf mehr zu erfahren [geführt, Seite für Leistung BI] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) erfahrend. Die Berichte, die im Paket enthalten inhaltliche werden, weisen den Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht          | Inhalt                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurs-Analyse | Erfassung nach Lagerplatz, Kursteilnehmer nach Status und Erfassungsliste |
| Kurstypen    | Kurstypen nach Qualifikation                                                       |

Sie können die und die Kacheln Diagramme in diesen Erklärungen Stift und die Diagramme und die Kacheln das Dashboard filtern. Weitere Informationen dazu, wie und Energie Stift in finden Sie BI, gefiltert [Dient zum Erstellen und Konfigurieren eines Dashboard] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 für Arbeitsgangsdaten wird verwendet, um die Berichte im das Content Pack des Trainings organisatorischen aufzufüllen. Die folgende Tabelle enthält die von Entitäten, dass das Inhaltstext Pack auf Grundlage war.

| Entität                    | Inhalt                                                         | Beziehungen mit anderen Entitäten                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_CalendarOffset Schulung  | Kalendergegenkonten zu den Segmentberichten                                | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| \_Trainings Unternehmen         | Unternehmen, z von Berichten nach filtern                                   | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| \_Trainings Kurs          | Kurs, Beschreibung, Kursleitername, Standort, Status ist und | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult\_CourseSkill schult                                                                                                                             |
| \_CourseAgenda Schulung    | Kursprogrammen, Kurs und Start- und Endzeiten                          | \_Trainings Unternehmen, das schult\_\_CalendarOffset Datum schult\_schult Kurs                                                                                                                         |
| \_CourseAttendees Schulung | Name, Status, Einzelvorgang und Erstzulassung                         | \_Trainings Unternehmen, das schult\_\_CalendarOffset Datum schult\_Demographie\_schult Beschäftigung schult\_Kurs schult\_WorkerName schult\_WorkerTitle schult\_\_Berufsausbildungs Position schult |
| \_CourseSkill Schulung     | Qualifikation, Fähigkeitstyp und Ebene                                     | \_Trainings Kurs                                                                                                                                                                                   |
| \_Trainings Datum            | Tagen, Wochen, Monaten und Jahre                                   | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| Trainings \_Demographie    | Geburtsdatum, Geschlecht, Familienstand Nationalität und         | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| Trainings Beschäftigung \_      | Startdatum, Enddatum und Umbuchungsdatum                        | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| \_Trainings Stelle             | Funktion, Typ und Titel                                        | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| \_Trainings Position        | Position, Titel und entsprechendes ganztägig(FTE)                  | Schulungskurse \_CourseAgenda, das\_CourseAttendees schult                                                                                                                                                   |
| \_WorkerName Schulung      | Vorname, Nachname und der Name                             | \_CourseAttendees Schulung                                                                                                                                                                          |
| \_WorkerTitle Schulung     | Titel- und Dienstalter                                         | \_CourseAttendees Schulung                                                                                                                                                                          |

Diese wurden Entitäten verwendet, um berechnete Kennzahlen im - Datenmodell zu erstellen. Diese berechneten Kennzahlen, werden dann die Leistungskennzahlen (KPIs) und Berichten zu verwendet, die in das Content Pack verwendet werden. Wenn zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die Training.pbix-Datei der Kreditbriefe herunterladen und ändern. Diese Datei ist das Standarddatmodell, das verwendet wurde, um das Inhaltstext Pack zu erstellen. Wenn Sie die gewünschten Änderungen vorgenommen haben, können Sie ein organisatorisches Pack und ein zufriedenes Dashboard erstellen, die die Informationen enthalten, denen Sie Gäste hinzugefügt sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



