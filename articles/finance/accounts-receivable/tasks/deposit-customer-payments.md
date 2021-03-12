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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9221101581a6a130889b7c941ca228070a000c56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003155"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="19006-103">Debitorenzahlungen empfangen</span><span class="sxs-lookup"><span data-stu-id="19006-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19006-104">Zahlen Sie Debitorenzahlungen ein.</span><span class="sxs-lookup"><span data-stu-id="19006-104">Deposit customer payments.</span></span> <span data-ttu-id="19006-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="19006-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="19006-106">Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungen > Zahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="19006-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="19006-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="19006-107">Select **New**.</span></span>
3. <span data-ttu-id="19006-108">Wählen Sie im Feld **Name** **CustPay** im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="19006-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="19006-109">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="19006-109">Select **Lines**.</span></span>
5. <span data-ttu-id="19006-110">Wählen Sie im Feld **Konto** den Debitor aus, für den Sie die Zahlung erfassen.</span><span class="sxs-lookup"><span data-stu-id="19006-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="19006-111">Geben Sie im Feld **Gutschrift** den Betrag der Zahlung ein.</span><span class="sxs-lookup"><span data-stu-id="19006-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="19006-112">Falls gewünscht, können Sie den Betrag leer lassen und dessen Berechnung dem System überlassen, indem Sie die Rechnungen auswählen, die bezahlt wurden.</span><span class="sxs-lookup"><span data-stu-id="19006-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="19006-113">Geben Sie im Feld **Zahlungsreferenz** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="19006-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="19006-114">Die Zahlungsreferenz kann die Schecknummer für die Zahlung sein, die Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="19006-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="19006-115">Die Zahlungsreferenz ist erforderlich, um die Zahlung auf einem Einzahlungsbeleg einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="19006-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="19006-116">Markieren Sie das Feld "Einzahlungsbeleg verwenden".</span><span class="sxs-lookup"><span data-stu-id="19006-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="19006-117">Wenn die Zahlung in der Einzahlung enthalten sein soll, ändern Sie diese Einstellung auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="19006-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="19006-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="19006-118">Select **New**.</span></span>
10. <span data-ttu-id="19006-119">Wählen Sie im Feld **Konto** den Debitoren für die nächste Zahlung aus.</span><span class="sxs-lookup"><span data-stu-id="19006-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="19006-120">Geben Sie im Feld **Gutschrift** den Zahlungsbetrag ein.</span><span class="sxs-lookup"><span data-stu-id="19006-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="19006-121">Geben Sie im Feld **Zahlungsreferenz** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="19006-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="19006-122">Markieren Sie das Feld **Einzahlungsbeleg verwenden**.</span><span class="sxs-lookup"><span data-stu-id="19006-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="19006-123">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="19006-123">Select **Post**.</span></span> <span data-ttu-id="19006-124">Zahlungen müssen gebucht werden, bevor der Einzahlungsbeleg generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="19006-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="19006-125">Damit soll sichergestellt werden, dass die Zahlungen sich nicht ändern, nachdem der Einzahlungsbeleg generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="19006-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="19006-126">Wählen Sie **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="19006-126">Select **Functions**.</span></span>
16. <span data-ttu-id="19006-127">Wählen Sie **Einzahlungsbeleg** aus.</span><span class="sxs-lookup"><span data-stu-id="19006-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="19006-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="19006-128">Select **OK**.</span></span> <span data-ttu-id="19006-129">Die erste Seite wird verwendet, um den Einzahlungsbeleg zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="19006-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="19006-130">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="19006-130">Select **OK**.</span></span> <span data-ttu-id="19006-131">Der zweite Schritt ist, den Einzahlungsbeleg zu drucken, aber dieser Schritt ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19006-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

