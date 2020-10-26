---
title: Methodik der Abschreibungskonvention für ein halbes Jahr
description: In diesem Thema wird die Methode beschrieben, mit der bei Anlagevermögen die Abschreibung nach der Halbjahreskonvention berechnet wird, die die sechsmonatige Abschreibung während des ersten und letzten Betriebsjahres eines Vermögenswerts berechnet.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977238"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="d3d78-103">Methodik der Abschreibungskonvention für ein halbes Jahr</span><span class="sxs-lookup"><span data-stu-id="d3d78-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d3d78-104">In diesem Thema wird die Methode beschrieben, mit der im Anlagevermögen die Abschreibung nach der Halbjahreskonvention berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3d78-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="d3d78-105">Mit der Halbjahreskonvention wird die sechsmonatige Abschreibung während des ersten und letzten Dienstjahres eines Vermögenswerts berechnet.</span><span class="sxs-lookup"><span data-stu-id="d3d78-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="d3d78-106">Weitere Informationen zu Abschreibungskonventionen finden Sie untere [Abschreibungsmethoden und - konventionen](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="d3d78-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="d3d78-107">Wenn Sie die sechsmonatige Abschreibungskonvention verwenden, nutzt das System das Erwerbsjahr oder das Jahr, in dem der Vermögenswert in Betrieb genommen wurde, berechnet dann fünf Jahre Abschreibung aus diesem Jahr und addiert dann sechs Monate.</span><span class="sxs-lookup"><span data-stu-id="d3d78-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="d3d78-108">Betrachten Sie zur Veranschaulichung dieses Prozesses einen Vermögenswert, der zum Preis von 50.000 erworben und im April 2020 in Betrieb genommen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3d78-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="d3d78-109">Nehmen Sie außerdem an, dass der Vermögenswert eine Lebensdauer von fünf Jahren hat.</span><span class="sxs-lookup"><span data-stu-id="d3d78-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="d3d78-110">Das erste Dienstjahr endet im Dezember 2020, d.h. die fünfjährige Nutzungsdauer des Vermögenswerts endet im Dezember 2024.</span><span class="sxs-lookup"><span data-stu-id="d3d78-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="d3d78-111">Die Halbjahresabschreibungskonvention verlängert die Lebensdauer des Vermögenswerts um sechs Monate, was bedeutet, dass seine Nutzungsdauer im Juni 2025 endet.</span><span class="sxs-lookup"><span data-stu-id="d3d78-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="d3d78-112">Jährliche Abschreibung 50.000/5 = 10.000 monatliche Abschreibung 10.000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="d3d78-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="d3d78-113">Abschreibung im ersten Jahr 10.000/2 = 5.000 und die anschließende monatliche Abschreibung 5.000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="d3d78-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="d3d78-114">[![Abschreibungsplan für die Halbjahresabschreibungskonvention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="d3d78-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="d3d78-115">Die verlängerten Abschreibungszeiträume die durch die Halbjahreskonvention hinzugefügt werden, ermöglichen eine genauere Zuordnung der Abschreibungen.</span><span class="sxs-lookup"><span data-stu-id="d3d78-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="d3d78-116">Die Sechsmonatsvereinbarung stellt die Abschreibungskosten gleichmäßiger dar, was für die Berichterstattung in der Gewinn- und Verlustrechnung nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="d3d78-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
