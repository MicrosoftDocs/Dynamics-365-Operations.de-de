--- 
title: "Überprüfung der Bestandsverfügbarkeit"
description: "Diese Prozedur zeigt Ihnen, wie Sie verfügbaren und physisch verfügbaren Lagerbestand für eine bestimmte Artikelnummer überprüfen."
author: 
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: 
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4be343a38f3f428261cf30c5b92c7a34d1f1ffa4
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="9db01-103">Überprüfung der Bestandsverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="9db01-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9db01-104">Diese Prozedur zeigt Ihnen, wie Sie verfügbaren und physisch verfügbaren Lagerbestand für eine bestimmte Artikelnummer überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9db01-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="9db01-105">Darüber hinaus zeigt sie Ihnen, wie Sie Lieferinformationen zu einem Artikel abrufen.</span><span class="sxs-lookup"><span data-stu-id="9db01-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="9db01-106">Physischer, verfügbare Lagerbestand ist der verfügbare Lagerbestand, der verfügbar ist – d. h. er ist gekauft, empfangen und erfasst worden.</span><span class="sxs-lookup"><span data-stu-id="9db01-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="9db01-107">Der verfügbare Lagerbestand umfasst den verfügbaren Lagerbestand, aber auch den Lagerbestand, der bestellt wurde und erwartet wird, der aber noch nicht empfangen oder erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="9db01-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="9db01-108">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="9db01-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="9db01-109">Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9db01-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="9db01-110">Diese Aufgaben werden normalerweise von einer Lagerarbeitskraft ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9db01-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="9db01-111">Verfügbaren Lagerbestand für einen Artikel überprüfen</span><span class="sxs-lookup"><span data-stu-id="9db01-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="9db01-112">Wechseln Sie zu "Lagerverwaltung" > "Abfragen und Berichte" > "Verfügbarer Lagerbestand".</span><span class="sxs-lookup"><span data-stu-id="9db01-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="9db01-113">Wählen Sie die "Artikelnummerzeile" aus.</span><span class="sxs-lookup"><span data-stu-id="9db01-113">Select the Item number row.</span></span>
    * <span data-ttu-id="9db01-114">Um den verfügbaren Lagerbestand nach Artikelnummer abzufragen, wählen Sie die Zeile aus, in der die "Tabelle" auf "Verfügbarer Lagerbestand" und "Feld" auf "Artikelnummer" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9db01-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="9db01-115">Wählen Sie im Feld "Kriterien" den Artikel aus, den Sie abfragen möchten.</span><span class="sxs-lookup"><span data-stu-id="9db01-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="9db01-116">Wenn Sie das USMF-Demodatunternehmen verwenden, können Sie "M9201" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9db01-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="9db01-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9db01-117">Click OK.</span></span>
5. <span data-ttu-id="9db01-118">Klicken Sie auf "Dimensionen".</span><span class="sxs-lookup"><span data-stu-id="9db01-118">Click Dimensions.</span></span>
    * <span data-ttu-id="9db01-119">Die Registerkarte "Dimensionen" ermöglicht es Ihnen auszuwählen, wie viel Detail Sie über Ihren verfügbaren Lagerbestand sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="9db01-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="9db01-120">Wenn Sie die Daten benötigen, die der Reservierung zugeordnet sind, müssen Sie alle Lagerbestandsdimensionen für die Artikel anzeigen, die erweiterte Lagerortprozesse verwenden.</span><span class="sxs-lookup"><span data-stu-id="9db01-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="9db01-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9db01-121">Click OK.</span></span>
7. <span data-ttu-id="9db01-122">Klicken Sie im Aktivitätsbereich auf "Zugehörige Informationen".</span><span class="sxs-lookup"><span data-stu-id="9db01-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="9db01-123">Wenn Sie das nicht sehen, müssen Sie möglicherweise auf der Schaltfläche "Auslassungspunkte" (...) klicken, um zusätzliche Aktionsbereichsoptionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9db01-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="9db01-124">Klicken Sie auf "Lieferübersicht".</span><span class="sxs-lookup"><span data-stu-id="9db01-124">Click Supply overview.</span></span>
    * <span data-ttu-id="9db01-125">Die Registerkarte "Lieferübersicht" stellt Lieferinformationen für einen bestimmten Artikel bereit, beispielsweise die verfügbare Menge, die Durchlaufzeit und die Kreditordaten.</span><span class="sxs-lookup"><span data-stu-id="9db01-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="9db01-126">Erweitern Sie den Abschnitt "Verfügbar".</span><span class="sxs-lookup"><span data-stu-id="9db01-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="9db01-127">Erweitern Sie den Abschnitt "Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="9db01-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="9db01-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9db01-128">Close the page.</span></span>
12. <span data-ttu-id="9db01-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9db01-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="9db01-130">Physischen Lagerbestand überprüfen</span><span class="sxs-lookup"><span data-stu-id="9db01-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="9db01-131">Wechseln Sie zu "Lagerortverwaltung" > "Abfragen und Berichte" > "Physischer Lagerbestand".</span><span class="sxs-lookup"><span data-stu-id="9db01-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="9db01-132">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9db01-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9db01-133">Sie können die Felder "Standort" und "Lagerort" verwenden, um die Liste der Artikel zu filtern.</span><span class="sxs-lookup"><span data-stu-id="9db01-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="9db01-134">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9db01-134">Refresh the page.</span></span>
4. <span data-ttu-id="9db01-135">Klicken Sie auf "Dimensionen anzeigen".</span><span class="sxs-lookup"><span data-stu-id="9db01-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="9db01-136">Die Registerkarte "Dimensionsanzeige" ermöglicht es Ihnen auszuwählen, wie viel Detail Sie über Ihren verfügbaren Lagerbestand sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="9db01-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="9db01-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9db01-137">Click OK.</span></span>
6. <span data-ttu-id="9db01-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9db01-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="9db01-139">Verfügbaren Lagerbestand nach Lagerplatz überprüfen</span><span class="sxs-lookup"><span data-stu-id="9db01-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="9db01-140">Wechseln Sie zu "Lagerortverwaltung" > "Abfragen und Berichte" > "Verfügbar nach Lagerplatz".</span><span class="sxs-lookup"><span data-stu-id="9db01-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="9db01-141">Geben Sie im Feld "Lagerort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9db01-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="9db01-142">Wenn Sie das USMF-Demodatunternehmen verwenden, können Sie "51 " verwenden.</span><span class="sxs-lookup"><span data-stu-id="9db01-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="9db01-143">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9db01-143">Refresh the page.</span></span>
4. <span data-ttu-id="9db01-144">Klicken Sie auf "Dimensionen anzeigen".</span><span class="sxs-lookup"><span data-stu-id="9db01-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="9db01-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9db01-145">Click OK.</span></span>
6. <span data-ttu-id="9db01-146">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9db01-146">Close the page.</span></span>


