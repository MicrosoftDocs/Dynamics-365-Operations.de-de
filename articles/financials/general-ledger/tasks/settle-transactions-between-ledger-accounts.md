---
title: Ausgleichen von Buchungen zwischen Sachkonten
description: Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568119"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="f927f-103">Ausgleichen von Buchungen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="f927f-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f927f-104">Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.</span><span class="sxs-lookup"><span data-stu-id="f927f-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="f927f-105">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f927f-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="f927f-106">Ausgleichen von Transaktionen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="f927f-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="f927f-107">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="f927f-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="f927f-108">Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="f927f-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="f927f-109">Der Saldo muss null sein.</span><span class="sxs-lookup"><span data-stu-id="f927f-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="f927f-110">Klicken Sie auf "Einschließen"..</span><span class="sxs-lookup"><span data-stu-id="f927f-110">Click Include.</span></span>
4. <span data-ttu-id="f927f-111">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="f927f-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="f927f-112">Stornieren eines Sachkontoausgleichs</span><span class="sxs-lookup"><span data-stu-id="f927f-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="f927f-113">Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".</span><span class="sxs-lookup"><span data-stu-id="f927f-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="f927f-114">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".</span><span class="sxs-lookup"><span data-stu-id="f927f-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="f927f-115">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f927f-115">Click Update.</span></span>
4. <span data-ttu-id="f927f-116">Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.</span><span class="sxs-lookup"><span data-stu-id="f927f-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="f927f-117">Klicken Sie auf "Alle Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="f927f-117">Click All transactions.</span></span>
6. <span data-ttu-id="f927f-118">Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f927f-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="f927f-119">Klicken Sie auf "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="f927f-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="f927f-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f927f-120">In the list, mark the selected row.</span></span>

