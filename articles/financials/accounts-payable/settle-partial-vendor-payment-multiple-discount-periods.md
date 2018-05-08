---
title: "Ausgleichen einer teilweisen Kreditorenzahlung, die mehrere Rabattzeiträume hat"
description: "Dieser Artikel führt Sie durch ein Szenario, in dem mehrere Teilzahlungen an einen Kreditoren vorgenommen werden, der mehrere Skonti anbietet."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d88630a62cfdebf0daf19d3bb6af7fcc6e877876
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Ausgleichen einer teilweisen Kreditorenzahlung, die mehrere Rabattzeiträume hat

[!include [banner](../includes/banner.md)]

Dieser Artikel führt Sie durch ein Szenario, in dem mehrere Teilzahlungen an einen Kreditoren vorgenommen werden, der mehrere Skonti anbietet. 

Kreditor 3054 bietet Fabrikam ein Skonto von 2 Prozent, wenn eine Rechnung in fünf Tagen bezahlt wird, und ein Skonto von 1 Prozent, wenn die Rechnung in 14 Tagen beglichen wird.

## <a name="invoice"></a>Rechnung
Am 28. Juni erstellt April eine Rechnung über 1.000,00 für den Kreditor 3054. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion anzeigen.

| Beleg   | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag   | Währung |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 6/28/2015 | 10060   |                                      | 1.000,00                              | -1.000,00 | USD      |

Die folgenden Skontodatumsangaben und Beträge sind für diese Rechnung verfügbar.

| Skontodatum | Skontobetrag | Betrag in Buchungswährung |
|--------------------|----------------------|--------------------------------|
| 7/3/2015           | 20,00                | 980,00                         |
| 7/12/2015          | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

## <a name="payment-on-july-2"></a>Zahlung am 2. Juli
Am 2. Juli möchte April 300,00 Euro dieser Rechnung ausgleichen. Sie erfasst eine einmalige Zahlung, indem er die **Zahlungserfassung** in "Kreditoren" verwendet. Sie fügt eine Position für Kreditor 3054 hinzu und gibt einen Zahlungsbetrag von **300.00** ein. April öffnet anschließend die Seite **Buchungen ausgleichen**, sodass Sie die Rechnung markieren kann, die ausgeglichen wird. Sie aktualisiert den Wert im Feld **Auszugleichender Betrag** auf **300,00** und bemerkt, dass der Wert im Feld **Zu verwendender Skontobetrag** auf **6,12** geändert ist. Da diese Zahlung im ersten Rabattzeitraum geleistet wird, wird ein Rabatt von 2 Prozent genommen.

| Markieren | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 6/28/2015 | 7/28/2015 | 10060   | 1.000,00                       | USD      | 300,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 02.07.2015 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -6,12     |

Da ein Skonto verfügbar ist, möchte April den Zahlungsbetrag ändern, sodass der gesamte ausgeglichene Betrag 300,00 ist, sowohl für die Zahlung als auch das Skonto. Sie ändert den Wert im Feld **Auszugleichender Betrag** auf **294,00** und bemerkt, dass der Wert im Feld **Zu verwendender Skontobetrag** auf **6,00** geändert ist.

| Markieren | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 6/28/2015 | 7/28/2015 | 10060   | 1.000,00                       | USD      | 294,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 02.07.2015 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -6,00     |

April bucht die Zahlung. Auf der Seite **Kreditorenbuchungen** kann Sie die Transaktionen anzeigen. Sie sieht, dass 300,00 auf die Rechnung angewendet wurde. Dieser Betrag umfasst einen Rabatt von 6,00. Daher entspricht der verbleibenden Saldo 700,00.

| Beleg    | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2015 | 10060   |                                      | 1.000,00                              | -700,00 | USD      |
| APP-10060  | 7/2/2015  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2015  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Zahlung am 8. Juli
Am 8. Juli leistet April eine Nachzahlung für die Rechnung. Um den Betrag einzugeben, öffnet sie die Seite **Buchungen ausgleichen**, und anschließend klickt sie auf die Registerkarte **Skonto** . Sie sieht die Datumsangaben und Beträge für die beiden Skonti, die verfügbar sind. Da diese Zahlung in der zweiten Rabattperiode geleistet wird, ist ein Rabatt von 1 Prozent oder 5,00 verfügbar. Dieser Betrag wird als Hälfte des 1-Prozent-Rabatts auf 1.000,00 oder die Hälfte von 10,00 berechnet.

| Skontodatum | Skontobetrag | Betrag in Buchungswährung |
|--------------------|----------------------|--------------------------------|
| 7/3/2015           | 20,00                | 680,00                         |
| 7/12/2015          | 10,00                | 690,00                         |
| 7/25/2015          | 0,00                 | 700,00                         |

April beschließt, 495,00 zu zahlen und das Skonto von 5,00 in Anspruch zu nehmen. Daher ist der Gesamtbetrag, der ausgeglichen wird, 500,00.

| Markieren | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 6/28/2015 | 7/28/2015 | 10060   | 1.000,00                       | USD      | 495,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 7/12/2015 |
| Skontobetrag         | -10,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | -6,00     |
| Zu verwendender Skontobetrag | -5,00     |

Auf der Seite **Kreditorenbuchungen** sieht April, dass der neue Saldo 200,00 beträgt.

| Beleg    | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2015 | 10060   |                                      | 1.000,00                              | -200.00 | USD      |
| APP-10060  | 7/2/2015  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 7/12/2015 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 7/12/2015 |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Zahlung am 20. Juli
Am 20. Juli erstellt April eine endgültige Zahlung von 200,00. Kein Rabatt wird in Anspruch genommen, da die Zahlung nach beiden Rabattperioden geleistet wird. Der Saldo der Rechnung ist 0,00.

| Beleg    | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2015 | 10060   |                                      | 1.000,00                              | -200.00 | USD      |
| APP-10060  | 7/2/2015  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 7/12/2015 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 7/12/2015 |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10062  | 20.07.2015 |         | 200,00                               |                                       | 0,00    | USD      |






