---
title: Erfassungseinträge und Transaktionen anzeigen
description: Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9768154e117ca09ae84c6a9c82d43000752c2b34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "366695"
---
# <a name="view-journal-entries-and-transactions"></a><span data-ttu-id="11e96-103">Erfassungseinträge und Transaktionen anzeigen</span><span class="sxs-lookup"><span data-stu-id="11e96-103">View journal entries and transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11e96-104">Dieser Artikel erklärt die verschiedenen Methoden zum Ansehen von Journal- und Transaktionseinträgen.</span><span class="sxs-lookup"><span data-stu-id="11e96-104">This article explains the various ways that you can view journal entries and transactions.</span></span> 

<span data-ttu-id="11e96-105">Benutzer, die Erfassungen und Transaktionen anzeigen möchten, haben mehrere Möglichkeiten für den Datenzugriff.</span><span class="sxs-lookup"><span data-stu-id="11e96-105">Users who want to view journals and transactions have several ways to access the data.</span></span> <span data-ttu-id="11e96-106">Sie können Anfragenseiten nutzen, die eine Detallanzeige ermöglichen, oder sie können verschiedene Berichtsoptionen im Hauptbuch verwenden.</span><span class="sxs-lookup"><span data-stu-id="11e96-106">They can take advantage of inquiry pages that provide drill-down ability, or they can use various report options in the general ledger.</span></span>

## <a name="voucher-transactions"></a><span data-ttu-id="11e96-107">Belegtransaktionen</span><span class="sxs-lookup"><span data-stu-id="11e96-107">Voucher transactions</span></span>
<span data-ttu-id="11e96-108">**Belegtransaktionen** ist eine Anfragenseite, in der Sie aus verschiedenen Tabellen und Feldern auswählen können, um Kriterien für den Saldo oder die Transaktion anzugeben, die Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="11e96-108">**Voucher transactions** is an inquiry page where you can select from various tables and fields to specify criteria for the balance or transaction that you're searching for.</span></span> <span data-ttu-id="11e96-109">So können Sie z. B. alle Transaktionen für ein bestimmtes Datum oder ein Konto oder alle Transaktionen des Typs **Benutzung** anzeigen, die sich auf einer bestimmten Buchungsebene befinden.</span><span class="sxs-lookup"><span data-stu-id="11e96-109">For example, you can view all transactions for a specific date or account, or all transactions of the **Operating** type that are in a specific posting layer.</span></span> <span data-ttu-id="11e96-110">Standardmäßig zeigt die Seite die Erfassungsnummer, Beleg, Datum und Hauptkonto an, Sie können jedoch zusätzliche Tabellen, Felder und Kriterien hinzufügen, um die Suche einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="11e96-110">By default, the page shows the journal number, voucher, date, and main account, but you can add additional tables, fields, and criteria to narrow down your search.</span></span>

## <a name="audit-trail"></a><span data-ttu-id="11e96-111">Audit-Trail</span><span class="sxs-lookup"><span data-stu-id="11e96-111">Audit trail</span></span>
<span data-ttu-id="11e96-112">**Audit-Trail** ist eine Anfragenseite, die Transaktionsarten, Beschreibungen, Transaktionsersteller und -datum anzeigt.</span><span class="sxs-lookup"><span data-stu-id="11e96-112">**Audit trail** is an inquiry page that shows the types of transactions, descriptions, who the transactions were created by, and when they were created.</span></span> <span data-ttu-id="11e96-113">Von der **Audit-Trail**-Anfragenseite können Sie die Belegtransaktionen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="11e96-113">From the **Audit trail** inquiry page, you can view the voucher transactions.</span></span>

## <a name="financial-reports"></a><span data-ttu-id="11e96-114">Finanzberichte</span><span class="sxs-lookup"><span data-stu-id="11e96-114">Financial reports</span></span>
<span data-ttu-id="11e96-115">Sie können Hauptbuchtransaktionen auch untersuchen und analysieren, indem Sie Finanzberichte ausführen.</span><span class="sxs-lookup"><span data-stu-id="11e96-115">You can also explore and analyze general ledger transactions by running financial reports.</span></span> <span data-ttu-id="11e96-116">Da das Design von Finanzberichten auf Konten, Dimensionen, Kontokategorien oder einer Kombination dieser drei basieren kann, können Sie die Transaktionen anzeigen, indem Sie auf verschiedene Weise Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="11e96-116">Because the design of financial reports can be based on accounts, dimensions, account categories, or a combination of the three, you can view the transactions by drilling down in various ways.</span></span> <span data-ttu-id="11e96-117">Wenn Sie weitere Informationen zu Hauptbuchtransaktionen erfordern, können Sie auch mehrere Transaktionseigenschaften als Teil des Berichtsdesigns einschließen.</span><span class="sxs-lookup"><span data-stu-id="11e96-117">If you require more information for general ledger transactions, you can also include multiple transaction properties as part of the report design.</span></span> <span data-ttu-id="11e96-118">Wenn Sie darüber hinaus die Transaktionen anzeigen möchten, aus denen sich ein Hauptbuchsaldo zusammensetzt, können Sie Details für die Kontotransaktionen anzeigen,genau wie aus der **Zwischenbilanz**-Listenseite.</span><span class="sxs-lookup"><span data-stu-id="11e96-118">Additionally, if you want to see the transactions that make up a general ledger balance, you can drill down to account transactions, just as you can from the **Trial balance** list page.</span></span>

## <a name="ledger-reports"></a><span data-ttu-id="11e96-119">Sachkonto – Berichte</span><span class="sxs-lookup"><span data-stu-id="11e96-119">Ledger reports</span></span>
<span data-ttu-id="11e96-120">Neben den Finanzberichten können Sie die folgenden Sachkontoberichte verwenden, um Hauptbuchtransaktionen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="11e96-120">In addition to the financial reports, you can use the following ledger reports to view general ledger transactions:</span></span>

-   <span data-ttu-id="11e96-121">**Dimensionsaufstellung** - Dieser Bericht zeigt Buchungen nach Tag und Konto und es gibt auch Optionen, um Transaktionen nach Dimension und Periode anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="11e96-121">**Dimension statement** – This report shows transactions by day and account, and there are also options to show transactions by dimension and period.</span></span>
-   <span data-ttu-id="11e96-122">**Sachkontobuchungsliste** – Dieser Bericht zeigt Transaktionen in Transaktions-, Buchhaltungs- und Berichtswährungen für ein Konto an.</span><span class="sxs-lookup"><span data-stu-id="11e96-122">**Ledger transaction list** – This report shows transactions in transaction, accounting, and reporting currencies for an account.</span></span>
-   <span data-ttu-id="11e96-123">**Erfassung drucken** – Dieser Bericht zeigt das Ergebnis einer gebuchte Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="11e96-123">**Print journal** – This report shows the result of a posted journal.</span></span> <span data-ttu-id="11e96-124">Sie können den Bericht auf Basis der Nummer der Stapelverarbeitungserfassung oder des Erfassungstyp ausführen oder zusätzliche Felder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11e96-124">You can run the report by journal batch number or journal type, or add additional fields.</span></span>
-   <span data-ttu-id="11e96-125">**Gebuchte Posten nach Erfassung** – In diesem Bericht werden die Transaktionen, die in einer Erfassung gebucht wurden gruppiert nach Beleg angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11e96-125">**Posted transactions by journal** – This report shows the transactions that have been posted to a journal, grouped by voucher.</span></span>
-   <span data-ttu-id="11e96-126">**Sachkontopostenliste nach Datum** – Dieser Bericht zeigt alle Transaktionen nach Datum, zusammen mit der Erfassungsnummer, dem Beleg und dem Sachkonto an.</span><span class="sxs-lookup"><span data-stu-id="11e96-126">**Transaction list by date** – This report shows all the transactions by date, together with the journal number, voucher, and ledger account.</span></span> <span data-ttu-id="11e96-127">Darin werden auch die Transaktionen in den Transaktions-, Buchhaltungs- und Berichtswährungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11e96-127">It also shows the transactions in the transaction, accounting, and reporting currencies.</span></span>
-   <span data-ttu-id="11e96-128">**Buchungsgrundlage** – Dieser Transaktionsbericht zeigt das Konto nach Efassuung und nach Transaktions-, Buchhaltungs- und Berichtswährung an.</span><span class="sxs-lookup"><span data-stu-id="11e96-128">**Transaction origin** – This transaction report shows the account by journal, and by transaction, accounting, and reporting currency.</span></span> <span data-ttu-id="11e96-129">Es wird auch jede Position der Erfassung angezeigt, die als Ausgleich verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="11e96-129">It also shows each line of the journal that was used as an offset.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="11e96-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11e96-130">Additional resources</span></span>
- [<span data-ttu-id="11e96-131">Kontosalden für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="11e96-131">General ledger account balances</span></span>](general-ledger-account-balances.md) 
- [<span data-ttu-id="11e96-132">Buchhaltungsquellen-Explorer</span><span class="sxs-lookup"><span data-stu-id="11e96-132">Accounting source explorer</span></span>](../accounts-payable/accounting-source-explorer.md)
- [<span data-ttu-id="11e96-133">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="11e96-133">Financial reporting</span></span>](financial-reporting-getting-started.md)
- [<span data-ttu-id="11e96-134">Journaleinträge anzeigen</span><span class="sxs-lookup"><span data-stu-id="11e96-134">View journal entries</span></span>](tasks/view-journal-entries-or-transactions.md)



