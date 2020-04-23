---
title: Allgemeine Ursachen für Produktionsabweichungen
description: In diesem Artikel werden verschiedene typische Quellen jedes Typs einer Produktionsabweichung beschrieben.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09e24d7ed041686385b8239287288228d3668e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201961"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="aaabc-103">Allgemeine Ursachen für Produktionsabweichungen</span><span class="sxs-lookup"><span data-stu-id="aaabc-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aaabc-104">In diesem Artikel werden verschiedene typische Quellen jedes Typs einer Produktionsabweichung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aaabc-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="aaabc-105">Nachfolgend sind einige typische Quellen einer **Losgrößen**abweichung:</span><span class="sxs-lookup"><span data-stu-id="aaabc-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="aaabc-106">Die Gutmenge eines Produktionsauftrags unterscheidet sich von der Berechnungsmenge, die für die Standardkostenberechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aaabc-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="aaabc-107">Die Menge bildet die Grundlage für die Amortisierung konstanter Kosten.</span><span class="sxs-lookup"><span data-stu-id="aaabc-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="aaabc-108">Der Wert der konstanten Kosten im Produktionsauftrag unterscheidet sich von den konstanten Kosten in der Standardkostenberechnung.</span><span class="sxs-lookup"><span data-stu-id="aaabc-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="aaabc-109">Die Abweichung der konstanten Kosten im Produktionsauftrag kann unterschiedliche Ursachen haben.</span><span class="sxs-lookup"><span data-stu-id="aaabc-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="aaabc-110">Beispielsweise beinhalteten die konstanten Kosten möglicherweise die folgenden Faktoren:</span><span class="sxs-lookup"><span data-stu-id="aaabc-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="aaabc-111">Manuelle Änderungen an der Stückliste oder am Arbeitsplan für die Produktion</span><span class="sxs-lookup"><span data-stu-id="aaabc-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="aaabc-112">Auswahl einer anderen Stücklisten- oder Arbeitplanversion beim Erstellen des Produktionsauftrags</span><span class="sxs-lookup"><span data-stu-id="aaabc-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="aaabc-113">Geplante Änderungen an der dem Artikel zugewiesenen Stücklisten- oder Arbeitsplanversion</span><span class="sxs-lookup"><span data-stu-id="aaabc-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="aaabc-114">Nachfolgend sind einige typische Quellen einer **Produktionpreis**abweichung:</span><span class="sxs-lookup"><span data-stu-id="aaabc-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="aaabc-115">Die Kostenkategorie (und der entsprechende Kostenkategoriepreis) für den gemeldeten Verbrauch eines Arbeitsplan-Arbeitsgangs unterscheidet sich von der Kostenkategorie, die in der Standardkostenberechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aaabc-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="aaabc-116">Die aktiven Kosten für den Kostenkategoriepreis unterscheiden sich vom Kostenkategoriepreis, der in der Standardkostenberechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aaabc-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="aaabc-117">Nachfolgend sind einige typische Quellen einer **Produktionsmengen**abweichung:</span><span class="sxs-lookup"><span data-stu-id="aaabc-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="aaabc-118">Zu hoher oder zu geringer Abgang einer Materialkomponente.</span><span class="sxs-lookup"><span data-stu-id="aaabc-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="aaabc-119">Über- oder unterbewerteter Bericht der Zeit für einen Routing-Arbeitsgang.</span><span class="sxs-lookup"><span data-stu-id="aaabc-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="aaabc-120">Über- oder Unterempfang der Warenmenge des übergeordneten Artikels, relativ zur Auftragsmenge.</span><span class="sxs-lookup"><span data-stu-id="aaabc-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="aaabc-121">Sie melden aber Komponenten und Meldungen zu Arbeitsgängen als abgeschlossen, basierend auf der Menge für den Produktionsauftrag.</span><span class="sxs-lookup"><span data-stu-id="aaabc-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="aaabc-122">Nachfolgend sind einige typische Quellen einer **Produktionsersatz**abweichung:</span><span class="sxs-lookup"><span data-stu-id="aaabc-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="aaabc-123">Abgang einer Materialkomponente, die sich nicht in der Produktionsstückliste befindet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="aaabc-124">Manuelles Hinzufügen einer Komponente zur Produktionsstückliste und Melden der Komponente als verbraucht.</span><span class="sxs-lookup"><span data-stu-id="aaabc-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="aaabc-125">Melden eines Artikels als verbraucht, ohne ihn manuell der Produktionsstückliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="aaabc-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="aaabc-126">Manuelles Hinzufügen eines Arbeitsgangs zum Produktionsarbeitsplan und Melden des Arbeitsgangs als verbraucht.</span><span class="sxs-lookup"><span data-stu-id="aaabc-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="aaabc-127">Auswählen einer anderen Stücklistenversion beim Erstellen des Produktionsauftrags, die sich von der in der Standardkostenberechnung verwendeten Stücklistenversion unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="aaabc-128">Auswählen einer anderen Arbeitsplanversion beim Erstellen des Produktionsauftrags, die sich von der in der Standardkostenberechnung verwendeten Arbeitsplanversion unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




