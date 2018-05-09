--- 
title: "Debitorenzahlungsgebühren einrichten"
description: "Erstellen Sie Zahlungsgebühren für Debitorenzahlungen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 02449aff2273d30e0d0d847e137e3283aef1839b
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="d1666-103">Debitorenzahlungsgebühren einrichten</span><span class="sxs-lookup"><span data-stu-id="d1666-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1666-104">Erstellen Sie Zahlungsgebühren für Debitorenzahlungen.</span><span class="sxs-lookup"><span data-stu-id="d1666-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="d1666-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1666-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d1666-106">Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsgebühr".</span><span class="sxs-lookup"><span data-stu-id="d1666-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="d1666-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d1666-107">Click New.</span></span>
3. <span data-ttu-id="d1666-108">Geben Sie im Feld "Gebührenkennung" eine Gebührenkennung ein.</span><span class="sxs-lookup"><span data-stu-id="d1666-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="d1666-109">Die "Gebührenkennung" wird auf Zahlungserfassungen angezeigt, damit sind sie beschreibend, um zu verstehen, welche Gebühr veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="d1666-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="d1666-110">Geben Sie im Feld "Name" einen Gebührennamen ein.</span><span class="sxs-lookup"><span data-stu-id="d1666-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="d1666-111">Geben Sie im Feld "Gebührenbeschreibung" eine Beschreibung für die Gebühr ein.</span><span class="sxs-lookup"><span data-stu-id="d1666-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="d1666-112">Wählen Sie aus, ob der Debitor oder ein Sachkonto mit der Gebühr belastet wird.</span><span class="sxs-lookup"><span data-stu-id="d1666-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="d1666-113">Wenn die Gebühr für den Debitor veranschlagt wird, wählen Sie "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="d1666-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="d1666-114">Wenn die Gebühr für Ihre Organisation als Ausgaben veranschlagt wird, wählen Sie "Sachkonto" aus.</span><span class="sxs-lookup"><span data-stu-id="d1666-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="d1666-115">Wählen Sie für diese Aufgabe "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="d1666-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="d1666-116">Wählen Sie den Erfassungstyp aus, der diese Zahlungsgebühr verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="d1666-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="d1666-117">Wenn diese Gebühren für Debitorenzahlungen verwendet werden, wird der Erfassungstyp wahrscheinlich "Debitorenzahlung" sein.</span><span class="sxs-lookup"><span data-stu-id="d1666-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="d1666-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d1666-118">Click Save.</span></span>
9. <span data-ttu-id="d1666-119">Klicken Sie auf "Zahlungsgebühreinstellungen".</span><span class="sxs-lookup"><span data-stu-id="d1666-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="d1666-120">Die Zahlungsgebühreneinstellungen werden verwendet, um die Kriterien zu definieren, wann die Zahlungsgebühr veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="d1666-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="d1666-121">So können Sie beispielsweise definieren, dass die Gebühr berechnet wird, wenn das Bankkonto USMF-OPERATION ist und die Zahlungsmethode per Scheck ist.</span><span class="sxs-lookup"><span data-stu-id="d1666-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="d1666-122">Wählen Sie entweder "Tabelle", "Gruppe" oder "Alle" aus, um zu definieren, welche Bankkonten für diese Gebühr bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="d1666-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="d1666-123">Wenn Sie "Alle" auswählen, könnte für alle Bankkonten diese Gebühr veranschlagt werden.</span><span class="sxs-lookup"><span data-stu-id="d1666-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="d1666-124">Wenn Sie "Tabelle" auswählen, kann nur für das Bankkonto, das Sie auswählen, diese Gebühr veranschlagt werden.</span><span class="sxs-lookup"><span data-stu-id="d1666-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="d1666-125">Wenn Sie "Gruppe" auswählen, könnte nur für Bankkonten in der ausgewählten Bankgruppe diese Gebühr veranschlagt bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="d1666-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="d1666-126">Wählen Sie entweder eine Bankgruppe oder ein Bankkonto aus.</span><span class="sxs-lookup"><span data-stu-id="d1666-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="d1666-127">Wenn Sie "Tabelle" ausgewählt haben, zeigt die Suche Bankkonten an.</span><span class="sxs-lookup"><span data-stu-id="d1666-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="d1666-128">Wenn Sie "Gruppe" ausgewählt haben, zeigt die Suche Bankgruppen an.</span><span class="sxs-lookup"><span data-stu-id="d1666-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="d1666-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d1666-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d1666-130">Wählen Sie die "Zahlungsmethode" aus, für die diese Gebühr veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="d1666-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="d1666-131">Beispielsweise veranschlagen Sie möglicherweise eine Gebühr für Ihre Debitoren, wenn sie Zahlungen als Scheck senden, anstatt als elektronische Zahlung.</span><span class="sxs-lookup"><span data-stu-id="d1666-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="d1666-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d1666-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="d1666-133">Falls relevant, geben Sie eine Zahlungswährung ein.</span><span class="sxs-lookup"><span data-stu-id="d1666-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="d1666-134">Die Zahlungswährung wird als zusätzliches Kriterien dafür verwendet, ob die Gebühr veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="d1666-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="d1666-135">Beispielsweise erhebt möglicherweise Ihrer Bank eine zusätzliche Gebühr für Zahlungseingänge in der USD-Währung, da sie normalerweise ihre Geschäfte nur in der EUR-Währung abwickelt.</span><span class="sxs-lookup"><span data-stu-id="d1666-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="d1666-136">Wählen Sie aus, ob die Gebühr ein Prozentsatz, ein Betrag oder ein Intervall ist.</span><span class="sxs-lookup"><span data-stu-id="d1666-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="d1666-137">Geben Sie entweder Prozentsatz oder Betrag der Gebühr ein.</span><span class="sxs-lookup"><span data-stu-id="d1666-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="d1666-138">Wenn das Feld "Prozentsatz/Betrag" die Bezeichnung "Prozent" hat, ist der Wert, den Sie hier eingeben, ein Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="d1666-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="d1666-139">Wenn das Feld "Prozentsatz/Betrag" die Bezeichnung "Betrag" hat, ist der Wert, den Sie hier eingeben, ein Betrag.</span><span class="sxs-lookup"><span data-stu-id="d1666-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="d1666-140">Wenn das Feld "Prozentsatz/Betrag" die Bezeichnung "Intervall" hat, verwenden Sie die Registerkarte "Intervall", um die Ebenen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d1666-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="d1666-141">Wählen Sie im Feld "Gebührenwährung" die Währung der Gebühr aus.</span><span class="sxs-lookup"><span data-stu-id="d1666-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="d1666-142">Dies ist die Währung, in der die Gebühr erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d1666-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="d1666-143">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d1666-143">Click Save.</span></span>


