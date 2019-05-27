---
title: Direkteinzugsmandat für einen Debitor erstellen
description: Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572534"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="fbb84-103">Direkteinzugsmandat für einen Debitor erstellen</span><span class="sxs-lookup"><span data-stu-id="fbb84-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbb84-104">Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbb84-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="fbb84-105">Bankkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="fbb84-105">Create a bank account</span></span>
1. <span data-ttu-id="fbb84-106">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="fbb84-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="fbb84-107">Wählen Sie z. B. "US-001" aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-107">For example, select US-001</span></span>
3. <span data-ttu-id="fbb84-108">Klicken Sie im Aktivitätsbereich auf "Debitor".</span><span class="sxs-lookup"><span data-stu-id="fbb84-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="fbb84-109">Klicken Sie auf Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="fbb84-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="fbb84-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fbb84-110">Click New.</span></span>
6. <span data-ttu-id="fbb84-111">Geben Sie im Feld "Bankkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="fbb84-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="fbb84-113">Geben Sie im Feld "IBAN" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="fbb84-114">Geben Sie im Feld "Währung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="fbb84-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fbb84-115">Click Save.</span></span>
11. <span data-ttu-id="fbb84-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbb84-116">Close the page.</span></span>
12. <span data-ttu-id="fbb84-117">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="fbb84-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="fbb84-118">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="fbb84-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="fbb84-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="fbb84-120">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="fbb84-120">Click Edit.</span></span>
16. <span data-ttu-id="fbb84-121">Erweitern Sie den Abschnitt "Zusätzliche Kennung".</span><span class="sxs-lookup"><span data-stu-id="fbb84-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="fbb84-122">Geben Sie im Feld "Bankeinzugskennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="fbb84-123">Geben Sie im Feld "IBAN" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="fbb84-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbb84-124">Close the page.</span></span>
20. <span data-ttu-id="fbb84-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbb84-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="fbb84-126">Elektronische Zahlungsmethode definieren</span><span class="sxs-lookup"><span data-stu-id="fbb84-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="fbb84-127">Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="fbb84-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="fbb84-128">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fbb84-128">Click New.</span></span>
3. <span data-ttu-id="fbb84-129">Geben Sie im Feld "Zahlungsmethode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="fbb84-130">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fbb84-131">Der Zahlungstyp für eine Einzugsermächtigungs-Zahlungsmethode muss "Elektronische Zahlung" sein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="fbb84-132">Wählen Sie "Ja" im Feld "Mandat anfordern" aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="fbb84-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbb84-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="fbb84-134">Direkteinzugsmandat einem Debitor hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fbb84-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="fbb84-135">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="fbb84-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="fbb84-136">Wählen Sie z. B. "US-001" aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-136">For example, select US-001</span></span>
3. <span data-ttu-id="fbb84-137">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="fbb84-137">Click Edit.</span></span>
4. <span data-ttu-id="fbb84-138">Erweitern Sie den Abschnitt "Zahlungsausfälle".</span><span class="sxs-lookup"><span data-stu-id="fbb84-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="fbb84-139">Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="fbb84-140">Erweitern Sie den Abschnitt "Zahlungsausfälle".</span><span class="sxs-lookup"><span data-stu-id="fbb84-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="fbb84-141">Erweitern Sie den Abschnitt "Einzugsermächtigungen".</span><span class="sxs-lookup"><span data-stu-id="fbb84-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="fbb84-142">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fbb84-142">Click Add.</span></span>
9. <span data-ttu-id="fbb84-143">Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="fbb84-144">Geben Sie im Feld 'Kreditorenbankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="fbb84-145">Geben Sie die Anzahl der Zahlungen ein, deren Verarbeitung Sie für diese Vollmacht erwarten.</span><span class="sxs-lookup"><span data-stu-id="fbb84-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="fbb84-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="fbb84-146">Click OK.</span></span>
13. <span data-ttu-id="fbb84-147">Klicken Sie auf Drucken.</span><span class="sxs-lookup"><span data-stu-id="fbb84-147">Click Print.</span></span>
14. <span data-ttu-id="fbb84-148">Klicken Sie auf "Vollmachtsbericht".</span><span class="sxs-lookup"><span data-stu-id="fbb84-148">Click Mandate report.</span></span>
15. <span data-ttu-id="fbb84-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbb84-149">Close the page.</span></span>
16. <span data-ttu-id="fbb84-150">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="fbb84-150">Click Edit.</span></span>
17. <span data-ttu-id="fbb84-151">Geben Sie im Feld "Unterschriftsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="fbb84-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="fbb84-152">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="fbb84-152">Click Yes.</span></span>
19. <span data-ttu-id="fbb84-153">Geben Sie den Ort ein, an dem die Vollmacht unterzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="fbb84-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="fbb84-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="fbb84-154">Click OK.</span></span>
21. <span data-ttu-id="fbb84-155">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbb84-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="fbb84-156">Freitextrechnung mit Vollmacht erstellen</span><span class="sxs-lookup"><span data-stu-id="fbb84-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="fbb84-157">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".</span><span class="sxs-lookup"><span data-stu-id="fbb84-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="fbb84-158">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fbb84-158">Click New.</span></span>
3. <span data-ttu-id="fbb84-159">Wählen Sie den Debitor aus, dem Sie die Vollmacht hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="fbb84-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="fbb84-160">Geben Sie im Feld "Direkteinzugsmandats-ID" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fbb84-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

