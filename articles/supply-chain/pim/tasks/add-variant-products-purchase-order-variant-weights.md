---
title: Verschiedene Produkte zu Bestellungen unter Verwendung der verschiedenen Gewichte hinzufügen
description: Diese Prozedur führt Sie Schritt für Schritt durch die Verwendung von Gewichtsvarianten zum automatischen Auffüllen von Bestellpositionen für jede Variante eines Produkts.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adb2300e51f8b5383eee4dea0dffe4129dc8a536
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934816"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="651e6-103">Verschiedene Produkte zu Bestellungen unter Verwendung der verschiedenen Gewichte hinzufügen</span><span class="sxs-lookup"><span data-stu-id="651e6-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="651e6-104">Diese Prozedur führt Sie Schritt für Schritt durch die Verwendung von Gewichtsvarianten zum automatischen Auffüllen von Bestellpositionen für jede Variante eines Produkts.</span><span class="sxs-lookup"><span data-stu-id="651e6-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="651e6-105">Wenn Sie die Menge des Produkts auswählen, das Sie kaufen möchten, werden Bestellpositionen für alle Varianten des Produkts mit vorgeschlagenen Mengen auf Grundlage das Gewicht erstellt, die für die Produktvarianten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="651e6-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="651e6-106">Diese Prozedur umfasst keine Schritte zum Konfigurieren von Gewichtswerten für Produktdimensionen und Produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="651e6-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="651e6-107">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="651e6-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="651e6-108">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="651e6-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="651e6-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="651e6-109">Click New.</span></span>
3. <span data-ttu-id="651e6-110">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="651e6-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="651e6-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="651e6-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="651e6-112">Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="651e6-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="651e6-113">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="651e6-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="651e6-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="651e6-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="651e6-115">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="651e6-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="651e6-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="651e6-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="651e6-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="651e6-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="651e6-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="651e6-118">Click OK.</span></span>
12. <span data-ttu-id="651e6-119">Schalten Sie die Erweiterung des Abschnitts "Positionsdetails" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="651e6-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="651e6-120">Klicken Sie auf die Registerkarte "Varianten".</span><span class="sxs-lookup"><span data-stu-id="651e6-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="651e6-121">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="651e6-121">Click Add line.</span></span>
15. <span data-ttu-id="651e6-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="651e6-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="651e6-123">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0140" ein.</span><span class="sxs-lookup"><span data-stu-id="651e6-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="651e6-124">Legen Sie die Menge auf "1000" fest.</span><span class="sxs-lookup"><span data-stu-id="651e6-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="651e6-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="651e6-125">Click Save.</span></span>

