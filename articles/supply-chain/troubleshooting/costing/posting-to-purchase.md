---
title: Einkaufsabgrenzungen mit einem Betrag von Null werden bei einem Warenzugang mit dem Wert von Null gebucht
description: Wenn ein Produktzugang mit dem Wert Null gebucht wird, erstellt das System eine Buchung zur Einkaufsabgrenzung, bei der der Betrag 0 (Null) beträgt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026557"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Einkaufsabgrenzungen mit einem Betrag von Null werden bei einem Warenzugang mit dem Wert von Null gebucht

KB-Nummer: 4612588

## <a name="symptoms"></a>Symptome

Wenn ein Produktzugang mit dem Wert Null gebucht wird, erstellt das System eine Buchung zur Einkaufsabgrenzung, bei der der Betrag 0 (Null) beträgt.

## <a name="resolution"></a>Lösung

Standardmäßig ist in Sachkontobuchungen vom Typ *Einkauf, Abgrenzung* das Feld `IsTransferredIndetail` bei Buchungen in untergeordneten Sachkonten immer auch *Zusammenfassung* gesetzt. Daher erstellt das System einen zugehörigen Belegeintrag, auch wenn der Betrag 0 (Null) ist.

Um diesen Buchungstyp zu überspringen, wenn der Betrag 0 (Null) ist, erweitern Sie die Methode `subledgerJournalizer.markDoNotTransferEntries`, sodass sie wie im folgenden Beispiel `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` enthält.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
