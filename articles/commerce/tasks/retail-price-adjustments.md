---
title: " Einzelhandelspreisregulierungen"
description: Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung einer Handelspreisregulierung.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbd2f818930424313e1d76aea4a257efa7c7b3be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232784"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="e8b13-103"> Einzelhandelspreisregulierungen</span><span class="sxs-lookup"><span data-stu-id="e8b13-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8b13-104">Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung einer Handelspreisregulierung.</span><span class="sxs-lookup"><span data-stu-id="e8b13-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="e8b13-105">Eine Preisregulierung kann den Verkaufspreis eines Artikels direkt festlegen oder den Basisverkaufspreis oder Handelsvereinbarungsverkaufspreis ändern.</span><span class="sxs-lookup"><span data-stu-id="e8b13-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="e8b13-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8b13-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="e8b13-107">Klicken Sie auf Verwaltung von Preisen und Rabatten.</span><span class="sxs-lookup"><span data-stu-id="e8b13-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="e8b13-108">Klicken Sie auf die Preisregulierungsregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="e8b13-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="e8b13-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e8b13-109">Click New.</span></span>
    * <span data-ttu-id="e8b13-110">Von hier aus können Sie alle am häufigsten verwendeten Preis- und Rabattregeln erstellen, einschließlich Rabatte, Preisregulierungen, Handelsvereinbarungserfassungen und Kategoriepreiskalkulationsregeln.</span><span class="sxs-lookup"><span data-stu-id="e8b13-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="e8b13-111">Klicken Sie auf "Preisregulierung".</span><span class="sxs-lookup"><span data-stu-id="e8b13-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="e8b13-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="e8b13-113">Erweitern Sie den Abschnitt "Positionen".</span><span class="sxs-lookup"><span data-stu-id="e8b13-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="e8b13-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8b13-114">Click Add.</span></span>
    * <span data-ttu-id="e8b13-115">In vorliegenden Beispiel geben Sie "81126" im Produkt-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="e8b13-116">Geben Sie anschließend "10,0" im Feld "Rabattprozentsatz" ein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="e8b13-117">Eine Rabattprozentsatz-Typpreisregulierung reduziert einen Basisverkaufspreis oder Handelsvereinbarungsverkaufspreis.</span><span class="sxs-lookup"><span data-stu-id="e8b13-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="e8b13-118">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8b13-118">Click Add.</span></span>
    * <span data-ttu-id="e8b13-119">In vorliegenden Beispiel geben Sie "81125" im Produkt-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="e8b13-120">Anschließend wählen Sie "Skontobetrag" im Feld "Rabattmethode" aus.</span><span class="sxs-lookup"><span data-stu-id="e8b13-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="e8b13-121">Schließlich geben Sie "5,0" im Skontobetrag-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="e8b13-122">Ein Skontobetrag-Rabatttyp ist ein Betrag, der von einem Basispreis oder von einem Handelsvereinbarungs-Preis abgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="e8b13-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="e8b13-123">Klicken Sie auf "Preisgruppen".</span><span class="sxs-lookup"><span data-stu-id="e8b13-123">Click Price groups.</span></span>
    * <span data-ttu-id="e8b13-124">Wählen Sie im Feld "Preisgruppe" die Option "RP-Houston" aus.</span><span class="sxs-lookup"><span data-stu-id="e8b13-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="e8b13-125">Dieses ordnet die Preisregulierung dem Houston-Shop zu.</span><span class="sxs-lookup"><span data-stu-id="e8b13-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="e8b13-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e8b13-126">Click Save.</span></span>
11. <span data-ttu-id="e8b13-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e8b13-127">Close the page.</span></span>
12. <span data-ttu-id="e8b13-128">Wählen Sie im Feld "Status" die Option "Aktiviert" aus.</span><span class="sxs-lookup"><span data-stu-id="e8b13-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="e8b13-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e8b13-129">Click Save.</span></span>
14. <span data-ttu-id="e8b13-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e8b13-130">Close the page.</span></span>
15. <span data-ttu-id="e8b13-131">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e8b13-131">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]