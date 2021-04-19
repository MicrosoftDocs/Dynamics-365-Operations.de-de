---
title: Ausführen einer Debitorenrückerstattung
description: In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden. Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd8b32e04743fdde3cc339e1535f8ae58c518aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816291"
---
# <a name="reimburse-customers"></a><span data-ttu-id="720c5-104">Ausführen einer Debitorenrückerstattung</span><span class="sxs-lookup"><span data-stu-id="720c5-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="720c5-105">In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="720c5-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="720c5-106">Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten.</span><span class="sxs-lookup"><span data-stu-id="720c5-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="720c5-107">In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.</span><span class="sxs-lookup"><span data-stu-id="720c5-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="720c5-108">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="720c5-108">Prerequisite</span></span>                                                            | <span data-ttu-id="720c5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="720c5-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="720c5-110">Legen Sie den Mindest-Rückerstattungsbetrag für die juristische Person fest.</span><span class="sxs-lookup"><span data-stu-id="720c5-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="720c5-111">Geben Sie auf der Seite **Debitorenkontenparameter** im Bereich **Allgemeines** im Feld **Mindestrückerstattung** den Mindestbetrag für die Überzahlungsrückerstattung an Debitoren ein.</span><span class="sxs-lookup"><span data-stu-id="720c5-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="720c5-112">Optional: Fügen Sie ein Kreditorenkonto für jeden Debitor hinzu, der Erstattungen erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="720c5-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="720c5-113">Wählen Sie auf der Seite **Debitoren** auf dem Inforegister **Sonstige Details** im Feld **Kreditorenkonto** das Kreditorenkonto für den Debitor aus.</span><span class="sxs-lookup"><span data-stu-id="720c5-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="720c5-114">Wenn Sie Rückerstattungsbuchungen erstellen, wird eine Kreditorenrechnung für den Betrag des Saldo erstellt.</span><span class="sxs-lookup"><span data-stu-id="720c5-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="720c5-115">Im Rahmen des Rückerstattungsprozesses wird das Saldo für das Debitorenkonto entfernt. Außerdem wird ein fälliger Saldo für das Kreditorenkonto erstellt, das dem Debitor entspricht.</span><span class="sxs-lookup"><span data-stu-id="720c5-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="720c5-116">Führen Sie in der Debitorenbuchhaltung den **Rückerstattung**-Prozess (**Debitoren \> Periodische Aufgaben \> Rückerstattung**) aus.</span><span class="sxs-lookup"><span data-stu-id="720c5-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="720c5-117">Um alle Transaktionen unabhängig von den Hauptbuchdimensionen zu gruppieren, legen Sie die **Debitor zusammenfassen** Option auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="720c5-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="720c5-118">Um nur Transaktionen mit ähnlichen Sachkontodimensionen zu gruppieren, setzen Sie die Option auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="720c5-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="720c5-119">Wählen Sie **Debitoren mit ausstehenden Habentransaktionen einschließen** aus, um Debitoren auszuwählen, deren Abbuchungsbeträge nicht abgewickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="720c5-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="720c5-120">Um bestimmte Debitorenkonten zu erstatten, wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, und geben Sie dann die Debitorenkonten in der Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="720c5-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="720c5-121">Die Habenbeträge werden auf die Kreditorenkonten der Debitoren überwiesen und als gewöhnliche Zahlungen behandelt.</span><span class="sxs-lookup"><span data-stu-id="720c5-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="720c5-122">Ist für den Debitor kein Kreditorenkonto vorhanden, wird für diesen Debitor automatisch ein einmaliges Kreditorenkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="720c5-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="720c5-123">Um die erstellten Erstattungstransaktionen anzuzeigen, verwenden Sie den Bericht **Rückerstattung** (**Debitoren \> Anfragen und Berichte \> Erstattungsbericht**).</span><span class="sxs-lookup"><span data-stu-id="720c5-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="720c5-124">Im Kreditorenmodul erstellen Sie eine Zahlung für die Kreditorenrechnungen, die durch den Rückerstattungsprozess erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="720c5-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="720c5-125">Informationen zum Bezahlen von Kreditoren finden Sie unter [Übersicht über Kreditorenzahlungen](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="720c5-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]