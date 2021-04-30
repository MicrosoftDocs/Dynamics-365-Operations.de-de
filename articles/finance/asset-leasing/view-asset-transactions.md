---
title: Verbindlichkeiten, Anlagen und Ausgabentransaktionen anzeigen
description: In diesem Thema wird erläutert, wie Sie Transaktionen für einen Leasingobjekt anzeigen. Diese Transaktionen umfassen Leasingverbindlichkeitstransaktionen und Transaktionen mit Ausführungskosten, die gebucht wurden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 55b8019db6abdb3bd5ecdb6eadc4f7443f2bf071
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881637"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="b25b4-104">Verbindlichkeiten, Anlagen und Ausgabentransaktionen anzeigen</span><span class="sxs-lookup"><span data-stu-id="b25b4-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b25b4-105">In diesem Thema wird erläutert, wie Sie Transaktionen für einen Leasingobjekt anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b25b4-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="b25b4-106">Diese Transaktionen umfassen Leasingverbindlichkeitstransaktionen und Transaktionen mit Ausführungskosten, die gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b25b4-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="b25b4-107">Die Buchwerte der Verbindlichkeit und des Nutzungsrechts am Leasingobjekt werden in mehreren Berichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b25b4-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="b25b4-108">Sie werden auch zur Berechnung von Regulierungswerten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b25b4-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="b25b4-109">Verbindlichkeitstransaktionen</span><span class="sxs-lookup"><span data-stu-id="b25b4-109">Liability transactions</span></span>

<span data-ttu-id="b25b4-110">Um die Leasingverbindlichkeitstransaktionen anzuzeigen, wählen Sie einen Mietvertrag auf der **Mietvertragsübersicht**-Seite und dann **Bücher** aus, um die Bücher zu öffnen, die dem Mietvertragsdatensatz zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b25b4-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="b25b4-111">Nachdem eine erstmalige Erfassung, eine Rechnung oder eine Zinserfassung gebucht wurde, wählen Sie **Verbindlichkeitstransaktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="b25b4-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="b25b4-112">Die **Verbindlichkeitstransaktionen**-Seite zeigt die Transaktionen, die die Leasingverbindlichkeit erhöhen oder verringern.</span><span class="sxs-lookup"><span data-stu-id="b25b4-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="b25b4-113">Negative Beträge auf dieser Seite repräsentieren Habentransaktionen in der Standardanwendung.</span><span class="sxs-lookup"><span data-stu-id="b25b4-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="b25b4-114">Zinsabgrenzungen werden als negative Werte ausgewiesen und erhöhen die gesamte Leasingverbindlichkeit.</span><span class="sxs-lookup"><span data-stu-id="b25b4-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="b25b4-115">Alle Mietvertragsregulierungen werden je nach Art und Auswirkung des Leasingbuchs als positive oder negative Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b25b4-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="b25b4-116">Der aktuelle Nettosaldo der Leasingverbindlichkeit für den ausgewählten Mietvertrag wird unten links auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b25b4-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="b25b4-117">Anlagenbuchungen</span><span class="sxs-lookup"><span data-stu-id="b25b4-117">Asset transactions</span></span>

<span data-ttu-id="b25b4-118">Um die Mietanlagentransaktionen anzuzeigen, wählen Sie einen Mietvertrag auf der **Mietvertragsübersicht**-Seite und dann **Bücher** aus, um die Leasingbücher zu öffnen, die dem Mietvertragsdatensatz zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b25b4-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="b25b4-119">Wählen Sie dann **Anlagentransaktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="b25b4-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="b25b4-120">Die **Anlagentransaktion**-Seite zeigt die Transaktionen, die die Mietanlage und die kumulierten Abschreibungskonten entweder erhöhen oder verringern.</span><span class="sxs-lookup"><span data-stu-id="b25b4-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="b25b4-121">Belastungen werden wie auf der **Verbindlichkeitstransaktionen**-Seite als positive Werte und Gutschriften als negative Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b25b4-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="b25b4-122">Die gebuchte erstmalige Erfassung und die nächste kumulierte Abschreibung werden unten links auf der Seite als Anlagensaldo angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b25b4-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="b25b4-123">Ausgabentransaktionen</span><span class="sxs-lookup"><span data-stu-id="b25b4-123">Expenses transactions</span></span>

<span data-ttu-id="b25b4-124">Um die Mietausgabentransaktionen anzuzeigen, wählen Sie einen Mietvertrag auf der **Mietvertragsübersicht**-Seite und dann **Bücher** aus, um die Leasingbücher zu öffnen, die dem Mietvertragsdatensatz zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b25b4-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="b25b4-125">Wählen Sie dann **Ausgabentransaktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="b25b4-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="b25b4-126">Die **Ausgabentransaktionen**-Seite werden alle Ausgaben angezeigt, die auf den Mietvertrag gebucht wurden, z. B. Zinsaufwendungen, Abschreibungsaufwendungen und etwaige Nebenkosten beim Leasing.</span><span class="sxs-lookup"><span data-stu-id="b25b4-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
