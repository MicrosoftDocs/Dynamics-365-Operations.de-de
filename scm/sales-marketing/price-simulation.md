---
title: Preissimulation
description: "Dieser Artikel enthält Informationen zu Preissimulation für Angebote. Preissimulation unterstützte Sie dabei, die Auswirkung von Abzügen auf künftigen Verkaufspreisen während dem Angebotsprozess zu evaluieren, bevor Sie einen bestimmten Preis festlegen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: c5381ab48e394702c2423de7a5b5cb9166993388
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="price-simulation"></a>Preissimulation

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu Preissimulation für Angebote. Preissimulation unterstützte Sie dabei, die Auswirkung von Abzügen auf künftigen Verkaufspreisen während dem Angebotsprozess zu evaluieren, bevor Sie einen bestimmten Preis festlegen.

In einer Preissimulation für ein Angebot wird ein neuer Gesamtbetrag auf Basis eines neuen vorgeschlagenen Preises angezeigt. In einer Preissimulation kann auch ein neuer Betrag für eine bestimmte Position angezeigt werden, die in einem vorhandenen Angebot erstellt wird. Sie können eine Preissimulation eingeben und zu einem späteren Zeitpunkt verwenden. Alternativ können Sie das ursprüngliche Angebot ohne Preissimulation verwenden und im Laufe des Verkaufsvorgangs weitere Änderungen vornehmen.  

Der Preis im Angebot wird durch eine Preissimulation nicht geändert. Wenn die Preissimulation für ein gesamtes Angebot gilt, wird sie als Sonderrabatt auf den Angebotskopf angewendet. Wenn die Preissimulation für bestimmte Artikel gilt, wird sie als Sonderrabatt auf die Angebotspositionen angewendet. Der Verkaufspreis pro Einheit in einer erstellten Angebotsposition wird bei Anwendung einer Preissimulation nicht geändert. Stattdessen wird ein Rabattprozentsatz angewendet, der der Preisverringerung für die Angebotsposition entspricht. Durch Anwenden einer Preissimulation werden der Verkaufspreis pro Einheit sowie der Rabattprozentsatz in die Angebotsposition oder in den Angebotskopf übertragen.  

**Hinweis:** Bei Ausführung einer Preissimulation wird für die Simulationserstellung ausschließlich die aktuelle Verkaufswährung verwendet. Beim Anzeigen der Angebotssummen wird dann allerdings eine Kombination aus Unternehmenswährung und Verkaufswährung angezeigt.  

Zusätzliche zu den Positionen eines Angebots hinzugefügte Artikel können die Anwendung von Positionsrabatten oder Sammelrabatten zur Folge haben. Sie können auch zur Aktivierung von Rechnungsrabatten führen, durch die sich Gewinnspanne und Deckungsbeitrag der Angebotspositionen sowie des gesamten Rabatts ändern.  

Sie haben die Möglichkeit zum Ausführen mehrerer Preissimulationen, um so die Auswirkungen von Preisregulierungen auf die Zielgruppen eines Angebots zu verfolgen. Die Ausführung dieser Simulationen ermöglicht eine Regulierung des Gesamtangebotspreises oder der Preise bestimmter Angebotspositionen, um schließlich die Preissimulation mit der höchsten Wahrscheinlichkeit für einen Geschäftsabschluss anzuwenden.  

Bei der Erstellung eines Angebots können Sie eine Warnung einrichten. Nachfolgend einige der Einsatzbereiche von Warnungen aufgeführt:

-   Warnungen können über den Status von Angeboten in der Organisation informieren.
-   Warnungen können eine Überprüfung eines bestimmten Angebots auslösen oder Sie bei Überschreitung von Rabattgrenzen informieren.

## <a name="price-simulation-and-discounts"></a>Preissimulation und Rabatte
Gehen Sie beim Ausführen von Preissimulationen für Angebote mit Rabatten sorgfältig vor, um eine ordnungsgemäße Berechnung der Rabatte und Preise sicherzustellen. Da alle Preissimulationen als Sonderrabatte auf die aktive Angebotsposition oder auf das gesamte Angebot behandelt werden, müssen die Unterschiede bei den Rabatten erfasst werden.

### <a name="types-of-discounts-in-trade-agreements"></a>Rabatttypen in Handelsvereinbarungen

Für die Handelsvereinbarungen in Microsoft Dynamics 365 for Finance and Operations stehen vier verschiedene Typen von Preisrabatten zur Auswahl. Diese Rabatte können für unterschiedliche Artikel, Debitoren oder Preisgruppen festgelegt sowie mithilfe eines Datums beschränkt werden. Zur Vermeidung von Berechnungsfehlern müssen beim Ausführen von Preissimulationen Handelsvereinbarungen berücksichtigt werden. Folgende vier Arten von Rabatten stehen in Handelsvereinbarungen zur Verfügung:

-   **Verkaufspreis** – Für Artikel können separate Verkaufspreise angegeben werden. Der korrekte Artikelverkaufspreis wird beim Erstellen der Angebotspositionen vom Programm gesucht und an die Angebotspositionen übertragen. Das bedeutet, dass die Preissimulation durch eine Handelsvereinbarung mit diesem Rabatttyp nicht beeinflusst wird. Der Verkaufspreis, der in der Angebotsposition verwendet wird, spiegelt die Handelsvereinbarung wider.
-   **Positionsrabatt** – Es wird ein besonderer Artikelrabatt angegeben, der von der bestellten Menge abhängt. Die Positionsbeträge werden üblicherweise um den Positionsrabatt verringert, bevor eine Preissimulation ausgeführt wird. Das bedeutet, dass die Preissimulation durch eine Handelsvereinbarung mit diesem Rabatttyp beeinflusst wird.
-   **Sammelrabatt** – Übersteigen die kombinierten Beträge den von Ihnen festgelegten Grenzwert, wird durch zuvor definierte Kombinationen bestellter Artikel ein Rabatt auf den gesamten Auftrag gewährt. Die Positionsbeträge werden üblicherweise um den Positionsrabatt verringert, bevor eine Preissimulation ausgeführt wird. Das bedeutet, dass die Preissimulation durch eine Handelsvereinbarung mit diesem Rabatttyp beeinflusst wird.
-   **Rechnungsrabatt** – Übersteigen die kombinierten Beträge den von Ihnen festgelegten Grenzwert, wird durch zuvor definierte Artikel ein Rabatt auf den gesamten Auftrag gewährt. Der Rechnungsrabatt wird durch die Positionen des Angebots generiert. Er wird jedoch als Rabatt auf den Gesamtbetrag angewendet, wodurch sich der Gesamtbetrag des Angebots verringert. Das bedeutet, dass die Preissimulation durch eine Handelsvereinbarung mit diesem Rabatttyp beeinflusst wird.

### <a name="quotation-lines-and-trade-agreements"></a>Angebotspositionen und Handelsvereinbarungen

Beim Erstellen oder Anpassen einer Angebotsposition werden die Positionsrabatte automatisch berechnet. Der entsprechende Verkaufspreis eines Artikels (gemäß Handelsvereinbarung) wird gesucht.

## <a name="price-simulation-examples"></a>Beispiele für Preissimulationen
In den folgenden Beispielen werden Preissimulationen für den Angebotskopf sowie für Artikel einzelner Positionen verwendet.

### <a name="price-simulation-for-quotation-headers"></a>Preissimulation für Angebotsköpfe

Situation: Erstellung eines Angebots mit den folgenden Positionen:

-   10 Einheiten des Artikels "BR-12" (Einstandspreis pro Einheit: EUR 9,52; Verkaufspreis pro Einheit: EUR 15,32)
-   12 Einheiten des Artikels "BR-14" (Einstandspreis pro Einheit: EUR 7,48; Verkaufspreis pro Einheit: EUR 13,75)

Die Angebotspositionen werden in der folgenden Tabelle veranschaulicht.

|                            | Herstellkostenkalkulation                          | Ergebnis   |
|----------------------------|--------------------------------------|----------|
| Verkaufsmenge             | 10 Einheiten + 12 Einheiten                  | 22 Einheiten |
| Verkaufswert in EUR         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Einstandswert in EUR          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Gewinnspanne in EUR | 318,20 – 184,96                      | 133,24   |
| Deckungsbeitragsverhältnis         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87 %   |

Sie führen eine Preissimulation mit einem Rechnungsrabatt von 15 % auf das gesamte Angebot oder auf den Angebotskopf aus. In der folgenden Tabelle werden die neuen Summen des Angebots nach dem Ausführen der Preissimulation angezeigt.

|                                                      | Berechnung                               | Ergebnis   |
|------------------------------------------------------|-------------------------------------------|----------|
| Verkaufsmenge                                       | 10 Einheiten + 12 Einheiten                       | 22 Einheiten |
| Alter Verkaufswert in EUR                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Alter Einstandswert in EUR                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Alte Gewinnspanne in EUR                       | 318,20 – 184,96                           | 133,24   |
| Alter Deckungsbeitrag                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87 %   |
| Preissimulation: Rechnungsrabatt von 15 % in EUR | (15 × 318,2) ÷ 100                        | 47,73    |
| Neuer Verkaufswert in EUR                               | 318,20 – 47,73                            | 270,47   |
| Neue Gewinnspanne in EUR                       | 270,47 – 184,96                           | 85,51    |
| Neues Deckungsbeitragsverhältnis                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61 %   |

### <a name="price-simulation-for-single-line-items"></a>Preissimulation für einzelne Positionen

Situation: Erstellung eines Angebots mit den folgenden Positionen:

-   10 Einheiten des Artikels "BR-12" (Einstandspreis pro Einheit: EUR 9,52; Verkaufspreis pro Einheit: EUR 15,32)
-   12 Einheiten des Artikels "BR-14" (Einstandspreis pro Einheit: EUR 7,48; Verkaufspreis pro Einheit: EUR 13,75)

Die Angebotspositionen werden in der folgenden Tabelle veranschaulicht.

|                                      | Herstellkostenkalkulation                          | Ergebnis   |
|--------------------------------------|--------------------------------------|----------|
| Verkaufsmenge                       | 10 Einheiten + 12 Einheiten                  | 22 Einheiten |
| Verkaufswert in EUR für "BR-12"         | 10 × 15,32                           | 153,20   |
| Verkaufswert für "BR-14" in EUR         | 12 × 13,75                           | 165,00   |
| Einstandswert für "BR-12" in EUR          | 10 × 9,52                            | 95,20    |
| Einstandswert für "BR-14" in EUR          | 12 × 7,48                            | 89,76    |
| Gewinnspanne für "BR-12" in EUR | 153,20 - 95,20                       | 58,00    |
| Gewinnspanne für "BR-14" in EUR | 165,00 - 89,76                       | 75,24    |
| Deckungsbeitrag für "BR-12" in EUR  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Deckungsbeitrag für "BR-14" in EUR  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Verkaufswert in EUR (gesamt)             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Einstandswert in EUR (gesamt)              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Gewinnspanne in EUR (gesamt)     | 318,20 – 184,96                      | 133,24   |
| Deckungsbeitrag (gesamt)             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87 %   |

Sie führen eine Preissimulation mit einem Rechnungsrabatt von 10 % auf Einheiten des Artikels "BR-12" durch. In der folgenden Tabelle werden die neuen Summen des Angebots angezeigt, nachdem die Preissimulation für die einzelne Position ausgeführt wurde.

|                                                   | Berechnung                             | Ergebnis   |
|---------------------------------------------------|-----------------------------------------|----------|
| Verkaufsmenge                                    | 10 Einheiten + 12 Einheiten                     | 22 Einheiten |
| Alter Verkaufswert für "BR-12" in EUR                  | 10 × 15,32                              | 153,20   |
| Preissimulation: 10 % Rabatt für "BR-12" | (10 × 153,2) ÷ 100                      | 15,32    |
| Neuer Verkaufswert für "BR-12" in EUR                  | (10 × 15,32) – 15,32                    | 137,88   |
| Verkaufswert für "BR-14" in EUR                      | 12 × 13,75                              | 165,00   |
| Einstandswert für "BR-12" in EUR                       | 10 × 9,52                               | 95,20    |
| Einstandswert für "BR-14" in EUR                       | 12 × 7,48                               | 89,76    |
| Neue Gewinnspanne für "BR-12" in EUR          | 137,88 - 95,20                          | 42,68    |
| Gewinnspanne für "BR-14" in EUR              | 165,00 - 89,76                          | 75,24    |
| Neuer Deckungsbeitrag für "BR-12" in EUR           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Deckungsbeitrag für "BR-14" in EUR               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Neuer Verkaufswert in EUR (gesamt)                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Einstandswert in EUR (gesamt)                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Neue Gewinnspanne in EUR (gesamt)              | 302,88 – 184,96                         | 117,92   |
| Neues gesamtes Deckungsbeitragsverhältnis                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93%   |

Die Preissimulation wirkt sich nur auf die ausgewählte Position aus, wodurch sich die Summe dieser Position verringert.




