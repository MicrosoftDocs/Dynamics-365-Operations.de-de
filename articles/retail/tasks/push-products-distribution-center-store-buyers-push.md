--- 
title: " Produkte vom Verteilzentrum zu Shops mithilfe von Käuferübertragung übertragen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung einer Käuferübertragung zum Vertreiben von Produkten von einem Lagerplatz an einen oder viele Shops."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: fc14a4e013eadaa5b4b1df357f0c646ab68b6072
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="a7bee-103"> Produkte vom Verteilzentrum zu Shops mithilfe von Käuferübertragung übertragen</span><span class="sxs-lookup"><span data-stu-id="a7bee-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a7bee-104">Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung einer Käuferübertragung zum Vertreiben von Produkten von einem Lagerplatz an einen oder viele Shops.</span><span class="sxs-lookup"><span data-stu-id="a7bee-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="a7bee-105">Der Benutzer kann mehrere Varianten definieren und das System vorschlagen lassen, wie die Produkte vertrieben werden sollen, oder manuell eingeben, wo die Produkte vertrieben werden und wie viel an jeden Shop vertrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a7bee-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="a7bee-106">Das Verfahren umfasst nicht die Einrichtung von Daten, die in der Käuferübertragung verwendet werden können, wie Auffüllungsregeln, Organisationshierarchien und Shopgewichte.</span><span class="sxs-lookup"><span data-stu-id="a7bee-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="a7bee-107">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7bee-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="a7bee-108">Gehen Sie zu "Käuferübertragung".</span><span class="sxs-lookup"><span data-stu-id="a7bee-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="a7bee-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a7bee-109">Click New.</span></span>
3. <span data-ttu-id="a7bee-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a7bee-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="a7bee-111">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a7bee-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="a7bee-112">Wählen Sie im Feld "Lagerort" einen Lagerort aus (bzw. geben Sie einen ein), der Produkte mit Lagerbestandsmengen hat.</span><span class="sxs-lookup"><span data-stu-id="a7bee-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="a7bee-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a7bee-113">Click Add.</span></span>
7. <span data-ttu-id="a7bee-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a7bee-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a7bee-115">Geben Sie im Feld "Artikelnummer" ein Produkt ein oder wählen Sie ein Produkt aus.</span><span class="sxs-lookup"><span data-stu-id="a7bee-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="a7bee-116">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a7bee-116">Click Add.</span></span>
10. <span data-ttu-id="a7bee-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a7bee-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="a7bee-118">Geben Sie im Feld "Artikelnummer" eine Produktvariante ein oder wählen Sie eine Produktvariante aus.</span><span class="sxs-lookup"><span data-stu-id="a7bee-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="a7bee-119">Wenn Sie eine Produktvariante eingeben, werden Positionen für jede Variante erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7bee-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="a7bee-120">Markieren Sie in der Liste eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="a7bee-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="a7bee-121">Im Feld "Übertragene Menge" geben Sie ein, wieviel des ausgewählten Produkts Sie verteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="a7bee-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="a7bee-122">Im Feld "Zusätzliche zu übertragende Menge" geben Sie die Menge der Produkte ein, die eine verfügbare zu verteilende Menge haben.</span><span class="sxs-lookup"><span data-stu-id="a7bee-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="a7bee-123">Geben Sie im Verteilungs-Feld "Location weight" ein.</span><span class="sxs-lookup"><span data-stu-id="a7bee-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="a7bee-124">Sie können die anderen Typen auswählen, um andere Regeln für die Verteilung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7bee-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="a7bee-125">Wählen Sie im Feld "Auffüllungshierarchie" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a7bee-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="a7bee-126">Wählen Sie "Ja" im Feld "Sortimente berücksichtigen" aus.</span><span class="sxs-lookup"><span data-stu-id="a7bee-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="a7bee-127">Klicken Sie auf "Mengen berechnen" und überprüfen Sie die Mengen, die zu den Zeilen im Lagerortabschnitt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a7bee-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="a7bee-128">Klicken Sie auf "Auftrag erstellen".</span><span class="sxs-lookup"><span data-stu-id="a7bee-128">Click Create order.</span></span>
20. <span data-ttu-id="a7bee-129">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a7bee-129">Click Yes.</span></span>


