---
title: Artikel zu Bestellung aus Artikelbedarf empfangen
description: In diesem Thema wird erläutert, wie Sie Artikel auf einer Bestellung von einem Artikelbedarf erhalten.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: 1f288a47f952a30d98a4a5b96409dc53f880d41d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139055"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="05ca0-103">Artikel zu Bestellung aus Artikelbedarf empfangen</span><span class="sxs-lookup"><span data-stu-id="05ca0-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05ca0-104">In diesem Thema wird erläutert, wie Sie Artikel auf einer Bestellung von einem Artikelbedarf erhalten.</span><span class="sxs-lookup"><span data-stu-id="05ca0-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="05ca0-105">Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="05ca0-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="05ca0-106">Diese Aufgabe verwendet das USSI-Dataset.</span><span class="sxs-lookup"><span data-stu-id="05ca0-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="05ca0-107">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und Rechnungswesen > Projekte > Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="05ca0-108">Wählen Sie in der Liste den Link in der gewünschten Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="05ca0-109">Wählen Sie im Aktivitätsbereich **Plan** aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="05ca0-110">Wählen Sie **Artikelanforderungen**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="05ca0-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-111">Select **New**.</span></span>
6. <span data-ttu-id="05ca0-112">Geben Sie in der neuen Zeile einen Wert im Feld **Artikelnummer** ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="05ca0-113">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="05ca0-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="05ca0-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-114">Select **Save**.</span></span>
9. <span data-ttu-id="05ca0-115">Wählen Sie im Aktionsbereich **Management**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="05ca0-116">Wählen Sie **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-116">Select **Functions**.</span></span>
11. <span data-ttu-id="05ca0-117">Wählen Sie **Bestellung anlegen**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="05ca0-118">Aktivieren Sie das Kontrollkästchen **Alle einbeziehen**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="05ca0-119">Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="05ca0-120">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-120">Select **OK**.</span></span>
15. <span data-ttu-id="05ca0-121">Gehen Sie im Navigationsbereich zu **Module > Kreditorenbuchhaltung > Bestellungen > Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="05ca0-122">Wählen Sie in der Liste den Link in der gewünschten Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="05ca0-123">Wählen Sie im Aktivitätsbereich **Einkauf** aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="05ca0-124">Wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="05ca0-125">Wählen Sie im Aktivitätsbereich **Wareneingang** aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="05ca0-126">Wählen Sie **Produktzugang** aus.</span><span class="sxs-lookup"><span data-stu-id="05ca0-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="05ca0-127">Geben Sie im Feld **Produktzugang** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="05ca0-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="05ca0-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="05ca0-128">Select **OK**.</span></span>

