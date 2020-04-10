---
title: " Produktpakete für Bestellungen erstellen"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141361"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="69aa1-103"> Produktpakete für Bestellungen erstellen</span><span class="sxs-lookup"><span data-stu-id="69aa1-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69aa1-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung.</span><span class="sxs-lookup"><span data-stu-id="69aa1-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="69aa1-105">Die Bestellung wird verwendet, um einen Auftrag für einen vordefinierten Satz Produkte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="69aa1-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="69aa1-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="69aa1-107">Erstellen eines Produktpakets</span><span class="sxs-lookup"><span data-stu-id="69aa1-107">Create a product package</span></span>
1. <span data-ttu-id="69aa1-108">Navigieren Sie zu Retail und Commerce > Lagerverwaltung > Wiederbeschaffung > Produktpakete.</span><span class="sxs-lookup"><span data-stu-id="69aa1-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="69aa1-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="69aa1-109">Click New.</span></span>
3. <span data-ttu-id="69aa1-110">Geben Sie im Feld "Paketnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="69aa1-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="69aa1-112">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="69aa1-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="69aa1-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="69aa1-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-114">Click Add.</span></span>
8. <span data-ttu-id="69aa1-115">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0160" ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="69aa1-116">Klicken Sie im Feld "Größe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="69aa1-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="69aa1-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="69aa1-118">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="69aa1-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-119">Click Add.</span></span>
13. <span data-ttu-id="69aa1-120">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0160" ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="69aa1-121">Klicken Sie im Feld "Variantennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="69aa1-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="69aa1-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="69aa1-123">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="69aa1-124">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-124">Click Add.</span></span>
18. <span data-ttu-id="69aa1-125">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0175" ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="69aa1-126">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="69aa1-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="69aa1-127">Click Save.</span></span>
21. <span data-ttu-id="69aa1-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="69aa1-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="69aa1-129">Hinzufügen eines Pakets zur Bestellung</span><span class="sxs-lookup"><span data-stu-id="69aa1-129">Add package to purchase order</span></span>
1. <span data-ttu-id="69aa1-130">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="69aa1-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="69aa1-131">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="69aa1-131">Click New.</span></span>
3. <span data-ttu-id="69aa1-132">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="69aa1-133">Wählen Sie in der Liste den gleichen Kreditor aus, für den das Produktpaket zuvor erstellt wurde, wenn ein Kreditor ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="69aa1-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="69aa1-134">Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="69aa1-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="69aa1-135">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="69aa1-136">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="69aa1-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="69aa1-137">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69aa1-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="69aa1-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="69aa1-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="69aa1-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="69aa1-139">Click OK.</span></span>
11. <span data-ttu-id="69aa1-140">Schalten Sie die Erweiterung des Abschnitts "Positionsdetails" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="69aa1-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="69aa1-141">Klicken Sie auf die Produktpaketregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="69aa1-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="69aa1-142">Klicken Sie auf die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="69aa1-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="69aa1-143">Klicken Sie auf "Positionen aus Paket erstellen".</span><span class="sxs-lookup"><span data-stu-id="69aa1-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="69aa1-144">Wählen Sie in der Liste das Produktpaket aus, das im vorherigen Schritt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="69aa1-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="69aa1-145">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="69aa1-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="69aa1-146">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="69aa1-146">Click Create.</span></span>
18. <span data-ttu-id="69aa1-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="69aa1-147">Click Save.</span></span>

