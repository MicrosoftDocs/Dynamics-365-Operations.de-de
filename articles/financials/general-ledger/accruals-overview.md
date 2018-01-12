---
title: "Abgrenzungsüberblick"
description: Dieser Artikel beschreibt Abgrenzungen und gibt Informationen, wie sie aufgesetzt werden und wie Transaktionen erstellt werden.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 47336a19899b1fad0e63265173fd7fd02fc74ec3
ms.openlocfilehash: 4fa27cbfe6129aa78b5e05de704894da173d853b
ms.contentlocale: de-de
ms.lasthandoff: 01/12/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="3c15e-103">Abgrenzungsüberblick</span><span class="sxs-lookup"><span data-stu-id="3c15e-103">Accruals overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3c15e-104">Dieser Artikel beschreibt Abgrenzungen und gibt Informationen, wie sie aufgesetzt werden und wie Transaktionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="3c15e-105">Abgrenzungen werden in der periodengerechten Abgrenzung verwendet, um den Umsatzerlös zu verfolgen, der in der Periode realisiert wird, in der er erzielt wurde und nicht bezahlt, und um Aufwendungen (Kosten) zu verfolgen, die realisiert werden, wenn Sie entstehen, nicht wenn Sie bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="3c15e-106">Abgrenzungsschemata</span><span class="sxs-lookup"><span data-stu-id="3c15e-106">Accrual schemes</span></span>
<span data-ttu-id="3c15e-107">Abgrenzungsschemata werden verwendet, um den Umsatzerlös und die Kosten einzurichten. Das gleiche Abgrenzungsschema kann für Umsatzerlöse und Kosten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="3c15e-108">Mit Sachkontoabgrenzungen werden die Kosten oder der Umsatzerlös einer Erfassungsposition neu verteilt, damit die Kosten und Umsatzerlöse in den entsprechenden Perioden berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="3c15e-109">Geben Sie auf der **Abgrenzungsschema**-Seite das die Soll- und Habenkonten an, die verwendet werden, wenn das Abgrenzungsschema angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c15e-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="3c15e-110">**Soll** - Das Hauptkonto, das Sie definieren, ersetzt das Sollhauptkonto auf der Erfassungsbelegposition.</span><span class="sxs-lookup"><span data-stu-id="3c15e-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="3c15e-111">Dieses Konto wird auf Grundlage der Sachkontoabgrenzungsbuchungen auch für die Rückbuchung der Stundung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c15e-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="3c15e-112">**Gutschrift** - Das Hauptkonto, das Sie definieren, ersetzt das Gutschriftenhauptkonto auf der Erfassungsbelegposition.</span><span class="sxs-lookup"><span data-stu-id="3c15e-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="3c15e-113">Dieses Konto wird auf Grundlage der Sachkontoabgrenzungsbuchungen auch für die Rückbuchung der Stundung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c15e-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="3c15e-114">Nachdem Sie bestimmt haben, welche Konten Sie verwenden, können Sie angeben, wie die Belegnummer erstellt wird, wenn Abgrenzungsbuchungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="3c15e-115">Sie können auch angeben, wie häufig die Buchungen auftreten, die Häufigkeit, mit der die Buchungen erstellt werden, und wann die Buchungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="3c15e-116">Nachdem das Abgrenzungsschema erstellt wurde, können Sie es in einigen der Erfassungen verwenden, indem Sie die Sachkontoabgrenzungsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="3c15e-117">Sachkontoabgrenzungen</span><span class="sxs-lookup"><span data-stu-id="3c15e-117">Ledger accruals</span></span>
<span data-ttu-id="3c15e-118">Wenn Sie eine Erfassung eingeben, können Sie im Menü **Funktionen** auf **Sachkontenabgrenzungen** klicken.</span><span class="sxs-lookup"><span data-stu-id="3c15e-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="3c15e-119">Wenn Sie anschließend das Abgrenzungsschema auswählen, wird der Grundbetrag aus der Erfassung angezeigt, die so über die Periode verteilt wird, wie es das Abgrenzungsschema bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3c15e-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="3c15e-120">Wenn Sie beispielsweise die Versicherung eines Mitarbeiters für das gesamte Jahr im Januar begleichen und der Betrag ist 12.000, müssen Sie diese Ausgaben jeden Monat realisieren. Sie können das Startdatum auswählen.</span><span class="sxs-lookup"><span data-stu-id="3c15e-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="3c15e-121">Wählen Sie das Startdatum der Vereinbarung aus.</span><span class="sxs-lookup"><span data-stu-id="3c15e-121">You can select the start date.</span></span> <span data-ttu-id="3c15e-122">Sie können auch angeben, ob der antizipierte Betrag auf dem Konto oder dem Gegenkonto basiert ist.</span><span class="sxs-lookup"><span data-stu-id="3c15e-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="3c15e-123">Nachdem Sie Ihre Auswahl treffen, klicken Sie auf **Buchungen**, um alle Buchungen anzuzeigen, die basierend auf das Abgrenzungsschema erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="3c15e-124">Wenn Sie 12.000 in den Versicherungskosten auf ein Jahr verteilen, sehen Sie die Zahl 1.000 für jeden Monat.</span><span class="sxs-lookup"><span data-stu-id="3c15e-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="3c15e-125">Nachdem Sie die Erfassung buchen, können Sie die Buchungen anzeigen, indem Sie die Abfragenseite **Belegbuchunge** verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="3c15e-126">Wenn ein Abgrenzungsschema nicht angewendet werden kann (beispielsweise, wenn eine Auftrags- oder eine Einkaufsrechnung vorhanden ist), können Sie den bereits bezahlten Betrag gutschreiben und den Kostenbetrag belasten.</span><span class="sxs-lookup"><span data-stu-id="3c15e-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="3c15e-127">Sie können dann **Gegenkonto** auswählen, wenn Sie das Abgrenzungsschema anwenden.</span><span class="sxs-lookup"><span data-stu-id="3c15e-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="3c15e-128">Weitere Informationen finden Sie unter [Erstellen von Abgrenzungsschemata](tasks/create-accrual-schemes.md) [Erstellen von Sachkonto-Abgrenzungsbuchungen](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3c15e-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

