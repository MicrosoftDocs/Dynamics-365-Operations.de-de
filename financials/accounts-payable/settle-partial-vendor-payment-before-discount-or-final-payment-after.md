---
title: "Ausgleichen einer teilweise Kreditorenzahlung vor dem Skontodatum mit einer vollständigen Zahlung nach dem Skontodatum"
description: "Dieser Artikel führt Sie durch ein Szenario, in dem mehrere Teilzahlungen erfolgen, einige innerhalb des Skontoperiode und andere außerhalb der Skontoperiode."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 33851ff7c9ee2c50544589ade0191798a13706e7
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Ausgleichen einer teilweise Kreditorenzahlung vor dem Skontodatum mit einer vollständigen Zahlung nach dem Skontodatum

Dieser Artikel führt Sie durch ein Szenario, in dem mehrere Teilzahlungen erfolgen, einige innerhalb des Skontoperiode und andere außerhalb der Skontoperiode.

Fabrikam-Einkaufwaren Kreditor von 3057. Bei Fabrikam geht ein Skonto von 1 %, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird. Rechnungen müssen in 30 Tagen bezahlt werden. Der Kreditor ermöglicht Fabrikam auch, Skonti auf Teilzahlungen zu erhalten. Die Ausgleichsparameter sind auf der Kreditorenparameter ** ** Seite.

## <a name="invoice-on-june-25"></a>Rechnung am 25. Juni
Am 25. Juni gibt April ein und Buchen einer Rechnung in Höhe von 1.000,00 für den Kreditor " 3057. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion anzeigen.

| Beleg   | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag   | Währung |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Rechnung          | 6/25/2015 | 10020   |                                      | 1.000,00                              | -1.000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Teilzahlung am 2. Juli
Am 2. Juli möchte April 300,00 Euro dieser Rechnung ausgleichen. Die Zahlung ist für einen Skonto berechtigt, da Fabrikam Rechnungsrabatte im Teilzahlungen nimmt. Daher zahlt April 297,00 und nimmt einen Rabatt von 3,00. Sie stellt eine Zahlungserfassung und gibt eine Position für Kreditor " 3057 ein. Sie öffnet anschließend die Bankbuchungen ** ** Seite, damit die Rechnung für den Ausgleich markieren können.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | Inv-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | -1.000,00                      | USD      | -297,00          |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | -10,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -3,00     |

April bucht anschließend die Zahlung. Die Rechnung hat nun einem Saldo von 700,00. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion anzeigen.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rechnung          | 6/25/2015 | 10020   |                                      | 1.000,00                              | -700,00 | USD      |
| APP-10020  | Zahlung          | 1. Juli 2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Skonto    | 1. Juli 2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Verbleibende Zahlung am 15. Juli, Skonto verwenden = Normal
April zahlt den Rest der Rechnung am 15. Juli, also nach der Rabattperiode. Auf der **Offene Buchungen ausgleichen** Seite wird kein Rabattbetrag im **Vorkalkuliertes Skonto **Feld angezeigt, und der Wert im Feld **Skontobetrag** beträgt **0,00**. Wenn April die verbleibenden 700,00 bezahlt, wird kein zusätzlicher Rabatt genommen.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | Inv-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | -700,00                        | USD      | -700,00          |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt. April kann sehen, dass sie bereits einen Rabatt 3,00 genommen hat.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 0,00      |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | -3,00     |
| Zu verwendender Skontobetrag | 0,00      |

April bucht anschließend die Zahlung. Wenn sie die Seite **Kreditorentransaktionen** öffnet, sieht sie, dass die Rechnung einem Saldo von 0,00 hat. Sie sieht auch, dass es zwei Zahlungen gibt. Eine Zahlung ist für 297,00 und hat einen Rabatt 3,00, während die anderen Zahlung für 700,00 ist.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rechnung          | 6/25/2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Zahlung          | 1. Juli 2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Skonto    | 1. Juli 2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Zahlung          | 7/15/2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Verbleibende Zahlung am 15. Juli: Skonto verwenden = Immer
Wenn der Kreditor einen Rabatt April nehmen können, obwohl sie nach dem Skontodatum bezahlt, kann sie den Wert im Feld ändern Verwendungsskonto ** ** ** immer **. ** Die berechnen Sie Skonti für Teilzahlungen ** Einrichtung wird überschrieben, und der Rabatt wird übernommen. Der Zahlungsbetrag ist 693,00 und der Rabatt sind die verbleibenden 7,00.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Ausgewählt | Immer            | Inv-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | 700,00                               |                                       | USD      | -693,00          |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 7:00      |
| Skonto verwenden            | Immer    |
| Verwendetes Skonto          | -3,00     |
| Zu verwendender Skontobetrag | -7,00     |

April bucht anschließend die Zahlung. Wenn sie die Seite **Kreditorentransaktionen** öffnet, sieht sie, dass die Rechnung einem Saldo von 0,00 hat. Sie sieht auch, dass es zwei Zahlungen gibt. Eine Zahlung ist für 297,00 und hat einen Rabatt von 3,00, während die andere Zahlung für 693,00 ist und einen Rabatt von 7,00 hat.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rechnung          | 6/25/2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Zahlung          | 1. Juli 2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Skonto    | 1. Juli 2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Zahlung          | 7/15/2015 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Skonto    | 7/15/2015 |         | 7:00                                 |                                       | 0,00    | USD      |




