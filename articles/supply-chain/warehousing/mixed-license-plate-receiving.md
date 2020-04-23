---
title: Gemischtes Kennzeichen – Empfang
description: In diesem Thema wird beschrieben, wie das Empfangen eines gemischten Ladungsträgers verwendet wird, um Arbeit für mehrere Artikel mit einem Mobilgerät zu erfassen und zu erstellen.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215768"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="97300-103">Gemischtes Kennzeichen – Empfang</span><span class="sxs-lookup"><span data-stu-id="97300-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97300-104">Das Empfangen eines gemischten Ladungsträgers ermöglicht Ihnen, einen Ladungsträger zu erstellen, der aus mehreren Artikeln besteht, ehe Sie eine Einlagerungsarbeit erstellen und erfassen.</span><span class="sxs-lookup"><span data-stu-id="97300-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="97300-105">Ein Ladungsträger, der aus mehreren Artikeln besteht, muss an der empfangenden Rampe nicht aufgeteilt werden, damit jeder Artikel erfasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="97300-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="97300-106">Wenn Sie eines Artikel-bezogenen Fluss verwenden, um die Quelldokumentpositionen zu identifizieren, können Sie Barcodes im Artikelsteuerelement scannen.</span><span class="sxs-lookup"><span data-stu-id="97300-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="97300-107">Wenn der Strichcode eine Menge und eine Maßeinheit (UOM) hat, werden Artikel und Menge automatisch zum gemischten Ladungsträger hinzugefügt und Sie kehren zum Bildschirm zurück, um einen weiteren Artikel zu scannen.</span><span class="sxs-lookup"><span data-stu-id="97300-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="97300-108">Dies ermöglicht Ihnen, schnell alle Artikel zu scannen, ohne jeden Schritt bestätigen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="97300-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="97300-109">Im Fluss für das Empfangen gemischter Ladungsträger können Sie die Liste der Artikel anzeigen, die bereits für den Ladungsträger gescannt wurden. Von hier können Sie die Menge eines Artikel ändern oder korrigieren.</span><span class="sxs-lookup"><span data-stu-id="97300-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="97300-110">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="97300-110">Where it applies</span></span>

<span data-ttu-id="97300-111">Der Empfang gemischter Ladungsträger ist ein Empfangsfluss eines Mobilgeräts, um gleichzeitig Arbeit für mehrere Positionen/Artikel zu erfassen und zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="97300-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="97300-112">Dies ist nützlich, wenn Sie eingehende Ladungsträger mit mehreren Artikel empfangen.</span><span class="sxs-lookup"><span data-stu-id="97300-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="97300-113">So richten Sie den Empfang gemischter Ladungsträger ein:</span><span class="sxs-lookup"><span data-stu-id="97300-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="97300-114">Der Empfang gemischter Ladungsträger wird als Menüoption des mobilen Geräts eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="97300-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="97300-115">Sie müssen eine neue Menüoption mit Modusarbeit erstellen, die keine vorhandene Arbeit nutzt, und eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="97300-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="97300-116">Gemischtes Kennzeichen – Empfang</span><span class="sxs-lookup"><span data-stu-id="97300-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="97300-117">Empfang und Einlagerung gemischter Kennzeichen</span><span class="sxs-lookup"><span data-stu-id="97300-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="97300-118">Die Optionen zum Identifizieren der Quelldokumentpositionen sind Bestellungsartikel, Bestellpositionen, Rücklieferungen, Umlagerungsaufträge und Umlagerungsauftragspositionen.</span><span class="sxs-lookup"><span data-stu-id="97300-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="97300-119">Diese Optionen können den eingehenden Auftrag für einen einzelnen Ladungsträger ändern.</span><span class="sxs-lookup"><span data-stu-id="97300-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="97300-120">Die letzte Option ist per Ladungsartikel.</span><span class="sxs-lookup"><span data-stu-id="97300-120">The last option is by load item.</span></span> <span data-ttu-id="97300-121">Sie können mehrere Artikel zu einem Ladungsträger hinzufügen, können aber nicht zwischen Ladungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="97300-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
