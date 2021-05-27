---
title: Wenn eine Artikelgewichtsmenge aufgeteilt wird, wird anstelle der nominellen Menge die Mindestmenge verwendet
description: Wenn eine Artikelgewichtsmenge in Batches aufgeteilt wird, verwendet das Feld „Entnahmemenge“ die Mindestmenge, die für den Artikel festgelegt wurde, nicht die nominelle Menge.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026550"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="2fe90-103">Wenn eine Artikelgewichtsmenge aufgeteilt wird, wird anstelle der nominellen Menge die Mindestmenge verwendet</span><span class="sxs-lookup"><span data-stu-id="2fe90-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="2fe90-104">KB-Nummer: 4612073</span><span class="sxs-lookup"><span data-stu-id="2fe90-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="2fe90-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="2fe90-105">Symptoms</span></span>

<span data-ttu-id="2fe90-106">Wenn eine Artikelgewichtsmenge in Batches aufgeteilt wird, verwendet das Feld **Entnahmemenge** die Mindestmenge, die für den Artikel festgelegt wurde, nicht die nominelle Menge.</span><span class="sxs-lookup"><span data-stu-id="2fe90-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="2fe90-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="2fe90-107">Resolution</span></span>

<span data-ttu-id="2fe90-108">Das System verhält sich wie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="2fe90-108">The system is behaving as designed.</span></span> <span data-ttu-id="2fe90-109">Das System verwendet für die Kommissionierung die Mindestmengeneinstellung jedes Artikels.</span><span class="sxs-lookup"><span data-stu-id="2fe90-109">The system uses each item's minimum quantity setup for picking.</span></span>
