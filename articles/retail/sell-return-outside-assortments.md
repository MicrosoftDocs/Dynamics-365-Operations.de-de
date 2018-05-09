---
title: "Produkte außerhalb eines Sortiments verkaufen und zurückgeben"
description: "Mit Dynamics 365 for Retail können Sie Produkte außerhalb der Sortimente verkaufen und zurückgeben."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0903879f7fa11c80e695dcb095ce1020984addf6
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="d4131-103">Produkte außerhalb eines Sortiments verkaufen und zurückgeben</span><span class="sxs-lookup"><span data-stu-id="d4131-103">Sell and return products outside of an assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4131-104">Ein allgemeines Szenario für einen beliebigen Einzelhändler ist es, Produkte an seine Kunden zu verkaufen oder Rücklieferungen von den Debitoren zu akzeptieren, wenn sie keine spezifische Produkte in ihrer Filiale führen (das heißt, die Produkte werden nicht nach Shop sortiert).</span><span class="sxs-lookup"><span data-stu-id="d4131-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="d4131-105">Nachfolgend sind einige typische Szenarios:</span><span class="sxs-lookup"><span data-stu-id="d4131-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="d4131-106">Ein Einzelhändler führt nicht alle zugehörigen Produkte in einem bestimmten Shop.</span><span class="sxs-lookup"><span data-stu-id="d4131-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="d4131-107">Die verbleibenden Produkte werden am Lagerort gelagert.</span><span class="sxs-lookup"><span data-stu-id="d4131-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="d4131-108">Die Der Mitarbeiter der Filiale kann dem Kunden beim Suchen nach Produkten am Lagerort helfen, sie dem Einkaufskorb hinzufügen, das Auschecken und die Wahl der Versandart vornehmen, wie der Versand an eine Adresse vom Lagerort aus oder dafür sorgen, dass der Kunde das Produkt in der aktuellen Filiale oder einer anderen Filiale abholen kann.</span><span class="sxs-lookup"><span data-stu-id="d4131-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="d4131-109">Ein Einzelhändler führt nicht bestimmte Produkte im Shop oder hat diese nicht an Lager, aber das Produkt ist in einer anderen Filiale verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4131-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="d4131-110">Der Mitarbeiter der Filiale kann dem Kunden helfen, das Produkt in einer anderen Filiale zu suchen, diese dem Einkaufskorb hinzuzufügen, sie Auszuchecken und die Versandmethode auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d4131-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="d4131-111">Ein Einzelhändler verfügt über eine Vielzahl von Shops in einem bestimmten Ort oder einem Postleitzahlkreis und möchte die Debitoren nicht dazu zwingen, die Produkte demselben Shop zurückzusenden, in dem sie bestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d4131-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="d4131-112">Stattdessen können Debitoren Produkten an einem beliebigen Shop zurücksenden.</span><span class="sxs-lookup"><span data-stu-id="d4131-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="d4131-113">Das sind allgemeine Szenarien für Einzelhändler, die in Dynamics 365 for Retail zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d4131-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="d4131-114">Mit Retail kénnen Sie:</span><span class="sxs-lookup"><span data-stu-id="d4131-114">With Retail, you can:</span></span>
+ <span data-ttu-id="d4131-115">Produkte in anderen Filialen suchen.</span><span class="sxs-lookup"><span data-stu-id="d4131-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="d4131-116">Alle vorhandenen Produkte suchen.</span><span class="sxs-lookup"><span data-stu-id="d4131-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="d4131-117">Cash- und Carry-Transaktionen oder Kundenaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4131-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="d4131-118">Lieferoptionen für Kundenaufträge auswählen.</span><span class="sxs-lookup"><span data-stu-id="d4131-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="d4131-119">Produkte im aktuellen Shops oder in einer anderen Filiale abholen.</span><span class="sxs-lookup"><span data-stu-id="d4131-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="d4131-120">Eine Bestellung in der aktuellen Filiale oder in einer anderen Filiale stornieren.</span><span class="sxs-lookup"><span data-stu-id="d4131-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="d4131-121">Einen Auftrag mit oder ohne Beleg in der aktuellen Filiale oder in einer anderen Filiale zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d4131-121">Return an order with or without the receipt at the current store or another store.</span></span>

