---
title: Power BI-Inhalt zu Vergütungen
description: In diesem Artikel wird der Power BI-Inhalt zu Vergütungen beschrieben.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.search.form: HcmBenefitWorkspace
ms.openlocfilehash: ed1fd0b86e44d022a4858e3b5bc61c83a8efd395
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206656"
---
# <a name="benefits-power-bi-content"></a>Power BI-Inhalt zu Vergütungen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird der Microsoft Power BI-Inhalt zu **Vergütungen** beschrieben. Es wird beschrieben, wie auf die Berichte, die enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Der Power BI-Inhalt zu **Vergütungen** wird im Arbeitsbereich **Vorteilsverwaltung** angezeigt, wenn Sie eines der folgenden Produkte verwenden:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind
Die Berichte, die im Power BI-Inhalt zu **Vergütungen** enthalten sind, haben Diagramme und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                      | Inhalt                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Überblick der Vorteils-Registrierung | Die meisten und am wenigsten registrierten Pläne, Registrierung durch Mitarbeitergruppe und ausgewählte Vorteilsplanoptionen |
| Mitarbeitervergütungen           | Mitarbeiterregistrierung nach ausgewählten Vorteilen                                                        |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgenden Daten werden verwendet, um die Berichte im Power BI-Inhalt zu **Vergütungen** zu füllen. Diese Tabelle zeigt die Entitäten, auf denen der Inhalt basiert.

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
