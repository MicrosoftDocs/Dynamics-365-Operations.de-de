---
title: Die geplante Einkaufsbestellung wird erstellt, wenn ein Kauf innerhalb negativer Tage vorliegt
description: Wenn das Dispositionsverfahren Min/Max lautet, erstellt die Planungsoptimierung eine geplante Einkaufsbestellung, wenn ein Kauf innerhalb negativer Tage vorliegt.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026547"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="f1a33-103">Die geplante Einkaufsbestellung wird erstellt, wenn ein Kauf innerhalb negativer Tage vorliegt</span><span class="sxs-lookup"><span data-stu-id="f1a33-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="f1a33-104">KB-Nummer: 4614298</span><span class="sxs-lookup"><span data-stu-id="f1a33-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="f1a33-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="f1a33-105">Symptoms</span></span>

<span data-ttu-id="f1a33-106">Wenn das Dispositionsverfahren *Min/Max* lautet, erstellt die Planungsoptimierung eine geplante Einkaufsbestellung, wenn ein Kauf innerhalb negativer Tage vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f1a33-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="f1a33-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="f1a33-107">Resolution</span></span>

<span data-ttu-id="f1a33-108">Die Planungsoptimierung unterstützt negative Tage nicht.</span><span class="sxs-lookup"><span data-stu-id="f1a33-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="f1a33-109">Es wird jedoch immer sichergestellt, dass geplante Bestellungen nicht innerhalb der Vorlaufzeit im Verhältnis zum aktuellen Datum geplant werden.</span><span class="sxs-lookup"><span data-stu-id="f1a33-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="f1a33-110">Beispielsweise beträgt die Vorlaufzeit für den Kauf 10 Tage, und eine Bestellung wird voraussichtlich in acht Tagen ab heute eintreffen.</span><span class="sxs-lookup"><span data-stu-id="f1a33-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="f1a33-111">In diesem Fall wird die Bestellung als Angebot für die Nachfrage verwendet, die fünf Tage ab heute liegt.</span><span class="sxs-lookup"><span data-stu-id="f1a33-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="f1a33-112">Wir empfehlen daher, dass Sie Ihre Vorlaufzeiten anpassen, um alle (oder fast alle) Ihrer Szenarien abzudecken.</span><span class="sxs-lookup"><span data-stu-id="f1a33-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
