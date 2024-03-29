---
title: Power BI-Inhalt zur Weiterbildung
description: In diesem Artikel wird der Power BI-Inhalt zur Weiterbildung beschrieben.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a7aca9e47ed26dcb4ef7f4b9aee72987e2d8fdd2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273958"
---
# <a name="learning-power-bi-content"></a>Power BI-Inhalt zur Weiterbildung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird der Microsoft Power BI-Inhalt zur **Weiterbildung** beschrieben.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind

Die Berichte, die im Power BI-Inhalt zur **Weiterbildung** enthalten sind, haben Diagramme und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                | Inhalt |
|-----------------------|----------|
| Überblick über die Weiterbildung     | Zusammenfassung der anderen Berichte |
| Kurs-Analyse       | Erfassung nach Lagerplatz, Teilnehmer nach Status, Kurse nach Typ pro Unternehmen und Kursanwesenheit nach Stelle |
| Erfassungsanalyse | Steuernummer |
| Kurstypen          | Kurstypen nach Qualifikation |
| Kursleiteranalyse   | Verhältnis von Kurse zu Kursleiter, Anzahl Kursleiter, Kurse vom Kursleiter, Kurse pro Kursleiter und Kursagenda nach Kursleiter |
| Angebotene Kurse       | Liste von Kursen |
| Kurs-Design        | Kursagenda |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichte im Power BI-Inhalt zur **Weiterbildung** zu füllen. Diese Tabelle zeigt die Entitäten, auf denen der Inhalt basiert.

| Entität           | Inhalt                                                         | Beziehungen mit anderen Entitäten |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalender-Gegenkonto  | Kalendergegenkonten zu den Segmentberichten                                | Kursagenda, Kursteilnehmer |
| Unternehmen          | Unternehmen, nach denen Berichte gefiltert werden können                                   | Kursagenda, Kursteilnehmer |
| Kurs           | Kurs, Beschreibung, Kursleitername, Standort und Status | Kursagenda, Kursteilnehmer, Kurs-Qualifikation |
| Kursagenda    | Kursprogrammen, Kurs und Start- und Endzeiten                          | Unternehmen, Kalender-Gegenkonto, Datum, Kurs |
| Kursteilnehmer | Name, Status, Einzelvorgang und Erstzulassung                         | Unternehmen, Kalender-Gegenkonto, Datum, Kurs, Demographie, Beschäftigung, Kurs, Mitarbeitername, Mitarbeitertitel, Stelle, Position |
| Kurs-Qualifikation     | Qualifikation, Fähigkeitstyp und Level                                     | Kurs |
| Datum             | Tage, Wochen, Monate und Jahre                                   | Kursagenda, Kursteilnehmer |
| Demografische Daten     | Geburtsdatum, Geschlecht, Familienstand und Nationalität         | Kursagenda, Kursteilnehmer |
| Anstellung       | Startdatum, Enddatum und Umbuchungsdatum                        | Kursagenda, Kursteilnehmer |
| Stelle              | Funktion, Typ und Titel                                        | Kursagenda, Kursteilnehmer |
| Position         | Position, Titel und FTE                  | Kursagenda, Kursteilnehmer |
| Mitarbeitername    | Vorname, Nachname, vollständiger Name                             | Kursteilnehmer |
| Mitarbeitertitel   | Titel- und Dienstalter                                         | Kursteilnehmer |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
