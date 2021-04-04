---
title: Versandcontainer
description: In diesem Thema wird beschrieben, wie Sie Transportcontainer für das Modul Gesamttransportkosten festlegen.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500957"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="2578b-103">Einrichten von Transportcontainern</span><span class="sxs-lookup"><span data-stu-id="2578b-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2578b-104">In diesem Thema wird beschrieben, wie Sie Transportcontainer für das Modul **Gesamttransportkosten** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2578b-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="2578b-105">Transportcontainer-Typen festlegen</span><span class="sxs-lookup"><span data-stu-id="2578b-105">Set up shipping container types</span></span>

<span data-ttu-id="2578b-106">Die Transportcontainer-Typen definieren die Arten von Transportcontainern, die für die Verwendung bei Schifffahrten und Fahrten zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="2578b-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="2578b-107">Um mit den Transportcontainer-Typen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Container einrichten \> Transportcontainer-Typen**.</span><span class="sxs-lookup"><span data-stu-id="2578b-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="2578b-108">Dort können Sie Datensätze für Ihre Containertypen anzeigen, hinzufügen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="2578b-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="2578b-109">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2578b-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="2578b-110">Feld</span><span class="sxs-lookup"><span data-stu-id="2578b-110">Field</span></span> | <span data-ttu-id="2578b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-111">Description</span></span> |
|---|---|
| <span data-ttu-id="2578b-112">Versandcontainertyp</span><span class="sxs-lookup"><span data-stu-id="2578b-112">Shipping container type</span></span> | <span data-ttu-id="2578b-113">Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Transportcontainer-Typ ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="2578b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-114">Description</span></span> | <span data-ttu-id="2578b-115">Geben Sie eine Beschreibung für den Transportcontainer-Typ ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="2578b-116">Volumen</span><span class="sxs-lookup"><span data-stu-id="2578b-116">Volume</span></span> | <span data-ttu-id="2578b-117">Geben Sie das maximale Volumen ein, das in Transportcontainern dieses Typs erlaubt ist.</span><span class="sxs-lookup"><span data-stu-id="2578b-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="2578b-118">Gewicht</span><span class="sxs-lookup"><span data-stu-id="2578b-118">Weight</span></span> | <span data-ttu-id="2578b-119">Geben Sie das maximale Gewicht ein, das in Transportcontainern dieses Typs zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2578b-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="2578b-120">Retourfähig</span><span class="sxs-lookup"><span data-stu-id="2578b-120">Returnable</span></span> | <span data-ttu-id="2578b-121">Geben Sie an, ob Transportcontainer dieses Typs an den Lieferanten zurückgegeben werden können, nachdem sie während einer Fahrt benutzt wurden.</span><span class="sxs-lookup"><span data-stu-id="2578b-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="2578b-122">Wenn diese Option auf *Ja* festgelegt ist, können zusätzliche Kosten für die Rückgabe von Transportcontainern dieses Typs an den Hafen anfallen.</span><span class="sxs-lookup"><span data-stu-id="2578b-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="2578b-123">Festlegen von Transportcontainern</span><span class="sxs-lookup"><span data-stu-id="2578b-123">Set up shipping containers</span></span>

<span data-ttu-id="2578b-124">Sie verwenden Transportcontainer-Datensätze, um jeden Container zu identifizieren, den Sie auf Fahrten verwenden.</span><span class="sxs-lookup"><span data-stu-id="2578b-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="2578b-125">Wenn Sie eine Fahrt erstellen, können Sie in der Liste aller Transportcontainer-Datensätze, die Sie hier definiert haben, einen bestimmten Container für diese Fahrt auswählen.</span><span class="sxs-lookup"><span data-stu-id="2578b-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="2578b-126">Diese Funktion ist besonders nützlich, wenn Ihre Firma eigene Transportcontainer besitzt.</span><span class="sxs-lookup"><span data-stu-id="2578b-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="2578b-127">Sie müssen keine Transportcontainernummern für Transportcontainer eingeben, die nur einmalig verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2578b-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="2578b-128">Stattdessen können Sie die Transportcontainer-Nummer hinzufügen, wenn Sie eine Fahrt erstellen.</span><span class="sxs-lookup"><span data-stu-id="2578b-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="2578b-129">Transportcontainer-Datensätze werden nur in den Gesamttransportkosten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2578b-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="2578b-130">Sie sind nicht im Standardmodul **Transportverwaltung** (TMS) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2578b-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="2578b-131">Um mit Transportcontainern zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Container einrichten \> Transportcontainer**.</span><span class="sxs-lookup"><span data-stu-id="2578b-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="2578b-132">Dort können Sie Datensätze Ihrer Transportcontainer anzeigen, hinzufügen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="2578b-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="2578b-133">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2578b-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="2578b-134">Feld</span><span class="sxs-lookup"><span data-stu-id="2578b-134">Field</span></span> | <span data-ttu-id="2578b-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-135">Description</span></span> |
|---|---|
| <span data-ttu-id="2578b-136">Versandcontainer</span><span class="sxs-lookup"><span data-stu-id="2578b-136">Shipping container</span></span> | <span data-ttu-id="2578b-137">Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Transportcontainer ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="2578b-138">Versandcontainertyp</span><span class="sxs-lookup"><span data-stu-id="2578b-138">Shipping container type</span></span> | <span data-ttu-id="2578b-139">Wählen Sie den Typ des Transportcontainers.</span><span class="sxs-lookup"><span data-stu-id="2578b-139">Select the type of shipping container.</span></span> <span data-ttu-id="2578b-140">Weitere Informationen finden Sie im Abschnitt [Versandcontainer-Typen festlegen](#shipping-container-types) weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="2578b-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="2578b-141">Das Einrichten des Transportcontainers ist optional.</span><span class="sxs-lookup"><span data-stu-id="2578b-141">The shipping container setup is optional.</span></span> <span data-ttu-id="2578b-142">Normalerweise werden Sie sie nur verwenden, wenn Ihre Firma eigene Transportcontainer besitzt oder häufig dieselben Transportcontainer wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="2578b-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="2578b-143">Für Transportcontainer-Nummern werden keine Prüfziffern berechnet.</span><span class="sxs-lookup"><span data-stu-id="2578b-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="2578b-144">Einheitstypen festlegen</span><span class="sxs-lookup"><span data-stu-id="2578b-144">Set up unit types</span></span>

<span data-ttu-id="2578b-145">Einheitstypen legen zusätzliche Gruppierungen und Identifikationsmethoden für Transportcontainer fest.</span><span class="sxs-lookup"><span data-stu-id="2578b-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="2578b-146">Die Art der Einheit wird typischerweise verwendet, um die Art des Behälters zu identifizieren, in dem Waren verpackt sind, wie z. B. Paletten oder Fässer.</span><span class="sxs-lookup"><span data-stu-id="2578b-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="2578b-147">Sie können einen Einheitstyp auswählen, wenn Sie einen Container auf der Seite **Alle Transportcontainer** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2578b-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="2578b-148">Einheitentypen werden nur in Gesamttransportkosten kalkuliert.</span><span class="sxs-lookup"><span data-stu-id="2578b-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="2578b-149">Sie sind in TMS nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2578b-149">They aren't available in TMS.</span></span>

<span data-ttu-id="2578b-150">Um mit Einheitentypen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Container einrichten \> Einheitentypen**.</span><span class="sxs-lookup"><span data-stu-id="2578b-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="2578b-151">Dort können Sie Datensätze für Ihre Einheitentypen anzeigen, hinzufügen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="2578b-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="2578b-152">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2578b-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="2578b-153">Feld</span><span class="sxs-lookup"><span data-stu-id="2578b-153">Field</span></span> | <span data-ttu-id="2578b-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-154">Description</span></span> |
|---|---|
| <span data-ttu-id="2578b-155">Einheitstyp</span><span class="sxs-lookup"><span data-stu-id="2578b-155">Unit type</span></span> | <span data-ttu-id="2578b-156">Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Einheitentyp ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="2578b-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-157">Description</span></span> | <span data-ttu-id="2578b-158">Geben Sie eine Beschreibung für den Einheitentyp ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="2578b-159">Kältetypen festlegen</span><span class="sxs-lookup"><span data-stu-id="2578b-159">Set up refrigeration types</span></span>

<span data-ttu-id="2578b-160">Kühltypen legen zusätzliche Gruppierungen und Identifikationsmethoden für Transportcontainer (in der Regel Kühlcontainer) fest.</span><span class="sxs-lookup"><span data-stu-id="2578b-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="2578b-161">Sie können einen Kühltyp auswählen, wenn Sie einen Transportcontainer auf der Seite **Alle Transportcontainer** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2578b-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="2578b-162">Um mit Kühltypen zu arbeiten, gehen Sie auf die Seite **Gesamttransportkosten \> Container einrichten \> Kühltypen**.</span><span class="sxs-lookup"><span data-stu-id="2578b-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="2578b-163">Dort können Sie Datensätze für Ihre Kühltypen anzeigen, hinzufügen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="2578b-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="2578b-164">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2578b-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="2578b-165">Feld</span><span class="sxs-lookup"><span data-stu-id="2578b-165">Field</span></span> | <span data-ttu-id="2578b-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-166">Description</span></span> |
|---|---|
| <span data-ttu-id="2578b-167">Kühlungsart</span><span class="sxs-lookup"><span data-stu-id="2578b-167">Refrigeration type</span></span> | <span data-ttu-id="2578b-168">Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Kühltyp ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="2578b-169">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2578b-169">Description</span></span> | <span data-ttu-id="2578b-170">Geben Sie eine Beschreibung des Kühlschranktyps ein.</span><span class="sxs-lookup"><span data-stu-id="2578b-170">Enter a description of the refrigeration type.</span></span> |
