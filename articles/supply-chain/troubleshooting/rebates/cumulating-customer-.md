---
title: Die Kumulierung von Debitorenrückvergütungen schlägt fehl, wenn Artikelrückvergütungsgruppen verwendet werden
description: Wenn Sie Kundenrückvergütungsvereinbarungen in Kombination mit Artikelrückvergütungsgruppen verwenden, werden Rückvergütungen berechnet, die Kumulierung schlägt jedoch fehl.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026531"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="ed8fe-103">Die Kumulierung von Debitorenrückvergütungen schlägt fehl, wenn Artikelrückvergütungsgruppen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ed8fe-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="ed8fe-104">KB-Nummer: 4611372</span><span class="sxs-lookup"><span data-stu-id="ed8fe-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed8fe-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="ed8fe-105">Symptoms</span></span>

<span data-ttu-id="ed8fe-106">Wenn Sie Kundenrückvergütungsvereinbarungen (vom Typ *Betrag*) in Kombination mit Artikelrückvergütungsgruppen verwenden, werden Rückvergütungen berechnet, die Kumulierung schlägt jedoch fehl.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed8fe-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="ed8fe-107">Resolution</span></span>

<span data-ttu-id="ed8fe-108">Das System verhält sich wie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-108">The system is behaving as designed.</span></span> <span data-ttu-id="ed8fe-109">Artikelgruppen gruppieren nur Artikel, die dieselbe Schwellenwertbedingung haben.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="ed8fe-110">Die Rückvergütungsbedingung (Schwellenwert) wird gegen den Betrag für jeden Artikel und nicht gegen den kumulierten Betrag für einen Artikel in der Artikelgruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
