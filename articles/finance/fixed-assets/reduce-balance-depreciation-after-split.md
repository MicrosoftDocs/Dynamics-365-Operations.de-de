---
title: Degressive Abschreibung nach einer Teilung reduzieren
description: In diesem Thema wird die Methode beschrieben, die im Anlagevermögen verwendet wird, um die Abschreibung nach der Aufteilung einer Anlage mithilfe der Methode zum Reduzieren des Saldos zu berechnen.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea89d54b9b8287d9c81b75a99c5808b5deb05cef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976090"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="60cfc-103">Degressive Abschreibung nach einer Teilung reduzieren</span><span class="sxs-lookup"><span data-stu-id="60cfc-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60cfc-104">In diesem Thema wird die Methode beschrieben, die im Anlagevermögen verwendet wird, um die Abschreibung nach der Aufteilung einer Anlage in eine andere Anlage mithilfe der Methode zum Reduzieren des Saldos zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="60cfc-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="60cfc-105">Das im Anlagenbuch konfigurierte Abschreibungsjahr ist das Geschäftsjahr.</span><span class="sxs-lookup"><span data-stu-id="60cfc-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="60cfc-106">Weitere Informationen finden Sie unter [Reduzierung der degressiven Abschreibung](reduce-balance-depreciation.md) und [Aufteilen einer Anlage](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="60cfc-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="60cfc-107">Wenn Sie eine Anlage während eines Finanzzeitraums aufteilen, der später als der Zeitraum ist, in dem die Anlage erworben wurde, wird der Nettobuchwert (NBV) der Anlage für das Vorjahr durch die reduzierte degressive Abschreibung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="60cfc-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="60cfc-108">Es werden auch die Anschaffungs- und Abschreibungsregulierungstransaktionen berücksichtigt, die aus der Transaktion generiert wurden, mit der die Anlage aufgeteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="60cfc-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="60cfc-109">Bei diesem Verhalten wird davon ausgegangen, dass die Anlage in einem Geschäftsjahr angeschafft und in einem späteren Geschäftsjahr aufgeteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="60cfc-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="60cfc-110">Der Betrag, der nach der Aufteilung für die ursprüngliche Anlage abgeschrieben werden muss, spiegelt den NBV der Anlage vor der Aufteilung der Anlage und die für die Aufteilung gebuchte Anschaffungs- und Abschreibungsregulierungstransaktion wider.</span><span class="sxs-lookup"><span data-stu-id="60cfc-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="60cfc-111">Beispielsweise gelten die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="60cfc-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="60cfc-112">Der Finanzzeitraum dauert vom 30. Juni bis zum 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="60cfc-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="60cfc-113">Der Prozentsatz des reduzierenden Saldos beträgt 18 Prozent, und eine Anlage wird im Juni 2019 zu einem Kaufpreis von 10.000 USD erworben.</span><span class="sxs-lookup"><span data-stu-id="60cfc-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="60cfc-114">Die Abschreibung im ersten Geschäftsjahr beträgt 18.000 USD, die monatliche Abschreibung entspricht 150 USD, und die Anlage wird dann bis November 2019 in Höhe von 738,75 USD abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="60cfc-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="60cfc-115">Im November 2019 werden 80 Prozent der Anlage auf eine andere Anlage aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="60cfc-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="60cfc-116">[![Degressive Abschreibung nach einer Teilung reduzieren](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="60cfc-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="60cfc-117">Der für die ursprüngliche Anlage abzuschreibende Betrag beträgt 1.822,25 USD.</span><span class="sxs-lookup"><span data-stu-id="60cfc-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="60cfc-118">Dieser Betrag entspricht dem NBV vor der Buchung der Aufteilungstransaktion (9.111,25 USD) zuzüglich der Anschaffungsregulierung, die während der Buchung der Aufteilungstransaktion generiert wird (-8.000 USD), zuzüglich der Abschreibungsregulierung, die während der Aufteilungstransaktion generiert wird (711 USD).</span><span class="sxs-lookup"><span data-stu-id="60cfc-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="60cfc-119">Daher beträgt die Abschreibung für das zweite Jahr (1.822,25 × 18 Prozent) ÷ 12 = 27,33 USD.</span><span class="sxs-lookup"><span data-stu-id="60cfc-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="60cfc-120">Der Abschreibungsbetrag für die neue Anlage im ersten Jahr beträgt (8.000 × 18 Prozent) ÷ 12 = $120.</span><span class="sxs-lookup"><span data-stu-id="60cfc-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
