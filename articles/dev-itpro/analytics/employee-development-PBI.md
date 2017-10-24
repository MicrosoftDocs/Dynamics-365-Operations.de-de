---
title: "Power BI-Inhalt – Mitarbeiterentwicklung"
description: "In diesem Thema wird der Microsoft Power BI-Inhalt Mitarbeiterentwicklung beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 91f7071cc759686dd90b5893adaf58d1521e9185
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="employee-development-power-bi-content"></a>Power BI-Inhalt – Mitarbeiterentwicklung

[!include[banner](../includes/banner.md)]

In diesem Thema wird der Microsoft Power BI-Inhalt **Mitarbeiterentwicklung** beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt

Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Juli 2017) verwenden, können Sie das **Mitarbeiterentwicklung**-Inhaltspaket in der freigegebenen Anlagenbibliothek in Microsoft Dynamics Lifecycle Services (LCS) suchen. Weitere Informationen dazu, wie das Inhaltspaket herunterladen und mit Ihren Daten verbinden, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind
Die Berichte, die im Power BI-Inhalt **Mitarbeiterentwicklung** enthalten sind, enthalten Diagramme und Tabellen, die zusätzliche Informationen. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                        | Inhalt |
|-------------------------------|----------|
| Überblick der Mitarbeiterentwicklung | Zusammenfassung der anderen Berichte |
| Mitarbeiterfähigkeitsanalyse       | Mitarbeiterfähigkeitstypen und Mitarbeiterfähigkeiten nach Typ |
| Stufenanalyse der Mitarbeiterfähigkeiten | Mitarbeiterfähigkeitenstufen nach Abteilung, Mitarbeiterfähigkeitenstufe und Fähigkeitstyp sowie die niedrigste und höchste Stufe pro Fähigkeit |
| Qualifikationsprofil                 | Qualifikationsprofil für den ausgewählten Mitarbeiter. |
| Qualifikationsanalyse                | Qualifikation nach Typ und Bewertung |
| Leistungsbewertungsanalyse   | Mitarbeiter nach der niedrigsten und höchsten Bewertung nach Stelle, Mitarbeiterbewertungen für Abteilung, Mitarbeiter nach Bewertung nach Positionstyp sowie die niedrigsten und höchsten Bewertungen nach Position  |
| Mitarbeiterleistungsanalyse | Mitarbeiterbewertungen für ausgewählten Bewertung nach Vorgesetztem |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
| Entität                   | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-Gegenkonto          | Kalendergegenkonten zu den Segmentberichten                                                                          | Zuweisung hinter der Position, Positionstrend, Mitarbeitertrend, ausgeschiedener Mitarbeiter 
| Unternehmen                  | Unternehmen, nach denen Berichte gefiltert werden können                                                                             | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Aktuelle Position         | Positionen nach dem aktuellen Datum, aufgerechtet nach Vollzeit (FTE), offen Positionen und offenen, zu besetzenden Positionen | Stelle, Position |
| Aktueller Mitarbeiter         | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                                         | Unternehmen, geografischer Standort, Mitarbeitername, Vorgesetzter, Mitarbeitertitel, Demographie, Stelle, Beschäftigung, Position, |
| Datum                     | Tage, Wochen, Monate und Jahre                                                                             | Vorheringe Positionszuweisung, Positionstrend, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Demografische Daten             | Geburtsdatum, Geschlecht, Familienstand und Nationalität                                                   | Aktueller Mitarbeiter, ausgeschieden, Mitarbeiter, Mitarbeitertrend |
| Anstellung               | Startdatum, Enddatum und Umbuchungsdatum                                                                  | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Geografischer Standort      | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Stelle                      | Funktion, Typ und Titel                                                                                  | Aktuelle Position, aktueller Mitarbeiter |
| Zuordnung hinter der Position | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                                           | Kalender-Gegenkonto, Datum, Stelle, Position |
| Position                 | Abteilung, FTE, Position, Titel, Positionstyp                                                        | Aktuelle Position, aktueller Mitarbeiter |
| Positionstrend           | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Kalender-Gegenkonto, Datum, Stelle, Position |
| Vorgesetzter               | Vorname, Nachname, vollständiger Name                                                                       | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Ausgeschiedener Mitarbeiter      | Gesperrte Arbeitskräfte, Kündigungsdatum, Position, Titel und Aufgabenbereich                                             | Unternehmen, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum, Mitarbeitertitel, Demographie, Beschäftigung, Stelle, Position |
| Mitarbeitername            | Vorname, Nachname, vollständiger Name                                                                       | Aktuelle Arbeitskraft, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertitel           | Titel- und Dienstalter                                                                                   | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertrend           | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Unternehmen, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum, Mitarbeitertitel, Demographie, Beschäftigung, Stelle |
| Stelle                      | Funktion, Typ und Titel                                                                                      | Aktueller Mitarbeiter, aktuelle Position, Mitarbeitertrend, bevorzugte Stellenfähigkeiten, vergangene Positionszuweisung, Positionstrend, ausgeschiedener Mitarbeiter |
| Bevorzugte Stellenfähigkeit      | Wichtigkeit, Bewertung, Qualifikationen und Fähigkeiten                                                                 | Stelle |
| Mitarbeiterfähigkeitsanalyse  | Zertifiziert, Ebene, Datumsebene und Qualifikation                                                                    | Name des Mitarbeiters, Fähigkeit |  
| Leistung              | Bewertung, Beschreibung und Bewertungsmodell                                                                      | Aktueller Mitarbeiter, aktuelle Position, Mitarbeitertrend, bevorzugte Stellenfähigkeiten, vergangene Positionszuweisung, Positionstrend, ausgeschiedener Mitarbeiter |
|  Qualifikation                   | Qualifikation, Fähigkeitstyp und Bewertung                                                                              | Mitarbeiterfähigkeitsanalyse, bevorzugte Stellenfähigkeit |                                                                                                                        

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden dann verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Power BI-Inhalt verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die PBIX-Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um den Power BI-Inhalt zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

