---
title: Teilzahlungen vor dem Rabattdatum ausgleichen und vollständige Zahlung nach dem Rabattdatum
description: Dieser Artikel führt Sie durch ein Szenario, in dem mehrere Teilzahlungen erfolgen, einige innerhalb des Skontoperiode und andere außerhalb der Skontoperiode.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 828c82d88bef1d942af1219505af591d27043fa5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780537"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Teilzahlungen vor dem Rabattdatum ausgleichen und vollständige Zahlung nach dem Rabattdatum

[!include [banner](../includes/banner.md)]

Dieser Artikel führt Sie durch ein Szenario, in dem mehrere Teilzahlungen erfolgen, einige innerhalb des Skontoperiode und andere außerhalb der Skontoperiode.

Fabrikam-Einkaufwaren Kreditor von 3057. Fabrikam erhält ein Skonto von 1 % an, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird. Rechnungen müssen in 30 Tagen bezahlt werden. Der Kreditor ermöglicht Fabrikam auch, Skonti auf Teilzahlungen zu erhalten. Die Ausgleichsparameter sind auf der Seite **Kreditorenkontenparameter** verfügbar.

## <a name="invoice-on-june-25"></a>Rechnung am 25. Juni
Am 25. Juni gibt April eine Rechnung für 1.000,00 für den Kreditor 3057 ein und bucht diese. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion anzeigen.

| Beleg   | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Saldo   | Währung |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Rechnung          | 25.06.2020 | 10020   |                                      | 1,000.00                              | -1.000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Teilzahlung am 2. Juli
Am 2. Juli möchte April 300,00 Euro dieser Rechnung ausgleichen. Die Zahlung ist für einen Skonto berechtigt, da Fabrikam Rechnungsrabatte im Teilzahlungen nimmt. Daher zahlt April 297,00 und nimmt einen Rabatt von 3,00. Sie erstellt eine Zahlungserfassung und gibt die Position für Kreditor 3057 ein. Sie öffnet anschließend die Seite **Buchungen ausgleichen**, sodass sie die Rechnung zum Ausgeleichen markieren kann.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | Inv-10020 | 3057    | 25.06.2020 | 25.07.2020 | 10020   | -1.000,00                      | USD      | -297,00          |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 09.07.2020 |
| Skontobetrag         | -10,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -3,00     |

April bucht anschließend die Zahlung. Die Rechnung hat nun einem Saldo von 700,00. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion anzeigen.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Saldo | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rechnung          | 25.06.2020 | 10020   |                                      | 1,000.00                              | -700,00 | USD      |
| APP-10020  | Zahlung          | 01.07.2020  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Skonto    | 01.07.2020  |         | 3.00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Verbleibende Zahlung am 15. Juli, Skonto verwenden = Normal
April zahlt den Rest der Rechnung am 15. Juli, also nach der Rabattperiode. Auf der **Offene Buchungen ausgleichen** Seite wird kein Rabattbetrag im **Vorkalkuliertes Skonto** Feld angezeigt, und der Wert im Feld **Skontobetrag** beträgt **0,00**. Wenn April die verbleibenden 700,00 bezahlt, wird kein zusätzlicher Rabatt genommen.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | Inv-10020 | 3057    | 25.06.2020 | 25.07.2020 | 10020   | -700,00                        | USD      | -700,00          |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt. April kann sehen, dass sie bereits einen Rabatt 3,00 genommen hat.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 09.07.2020 |
| Skontobetrag         | 0,00      |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | -3,00     |
| Zu verwendender Skontobetrag | 0,00      |

April bucht anschließend die Zahlung. Wenn sie die Seite **Kreditorentransaktionen** öffnet, sieht sie, dass die Rechnung einem Saldo von 0,00 hat. Sie sieht auch, dass es zwei Zahlungen gibt. Eine Zahlung ist für 297,00 und hat einen Rabatt 3,00, während die anderen Zahlung für 700,00 ist.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Saldo | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rechnung          | 25.06.2020 | 10020   |                                      | 1,000.00                              | 0,00    | USD      |
| APP-10020  | Zahlung          | 01.07.2020  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Skonto    | 01.07.2020  |         | 3.00                                 |                                       | 0,00    | USD      |
| APP-10021  | Zahlung          | 15.07.2020 |         | 700.00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Verbleibende Zahlung am 15. Juli: Skonto verwenden = Immer
Wenn der Kreditor April ermöglicht, einen Rabatt zu nehmen, auch wenn sie nach dem Skontodatum bezahlt, kann sie den Wert im Feld **Skonto verwenden** zu **Immer** ändern. Die **Skonti für Teilzahlungen berechnen** Einstellung wird überschrieben, und der Rabatt wird übernommen. Der Zahlungsbetrag ist 693,00 und der Rabatt sind die verbleibenden 7,00.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|----------|------|------|-----------|-----------|---------|-----------------------|---------------------------------------|----------|------------------|
| Ausgewählt | Immer            | Inv-10020 | 3057    | 25.06.2020 | 25.07.2020 | 10020   | 700.00                   |                   | USD      | -693,00          |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 09.07.2020 |
| Skontobetrag         | 7.00      |
| Skonto verwenden            | Immer    |
| Verwendetes Skonto          | -3,00     |
| Zu verwendender Skontobetrag | -7,00     |

April bucht anschließend die Zahlung. Wenn sie die Seite **Kreditorentransaktionen** öffnet, sieht sie, dass die Rechnung einem Saldo von 0,00 hat. Sie sieht auch, dass es zwei Zahlungen gibt. Eine Zahlung ist für 297,00 und hat einen Rabatt von 3,00, während die andere Zahlung für 693,00 ist und einen Rabatt von 7,00 hat.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Saldo | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rechnung          | 25.06.2020 | 10020   |                                      | 1,000.00                              | 0,00    | USD      |
| APP-10020  | Zahlung          | 01.07.2020  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Skonto    | 01.07.2020  |         | 3.00                                 |                                       | 0,00    | USD      |
| APP-10021  | Zahlung          | 15.07.2020 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Skonto    | 15.07.2020 |         | 7.00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
