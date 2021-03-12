---
title: MwSt-Berichtdetails für Österreich
description: In diesem Thema wird erläutert, wie der MwSt Bericht für juristische Personen in Österreich erfasst wird.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 264334
ms.search.region: Austria
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: eec58a43e400186c781f1c3d5ac943029c9854e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988339"
---
# <a name="vat-statement-details-for-austria"></a>MwSt-Berichtdetails für Österreich

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie der MwSt Bericht für juristische Personen in Österreich erfasst wird.

Dieses Thema enthält länder-/regionsspezifische Informationen zu den Einstellungen des Auszugs Mehrwertsteuer (MwSt)- für juristische Personen nur in Österreich. Weitere Informationen zur Einrichtung des MwSt.-Auszugs finden Sie unter [MwSt-Berichterstattung für Europa](emea-vat-reporting.md). Der Rest dieses Themas zeigt, wie Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes für die österreichischen Mehrwertsteuererklärung eingerichtet wird, sodass MwSt. -Auszüge generiert werden können.

## <a name="set-up-sales-tax-authorities"></a>Einrichten von Mehrwertsteuerbehörden
Um eine Umsatzsteuervoranmeldung im richtigen Format der entsprechenden Steuerbehörde zu generieren, müssen das Berichtslayout für die Mehrwertsteuerbehörden eingerichtet werden. Sie müssen auch das Feld **Berichtslayout** im Bereich **Allgemein** auf der Seite **Mehrwertsteuer-Behörden** auswählen. Wählen Sie dieselbe Mehrwertsteuerbehörde für den Mehrwertsteuer-Abrechnungszeitraum aus, in der der Mehrwertsteuercodes verwendet wird.

## <a name="set-up-sales-tax-codes-and-sales-tax-reporting-codes-for-vat-reporting"></a>Hier können Sie Erklärungscodes für Verkäufe und Einkäufe für Mehrwertsteuererklärungen einrichten.
Das folgende Beispiel zeigt, dass Sie möglicherweise Mehrwertsteuer-Erklärungscodes und Mehrwertsteuercodes einrichten, um einer Mehrwertsteuererklärung zu generieren.

| Mehrwertsteuercode | Prozentsatz | Beschreibung                                                                                                                  |
|----------------|------------|------------------------------------------------------------------------------------------------------------------------------|
| AT20           | 20         | Eingeschlossen in Gruppen für österreichische Debitoren und Kreditoren und Kreditoren der Europäischen Union (EU)-. Für EU-Verkäufer **Verbrauchssteuer**=**Yes**. |
| AT13           | 13         | Eingeschlossen in Gruppen für österreichische Debitoren und Kreditoren und Kreditoren. Für EU-Verkäufer **Verbrauchssteuer**=**Yes**.                  |
| AT10           | 10         | Eingeschlossen in Gruppen für österreichische Debitoren und Kreditoren und Kreditoren. Für EU-Verkäufer **Verbrauchssteuer**=**Yes**.                  |
| ATImp20        | 20         | In einer Gruppe für nicht-EU Kreditoren.                                                                                      |
| ATImp13        | 13         | In einer Gruppe für nicht-EU Kreditoren.                                                                                      |
| ATImp10        | 10         | In einer Gruppe für nicht-EU Kreditoren.                                                                                      |
| ATRC20         | 20         | In einer Gruppe für Kreditoren mit Steuerschuldumkehr. **Verbrauchssteuer**=**Ja**.                                                    |
| ATRC13         | 13         | In einer Gruppe für Kreditoren mit Steuerschuldumkehr. **Verbrauchssteuer**=**Ja**.                                                    |
| ATRC10         | 10         | In einer Gruppe für Kreditoren mit Steuerschuldumkehr. **Verbrauchssteuer**=**Ja**.                                                    |

Hier ist ein Beispiel von Mehrwertsteuer-Erklärungscodes.

| Mehrwertsteuer-Erklärungscode | Beschreibung                                                                   | Entsprechendes Feld in der Meldung |
|--------------------------|-------------------------------------------------------------------------------|--------------------------------------|
| 1022                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen Standardsteuersatz von 20 Prozent haben | 022                                  |
| 1122                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen Standardsteuersatz von 20 Prozent haben      | 022                                  |
| 1029                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen reduzierten Standardsteuersatz von 10 Prozent haben  | 029                                  |
| 1129                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen reduzierten Standardsteuersatz von 10 Prozent haben       | 029                                  |
| 1006                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen reduzierten Standardsteuersatz von 13 Prozent haben  | 006                                  |
| 1106                     | Inländische Steuergrundlagenbetrag nach Umsatz, die einen reduzierten Standardsteuersatz von 13 Prozent haben       | 006                                  |
| 1072                     | Inländische Steuergrundlagenbetrag nach EU-Umsatz, die einen Standardsteuersatz von 20 Prozent haben   | 072                                  |
| 1172                     | Inländische Steuergrundlagenbetrag nach EU-Umsatz, die einen Standardsteuersatz von 20 Prozent haben        | 072                                  |
| 1073                     | Inländische Steuergrundlagenbetrag nach EU-Umsatz, die einen reduzierten Standardsteuersatz von 10 Prozent haben    | 073                                  |
| 1173                     | Inländische Steuergrundlagenbetrag nach EU-Umsatz, die einen reduzierten Standardsteuersatz von 10 Prozent haben         | 073                                  |
| 1008                     | Inländische Steuergrundlagenbetrag nach EU-Umsatz, die einen reduzierten Standardsteuersatz von 13 Prozent haben    | 008                                  |
| 1108                     | Inländische Steuergrundlagenbetrag nach EU-Umsatz, die einen reduzierten Standardsteuersatz von 13 Prozent haben         | 008                                  |
| 1161                     | Steuerbetrag nach Import                                                | 061                                  |
| 1160                     | Steuerbetrag nach Einkauf                                                       | 060                                  |
| 1165                     | Steuerforderung nach EU-Einkäufe                                                | 065                                  |
| 1132                     | Steuerverbindlichkeiten gemäß dem §19 1d Verbindlichkeiten                                      | 032                                  |
| 1189                     | Steuerverbindlichkeiten gemäß §19 1d Verbindlichkeiten                                   | 089                                  |

Wenn Sie eine Zuweisung von Mehrwertsteuer-Erklärungscodes zu Mehrwertsteuercodes einrichten, wechseln Sie zu <strong>Mehrwertsteuercodes</strong> &gt; *<strong><em>Berichtseinstellung</em></strong>*. Hier ein Beispiel einer Zuweisung von Mehrwertsteuer-Erklärungscodes zu Mehrwertsteuercodes.

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

**Note:** Die vorhergehende Konfiguration ist ein Beispiel und hängt von der Struktur der Mehrwertsteuercodes ab, die verwendet werden und vom Benutzer festgelegt werden. Damit Werte für die Erklärung berechnet und übertragen werde, müssen Sie für jeden Steuercode, der im Mehrwertsteuerzahlungsprozess verwendet wird, einen entsprechenden Mehrwertsteuer-Erklärungscode in einem oder mehrere Felder der Registerkarte **Berichteinstellung** festlegen.

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Konfiguriert das elektronische Berichterstellungsmodell und das Format für den Bericht.
Um die MwSt. -Auszugskonfiguration für juristische Personen in Österreich zu überprüfen, gehen Sie auf die Seitee **Berichtskonfiguration** und wählen **MwsT Deklarationsmodell** in der Liste der Modelle. Dieses Modell wird für Österreich, Tschechische Republik, Estland, Finnland, Lettland und Litauen und für die gesamte Steuerdaten verwendet, die für die Mehrwertsteuererklärung erforderlich sind. Klicken Sie im Aktivitätsbereich auf **Designer**, um das Modell zu prüfen oder zu ändern. Um die MwSt. -Auszugskonfiguration für juristische Personen in Österreich zu überprüfen, gehen Sie auf die Seite **Berichtskonfiguration** und wählen **MwSt Deklarationsmodell** in der Liste der Modelle und wählen dann **U30** unten **MwSt Deklarationsmodell**. Klicken Sie im Aktivitätsbereich auf **Designer**, um das Modell zu prüfen oder das Format zu ändern.

## <a name="generate-a-vat-statement"></a>MwST-Aufstellung generieren
Am Ende der MwSt Berichtsperiode führen Sie **Mehrwertsteuer** **begleichen und buchen** aus, um die Berichtszeilenbeträge für die Definition der Steuerberichtscodes, die Sie erstellt haben, zu berechnen. In der folgenden Tabelle werden die Felder beschrieben, die zur Verfügung stehen.


|           Feld           |                                                                                                                                                                    Beschreibung                                                                                                                                                                     |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Ausgleichsperiode     |                                                                                                                                                      Wählen Sie den gewünschten Berichtszeitraum aus.                                                                                                                                                       |
|         Von Datum         |                                                                                 Geben Sie den ersten Tag des zu berechnenden Mehrwertsteuer-Abrechnungszeitraums an, um die Mehrwertsteuer zu berechnen. Dieser Wert entspricht dem Datum im Feld auf der Mehrwertsteuer-Abrechnungszeitraum-Seite.                                                                                  |
|     Buchungsdatum      | Geben Sie das Datum an, für das die Mehrwertsteuererklärung berechnet wird. Der aktuelle Wert ist das aktuelle Datum. Das Enddatum des Abrechnungszeitraums, der im Feld angezeigt wird, entspricht dem Feld auf der Mehrwertsteuer-Abrechnungszeitraum-Seite. Die Mehrwertsteuerzahlung wird für alle Buchungen berechnet, die im Abrechnungszeitraum gebucht wurden. |
| Mehrwertsteuer, Zahlungsversion |                                                                                                                                  Wählen Sie die Buchungsarten aus, die in die Berechnung der Mehrwertsteuerzahlung einbezogen werden sollen:                                                                                                                                  |

**Original** – Mehrwertsteuerbuchungen für die erste gebuchte Ausgleichsberechnung für das Periodenintervall.
**Letzte Korrekturen** – enthalten Mehrwertsteuerbuchungen, die in der letzten Ausgleichsberechnung für den Zeitraum enthalten sin.| |Format mapping|Specify U30.|d

Um eine MwSt. -XML-Datei zu generieren, verwenden Sie die Seite the **Mehrwertsteuerberichtsausgleichsperiode**.



