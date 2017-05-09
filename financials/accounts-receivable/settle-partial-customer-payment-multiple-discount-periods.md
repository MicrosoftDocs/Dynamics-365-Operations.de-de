---
title: "Ausgleichen einer teilweisen Debitorenzahlung, die mehrere Rabattzeiträume hat"
description: "Dieser Artikel beschreibt, wie Debitorenteilzahlungen ausgeglichen werden, die mehrere Rabattzeiträume enthalten."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9da48c7861f48ec2a154ac12616149d1208346cf
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Ausgleichen einer teilweisen Debitorenzahlung, die mehrere Rabattzeiträume hat

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt, wie Debitorenteilzahlungen ausgeglichen werden, die mehrere Rabattzeiträume enthalten.

Fabrikam bietet Debitor 4031 zwei Skontozeiträume. Der Debitor erhält ein 2-Prozent Skonto, wenn die Rechnung in fünf Tagen bezahlt wird, und ein 1-Prozent-Skonto, wenn die Rechnung in 14 Tagen beglichen wird. Fabrikam bietet auch Skonti auf Teilzahlungen an. Die Ausgleichsparameter sind auf der Seite **Debitorenkontenparameter** Seite verfügbar.

## <a name="invoice"></a>Rechnung
Am 25. Juni gibt Arnie eine Rechnung für 1.000,00 für den Debitor 4031 ein und bucht diese. Beim Zuweisen der Skonto für diese Rechnung geprüft, sieht Arnie, dass 4031 Debitoren einen Rabatt 20,00 erhält, wenn die Rechnung bis 30. Juni bezahlt wird. Wenn die Rechnung bis 9. Juli bezahlt wird, erhält der Debitor ein Skonto 10,00.

| Skontodatum | Skontobetrag | Betrag in Buchungswährung |
|--------------------|----------------------|--------------------------------|
| 6/30/2015          | 20,00                | 980,00                         |
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

Auf der Seite** Debitorenbuchungen** kann Arnie diese Transaktion anzeigen.

| Beleg   | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag  | Währung |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Rechnung          | 6/25/2015 | 10030   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Teilzahlung vor dem Skontodatum
Am 28. Juni leistet Debitor 4031 eine Teilzahlung von 294,00. Da der 28. Juni im ersten Skontoabzinsungszeitraum liegt, nutzt der Debitor einen Rabatt von 6,00. Auf der Seite **Bankbuchungen** ist der Wert** Skontobetrag** 20,00, und der Wert **Zu verwendender Skontobetrag** ist 6,00.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 1.000,00                       | USD      | 294,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Wenn Sie den Wert **Auszugleichender Betrag** nicht auf **294,00** ändern, weichen die erscheinenden Werte für **Skontobetrag** ab. Allerdings werden 6,00 als das Skonto übernommen, wenn die Zahlung gebucht wurde, da der Ausgleich automatisch den Wert **Auszugleichender Betrag** für Sie anpasst.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 6/30/2015 |
| Skontobetrag         | 20,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 6,00      |

Nachdem Arnie die Zahlung gebucht hat, ist der Rechnungssaldo 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Teilzahlung vor dem zweiten Skontodatum
Am 8. Juli zahlt der Debitor den Rest des Rechnungsbetrags. Da diese Zahlung im zweiten Rabattzeitraum geleistet wird, wird ein Rabatt von 7,00 (1 Prozent) genommen.

| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 09. Juli 2015 |
| Skontobetrag         | 30,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 6,00      |
| Zu verwendender Skontobetrag | 7:00      |

Der Rechnungssaldo ist jetzt 0,00. Auf der Seite **Debitorenbuchungen** zeigt Arnie diese Transaktion an.

| Beleg    | Transaktionstyp | Datum      | Rechnung | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag | Währung |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Rechnung          | 6/25/2015 | 10030   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Zahlung         | 6/28/2015 |         |                                      | 294,00                                | 0,00    | USD      |
| DISC-10030 |  Skonto   | 6/28/2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Zahlung         | 8. Juli 2015  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Skonto   | 8. Juli 2015  |         |                                      | 7:00                                  | 0,00    | USD      |






