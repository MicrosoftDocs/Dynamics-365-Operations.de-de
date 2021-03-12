---
title: Abschreibungsmethoden und -konventionen
description: Dieser Artikel gibt einen Überblick über die Abschreibungskonventionen und Abschreibungsmethoden, die von Microsoft Dynamics 365 Finance unterstützt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af1c1a222981a0bcf9d7341cde5b83dd720da802
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994964"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="17684-103">Abschreibungsmethoden und -konventionen</span><span class="sxs-lookup"><span data-stu-id="17684-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17684-104">Dieser Artikel gibt einen Überblick über die unterstützten Abschreibungskonventionen und Abschreibungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="17684-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="17684-105">Es können verschiedene Abschreibungsmethoden und -konventionen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="17684-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="17684-106">Zweck der Methoden ist die Verteilung des abschreibungsfähigen Werts der Anlage auf Finanzzeiträume.</span><span class="sxs-lookup"><span data-stu-id="17684-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="17684-107">Der abschreibungsfähige Wert der Anlage ist der Anschaffungspreis abzüglich eines Schrottwerts (sofern zutreffend).</span><span class="sxs-lookup"><span data-stu-id="17684-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="17684-108">Wenn Sie bei der Verwendung von Abschreibungskonventionen das letzte Ausführungsdatum der Abschreibung für eine Anlage ändern, woraufhin einige Abschreibungen übersprungen werden, ist die Abschreibung für das letzte Jahr möglicherweise größer oder kleiner als erwartet.</span><span class="sxs-lookup"><span data-stu-id="17684-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="17684-109">Die Abschreibung wird durch die Anzahl der Abschreibungszeiträume reguliert, die von der Änderung des letzten Anfangsdatums der Abschreibung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="17684-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="17684-110">Wenn Sie zum Beispiel die Abschreibungskonvention "Halbjahr" über einen Zeitraum von drei Jahren verwenden, erstreckt sich der Abschreibungszeitraum in der Regel auf 3,5 Jahre.</span><span class="sxs-lookup"><span data-stu-id="17684-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="17684-111">Wenn Sie das letzte Anfangsdatum während dieser 3,5 Jahre ändern, wird das letzte Abschreibungsjahr um die Anzahl der betroffenen Zeiträume verlängert.</span><span class="sxs-lookup"><span data-stu-id="17684-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="17684-112">Verschieben Sie z. B. das Datum um drei Monate, umfasst das letzte Jahr neun Abschreibungsmonate, während es normalerweise sechs Monate umfassen würde.</span><span class="sxs-lookup"><span data-stu-id="17684-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="17684-113">Die folgenden Abschreibungskonventionen stehen zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="17684-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="17684-114">Halbjahr</span><span class="sxs-lookup"><span data-stu-id="17684-114">Half year</span></span>
-   <span data-ttu-id="17684-115">Ganzer Monat</span><span class="sxs-lookup"><span data-stu-id="17684-115">Full month</span></span>
-   <span data-ttu-id="17684-116">Quartalsmitte</span><span class="sxs-lookup"><span data-stu-id="17684-116">Mid quarter</span></span>
-   <span data-ttu-id="17684-117">Monatsmitte (1. des Monats)</span><span class="sxs-lookup"><span data-stu-id="17684-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="17684-118">Monatsmitte (15. des Monats)</span><span class="sxs-lookup"><span data-stu-id="17684-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="17684-119">Halbes Jahr (Jahresanfang)</span><span class="sxs-lookup"><span data-stu-id="17684-119">Half year (start of year)</span></span>
-   <span data-ttu-id="17684-120">Halbes Jahr (nächstes Jahr)</span><span class="sxs-lookup"><span data-stu-id="17684-120">Half year (next year)</span></span>

<span data-ttu-id="17684-121">Die folgenden Abschreibungsmethoden stehen zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="17684-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="17684-122">Lineare Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="17684-122">Straight line service life</span></span>
-   <span data-ttu-id="17684-123">Degressiv</span><span class="sxs-lookup"><span data-stu-id="17684-123">Reducing balance</span></span>
-   <span data-ttu-id="17684-124">Manuell</span><span class="sxs-lookup"><span data-stu-id="17684-124">Manual</span></span>
-   <span data-ttu-id="17684-125">Faktor</span><span class="sxs-lookup"><span data-stu-id="17684-125">Factor</span></span>
-   <span data-ttu-id="17684-126">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="17684-126">Consumption</span></span>
-   <span data-ttu-id="17684-127">Verbleibende lineare Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="17684-127">Straight line life remaining</span></span>
-   <span data-ttu-id="17684-128">200% degressiv</span><span class="sxs-lookup"><span data-stu-id="17684-128">200% reducing balance</span></span>
-   <span data-ttu-id="17684-129">175% degressiv</span><span class="sxs-lookup"><span data-stu-id="17684-129">175% reducing balance</span></span>
-   <span data-ttu-id="17684-130">150% degressiv</span><span class="sxs-lookup"><span data-stu-id="17684-130">150% reducing balance</span></span>
-   <span data-ttu-id="17684-131">125% degressiv</span><span class="sxs-lookup"><span data-stu-id="17684-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="17684-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17684-132">Additional resources</span></span>
--------

[<span data-ttu-id="17684-133">Anlagenabschreibung</span><span class="sxs-lookup"><span data-stu-id="17684-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="17684-134">Abschreibungsmethode „Lineare Nutzungsdauer“</span><span class="sxs-lookup"><span data-stu-id="17684-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="17684-135">Degressive Abschreibung reduzieren</span><span class="sxs-lookup"><span data-stu-id="17684-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="17684-136">Manuelle Abschreibung</span><span class="sxs-lookup"><span data-stu-id="17684-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="17684-137">Faktorabschreibung</span><span class="sxs-lookup"><span data-stu-id="17684-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="17684-138">Verbrauchsabschreibung</span><span class="sxs-lookup"><span data-stu-id="17684-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="17684-139">Abschreibungsmethode "Verbleibende lineare Nutzungsdauer"</span><span class="sxs-lookup"><span data-stu-id="17684-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="17684-140">Degressiven Abschreibung von 125 Prozent</span><span class="sxs-lookup"><span data-stu-id="17684-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="17684-141">Degressiven Abschreibung von 150 Prozent</span><span class="sxs-lookup"><span data-stu-id="17684-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="17684-142">Degressiven Abschreibung von 175 Prozent</span><span class="sxs-lookup"><span data-stu-id="17684-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="17684-143">Degressiven Abschreibung von 200 Prozent</span><span class="sxs-lookup"><span data-stu-id="17684-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



