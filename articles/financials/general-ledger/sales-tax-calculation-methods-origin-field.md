---
title: Mehrwertsteuer-Berechnungsmethoden im Feld "Ursprung"
description: "In diesem Artikel wird beschrieben die Optionen im Feld \"Ursprung\" auf der Mehrwertsteuercodeseite und wie Mehrwertsteuer basierend auf der ausgewählten Option für einen Mehrwertsteuercode berechnet wird."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f420341a7d5d12825a983ee96e814f0eedbc60c4
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Mehrwertsteuer-Berechnungsmethoden im Feld "Ursprung"

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


In diesem Artikel wird beschrieben die Optionen im Feld "Ursprung" auf der Mehrwertsteuercodeseite und wie Mehrwertsteuer basierend auf der ausgewählten Option für einen Mehrwertsteuercode berechnet wird.

Für jeden Mehrwertsteuercode, der auf der Seite "Mehrwertsteuercodes" erstellt wird, wählen Sie im Feld "Ursprung" die Berechnungsmethode aus, die auf den Steuergrundbetrag angewendet werden soll.

## <a name="percentage-of-net-amount"></a>Prozentanteil am Nettobetrag
Die Berechnungsmethode "Prozentanteil am Nettobetrag" ist der Standardwert im Feld "Ursprung". Hierbei wird die Mehrwertsteuer als Prozentanteil der Einkaufs- oder Verkaufssumme ohne irgendwelche anderen Verkaufssteuern berechnet.
### <a name="example"></a>Beispiel

Mehrwertsteuersatz = 25 % Unter der Rechnungsposition wird eine Menge von 10 Artikeln zu je 1,00 angezeigt, und der Debitor erhält einen Positionsrabatt von 10 %. Nettobetrag: (10 x 1,00) Mehrwertsteuer -10 % = 9,00: 9,00 x 25 % = 2,25 Gesamtbetrag: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Prozentanteil am Bruttobetrag
Wenn Sie die Methode "Prozentanteil am Bruttobetrag" auswählen, wird die Mehrwertsteuer als Prozentanteil der Bruttoverkaufssumme berechnet. Der Bruttobetrag ist der Positionsnettobetrag einschließlich aller Steuern und Gebühren für die Position mit Ausnahme der Steuer mit Ursprung = Prozentanteil am Bruttobetrag.
### <a name="example"></a>Beispiel

Die Steuerbehörde sieht für einen Artikel die Zahlung spezieller Abgaben vor. Der Abgabenbetrag wird zum Nettobetrag hinzuaddiert, bevor die Mehrwertsteuer berechnet wird. Folgende Mehrwertsteuercodes werden verwendet:
-   ABGABE 1 = 10 %, mit Berechnungsmethode "Prozentanteil am Nettobetrag"
-   ABGABE 2 = 20 %, mit Berechnungsmethode "Prozentanteil am Nettobetrag"
-   MEHRWERTSTEUER = 25 %, mit Berechnungsmethode "Prozentanteil am Bruttobetrag"

Wenn der Nettobetrag 10,00 beträgt, dann ist ABGABE 1 "1,00 (10,00 x 10 %)" und ABGABE 2 "2,00 (10,00 x 20 %)". Die Beträge wären wie folgt: Bruttobetrag: Nettobetrag + Betrag ABGABE 1 + Betrag ABGABE 2 (10,00 + 1,00 + 2,00) = 13,00 MEHRWERTSTEUER = 13,00 x 25 % = 3,25 gesamte ABGABEN und MEHRWERTSTEUER: 1,00 + 2,00 + 3,25 = 6,25 Gesamtbetrag: 10,00 + 6,25 = 16,25
| **Hinweis**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nur ein Steuercode mit Ursprung = "Prozentanteil des Bruttobetrags" kann für eine Buchung verwendet werden. Wenn mehr als ein Steuercode für eine Buchung bestimmt wird, wird ein Fehler angezeigt, dass keine Steuer berechnet werden kann. |

 
<a name="percentage-of-sales-tax"></a>Mehrwertsteuer-Prozentsatz
-----------------------

Wenn Sie im Feld "Ursprung" die Berechnungsmethode "Mehrwertsteuer-Prozentsatz" auswählen, wird die Mehrwertsteuer als Prozentsatz der im Feld "Mehrwertsteuer auf Mehrwertsteuer" ausgewählten Mehrwertsteuer berechnet. Die im Feld "Mehrwertsteuer auf Mehrwertsteuer" ausgewählte Mehrwertsteuer wird zuerst berechnet. Die zweite Mehrwertsteuer wird anschließend auf Basis des ersten Mehrwertsteuerbetrags berechnet.
### <a name="example"></a>Beispiel

Folgende Mehrwertsteuercodes werden verwendet:
-   ABGABE 1 = 10 %, mit Methode "Prozentanteil am Nettobetrag"
-   ABGABE 2 = 20 %, mithilfe der Methode "Mehrwertsteuer-Prozentsatz" und mit Abgabe 1 im Feld "Mehrwertsteuer auf Mehrwertsteuer"
-   MEHRWERTSTEUER = 25 %, mit Methode "Prozentanteil am Bruttobetrag"

Nettobetrag: 10,00 ABGABE 1: 10,00 x 10 % = 1,00 ABGABE 2: 1,00 x 20 % = 0,20 Bruttobetrag: 10,00 + 1,00 + 0,20 = 11,20 MEHRWERTSTEUER: 11,20 x 25 % = 2,80 ABGABE und MEHRWERTSTEUER gesamt: 1,00 + 0,20 + 2,80 = 4,00 Gesamtbetrag: 10,00 + 4,00 = 14,00
| **Hinweis**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mehrstufige Berechnungen für Steuer auf Steuer sind nicht möglich. Eine Steuer kann nicht basierend auf einer Steuer berechnet werden, die bereits auf Basis einer anderen Steuer berechnet wurde. Mehrere einstufige "Steuer auf Steuer"-Codes können für eine Buchung berechnet werden. |

## <a name="amount-per-unit"></a> Betrag pro Einheit
Wenn Sie "Betrag pro Einheit" im Feld "Ursprung" auswählen, wird die Mehrwertsteuer als fester Betrag pro Einheit multipliziert mit der Menge berechnet, die für die Dokumentposition eingegeben wurde. Eine Einheit muss im Feld "Einheit" ausgewählt werden. Der Betrag pro Einheit wird auf der Seite "Mehrwertsteuer-Codewerte" angegeben.
### <a name="example"></a>Beispiel

Der Mehrwertsteuercode wird folgendermaßen eingerichtet: EUR 1,20 pro Einheit = Schachtel, bei einer Verkaufsrechnungsposition von 25 Schachteln eines verkauften Artikels wird die Verkaufsmehrwertsteuer berechnet als 25 x 1,20 = 30,00
| **Hinweis**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wenn die Buchung in einer anderen Einheit eingegeben wurde als die im Mehrwertsteuercode angegebene, wird sie automatisch basierend auf der Einheitenumrechnung umgewandelt, die auf der Seite "Einheitenumrechnungen" eingerichtet wurde. |

###  <a name="amount-per-unit-additional-option"></a> Berechnungsmethode "Betrag pro Einheit", zusätzliche Option

Auf der Registerkarte "Berechnung" können Sie auswählen, ob ein berechneter Steuerbetrag pro Einheit vor einem anderen Steuercode berechnet und zum Nettobetrag hinzuaddiert wird, bevor andere Steuercodes mit Ursprung = "Prozentanteil am Nettobetrag" berechnet werden.

### <a name="examples"></a>Beispiele

Wir gehen von der Berechnung von 2 Steuercodes in einer Buchung aus:

-   ABGABE: Ursprung = Betrag pro Einheit und Mehrwertsteuer, der Wert wird auf 5,00 pro Einheit = Stck. festgelegt
-   MEHRWERTSTEUER: Ursprung = (siehe Beispiele weiter unten, der Wert wird auf 25 % festgelegt

Wir verkaufen 1 Stück eines Artikels zu einem Einheitenpreis von 10,00
#### <a name="example-1"></a>Beispiel 1

MEHRWERTSTEUER: Ursprung = Methode "Prozentanteil des Bruttobetrags", Option "Vor Mehrwertsteuer berechnen"hat keine Auswirkung, denn MEHRWERTSTEUER wird als Prozentanteil des Bruttobetrags berechnet. ANGABE: 1 x 5,00 = 5.00 Bruttobetrag: 10,00 + 5,00 = 15.00 MEHRWERTSTEUER: 15,00 x 25 % = 3,75 Mehrwertsteuer insgesamt: 5,00 + 3,75 = 8,75 Gesamtbetrag: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Beispiel 2

MEHRWERTSTEUER: Ursprung = "Prozentanteil des Nettobetrags", Option "Vor Mehrwertsteuer berechnen" wird für die Berechnung der ABGABE nicht ausgewählt. Nettobetrag: 10,00 ABGABE: 1 x 5,00 = 5,00 MEHRWERTSTEUER: 10,00 x 25 % = 2.50 Mehrwertsteuer gesamt: 5,00 + 2,50 = 7,50 Gesamtbetrag: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Beispiel 3

MEHRWERTSTEUER: Ursprung = "Prozentanteil des Nettobetrags", Option "Vor Mehrwertsteuer berechnen" wird für die Berechnung der ABGABE ausgewählt. Nettobetrag: 10,00 ABGABE: 1 x 5,00 = 5,00 MEHRWERTSTEUER: (10,00 + 5,00) x 25 % = 3.75 Mehrwertsteuer gesamt: 5,00 + 3,75 = 8,75 Gesamtbetrag: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Beispiel 4

Die Ergebnisse von Beispiel 3 und Beispiel 1 sind gleich, da es nur eine Abgabe gibt. Angenommen, es gibt zwei ABGABEN, und nur eine davon wird in den Nettobetrag für die Mehrwertsteuerberechnung eingeschlossen: ABGABE 1: 5,00, mithilfe der Methode "Betrag pro Einheit" und ausgewählter Option "Vor Mehrwertsteuer berechnen"; ABGABE 2: 2,50, mithilfe der Methode "Betrag pro Einheit" und deaktivierter Option "Vor Mehrwertsteuer berechnen"; Mehrwertsteuer: 25 %, mithilfe der Methode "Prozentanteil am Nettobetrag"; Nettobetrag: 10,00 ABGABE 1: 1 x 5,00 = 5,00 ABGABE 2: 1 x 2,50 = 2,50 Nettobetrag für Mehrwertsteuer: 10,00 + 5,00 = 15,00 MEHRWERTSTEUER: 15,00 x 25 % = 3,75 Gesamtumsatzsteuern, einschließlich Abgaben: 5,00 + 2,50 + 3,75 = 11,25 Gesamtbetrag: 10,00 + 11,25 = 21,25 mit 25 % MEHRWERTSTEUER wird für die Summe aus dem Nettobetrag (10,00) + ABGABE 1 (5,00) = 15,00 berechnet. ABGABE 2 wird nach der Berechnung der Mehrwertsteuer zum Steuerbetrag hinzuaddiert.

## <a name="calculated-percentage-of-net-amount"></a> Berechneter Prozentanteil am Nettobetrag
Die Methode "Berechneter Prozentanteil am Nettobetrag" berechnet die Steuer je nach den Einstellungen des Parameters "Beträge einschließlich Mehrwertsteuer" für das Dokument oder die Erfassung anders.
### <a name="example-1"></a>Beispiel 1

Dokument/Erfassung ist auf "Beträge einschließlich Mehrwertsteuer" festgelegt = Ja; Buchungspositionsbetrag: 10,00; Steuersatz: 25 % Mehrwertsteuer; Betrag des Steuersatzes der Buchungsposition x (10,00 x 25 %) = 2,50; Steuergrundlagenbetrag (Ursprungsbetrag): Buchungspositionsbetrag - Mehrwertsteuer (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Beispiel 2

Dokument/Erfassung ist auf "Beträge einschließlich Mehrwertsteuer" festgelegt = Nein; Buchungspositionsbetrag: 10,00; Steuersatz: 25 % Mehrwertsteuer: (Betrag des Steuersatzes der Buchungsposition) / (100 - Steuersatz) (10,00 x 25 %) / (100 % - 25 %) = 3,33; Steuergrundlagenbetrag (Ursprungsbetrag): Buchungspositionsbetrag = 10,00



<a name="see-also"></a>Siehe auch
--------

[Bestimmen von Mehrwertsteuersteuersätzen auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode](marginal-base-field.md)

[Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes](whole-amount-interval-options-sales-tax-codes.md)




