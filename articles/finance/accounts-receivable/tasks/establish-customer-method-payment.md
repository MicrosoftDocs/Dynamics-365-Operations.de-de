---
title: Debitorenzahlungsmethode festlegen
description: In diesem Thema wird erläutert, wie eine Zahlungsmethode für Debitorenzahlungen erstellt wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b9960c3fdf0d65be19e28dbb41913a310ae7530
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140213"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="a760e-103">Debitorenzahlungsmethode festlegen</span><span class="sxs-lookup"><span data-stu-id="a760e-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a760e-104">In diesem Thema wird erläutert, wie eine Zahlungsmethode für Debitorenzahlungen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a760e-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="a760e-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="a760e-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a760e-106">Wechseln Sie im Navigationsbereich zu **Module > Debitorenkonten > Zahlungseinstellungen > Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="a760e-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="a760e-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a760e-107">Select **New**.</span></span>
3. <span data-ttu-id="a760e-108">Geben Sie im Feld **Zahlungsmethode** eine Kennung für die Zahlungsmethode ein.</span><span class="sxs-lookup"><span data-stu-id="a760e-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="a760e-109">Die "Zahlungsmethodenkennung" wird auf Rechnungen und Zahlungen angezeigt, damit werden sie beschreibend genug, um zu verstehen, welche Art der Zahlung erfasst wird und für welches Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="a760e-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="a760e-110">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="a760e-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a760e-111">Wählen Sie aus, welcher Zahlungsstatus erforderlich ist, damit Zahlungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a760e-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="a760e-112">Wird eine Debitorenzahlung erstellt, kann sie nur gebucht werden, wenn der Zahlungsstatus mit dem Zahlungsstatus übereinstimmt, den Sie hier definieren.</span><span class="sxs-lookup"><span data-stu-id="a760e-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="a760e-113">Wählen Sie aus, wie Debitorenzahlungen für Rechnungen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a760e-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="a760e-114">Diese Option wird nur verwendet, wenn ein Zahlungsvorschlag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a760e-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="a760e-115">Ein Zahlungsvorschlag könnte für Debitorenzahlungen verwendet werden, wenn Direktbelastungen ausgeführt werden und die Mittel aus den Bankkonten der Debitoren eingezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a760e-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="a760e-116">Wählen Sie den Typ der Zahlung aus.</span><span class="sxs-lookup"><span data-stu-id="a760e-116">Select the type of payment.</span></span> <span data-ttu-id="a760e-117">Mithilfe des Zahlungstyps können Sie feststellen, ob irgendeine Prüfung für die Zahlung erfolgt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a760e-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="a760e-118">Wählen Sie aus, auf welchen Kontotyp Zahlungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a760e-118">Select what account type payments will post to.</span></span> <span data-ttu-id="a760e-119">Normalerweise wird Bank für diese Option aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a760e-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="a760e-120">Wählen Sie das Bankkonto aus, in dem diese Zahlung erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="a760e-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="a760e-121">Geben Sie den Banktransaktionstyp ein, um den Typ der Zahlung zu identifizieren, der von Ihrer Bank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a760e-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="a760e-122">Der Banktransaktionstyp wird während des Bankabstimmungsprozesses verwendet und kann die Abstimmung erleichtern.</span><span class="sxs-lookup"><span data-stu-id="a760e-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="a760e-123">Wählen Sie aus, ob diese Zahlung vorübergehend auf ein Transferkonto gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a760e-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="a760e-124">Wenn Sie die Zeittoleranz ausprobieren möchten, mit der eine Zahlung bei der Bank verrechnet wird, verwenden Sie die Funktionen "Transfer".</span><span class="sxs-lookup"><span data-stu-id="a760e-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="a760e-125">Die Zahlung wird vorübergehend zu einem "Sachkonto" gebucht, bis sie bei der Bank verrechnet wird. Zu diesem Zeitpunkt erreicht die Zahlung das Bankkonto, das Sie hier definiert haben.</span><span class="sxs-lookup"><span data-stu-id="a760e-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="a760e-126">'Geben Sie das Hauptkonto ein, das für die Transferbuchung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a760e-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="a760e-127">Dies ist das Hauptkonto, auf das die Zahlung vorübergehend gebucht wird, wenn Sie den Transfer verwenden.</span><span class="sxs-lookup"><span data-stu-id="a760e-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="a760e-128">Verwenden Sie die Registerkarte **Dateiformat**, um Einstellungen für elektronische Zahlungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a760e-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="a760e-129">Verwenden Sie die Registerkarte **Zahlungskontrolle**, um Felder zu definieren, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a760e-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="a760e-130">Wenn Sie beispielsweise verlangen, dass alle Zahlungen mit dieser Zahlungsmethode eingezahlt werden, können Sie diese Option auf dieser Registerkarte auswählen.</span><span class="sxs-lookup"><span data-stu-id="a760e-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="a760e-131">Verwenden Sie die Registerkarte **Zahlungsattribute**, um zu definieren, welche Zahlungsattribute Sie für diese Zahlungsmethode verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a760e-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="a760e-132">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a760e-132">Select **Save**.</span></span>

