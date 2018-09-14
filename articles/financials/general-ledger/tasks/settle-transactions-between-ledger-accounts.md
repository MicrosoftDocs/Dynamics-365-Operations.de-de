--- 
title: Ausgleichen von Buchungen zwischen Sachkonten
description: Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 27064331191f3de35bd3c77dc0c8aeca6d4b9edb
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="94c55-103">Ausgleichen von Buchungen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="94c55-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94c55-104">Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.</span><span class="sxs-lookup"><span data-stu-id="94c55-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="94c55-105">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="94c55-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="94c55-106">Ausgleichen von Transaktionen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="94c55-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="94c55-107">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="94c55-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="94c55-108">Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="94c55-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="94c55-109">Der Saldo muss null sein.</span><span class="sxs-lookup"><span data-stu-id="94c55-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="94c55-110">Klicken Sie auf "Einschließen"..</span><span class="sxs-lookup"><span data-stu-id="94c55-110">Click Include.</span></span>
4. <span data-ttu-id="94c55-111">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="94c55-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="94c55-112">Stornieren eines Sachkontoausgleichs</span><span class="sxs-lookup"><span data-stu-id="94c55-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="94c55-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="94c55-113">Close the page.</span></span>
2. <span data-ttu-id="94c55-114">Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".</span><span class="sxs-lookup"><span data-stu-id="94c55-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="94c55-115">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".</span><span class="sxs-lookup"><span data-stu-id="94c55-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="94c55-116">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="94c55-116">Click Update.</span></span>
5. <span data-ttu-id="94c55-117">Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.</span><span class="sxs-lookup"><span data-stu-id="94c55-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="94c55-118">Klicken Sie auf "Alle Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="94c55-118">Click All transactions.</span></span>
7. <span data-ttu-id="94c55-119">Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="94c55-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="94c55-120">Klicken Sie auf "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="94c55-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="94c55-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="94c55-121">In the list, mark the selected row.</span></span>


