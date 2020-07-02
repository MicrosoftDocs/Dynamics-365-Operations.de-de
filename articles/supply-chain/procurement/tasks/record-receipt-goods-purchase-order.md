---
title: Den Warenzugang auf der Bestellung erfassen
description: In diesem Thema wird erläutert, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa4043aca2e53eae32256a98d556c25b4ec1957
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454786"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="16197-103">Den Warenzugang auf der Bestellung erfassen</span><span class="sxs-lookup"><span data-stu-id="16197-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16197-104">In diesem Thema wird erläutert, wie der Zugang von Waren direkt auf einer Bestellung erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="16197-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="16197-105">Es ist auch möglich, den Produktzugang im Lagerort zu erfassen und ihn dann später auf der Bestellung aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="16197-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="16197-106">Diese Aufgabe wird gewöhnlich von einem Einkäufer oder einem Kreditorenkontenkoordinator ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16197-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="16197-107">Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16197-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="16197-108">Das Beispiel umfasst Schritte, um eine einfache Bestellung zu erstellen, damit Sie die Prozedur als Aufgabenleitfaden wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="16197-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="16197-109">Wenn Sie die Prozedur mit Ihren eigenen Daten verwenden, müssen Sie bei der Unteraufgabe **Warenzugang erfassen** beginnen.</span><span class="sxs-lookup"><span data-stu-id="16197-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="16197-110">Eine neue Bestellung für den Warenzugang vorbereiten</span><span class="sxs-lookup"><span data-stu-id="16197-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="16197-111">Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Bestellungen > Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="16197-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="16197-112">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="16197-112">Select **New**.</span></span>
3. <span data-ttu-id="16197-113">Geben Sie im Feld **Kreditorenkonto** den Wert `US-101` ein.</span><span class="sxs-lookup"><span data-stu-id="16197-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="16197-114">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="16197-114">Select **OK**.</span></span>
5. <span data-ttu-id="16197-115">Geben Sie im Feld **Artikelnummer** den Wert `M0001` ein.</span><span class="sxs-lookup"><span data-stu-id="16197-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="16197-116">Geben Sie im Feld **Menge** den Wert `5` ein.</span><span class="sxs-lookup"><span data-stu-id="16197-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="16197-117">Wählen Sie im Aktivitätsbereich **Einkauf** aus.</span><span class="sxs-lookup"><span data-stu-id="16197-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="16197-118">Wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="16197-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="16197-119">Warenzugang erfassen</span><span class="sxs-lookup"><span data-stu-id="16197-119">Record receipt of goods</span></span>
1. <span data-ttu-id="16197-120">Wählen Sie im Aktivitätsbereich **Wareneingang** aus.</span><span class="sxs-lookup"><span data-stu-id="16197-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="16197-121">Wählen Sie **Produktzugang** aus.</span><span class="sxs-lookup"><span data-stu-id="16197-121">Select **Product receipt**.</span></span> <span data-ttu-id="16197-122">Das Feld **Menge** ermöglicht es Ihnen, verschiedene Optionen für die Menge auszuwählen, die Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="16197-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="16197-123">Zum Beispiel wenn eine Menge vorher im Lagerort registriert worden ist, können Sie **Erfasste Menge** auswählen.</span><span class="sxs-lookup"><span data-stu-id="16197-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="16197-124">Für dieses Beispiel verwenden Sie den Wert **Bestellte Menge**.</span><span class="sxs-lookup"><span data-stu-id="16197-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="16197-125">Erweitern Sie den Abschnitt **Übersicht**.</span><span class="sxs-lookup"><span data-stu-id="16197-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="16197-126">Geben Sie im Feld **Produktzugang** irgendeinen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="16197-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="16197-127">Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16197-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="16197-128">Erweitern Sie den Abschnitt **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="16197-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="16197-129">Legen Sie **Menge** auf „4“ fest.</span><span class="sxs-lookup"><span data-stu-id="16197-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="16197-130">Hier sind Sie in der Lage, die Menge manuell zu anzugeben, die für jede Position zum Auftrag empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="16197-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="16197-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="16197-131">Select **OK**.</span></span> <span data-ttu-id="16197-132">Die Waren sind jetzt auf der Bestellung als empfangen erfasst worden und eine Produktzugangserfassung ist als Dokument, um dies widerzuspiegeln, erstellt worden.</span><span class="sxs-lookup"><span data-stu-id="16197-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="16197-133">Sie können die Aktivität "Produktzugang" verwenden, um die Erfassungen zu überprüfen, die mit der Bestellung erstellt wurden und um zu sehen, was wann empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="16197-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

