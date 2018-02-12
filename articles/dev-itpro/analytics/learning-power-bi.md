---
title: Power BI-Weiterbildung
description: In diesem Thema wird der Power BI-Weiterbildungsinhalt beschrieben.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: e5a78812aabaa5c835fe23787a9cbb57d1a7770e
ms.contentlocale: de-de
ms.lasthandoff: 12/19/2017

---

# <a name="learning-power-bi-content"></a>Power BI-Weiterbildung

[!include[banner](../includes/banner.md)]

In diesem Thema wird der **Weiterbildungs**-Inhalt für Microsoft Power BI beschrieben.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind

Die Berichte, die im **Weiterbildungs**-Inhalt von Power BI enthalten sind, haben Diagramme und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                | Inhalt |
|-----------------------|----------|
| Überblick über die Weiterbildung     | Zusammenfassung der anderen Berichte |
| Kurs-Analyse       | Erfassung nach Lagerplatz, Teilnehmer nach Status, Kurse nach Typ pro Unternehmen und Kursanwesenheit nach Stelle |
| Erfassungsanalyse | Steuernummer |
| Kurstypen          | Kurstypen nach Qualifikation |
| Kursleiteranalyse   | Verhältnis von Kurse zu Kursleiter, Anzahl Kursleiter, Kurse vom Kursleiter, Kurse pro Kursleiter und Kursagenda nach Kursleiter |
| Angebotene Kurse       | Liste von Kursen |
| Kurs-Design        | Kursagenda |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichte im **Weiterbildungs**-Inhalt von Power BI zu füllen. Diese Tabelle zeigt die Entitäten, auf denen der Inhalt basiert.

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



