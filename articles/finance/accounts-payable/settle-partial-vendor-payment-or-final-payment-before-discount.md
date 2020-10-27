---
title: Ausgleichen einer teilweisen Kreditorenzahlung und Ausgleichen der vollständigen Zahlung vollständig vor dem Skontodatum
description: Dieser Artikel führt Sie durch ein Szenario, in dem Teilzahlungen für eine Kreditorenrechnung vorgenommen werden, und ein Skonto abgezogen wird.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34d941c3806ccc9d2b8baa29eef45fbd4216686e
ms.sourcegitcommit: 165e082e59ab783995c16fd70943584bc3ba3455
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967309"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Ausgleichen einer teilweisen Kreditorenzahlung und Ausgleichen der vollständigen Zahlung vollständig vor dem Skontodatum

[!include [banner](../includes/banner.md)]

Dieser Artikel führt Sie durch ein Szenario, in dem Teilzahlungen für eine Kreditorenrechnung vorgenommen werden, und ein Skonto abgezogen wird.

Fabrikam kauf Waren von Kreditor 3064. Der Kreditor gibt Fabrikam ein Skonto von 1 Prozent, wenn eine Rechnung in 14 Tagen beglichen wird. Rechnungen müssen in 30 Tagen bezahlt werden. Der Kreditor ermöglicht Fabrikam auch, Skonti auf Teilzahlungen zu erhalten. Die Ausgleichsparameter sind auf der Seite **Kreditorenkontenparameter** verfügbar. Am 25. Juni gibt April eine Rechnung für 1.000,00 für den Kreditor 3064 ein.

## <a name="vendor-invoice-on-june-25"></a>Kreditorenrechnung am 25. Juni
Am 25. Juni gibt April eine Rechnung für 1.000,00 für den Kreditor 3064 ein und bucht diese. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion anzeigen.

| Beleg   | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag   | Währung |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 6/25/2015 | 10010   |                                      | 1.000,00                              | -1.000,00 | USD      |

Über die Seite **Kreditoren** öffnet April die Seite **Bankbuchungen**. Sie kann die Seite **Buchungen ausgleichen** verwenden, um die Datumsangaben und Beträge von Skonti anzuzeigen. Das Fälligkeitsdatum ist am 25. Juli, und ein Skonto von -10,00 ist verfügbar, wenn die Rechnung bis 9. Juli bezahlt wird.

| Markieren | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10010 | 3064    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen**angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | -10,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -10,00    |

April klickt auf die Registerkarte **Skonto**, um den Rabattbetrag anzuzeigen.

| Skontodatum | Skontobetrag | Betrag in Buchungswährung |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Teilzahlung am 1. Juli durch Verwendung der Seite "Buchungen ausgleichen"
April kann eine Zahlungserfassung für diese Zahlung erstellen, indem sie die Kreditorenseite **Zahlungserfassung** öffnet. Sie erstellt eine neue Erfassung und gibt eine Position für Kreditor 3064 ein. Sie öffnet anschließend die Seite **Buchungen ausgleichen**, sodass sie die Rechnung zum Ausgeleichen markieren kann. April markiert die Rechnung und ändert den Wert im Feld **Auszugleichender Betrag** zu **–500,00**. Sie sieht wieder, dass der Wert im Feld **Skontobetrag** der Betrag **–10,00** für die gesamte Rechnung ist, und der Wert im Feld **In Anspruch zu nehmender Skontobetrag** beträgt **–5,05**. Daher gleicht April -505,05 dieser Rechnung aus.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | -500,00          |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | -10,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -5,05     |

April möchte genau die Hälfte der Rechnung ausgleichen. Daher ändert sie den Wert im Feld **Auszugleichender Betrag** auf **–495,00**. Der Gesamtbetrag, der ausgeglichen wird, ist jetzt 500,00. Dieser Betrag umfasst einen Rabatt von –5,00.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | -495,00          |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | -10,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -5,00     |

April schließt die Seite **Transaktionen abgleichen**. Eine Zahlungsposition für 495,00 wird in der Erfassung erstellt, und April dann bucht die Erfassung. Auf der Seite **Kreditorenbuchungen** kann April diese Transaktion prüfen. In diesem Formular sieht sie, dass die Rechnung ein Saldo von -500,00 hat. Sie sieht auch eine Zahlung von 495,00 und ein Skonto von 5,00.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Rechnung          | 6/25/2015 | 10010   |                                      | 1.000,00                              | -500,00 | USD      |
| APP-10010  | Zahlung          | 1. Juli 2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Skonto    | 1. Juli 2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Verbleibender Betrag am 8. Juli bezahlt
April zahlt den Rest der Rechnung für Kreditor 3064 am 8. Juli, der im Skontozeitraum ist. April erstellt die Zahlungserfassung am 8. Juli und markiert die Buchung für den Ausgleich. Sie sieht, dass der auszugleichende Betrag 495,00 ist. Der Wert im Feld **Vorkalkuliertes Skonto** ist **–5,00**, da der Rabatt von 5,00 zuvor in Anspruch genommen wurde.

|                         |        |
|-------------------------|--------|
| Insgesamt markiert            | 495,00 |
| Vorkalkuliertes Skonto | -5,00  |

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

April bucht diese Zahlungserfassung und prüft die Kreditorentransaktionen auf der Seite **Kreditorentransaktionen**. Der Saldo der Rechnung ist jetzt 0,00, und April sieht die zwei Zahlungen und die zwei Skonti.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Rechnung          | 6/25/2015 | 10010   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10010  |  Zahlung         | 1. Juli 2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Skonto    | 1. Juli 2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Zahlung          | 8. Juli 2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Skonto    | 8. Juli 2015  |         | 5,00                                 |                                       | 0,00    | USD      |





