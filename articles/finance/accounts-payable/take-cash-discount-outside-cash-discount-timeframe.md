---
title: Ein Skonto außerhalb der Skontoperiode in Anspruch nehmen
description: Dieser Artikel beschreibt zwei Szenarien, die zeigen, wie ein Skonto übernommen werden kann, wenn die Zahlung außerhalb der Skontoperiode erfolgt.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b1eb5e542acf7496d1a0cf7196716a5de75e4e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780532"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Ein Skonto außerhalb der Skontoperiode in Anspruch nehmen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt zwei Szenarien, die zeigen, wie ein Skonto übernommen werden kann, wenn die Zahlung außerhalb der Skontoperiode erfolgt.

Am 28. Juni erstellt April eine Rechnung über 2.000,00 für den Kreditor 3052. Von dem Rechnungsbetrag wird ein Skonto von 1 % abgezogen, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird.

## <a name="use-cash-discount-option--always"></a>Option "Skonto verwenden" = "Immer"
April erstellt eine Zahlung am 1. Juli, was nach dem Skontodatum ist. April öffnet die Seite **Transaktionen ausgleichen**, um die Transaktionen anzuzeigen, die ausgeglichen werden können. 

April markiert die Rechnung zur Zahlung. Kein Skonto wird genommen, da die Zahlung nach dem Skontodatum ist. Der Lieferant hat April jedoch erlaubt, den Abzug in jedem Fall in Anspruch zu nehmen. Daher ändert April den Wert im Feld **Skonto verwenden** in **Immer**.

| Markieren     | Skonto verwenden | Beleg   | Konto | Skontodatum | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Immer            | Inv-10030 | 3052    | 28.06.2020          | 12.07.2020 | 10030   | -2,000,00                      | USD      | -1.980,00        |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 12.07.2020 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Immer    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Für die Berechnung von Rabatten zu verwendendes Datum = Ausgewähltes Datum
Wenn sowohl die Rechnung als auch die Zahlung gebucht wurden, kann das Skonto immer noch in Anspruch genommen werden, wenn die Transaktionen auf der Seite **Transaktionen ausgleichen** ausgeglichen werden. April ändert den Wert im Feld **Für die Berechnung von Rabatten zu verwendendes Datum** auf **Ausgewähltes Datum**. Sie gibt das Datum 28. Juni ein, das in der Skontoperiode für die Rechnung liegt. Dieses Datum wird verwendet, um ein Skonto für die Buchung zu berechnen. Auf der Seite **Offene Transaktionen ausgleichen** sieht April, dass standardmäßig der vollständige Rabatt von 20,00 angezeigt wird. Die Rechnungsposition zeigt, dass der auszugleichende Betrag 1.980,00 ist.

| Markieren          | Skonto verwenden | Beleg   | Konto | Skontodatum | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt und hervorgehoben | Normal    | Inv-10030 | 3052    | 28.06.2020         | 12.07.2020 | 10030   | -2,000,00                      | USD      | -1.980,00        |
| Ausgewählt                 | Normal    | APP-10030 | 3052    | 15.07.2020          | 15.07.2020 |         | 500.00                         | USD      | 500.00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Der angewendete Rabattbetrag ist 20,00, da der auszugleichende Betrag für die Rechnung der Standardbetrag ist, 1.980,00.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 12.07.2020 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -20,00    |

April aktualisiert den Wert im Feld **Auszugleichender Betrag** auf **500,00**. Der Wert im Feld **Anzuwendender Skontobetrag** wird als **5,05** berechnet.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt und hervorgehoben | Normal            | Inv-10030 | 3052    | 28.06.2020 | 12.07.2020 | 10030   | 2,000.00                       | USD      | -500,00          |
| Ausgewählt                 | Normal            | APP-10030 | 3052    | 15.07.2020 | 15.07.2020 |         | 500.00                         | USD      | 500.00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Der Wert im Feld **Anzuwendender Skontobetrag** ist **5,05**, da der auszugleichende Betrag für die Rechnung zu dem Zahlungsbetrag 500,00 geändert wurde.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 12.07.2020 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
