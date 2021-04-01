---
title: Konsolidierte Chargenaufträge
description: Dieser Artikel beschreibt das Konzept der konsolidierten Chargenaufträgen.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed722ba0c79afa038f1af7b4491f3ff18b052067
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246380"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="0f986-103">Konsolidierte Chargenaufträge</span><span class="sxs-lookup"><span data-stu-id="0f986-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f986-104">Dieser Artikel beschreibt das Konzept der konsolidierten Chargenaufträgen.</span><span class="sxs-lookup"><span data-stu-id="0f986-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="0f986-105">Ein produzierter Sammelartikel wird als übergeordneter Artikel angesehen, und ein verpackter Artikel ist ein untergeordneter Artikel.</span><span class="sxs-lookup"><span data-stu-id="0f986-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="0f986-106">Die Beziehung zwischen dem Sammelartikel und dem verpackten Artikel wird in einer Konvertierung von Sammelartikeln ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="0f986-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="0f986-107">Diese Konvertierung von Sammelartikeln wird im Sammelartikel selbst definiert.</span><span class="sxs-lookup"><span data-stu-id="0f986-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="0f986-108">Verpackte Artikel können Containern entweder der gleichen Größe oder mit mehreren Größen verpackt werden, die als eine Einheit eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="0f986-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="0f986-109">Indem Sie die Aufträge für einen Sammelartikel konsolidieren, können Sie alle zugehörigen Chargenaufträge in einer einzigen Ansicht anzeigen, mit deren Hilfe Sie noch verbleibende Arbeit leichter ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="0f986-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="0f986-110">Ein konsolidierter Chargenauftrag kann eine beliebige Kombination der folgenden Aufträge enthalten:</span><span class="sxs-lookup"><span data-stu-id="0f986-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="0f986-111">Einzelner Sammelauftrag und mehrere Verpackungsaufträge</span><span class="sxs-lookup"><span data-stu-id="0f986-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="0f986-112">Mehrere Sammelaufträge und mehrere Verpackungsaufträge</span><span class="sxs-lookup"><span data-stu-id="0f986-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="0f986-113">Mehrere Sammelaufträge und ein einzelner Verpackungsauftrag</span><span class="sxs-lookup"><span data-stu-id="0f986-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="0f986-114">Nur Verpackungsaufträge</span><span class="sxs-lookup"><span data-stu-id="0f986-114">Only packed orders</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]