---
title: Ausgleichen einer teilweisen Debitorenzahlung, die mehrere Rabattzeiträume hat
description: Dieser Artikel beschreibt, wie Debitorenteilzahlungen ausgeglichen werden, die mehrere Rabattzeiträume enthalten.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62defda8831d2915050fc6822f60a905f067fe88
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778438"
---
# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Ausgleichen einer teilweisen Debitorenzahlung, die mehrere Rabattzeiträume hat

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Debitorenteilzahlungen ausgeglichen werden, die mehrere Rabattzeiträume enthalten.

Fabrikam bietet Debitor 4031 zwei Skontozeiträume. Der Debitor erhält ein 2-Prozent Skonto, wenn die Rechnung in fünf Tagen bezahlt wird, und ein 1-Prozent-Skonto, wenn die Rechnung in 14 Tagen beglichen wird. Fabrikam bietet auch Skonti auf Teilzahlungen an. Die Ausgleichsparameter sind auf der Seite **Debitorenkontenparameter** Seite verfügbar.

## <a name="invoice"></a>Rechnung
Am 25. Juni gibt Arnie eine Rechnung für 1.000,00 für den Debitor 4031 ein und bucht diese. Beim Zuweisen der Skonto für diese Rechnung geprüft, sieht Arnie, dass Debitor 4031 einen Rabatt von 20,00 erhält, wenn die Rechnung bis 30. Juni bezahlt wird. Wenn die Rechnung bis 9. Juli bezahlt wird, erhält der Debitor ein Skonto 10,00.

| Skontodatum | Skontobetrag | Betrag in Buchungswährung |
|--------------------|----------------------|--------------------------------|
| 30.06.2020          | 20.00                | 980.00                         |
| 09.07.2020           | 10.00                | 990.00                         |
| 25.07.2020          | 0,00                 | 1,000.00                       |

Auf der Seite **Debitorenbuchungen** kann Arnie diese Transaktion anzeigen.

| Beleg   | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Saldo  | Währung |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Rechnung          | 25.06.2020 | 10030   | 1,000.00                             |                                       | 1,000.00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Teilzahlung vor dem Skontodatum
Am 28. Juni leistet Debitor 4031 eine Teilzahlung von 294,00. Da der 28. Juni im ersten Skontoabzinsungszeitraum liegt, nutzt der Debitor einen Rabatt von 6,00. Auf der Seite **Bankbuchungen** ist der Wert **Skontobetrag** 20,00, und der Wert **Zu verwendender Skontobetrag** ist 6,00.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10030 | 4031    | 25.06.2020 | 25.07.2020 | 10030   | 1,000.00                       | USD      | 294,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Wenn Sie den Wert **Auszugleichender Betrag** nicht auf **294,00** ändern, weichen die erscheinenden Werte für **Skontobetrag** ab. Allerdings werden 6,00 als das Skonto übernommen, wenn die Zahlung gebucht wurde, da der Ausgleich automatisch den Wert **Auszugleichender Betrag** für Sie anpasst.

| &nbsp;                       | &nbsp;    |
|------------------------------|-----------|
| Skontodatum           | 30.06.2020 |
| Skontobetrag         | 20.00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 6,00      |

Nachdem Arnie die Zahlung gebucht hat, ist der Rechnungssaldo 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Teilzahlung vor dem zweiten Skontodatum
Am 8. Juli zahlt der Debitor den Rest des Rechnungsbetrags. Da diese Zahlung im zweiten Rabattzeitraum geleistet wird, wird ein Rabatt von 7,00 (1 Prozent) genommen.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------|-----------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10030 | 4031    | 25.06.2020 | 25.07.2020 | 10030   | 700.00       |            | USD      | 693,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

| &nbsp;                       | &nbsp;    |
|------------------------------|-----------|
| Skontodatum           | 09.07.2020 |
| Skontobetrag         | 30.00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 6,00      |
| Zu verwendender Skontobetrag | 7:00      |

Der Rechnungssaldo ist jetzt 0,00. Auf der Seite **Debitorenbuchungen** zeigt Arnie diese Transaktion an.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Saldo | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Rechnung          | 25.06.2020 | 10030   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Zahlung         | 28.06.2020 |         |                                      | 294,00                                | 0,00    | USD      |
| DISC-10030 |  Skonto   | 28.06.2020 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Zahlung         | 08.07.2020  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Skonto   | 08.07.2020  |         |                                      | 7.00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
