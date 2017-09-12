--- 
title: Ausgleichen von Buchungen zwischen Sachkonten
description: Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 97a28069f8d560c98099a667852c932ba7658996
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="aa02c-103">Ausgleichen von Buchungen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="aa02c-103">Settle transactions between ledger accounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa02c-104">Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.</span><span class="sxs-lookup"><span data-stu-id="aa02c-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="aa02c-105">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa02c-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="aa02c-106">Ausgleichen von Transaktionen zwischen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="aa02c-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="aa02c-107">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="aa02c-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="aa02c-108">Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="aa02c-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="aa02c-109">Der Saldo muss null sein.</span><span class="sxs-lookup"><span data-stu-id="aa02c-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="aa02c-110">Klicken Sie auf "Einschließen"..</span><span class="sxs-lookup"><span data-stu-id="aa02c-110">Click Include.</span></span>
4. <span data-ttu-id="aa02c-111">Klicken Sie auf "Annehmen".</span><span class="sxs-lookup"><span data-stu-id="aa02c-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="aa02c-112">Stornieren eines Sachkontoausgleichs</span><span class="sxs-lookup"><span data-stu-id="aa02c-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="aa02c-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="aa02c-113">Close the page.</span></span>
2. <span data-ttu-id="aa02c-114">Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".</span><span class="sxs-lookup"><span data-stu-id="aa02c-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="aa02c-115">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".</span><span class="sxs-lookup"><span data-stu-id="aa02c-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="aa02c-116">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa02c-116">Click Update.</span></span>
5. <span data-ttu-id="aa02c-117">Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.</span><span class="sxs-lookup"><span data-stu-id="aa02c-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="aa02c-118">Klicken Sie auf "Alle Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="aa02c-118">Click All transactions.</span></span>
7. <span data-ttu-id="aa02c-119">Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="aa02c-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="aa02c-120">Klicken Sie auf "Sachkontoausgleiche".</span><span class="sxs-lookup"><span data-stu-id="aa02c-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="aa02c-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="aa02c-121">In the list, mark the selected row.</span></span>


