--- 
title: Den Warenzugang auf der Bestellung erfassen
description: Diese Prozedur zeigt Ihnen an, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="1ca28-103">Den Warenzugang auf der Bestellung erfassen</span><span class="sxs-lookup"><span data-stu-id="1ca28-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ca28-104">Diese Prozedur zeigt Ihnen an, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="1ca28-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="1ca28-105">Es ist auch möglich, den Produktzugang im Lagerort zu erfassen und ihn dann später auf der Bestellung aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="1ca28-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="1ca28-106">Diese Aufgabe wird gewöhnlich von einem Einkäufer oder einem Kreditorenkontenkoordinator ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ca28-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="1ca28-107">Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ca28-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="1ca28-108">Das Beispiel umfasst Schritte, um eine einfache Bestellung zu erstellen, damit Sie die Prozedur als Aufgabenleitfaden wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="1ca28-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="1ca28-109">Wenn Sie die Prozedur mit Ihren eigenen Daten verwendeten, würden Sie bei der Unteraufgabe "Warenzugang erfassen" beginnen.</span><span class="sxs-lookup"><span data-stu-id="1ca28-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="1ca28-110">Eine neue Bestellung für den Warenzugang vorbereiten</span><span class="sxs-lookup"><span data-stu-id="1ca28-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="1ca28-111">Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="1ca28-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="1ca28-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1ca28-112">Click New.</span></span>
3. <span data-ttu-id="1ca28-113">Geben Sie im Feld "Kreditorenkonto" den Wert US-101 ein.</span><span class="sxs-lookup"><span data-stu-id="1ca28-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="1ca28-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ca28-114">Click OK.</span></span>
5. <span data-ttu-id="1ca28-115">Geben Sie im Feld "Artikelnummer" den Wert M0001 ein.</span><span class="sxs-lookup"><span data-stu-id="1ca28-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="1ca28-116">Geben Sie im Feld "Menge" den Wert "5" ein.</span><span class="sxs-lookup"><span data-stu-id="1ca28-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="1ca28-117">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="1ca28-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="1ca28-118">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="1ca28-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="1ca28-119">Warenzugang erfassen</span><span class="sxs-lookup"><span data-stu-id="1ca28-119">Record receipt of goods</span></span>
1. <span data-ttu-id="1ca28-120">Klicken Sie im Aktivitätsbereich auf "Empfangen".</span><span class="sxs-lookup"><span data-stu-id="1ca28-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="1ca28-121">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="1ca28-121">Click Product receipt.</span></span>
    * <span data-ttu-id="1ca28-122">Das Feld "Menge" ermöglicht es Ihnen, verschiedene Optionen für die Menge auszuwählen, die Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="1ca28-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="1ca28-123">Zum Beispiel wenn eine Menge vorher im Lagerort registriert worden ist, können Sie "Erfasste Menge" auswählen.</span><span class="sxs-lookup"><span data-stu-id="1ca28-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="1ca28-124">Für dieses Beispiel verwenden Sie den Wert "Bestellte Menge".</span><span class="sxs-lookup"><span data-stu-id="1ca28-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="1ca28-125">Geben Sie im Feld "Produktzugang" irgendeinen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1ca28-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="1ca28-126">Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ca28-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="1ca28-127">Erweitern Sie den Abschnitt "Positionen".</span><span class="sxs-lookup"><span data-stu-id="1ca28-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="1ca28-128">Legen Sie die Menge auf "4" fest.</span><span class="sxs-lookup"><span data-stu-id="1ca28-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="1ca28-129">Hier sind Sie in der Lage, die Menge manuell zu anzugeben, die für jede Position zum Auftrag empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="1ca28-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="1ca28-130">Reduzieren Sie den Abschnitt "Positionen".</span><span class="sxs-lookup"><span data-stu-id="1ca28-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="1ca28-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1ca28-131">Click OK.</span></span>
    * <span data-ttu-id="1ca28-132">Die Waren sind jetzt auf der Bestellung als empfangen erfasst worden und eine Produktzugangserfassung ist als Dokument, um dies widerzuspiegeln, erstellt worden.</span><span class="sxs-lookup"><span data-stu-id="1ca28-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="1ca28-133">Sie können die Aktivität "Produktzugang" verwenden, um die Erfassungen zu überprüfen, die mit der Bestellung erstellt wurden und um zu sehen, was wann empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1ca28-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


