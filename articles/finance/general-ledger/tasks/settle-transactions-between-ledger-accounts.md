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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994414"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="51496-103">Ausgleichen von Buchungen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="51496-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51496-104">Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.</span><span class="sxs-lookup"><span data-stu-id="51496-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="51496-105">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="51496-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="51496-106">Ausgleichen von Transaktionen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="51496-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="51496-107">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="51496-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="51496-108">Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="51496-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="51496-109">Der Saldo muss null sein.</span><span class="sxs-lookup"><span data-stu-id="51496-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="51496-110">Klicken Sie auf "Einschließen"..</span><span class="sxs-lookup"><span data-stu-id="51496-110">Click Include.</span></span>
4. <span data-ttu-id="51496-111">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="51496-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="51496-112">Stornieren eines Sachkontoausgleichs</span><span class="sxs-lookup"><span data-stu-id="51496-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="51496-113">Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".</span><span class="sxs-lookup"><span data-stu-id="51496-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="51496-114">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".</span><span class="sxs-lookup"><span data-stu-id="51496-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="51496-115">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="51496-115">Click Update.</span></span>
4. <span data-ttu-id="51496-116">Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.</span><span class="sxs-lookup"><span data-stu-id="51496-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="51496-117">Klicken Sie auf "Alle Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="51496-117">Click All transactions.</span></span>
6. <span data-ttu-id="51496-118">Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="51496-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="51496-119">Klicken Sie auf "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="51496-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="51496-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="51496-120">In the list, mark the selected row.</span></span>

