---
title: "Übersicht Transportverwaltungsaufgaben"
description: "Dieses Thema enthält eine Übersicht der Transportverwaltungsfunktionen in Microsoft Dynamics 365 for Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4dc2c15d35d93d1563c866b20ad7f2bbb5c8457
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="988c5-103">Übersicht Transportverwaltungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="988c5-103">Transportation management overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="988c5-104">Dieses Thema enthält eine Übersicht der Transportverwaltungsfunktionen in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="988c5-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="988c5-105">Mit der Transportverwaltung können Sie den Transport Ihres Unternehmens verwenden und Kreditor- und Routinglösungen für ein- und ausgehende Aufträge identifizieren.</span><span class="sxs-lookup"><span data-stu-id="988c5-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="988c5-106">So können Sie beispielsweise die schnellste Route oder den günstigsten Satz für eine Lieferung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="988c5-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="988c5-107">In der folgenden Tabelle werden die wichtigsten Szenarien für die Nutzung der Transportverwaltung in Microsoft Dynamics 365 for Finance and Operations beschrieben.</span><span class="sxs-lookup"><span data-stu-id="988c5-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="988c5-108">Szenario</span><span class="sxs-lookup"><span data-stu-id="988c5-108">Scenario</span></span></th>
<th><span data-ttu-id="988c5-109">Nutzen der Transportverwaltung</span><span class="sxs-lookup"><span data-stu-id="988c5-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="988c5-110">Nutzung externer Logistikanbieter für Transportaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="988c5-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="988c5-111">Verwenden Sie die Transportverwaltung für den eingehenden und ausgehenden Transport.</span><span class="sxs-lookup"><span data-stu-id="988c5-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="988c5-112">Die eigene Flotte des Unternehmens ist für Lieferung/Abholung verfügbar, und Zustellgebühren werden an an Debitoren weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="988c5-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="988c5-113">Für ausgehende Prozesse können Sie die Transportverwaltung verwenden, um die Transportbelastungen festzulegen und sie an Debitoren weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="988c5-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="988c5-114">Allerdings ist der Spediteursrechnung-Abstimmungsprozess nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="988c5-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="988c5-115">Die eigene Flotte des Unternehmens steht für Lieferung/Abholung zur Verfügung, aber Zustellgebühren werden nicht an Debitoren weitergegeben, da Produktpreise den Transport enthalten.</span><span class="sxs-lookup"><span data-stu-id="988c5-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="988c5-116">Viele Transportverwaltungsfunktionen sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="988c5-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="988c5-117">Sie können jedoch die Transportverwaltung verwenden, um die Transportsätze zu bestimmen und den Verkaufspreis entsprechend anzupassen.</span><span class="sxs-lookup"><span data-stu-id="988c5-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="988c5-118">Logistikdienste werden von einer anderen juristischen Person im gleichen Unternehmen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="988c5-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="988c5-119">Sie können die Transportverwaltung nutzen, indem Sie die andere juristische Person wie jeden anderen Spediteur behandeln.</span><span class="sxs-lookup"><span data-stu-id="988c5-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="988c5-120">Sie können die wirtschaftlichen Buchungen zwischen juristischen Personen nicht automatisieren.</span><span class="sxs-lookup"><span data-stu-id="988c5-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="988c5-121">Daher müssen Sie diese Buchungen manuell behandeln (beispielsweise mithilfe einer Bestellung).</span><span class="sxs-lookup"><span data-stu-id="988c5-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="988c5-122">In der juristischen Person, die die Logistik zur Verfügung stellt, kann die Transportverwaltung verwendet werden, um zu bestimmen Transportsätze festzulegen.</span><span class="sxs-lookup"><span data-stu-id="988c5-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="988c5-123">Transport in Finance and Operations planen</span><span class="sxs-lookup"><span data-stu-id="988c5-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="988c5-124">In der Transportverwaltung kann die Transportplanung entweder auf Aufträgen oder auf Lieferungen basieren, die auf Basis dieser Aufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="988c5-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="988c5-125">Die Lieferungen sind immer irgendwann vorhanden. Sie sind jedoch nicht zur Transportplanung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="988c5-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="988c5-126">Umlagerungsaufträge sind Teil des ausgehenden Szenarios und können zusammen mit Aufträgen geplant werden.</span><span class="sxs-lookup"><span data-stu-id="988c5-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Auslastungabbildung](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="988c5-128">Eingehender Transport</span><span class="sxs-lookup"><span data-stu-id="988c5-128">Inbound transportation</span></span>
<span data-ttu-id="988c5-129">Wenn Sie Artikel von einem Kreditor zur Lieferung an Ihren Lagerort bestellen, möchten Sie den Transport der Artikel möglicherweise selbst organisieren.</span><span class="sxs-lookup"><span data-stu-id="988c5-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="988c5-130">Sie können Finance and Operations nutzen, um den Transport und den Empfang einer eingehenden Ladung zu planen.</span><span class="sxs-lookup"><span data-stu-id="988c5-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="988c5-131">Die folgende Abbildung zeigt den Geschäftsprozessablauf für die Planung des Transports einer eingehenen Auslastung.</span><span class="sxs-lookup"><span data-stu-id="988c5-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Geschäftsprozessfluss für den Transport eingehender Auslastungen](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="988c5-133">Ausgehender Transport</span><span class="sxs-lookup"><span data-stu-id="988c5-133">Outbound transportation</span></span>
<span data-ttu-id="988c5-134">Sie können eine ausgehende Ladung planen und verarbeiten, um bestimmte Artikel aus dem Lagerort eines Unternehmens an einen Debitor zu versenden.</span><span class="sxs-lookup"><span data-stu-id="988c5-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="988c5-135">Sie können Finance and Operations nutzen, um den Transport und den Versand einer azusgehenden Ladung zu planen.</span><span class="sxs-lookup"><span data-stu-id="988c5-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="988c5-136">Die folgende Abbildung zeigt den Geschäftsprozessablauf für die Planung und Verarbeitung von ausgehenden Ladungen für den Versand.</span><span class="sxs-lookup"><span data-stu-id="988c5-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Planung und Verarbeitung von ausgehenden Ladungen](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="988c5-138">Ladungserstellung</span><span class="sxs-lookup"><span data-stu-id="988c5-138">Load building</span></span>
<span data-ttu-id="988c5-139">Finance and Operations enthält eine Ladungserstellungsstrategie mit dem Namen "Volumenbasierte Ladungserstellungsstrategie".</span><span class="sxs-lookup"><span data-stu-id="988c5-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="988c5-140">Mit dieser Strategie können Sie die Höchstwerte verwenden, die für Höhe und Gewicht in der Ladungsvorlage angegeben sind, oder die Einstellungen überschreiben, indem sie neuen Werte eingeben.</span><span class="sxs-lookup"><span data-stu-id="988c5-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="988c5-141">Um diese Strategie zu verwenden, wählen Sie sie im Feld **Ladungserstellungsstrategie** im Inforegister **Einstellungen** auf der Seite **Ladungserstellungsworkbench** aus.</span><span class="sxs-lookup"><span data-stu-id="988c5-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="988c5-142">Darüber hinaus können Sie eigene Ladungserstellungsstrategien hinzufügen, indem Sie eine neue Klasse in der Entwicklungsumgebung erstellen.</span><span class="sxs-lookup"><span data-stu-id="988c5-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




