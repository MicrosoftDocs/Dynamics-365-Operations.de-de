---
title: " Produktpakete für Bestellungen erstellen"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c84c829ca1344d70dee294da35b659299d6fa37
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802718"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="be7cd-103"> Produktpakete für Bestellungen erstellen</span><span class="sxs-lookup"><span data-stu-id="be7cd-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be7cd-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung.</span><span class="sxs-lookup"><span data-stu-id="be7cd-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="be7cd-105">Die Bestellung wird verwendet, um einen Auftrag für einen vordefinierten Satz Produkte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="be7cd-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="be7cd-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="be7cd-107">Erstellen eines Produktpakets</span><span class="sxs-lookup"><span data-stu-id="be7cd-107">Create a product package</span></span>
1. <span data-ttu-id="be7cd-108">Navigieren Sie zu Einzelhandel und Handel > Lagerverwaltung > Wiederbeschaffung > Produktpakete.</span><span class="sxs-lookup"><span data-stu-id="be7cd-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="be7cd-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="be7cd-109">Click New.</span></span>
3. <span data-ttu-id="be7cd-110">Geben Sie im Feld "Paketnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="be7cd-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="be7cd-112">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="be7cd-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="be7cd-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="be7cd-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-114">Click Add.</span></span>
8. <span data-ttu-id="be7cd-115">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0160" ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="be7cd-116">Klicken Sie im Feld "Größe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="be7cd-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="be7cd-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="be7cd-118">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="be7cd-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-119">Click Add.</span></span>
13. <span data-ttu-id="be7cd-120">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0160" ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="be7cd-121">Klicken Sie im Feld "Variantennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="be7cd-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="be7cd-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="be7cd-123">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="be7cd-124">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-124">Click Add.</span></span>
18. <span data-ttu-id="be7cd-125">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0175" ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="be7cd-126">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="be7cd-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="be7cd-127">Click Save.</span></span>
21. <span data-ttu-id="be7cd-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="be7cd-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="be7cd-129">Hinzufügen eines Pakets zur Bestellung</span><span class="sxs-lookup"><span data-stu-id="be7cd-129">Add package to purchase order</span></span>
1. <span data-ttu-id="be7cd-130">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="be7cd-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="be7cd-131">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="be7cd-131">Click New.</span></span>
3. <span data-ttu-id="be7cd-132">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="be7cd-133">Wählen Sie in der Liste den gleichen Kreditor aus, für den das Produktpaket zuvor erstellt wurde, wenn ein Kreditor ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="be7cd-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="be7cd-134">Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="be7cd-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="be7cd-135">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="be7cd-136">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="be7cd-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="be7cd-137">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="be7cd-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="be7cd-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="be7cd-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="be7cd-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="be7cd-139">Click OK.</span></span>
11. <span data-ttu-id="be7cd-140">Schalten Sie die Erweiterung des Abschnitts "Positionsdetails" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="be7cd-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="be7cd-141">Klicken Sie auf die Produktpaketregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="be7cd-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="be7cd-142">Klicken Sie auf die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="be7cd-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="be7cd-143">Klicken Sie auf "Positionen aus Paket erstellen".</span><span class="sxs-lookup"><span data-stu-id="be7cd-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="be7cd-144">Wählen Sie in der Liste das Produktpaket aus, das im vorherigen Schritt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="be7cd-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="be7cd-145">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="be7cd-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="be7cd-146">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="be7cd-146">Click Create.</span></span>
18. <span data-ttu-id="be7cd-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="be7cd-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]