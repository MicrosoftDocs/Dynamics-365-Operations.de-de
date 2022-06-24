---
title: Eine Zahlung zum Ausgleichen von Rechnungen verwenden, die sich über mehrere Rabattperioden erstrecken
description: Dieser Artikel zeigt, wie mehrere Rechnungen bezahlt werden, wenn jede einzelne Rechnung zum Abzug eines Skontos berechtigt ist. Die Szenarien in diesem Artikel zeigen auf, wie Skonti je nach Zeitpunkt der Zahlung variieren.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6035973abea9dacd4b6d4d8bf2fd3c7d6b10fb0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872643"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Eine Zahlung zum Ausgleichen von Rechnungen verwenden, die sich über mehrere Rabattperioden erstrecken

[!include [banner](../includes/banner.md)]

Dieser Artikel zeigt, wie mehrere Rechnungen bezahlt werden, wenn jede einzelne Rechnung zum Abzug eines Skontos berechtigt ist. Die Szenarien in diesem Artikel zeigen auf, wie Skonti je nach Zeitpunkt der Zahlung variieren.

Fabrikam verkauft Waren an Kunde 4032. Fabrikam bietet ein Skonto von 1 % an, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird. Fabrikam bietet auch Skonti auf Teilzahlungen an. Die Ausgleichsparameter sind auf der Seite **Debitorenkontenparameter** Seite verfügbar.

## <a name="invoices"></a>Rechnungen
Debitor 4032 hat drei Rechnungen, die Summe ist 3.000,00:

-   Rechnung FTI-10040, für 1.000,00 wurde am 15. Mai eingegeben. Von dem Rechnungsbetrag wird ein Skonto von 1 % abgezogen, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird.
-   Rechnung FTI-10041, für 1.000,00 wurde am 25. Mai eingegeben. Von dem Rechnungsbetrag wird ein Skonto von 1 % abgezogen, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird.
-   Rechnung FTI-10042, für 1.000,00 wurde am 25. Mai eingegeben. Diese Rechnung berechtigt für einen Rabatt von 2 Prozent, wenn sie in fünf Tagen und einen Rabatt von 1 Prozent, wenn sie in 14 Tagen bezahlt wird.

## <a name="settle-all-invoices-on-june-29"></a>Begleichen aller Rechnungen am 29. Juni
Wenn Arnie eine Zahlungserfassung erstellt, um diese Rechnungen am 29. Juni vollständig zu begleichen, beträgt die Zahlung 2.970,00. Die Summe aller Rabattbeträge ist 30.00. Arnie erstellt eine Zahlung für Debitor 4032 und öffnet anschließend die Seite **Buchungen ausgleichen**. Auf der Seite **Buchungen ausgleichen** markiert Arnie alle drei Rechnungspositionen für den Ausgleich:

-   Die Zahlung der Rechnung FTI-10040 beträgt 1.000,00. Es wird kein Skonto genommen.
-   Die Zahlung der Rechnung FTI-10041 beträgt 990,00. Ein Skonto von 1 Prozent oder 10,00 wird in Anspruch genommen.
-   Die Zahlung der Rechnung FTI-10042 beträgt 980,00. Ein Skonto von 2 Prozent oder 20,00 wird in Anspruch genommen.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Ausgewählt                 | Normal            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1.000,00                             |                                       | USD      | 1.000,00         |
| Ausgewählt                 | Normal            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1.000,00                             |                                       | USD      | 990,00           |
| Ausgewählt und hervorgehoben | Normal            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1.000,00                             |                                       | USD      | 980,00           |

Nachdem die Zahlung gebucht wurde, ist der Debitorensaldo 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Begleichen aller Rechnungen am 1. Juli
Wenn Arnie eine Zahlungserfassung erstellt, um diese Rechnungen am 1. Juli vollständig zu begleichen, beträgt die Zahlung 2.980,00. Arnie erstellt eine Zahlung für Debitor 4032 und öffnet anschließend die Seite **Buchungen ausgleichen**. Auf der Seite **Buchungen ausgleichen** markiert Arnie alle drei Rechnungspositionen für den Ausgleich:

-   Die Zahlung der Rechnung FTI-10040 beträgt 1.000,00. Es wird kein Skonto genommen.
-   Die Zahlung der Rechnung FTI-10041 beträgt 990,00. Ein Skonto von 1 Prozent oder 10,00 wird in Anspruch genommen.
-   Die Zahlung der Rechnung FTI-10042 beträgt 990,00. Ein Skonto von 1 Prozent oder 10,00 wird in Anspruch genommen. Obwohl der 1. Juli nach der Periode ist, für die der 2-Prozent Rabatt gilt, liegt er immer noch in der Periode, für die der 1-Prozent-Rabatt gilt.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Ausgewählt                 | Normal            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1.000,00                             |                                       | USD      | 1.000,00         |
| Ausgewählt                 | Normal            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1.000,00                             |                                       | USD      | 990,00           |
| Ausgewählt und hervorgehoben | Normal            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1.000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Teilausgleich am 29. Juni
Debitor 4032 kann einen Teilbetrag, wie etwa die Hälfte jeder Rechnung, bezahlen. Arnie erstellt eine Zahlung für Debitor 4032 und öffnet anschließend die Seite **Buchungen ausgleichen**. Auf der Seite **Buchungen ausgleichen** markiert Arnie alle drei Rechnungspositionen für den Ausgleich. Für jede Position gibt Arnie den auszugleichenden Betrag auf Grundlage der Anweisungen ein, die dem Debitor bereitgestellt werden. Wenn Arnie eine Position auswählt, sieht Arnie den Rabattbetrag für diese Position und den Skontobetrag, der veranschlagt wird. Da der Debitor die Hälfte der Rechnung bezahlt, sieht Arnie, dass der Wert im Feld **Skontobetrag** für FTI-10042 **20,00** betragt, aber der Wert im Feld **In Anspruch genommener Skonto** beträgt **10,00**. Der Zahlungsbetrag ist 1,485.00.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Ausgewählt                 | Normal            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1.000,00                             |                                       | USD      | 500,00           |
| Ausgewählt                 | Normal            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1.000,00                             |                                       | USD      | 495,00           |
| Ausgewählt und hervorgehoben | Normal            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1.000,00                             |                                       | USD      | 490,00           |

Arnie kann auch manuell den Zahlungsbetrag von 1.485,00 eingeben, bevor die Seite **Bankbuchungen** geöffnet wird. Wenn Arnie manuell den Zahlungsbetrag eingeben und dann alle drei Buchungen markiert hat, doch den Wert im Feld **Auszugleichenden Betrag** nicht für jede Buchung anpasst, erhält Arnie beim Schließen der Seite folgende Nachricht:

> Der Gesamtbetrag der markierten Transaktionen unterscheidet sich vom Erfassungsbetrag. Erfassungsbetrag ändern?

Wenn Arnie will, dass der Zahlungsbetrag nur 1.485,00 ist, klickt Arnie auf **Nein** und bucht anschließend die Erfassung. Die Buchungen werden ausgeglichen, wie folgt:

1.  Rechnung FTI-10040 ist vollständig für 1.000,00 ausgeglichen, da sie am 15. Mai eingegeben wurde und sie ist die älteste Rechnung. Es wird kein Skonto genommen. Der verbleibende Betrag der Zahlungsbuchung ist 485,00.
2.  Rechnung FTI-10041 wird gar nicht ausgeglichen. Rechnungen FTI-10041 und FTI-10042 wurden gleichzeitig eingegeben. Allerdings ist für Rechnung FTI-10041 ein 1-Prozent-Rabatt verfügbar, und für Rechnung FTI-10042 ist ein 2-Prozent-Rabatt verfügbar. Da ein besserer Rabatt für FTI-10042 verfügbar ist, werden die verbleibenden 485,00 mit Rechnung FTI-10042 ausgeglichen.
3.  Rechnung FTI-10042 wird mit den restlichen 485,00 ausgeglichen. Fabrikam bietet Teilrabatte. In diesem Fall beträgt der Rabatt 9,90 (= 485,00 ÷ 0,98 × 0,02). Der Betrag (485,00) wird durch 0,98 dividiert, da es einen 2-Prozent Rabatt gibt (daher zahlt der Debitor 98 Prozent der Rechnung). Das Ergebnis wird dann mit dem Rabattprozentsatz oder 2 Prozent multipliziert. Die Zahlung von 485,00 plus dem Rabatt von 9,90 ist gleich 494,90. Der Betrag der ursprünglichen Rechnung war 1.000,00. Daher hat die Transaktion ein Saldo von 505,10 (= 1.000,00 - 494,90).

Auf der Seite **Debitorenbuchungen** zeigt Arnie diese Transaktion an.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag  | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Rechnung          | 5/15/2015 | 10040   | 1.000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Rechnung          | 6/25/2015 | 10041   | 1.000,00                             |                                       | 1.000,00 | USD      |
| FTI-10042  | Rechnung          | 6/25/2015 | 10042   | 1.000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Zahlung          | 6/29/2015 |         |                                      | 1.485,00                              | 0,00     | USD      |
| DISC-10040 | Skonto    | 6/29/2015 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
