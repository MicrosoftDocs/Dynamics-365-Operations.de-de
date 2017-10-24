---
title: Shop-Lagerbestand verwalten
description: "Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="c1d49-103">Shop-Lagerbestand verwalten</span><span class="sxs-lookup"><span data-stu-id="c1d49-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c1d49-104">Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c1d49-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="c1d49-105">Sie können die folgenden Typen von Dokumenten verwenden, um den Lagerbestand der Organisation zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c1d49-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="c1d49-106">Bestellungen</span><span class="sxs-lookup"><span data-stu-id="c1d49-106">Purchase orders</span></span>
<span data-ttu-id="c1d49-107">Bestellungen werden in der Zentrale erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="c1d49-108">Wenn ein Einzelhandelslagerort im Bestellkopf enthalten ist, kann der Auftrag im Shop mithilfe von Modern POS (MPOS) oder Cloud POS in Microsoft Dynamics 365 for Retail empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="c1d49-109">Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="c1d49-110">Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="c1d49-111">In der Zentrale werden die Mengen, die im Shop eingegangen sind, in Microsoft Dynamics 365 for Retail im Feld **Aktuelle Lieferung** auf der Bestellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="c1d49-112">Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="c1d49-112">Transfer orders</span></span>
<span data-ttu-id="c1d49-113">Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, von dem Artikel versendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c1d49-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="c1d49-114">In diesem Fall wird der Umlagerungsauftrag im Shop als Kommissionierungsanfrage in MPOS oder Cloud POS angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="c1d49-115">Nachdem die angeforderten Mengen entnommen wurden, werden sie kommissioniert und an die Zentrale gesendet.</span><span class="sxs-lookup"><span data-stu-id="c1d49-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="c1d49-116">In der Zentrale werden die Mengen, die im Shop entnommen wurden, in Microsoft Dynamics 365 for Retail im Feld **Jetzt liefern** des Umlagerungsauftrags angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="c1d49-117">Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, an den Artikel versendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c1d49-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="c1d49-118">In diesem Fall wird der Umlagerungsauftrag im Shop als Eingangsanforderung in MPOS oder Cloud POS angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="c1d49-119">Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="c1d49-120">Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="c1d49-121">In der Zentrale werden die Mengen, die im Shop eingegangen sind, in Microsoft Dynamics 365 for Retail im Feld **Aktuelle Lieferung** im Umlagerungsauftrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="c1d49-122">Bestandsmengen</span><span class="sxs-lookup"><span data-stu-id="c1d49-122">Stock counts</span></span>
<span data-ttu-id="c1d49-123">Bestandsmengen können entweder geplant oder ungeplant sein.</span><span class="sxs-lookup"><span data-stu-id="c1d49-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="c1d49-124">Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt.</span><span class="sxs-lookup"><span data-stu-id="c1d49-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="c1d49-125">Von der Zentrale wird ein Inventurdokument erstellt, das im Shop empfangen werden kann und in dem die tatsächlich verfügbaren Mengen in MPOS oder Cloud POS eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="c1d49-126">Ungeplante Bestandsmengen werden in einem Shop initiiert, und die Mengen des tatsächlich verfügbaren Lagerbestands werden in MPOS oder Cloud POS aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1d49-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="c1d49-127">Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln.</span><span class="sxs-lookup"><span data-stu-id="c1d49-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="c1d49-128">Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet.</span><span class="sxs-lookup"><span data-stu-id="c1d49-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="c1d49-129">In der Zentrale wird die Bestandsmenge geprüft und gebucht.</span><span class="sxs-lookup"><span data-stu-id="c1d49-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="c1d49-130">Bestandsuche</span><span class="sxs-lookup"><span data-stu-id="c1d49-130">Inventory lookup</span></span>
<span data-ttu-id="c1d49-131">Die aktuelle Produktmenge für Mehrfachshops und Lagerorte kann auf der Bestandssuchenseite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="c1d49-132">Neben der aktuellen verfügbaren Menge können auch künftige Verfügbarkeitszusagen-Mengen (ATP) für jede einzelne Filiale angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c1d49-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="c1d49-133">Klicken Sie hierfür auf die Filiale, für die Sie die VfZ für anzeigen möchten, und klicken Sie auf **Verfügbarkeit in Filiale anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="c1d49-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





