---
title: Lagerplätze für Lagerbestand
description: Lagerplätze für Lagerbestand werden mit grundlegendem Warehousing (WMS I) verwendet , um zu bestimmen, wo Artikel in einem WMS I-Lagerort gelagert und entnommen werden.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31096aa9c97f0307c7004d1af1e424dde1dc65cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264065"
---
# <a name="inventory-locations"></a><span data-ttu-id="50fd5-103">Lagerplätze für Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="50fd5-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50fd5-104">Lagerplätze für Lagerbestand werden mit grundlegendem Warehousing (WMS I) verwendet , um zu bestimmen, wo Artikel in einem WMS I-Lagerort gelagert und entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="50fd5-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="50fd5-105">Dieses Thema gilt für Funktionen im Modul "Bestandsverwaltung".</span><span class="sxs-lookup"><span data-stu-id="50fd5-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="50fd5-106">Es gilt nicht für Funktionen im Modul "Lagerverwaltung".</span><span class="sxs-lookup"><span data-stu-id="50fd5-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="50fd5-107">Der Begriff Lagerplatz bezieht sich auf den Ort, an dem Artikel gespeichert und entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="50fd5-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="50fd5-108">Für jeden Lagerplatz kann auch der Ort angegeben werden, an dem der Artikel eingelagert wird.</span><span class="sxs-lookup"><span data-stu-id="50fd5-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="50fd5-109">Standardmäßig handelt es sich hierbei um den gleichen Ort.</span><span class="sxs-lookup"><span data-stu-id="50fd5-109">By default, they are the same.</span></span> <span data-ttu-id="50fd5-110">Artikel werden an einem Lagerplatz in der Regel von der gleichen Seite aus eingelagert und entnommen. Es gibt jedoch auch Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="50fd5-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="50fd5-111">So werden beispielsweise Artikel, die in Durchreichregalen gelagert werden, von einem Lagergang aus eingelagert und von einem anderen Gang aus entnommen.</span><span class="sxs-lookup"><span data-stu-id="50fd5-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="50fd5-112">Die wichtigste Angabe ist der Lagerplatzname, der üblicherweise anhand der Koordinaten "Lagerort", "Gang", "Regal", "Regalboden" und "Lagerfach" bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="50fd5-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="50fd5-113">Dieser Name bzw. diese Kennung kann manuell eingegeben oder auf der Seite "Lagerplätze für Lagerbestand" auf Basis der Lagerplatzkoordinaten generiert werden. Beispiel: "01-02-03-4" für Gang 1, Regal 2, Regalboden 3, Lagerfach 4.</span><span class="sxs-lookup"><span data-stu-id="50fd5-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="50fd5-114">Lagerplatzeigenschaften</span><span class="sxs-lookup"><span data-stu-id="50fd5-114">Location properties</span></span>

<span data-ttu-id="50fd5-115">Ein Lagerplatz hat folgende Merkmale:</span><span class="sxs-lookup"><span data-stu-id="50fd5-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="50fd5-116">Größe (Höhe, Breite, Tiefe und damit Volumen)</span><span class="sxs-lookup"><span data-stu-id="50fd5-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="50fd5-117">Lagerort, Gang, Regal, Regalboden und Lagerfach.</span><span class="sxs-lookup"><span data-stu-id="50fd5-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="50fd5-118">Lagerplatztyp (Sammellagerplatz, Entnahmeort, Eingangsrampe, Ausgangsrampe, Produktionseingangslagerplatz, Inspektionslagerplatz oder Kanban-Supermarkt)</span><span class="sxs-lookup"><span data-stu-id="50fd5-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="50fd5-119">In Onlinesystemen kann ein Prüftext verwendet werden, um sicherzustellen, dass der Mitarbeiter den richtigen Lagerplatz für einen bestimmten Artikel gewählt hat.</span><span class="sxs-lookup"><span data-stu-id="50fd5-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="50fd5-120">Dieser Prüftext kann manuell erstellt oder standardmäßig bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="50fd5-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="50fd5-121">Sortiercodes</span><span class="sxs-lookup"><span data-stu-id="50fd5-121">Sort codes</span></span>
<span data-ttu-id="50fd5-122">Sortiercodes dienen zur Optimierung der Handhabung von Entnahmepositionen. Sie enthalten detaillierte Informationen für die Entnahme von Artikeln aus dem Lager, einschließlich der Entnahmereihenfolge.</span><span class="sxs-lookup"><span data-stu-id="50fd5-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="50fd5-123">Sortiercodes können nach Gang oder anderen Koordinaten angegeben oder manuell für den Lagerplatz zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="50fd5-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="50fd5-124">Blockierte Lagerplätze</span><span class="sxs-lookup"><span data-stu-id="50fd5-124">Blocked locations</span></span>
<span data-ttu-id="50fd5-125">Gelegentlich kann es erforderlich sein, einen Lagerplatz für einen gewissen Zeitraum zu blockieren, z. B. für Reparaturarbeiten.</span><span class="sxs-lookup"><span data-stu-id="50fd5-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="50fd5-126">Es kann möglicherweise auch ausreichend sein, nur die Eingabe oder nur die Ausgabe zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="50fd5-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="50fd5-127">Strukturdarstellung</span><span class="sxs-lookup"><span data-stu-id="50fd5-127">Tree structure</span></span>

<span data-ttu-id="50fd5-128">Auf der Seite "Lagerplätze für Lagerbestand" können Sie das Lagerortlayout in einer Strukturdarstellung auf Basis der Koordinaten der Lagerplätze des Lagerbestands in einem definierten Anzeigeformat anzeigen.</span><span class="sxs-lookup"><span data-stu-id="50fd5-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="50fd5-129">Verwalten von Lagerplätzen über das Formular "Lagerort"</span><span class="sxs-lookup"><span data-stu-id="50fd5-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="50fd5-130">Es ist möglich, Lagerplätze von einem Lagerort an einen anderen zu kopieren und Lagerplätze mit einem Assistenten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50fd5-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="50fd5-131">Bevor Sie den Assistenten ausführen, sollten Sie sicherstellen, dass Sie die Standard-Lagerortnamen auf der Seite "Lagerort" definiert haben.</span><span class="sxs-lookup"><span data-stu-id="50fd5-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="50fd5-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="50fd5-132">Additional resources</span></span>
--------

[<span data-ttu-id="50fd5-133">Ein neues Lagerortlayout erstellen</span><span class="sxs-lookup"><span data-stu-id="50fd5-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]