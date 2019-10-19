---
title: Ausgleichen einer teilweisen Debitorenzahlung und Ausgleichen der vollständigen Zahlung vollständig vor dem Skontodatum
description: Dieser Artikel beschreibt Szenarien, die zeigen, wie Teilzahlungen für einen Debitor erfasst und Skonti innerhalb der Skontoperiode übernommen werden.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37c378a424d89a884d1f3f0f14e1d544b3af178b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177977"
---
# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Ausgleichen einer teilweisen Debitorenzahlung und Ausgleichen der vollständigen Zahlung vollständig vor dem Skontodatum

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt Szenarien, die zeigen, wie Teilzahlungen für einen Debitor erfasst und Skonti innerhalb der Skontoperiode übernommen werden.

Fabrikam verkauft Waren an Kunde 4028. Fabrikam bietet ein Skonto von 1 % an, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird. Rechnungen müssen in 30 Tagen bezahlt werden. Fabrikam bietet auch Skonti auf Teilzahlungen an. Die Ausgleichsparameter sind auf der Seite **Debitorenkontenparameter** Seite verfügbar.

## <a name="customer-invoice"></a>Debitorenrechnung
Am 25. Juni gibt Arnie eine Rechnung für 1.000,00 für den Debitor 4028 ein und bucht diese. Auf der Seite**Debitorenbuchungen** kann Arnie diese Transaktion anzeigen.

| Beleg   | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag  | Währung |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Rechnung          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 1.000,00 | USD      |

Von der Seite **Debitor** oder **Debitorentransaktionen** kann Arnie die Seite **Transaktionen ausgleichen** öffnen, um die Datumsangaben und die Beträge von Skonti anzuzeigen, die für die Rechnung verfügbar sind. Das Fälligkeitsdatum ist am 25. Juli, und ein Skonto von 10,00 ist verfügbar, wenn die Rechnung bis 9. Juli gezahlt wird.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Rabattinformationen werden am unteren Rand der Seite **Transaktionen abgleichen** für die markierte Rechnung angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 10,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 10,00     |

Arnie klicket auf die Registerkarte **Skonto**, um den Rabattbetrag anzuzeigen.

| Skontodatum | Skontobetrag | Betrag in Buchungswährung |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Teilzahlung mithilfe der Seite "Debitorenzahlungen eingeben"
Debitor 4028 übermittelt eine Zahlung in Höhe von 500,00. am 1. Juli Um dieser Zahlung einzugeben, klickt Arnie nicht **Positionen**. Stattdessen erfasst er die Zahlung, indem er eine neue Zahlungserfassung erstellt und dann die Seite **Debitorenzahlungen eingeben** öffnet. Er gibt die Zahlungsinformationen ein und markiert die Rechnung, die er eingegeben hat. Wenn Arnie **500,00** als Betrag eingibt, gibt er auch **500,00** im Feld **Zu zahlender Betrag** im Raster ein. Da Fabrikam ein Skonto für Teilzahlungen zulässt, sieht er, dass auch ein Teilskonto von 5,05 gewährt wird. Die Berechnung für diesen Rabatt ist 500,00 ÷ 0,99 × 0,01 = 5,05. (In dieser Berechnung werden 500,00 durch 0,99 dividiert, da es einen Rabatt von einem Prozent gibt. Daher zahlt der Debitor 99 Prozent der Rechnung. Das Ergebnis wird dann mit dem Rabattprozentsatz 1 Prozent oder 0,01 multipliziert. Wenn der Debitor den vollen Rabatt von 10,00 nimmt, ist der Betrag, der ausgeglichen werden muss, 990,00.) Rabattinformationen werden im Raster im unteren Bereich der **Debitorenzahlungen eingeben** Seite.

| Zu verwendender Skontobetrag | Verwendetes Skonto | Zu zahlender Betrag |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Teilzahlung mithilfe der Erfassungspositionen
Anstatt die Seite **Debitorenzahlungen eingeben** in der Zahlungserfassung zu öffnen, kann Arnie auf **Positionen** klicken, um eine Zahlung einzugeben. Die Zahlungserfassung wird angezeigt, wo Arnie einer Position für Debitor 4028 eingeben kann. Arnie öffnet anschließend die Seite **Buchungen ausgleichen**, sodass er die Rechnung zum Ausgeleichen markieren kann. Arnie markiert die Rechnung und ändert den Wert im Feld **Auszugleichender Betrag** zu **500,00**. Er sieht wieder, dass der Wert im Feld **Skontobetrag** der Betrag **10,00** für die gesamte Rechnung ist, und der Wert im Feld **In Anspruch zu nehmender Skontobetrag** beträgt **5,05**. Daher gleicht Arnie 505,05 dieser Rechnung aus.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 500,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 10,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 5,05      |

Wenn der Debitor genau die Hälfte der Rechnung ausgleichen möchte, übermittelt der Debitor eine Zahlung von 495,00. In diesem Fall gibt Arnie **495,00** im Feld **Auszugleichender Betrag** ein. Das Skonto für 5,00 wird auch in Anspruch genommen, sodass die Summe des ausgeglichenen Betrags 500,00 ist.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 10,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 5,00      |

Arnie schließt die Seite **Transaktionen abgleichen**. Eine Zahlungsposition für 495,00 wird in der Erfassung erstellt, und Arnie dann bucht die Erfassung. Er kann die Debitorentransaktionen auf der Seite **Debitorentransaktionen** überprüfen. Auf dieser Seite sieht Arnie, dass die Rechnung ein Saldo von 500,00 hat. Er sieht auch eine Zahlung von 495,00 und einen Rabatt von 5,00.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Rechnung          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Zahlung         | 1. Juli 2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Skonto   | 1. Juli 2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Zahlung für den verbleibenden Betrag
Debitor 4028 zahlt den verbleibenden Betrag von 495,00 am 8. Juli, also innerhalb des Skontozeitraums. Arnie erstellt die Zahlungserfassung am 8. Juli und markiert die Buchung für den Ausgleich. Er sieht, dass der auszugleichende Betrag 495,00 ist. Der Wert im Feld **Vorkalkuliertes Skonto** ist **5,00**, da der Rabatt 5,00 zuvor in Anspruch genommen wurde.

|                         |        |
|-------------------------|--------|
| Insgesamt markiert            | 495,00 |
| Vorkalkuliertes Skonto | 5,00   |

Informationen zur markierte Buchung werden im Raster auf der **Offene Buchungen ausgleichen** Seite angezeigt.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 10,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 5,00      |
| Zu verwendender Skontobetrag | 5,00      |

Arnie bucht diese Erfassung und prüft die Debitorentransaktionen auf der Seite **Debitorentransaktionen**. Der Saldo der Rechnung ist jetzt 0,00, und Arnie sieht die zwei Zahlungen und die zwei Skonti.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Rechnung          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Zahlung          | 1. Juli 2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Skonto    | 1. Juli 2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Zahlung          | 8. Juli 2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Skonto    | 8. Juli 2015  |         |                                      | 5,00                                  | 0,00    | USD      |





