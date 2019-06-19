---
title: ESR-Debitorenzahlungen für Importe
description: Unter dem folgenden Thema finden Sie Informationen zum Importieren von Debitorenzahlungen in das ESR-Forrmat.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264584
ms.search.region: Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3215142e214ada75bc1978055f055c269a0791a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565328"
---
# <a name="esr-customer-payments-import"></a><span data-ttu-id="3c9b3-103">ESR-Debitorenzahlungen für Importe</span><span class="sxs-lookup"><span data-stu-id="3c9b3-103">ESR customer payments import</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c9b3-104">Unter dem folgenden Thema finden Sie Informationen zum Importieren von Debitorenzahlungen in das ESR-Forrmat.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-104">This topic provides information about importing customer payments in the ESR format.</span></span>

<span data-ttu-id="3c9b3-105">ESR ist ein elektronischer Schuldner-Service, der Zahlungsbelege verwendet, um Geld einzuziehen.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-105">ESR is an electronic debtor service that uses payment slips to collect money.</span></span> <span data-ttu-id="3c9b3-106">Hierbei handelt es sich um das Standardsystem der elektronische Zahlungsmethode, das von den schweizerischen Post erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-106">It is the standard electronic payment system created by the Swiss Post.</span></span> <span data-ttu-id="3c9b3-107">Sie können im ESR-Format Debitorenzahlungsdateien erhalten, das Buchungen und Bankgebühren enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-107">You can receive customer payment files in the ESR format, which can include transactions and bank fees.</span></span> <span data-ttu-id="3c9b3-108">Diese Funktionalität ist für importierte Debitorentransaktionen auf Grundlage von Zahlungsreferenzen vorgesehen, die ursprünglich in Microsoft Dynamics 365 for Finance and Operations generiert und auf den Zahlungsbeleg gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-108">This functionality is intended for imported customer transactions based on payment references that were originally generated in Microsoft Dynamics 365 for Finance and Operations and printed on the payment slip.</span></span>

## <a name="generate-payment-references"></a><span data-ttu-id="3c9b3-109">Zahlungsreferenzen generieren</span><span class="sxs-lookup"><span data-stu-id="3c9b3-109">Generate payment references</span></span>
<span data-ttu-id="3c9b3-110">Zahlungsreferenzen sollten auf den Zahlungsbeleg gedruckt werden, nachdem sie gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-110">Payment references should be printed on the payment slip after posting.</span></span> <span data-ttu-id="3c9b3-111">Sie können auch die Zahlungsreferenzen auf der Seite **Rechnungserfassung** für den ausgewählten Auftrag überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-111">You can also verify payment references on the **Invoice journal** page for the selected sales order.</span></span> <span data-ttu-id="3c9b3-112">Um Zahlungsreferenzen zu generieren, müssen die folgenden Einstellungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-112">To generate payment references, the following settings must be specified.</span></span>

1.  <span data-ttu-id="3c9b3-113">Legen Sie die Bankkontoeinstellungen auf **ESR**, **BESR-ID** und **Bankleitzahl** fest.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-113">Set the bank account settings to **ESR**, **BESR ID,** and **Routing number**.</span></span>
2.  <span data-ttu-id="3c9b3-114">Legt das Feld **Anzahl von Zeichen für Girokonto** auf der Seite **Debitorenparameter** auf der Registerkarte **Sachkonto und Mehrwertsteuer** fest. Dies definiert, wie viele Symbole vom Debitorenkonto in der Zahlungsreferenz einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-114">Set the **Number of characters for Giro account** field on the **Account Receivables parameters** page on the **Ledger and sales tax** tab. This defines how many symbols from the customer account should be included in the payment reference.</span></span>
3.  <span data-ttu-id="3c9b3-115">Der Verkaufsrechnungsnummernkreis soll im richtigen Format (es sollte Symbole nicht anders als Ziffern haben und dieses sollen keine führende Null aufweisen) sein.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-115">The sales invoice number sequence should be in the correct format (it should not have symbols other than digits and it should not contain leading zeros).</span></span>
4.  <span data-ttu-id="3c9b3-116">Das Format **Orange** muss für das Debitorenkonto im Feld **Auf einer Debitorenrechnung** auf der **Rechnung und Lieferung** Registerkarte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-116">The **Orange** format should be specified for the customer account in the **On a customer invoice** field on the **Invoice and delivery** tab.</span></span>

<span data-ttu-id="3c9b3-117">Weitere Informationen finden Sie unter [Zahlungsbericht (Giro)](emea-eur-payment-slip-report-giro.md).</span><span class="sxs-lookup"><span data-stu-id="3c9b3-117">For more information, see [Payment slip report (Giro)](emea-eur-payment-slip-report-giro.md).</span></span>

## <a name="import-a-payment-file"></a><span data-ttu-id="3c9b3-118">Zahlungsdatei importieren</span><span class="sxs-lookup"><span data-stu-id="3c9b3-118">Import a payment file</span></span>
1. <span data-ttu-id="3c9b3-119">Gehen Sie zur Seite **Zahlungsjournal**</span><span class="sxs-lookup"><span data-stu-id="3c9b3-119">Go to the **Payment journal** page</span></span>
2. <span data-ttu-id="3c9b3-120">Klicken Sie auf **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-120">Click **Lines**.</span></span>
3. <span data-ttu-id="3c9b3-121">Klicken Sie auf **Funktionen** &gt; **Zahlungen importieren**.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-121">Click **Functions** &gt; **Import payments**.</span></span>
4. <span data-ttu-id="3c9b3-122">Wählen Sie im Dialogfeld die Zahlungsmethode, und suchen Sie dann den Speicherort der Datei, die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-122">In the dialog box, select the method of payment, and then browse to the location of the file to import.</span></span> 
   > [!NOTE]
   >  <span data-ttu-id="3c9b3-123">Bevor Sie diesen Schritt ausführen können, müssen Sie die **ESR (CH)** Konfigurationen aus dem Lifecycle Services (LCS) bereits importiert haben und die ESR-Zahlungsmethode einrichten.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-123">Before you can complete this step, you must have already imported the **ESR (CH)** configurations from Lifecycle Services (LCS) and set up the ESR method of payment.</span></span> <span data-ttu-id="3c9b3-124">Weitere Informationen finden Sie unter [Dateiformate für Zahlungen](emea-select-file-formats-for-the-method-of-payments.md).</span><span class="sxs-lookup"><span data-stu-id="3c9b3-124">For more information, see [File formats for method of payments](emea-select-file-formats-for-the-method-of-payments.md).</span></span>

<span data-ttu-id="3c9b3-125">Nachdem Sie die Zahlungsdatei importieren haben, werden die Zahlungserfassungspositionen für den Ausgleich mit Debitorenrechnungen anhand der Zahlungsreferenz erstellt und markiert.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-125">After you import the payment file, payment journal lines are created and marked for settlement with customer invoices based on the payment reference.</span></span> <span data-ttu-id="3c9b3-126">Wenn es Gebühren gibt, die für das Bankkonto angegeben werden, die in der Datei angezeigt werden, wie Buchungen zwischen dem Hauptkonto und dem Gebührenkonto, sind diese Gebühren der Erfassung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3c9b3-126">If there are any fees specified for the bank account that are represented in the file, such as transactions between the main account and fee account, these fees will be added to the journal.</span></span>



