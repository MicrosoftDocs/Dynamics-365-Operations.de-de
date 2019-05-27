---
title: Debitorenzahlungen empfangen
description: Zahlen Sie Debitorenzahlungen ein.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565484"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="e9636-103">Debitorenzahlungen empfangen</span><span class="sxs-lookup"><span data-stu-id="e9636-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9636-104">Zahlen Sie Debitorenzahlungen ein.</span><span class="sxs-lookup"><span data-stu-id="e9636-104">Deposit customer payments.</span></span> <span data-ttu-id="e9636-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9636-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e9636-106">Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="e9636-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e9636-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e9636-107">Click New.</span></span>
3. <span data-ttu-id="e9636-108">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9636-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e9636-109">Wählen Sie die Zahlungserfassung aus.</span><span class="sxs-lookup"><span data-stu-id="e9636-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="e9636-110">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="e9636-110">Click Lines.</span></span>
6. <span data-ttu-id="e9636-111">Wählen Sie im Feld "Konto" den "Debitor" aus, für den Sie die Zahlung erfassen.</span><span class="sxs-lookup"><span data-stu-id="e9636-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="e9636-112">Geben Sie im Feld "Gutschrift" den Betrag der Zahlung ein.</span><span class="sxs-lookup"><span data-stu-id="e9636-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="e9636-113">Falls gewünscht, können Sie den Betrag leer lassen und dessen Berechnung dem System überlassen, indem Sie die Rechnungen auswählen, die bezahlt wurden.</span><span class="sxs-lookup"><span data-stu-id="e9636-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="e9636-114">Geben Sie im Feld "Zahlungsreferenz" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e9636-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="e9636-115">Die Zahlungsreferenz kann die Schecknummer für die Zahlung sein, die Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="e9636-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="e9636-116">Die Zahlungsreferenz ist erforderlich, um die Zahlung auf einem Einzahlungsbeleg einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e9636-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="e9636-117">Markieren Sie das Feld "Einzahlungsbeleg verwenden".</span><span class="sxs-lookup"><span data-stu-id="e9636-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="e9636-118">Wenn die Zahlung in der Einzahlung enthalten sein soll, ändern Sie diese Einstellung auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="e9636-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="e9636-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e9636-119">Click New.</span></span>
11. <span data-ttu-id="e9636-120">Wählen Sie im Feld "Konto" den Debitoren für die nächste Zahlung aus.</span><span class="sxs-lookup"><span data-stu-id="e9636-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="e9636-121">Geben Sie im Feld "Gutschrift" den Zahlungsbetrag ein.</span><span class="sxs-lookup"><span data-stu-id="e9636-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="e9636-122">Geben Sie im Feld "Zahlungsreferenz" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e9636-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="e9636-123">Markieren Sie das Feld "Einzahlungsbeleg verwenden".</span><span class="sxs-lookup"><span data-stu-id="e9636-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="e9636-124">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="e9636-124">Click Post.</span></span>
    * <span data-ttu-id="e9636-125">Zahlungen müssen gebucht werden, bevor der Einzahlungsbeleg generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9636-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="e9636-126">Damit soll sichergestellt werden, dass die Zahlungen sich nicht ändern, nachdem der Einzahlungsbeleg generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e9636-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="e9636-127">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e9636-127">Click Functions.</span></span>
17. <span data-ttu-id="e9636-128">Klicken Sie auf "Einzahlungsbeleg".</span><span class="sxs-lookup"><span data-stu-id="e9636-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="e9636-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e9636-129">Click OK.</span></span>
    * <span data-ttu-id="e9636-130">Die erste Seite wird verwendet, um den Einzahlungsbeleg zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9636-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="e9636-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e9636-131">Click OK.</span></span>
    * <span data-ttu-id="e9636-132">Der zweite Schritt ist, den Einzahlungsbeleg zu drucken, aber dieser Schritt ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9636-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

