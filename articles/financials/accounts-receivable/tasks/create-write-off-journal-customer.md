---
title: Eine Abschreibungserfassung für einen Debitor erstellen
description: In diesem Aufgabenhandbuch wird dargestellt, wie Sie die Parameter für Abschreibungen einrichten und dann Abschreibungstransaktionen auf der Seite "Inkassi", der Seite "Offene Debitorenrechnungen" und auf der Seite "Debitoren" abschreiben.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cd576458bab1e4654d21773b581a5b0f726c928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545514"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="9f7c4-103">Eine Abschreibungserfassung für einen Debitor erstellen</span><span class="sxs-lookup"><span data-stu-id="9f7c4-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f7c4-104">In diesem Aufgabenhandbuch wird dargestellt, wie Sie die Parameter für Abschreibungen einrichten und dann Abschreibungstransaktionen auf der Seite "Inkassi", der Seite "Offene Debitorenrechnungen" und auf der Seite "Debitoren" abschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="9f7c4-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="9f7c4-106">Abschreibungsparameter einrichten</span><span class="sxs-lookup"><span data-stu-id="9f7c4-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="9f7c4-107">Wechseln Sie zu "Kredit und Inkasso" > "Einrichten" > "Debitorenkontenparameter".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="9f7c4-108">Klicken Sie auf die Registerkarte "Inkassi".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="9f7c4-109">Erweitern oder reduzieren Sie den Abschnitt "Abschreiben".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="9f7c4-110">Die Abschreibungserfassung ist die allgemeine Erfassung, die die Abschreibungstransaktionen einer Buchung enthält, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="9f7c4-111">Sie können einen Ursachencode zu jeder Abschreibung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="9f7c4-112">Sie können diesen Standardwert in der Erfassung zum Zeitpunkt der Abschreibung übergehen.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="9f7c4-113">Legen Sie dies auf "Ja" fest, wenn die Mehrwertsteuer aus der ursprünglichen Transaktion in der Abschreibung trennen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="9f7c4-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-114">Close the page.</span></span>
5. <span data-ttu-id="9f7c4-115">Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Debitorenbuchungsprofile".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="9f7c4-116">Das Abschreibungskonto wird als die Ausgabenkonto- oder Rücklageregulierung in der allgemeinen Erfassung verwendet</span><span class="sxs-lookup"><span data-stu-id="9f7c4-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="9f7c4-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="9f7c4-118">Debitorensaldo auf der Seite "Saldenrückblick" abschreiben</span><span class="sxs-lookup"><span data-stu-id="9f7c4-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="9f7c4-119">Wechseln Sie zu "Kredit und Inkasso" > "Inkassi" > "Saldenrückblick".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="9f7c4-120">Markieren Sie die Zeile für den Debitor, den Sie abschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="9f7c4-121">Markieren Sie z. B. die Position mit Birch Company.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="9f7c4-122">Klicken Sie im Aktivitätsbereich auf "Sammeln".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="9f7c4-123">Klicken Sie auf "Abschreiben".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-123">Click Write off.</span></span>
5. <span data-ttu-id="9f7c4-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-124">Click OK.</span></span>
6. <span data-ttu-id="9f7c4-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-125">Close the page.</span></span>
7. <span data-ttu-id="9f7c4-126">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="9f7c4-127">Wählen Sie die Nummer der Stapelverarbeitungserfassung für die Erfassung aus, die die Abschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="9f7c4-128">Eine Position wird erstellt, um den Debitorensaldo umzukehren.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="9f7c4-129">Eine oder mehrere Positionen werden erstellt, um die Abschreibung auf dem Abschreibungskonto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="9f7c4-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-130">Close the page.</span></span>
10. <span data-ttu-id="9f7c4-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="9f7c4-132">Transaktionen aus dem Inkassoformular abschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="9f7c4-133">Wechseln Sie zu "Kredit und Inkasso" > "Inkassi" > "Saldenrückblick".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="9f7c4-134">Wählen Sie den Namen des Debitors aus, der die Transaktionen beinhaltet, die Sie abschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="9f7c4-135">Wählen Sie beispielsweise Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="9f7c4-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="9f7c4-136">Zeile für erste Transaktion markieren.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="9f7c4-137">Zeile für zweite Transaktion markieren.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="9f7c4-138">Klicken Sie auf "Abschreiben".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-138">Click Write off.</span></span>
6. <span data-ttu-id="9f7c4-139">Geben Sie im Feld "Kommentar zur Ursache" "uneinbringliche Außenstände" ein.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="9f7c4-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-140">Click OK.</span></span>
8. <span data-ttu-id="9f7c4-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-141">Close the page.</span></span>
9. <span data-ttu-id="9f7c4-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-142">Close the page.</span></span>
10. <span data-ttu-id="9f7c4-143">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="9f7c4-144">Wählen Sie die Nummer der Stapelverarbeitungserfassung für die Erfassung aus, die die Abschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="9f7c4-145">Eine Position wird erstellt, um den Debitorensaldo umzukehren.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="9f7c4-146">Eine oder mehrere Positionen werden erstellt, um die Abschreibung auf dem Abschreibungskonto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="9f7c4-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-147">Close the page.</span></span>
13. <span data-ttu-id="9f7c4-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="9f7c4-149">Rechnung auf der Seite der offenen Debitorenrechnungsseite abschreiben</span><span class="sxs-lookup"><span data-stu-id="9f7c4-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="9f7c4-150">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Offene Debitorenrechnungen".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="9f7c4-151">Markieren Sie die Position für eine Rechnung.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-151">Mark the line for an invoice.</span></span> <span data-ttu-id="9f7c4-152">Markieren Sie z. B. die Position für CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="9f7c4-153">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="9f7c4-154">Klicken Sie auf "Abschreiben".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-154">Click Write off.</span></span>
5. <span data-ttu-id="9f7c4-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-155">Click OK.</span></span>
6. <span data-ttu-id="9f7c4-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="9f7c4-157">Saldo eines Debitors auf der Seite "Debitoren" abschreiben</span><span class="sxs-lookup"><span data-stu-id="9f7c4-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="9f7c4-158">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9f7c4-159">Dient zum Auswählen eines Debitorenkontos.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-159">Select a customer account.</span></span> <span data-ttu-id="9f7c4-160">Wählen Sie beispielsweise US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="9f7c4-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="9f7c4-161">Klicken Sie im Aktivitätsbereich auf "Sammeln".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="9f7c4-162">Klicken Sie auf "Abschreiben".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-162">Click Write off.</span></span>
5. <span data-ttu-id="9f7c4-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9f7c4-163">Click OK.</span></span>
6. <span data-ttu-id="9f7c4-164">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9f7c4-164">Close the page.</span></span>

