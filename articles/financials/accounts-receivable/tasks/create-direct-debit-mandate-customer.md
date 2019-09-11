---
title: Direkteinzugsmandat für einen Debitor erstellen
description: Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916368"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="06e31-103">Direkteinzugsmandat für einen Debitor erstellen</span><span class="sxs-lookup"><span data-stu-id="06e31-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06e31-104">Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06e31-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="06e31-105">Bankkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="06e31-105">Create a bank account</span></span>
1. <span data-ttu-id="06e31-106">Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Debitoren > Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="06e31-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="06e31-107">Wählen Sie in der Liste einen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-107">In the list, select a record.</span></span> <span data-ttu-id="06e31-108">Wählen Sie z. B. "US-001" aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-108">For example, select US-001</span></span>
3. <span data-ttu-id="06e31-109">Klicken Sie im Aktivitätsbereich **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="06e31-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="06e31-110">Klicken Sie auf **Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="06e31-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="06e31-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="06e31-111">Click **New**.</span></span>
6. <span data-ttu-id="06e31-112">Geben Sie im Feld **Bankkonto** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="06e31-113">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="06e31-114">Geben Sie im Feld **IBAN** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="06e31-115">Geben Sie im Feld **Währung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="06e31-116">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="06e31-116">Click **Save**.</span></span>
11. <span data-ttu-id="06e31-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="06e31-117">Close the page.</span></span>
12. <span data-ttu-id="06e31-118">Gehen Sie im **Navigationsbereich** zu **Module > Bargeld- und Bankverwaltung > Bankkonten > Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="06e31-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="06e31-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="06e31-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="06e31-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="06e31-121">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="06e31-121">Click **Edit**.</span></span>
16. <span data-ttu-id="06e31-122">Erweitern Sie das Inforegister **Zusätzliche Kennung**.</span><span class="sxs-lookup"><span data-stu-id="06e31-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="06e31-123">Geben Sie im Feld **Bankeinzugskennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="06e31-124">Geben Sie im Feld **IBAN** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="06e31-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="06e31-125">Close the page.</span></span>
20. <span data-ttu-id="06e31-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="06e31-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="06e31-127">Elektronische Zahlungsmethode definieren</span><span class="sxs-lookup"><span data-stu-id="06e31-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="06e31-128">Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Zahlungseinstellungen > Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="06e31-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="06e31-129">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="06e31-129">Click **New**.</span></span>
3. <span data-ttu-id="06e31-130">Geben Sie im Feld **Zahlungsmethode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="06e31-131">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="06e31-132">Geben Sie im Feld **Zahlungstyp** 'Elektronischer Zahlungsverkehr' ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="06e31-133">Der Zahlungstyp für eine Einzugsermächtigungs-Zahlungsmethode muss "Elektronische Zahlung" sein.</span><span class="sxs-lookup"><span data-stu-id="06e31-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="06e31-134">Wählen Sie „Ja“ im Feld **Mandat anfordern** aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="06e31-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="06e31-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="06e31-136">Direkteinzugsmandat einem Debitor hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="06e31-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="06e31-137">Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Debitoren > Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="06e31-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="06e31-138">Wählen Sie in der Liste einen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-138">In the list, select a record.</span></span> <span data-ttu-id="06e31-139">Wählen Sie z. B. "US-001" aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-139">For example, select US-001</span></span>
3. <span data-ttu-id="06e31-140">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="06e31-140">Click **Edit**.</span></span>
4. <span data-ttu-id="06e31-141">Erweitern Sie das Inforegister **Zahlungsausfälle**.</span><span class="sxs-lookup"><span data-stu-id="06e31-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="06e31-142">Geben Sie im Feld **Zahlungsmethode** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="06e31-143">Erweitern Sie das Inforegister **Zahlungsausfälle**.</span><span class="sxs-lookup"><span data-stu-id="06e31-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="06e31-144">Erweitern Sie das Inforegister **Einzugsermächtigungen**.</span><span class="sxs-lookup"><span data-stu-id="06e31-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="06e31-145">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="06e31-145">Click **Add**.</span></span>
9. <span data-ttu-id="06e31-146">Geben Sie im Feld **Bankkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="06e31-147">Geben Sie im Feld **Kreditorenbankkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="06e31-148">Geben Sie im Feld **Zahlungshäufigkeit** die Anzahl der Zahlungen ein, deren Verarbeitung Sie für diese Vollmacht erwarten.</span><span class="sxs-lookup"><span data-stu-id="06e31-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="06e31-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="06e31-149">Click **OK**.</span></span>
13. <span data-ttu-id="06e31-150">Klicken Sie auf **Drucken**.</span><span class="sxs-lookup"><span data-stu-id="06e31-150">Click **Print**.</span></span>
14. <span data-ttu-id="06e31-151">Klicken Sie auf **Vollmachtsbericht**.</span><span class="sxs-lookup"><span data-stu-id="06e31-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="06e31-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="06e31-152">Close the page.</span></span>
16. <span data-ttu-id="06e31-153">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="06e31-153">Click **Edit**.</span></span>
17. <span data-ttu-id="06e31-154">Geben Sie im Feld **Unterschriftsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="06e31-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="06e31-155">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="06e31-155">Click **Yes**.</span></span>
19. <span data-ttu-id="06e31-156">Geben Sie den Ort ein, an dem die Vollmacht unterzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="06e31-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="06e31-157">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="06e31-157">Click **OK**.</span></span>
21. <span data-ttu-id="06e31-158">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="06e31-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="06e31-159">Freitextrechnung mit Vollmacht erstellen</span><span class="sxs-lookup"><span data-stu-id="06e31-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="06e31-160">Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Rechnungen > Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="06e31-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="06e31-161">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="06e31-161">Click **New**.</span></span>
3. <span data-ttu-id="06e31-162">Wählen Sie den Debitor aus, dem Sie die Vollmacht hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="06e31-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="06e31-163">Geben Sie im Feld **Direkteinzugsmandats-ID** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="06e31-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

