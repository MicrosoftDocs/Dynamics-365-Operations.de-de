---
title: Stückentnahmebestätigung
description: Die Stückentnahme ermöglicht Ihnen, jedes Teil des Bestands zu bestätigen über Entnahme- oder Inventurarbeit auf einem mobilen Gerät.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f9da533998341de60d210e196baae64d285d372
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818847"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="fa607-103">Stückentnahmebestätigung</span><span class="sxs-lookup"><span data-stu-id="fa607-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa607-104">Die Stückentnahme ermöglicht Ihnen, jedes Teil des Bestands zu bestätigen über Entnahme- oder Inventurarbeit auf einem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="fa607-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="fa607-105">Bei der Entnahme können Sie die Menge der zu verarbeitenden Arbeit bis zu der Menge bestätigen, die für die zu entnehmende Arbeit angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fa607-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="fa607-106">Bei Inventurarbeit können Sie den Bestand scannen, den Sie zählen und die Gesamtsumme nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="fa607-106">For counting work, you can scan the inventory you are counting and track the total amount.</span></span>

<span data-ttu-id="fa607-107">Wenn Sie die Stückentnahme aktivieren, wird die Produktbestätigung automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa607-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="fa607-108">Für Arbeitstypentnahmen können Sie eine maximale Anzahl an Stücken festlegen.</span><span class="sxs-lookup"><span data-stu-id="fa607-108">For work-type picks, you can set a maximum number of pieces.</span></span> <span data-ttu-id="fa607-109">Dadurch wird es Ihnen ermöglicht, eine Maximalzahl an Stücken festzulegen, die während des Arbeitsprozesses bestätigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fa607-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="fa607-110">Die maximale Menge basiert auf der aktuellen Leistungseinheit, die verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="fa607-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="fa607-111">Der Inventurarbeitstyp erlaubt kein Maximum.</span><span class="sxs-lookup"><span data-stu-id="fa607-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="fa607-112">Sie können die Menge und die Maßeinheit (UOM) verwenden, die einem gescannten Strichcode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa607-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="fa607-113">Dies funktioniert für den Empfang an eingehenden Flüssen einschließlich des Empfangs gemischter Ladungsträger, Bestellungsartikel, Umlagerungsauftragsartikel und Ladungsartikel.</span><span class="sxs-lookup"><span data-stu-id="fa607-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="fa607-114">Es funktioniert auch für die Stückentnahme, bei der durch das Scannen des Barcodes die Menge zur Gesamtanzahl bestätigter Stücke hinzugefügt wird und es zu einer Konvertierung zwischen der UOM auf dem Barcode und der Leistungseinheit kommt.</span><span class="sxs-lookup"><span data-stu-id="fa607-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="fa607-115">Wenn beim Zählen der Maßeinheit im Barcode bestätigt ist, dass die Menge für das Zählen in der Nummernkreisgruppe zulässig ist, wird die Menge zur Gesamtzählung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa607-115">When counting the UOM on the bar code, if it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="fa607-116">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="fa607-116">Where it applies</span></span>

<span data-ttu-id="fa607-117">Die Stückentnahme funktioniert für alle Inventurarbeiten und für die Erstentnahme aller Arten von Arbeit.</span><span class="sxs-lookup"><span data-stu-id="fa607-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="fa607-118">Die Stückentnahme gilt nicht, wenn der Artikel über Seriennummern kontrolliert wird oder wenn es sich um eine Produktions- oder Kanban-Entnahme von einem Ladungsträger-Lagerplatz handelt und der Artikel auf „Staging“ gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="fa607-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="fa607-119">Stückentnahme einrichten</span><span class="sxs-lookup"><span data-stu-id="fa607-119">Set up piece picking</span></span>

1.  <span data-ttu-id="fa607-120">Öffnen Sie über ein Menüelement des mobilen Geräts das Einstellungsformular für Arbeitsbestätigung: Lagerortverwaltung > **Lagerortverwaltung** > **Einstellungen** > **Mobiles Gerät** > **Menüelemente des mobilen Geräts**.</span><span class="sxs-lookup"><span data-stu-id="fa607-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="fa607-121">Öffnen Sie über das Menüelement des mobilen Geräts die Einrichtung Arbeitsbestätigung.</span><span class="sxs-lookup"><span data-stu-id="fa607-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="fa607-122">Die folgenden Optionen sind zur Auswahl verfügbar, wenn der Arbeitstyp Entnahme oder Inventur ist.</span><span class="sxs-lookup"><span data-stu-id="fa607-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="fa607-123">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="fa607-123">Option</span></span>           |                                                                            <span data-ttu-id="fa607-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa607-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa607-125">Stückentnahmebestätigung</span><span class="sxs-lookup"><span data-stu-id="fa607-125">Piece picking confirmation</span></span> | <span data-ttu-id="fa607-126">Verfügbar für Entnahme- und Inventurarbeitstypen.</span><span class="sxs-lookup"><span data-stu-id="fa607-126">Available for pick and counting work types.</span></span> <span data-ttu-id="fa607-127">Produktbestätigung wird automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fa607-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="fa607-128">Ermöglicht Ihnen, jeden Inventurartikel über das mobile Gerät zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="fa607-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="fa607-129">Maximale Anzahl von Stücken</span><span class="sxs-lookup"><span data-stu-id="fa607-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="fa607-130">Verfügbar für Entnahmearbeit, wenn Stückentnahmebestätigung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa607-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="fa607-131">Beschränkt die Anzahl der Teile, die Sie bestätigen müssen.</span><span class="sxs-lookup"><span data-stu-id="fa607-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]