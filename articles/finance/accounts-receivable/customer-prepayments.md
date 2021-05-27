---
title: Debitorenvorauszahlungen
description: In diesem Thema wird erläutert, wie Sie Debitorenvorauszahlungen (auch Debitoreneinzahlungen genannt) einrichten und verarbeiten.
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019419"
---
# <a name="customer-prepayments"></a><span data-ttu-id="4ffdb-103">Debitorenvorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="4ffdb-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ffdb-104">Debitorenvorauszahlungen werden verwendet, wenn Sie eine Zahlung von einem Kunden erhalten, es jedoch noch keine Rechnung gibt, gegen die die Zahlung abgerechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="4ffdb-105">Solche Zahlungen werden auch als Debitoreneinzahlungen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="4ffdb-106">Das Einrichten und Arbeiten mit Kundenvorauszahlungen besteht aus den folgenden grundlegenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="4ffdb-107">Erstellen Sie ein Debitorenbuchungsprofil für Vorauszahlungen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="4ffdb-108">Stellen Sie den Parameter **Buchungsprofil mit Erfassungsbeleg für Vorauszahlung** ein,</span><span class="sxs-lookup"><span data-stu-id="4ffdb-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="4ffdb-109">Erstellen Sie eine Zahlungserfassung und wählen Sie für jede Position das Kontrollkästchen **Erfassungsbeleg für Vorauszahlung** aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="4ffdb-110">Dient zum Buchen der Debitorenzahlungserfassung.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="4ffdb-111">Nachdem eine Rechnung erstellt wurde, gleichen Sie sie auf der Seite **Offene Buchungen ausgleichen** mit der Vorauszahlung aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="4ffdb-112">Ein Debitorenbuchungsprofil für Vorauszahlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="4ffdb-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="4ffdb-113">Wenn Sie Vorauszahlungen oder Einzahlungen von Ihren Debitoren annehmen, bevor Waren oder Dienstleistungen geliefert werden oder bevor eine Rechnung in Ihrem System vorhanden ist, müssen Sie den Zahlungseingang in der Regel als Verbindlichkeit und nicht als Aktivposten in Ihrem Kontenplan erfassen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="4ffdb-114">Die Anforderungen für die Erfassung dieser Beträge in Ihrem Hauptbuch können jedoch je nach Land oder Region unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="4ffdb-115">Fragen Sie daher unbedingt Ihre Buchhalter nach den jeweils geltenden Vorschriften.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="4ffdb-116">Grundsätzlich ist der Prozess zum Erstellen eines Buchungsprofils, das für Vorauszahlungen verwendet werden kann, der gleiche wie zum Erstellen anderer Buchungsprofile.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="4ffdb-117">Der Hauptunterschied ist das Hauptkonto, das Sie im Feld **Sammelkonto** auswählen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="4ffdb-118">Weitere Informationen finden Sie unter [Debitorenbuchungsprofile](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="4ffdb-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="4ffdb-119">Parameter für Debitorenvorauszahlungen festlegen</span><span class="sxs-lookup"><span data-stu-id="4ffdb-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="4ffdb-120">Es gibt zwei Hauptparameter für Debitorenkonten, die Sie berücksichtigen müssen, wenn Sie das System für Debitorenvorauszahlungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="4ffdb-121">Gehen Sie folgendermaßen vor, um die Parameter zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="4ffdb-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="4ffdb-122">Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="4ffdb-123">Optional: Wählen Sie auf der Registerkarte **Hauptbuch und Mehrwertsteuer** das Inforegister **Zahlung** aus und legen Sie die Option **Mehrwertsteuer auf Vorauszahlung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="4ffdb-124">Wählen Sie im Feld **Buchungsprofil mit Erfassungsbeleg für Vorauszahlung** das Debitorenuchungsprofil aus, das verwendet werden soll, wenn Debitorenvorauszahlungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="4ffdb-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="4ffdb-126">Erfassungen für Debitorenvorauszahlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="4ffdb-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="4ffdb-127">Wenn Sie die Debitorenzahlungserfassung erstellen, müssen Sie für jede Vorauszahlung die Option **Erfassungsbeleg für Vorauszahlung** auf der Seite **Kundenzahlungserfassung** auf **Ja** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="4ffdb-128">Gehen Sie folgendermaßen vor, um eine Debitorenvorauszahlung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="4ffdb-129">Gehen Sie zu **Debitorenkonten \> Zahlungen \> Kundenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="4ffdb-130">Wählen Sie **Neu** aus, um eine Erfassung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="4ffdb-131">Wählen Sie im Feld **Name** den Namen der Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4ffdb-132">Wenn Sie im vorherigen Verfahren die Option **Mehrwertsteuer auf Vorauszahlung** auf **Ja** festlegen, müssen Sie einen Erfassungsnamen auswählen, in dem der Parameter **Betrag enthält Mehrwertsteuer** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="4ffdb-133">Optional: Sie können im Feld **Beschreibung** eine detaillierte Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="4ffdb-134">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-134">Select **Lines**.</span></span>
6. <span data-ttu-id="4ffdb-135">Wenn keine leere Position vorhanden ist, wählen Sie **Neu**, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="4ffdb-136">Geben Sie im Feld **Datum** das Datum ein, an dem die Vorauszahlung gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="4ffdb-137">Wählen Sie im Feld **Konto** den Debitor für die Vorauszahlung aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="4ffdb-138">Optional: Sie können im Feld **Beschreibung** eine detaillierte Beschreibung der Buchung eingeben.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="4ffdb-139">Geben Sie im Feld **Gutschrift** den Betrag der Vorauszahlung ein.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="4ffdb-140">Wählen Sie im Feld **Gegenkonto** das Konto aus, auf das die Zahlung gegengebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="4ffdb-141">Wählen Sie beispielsweise die Bank oder das Hauptkonto aus, auf die/das die Zahlung gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="4ffdb-142">Wählen Sie im Feld **Zahlungsmethode** eine die Zahlungsmethode des Debitors aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="4ffdb-143">Legen Sie die Registerkarte **Zahlung** die Option **Erfassungsbeleg für Vorauszahlung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="4ffdb-144">Wiederholen Sie die Schritte 7 bis 13 für jede weitere Vorauszahlung, die gebucht werden muss.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="4ffdb-145">Wählen Sie **Buchen** aus, um die Erfassung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="4ffdb-146">Vorauszahlungen mit Rechnungen ausgleichen</span><span class="sxs-lookup"><span data-stu-id="4ffdb-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="4ffdb-147">Sie können den Arbeitsbereich **Debitorenzahlungen** benutzen, um Zahlungen, die noch nicht vollständig ausgeglichen wurden, einfach zu finden und auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="4ffdb-148">Wählen Sie im Dashboard **Home** die Kachel **Debitorenzahlungen** aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="4ffdb-149">Suchen Sie im Abschnitt **Debitorenbuchen** auf der Registerkarte **Nicht ausgeglichene Zahlungen** nach der auszugleichenden Zahlung und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="4ffdb-150">Wählen Sie **Buchungen ausgleichen**.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="4ffdb-151">Aktivieren Sie für die Rechnung und die auszugleichende Zahlung das Kontrollkästchen **Markieren**.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="4ffdb-152">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="4ffdb-152">Select **Post**.</span></span>

<span data-ttu-id="4ffdb-153">Weitere Informationen zum Ausgleichen offener Buchungen finden Sie unter [Übersicht über Ausgleiche](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4ffdb-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
