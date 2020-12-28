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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443597"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="52df9-103">Ausgleichen von Buchungen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="52df9-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52df9-104">Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.</span><span class="sxs-lookup"><span data-stu-id="52df9-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="52df9-105">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="52df9-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="52df9-106">Ausgleichen von Transaktionen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="52df9-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="52df9-107">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="52df9-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="52df9-108">Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="52df9-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="52df9-109">Der Saldo muss null sein.</span><span class="sxs-lookup"><span data-stu-id="52df9-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="52df9-110">Klicken Sie auf "Einschließen"..</span><span class="sxs-lookup"><span data-stu-id="52df9-110">Click Include.</span></span>
4. <span data-ttu-id="52df9-111">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="52df9-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="52df9-112">Stornieren eines Sachkontoausgleichs</span><span class="sxs-lookup"><span data-stu-id="52df9-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="52df9-113">Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".</span><span class="sxs-lookup"><span data-stu-id="52df9-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="52df9-114">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".</span><span class="sxs-lookup"><span data-stu-id="52df9-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="52df9-115">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="52df9-115">Click Update.</span></span>
4. <span data-ttu-id="52df9-116">Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.</span><span class="sxs-lookup"><span data-stu-id="52df9-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="52df9-117">Klicken Sie auf "Alle Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="52df9-117">Click All transactions.</span></span>
6. <span data-ttu-id="52df9-118">Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="52df9-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="52df9-119">Klicken Sie auf "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="52df9-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="52df9-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="52df9-120">In the list, mark the selected row.</span></span>

