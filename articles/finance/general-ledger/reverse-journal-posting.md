---
title: Buchungserfassung stornieren
description: In diesem Thema wird die Funktion beschrieben, mit der Belege von der Belegbuchungsliste oder von Finanzerfassungen storniert werden können.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248584"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="61b6e-103">Buchungserfassung stornieren</span><span class="sxs-lookup"><span data-stu-id="61b6e-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61b6e-104">In diesem Thema wird die Funktion von Microsoft Dynamics 365 Finance beschrieben, die es Ihnen ermöglicht, eine gesamte Erfassung zu stornieren oder eine oder mehrere Belege aus der Belegbuchungsliste unabhängig von ihrem Ursprung umzukehren.</span><span class="sxs-lookup"><span data-stu-id="61b6e-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="61b6e-105">Stornieren von Erfassungen</span><span class="sxs-lookup"><span data-stu-id="61b6e-105">Reversing journals</span></span>

<span data-ttu-id="61b6e-106">Sie können Erfassungspositionen einzeln stornieren.</span><span class="sxs-lookup"><span data-stu-id="61b6e-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="61b6e-107">Mit Rückerfassungsbuchung können Sie eine gesamte Finanzerfassung auch stornieren.</span><span class="sxs-lookup"><span data-stu-id="61b6e-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="61b6e-108">So stornieren Sie eine Erfassung</span><span class="sxs-lookup"><span data-stu-id="61b6e-108">To reverse a journal:</span></span> 
- <span data-ttu-id="61b6e-109">Öffnen Sie die Finanzerfassung und filtern Sie die gebuchten Erfassungen</span><span class="sxs-lookup"><span data-stu-id="61b6e-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="61b6e-110">Klicken Sie im Menü „Stornieren“ oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="61b6e-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="61b6e-111">Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden</span><span class="sxs-lookup"><span data-stu-id="61b6e-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="61b6e-112">Wählen Sie die Option „Ja“ aus, um ein vorhandenes Buchungsdatum zu verwenden, oder „Nein“, um ein neues zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="61b6e-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="61b6e-113">In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.</span><span class="sxs-lookup"><span data-stu-id="61b6e-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="61b6e-114">Wenn Sie „Nein“ ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein.</span><span class="sxs-lookup"><span data-stu-id="61b6e-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="61b6e-115">Geben Sie einen Kommentar ein, der der Stornobuchung hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="61b6e-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="61b6e-116">Klicken Sie auf die Schaltfläche „Stornieren“.</span><span class="sxs-lookup"><span data-stu-id="61b6e-116">Click the Reverse button</span></span>

<span data-ttu-id="61b6e-117">Die Buchungen werden storniert.</span><span class="sxs-lookup"><span data-stu-id="61b6e-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="61b6e-118">Wenn die Anzahl der Belegpositionen 100 übersteigt, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61b6e-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="61b6e-119">Sie können die Ergebnisse einer Stornierung überprüfen, indem Sie die Kommentare im Stapelverarbeitungsauftrag anzeigen, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="61b6e-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="61b6e-120">Alle Fehler werden in der Historie vermerkt.</span><span class="sxs-lookup"><span data-stu-id="61b6e-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="61b6e-121">Wenn die Anzahl der Belegpositionen 100 oder weniger beträgt, wird der Umkehr-Prozess sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61b6e-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="61b6e-122">Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="61b6e-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="61b6e-123">Um das Dialogfeld zu schließen, klicken Sie auf „OK“.</span><span class="sxs-lookup"><span data-stu-id="61b6e-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="61b6e-124">Stornieren von Belegen mit der Belegbuchungsliste.</span><span class="sxs-lookup"><span data-stu-id="61b6e-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="61b6e-125">Sie können alle Belege von der **Belegbuchungsliste** in allen untergeordneten Sachkonten stornieren.</span><span class="sxs-lookup"><span data-stu-id="61b6e-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="61b6e-126">Darüber hinaus können Sie mehrere Belege gleichzeitig stornieren.</span><span class="sxs-lookup"><span data-stu-id="61b6e-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="61b6e-127">So stornieren Sie einen oder mehrere Belege:</span><span class="sxs-lookup"><span data-stu-id="61b6e-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="61b6e-128">Klicken Sie im Menü „Stornieren“ oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="61b6e-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="61b6e-129">Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden</span><span class="sxs-lookup"><span data-stu-id="61b6e-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="61b6e-130">Wählen Sie die Option „Ja“ aus, um ein vorhandenes Buchungsdatum zu verwenden, oder „Nein“, um ein neues zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="61b6e-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="61b6e-131">In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.</span><span class="sxs-lookup"><span data-stu-id="61b6e-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="61b6e-132">Wenn Sie „Nein“ ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein.</span><span class="sxs-lookup"><span data-stu-id="61b6e-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="61b6e-133">Geben Sie einen Kommentar ein, der der Stornobuchung hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="61b6e-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="61b6e-134">Klicken Sie auf die Schaltfläche „Stornieren“.</span><span class="sxs-lookup"><span data-stu-id="61b6e-134">Click the Reverse button</span></span>

<span data-ttu-id="61b6e-135">Die Buchungen werden storniert.</span><span class="sxs-lookup"><span data-stu-id="61b6e-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="61b6e-136">Wenn die Anzahl der Belegpositionen 100 übersteigt, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61b6e-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="61b6e-137">Sie können die Ergebnisse einer Stornierung überprüfen, indem Sie die Kommentare im Stapelverarbeitungsauftrag anzeigen, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="61b6e-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="61b6e-138">Alle Fehler werden in der Historie vermerkt.</span><span class="sxs-lookup"><span data-stu-id="61b6e-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="61b6e-139">Wenn die Anzahl der Belegpositionen 100 oder weniger beträgt, wird der Umkehr-Prozess sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61b6e-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="61b6e-140">Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="61b6e-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="61b6e-141">Um das Dialogfeld zu schließen, klicken Sie auf „OK“.</span><span class="sxs-lookup"><span data-stu-id="61b6e-141">Click on Ok to close the dialog.</span></span>

