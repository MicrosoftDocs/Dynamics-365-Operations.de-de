---
title: Rechnungsabgleich von Kreditorenkonten – Übersicht
description: Beim Kreditorenrechnungsabgleich handelt es sich um den Prozess zum Abgleich der Informationen aus der Kreditorenrechnung, der Bestellung und des Produktzugangs.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b45c6f20bf5b6fb02379f71b5806c6c147789e73
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865063"
---
# <a name="accounts-payable-invoice-matching-overview"></a>Rechnungsabgleich von Kreditorenkonten – Übersicht

[!include [banner](../includes/banner.md)]

Beim Kreditorenrechnungsabgleich handelt es sich um den Prozess zum Abgleich der Informationen aus der Kreditorenrechnung, der Bestellung und des Produktzugangs.

Beim Abgleich von Dokumenten werden Unterschiede zwischen diesen Dokumenten als Abgleichsabweichung bezeichnet. Abgleichsabweichungen werden mit den angegebenen Toleranzen verglichen. Übersteigt die Abgleichsabweichung den Toleranzprozentsatz oder -betrag, werden auf der Seite "Kreditorenrechnung" und auf er Seite "Details zum Rechnungsabgleich" Abweichungssymbole angezeigt. 

Angenommen, Sie geben eine Bestellung mit einem Positionsartikel (1.000 Batterien) zu einem Preis von jeweils 1,00 EUR ein. Die Bestellung wird genehmigt und an den Kreditor übermittelt. Der Kreditor liefert 1.000 Batterien, und Sie geben einen Produktzugang für 1.000 Batterien zu einem Preis von jeweils 1,00 EUR ein. Die Lagerkosten für die Batterien werden mit diesen Preis aktualisiert. 

Eine Rechnung über 1.000 Batterien zu einem Preis von jeweils 1,10 EUR geht ein. Gemäß der Richtlinie für die juristische Person ist bei dieser Artikelkategorie eine Nettostückpreis-Toleranz von 5 Prozent zulässig. Ein Preis von 1,05 EUR wäre also in Ordnung, 1,10 EUR sind jedoch zu viel. Bei der Eingabe der Rechnungsinformationen wird eine Preisabweichung erkannt, und die Rechnung kann gespeichert werden, bis die Abweichung behoben ist.

Die folgenden Arten von Kreditorenrechnungsabgleich können verwendet werden:

-   Rechnungssummenabgleich – Die Gesamtbeträge der Rechnung werden mit den Gesamtbeträgen der Bestellung abgeglichen. Bei dieser Art von Rechnungsabgleich werden die wenigsten Details einbezogen. Deshalb können Sie mit dieser Option Steuerfunktionen zur Minimierung der Arbeitszeit einrichten, die für die Prüfung der Informationen aus dem Abgleich erforderlich ist.
-   Zweiseitiger Abgleich – Die Preisinformationen der Rechnung werden mit den Preisinformationen der Bestellung abgeglichen.
-   Dreiseitiger Abgleich – Die Preisinformationen der Rechnung werden mit den Preisinformationen der Bestellung abgeglichen. Zudem werden die Mengeninformationen der Rechnung mit den Mengeninformationen der Produktzugänge abgeglichen, die für die Rechnung ausgewählt sind.
-   Abgleich für Zuschläge – Die Informationen zu Zuschlägen (Beträge) der Rechnung werden mit den Informationen zu Zuschlägen (Beträge) der Bestellung abgeglichen.

> [!NOTE]
> Mithilfe von Kreditorenrechnungsrichtlinien können weitere Formen der Rechnungsprüfung vorgenommen werden. 

Beim zweiseitigen und beim dreiseitigen Abgleich werden Preisinformationen stets nach dem Einheitspreis abgeglichen. Sie können diese Abgleichsrichtlinien für einen Abgleich der Preisinformationen nach dem Preissumme konfigurieren.
-   Nettostückpreis-Abgleich – Die Preisinformationen beim zweiseitigen oder dreiseitigen Abgleich werden durch einen Vergleich des Nettostückpreises jeder Rechnungsposition mit dem entsprechenden Nettostückpreis der Bestellung abgeglichen. Der Nettostückpreis ergibt sich aus der folgenden Formel: Nettobetrag der Position / die Menge der Position.
-   Preissummenabgleich – Die Preisinformationen beim zweiseitigen oder dreiseitigen Abgleich werden durch einen Vergleich des Nettobetrags (Preissumme) jeder Rechnungsposition mit dem entsprechenden Nettobetrag der Bestellung abgeglichen. Der Nettobetrag ergibt sich aus der folgenden Formel: *(Einheitspreis \* Positionsmenge) + Positionszuschläge - Positionsrabatte*. Bei einem Abgleich der Preissummen nach Prozentsatz vergleicht das System Werte mithilfe der Transaktionswährung. Bei einem Abgleich der Preissummen nach Menge vergleicht das System die Werte mithilfe der Buchungswährung.

Rechnungsabgleichsberechnungen werden in der Regel ausgeführt, wenn Kreditorenrechnungen auf der Seite "Kreditorenrechnung" bearbeitet werden. Alternativ kann der Rechnungsabgleich bei Bedarf ausgeführt werden, falls erforderlich. Der Rechnungsabgleich bei Bedarf wird für die juristischen Person über "Rechnungskopfstatus automatisch aktualisieren" auf der Seite "Kreditorenkontenparameter" in der Registerkarte "Rechnungsprüfung" durchgeführt. Der Rechnungsabgleich kann auch im Rahmen eines Rechnungsprüfungsprozesses erfolgen. Sie können die Ergebnisse eines Rechnungsabgleichs auf der Seite "Kreditorenrechnung" und den zugehörigen Rechnungsabgleichseiten anzeigen.

## <a name="invoice-totals-matching"></a>Rechnungssummenabgleich
Mit dem Rechnungssummenabgleich können Sie sicherstellen, dass die Abweichung der Gesamtbeträge in Rechnungen von den erwarteten Beträgen in einem akzeptablen Rahmen bleibt. Sechs Summen werden auf der Seite "Detailabgleich für Rechnungssummen" verglichen (siehe folgende Tabelle). Wenn die zulässige Toleranz für den Rechnungssummenabgleich bei 20 % liegt, wird der Abweichungsprozentsatz von 100 % für den Gesamtrabattbetrag als Abgleichsabweichung angesehen.

| Summenfeld    | Tatsächliche Rechnungssumme | Erwartete Rechnungssumme | Abweichung in Prozent | Status des Abgleichs |
|----------------|----------------------|------------------------|---------------------|--------------|
| Gesamtbetrag        | 495,00               | 495,00                 | 0 %                  | Erfolgreich       |
| Rechnungsrabatt | 0,00                 | 9,90                   | 100 %                | Fehlgeschlagen       |
| Gebühren        | 64,90                | 64,90                  | 0 %                  | Erfolgreich       |
| Mehrwertsteuer      | 139,98               | 137,50                 | 2 %                  | Erfolgreich       |
| Rundung      | 0,00                 | 0,00                   | 0 %                  | Erfolgreich       |
| Rechnungsbetrag | 699,88               | 687,50                 | 2 %                  | Erfolgreich       |

Der Rechnungssummenabgleich wird für die juristischen Person über die Option "Rechnungssummen abgleichen" auf der Kreditorenparameterseite gesteuert. Der Abgleich wird basierend auf den erwarteten Rechnungssummen und den tatsächlichen Summen ausgeführt. Die Berechnung der erwarteten Rechnungssummen erfolgt basierend auf den Preisen, Zuschlägen und Mehrwertsteuerinformationen aus der Bestellung und auf den Mengen aus der Rechnung.

## <a name="two-way-price-totals-matching"></a>Zweiseitiger Preissummenabgleich
Mit dem zweiseitigen Abgleich können Sie sicherstellen, dass die Abweichung zwischen den Preisinformationen auf der Bestellung und den Rechnungen in einem akzeptablen Rahmen bleibt. Sie können die Preisinformationen für den Nettobetrag der einzelnen Rechnungspositionen sowie alle ausstehenden und bereits gebuchten Rechnungspositionen mit den Nettobetrag der entsprechenden Bestellposition vergleichen. Dieser Vorgang wird Preissummenabgleich genannt. 

Der Preissummenabgleich kann auf einem Prozentsatz, einem Betrag oder auf einem Prozentsatz und Betrag basieren. 

Wenn der Toleranzprozentsatz einer Einkaufspreissumme angegeben wird, werden fünf Felder verglichen (siehe folgende Tabelle). Da der Toleranzprozentsatz der Einkaufspreissumme bei 10 % liegt, stellt der Prozentsatz der Preissummenabweichung von 50 % ein Abgleichsabweichung dar.

| Status des Abgleichs | Nettobetrag der Rechnung | Erwarteter Nettobetrag | Nicht abgeglichene Einkaufspreissumme (Abweichungsbetrag) | Nicht abgeglichene Einkaufspreissumme in Prozent (Abweichung in Prozent) | Toleranz für die Einkaufspreissumme in Prozent |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Erfolgreich       | 105,00             | 100,00              | 5,00                                             | 5 %                                                              | 10 %                                    |
| Fehlgeschlagen       | 150,00             | 100,00              | 50,00                                            | 50 %                                                             | 10 %                                    |

Wenn der Toleranzbetrag einer Einkaufspreissumme angegeben wird, werden fünf Felder verglichen (siehe folgende Tabelle). Da der Toleranzbetrag der Einkaufspreissumme bei 100,00 EUR liegt, stellt der Betrag der Preissummenabweichung von 105,00 EUR ein Abgleichsabweichung dar.

| Status des Abgleichs | Nettobetrag der Rechnung | Erwarteter Nettobetrag | Nicht abgeglichene Einkaufspreissumme (Abweichungsbetrag) | Nicht abgeglichene Einkaufspreissumme in Buchhaltungswährung (Abweichungsbetrag) | Toleranz für die Einkaufspreissumme |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Erfolgreich       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Fehlgeschlagen       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Wenn der Preissummenabgleich mit einen Toleranzprozentsatz und einem Toleranzbetrag (auch als nicht zu überschreitender Betrag bezeichnet) eingerichtet ist, werden beide Toleranzen bei der Auswertung, ob bei der Position eine Abgleichsabweichung vorliegt, berücksichtigt. Überschreitet der Prozentsatz oder der Betrag den Toleranzwert, weist die Position eine Abgleichsabweichung auf, wie an den Positionen 150,00 und 205,00 in der folgenden Tabelle zu sehen ist.

| Status des Abgleichs | Nettobetrag der Rechnung | Erwarteter Nettobetrag | Nicht abgeglichene Einkaufspreissumme in Prozent (Abweichung in Prozent) | Toleranz für die Einkaufspreissumme in Prozent | Nicht abgeglichene Einkaufspreissumme in Buchhaltungswährung (Abweichungsbetrag) | Toleranz für die Einkaufspreissumme |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Erfolgreich       | 105,00             | 100,00              | 5 %                                                              | 10 %                                    | 5,00                                                                    | 100,00                         |
| Fehlgeschlagen       | 150,00             | 100,00              | 50 %                                                             | 10 %                                    | 50,00                                                                   | 100,00                         |
| Fehlgeschlagen       | 205,00             | 100,00              | 105 %                                                            | 10 %                                    | 105,00                                                                  | 100,00                         |

Der zweiseitige Rechnungssummenabgleich wird für die juristische Person gesteuert, die im Feld Positionsabgleichsrichtlinien der Seite Kreditorenparameter angegeben ist. Abhängig von der Auswahl im Feld "Überschreiben der Abgleichsrichtlinie zulassen" können Sie einen zweiseitigen Abgleich für einen bestimmten Kreditor, Artikel oder eine Kombination aus Artikel und Kreditor auf der Seite "Abgleichsrichtlinie" und für eine bestimmte Bestellung auf der Seite "Bestellung" auswählen.

Der Preissummenabgleich wird für die juristischen Person über die Option "Preissummen abgleichen" auf der Kreditorenparameterseite gesteuert. Der Toleranzprozentsatz einer Einkaufspreissumme und der Toleranzbetrag (nicht zu überschreitender Betrag) werden ebenfalls auf dieser Seite angegeben.

## <a name="two-way-net-unit-price-matching"></a>Zweiseitiger Nettostückpreis-Abgleich
Mit dem zweiseitigen Abgleich können Sie sicherstellen, dass die Abweichung zwischen den Preisinformationen auf der Bestellung und der Rechnung in einem akzeptablen Rahmen bleibt. Sie können die Preisinformationen für den Nettostückpreis der einzelnen Artikel in der Rechnung vergleichen. Dieser Vorgang ist der Nettostückpreis-Abgleich. 

Neun Positionsbeträge werden auf der Seite "Details zum Rechnungsabgleich" verglichen (siehe folgende Tabelle). Wenn die zulässige Preistoleranz für den Nettostückpreis-Abgleich bei 10 % liegt, wird der Abweichungsprozentsatz von 22,61 % für den Nettostückpreis als Abgleichsabweichung angesehen.

| Positionsfeld                    | Rechnungswert | Wert der Erstbestellung | Abweichung in Prozent | Status des Abgleichs |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Preis je Einheit                    | 55,40         | 55,38                | 0 %                  | Erfolgreich       |
| Preiseinheit                    | 1,00          | 1,00                 | 0 %                  | Erfolgreich       |
| Belastungen für Einkäufe          | 50,00         | 0,00                 | 100 %                | Fehlgeschlagen       |
| Rabatt                      | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Rabatt in Prozent              | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Sammelrabatt            | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Sammelrabatt (Prozentsatz) | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Nettobetrag                    | 271,60        | 221,52               | 22,61 %              | Fehlgeschlagen       |
| Nettostückpreis                | 67,9000       | 55,3800              | 22,61 %              | Fehlgeschlagen       |

Der zweiseitige Rechnungssummenabgleich wird für die juristische Person gesteuert, die im Feld Positionsabgleichsrichtlinien der Seite Kreditorenparameter angegeben ist. Abhängig von der Auswahl im Feld "Überschreiben der Abgleichsrichtlinie zulassen" können Sie einen zweiseitigen Abgleich für einen bestimmten Kreditor, Artikel oder eine Kombination aus Artikel und Kreditor auf der Seite "Abgleichsrichtlinie" und für eine bestimmte Bestellung auf der Seite "Bestellung" auswählen. 

Der Nettostückpreisabgleich wird für die juristischen Person über die Option "Rechnungsabgleichüberprüfung aktivieren" auf der Kreditorenparameterseite gesteuert. Die Toleranzprozentsätze für Nettostückpreise können auf der Seite "Preistoleranzen" für Artikel, Artikelgruppen, Kreditoren, Kreditorengruppen, Kombinationen aus Artikel und Kreditor oder für eine juristische Person konfiguriert werden.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a>Zweiseitiger Preissummenabgleich und Nettostückpreis-Abgleich
Preissummenabgleich und Nettostückpreis-Abgleich können zusammen verwendet werden. Das folgende Beispiel basiert auf folgender Konfiguration:

-   Die Nettostückpreis-Toleranz für den Artikel "USB-Laufwerk" liegt bei 10 %.
-   Die Preissummenabgleich-Toleranz für die juristische Person liegt bei 15 % oder 500,00 EUR.

Die Bestellung enthält die folgende Position:

| Artikelnummer | Menge | Preis je Einheit | Nettobetrag |
|-------------|----------|------------|------------|
| USB-Laufwerk   | 1.000    | 10,00      | 10.000,00  |

Drei Rechnungen werden wie in der folgenden Tabelle dargestellt eingegeben. Rechnung 3 stellt eine Abweichung beim Rechnungsabgleich dar, da die Abweichung von 1.880,00 EUR den Toleranzbetrag der Einkaufspreissumme von 500,00 EUR übersteigt. Beim Preissummenabgleich schließt der Rechnungsnettobetrag alle bereits gebuchten Rechnungen zusätzlich zur aktuell bearbeiteten Rechnung ein.

| Artikelnummer          | Menge | Preis je Einheit | Nettobetrag | Preisabgleich | Preissummenabgleich |
|----------------------|----------|------------|------------|-------------|-------------------|
| Rechnung 1: USB-Laufwerk | 800      | 10,80      | 8.640,00   | Erfolgreich      | Erfolgreich            |
| Rechnung 2: USB-Laufwerk | 100      | 10,80      | 1.080,00   | Erfolgreich      | Erfolgreich            |
| Rechnung 3: USB-Laufwerk | 200      | 10,80      | 2.160,00   | Erfolgreich      | Fehlgeschlagen            |
| Summe                |          |            | 11.880,00  |             |                   |

## <a name="three-way-matching"></a>Dreiseitiger Abgleich

Verwenden Sie den dreiseitigen Abgleich, um sicherzustellen dass die Abweichung zwischen den Preisinformationen der Bestellung und der Rechnung in einem akzeptablen Rahmen liegt. Außerdem können Sie damit sicherstellen, dass die Menge in der Rechnung mit der Menge in den entsprechenden Produktzugängen übereinstimmt.

Auf der Seite "Details zum Rechnungsabgleich" werden dieselben Positionsbeträge verglichen wie für den zweiseitigen Abgleich. Zudem wird die Menge in der Rechnung mit den erhaltenen Mengen in den Produktzugängen abgeglichen. Weicht die Rechnungsmenge von der abgeglichene Produktzugangsmenge ab, liegt ein Fehler beim Mengenabgleich vor.

| Positionsfeld                    | Rechnungswert | Wert der Erstbestellung | Abweichung in Prozent | Status des Abgleichs |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Preis je Einheit                    | 55,40         | 55,38                | 0 %                  | Erfolgreich       |
| Preiseinheit                    | 1,00          | 1,00                 | 0 %                  | Erfolgreich       |
| Belastungen für Einkäufe          | 50,00         | 0,00                 | 100 %                | Fehlgeschlagen       |
| Rabatt                      | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Rabatt in Prozent              | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Sammelrabatt            | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Sammelrabatt (Prozentsatz) | 0,00          | 0,00                 | 0 %                  | Erfolgreich       |
| Nettobetrag                    | 271,60        | 221,52               | 22,61 %              | Fehlgeschlagen       |
| Nettostückpreis                | 67,9000       | 55,3800              | 22,61 %              | Fehlgeschlagen       |

| Positionsfeld                     | Rechnungswert | Status des Abgleichs |
|--------------------------------|---------------|--------------|
| Rechnungsmenge               | 4,00          |              |
| Gesamtanzahl abgeglichener Produktzugänge | 0,00          | Fehlgeschlagen       |

Der dreiseitige Rechnungssummenabgleich wird für die juristische Person gesteuert, die im Feld Positionsabgleichsrichtlinien der Seite Kreditorenparameter angegeben ist. Abhängig von der Auswahl im Feld "Überschreiben der Abgleichsrichtlinie zulassen" können Sie einen dreiseitigen Abgleich für einen bestimmten Kreditor, Artikel oder eine Kombination aus Artikel und Kreditor auf der Seite "Abgleichsrichtlinie" und für eine bestimmte Bestellung auf der Seite "Bestellung" auswählen.

## <a name="charges-matching"></a>Abgleich von Belastungen
Mit dem Abgleich für Zuschläge können Sie sicherstellen, dass die Abweichung der Zuschlagsbeträge von den erwarteten Beträgen in einem akzeptablen Prozentrahmen bleibt. Die Gesamtbeträge der einzelnen Zuschlagscodes, die für die Rechnung und die Bestellung gelten, werden auf der Seite "Werte für Belastungen vergleichen - Rechnung: Seite, wie in der folgenden Tabelle dargestellt. Wenn die zulässige Toleranz für den Zuschlagscode bei 25 % liegt, wird der Abweichungsprozentsatz von 99.999.999.999,99 % für den Zuschlagscode "Lizenz" als Abgleichsabweichung angesehen.

> [!NOTE] 
> Ein Abweichungsprozentsatz von 99.999.999.999,99 % bedeutet, dass der auf der Bestellung basierende erwartete Betrag null und der tatsächliche Betrag der Rechnung ein positiver Wert ist. 

| Status des Abgleichs von Belastungen | Code für Belastungen (Rechnung) | Tatsächlicher berechneter Gesamtwert | Erwarteter berechneter Gesamtwert | Abweichungsbetrag | Abweichung in Prozent | Toleranzprozentsatz |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Fehlgeschlagen               | Lizenz              | 25                            | 0                               | 25              | 99.999.999.999,99 %  | 25 %                  |
| Erfolgreich               | Fracht              | 200                           | 200                             | 0               | 0 %                  | 25 %                  |
| Fehlgeschlagen               | Eillieferung             | 4                             | 2                               | 2               | 100 %                | 25 %                  |

Der Abgleich von Belastungen wird für die juristischen Person über die Option "Belastungen abgleichen" auf der Kreditorenparameterseite gesteuert. Sie können Toleranzprozentsätze für Abweichungen bei Zuschlägen auf der Seite "Toleranzen für Belastungen" einrichten.

> [!NOTE]
> Der Abgleich für Zuschläge wird nur bei Zuschlägen ausgeführt, für die die Option "Bestellungs- und Rechnungswerte vergleichen" auf der Belastungscodeseite aktiviert ist.

## <a name="related-functionality"></a>Zugehörige Funktionen
Kreditorenrechnungen basieren häufig auf Produktzugängen, die für die tatsächlichen Lieferungen stehen, und weniger auf Bestellungen. In manchen Fällen stimmen die fakturierten Beträge nicht mit den Beträgen der Bestellung überein, in anderen liegt eine Diskrepanz zwischen der Liefermenge und der fakturierten Menge vor. Sie haben folgende Möglichkeiten, um die Verwaltung dieser Informationen zu vereinfachen:
-   Erstellen einer Kreditorenrechnung basierend auf den Produktzugängen. Produktzugänge werden für Rechnungen automatisch vorgeschlagen, und Sie können den zu verwendenden Produktzugang auswählen. Sie können ggf. auch bestimmte Positionsartikel in Produktzugängen aus mehreren Bestellungen auswählen.
-   Anzeigen und Genehmigen von Mengenabweichungen zwischen der fakturierten Menge (Rechnung) und der Eingangsmenge (Produktzugang). Liegt eine Differenz vor, kann die Rechnung gespeichert und später mit einem anderen Produktzugang abgeglichen werden. Alternativ kann auch die Rechnungsmenge der Eingangsmenge angepasst werden.
-   Eingeben von Rechnungsbeträgen, die nicht Teil der ursprünglichen Bestellung waren, um die Rechnungsinformationen mit der vom Kreditor erhaltenen Rechnung abzugleichen. Die Zuschläge für Bestellungen können mit den Zuschlägen für Rechnungen verglichen werden. Sie haben auch die Möglichkeit, Rechnungen Zuschläge hinzuzufügen und diese den Rechnungspositionen zuzuweisen.
-   Anzeigen und Genehmigen von Preisabweichungen zwischen dem Nettostückpreis der Rechnung und dem Nettostückpreis der Bestellung. Sie haben die Möglichkeit zum Einrichten von Preistoleranz-Prozentwerten für juristische Personen, Kreditoren und Artikel. Liegt der Preis in einer Position der Kreditorenrechnung nicht innerhalb der zulässigen Preistoleranz, kann die Rechnung gespeichert werden, bis entweder die Buchung genehmigt wird oder eine Korrektur vom Kreditor eingeht.

Weitere Informationen finden Sie unter [Dreiseitige Abgleichsrichtlinien](three-way-matching-policies.md) und [Einstellungskreditor-Rechnungsabgleichsprüfung](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




