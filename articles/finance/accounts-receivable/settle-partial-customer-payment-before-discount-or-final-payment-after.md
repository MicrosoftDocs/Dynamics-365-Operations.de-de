---
title: Teilzahlungen vor dem Rabattdatum ausgleichen mit vollständiger Zahlung nach dem Rabattdatum
description: Dieser Artikel erläutert die Auswirkung von Zahlungsvereinbarungen auf Rechnungen für Debitoren. Das Szenario konzentriert sich auf die Auswirkungen im untergeordneten Sachkonto, nicht im Hauptbuch.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10ba8d59855b60b3d05b4c6b44c98905e10487ecdcf7bc459acca73c12bc72d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740169"
---
# <a name="settle-partial-payment-before-discount-date-with-final-payment-after-discount-date"></a>Teilzahlungen vor dem Rabattdatum ausgleichen mit vollständiger Zahlung nach dem Rabattdatum

[!include [banner](../includes/banner.md)]

Dieser Artikel erläutert die Auswirkung von Zahlungsvereinbarungen auf Rechnungen für Debitoren. Das Szenario konzentriert sich auf die Auswirkungen im untergeordneten Sachkonto, nicht im Hauptbuch.

Fabrikam verkauft Waren an Kunde 4027. Fabrikam bietet ein Skonto von 1 % an, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird. Rechnungen müssen in 30 Tagen bezahlt werden. Fabrikam bietet auch Skonti auf Teilzahlungen an. Die Ausgleichsparameter sind auf der Seite **Debitorenkontenparameter** Seite verfügbar.

## <a name="invoice"></a>Rechnung
Am 25. Juni gibt Arnie eine Rechnung für 1.000,00 für den Debitor 4027 ein und bucht diese. Arnie kann diese Rechnung anzeigen, indem er die **Buchungen** Schaltfläche in der **Debitoren** Seite verwendet.

| Beleg   | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag  | Währung |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Rechnung          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Teilzahlung vor dem Skontodatum
Am 2. Juli leistet Debitor 4027 eine Teilzahlung von 297,00 für die Rechnung. Die Zahlung ist für ein Skonto freigegeben, da Fabrikam Skonti auf Teilzahlungen anbietet, und die Teilzahlungs vor dem Skontodatum geleistet wurde. Daher zahlt nimmt Debitor 4027 ein Skonto von 3,00 in Anspruch. Arnie erfasst die Zahlung für Debitor 4027, indem er die Zahlungserfassung verwendet. Arnie öffnet anschließend die Seite **Buchungen ausgleichen**, sodass Arnie die Rechnung zum Ausgleichen markieren kann.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 1.000,00                             | USD      | 297,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Wenn Sie den Wert **Auszugleichender Betrag** nicht auf **297,00** ändern, weichen die erscheinenden Werte für Skontobetrag ab. Allerdings werden 3,00 als das Skonto übernommen, wenn die Zahlung gebucht wurde, da der Ausgleich automatisch den Wert **Auszugleichender** Betrag für Sie anpasst.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 10.00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 3,00      |

Arnie bucht diese Zahlung. Die Rechnung hat nun einem Saldo von 700,00. Folgende Buchungen können für den Debitor angezeigt werden.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Rechnung          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Zahlung         | 1. Juli 2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |  Skonto   | 1. Juli 2015  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Verbleibende Teilzahlung nach dem Skontodatum
Am 11. Juli, also nach der Rabattperiode, zahlt Debitor 4027 den Rest dieser Rechnung. Auf der **Offene Buchungen ausgleichen** Seite wird kein Rabattbetrag im Feld **Vorkalkuliertes Skonto** angezeigt, und der Wert im Feld **Skontobetrag** beträgt **0,00**. Wenn Debitor 4027 die verbleibenden 700,00 bezahlt, wird kein zusätzlicher Rabatt genommen.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 700,00                               | USD      | 700,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 0,00      |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 3,00      |
| Zu verwendender Skontobetrag | 0,00      |

Wenn Arnie den Wert im **Skonto verwenden**-Feld auf **Immer** ändert, wird die **Skonti für Teilzahlungen berechnen**-Einstellung überschrieben, und das Skonto wird übernommen. Der Zahlungsbetrag ändert sich auf 693,00 und der Rabatt 7,00 verbleibt.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Ausgewählt | Immer            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 700,00                               |                                       | USD      | 693,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

| Feld                        | Wert     |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 7.00      |
| Skonto verwenden            | Immer    |
| Verwendetes Skonto          | 3,00      |
| Zu verwendender Skontobetrag | 7:00      |

Arnie ändert der Wert im Feld **Skonto verwenden** wieder zu **Normal**, da Arnie diesem Debitor nicht den verbleibenden Barzahlungsrabatt von 7,00 gewährt. Arnie bucht anschließend die Zahlung. Wenn Arnie die Seite **Debitorentransaktionen** öffnet, hat die Rechnung einen Saldo von 0,00. Es gibt zwei Zahlungen. Eine Zahlung ist für 297,00 und hat ein Skonto von 3,00, während die anderen Zahlung für 700,00 ist.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Rechnung          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 1. Juli 2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |                  | 1. Juli 2015  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 11.7.2015 |         |                                      | 700,00                                | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]