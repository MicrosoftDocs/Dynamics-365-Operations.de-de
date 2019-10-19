---
title: Debitorenzahlungen empfangen
description: Zahlen Sie Debitorenzahlungen ein.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177953"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="7f449-103">Debitorenzahlungen empfangen</span><span class="sxs-lookup"><span data-stu-id="7f449-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f449-104">Zahlen Sie Debitorenzahlungen ein.</span><span class="sxs-lookup"><span data-stu-id="7f449-104">Deposit customer payments.</span></span> <span data-ttu-id="7f449-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f449-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="7f449-106">Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungen > Zahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="7f449-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="7f449-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-107">Select **New**.</span></span>
3. <span data-ttu-id="7f449-108">Wählen Sie im Feld **Name** **CustPay** im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="7f449-109">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-109">Select **Lines**.</span></span>
5. <span data-ttu-id="7f449-110">Wählen Sie im Feld **Konto** den Debitor aus, für den Sie die Zahlung erfassen.</span><span class="sxs-lookup"><span data-stu-id="7f449-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="7f449-111">Geben Sie im Feld **Gutschrift** den Betrag der Zahlung ein.</span><span class="sxs-lookup"><span data-stu-id="7f449-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="7f449-112">Falls gewünscht, können Sie den Betrag leer lassen und dessen Berechnung dem System überlassen, indem Sie die Rechnungen auswählen, die bezahlt wurden.</span><span class="sxs-lookup"><span data-stu-id="7f449-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="7f449-113">Geben Sie im Feld **Zahlungsreferenz** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f449-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="7f449-114">Die Zahlungsreferenz kann die Schecknummer für die Zahlung sein, die Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="7f449-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="7f449-115">Die Zahlungsreferenz ist erforderlich, um die Zahlung auf einem Einzahlungsbeleg einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="7f449-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="7f449-116">Markieren Sie das Feld "Einzahlungsbeleg verwenden".</span><span class="sxs-lookup"><span data-stu-id="7f449-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="7f449-117">Wenn die Zahlung in der Einzahlung enthalten sein soll, ändern Sie diese Einstellung auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="7f449-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="7f449-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-118">Select **New**.</span></span>
10. <span data-ttu-id="7f449-119">Wählen Sie im Feld **Konto** den Debitoren für die nächste Zahlung aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="7f449-120">Geben Sie im Feld **Gutschrift** den Zahlungsbetrag ein.</span><span class="sxs-lookup"><span data-stu-id="7f449-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="7f449-121">Geben Sie im Feld **Zahlungsreferenz** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f449-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="7f449-122">Markieren Sie das Feld **Einzahlungsbeleg verwenden**.</span><span class="sxs-lookup"><span data-stu-id="7f449-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="7f449-123">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-123">Select **Post**.</span></span> <span data-ttu-id="7f449-124">Zahlungen müssen gebucht werden, bevor der Einzahlungsbeleg generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f449-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="7f449-125">Damit soll sichergestellt werden, dass die Zahlungen sich nicht ändern, nachdem der Einzahlungsbeleg generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7f449-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="7f449-126">Wählen Sie **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-126">Select **Functions**.</span></span>
16. <span data-ttu-id="7f449-127">Wählen Sie **Einzahlungsbeleg** aus.</span><span class="sxs-lookup"><span data-stu-id="7f449-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="7f449-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f449-128">Select **OK**.</span></span> <span data-ttu-id="7f449-129">Die erste Seite wird verwendet, um den Einzahlungsbeleg zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f449-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="7f449-130">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f449-130">Select **OK**.</span></span> <span data-ttu-id="7f449-131">Der zweite Schritt ist, den Einzahlungsbeleg zu drucken, aber dieser Schritt ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f449-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

