---
title: "Ausführen einer Debitorenrückerstattung"
description: "In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden. Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 01c9dcebe82544624c6dd0feb3672d1c5bdfe2d1
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="reimburse-customers"></a><span data-ttu-id="387e4-104">Ausführen einer Debitorenrückerstattung</span><span class="sxs-lookup"><span data-stu-id="387e4-104">Reimburse customers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="387e4-105">In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="387e4-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="387e4-106">Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten.</span><span class="sxs-lookup"><span data-stu-id="387e4-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="387e4-107">In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.</span><span class="sxs-lookup"><span data-stu-id="387e4-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="387e4-108">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="387e4-108">Prerequisite</span></span>                                                            | <span data-ttu-id="387e4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="387e4-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="387e4-110">Legen Sie den Mindest-Rückerstattungsbetrag für die juristische Person fest.</span><span class="sxs-lookup"><span data-stu-id="387e4-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="387e4-111">Geben Sie auf der Seite **Debitorenkontenparameter** im Bereich **Allgemeines** im Feld **Mindestrückerstattung** den Mindestbetrag für die Überzahlungsrückerstattung an Debitoren ein.</span><span class="sxs-lookup"><span data-stu-id="387e4-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="387e4-112">Optional: Fügen Sie ein Kreditorenkonto für jeden Debitor hinzu, der Erstattungen erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="387e4-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="387e4-113">Wählen Sie auf der Seite **Debitoren** auf dem Inforegister **Sonstige Details** im Feld **Kreditorenkonto** das Kreditorenkonto für den Debitor aus.</span><span class="sxs-lookup"><span data-stu-id="387e4-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="387e4-114">Wenn Sie Rückerstattungsbuchungen erstellen, wird eine Kreditorenrechnung für den Betrag des Saldo erstellt.</span><span class="sxs-lookup"><span data-stu-id="387e4-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="387e4-115">Im Rahmen des Rückerstattungsprozesses wird das Saldo für das Debitorenkonto entfernt. Außerdem wird ein fälliger Saldo für das Kreditorenkonto erstellt, das dem Debitor entspricht.</span><span class="sxs-lookup"><span data-stu-id="387e4-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="387e4-116">Führen Sie im Debitorenmodul den Prozess **Rückerstattung** aus.</span><span class="sxs-lookup"><span data-stu-id="387e4-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="387e4-117">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="387e4-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="387e4-118">Klicken Sie zum Vornehmen einer Rückerstattung für bestimmte Debitorenkonten auf **Auswählen**, und geben Sie in der Abfrage die gewünschten Debitorenkonten an.</span><span class="sxs-lookup"><span data-stu-id="387e4-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="387e4-119">Klicken Sie zum Vornehmen einer Rückerstattung für alle Konten auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="387e4-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="387e4-120">Die Habenbeträge werden auf die Kreditorenkonten der Debitoren überwiesen und als gewöhnliche Zahlungen behandelt.</span><span class="sxs-lookup"><span data-stu-id="387e4-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="387e4-121">Ist für den Debitor kein Kreditorenkonto vorhanden, wird für diesen Debitor automatisch ein einmaliges Kreditorenkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="387e4-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="387e4-122">Die erstellten Rückerstattungstransaktionen zeigen Sie auf der Seite **Rückerstattung** an.</span><span class="sxs-lookup"><span data-stu-id="387e4-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="387e4-123">Im Kreditorenmodul erstellen Sie eine Zahlung für die Kreditorenrechnungen, die durch den Rückerstattungsprozess erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="387e4-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





