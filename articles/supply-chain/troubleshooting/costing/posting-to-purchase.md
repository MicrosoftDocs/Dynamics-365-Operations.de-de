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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="d4d86-103">Einkaufsabgrenzungen mit einem Betrag von Null werden bei einem Warenzugang mit dem Wert von Null gebucht</span><span class="sxs-lookup"><span data-stu-id="d4d86-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="d4d86-104">KB-Nummer: 4612588</span><span class="sxs-lookup"><span data-stu-id="d4d86-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="d4d86-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="d4d86-105">Symptoms</span></span>

<span data-ttu-id="d4d86-106">Wenn ein Produktzugang mit dem Wert Null gebucht wird, erstellt das System eine Buchung zur Einkaufsabgrenzung, bei der der Betrag 0 (Null) beträgt.</span><span class="sxs-lookup"><span data-stu-id="d4d86-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="d4d86-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="d4d86-107">Resolution</span></span>

<span data-ttu-id="d4d86-108">Standardmäßig ist in Sachkontobuchungen vom Typ *Einkauf, Abgrenzung* das Feld `IsTransferredIndetail` bei Buchungen in untergeordneten Sachkonten immer auch *Zusammenfassung* gesetzt.</span><span class="sxs-lookup"><span data-stu-id="d4d86-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="d4d86-109">Daher erstellt das System einen zugehörigen Belegeintrag, auch wenn der Betrag 0 (Null) ist.</span><span class="sxs-lookup"><span data-stu-id="d4d86-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="d4d86-110">Um diesen Buchungstyp zu überspringen, wenn der Betrag 0 (Null) ist, erweitern Sie die Methode `subledgerJournalizer.markDoNotTransferEntries`, sodass sie wie im folgenden Beispiel `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` enthält.</span><span class="sxs-lookup"><span data-stu-id="d4d86-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
