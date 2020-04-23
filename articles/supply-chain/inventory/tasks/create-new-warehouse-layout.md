---
title: Ein neues Lagerortlayout erstellen
description: In diesem Thema wird beschrieben, wie Informationen zu Lagerplätzen in einem Lager eingerichtet werden.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214020"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="4da04-103">Ein neues Lagerortlayout erstellen</span><span class="sxs-lookup"><span data-stu-id="4da04-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4da04-104">In diesem Thema wird beschrieben, wie Informationen zu Lagerplätzen in einem Lager eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="4da04-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="4da04-105">Dies gilt nur für Lagerorte, die mithilfe von die mithilfe der "Standardlagerung" im Modul "Lagerverwaltung" erstellt wurden, nicht für Lagerorte, die im Modul "Lagerortverwaltung" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4da04-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="4da04-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="4da04-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="4da04-107">Die Standardlagerplatzkapazität festlegen</span><span class="sxs-lookup"><span data-stu-id="4da04-107">Set the default location capacity</span></span>
1. <span data-ttu-id="4da04-108">Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Parameter für Lager- und Lagerortverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="4da04-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="4da04-109">Wählen Sie die Registerkarte **Lagerplätze** aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="4da04-110">Geben Sie im Feld **Standardbreite** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="4da04-111">Geben Sie im Feld **Standardtiefe** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="4da04-112">Geben Sie im Feld **Standardhöhe** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="4da04-113">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4da04-113">Select **Save**.</span></span>
7. <span data-ttu-id="4da04-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4da04-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="4da04-115">Das Format des Lagerplatznamens definieren</span><span class="sxs-lookup"><span data-stu-id="4da04-115">Define the location name format</span></span>
1. <span data-ttu-id="4da04-116">Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Lageraufschlüsselung > Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="4da04-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="4da04-117">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-117">Select **New**.</span></span>
3. <span data-ttu-id="4da04-118">Geben Sie im Feld **Lagerort** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="4da04-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="4da04-120">Wählen Sie im Feld **Standort** den gewünschten Datensatz in der Suche aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="4da04-121">Schalten Sie die Erweiterung des Abschnitts **Lagerplatznamen** ein/aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="4da04-122">Die Optionen in diesem Abschnitt definieren das Standardformat für Lagerplatznamen.</span><span class="sxs-lookup"><span data-stu-id="4da04-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="4da04-123">In unserem Beispiel schließen wir die Gangnummer, Regalnummer und Regelbodennummer ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="4da04-124">Legen Sie die Option **Gang einschließen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="4da04-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="4da04-125">Legen Sie die Option **Regal einschließen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="4da04-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="4da04-126">Geben Sie im Feld **Format** für das Regal einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="4da04-127">Legen Sie die Option **Regalboden einschließen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="4da04-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="4da04-128">Geben Sie im Feld **Format** für den Regalboden einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4da04-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="4da04-129">Lagerort-Lagerplätze definieren</span><span class="sxs-lookup"><span data-stu-id="4da04-129">Define warehouse locations</span></span>
1. <span data-ttu-id="4da04-130">Wählen Sie im Aktivitätsbereich **Lagerort** aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="4da04-131">Wählen Sie **Lagerplatz-Assistent** aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="4da04-132">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="4da04-132">Select **Next**.</span></span>
4. <span data-ttu-id="4da04-133">Heben Sie die Auswahl für die Option **Ausgangsrampen** auf</span><span class="sxs-lookup"><span data-stu-id="4da04-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="4da04-134">Heben Sie die Auswahl für die Option **Sammellagerplätze** auf</span><span class="sxs-lookup"><span data-stu-id="4da04-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="4da04-135">Wählen Sie **Weiter** aus, bis die Option zur Auswahl von **Fertig stellen** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4da04-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="4da04-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4da04-136">Close the page.</span></span>
8. <span data-ttu-id="4da04-137">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4da04-137">Refresh the page.</span></span>

