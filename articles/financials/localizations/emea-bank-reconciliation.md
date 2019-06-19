---
title: Bankauszug und Zahlungsabstimmung für die EU
description: Dieses Thema bietet einen Überblick der Funktionen, die Sie verwenden können, um Zahlungsinformationen von den Banken in Formate abzustimmen, die von den europäischer Länder verwendet werden.
author: neserovleo
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 40742ff82e916b64e68662f79899baf2549b1f2c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565338"
---
# <a name="bank-statement-and-payment-reconciliation-for-the-eu"></a><span data-ttu-id="3aed2-103">Bankauszug und Zahlungsabstimmung für die EU</span><span class="sxs-lookup"><span data-stu-id="3aed2-103">Bank statement and payment reconciliation for the EU</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3aed2-104">Dieses Thema bietet einen Überblick der Funktionen, die Sie verwenden können, um Zahlungsinformationen von den Banken in Formate abzustimmen, die von den europäischer Länder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aed2-104">This topic provides an overview of the functionality that you can use to reconcile payment information from banks in formats that are used by European countries.</span></span>

<span data-ttu-id="3aed2-105">In Microsoft Dynamics 365 for Finance and Operations können Sie Transaktionen von Banken importieren und diese Transaktionen mit bestehenden Transaktionen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="3aed2-105">In Microsoft Dynamics 365 for Finance and Operations, you can import transactions from banks and settle these transactions against existing transactions.</span></span> <span data-ttu-id="3aed2-106">In Europa können Sie dies für die folgenden Szenarien tun:</span><span class="sxs-lookup"><span data-stu-id="3aed2-106">In Europe, you can do this for the following scenarios:</span></span>

-   <span data-ttu-id="3aed2-107">Importieren von Bankauszügen</span><span class="sxs-lookup"><span data-stu-id="3aed2-107">Importing bank statements</span></span>
-   <span data-ttu-id="3aed2-108">Importieren von Zahlungen</span><span class="sxs-lookup"><span data-stu-id="3aed2-108">Importing payments</span></span>
-   <span data-ttu-id="3aed2-109">Importieren von Rückgabedateien</span><span class="sxs-lookup"><span data-stu-id="3aed2-109">Importing return files</span></span>

## <a name="bank-statements"></a><span data-ttu-id="3aed2-110">Bankauszüge</span><span class="sxs-lookup"><span data-stu-id="3aed2-110">Bank statements</span></span>
<span data-ttu-id="3aed2-111">Ein *Bankauszug* oder ein *Kontoauszug* ist eine Zusammenfassung von wertmäßigen Buchungen, die über eine bestimmte Zeitperiode auf einem Konto erfolgt sind, das aus einem Unternehmen mit dem Finanzinstitut stattfindet.</span><span class="sxs-lookup"><span data-stu-id="3aed2-111">A *bank statement* or *account statement* is a summary of financial transactions that have occurred over a given period on a bank account held by a company with a financial institution.</span></span> <span data-ttu-id="3aed2-112">In Finance and Operations können Sie einen Bankauszug importieren.</span><span class="sxs-lookup"><span data-stu-id="3aed2-112">In Finance and Operations you can import a bank statement.</span></span> <span data-ttu-id="3aed2-113">Es ist wichtig, importierte Buchungen mit vorhandenen Buchungen auszugleichen sowie den Anfangs- und den Endsaldo der Bankkonten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3aed2-113">It is important to settle imported transactions with existing transactions as well as verify the opening and ending balance of the bank accounts.</span></span> <span data-ttu-id="3aed2-114">Die folgende Liste umfasst die unterstützten europäischen Formate.</span><span class="sxs-lookup"><span data-stu-id="3aed2-114">The following list includes the supported European formats.</span></span>

-   <span data-ttu-id="3aed2-115">Erweiterte Banabstimmungen für europäische Dateiformate.</span><span class="sxs-lookup"><span data-stu-id="3aed2-115">Advanced bank reconciliation European file formats.</span></span> <span data-ttu-id="3aed2-116">Weitere Informationen finden Sie unter [Bankabstimmungsüberblick](../cash-bank-management/advanced-bank-reconciliation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3aed2-116">For more information, see [Advanced bank reconciliation overview](../cash-bank-management/advanced-bank-reconciliation-overview.md).</span></span>
-   <span data-ttu-id="3aed2-117">Bankauszugsnachrichten-Dateiformat ISO 20022 camt.053.</span><span class="sxs-lookup"><span data-stu-id="3aed2-117">ISO 20022 camt.053 bank statement message file format.</span></span>
-   <span data-ttu-id="3aed2-118">CODA Bankauszugs-Dateiformat</span><span class="sxs-lookup"><span data-stu-id="3aed2-118">CODA bank statement file format.</span></span> <span data-ttu-id="3aed2-119">Weitere Informationen finden Sie unter [CODA Bankauszug](emea-bel-coda-bank-statement-import.md).</span><span class="sxs-lookup"><span data-stu-id="3aed2-119">For more information, see [CODA bank statement](emea-bel-coda-bank-statement-import.md).</span></span>

## <a name="customer-and-vendor-payments-import-and-return-messages"></a><span data-ttu-id="3aed2-120">Debitoren- und Kreditorenzahlungen Import und Rücklieferungsnachrichten</span><span class="sxs-lookup"><span data-stu-id="3aed2-120">Customer and vendor payments import and return messages</span></span>
<span data-ttu-id="3aed2-121">Neben einem Bankauszug können Banken bestimmte Meldungen bereitstellen, die Informationen zu Debitoren und Kreditorenzahlungen enthalten, die in Finance and Operations importiert werden und mit Debitoren- und Kreditorenrechnungsbuchungen abgestimmt werden können.</span><span class="sxs-lookup"><span data-stu-id="3aed2-121">In addition to a bank statement, banks can provide specific messages, containing information about customer and vendor payments, which can be imported into Finance and Operations and reconciled with customer and vendor transactions.</span></span> <span data-ttu-id="3aed2-122">Wenn ein Unternehmen Informationen über eingehende Debitorenzahlungsbuchungen von der Bank erhalten muss, können Importformate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3aed2-122">When a company needs to receive information about incoming customer payments transactions from the bank, the import formats can be used.</span></span> <span data-ttu-id="3aed2-123">Bei Unternehmen, die direkte Banküberweisung verwenden, können die Rückgabemeldungen empfangen werden, um den Status ausstehender Zahlungen zu aktualisieren, die zuvor exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3aed2-123">For companies that use direct debit and credit transfer, the return messages can be received to update the status of payments that were previously exported.</span></span> <span data-ttu-id="3aed2-124">Die Differenz zwischen Importformaten und Rücklieferungsformaten ist, dass Rücklieferungen meistens dazu dienen, bereits erstellte Zahlungserfassungspositionen zu aktualisieren (Sie können erstellt werden, wenn direkte Überweisungen ausgeführt wurden), anstatt neue Positionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3aed2-124">The difference between import formats and return formats is that returns are targeted mostly to update already created payment journal lines (they can be created when direct debit or credit transfer were initiated) instead of creating new lines.</span></span> <span data-ttu-id="3aed2-125">Einige komplexe Importformate können auch Rückholszenarien enthalten.</span><span class="sxs-lookup"><span data-stu-id="3aed2-125">Some complex import formats can also include return scenarios.</span></span> <span data-ttu-id="3aed2-126">Das folgende Beispiel veranschaulicht, wie diese Teilung implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3aed2-126">The following example shows how this division should be implemented.</span></span>

### <a name="import-formats"></a><span data-ttu-id="3aed2-127">Importformat</span><span class="sxs-lookup"><span data-stu-id="3aed2-127">Import formats</span></span>

-   <span data-ttu-id="3aed2-128">Bankbenachrichtigungsmitteilung ISO 20022 [camt.054](emea-ISO20022-file-formats.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-128">ISO 20022 [camt.054](emea-ISO20022-file-formats.md) bank notification message</span></span>
-   <span data-ttu-id="3aed2-129">[Netzwerkimportformat ](emea-nor-nets-import-format.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-129">[Nets import format](emea-nor-nets-import-format.md) - Complex feature for Norwegian payment formats</span></span>
-   <span data-ttu-id="3aed2-130">Importieren von [ESR](emea-che-esr-customer-payments-import.md)-Kundenzahlungen</span><span class="sxs-lookup"><span data-stu-id="3aed2-130">[ESR](emea-che-esr-customer-payments-import.md) customer payments import</span></span>
-   <span data-ttu-id="3aed2-131">Importieren Sie Zahlungsformate für Schweden - BankGirot-Maximum und BankGirot OCR-Formate</span><span class="sxs-lookup"><span data-stu-id="3aed2-131">Import payment formats for Sweden - BankGirot Max and BankGirot OCR formats</span></span>

### <a name="return-formats"></a><span data-ttu-id="3aed2-132">Rückgabeformat</span><span class="sxs-lookup"><span data-stu-id="3aed2-132">Return formats</span></span>

-   <span data-ttu-id="3aed2-133">Zahlungsstatusbericht ISO 20022 [pain.002](emea-ISO20022-file-formats.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-133">ISO 20022 [pain.002](emea-ISO20022-file-formats.md) payment status report</span></span>
-   <span data-ttu-id="3aed2-134">(DNK) BetalingsserviceBasis-returformat – Rückgabeformat für Kunden Betalingsservice-Exportformat</span><span class="sxs-lookup"><span data-stu-id="3aed2-134">(DNK) BetalingsserviceBasis-returformat – Return format for customer Betalingsservice export format</span></span>
-   <span data-ttu-id="3aed2-135">[Importzahlungsformate für Schweden](emea-swe-payment-formats-import.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-135">[Import payment formats for Sweden](emea-swe-payment-formats-import.md) - Bankgirot Autogiro returns</span></span>
-   <span data-ttu-id="3aed2-136">(SWE) BankGirot-Rücklieferung – Kreditorenzahlungen geben das Format zurück, das dem Bankgirot-Exportformat entspricht</span><span class="sxs-lookup"><span data-stu-id="3aed2-136">(SWE) BankGirot return – Vendor payments return format, which corresponds to Bankgirot export format</span></span>


