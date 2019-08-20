---
title: Artikel zu Bestellung aus Artikelbedarf empfangen
description: Diese Prozedur zeigt, wie Artikel in einer Bestellung aus einem Artikelbedarf empfangen werden.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fee2c965b0c065f00564b849ec93504336fb3f60
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838246"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="f9693-103">Artikel zu Bestellung aus Artikelbedarf empfangen</span><span class="sxs-lookup"><span data-stu-id="f9693-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9693-104">Diese Prozedur zeigt, wie Artikel in einer Bestellung aus einem Artikelbedarf empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="f9693-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="f9693-105">Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="f9693-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="f9693-106">Diese Aufgabe verwendet das USSI-Dataset.</span><span class="sxs-lookup"><span data-stu-id="f9693-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f9693-107">Wechseln Sie zu "Projektverwaltung und -verrechnung" > "Projekte" > "Alle Projekte".</span><span class="sxs-lookup"><span data-stu-id="f9693-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="f9693-108">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9693-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f9693-109">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="f9693-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="f9693-110">Klicken Sie auf „Artikelbedarf”.</span><span class="sxs-lookup"><span data-stu-id="f9693-110">Click Item requirements.</span></span>
5. <span data-ttu-id="f9693-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f9693-111">Click New.</span></span>
6. <span data-ttu-id="f9693-112">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9693-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f9693-113">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f9693-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="f9693-114">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9693-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="f9693-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f9693-115">Click Save.</span></span>
10. <span data-ttu-id="f9693-116">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="f9693-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="f9693-117">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f9693-117">Click Functions.</span></span>
12. <span data-ttu-id="f9693-118">Klicken Sie auf „Bestellung erstellen”.</span><span class="sxs-lookup"><span data-stu-id="f9693-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="f9693-119">Aktivieren Sie das Kontrollkästchen „Einschließen”.</span><span class="sxs-lookup"><span data-stu-id="f9693-119">Select the Include check box.</span></span>
14. <span data-ttu-id="f9693-120">Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f9693-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="f9693-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f9693-121">Click OK.</span></span>
16. <span data-ttu-id="f9693-122">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="f9693-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="f9693-123">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9693-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f9693-124">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="f9693-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="f9693-125">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="f9693-125">Click Confirm.</span></span>
20. <span data-ttu-id="f9693-126">Klicken Sie im Aktivitätsbereich auf "Empfangen".</span><span class="sxs-lookup"><span data-stu-id="f9693-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="f9693-127">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="f9693-127">Click Product receipt.</span></span>
22. <span data-ttu-id="f9693-128">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9693-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="f9693-129">Geben Sie im Feld "Produktzugang" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f9693-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="f9693-130">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f9693-130">Click OK.</span></span>

