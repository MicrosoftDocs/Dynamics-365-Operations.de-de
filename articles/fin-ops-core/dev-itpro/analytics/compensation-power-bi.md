---
title: Power BI-Inhalt zur Kompensation
description: In diesem Thema wird der Power BI-Inhalt zur Kompensation beschrieben. Es wird erläutert, wie auf Berichte zugegriffen wird, und es werden Informationen zum verwendeten Datenmodell bereitgestellt.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmCompensationWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b625ea7dcbb6bd8b80cbcdcc544c59b9839fc19d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093055"
---
# <a name="compensation-power-bi-content"></a>Power BI-Inhalt zur Kompensation

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Microsoft Power BI-Inhalt zur **Kompensation** beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Der Power BI-Inhalt zur **Kompensation** wird im Arbeitsbereich **Vergütungsverwaltung** angezeigt, wenn Sie eines der folgenden Produkte verwenden:

- Finance and Operations Apps
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind
Die Berichte, die im Power BI-Inhalt zur **Kompensation** enthalten sind, haben Diagramme und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                     | Inhalt |
|----------------------------|----------|
| Vergütungsüberblick      | Zusammenfassung der anderen Berichte |
| Vergütungsanalyse      | Stunden- und angestellte Mitarbeiter nach Unternehmen, gesamte Mitarbeiter nach Vergütungsplan, männliche und weibliche Mitarbeiter nach Vergütungsplan und Mitarbeitervergütung nach Abteilung |
| Stellenlohnanalyse      | Höchster und niedrigster stündlicher und Gehaltslohn, höchster und niedrigster Lohn und Vollzeit- und Teilzeitpositionen |
| Vergütungsplananalyse | Mitarbeiterregistrierung nach ausgewählten Vorteilen |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgenden Daten werden verwendet, um die Berichte im Power BI-Inhalt zur **Kompensation** zu füllen. Diese Tabelle zeigt die Entitäten, auf denen der Inhalt basiert.

| Entität                   | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-Gegenkonto          | Kalendergegenkonten zu den Segmentberichten                                                                          | Zuweisung hinter der Position, Positionstrend, Mitarbeitertrend, ausgeschiedener Mitarbeiter |
| Unternehmen                  | Unternehmen, nach denen Berichte gefiltert werden können                                                                             | Aktuelle Vergütung, aktuelle Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Vergütung             | Lohnsatz und Häufigkeit im Zeitverlauf                                                                           | Aktuelle Vergütung, aktuelle Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Aktuelle Vergütung     | Lohnsatz und Häufigkeit ab dem aktuellen Datum                                                              | Unternehmen, Vergütung, Demographie, Einzelvorgang, Position |
| Aktuelle Position         | Positionen nach dem aktuellen Datum, aufgerechtet nach Vollzeit (FTE), offen Positionen und offenen, zu besetzenden Positionen | Stelle, Position |
| Aktueller Mitarbeiter         | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                                         | Unternehmen, Vergütung, geografischer Standort, Mitarbeitername, Vorgesetzter, Mitarbeitertitel, Demographie, Stelle, Beschäftigung, Position, Vergütungen, |
| Datum                     | Tage, Wochen, Monate und Jahre                                                                             | Vorheringe Positionszuweisung, Positionstrend, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Demografische Daten             | Geburtsdatum, Geschlecht, Familienstand und Nationalität                                                   | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Anstellung               | Startdatum, Enddatum und Umbuchungsdatum                                                                  | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Geografischer Standort      | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Stelle                      | Funktion, Typ und Titel                                                                                  | Aktuelle Position, aktueller Mitarbeiter |
| Zuordnung hinter der Position | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                                           | Kalender-Gegenkonto, Datum, Stelle, Position |
| Position                 | Abteilung, FTE, Position, Titel, Positionstyp                                                        | Aktuelle Position, aktueller Mitarbeiter |
| Positionstrend           | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Kalender-Gegenkonto, Datum, Stelle, Position |
| Vorgesetzter               | Vorname, Nachname, vollständiger Name                                                                       | Aktuelle Arbeitskraft, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Ausgeschiedener Mitarbeiter      | Ausgeschiedene Mitarbeiter, Kündigungsdatum, Titel, Position und Stelle                                           | Unternehmen, Vergütung, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum Mitarbeitertitel, Demographie, Beschäftigung, Stelle, Position, Vergütungen |
| Vorteile                 | Gültigkeitsdatum, Vergütungsoption, Vergütungsplan und Vergütungstyp                                             | Aktueller Name, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitername            | Vorname, Nachname, vollständiger Name                                                                       | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertitel           | Titel- und Dienstalter                                                                                   | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertrend           | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Unternehmen, Vergütung, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum Mitarbeitertitel, Demographie, Beschäftigung, Stelle, Vergütungen |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]