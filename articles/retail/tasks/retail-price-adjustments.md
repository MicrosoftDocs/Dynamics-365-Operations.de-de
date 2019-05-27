---
title: " Einzelhandelspreisregulierungen"
description: Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung einer Einzelhandelspreisregulierung.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550011"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="4d4b6-103"> Einzelhandelspreisregulierungen</span><span class="sxs-lookup"><span data-stu-id="4d4b6-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4d4b6-104">Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung einer Einzelhandelspreisregulierung.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="4d4b6-105">Eine Einzelhandelspreisregulierung kann den Verkaufspreis eines Artikels direkt festlegen oder den Basisverkaufspreis oder Handelsvereinbarungsverkaufspreis ändern.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="4d4b6-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="4d4b6-107">Klicken Sie auf Verwaltung von Preisen und Rabatten.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="4d4b6-108">Klicken Sie auf die Preisregulierungsregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="4d4b6-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4d4b6-109">Click New.</span></span>
    * <span data-ttu-id="4d4b6-110">Von hier aus können Sie alle am häufigsten verwendeten Preis- und Rabattregeln erstellen, einschließlich Einzelhandelsrabatte, Preisregulierungen, Handelsvereinbarungserfassungen und Kategoriepreiskalkulationsregeln.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="4d4b6-111">Klicken Sie auf "Preisregulierung".</span><span class="sxs-lookup"><span data-stu-id="4d4b6-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="4d4b6-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="4d4b6-113">Erweitern Sie den Abschnitt "Positionen".</span><span class="sxs-lookup"><span data-stu-id="4d4b6-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="4d4b6-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-114">Click Add.</span></span>
    * <span data-ttu-id="4d4b6-115">In vorliegenden Beispiel geben Sie "81126" im Produkt-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="4d4b6-116">Geben Sie anschließend "10,0" im Feld "Rabattprozentsatz" ein.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="4d4b6-117">Eine Rabattprozentsatz-Typpreisregulierung reduziert einen Basisverkaufspreis oder Handelsvereinbarungsverkaufspreis.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="4d4b6-118">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-118">Click Add.</span></span>
    * <span data-ttu-id="4d4b6-119">In vorliegenden Beispiel geben Sie "81125" im Produkt-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="4d4b6-120">Anschließend wählen Sie "Skontobetrag" im Feld "Rabattmethode" aus.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="4d4b6-121">Schließlich geben Sie "5,0" im Skontobetrag-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="4d4b6-122">Ein Skontobetrag-Rabatttyp ist ein Betrag, der von einem Basispreis oder von einem Handelsvereinbarungs-Preis abgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="4d4b6-123">Klicken Sie auf "Preisgruppen".</span><span class="sxs-lookup"><span data-stu-id="4d4b6-123">Click Price groups.</span></span>
    * <span data-ttu-id="4d4b6-124">Wählen Sie im Feld "Preisgruppe" die Option "RP-Houston" aus.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="4d4b6-125">Dieses ordnet die Preisregulierung dem Houston-Shop zu.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="4d4b6-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4d4b6-126">Click Save.</span></span>
11. <span data-ttu-id="4d4b6-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-127">Close the page.</span></span>
12. <span data-ttu-id="4d4b6-128">Wählen Sie im Feld "Status" die Option "Aktiviert" aus.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="4d4b6-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4d4b6-129">Click Save.</span></span>
14. <span data-ttu-id="4d4b6-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-130">Close the page.</span></span>
15. <span data-ttu-id="4d4b6-131">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4d4b6-131">Refresh the page.</span></span>

