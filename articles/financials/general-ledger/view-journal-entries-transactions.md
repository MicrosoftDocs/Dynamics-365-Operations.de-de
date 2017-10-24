---
title: "Erfassungseinträge und Transaktionen anzeigen"
description: "Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fda51a8382cb7d8a9aa7392224486189c442550f
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="view-journal-entries-and-transactions"></a><span data-ttu-id="64ce6-103">Erfassungseinträge und Transaktionen anzeigen</span><span class="sxs-lookup"><span data-stu-id="64ce6-103">View journal entries and transactions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="64ce6-104">Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-104">This article explains the various ways that you can view journal entries and transactions.</span></span> 

<span data-ttu-id="64ce6-105">Benutzer, die Erfassungen und Transaktionen anzeigen möchten, haben mehrere Möglichkeiten für den Datenzugriff.</span><span class="sxs-lookup"><span data-stu-id="64ce6-105">Users who want to view journals and transactions have several ways to access the data.</span></span> <span data-ttu-id="64ce6-106">Sie können Anfragenseiten nutzen, die eine Detallanzeige ermöglichen, oder sie können verschiedene Berichtsoptionen im Hauptbuch verwenden.</span><span class="sxs-lookup"><span data-stu-id="64ce6-106">They can take advantage of inquiry pages that provide drill-down ability, or they can use various report options in the general ledger.</span></span>

## <a name="voucher-transactions"></a><span data-ttu-id="64ce6-107">Belegtransaktionen</span><span class="sxs-lookup"><span data-stu-id="64ce6-107">Voucher transactions</span></span>
<span data-ttu-id="64ce6-108">**Belegtransaktionen** ist eine Anfragenseite, in der Sie aus verschiedenen Tabellen und Feldern auswählen können, um Kriterien für den Saldo oder die Transaktion anzugeben, die Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-108">**Voucher transactions** is an inquiry page where you can select from various tables and fields to specify criteria for the balance or transaction that you're searching for.</span></span> <span data-ttu-id="64ce6-109">So können Sie z. B. alle Transaktionen für ein bestimmtes Datum oder ein Konto oder alle Transaktionen des Typs **Benutzung** anzeigen, die sich auf einer bestimmten Buchungsebene befinden.</span><span class="sxs-lookup"><span data-stu-id="64ce6-109">For example, you can view all transactions for a specific date or account, or all transactions of the **Operating** type that are in a specific posting layer.</span></span> <span data-ttu-id="64ce6-110">Standardmäßig zeigt die Seite die Erfassungsnummer, Beleg, Datum und Hauptkonto an, Sie können jedoch zusätzliche Tabellen, Felder und Kriterien hinzufügen, um die Suche einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-110">By default, the page shows the journal number, voucher, date, and main account, but you can add additional tables, fields, and criteria to narrow down your search.</span></span>

## <a name="audit-trail"></a><span data-ttu-id="64ce6-111">Audit-Trail</span><span class="sxs-lookup"><span data-stu-id="64ce6-111">Audit trail</span></span>
<span data-ttu-id="64ce6-112">**Audit-Trail** ist eine Anfragenseite, die Transaktionsarten, Beschreibungen, Transaktionsersteller und -datum anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64ce6-112">**Audit trail** is an inquiry page that shows the types of transactions, descriptions, who the transactions were created by, and when they were created.</span></span> <span data-ttu-id="64ce6-113">Von der **Audit-Trail**-Anfragenseite können Sie die Belegtransaktionen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-113">From the **Audit trail** inquiry page, you can view the voucher transactions.</span></span>

## <a name="financial-reports"></a><span data-ttu-id="64ce6-114">Finanzberichte</span><span class="sxs-lookup"><span data-stu-id="64ce6-114">Financial reports</span></span>
<span data-ttu-id="64ce6-115">Sie können Hauptbuchtransaktionen auch untersuchen und analysieren, indem Sie Finanzberichte ausführen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-115">You can also explore and analyze general ledger transactions by running financial reports.</span></span> <span data-ttu-id="64ce6-116">Da das Design von Finanzberichten auf Konten, Dimensionen, Kontokategorien oder einer Kombination dieser drei basieren kann, können Sie die Transaktionen anzeigen, indem Sie auf verschiedene Weise Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-116">Because the design of financial reports can be based on accounts, dimensions, account categories, or a combination of the three, you can view the transactions by drilling down in various ways.</span></span> <span data-ttu-id="64ce6-117">Wenn Sie weitere Informationen zu Hauptbuchtransaktionen erfordern, können Sie auch mehrere Transaktionseigenschaften als Teil des Berichtsdesigns einschließen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-117">If you require more information for general ledger transactions, you can also include multiple transaction properties as part of the report design.</span></span> <span data-ttu-id="64ce6-118">Wenn Sie darüber hinaus die Transaktionen anzeigen möchten, aus denen sich ein Hauptbuchsaldo zusammensetzt, können Sie Details für die Kontotransaktionen anzeigen,genau wie aus der **Zwischenbilanz**-Listenseite.</span><span class="sxs-lookup"><span data-stu-id="64ce6-118">Additionally, if you want to see the transactions that make up a general ledger balance, you can drill down to account transactions, just as you can from the **Trial balance** list page.</span></span>

## <a name="ledger-reports"></a><span data-ttu-id="64ce6-119">Sachkonto – Berichte</span><span class="sxs-lookup"><span data-stu-id="64ce6-119">Ledger reports</span></span>
<span data-ttu-id="64ce6-120">Neben den Finanzberichten können Sie die folgenden Sachkontoberichte verwenden, um Hauptbuchtransaktionen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="64ce6-120">In addition to the financial reports, you can use the following ledger reports to view general ledger transactions:</span></span>

-   <span data-ttu-id="64ce6-121">**Dimensionsaufstellung** - Dieser Bericht zeigt Buchungen nach Tag und Konto und es gibt auch Optionen, um Transaktionen nach Dimension und Periode anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-121">**Dimension statement** – This report shows transactions by day and account, and there are also options to show transactions by dimension and period.</span></span>
-   <span data-ttu-id="64ce6-122">**Sachkontobuchungsliste** – Dieser Bericht zeigt Transaktionen in Transaktions-, Buchhaltungs- und Berichtswährungen für ein Konto an.</span><span class="sxs-lookup"><span data-stu-id="64ce6-122">**Ledger transaction list** – This report shows transactions in transaction, accounting, and reporting currencies for an account.</span></span>
-   <span data-ttu-id="64ce6-123">**Erfassung drucken** – Dieser Bericht zeigt das Ergebnis einer gebuchte Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="64ce6-123">**Print journal** – This report shows the result of a posted journal.</span></span> <span data-ttu-id="64ce6-124">Sie können den Bericht auf Basis der Nummer der Stapelverarbeitungserfassung oder des Erfassungstyp ausführen oder zusätzliche Felder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="64ce6-124">You can run the report by journal batch number or journal type, or add additional fields.</span></span>
-   <span data-ttu-id="64ce6-125">**Gebuchte Posten nach Erfassung** – In diesem Bericht werden die Transaktionen, die in einer Erfassung gebucht wurden gruppiert nach Beleg angezeigt.</span><span class="sxs-lookup"><span data-stu-id="64ce6-125">**Posted transactions by journal** – This report shows the transactions that have been posted to a journal, grouped by voucher.</span></span>
-   <span data-ttu-id="64ce6-126">**Sachkontopostenliste nach Datum** – Dieser Bericht zeigt alle Transaktionen nach Datum, zusammen mit der Erfassungsnummer, dem Beleg und dem Sachkonto an.</span><span class="sxs-lookup"><span data-stu-id="64ce6-126">**Transaction list by date** – This report shows all the transactions by date, together with the journal number, voucher, and ledger account.</span></span> <span data-ttu-id="64ce6-127">Darin werden auch die Transaktionen in den Transaktions-, Buchhaltungs- und Berichtswährungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="64ce6-127">It also shows the transactions in the transaction, accounting, and reporting currencies.</span></span>
-   <span data-ttu-id="64ce6-128">**Buchungsgrundlage** – Dieser Transaktionsbericht zeigt das Konto nach Efassuung und nach Transaktions-, Buchhaltungs- und Berichtswährung an.</span><span class="sxs-lookup"><span data-stu-id="64ce6-128">**Transaction origin** – This transaction report shows the account by journal, and by transaction, accounting, and reporting currency.</span></span> <span data-ttu-id="64ce6-129">Es wird auch jede Position der Erfassung angezeigt, die als Ausgleich verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="64ce6-129">It also shows each line of the journal that was used as an offset.</span></span>


##<a name="see-also"></a><span data-ttu-id="64ce6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64ce6-130">See also</span></span>
- [<span data-ttu-id="64ce6-131">Kontosalden für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="64ce6-131">General ledger account balances</span></span>](general-ledger-account-balances.md) 
- [<span data-ttu-id="64ce6-132">Buchhaltungsquellen-Explorer</span><span class="sxs-lookup"><span data-stu-id="64ce6-132">Accounting source explorer</span></span>](..\accounts-payable\accounting-source-explorer.md)
- [<span data-ttu-id="64ce6-133">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="64ce6-133">Financial reporting</span></span>](financial-reporting-getting-started.md)
- [<span data-ttu-id="64ce6-134">Journaleinträge anzeigen</span><span class="sxs-lookup"><span data-stu-id="64ce6-134">View journal entries</span></span>](tasks/view-journal-entries-or-transactions.md)




