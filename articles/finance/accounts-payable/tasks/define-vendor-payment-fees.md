---
title: Gebühren für Kreditorenzahlung definieren
description: Richten Sie Kreditorenzahlungsgebühren ein.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 404bd1e22caa8098f114a2dcc67dd420509cce2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443414"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="bf29c-103">Gebühren für Kreditorenzahlung definieren</span><span class="sxs-lookup"><span data-stu-id="bf29c-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf29c-104">Richten Sie Kreditorenzahlungsgebühren ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-104">Set up vendor payment fees.</span></span> <span data-ttu-id="bf29c-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf29c-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="bf29c-106">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsgebühr".</span><span class="sxs-lookup"><span data-stu-id="bf29c-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="bf29c-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="bf29c-107">Click New.</span></span>
3. <span data-ttu-id="bf29c-108">Geben Sie im Feld "Gebührenkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="bf29c-109">Die "Gebührenkennung" sollte beschreiben, wann diese Gebühr verwendet wird, beispielsweise "Gebühr für Überweisung (elektronisch)".</span><span class="sxs-lookup"><span data-stu-id="bf29c-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="bf29c-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bf29c-111">Geben Sie im Feld "Gebührenbeschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="bf29c-112">Fügen Sie eine Beschreibung hinzu, um weitere Informationen dazu bereitzustellen, wann die Gebühr veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="bf29c-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="bf29c-113">Wählen Sie im Feld "Belastung" entweder "Kreditor" oder "Sachkonto" aus.</span><span class="sxs-lookup"><span data-stu-id="bf29c-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="bf29c-114">Sachkonto wird verwendet, wenn die Gebühr zu Ihrer Organisation in Aufwand gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="bf29c-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="bf29c-115">Kreditor wird verwendet, wenn die Gebühr dem Kreditor veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="bf29c-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="bf29c-116">Geben Sie ein Hauptkonto ein, für das die Gebühr in Aufwand gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="bf29c-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="bf29c-117">Diese Option ist nur verfügbar, wenn "Sachkonto" als Option für "Belastung" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf29c-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="bf29c-118">Wählen Sie die Erfassung aus, für die diese Gebühr verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf29c-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="bf29c-119">Für eine Kreditorenzahlungsgebühr würden Sie die Erfassung "Kreditorenzahlung" auswählen.</span><span class="sxs-lookup"><span data-stu-id="bf29c-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="bf29c-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="bf29c-120">Click Save.</span></span>
10. <span data-ttu-id="bf29c-121">Klicken Sie auf "Zahlungsgebühreinstellungen".</span><span class="sxs-lookup"><span data-stu-id="bf29c-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="bf29c-122">Fahren Sie fort zu den "Zahlungsgebühreneinstellungen", um zu definieren, wann sich die Gebühr standardmäßig auf die Erfassung, die Sie ausgewählt haben, beziehen soll.</span><span class="sxs-lookup"><span data-stu-id="bf29c-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="bf29c-123">Wählen Sie entweder "Tabelle", "Gruppe" oder "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="bf29c-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="bf29c-124">Tabelle wird verwendet, um ein einzelnes Bankkonto auszuwählen, "Gruppe" wird verwendet, um eine Bankgruppe auszuwählen, und "Alle" wird verwendet, um diese Gebühreneinstellungen für alle Bankkonten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf29c-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="bf29c-125">Wählen Sie entweder eine Bankgruppe oder ein Bankkonto aus.</span><span class="sxs-lookup"><span data-stu-id="bf29c-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="bf29c-126">Die Suche wird Bankgruppe anzeigen, wenn Sie "Gruppe" ausgewählt haben, und wird Bankkonten anzeigen, wenn Sie "Tabelle" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bf29c-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="bf29c-127">Wählen Sie die Zahlungsmethode aus, für wann diese Gebühr veranschlagt wird.</span><span class="sxs-lookup"><span data-stu-id="bf29c-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="bf29c-128">Wählen Sie die "Zahlungsspezifikation" für die ausgewählte Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="bf29c-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="bf29c-129">Die Zahlungsspezifikation wird mit Methoden des elektronischen Geldverkehrs für Zahlungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf29c-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="bf29c-130">Wählen Sie aus, ob die Gebühr ein Prozentsatz, ein Betrag oder ein Intervall ist.</span><span class="sxs-lookup"><span data-stu-id="bf29c-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="bf29c-131">Geben Sie den Prozentsatz oder Betrag der Gebühr ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="bf29c-132">Wenn die "Gebühr" ein Prozentsatz ist, geben Sie den Prozentsatz ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="bf29c-133">Wenn die "Gebühr" ein Betrag ist, geben Sie den Betrag der Gebühr ein.</span><span class="sxs-lookup"><span data-stu-id="bf29c-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="bf29c-134">Wenn die "Gebühr" ein Intervall ist, verwenden Sie die Registerkarte "Intervall", um die gestaffelten Gebühren zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bf29c-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="bf29c-135">Wählen Sie im Feld "Gebührwährung" die Währung aus, in der die Gebühr berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="bf29c-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="bf29c-136">Diese Währung ist für die Gebühr.</span><span class="sxs-lookup"><span data-stu-id="bf29c-136">This currency is for the fee.</span></span> <span data-ttu-id="bf29c-137">Die Zahlungswährung wird verwendet, um zu definieren, wann die Gebührenregel basierend auf der Währung der Zahlung veranschlagt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf29c-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="bf29c-138">Beispielsweise erhebt Ihre Bank möglicherweise eine Gebühr, wenn eine Zahlung in EUR geleistet wird, aber bei allen anderen Zahlungen wird keine Gebühr veranschlagt.</span><span class="sxs-lookup"><span data-stu-id="bf29c-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="bf29c-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="bf29c-139">Click Save.</span></span>

