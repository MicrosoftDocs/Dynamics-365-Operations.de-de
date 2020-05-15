---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Commerce
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335275"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="77edc-103">Entfernte oder veraltete Funktionen in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="77edc-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77edc-104">In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="77edc-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="77edc-105">Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77edc-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="77edc-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="77edc-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="77edc-107">Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="77edc-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="77edc-108">Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="77edc-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="77edc-109">Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="77edc-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="77edc-110">Entfernte oder veraltete Funktionen in Commerce Version 10.0.10</span><span class="sxs-lookup"><span data-stu-id="77edc-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="77edc-111">POS-Vorgang 803 – Entnahme und Empfang</span><span class="sxs-lookup"><span data-stu-id="77edc-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="77edc-112">**Grund für veralteten Zustand/Entfernung**</span><span class="sxs-lookup"><span data-stu-id="77edc-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="77edc-113">Entnahme- und Empfangsvorgänge werden veraltet, aufgrund der Neugestaltung des neuen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="77edc-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="77edc-114">**Ersetzt durch eine andere Funktion?**</span><span class="sxs-lookup"><span data-stu-id="77edc-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="77edc-115">Ja.</span><span class="sxs-lookup"><span data-stu-id="77edc-115">Yes.</span></span> <span data-ttu-id="77edc-116">Er wird durch zwei neue POS-Vorgänge ersetzt: Eingangsvorgang (804) und Ausgangsvorgang (805).</span><span class="sxs-lookup"><span data-stu-id="77edc-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="77edc-117">**Betroffene Produktbereiche**</span><span class="sxs-lookup"><span data-stu-id="77edc-117">**Product areas affected**</span></span>         | <span data-ttu-id="77edc-118">Verkaufsstellen-(POS)-Anwendung</span><span class="sxs-lookup"><span data-stu-id="77edc-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="77edc-119">**Bereitstellungsoption**</span><span class="sxs-lookup"><span data-stu-id="77edc-119">**Deployment option**</span></span>              | <span data-ttu-id="77edc-120">Alle</span><span class="sxs-lookup"><span data-stu-id="77edc-120">All</span></span> |
| <span data-ttu-id="77edc-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="77edc-121">**Status**</span></span>                         | <span data-ttu-id="77edc-122">Veraltet: Ab Version 10.0.10 erhält der Entnahme- und Empfangsvorgang keine neuen Funktionsupdates mehr.</span><span class="sxs-lookup"><span data-stu-id="77edc-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="77edc-123">Nur kritische Fehlerbehebungen werden für diesen Vorgang in zukünftigen Versionen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="77edc-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="77edc-124">Alle Kunden werden aufgefordert, auf die neuen [Eingehenden Vorgänge](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) und [Ausgehenden Vorgänge](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) zu wechseln, die weiterhin Teil unserer langfristigen Produkt-Roadmap sein werden.</span><span class="sxs-lookup"><span data-stu-id="77edc-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="77edc-125">Entfernte oder veraltete Funktionen in Commerce Version 10.0.7</span><span class="sxs-lookup"><span data-stu-id="77edc-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="77edc-126">Commerce GetProductAvailabilities und GetAvailableInventoryNearby-APIs</span><span class="sxs-lookup"><span data-stu-id="77edc-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="77edc-127">**Grund für veralteten Zustand/Entfernung**</span><span class="sxs-lookup"><span data-stu-id="77edc-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="77edc-128">Neue optimierte APIs sind erstellt worden, um die GetProductAvailabilities und GetAvailableInventoryNearby-APIs zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="77edc-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="77edc-129">**Ersetzt durch eine andere Funktion?**</span><span class="sxs-lookup"><span data-stu-id="77edc-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="77edc-130">Ja: Es wird durch GetEstimatedAvailability- und GetEstimatedProductWarehouseAvailability-APIs ersetzt.</span><span class="sxs-lookup"><span data-stu-id="77edc-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="77edc-131">**Betroffene Produktbereiche**</span><span class="sxs-lookup"><span data-stu-id="77edc-131">**Product areas affected**</span></span>         | <span data-ttu-id="77edc-132">E-Commerce-Anwendung SDK</span><span class="sxs-lookup"><span data-stu-id="77edc-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="77edc-133">**Bereitstellungsoption**</span><span class="sxs-lookup"><span data-stu-id="77edc-133">**Deployment option**</span></span>              | <span data-ttu-id="77edc-134">Alle</span><span class="sxs-lookup"><span data-stu-id="77edc-134">All</span></span> |
| <span data-ttu-id="77edc-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="77edc-135">**Status**</span></span>                         | <span data-ttu-id="77edc-136">Veraltet: Ab Version 10.0.7 werden keine technischen Investitionen mehr für GetProductAvailabilities und GetAvailableInventoryNearby getätigt.</span><span class="sxs-lookup"><span data-stu-id="77edc-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="77edc-137">Organisationen, die diese APIs in ihren E-Commerce-Bereitstellungen verwenden, sollten zu den neuen GetEstimatedAvailability- und GetEstimatedProductWarehouseAvailability-APIs wechseln und die [Optimierte Funktion zur Berechnung der Produktverfügbarkeit](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="77edc-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="77edc-138">Frühere Ankündigungen über entfernte oder veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="77edc-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="77edc-139">Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="77edc-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
