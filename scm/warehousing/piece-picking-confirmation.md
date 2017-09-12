---
title: "Stückentnahmebestätigung"
description: "In diesem Thema wird beschrieben, wie Sie Stückentnahmebestätigung über ein mobiles Gerät einrichten und anwenden."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 62b637b81a522c353067248deea79cfbf98518e9
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="piece-picking-confirmation"></a><span data-ttu-id="37bfc-103">Stückentnahmebestätigung</span><span class="sxs-lookup"><span data-stu-id="37bfc-103">Piece picking confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37bfc-104">Die Stückentnahme ermöglicht Ihnen, jedes Teil des Bestands zu bestätigen über Entnahme- oder Inventurarbeit auf einem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="37bfc-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="37bfc-105">Bei der Entnahme können Sie die Menge der zu verarbeitenden Arbeit bis zu der Menge bestätigen, die für die zu entnehmende Arbeit angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="37bfc-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="37bfc-106">Bei Inventurarbeit können Sie den Bestand scannen, den Sie zählen und die Gesamtsumme nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="37bfc-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="37bfc-107">Wenn Sie die Stückentnahme aktivieren, wird die Produktbestätigung automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37bfc-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="37bfc-108">Für Arbeitstypentnahmen wird eine maximale Anzahl an Stücken aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37bfc-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="37bfc-109">Dadurch wird es Ihnen ermöglicht, eine Maximalzahl an Stücken festzulegen, die während des Arbeitsprozesses bestätigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="37bfc-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="37bfc-110">Die maximale Menge basiert auf der aktuellen Leistungseinheit, die verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="37bfc-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="37bfc-111">Der Inventurarbeitstyp erlaubt kein Maximum.</span><span class="sxs-lookup"><span data-stu-id="37bfc-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="37bfc-112">Sie können die Menge und die Maßeinheit (UOM) verwenden, die einem gescannten Strichcode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="37bfc-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="37bfc-113">Dies funktioniert für den Empfang an eingehenden Flüssen einschließlich des Empfangs gemischter Ladungsträger, Bestellungsartikel, Umlagerungsauftragsartikel und Ladungsartikel.</span><span class="sxs-lookup"><span data-stu-id="37bfc-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="37bfc-114">Es funktioniert auch für die Stückentnahme, bei der durch das Scannen des Barcodes die Menge zur Gesamtanzahl bestätigter Stücke hinzugefügt wird und es zu einer Konvertierung zwischen der UOM auf dem Barcode und der Leistungseinheit kommt.</span><span class="sxs-lookup"><span data-stu-id="37bfc-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="37bfc-115">Wenn beim Zählen der Maßeinheit im Barcode bestätigt ist, dass die Menge für das Zählen in der Nummernkreisgruppe zulässig ist, wird die Menge zur Gesamtzählung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37bfc-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="37bfc-116">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="37bfc-116">Where it applies</span></span>

<span data-ttu-id="37bfc-117">Die Stückentnahme funktioniert für alle Inventurarbeiten und für die Erstentnahme aller Arten von Arbeit.</span><span class="sxs-lookup"><span data-stu-id="37bfc-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="37bfc-118">Die Stückentnahme gilt nicht, wenn der Artikel über Seriennummern kontrolliert wird oder wenn es sich um eine Produktions- oder Kanban-Entnahme von einem Ladungsträger-Lagerplatz handelt und der Artikel auf „Staging“ gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="37bfc-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="37bfc-119">Stückentnahme einrichten</span><span class="sxs-lookup"><span data-stu-id="37bfc-119">Set up piece picking</span></span>

1.  <span data-ttu-id="37bfc-120">Öffnen Sie über ein Menüelement des mobilen Geräts das Einstellungsformular für Arbeitsbestätigung: Lagerortverwaltung > **Lagerortverwaltung** > **Einstellungen** > **Mobiles Gerät** > **Menüelemente des mobilen Geräts**.</span><span class="sxs-lookup"><span data-stu-id="37bfc-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="37bfc-121">Öffnen Sie über das Menüelement des mobilen Geräts die Einrichtung Arbeitsbestätigung.</span><span class="sxs-lookup"><span data-stu-id="37bfc-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="37bfc-122">Die folgenden Optionen sind zur Auswahl verfügbar, wenn der Arbeitstyp Entnahme oder Inventur ist.</span><span class="sxs-lookup"><span data-stu-id="37bfc-122">The following options become available for selection when the work type is pick or counting.</span></span>

| <span data-ttu-id="37bfc-123">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="37bfc-123">Option</span></span>        | <span data-ttu-id="37bfc-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37bfc-124">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="37bfc-125">Stückentnahmebestätigung</span><span class="sxs-lookup"><span data-stu-id="37bfc-125">Piece picking confirmation</span></span>   | <span data-ttu-id="37bfc-126">Verfügbar für Entnahme- und Inventurarbeitstypen.</span><span class="sxs-lookup"><span data-stu-id="37bfc-126">Available for pick and counting work types.</span></span> <span data-ttu-id="37bfc-127">Produktbestätigung wird automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="37bfc-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="37bfc-128">Ermöglicht Ihnen, jeden Inventurartikel über das mobile Gerät zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="37bfc-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> | 
| <span data-ttu-id="37bfc-129">Maximale Anzahl von Stücken</span><span class="sxs-lookup"><span data-stu-id="37bfc-129">Maximum number of pieces</span></span>     | <span data-ttu-id="37bfc-130">Verfügbar für Entnahmearbeit, wenn Stückentnahmebestätigung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="37bfc-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="37bfc-131">Beschränkt die Anzahl der Teile, die Sie bestätigen müssen.</span><span class="sxs-lookup"><span data-stu-id="37bfc-131">Sets a limit to the number of pieces that you must confirm.</span></span> |  

