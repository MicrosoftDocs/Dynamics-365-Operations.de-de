---
title: "Skontobehandlung für Überzahlungen"
description: "Dieser Artikel enthält Szenarien, die zeigen, wie eine Zahlung behandelt wird, wenn der Debitor ein Skonto abzieht aber auch zu viel bezahlt."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5604f806eed81c60dfcae7cb7b1a22bba25aa454
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="handling-cash-discounts-for-overpayments"></a>Skontobehandlung für Überzahlungen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Szenarien, die zeigen, wie eine Zahlung behandelt wird, wenn der Debitor ein Skonto abzieht aber auch zu viel bezahlt. 

Eine Rechnung gilt als zu viel bezahlt, wenn der Zahlungsbetrag höher als der Rechnungsbetrag minus des Skontos ist. Um anzugeben, wie eine verfügbare Skontodifferenz behandelt wird, wenn eine Rechnung zu viel bezahlt wird, verwenden Sie die Felder **Skontoverwaltung** und **Maximale Über- bzw. Unterzahlung** auf der **Debitorenparameter** Seite. Im folgenden Beispiel hat der Debitor bei der Rechnung 0,50 zu viel bezahlt.

| Rechnungssumme | Skonto verfügbar | Zu zahlender Betrag, der das Skonto enthält | Betrag, den der Debitor tatsächlich zahlt |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Skontoverwaltungsoption = Spezifisch
Wenn **Spezifisch** im Feld **Skontoverwaltung** der Seite **Konten für automatische Buchungen** ausgewählt ist, wird das vollständige Skonto übernommen. Der Überzahlungsbetrag wird entweder zu einem Sachkonto für den Skontounterschied gebucht oder bleibt als Kontensaldo auf dem Debitorenkonto. Das genaue Verhalten hängt davon ab, ob der Überzahlungsbetrag zwischen 0,00 und dem Betrag liegt, der im Feld**Maximale Über- bzw. Unterzahlung** eingegeben wurde, oder ob der Überzahlungsbetrag größer als der Betrag in **Maximale Über- bzw. Unterzahlung** ist.

### <a name="scenario-1"></a>Szenario 1

In diesem Szenario liegt der Überzahlungsbetrag zwischen 0,00 und dem Maximum für die Überzahlung oder Unterzahlung. Es wird eine Rechnung über 105,00 mit einem Skonto erfasst, das verfügbar ist, wenn die Rechnung innerhalb von sieben Tagen beglichen wird.

| Rechnungssumme | Skonto verfügbar | Zu zahlender Betrag, der das Skonto enthält |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Der Debitor übermittelt eine Zahlung für 95,00 innerhalb des Skontoabzinsungszeitraums. Die Zahlung wird mit der offenen Rechnung über 105,00 ausgeglichen. Nachdem die Rechnung und die Zahlung ausgeglichen sind, werden für den Debitor die folgenden Transaktionen in Debitor erstellt.

| Transaktion   | Betrag | Gesamtbetrag |
|---------------|--------|---------|
| Rechnung       | 105,00 | 0,00    |
| Zahlung       | -95,00 | 0,00    |
| Skonto | -10,50 | 0,00    |

Die folgenden Buchhaltungseinträge werden zur Zahlung und dem Ausgleich generiert. **Zahlung**

| Konto             | Sollbetrag | Habenbetrag |
|---------------------|--------------|---------------|
| Bargeld                | 95,00        |               |
| Debitoren |              | 95,00         |

**Ausgleich**

| Konto                                                                                                          | Sollbetrag | Habenbetrag |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Skonto (das Feld **Hauptkonto für Debitorenrabatte** auf der **Skonti** Seite)                 | 10,50        |               |
| Debitoren                                                                                              |              | 10,50         |
| Debitorenskonto (das Feld **Debitorenskonto** auf der **Konten für automatische Buchungen** Seite) |              | 0,50          |
| Debitoren                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Szenario 2

In diesem Szenario übersteigt der Überzahlungsbetrag das Maximum für den Überzahlungs- oder Unterzahlungsbetrag. Es wird eine Rechnung über 105,00 mit einem Skonto erfasst, das verfügbar ist, wenn die Rechnung innerhalb von sieben Tagen beglichen wird.

| Rechnungssumme | Skonto verfügbar | Zu zahlender Betrag, der das Skonto enthält |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Der Debitor übermittelt eine Zahlung für 95,00 innerhalb des Skontoabzinsungszeitraums. Die Zahlung wird mit der offenen Rechnung über 105,00 ausgeglichen. Nachdem die Rechnung und die Zahlung ausgeglichen sind, werden für den Debitor die folgenden Transaktionen in Debitor erstellt.

| Transaktion   | Betrag | Gesamtbetrag |
|---------------|--------|---------|
| Rechnung       | 105,00 | 0,00    |
| Zahlung       | -95,00 | -0,50   |
| Skonto | -10,50 | 0,00    |

Der Überzahlungsbetrag von 0,50 verbleibt als offener Saldo auf der Zahlung und kann mit einer anderen Rechnung ausgeglichen werden. Die folgenden Buchhaltungseinträge werden zur Zahlung und dem Ausgleich generiert. **Zahlung**

| Konto             | Sollbetrag | Habenbetrag |
|---------------------|--------------|---------------|
| Bargeld                | 95,00        |               |
| Debitoren |              | 95,00         |

**Ausgleich**

| Konto                                                                                          | Sollbetrag | Habenbetrag |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Skonto (das Feld **Hauptkonto für Debitorenrabatte** auf der Seite**Skonti**) | 10,50        |               |
| Debitoren                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Skontoverwaltungsoption = Unspezifisch
Wenn **Unspezifisch** im Feld **Skontoverwaltung** der Seite **Konten für automatische Buchungen** ausgewählt ist, wird der Skontobetrag um den zu viel gezahlten Betrag gesenkt. Dieses Verhalten wird immer verwendet, unabhängig davon, ob der Überzahlungsbetrag möglicherweise größer oder kleiner ist als der Betrag, der im Feld **Maximale Über- bzw. Unterzahlung** eingegeben wird.

### <a name="scenario-3"></a>Szenario 3

In diesem Szenario wird eine Rechnung über 105,00 mit einem Skonto erfasst, das verfügbar ist, wenn die Rechnung innerhalb von sieben Tagen beglichen wird.

| Rechnungssumme | Skonto verfügbar | Zu zahlender Betrag, der das Skonto enthält |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Der Debitor übermittelt eine Zahlung für 95,00 innerhalb des Skontoabzinsungsdatum. Die Zahlung wird mit der offenen Rechnung über 105,00 ausgeglichen. Nachdem die Rechnung und die Zahlung ausgeglichen sind, werden für den Debitor die folgenden Transaktionen in Debitor erstellt.

| Transaktion   | Betrag | Gesamtbetrag |
|---------------|--------|---------|
| Rechnung       | 105,00 | 0,00    |
| Zahlung       | -95,00 | -0,00   |
| Skonto | -10,00 | 0,00    |

Der Skontobetrag wird von 10,50 auf 10,00 verringert. Die Zahlung und die Rechnung gelten als ausgeglichen. **Zahlung**

| Konto             | Sollbetrag | Habenbetrag |
|---------------------|--------------|---------------|
| Bargeld                | 95,00        |               |
| Debitoren |              | 95,00         |

**Ausgleich**

| Konto                                                                                          | Sollbetrag | Habenbetrag |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Skonto (das Feld **Hauptkonto für Debitorenrabatte** auf der **Skonti** Seite) | 10,50        |               |
| Debitoren                                                                              |              | 10,50         |






