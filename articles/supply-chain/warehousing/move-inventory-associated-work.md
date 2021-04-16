---
title: Bewegung von Bestand mit zugeordneter Arbeit in der Lagerortverwaltung
description: Mit der Bewegung von Bestand können Sie festlegen, welche Lagerortverwalter reservierten Bestand bewegen dürfen.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6477a91b3c65e8be5ab527eaff12c92ae7918b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808749"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="3c8c6-103">Bewegung von Bestand mit zugeordneter Arbeit in der Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="3c8c6-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c8c6-104">Mit der Bewegung von Bestand können Sie festlegen, welche Lagerortverwalter reservierten Bestand bewegen dürfen.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="3c8c6-105">Dies bietet Flexibilität an geregelten Lagerorten, wo Sie festlegen können, dass eine Arbeitskraft nicht berechtigt ist, einen neuen Entnahmeort zu wählen, um Arbeit zu entnehmen, die bereits erledigt wurde.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="3c8c6-106">Es ermöglicht auch einem Lageortleiter festzulegen, welche Funktionen weniger erfahrene Arbeitskräfte haben sollen.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="3c8c6-107">Die Möglichkeit, die täglichen Arbeitsgänge von Lagerortarbeitskräften zu verwalten, kann in folgenden Szenarien hilfreich sein:</span><span class="sxs-lookup"><span data-stu-id="3c8c6-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="3c8c6-108">Szenario 1</span><span class="sxs-lookup"><span data-stu-id="3c8c6-108">Scenario 1</span></span>

<span data-ttu-id="3c8c6-109">Ein Unternehmen hat einen relativ kleinen Wareneingangsbereich, der mit Paletten und Kartons verstopft ist, die auf ihre Einlagerung warten.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="3c8c6-110">Eine große Lieferung wird für den aktuellen Tag erwartet. Deshalb entscheidet der zuständige Sachbearbeiter, den Wareneingang zu räumen, indem er einige Palletten in einen zweiten Eingangsbereich verschiebt.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="3c8c6-111">Szenario 2</span><span class="sxs-lookup"><span data-stu-id="3c8c6-111">Scenario 2</span></span>

<span data-ttu-id="3c8c6-112">Ein erfahrener Lagerarbeiter hat die Möglichkeit, Artikel an einem Lagerort zusammenzufassen, anstatt diese auf drei Lagerplätze in der Nähe mit jeweils geringen Mengen zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across three nearby locations with little quantity on each.</span></span> <span data-ttu-id="3c8c6-113">Die Arbeitskraft möchte die Menge konsolidieren, indem Artikel von den einzelnen Lagerplätzen zu einem Lagerplatz auf demselben Ladungsträger verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="3c8c6-114">Szenario 3</span><span class="sxs-lookup"><span data-stu-id="3c8c6-114">Scenario 3</span></span>

<span data-ttu-id="3c8c6-115">Eine Palette in einem Staginglagerplatz wie STAGE01, der sich in der Nähe von BAYDOOR01 befindet, soll ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="3c8c6-116">Aufgrund einer Planungsänderung soll der LKW allerdings bei BAYDOOR04 eintreffen.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="3c8c6-117">Der Sachbearbeiter ist darüber informiert und muss sicherstellen, dass der LKW nicht bei STAGE01 auf die Ladung warten muss.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="3c8c6-118">Er beschließt, die Artikel der Lieferung von STAGE01 nach STAGE04 zu verschieben, da dieser näher am Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="3c8c6-119">Aktuelle Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3c8c6-119">Current limitations</span></span>

<span data-ttu-id="3c8c6-120">Die Arbeitsreservierungen, die Sie verschieben können, sind begrenzt auf Aufträge, Umlagerungsauftragsprobleme, Umlagerungsauftragszugang, Bestellungen und Wiederbeschaffungsarbeit.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="3c8c6-121">Das Verschieben von Artikel ist eingeschränkt, um das Aufteilen von Arbeitspositionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="3c8c6-122">Das bedeutet, wenn Sie eine Arbeitsposition für 100 Stück von Artikel A am Lagerplatz Loc1 haben, können Sie nicht nur 30 Stück von Artikel A zu einem anderen Lagerplatz verschieben.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="3c8c6-123">Dies würde zu einer Teilung der vorhandenen Arbeitsposition in je 30 und 70 Stück führen, da die Lagerplätze unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="3c8c6-124">Bei Staging-Szenarien, bei denen der Ladungsträger, von dem Sie die Waren verschieben oder bei denen der Ladungsträger, zu dem Sie die Waren verschieben als Zielladungsträger für eine Arbeitsauftrag eingerichtet sind, sind nur Verschiebungen des ganzen Ladungsträgers zulässig, damit der Zielladungsträger nicht geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>

<span data-ttu-id="3c8c6-125">Nur die Ad-hoc-Bewegung wird derzeit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="3c8c6-126">Das bedeutet, dass Sie nicht in der Lage sind, reservierten Bestand durch eine Bewegung über das Vorlagenmenü des Mobilgeräts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="3c8c6-127">Einrichten von Berechtigungen zum Bewegen von Bestand für einzelne Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="3c8c6-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="3c8c6-128">Für die Arbeitskraft, die autorisiert werden soll, Bestand zu verschieben, aktivieren Sie das Kontrollkästchen **Bewegung von Bestand mit zugeordneter Arbeit zulassen** unter **Lagerortverwaltung \> Einstellungen \> Arbeitskraft**.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-128">For the worker who is allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management \> Setup \> Worker**.</span></span>  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
