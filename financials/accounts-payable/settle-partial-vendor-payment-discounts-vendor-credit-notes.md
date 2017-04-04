---
title: Ausgleichen einer teilweise Kreditorenzahlung, Rabatte auf Kreditorengutschriften hat
description: "Dieser Artikel führt Sie durch ein Szenario, in dem eine Gutschrift mit einer Rechnung ausgeglichen wird."
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
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 849cffa64eaf777f9f4c9243dab41b00fa59ad79
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Ausgleichen einer teilweise Kreditorenzahlung, Rabatte auf Kreditorengutschriften hat

Dieser Artikel führt Sie durch ein Szenario, in dem eine Gutschrift mit einer Rechnung ausgeglichen wird.

Fabrikam gibt Kreditoren Skonti auf Gutschriften. Kreditor 3050 gewährt Fabrikam ein Skonto von 1 Prozent, wenn eine Rechnung in 14 Tagen beglichen wird.

## <a name="invoice-and-credit-memo"></a>Rechnung und Gutschrift
Am 29. Juni erstellt April eine Rechnung in Höhe von 1.000,00 für den Kreditor " 3050. Am 2. Juli erstellt Sie eine Gutschrift für 200,00. Über die Seite **Kreditoren** öffnet April die Seite **Bankbuchungen**. Sie kann die Seite **Buchungen ausgleichen** verwenden, um die Gutschrift und die Rechnung für den Ausgleich zu markieren. Ein Rabatt von 2,00 wird auf der Gutschrift berechnet. Daher wird der Gesamtwert der Gutschrift auf 198,00 verringert.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt                 | Normal            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1.000,00                      | USD      | -990.00          |
| Ausgewählt und hervorgehoben | Normal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USD      | 198,00           |

Rabattinformationen für die Gutschrift werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 13.07.2015 |
| Skontobetrag         | 2,00      |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 2,00      |

April klickt auf **Buchen**. Sie prüft dann den abgeschlossenen Ausgleich. April sieht, dass 198,00 Euro der Gutschrift angewendet wurden, und ein Rechnungsrabatt von 2,00 Euro übernommen wurde. Daher ist die Summe 200,00.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung  | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Ausgewählt und hervorgehoben | Normal            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | -1.000,00                      | USD      | -200.00          |
| Ausgewählt                 | Normal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200,00                         | USD      | 198,00           |

April kann die Kreditorenbuchungen auf der Seite **Kreditorenbuchungen** überprüfen, indem sie einen Kreditor auf der Seite **Alle Kreditoren **auswählt und dann im Aktivitätsbereich auf **Buchungen** klickt. Auf dieser Seite sieht April, dass die Rechnung ein Saldo von –800,00 hat. Sie sieht auch eine Gutschrift für 198,00 und einen Rabatt von 2,00.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Rechnung          | 6/29/2015 | 10070   |                                      | 1.000,00                              | –800,00 | USD      |
| Inv-10071  |                  | 7/2/2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| DISC-10071 |  Skonto   | 7/2/2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| DISC-10071 |  Skonto   | 7/2/2015  |         |                                      | 2,00                                  | 0,00    | USD      |




