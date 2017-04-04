---
title: "MwSt für Österreich. -Auszugsdetails"
description: "In diesem Thema wird erläutert, wie Sie die Mehrwertsteuererklärung. im für juristische Personen in Österreich eingerichtet."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 264334
ms.assetid: 2542c9e1-ed47-416f-9773-7b87eef66e78
ms.search.region: Austria
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: bf323371c79ab5b2b6b4e829057ddad0b590c043
ms.lasthandoff: 03/31/2017


---

# <a name="vat-statement-details-for-austria"></a>MwSt für Österreich. -Auszugsdetails

In diesem Thema wird erläutert, wie Sie die Mehrwertsteuererklärung. im für juristische Personen in Österreich eingerichtet.

Dieses Thema enthält länder-/regionsspezifische Informationen zu den Einstellungen des Auszugs Mehrwertsteuer (VAT)- für juristische Personen nur in Österreich. Weitere Informationen zu den Einstellungen des MwSt. -Auszugs, lesen Sie. [] (MwSt Berichte in Bezug emea-vat-reporting.md ). Der Rest dieses Themas zeigt, wie und für Mehrwertsteuercodes Mehrwertsteuer-Erklärungscodes die österreichischen Mehrwertsteuererklärung eingerichtet, sodass MwSt. -Auszüge generiert werden können.

## <a name="set-up-sales-tax-authorities"></a>Einrichten von Mehrwertsteuerbehörden
Um eine Umsatzsteuervoranmeldung im richtigen Format der entsprechenden Steuerbehörde zu generieren, müssen Sie das Berichtslayout für die Mehrwertsteuerbehörden eingerichtet werden. Auf der Mehrwertsteuerbehörden ** ** Seite im ** Berichtslayout ** Feld, wählen Sie aus ** österreichisches Berichtslayout **. Wählen Sie dieselbe Mehrwertsteuerbehörde für den Mehrwertsteuer-Abrechnungszeitraum aus, in den der Mehrwertsteuercodes verwendet wird.

## <a name="set-up-sales-tax-codes-and-sales-tax-reporting-codes-for-vat-reporting"></a>Einrichten von Mehrwertsteuercodes und Berichte in Bezug Mehrwertsteuer-Erklärungscodes für Mehrwertsteuer.
Das folgende Beispiel, das anzeigt, z Sie möglicherweise Mehrwertsteuer-Erklärungscodes und Mehrwertsteuercodes einrichten, um einer Mehrwertsteuererklärung. im zu generieren.

| Mehrwertsteuercode | Prozentsatz | Beschreibung                                                                                                                  |
|----------------|------------|------------------------------------------------------------------------------------------------------------------------------|
| AT20           | 20         | In Gruppen für österreichische Debitoren und Kreditoren und Kreditoren der Europäischen Union (EU)-. Für EU-Kreditoren ** Verbrauchssteuer **=** Ja **. |
| AT13           | 13         | In Gruppen für österreichische Debitoren und Kreditoren und IN EU-Kreditoren. Für EU-Kreditoren ** Verbrauchssteuer **=** Ja **.                  |
| AT10           | 10         | In Gruppen für österreichische Debitoren und Kreditoren und IN EU-Kreditoren. Für EU-Kreditoren ** Verbrauchssteuer **=** Ja **.                  |
| ATImp20        | 20         | In einer Gruppe für nicht-EU Kreditoren.                                                                                      |
| ATImp13        | 13         | In einer Gruppe für nicht-EU Kreditoren.                                                                                      |
| ATImp10        | 10         | In einer Gruppe für nicht-EU Kreditoren.                                                                                      |
| ATRC20         | 20         | In einer Gruppe für Kreditoren mit Steuerschuldumkehr. ** Verbrauchssteuer **=** Ja **.                                                    |
| ATRC13         | 13         | In einer Gruppe für Kreditoren mit Steuerschuldumkehr. ** Verbrauchssteuer **=** Ja **.                                                    |
| ATRC10         | 10         | In einer Gruppe für Kreditoren mit Steuerschuldumkehr. ** Verbrauchssteuer **=** Ja **.                                                    |

Das folgende Beispiel von Mehrwertsteuer-Erklärungscodes.

| Mehrwertsteuer-Erklärungscode | Beschreibung                                                                   | Entsprechendes Feld in der Meldung |
|--------------------------|-------------------------------------------------------------------------------|--------------------------------------|
| 1022                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen Standardsteuersatz von 20 Prozent haben | 022                                  |
| 1122                     | Steuerbetrag von inländischer Verkäufe, die einen Standardsteuersatz von 20 Prozent haben      | 022                                  |
| 1029                     | Steuergrundlagenbetrag von inländischer Verkäufe verwendet, für die ein Steuersatz der ermäßigten Steuer von 10 Prozent haben  | 029                                  |
| 1129                     | Steuerbetrag von inländischer Verkäufe verwendet, für die ein Steuersatz der ermäßigten Steuer von 10 Prozent haben       | 029                                  |
| 1006                     | Steuergrundlagenbetrag von inländischer Verkäufe verwendet, für die ein Steuersatz der ermäßigten Steuer von 13 Prozent haben  | 006                                  |
| 1106                     | Steuerbetrag von inländischer Verkäufe verwendet, für die ein Steuersatz der ermäßigten Steuer von 13 Prozent haben       | 006                                  |
| 1072                     | Steuergrundlagenbetrag nach EU-Einkäufe, die einen Standardsteuersatz von 20 Prozent haben   | 072                                  |
| 1172                     | Steuerbetrag für EU-Einkäufe, die einen Standardsteuersatz von 20 Prozent haben        | 072                                  |
| 1073                     | Steuergrundlagenbetrag EU-Einkäufe durch die ein Steuersatz, der ermäßigten Steuer von 10 Prozent haben    | 073                                  |
| 1173                     | Steuerbetrag für EU-Einkäufe die ein Steuersatz, der ermäßigten Steuer von 10 Prozent haben         | 073                                  |
| 1008                     | Steuergrundlagenbetrag EU-Einkäufe durch die ein Steuersatz, der ermäßigten Steuer von 13 Prozent haben    | 008                                  |
| 1108                     | Steuerbetrag für EU-Einkäufe die ein Steuersatz, der ermäßigten Steuer von 13 Prozent haben         | 008                                  |
| 1161                     | Steuerbetrag von Importeinkäufe                                                | 061                                  |
| 1160                     | Steuerbetrag von Einkäufen                                                       | 060                                  |
| 1165                     | Steuerforderung nach EU-Einkäufe                                                | 065                                  |
| 1132                     | Steuerverbindlichkeiten gemäß dem 1D §19 Verbindlichkeiten                                      | 032                                  |
| 1189                     | Steuerverbindlichkeiten er gemäß des 1D §19                                   | 089                                  |

Wenn Sie eine Zuweisung von Mehrwertsteuer-Erklärungscodes zu Mehrwertsteuercodes einrichten, wechseln ** Mehrwertsteuercodes ** &gt; **** Berichts-Einstellung ****. Das folgende Beispiel einer Zuweisung von Mehrwertsteuer-Erklärungscodes zu Mehrwertsteuercodes.

| Mehrwertsteuercode | Steuerpflichtiger Umsatz | Mehrwertsteuer | Steuerpflichtige Einkäufe | Vorsteuer | Steuerpflichtiger Import | Erwerbsteuer (USA) | Ausgleich Erwerbsteuer (USA) |
|----------------|---------------|-------------------|-------------------|----------------------|----------------|---------|----------------|
| AT20           | 1022          | 1122              |                   | 1160                 | 1072           | 1172    | 1165           |
| AT13           | 1006          | 1106              |                   | 1160                 | 1008           | 1108    | 1165           |
| AT10           | 1029          | 1129              |                   | 1160                 | 1073           | 1173    | 1165           |
| ATImp20        |               |                   |                   |                      | 1061           |         | 1161           |
| ATImp13        |               |                   |                   |                      | 1061           |         | 1161           |
| ATImp10        |               |                   |                   |                      | 1061           |         | 1161           |
| ATRC20         |               |                   |                   |                      |                | 1132    | 1189           |
| ATRC13         |               |                   |                   |                      |                | 1132    | 1189           |
| ATRC10         |               |                   |                   |                      |                | 1132    | 1189           |

** Hinweis: ** Die Konfiguration vorstehende Beispiel und hängt von der Struktur der Mehrwertsteuercodes, die verwendet werden, z vom Benutzer festgelegt ab. Damit die Werte besitzen, in die Meldung, die für jeden Steuercode berechnet und übertragen wurden der verwendet wird, müssen Sie im Mehrwertsteuerzahlungsprozess muss ein entsprechender Mehrwertsteuer-Erklärungscode in einem oder mehrere Felder der Bericht eingerichtet ** ** der Registerkarte festlegen.

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Konfigurieren Sie das Berichterstellungsmodell und elektronische -Format für den Bericht
Um die MwSt. -Auszugskonfiguration für juristische Personen in Österreich, auf der Berichterstellungskonfigurationen ** ** Seite zu prüfenden oder zu ändern, wählen Mehrwertsteuererklärungsmodell ** ** von Modellen in der Liste aus. Dieses Modell wird für Österreich, Tschechische Republik, Estland, Finnland, Lettland und Litauen und für gesamte Steuerdaten verwendet, die für die Mehrwertsteuererklärung erforderlich ist. Klicken Sie im Aktivitätsbereich auf Designer ** ** um das Modell zu prüfenden oder zu ändern. Um auf das MwSt. -Auszugsformat für juristische Personen in Österreich, auf der Berichterstellungskonfigurationen ** ** Seite zu prüfenden oder zu ändern, wählen Mehrwertsteuererklärungsmodell ** ** in der Liste von Modellen und wählen dann U30 ** ** unten aus ** Mehrwertsteuererklärungsmodell **. Klicken Sie im Aktivitätsbereich ** Designer ** um das Format zu prüfenden oder zu ändern.

## <a name="generate-a-vat-statement"></a>Generieren Sie im. einer Mehrwertsteuererklärung
Am Ende des MwSt. -Berichtszeitraums, Ausführung ** Bank und Buchung ** ** Mehrwertsteuer ** Aufstellungszeilebeträge für die Definition von Mehrwertsteuer-Erklärungscodes berechnen, die Sie erstellt haben. In der folgenden Tabellen werden die Felder beschrieben, die Sie festlegen müssen.

|Feld|Beschreibung|
|-----|-----------|
|Ausgleichsperiode|Wählen Sie den gewünschten Berichtszeitraum aus.|
|Von Datum|Geben Sie den ersten Tag des Mehrwertsteuer-Abrechnungszeitraums, um die Mehrwertsteuer zu berechnen. Dieser Wert entspricht dem Datum im Feld auf der Mehrwertsteuer-Abrechnungszeitraum-Seite.|
|Buchungsdatum|Geben Sie das Datum, an dem die Mehrwertsteuererklärung berechnet wird. Der aktuelle Wert ist das aktuelle Datum. Das Enddatum des Abrechnungszeitraums, die im Feld angezeigt wird, entspricht dem Feld auf der Mehrwertsteuer-Abrechnungszeitraum-Seite. Die Mehrwertsteuerzahlung wird für alle Buchungen berechnet, die für den Abrechnungszeitraum gebucht wurden.|
|Mehrwertsteuer, Zahlungsversion|Wählen Sie die Buchungsarten aus, die in die Berechnung der Mehrwertsteuerzahlung einbezogen werden sollen: 
** Vorlage ** – Bezieht Mehrwertsteuerbuchungen der ersten gebuchten Ausgleichsberechnung für die Periode ein.
** Zuletzt Korrekturen ** enthalten – Mehrwertsteuerbuchungen, die in der letzten Ausgleichsberechnung für den Zeitraum enthalten sind_=_ _=_Formatzuordnung_=_Geben Sie U30 angezeigt. _=_

Um eine MwSt. -XML-Datei zu generieren, verwenden Sie die ** Melden des Mehrwertsteuer für Ausgleichsperiode ** Seite.


