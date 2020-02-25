---
title: Buchungserfassung stornieren
description: In diesem Thema wird die Funktion beschrieben, mit der Belege von der Belegbuchungsliste oder von Finanzerfassungen storniert werden können.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08aec836ce4b7b6a59c445f138365f101a78c68e
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030921"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="b14c0-103">Buchungserfassung stornieren</span><span class="sxs-lookup"><span data-stu-id="b14c0-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b14c0-104">In diesem Thema wird die Funktion von Microsoft Dynamics 365 Finance beschrieben, die es Ihnen ermöglicht, eine gesamte Erfassung zu stornieren oder eine oder mehrere Belege aus der Belegbuchungsliste unabhängig von ihrem Ursprung umzukehren.</span><span class="sxs-lookup"><span data-stu-id="b14c0-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="b14c0-105">Stornieren von Erfassungen</span><span class="sxs-lookup"><span data-stu-id="b14c0-105">Reversing journals</span></span>

<span data-ttu-id="b14c0-106">Sie können Erfassungspositionen einzeln stornieren.</span><span class="sxs-lookup"><span data-stu-id="b14c0-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="b14c0-107">Mit Rückerfassungsbuchung können Sie eine gesamte Finanzerfassung auch stornieren.</span><span class="sxs-lookup"><span data-stu-id="b14c0-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="b14c0-108">So stornieren Sie eine Erfassung</span><span class="sxs-lookup"><span data-stu-id="b14c0-108">To reverse a journal:</span></span> 

- <span data-ttu-id="b14c0-109">Öffnen Sie die Finanzerfassung und filtern Sie die gebuchten Erfassungen.</span><span class="sxs-lookup"><span data-stu-id="b14c0-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="b14c0-110">Wählen Sie das Menü **Stornieren** oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="b14c0-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="b14c0-111">Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden</span><span class="sxs-lookup"><span data-stu-id="b14c0-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b14c0-112">Wählen Sie die Option **Ja** aus, um ein vorhandenes Buchungsdatum zu verwenden, oder **Nein**, um ein neues zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b14c0-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="b14c0-113">In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.</span><span class="sxs-lookup"><span data-stu-id="b14c0-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b14c0-114">Wenn Sie **Nein** ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein.</span><span class="sxs-lookup"><span data-stu-id="b14c0-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b14c0-115">Geben Sie einen Kommentar ein, der der Stornobuchung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b14c0-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="b14c0-116">Wählen Sie die Schaltfläche **Stornieren**.</span><span class="sxs-lookup"><span data-stu-id="b14c0-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="b14c0-117">Die Buchungen werden storniert.</span><span class="sxs-lookup"><span data-stu-id="b14c0-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="b14c0-118">Wenn der Beleg mehr als 100 Positionen enthält, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14c0-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="b14c0-119">Sie können die Ergebnisse überprüfen, indem Sie die Kommentare im Batchauftrag anzeigen, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b14c0-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="b14c0-120">Alle Buchungen, die nicht storniert werden konnten, werden in der Historie des Batchauftrags aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14c0-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="b14c0-121">Wenn der Beleg 100 oder weniger Positionen enthält, wird der Umkehr-Prozess sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14c0-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="b14c0-122">Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b14c0-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="b14c0-123">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b14c0-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="b14c0-124">Stornieren von Belegen mit der Belegbuchungsliste.</span><span class="sxs-lookup"><span data-stu-id="b14c0-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="b14c0-125">Sie können alle Belege von der **Belegbuchungsliste** in allen untergeordneten Sachkonten stornieren.</span><span class="sxs-lookup"><span data-stu-id="b14c0-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="b14c0-126">Darüber hinaus können Sie mehrere Belege gleichzeitig stornieren.</span><span class="sxs-lookup"><span data-stu-id="b14c0-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="b14c0-127">So stornieren Sie einen oder mehrere Belege:</span><span class="sxs-lookup"><span data-stu-id="b14c0-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="b14c0-128">Wählen Sie das Menü **Stornieren** oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="b14c0-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="b14c0-129">Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden.</span><span class="sxs-lookup"><span data-stu-id="b14c0-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="b14c0-130">Wählen Sie die Option **Ja** aus, um ein vorhandenes Buchungsdatum zu verwenden, oder **Nein**, um ein neues zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b14c0-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="b14c0-131">In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.</span><span class="sxs-lookup"><span data-stu-id="b14c0-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="b14c0-132">Wenn Sie **Nein** ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein.</span><span class="sxs-lookup"><span data-stu-id="b14c0-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b14c0-133">Geben Sie einen Kommentar ein, um die Stornobuchung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b14c0-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="b14c0-134">Wählen Sie die Schaltfläche **Stornieren**.</span><span class="sxs-lookup"><span data-stu-id="b14c0-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="b14c0-135">Die Buchungen werden storniert.</span><span class="sxs-lookup"><span data-stu-id="b14c0-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="b14c0-136">Wenn der Beleg mehr als 100 Positionen enthält, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14c0-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="b14c0-137">Sie können die Ergebnisse überprüfen, indem Sie die Kommentare im Batchauftrag anzeigen, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b14c0-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="b14c0-138">Alle Buchungen, die nicht storniert werden konnten, werden in der Historie des Batchauftrags aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14c0-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="b14c0-139">Wenn die Anzahl der Belegpositionen 100 oder weniger beträgt, wird der Umkehr-Prozess sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14c0-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="b14c0-140">Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b14c0-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="b14c0-141">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b14c0-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="b14c0-142">Buchungen können nur storniert werden, wenn sie die Geschäftsregeln für das Zurücksetzen sie gelten.</span><span class="sxs-lookup"><span data-stu-id="b14c0-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="b14c0-143">Kreditorenzahlungen können nicht mithilfe der Funktion storniert werden, die in diesem Thema beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b14c0-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="b14c0-144">Kreditorenzahlungen müssen storniert werden, indem die Schritte unter [Stornieren einer Kreditorenzahlung](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b14c0-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

