---
title: Power BI-Inhalt zu Arbeitskraftkennzahlen
description: In diesem Thema wird der Power BI-Inhalt Arbeitskraftkennzahlen beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorkforceWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Human Resources
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 263fa2fc97e39b0521407d3fdc5a6d6e3f2ca034
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005755"
---
# <a name="workforce-metrics-power-bi-content"></a>Power BI-Inhalt zu Arbeitskraftkennzahlen

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Microsoft Power BI-Inhalt **Arbeitskraftkennzahlen** beschrieben. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Der **Arbeitskraftkennzahlen**-Inhalt für Power BI wird im Arbeitsbereich **Personalverwaltung** angezeigt, wenn Sie eines der folgenden Produkte verwenden:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriken, die im Power BI-Inhalt enthalten sind
Die folgende Tabelle enthält die Metrik, die für jede Berichtsseite verfügbar ist.

| Bericht                                           | Metriken |
|--------------------------------------------------|---------|
| Personen-Metrik                                   | Zusammenfassung der anderen Berichte |
| Mitarbeiterzahlanalyse nach Unternehmen, Abteilung, Standort | Mitarbeiterzahl nach Unternehmen, Mitarbeiterzahl nach Abteilung, Mitarbeiterzahl nach Standort und Mitarbeiterzahl gesamt |
| Mitarbeiterzahlanalyse nach Stelle, Schritt, Manager            | Mitarbeiterzahl nach Stelle, Mitarbeiterzahl nach Schritt, Mitarbeiterzahl nach Manager und Mitarbeiterzahl gesamt |
| Mitarbeiterzahl-Trendanalyse                         | Mitarbeiteranzahl in diesem Jahr kontra letztem Jahr nach Unternehmen und rollierende Mitarbeiterzahl der letzten 12 Monate. |
| FTE-Analyse                                     | Gesamtzahl der Vollzeitmitarbeiter (FTE), Total zugewiesene FTE, FTE nach Abteilung, FTE für die letzten 12 Monate und FTE nach Stelle |
| Belegschaftsdemografie                           | Mitarbeiterzahl nach Alter und Geschlecht, Mitarbeiterzahl nach ethnischer Herkunft, Mitarbeiterzahl nach Veteranenstatus, Mitarbeiterzahl nach Familienstand, Anzahl an Vollzeitstudenten, durchschnittliche Beschäftigungsdauer, Durchschnittsalter, Anzahl weiblicher und männlicher Mitarbeiter im Vergleich und von Mitarbeiter gesprochene Sprachen. |
| Stellenanalyse                                | Offene Stellen nach Abteilung, offene kontra besetzte Stellen, aktive kontra inaktive Stellen und Stellen nach Abteilung |
| Analyse der Abgänge                               | Abgänge in diesem Jahr im Vergleich zum letzten Jahr, Abgänge, ausscheidende Mitarbeiter nach Alter und Geschlecht, durchschnittliche Beschäftigungsdauer von ausscheidenden Mitarbeitern, ausscheidende Mitarbeiter in diesem Monat und Mitarbeiter mit Ausscheidungsgrund. |
| Personen nach Abteilung                             | Mitarbeiter mit einer Personalnummer nach Abteilung, Position und Zuweisungsstart-und enddaten |
| Dienstalteranalyse                               | Durchschnittliche Beschäftigung, durchschnittliche Dienstjahre nach Unternehmen und Dienstalterliste |
| Mitarbeiter-Jahrestage                           | Jahrestage in diesem Monat, Jahrestage im nächsten Monat, Mitarbeiter nach Dienstjahren und Dienstjahre nach Abteilung |
| Mitarbeiter-Geburtstage                               | Geburtstage in diesem Monat, Geburtstage im nächsten Monat, Mitarbeitergeburtstage und Geburtstage nach Monat und Abteilung |
| Masseneinstellungsprojekte                               | Gesamte Masseneinstellungsprojekte, Masseneinstellungsprojekte nach Status, Masseneinstellungsprojekte nach Abteilung und Eigentümer, Masseneinstellungsprojekte nach Einzelvorgang und Masseneinstellungsprojekte |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Stellen Sie sicher, dass Sie den **Arbeitskraftkennzahlen** Power BI-Inhalt herunterladen, der der von Ihnen verwendeten Microsoft Dynamics 365-Version entspricht.

> [!NOTE]
> Die .pbix-Dateien, die in Lifecycle Services verfügbar sind, gelten nur für Finance and Operations Apps.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                   | Inhalt                                                                            | Beziehungen mit anderen Entitäten |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-Gegenkonto          | Kalendergegenkonten zu den Segmentberichten                                                   | Zuweisung hinter der Position, Positionstrend, Mitarbeitertrend, ausgeschiedener Mitarbeiter |
| Unternehmen                  | Unternehmen, nach denen Berichte gefiltert werden können                                                      | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Aktuelle Position         | Positionen nach dem aktuellen Datum, FTE, offen Positionen und offene, zu besetzende Positionen | Stelle, Position |
| Aktueller Mitarbeiter         | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                  | Unternehmen, geografischer Standort, Mitarbeitername, Vorgesetzter, Mitarbeitertitel, Demographie, Stelle, Beschäftigung, Position, |
| Datum                     | Tage, Wochen, Monate und Jahre                                                      | Vorheringe Positionszuweisung, Positionstrend, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Demografische Daten             | Geburtsdatum, Geschlecht, Familienstand und Nationalität                            | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Anstellung               | Startdatum, Enddatum und Umbuchungsdatum                                           | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Geografischer Standort      | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                    | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Stelle                      | Funktion, Typ und Titel                                                           | Aktuelle Position, aktueller Mitarbeiter |
| Zuordnung hinter der Position | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                    | Kalender-Gegenkonto, Datum, Stelle, Position |
| Position                 | Abteilung, FTE, Position, Titel, Positionstyp                                 | Aktuelle Position, aktueller Mitarbeiter |
| Positionstrend           | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                   | Kalender-Gegenkonto, Datum, Stelle, Position |
| Vorgesetzter               | Vorname, Nachname, vollständiger Name                                                | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Ausgeschiedener Mitarbeiter      | Gesperrte Arbeitskräfte, Kündigungsdatum, Position, Titel und Aufgabenbereich                      | Unternehmen, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum, Mitarbeitertitel, Demographie, Beschäftigung, Stelle, Position |
| Mitarbeitername            | Vorname, Nachname, vollständiger Name                                                | Aktuelle Arbeitskraft, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertitel           | Titel- und Dienstalter                                                            | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertrend           | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                 | Unternehmen, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum, Mitarbeitertitel, Demographie, Beschäftigung, Stelle |
| Masseneinstellungsprojekt        | Anzahl der Massenprojekte, Projekteigentümer und Projektstatus                     | Unternehmen, Positionsstatus für Masseneinstellung. |
| Positionen für Masseneinstellung           | Abteilung, Beschäftigungstyp und Position                                           | Datum, Stelle, Masseneinstellungsprojekt |
