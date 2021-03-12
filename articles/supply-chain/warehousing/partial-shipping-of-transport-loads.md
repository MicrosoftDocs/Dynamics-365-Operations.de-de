---
title: Teillieferung einer Transportladung
description: In diesem Thema wird erläutert, wie Sie eine Ladung teilweise liefern können und die Planung der Kapazität für die Ladung verschieben können.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 68a3d175e89e89d0909b140863b1aa61a184fce6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963284"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="c4aa3-103">Teillieferung einer Transportladung</span><span class="sxs-lookup"><span data-stu-id="c4aa3-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c4aa3-104">Durch Einrichten einer Teillieferung von Ladungen können Sie Ladungen handhaben, wo die Kapazität nicht bestimmt werden kann, bis alle Verkaufspositionen zu einer Ladung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="c4aa3-105">Der Prozess kann dann abgeschlossen werden, wenn die genaue Palettenanzahl bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="c4aa3-106">Daher müssen Sie nicht entscheiden, welche Paletten welchem Transport zugewiesen werden, bis zum Augenblick, an dem der Transport physisch aus dem bereitgestellten Bestand geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="c4aa3-107">Diese Funktion bietet eine Alternative zur Durchführung einer steiferen Struktur, in der Sie bestimmen müssen, welche Paletten welchem Transport zugewiesen werden, bevor die Entnahmearbeit und Ladearbeit erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="c4aa3-108">Stattdessen können Benutzer Einzellasten für eine Teillieferungsbestätigung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="c4aa3-109">Die Transportladeprozesse für diese Ladungen können dann erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="c4aa3-110">Daher kann die Transportplanungsabteilung Ladungen planen, ohne die Kapazität einzelner Transporte berücksichtigen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="c4aa3-111">Zum Zeitpunkt des Ladens können Arbeitskräfte eine neue Transportladung definieren, zu der eine Palette geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="c4aa3-112">Alternativ können sie eine vorhandene Transportladung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="c4aa3-113">Diese Daten können über ein mobiles Gerät erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="c4aa3-114">Daher können mehrere Lagerarbeitskräfte Lagerbestand aus denselben Ladungen oder verschiedenen Ladungen auf denselben LKW laden.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="c4aa3-115">Die Ladungen können dann vollständig oder teilweise geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="c4aa3-116">Um Lagerbestand aus einer Ladung in eine bestimmte Transportladung zu laden und die Ladung teilweise zu liefern, muss Arbeit generiert werden, indem eine Ladungsklasse in einer Arbeitsvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="c4aa3-117">Gewöhnliche Entnahmearbeit des Typs **Entnahme** kann nicht in eine Transportladung, wie einen LKW, geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="c4aa3-118">Transportladungen für Teillieferung einrichten</span><span class="sxs-lookup"><span data-stu-id="c4aa3-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="c4aa3-119">Die Einrichtung für die Teillieferung von Ladungen besteht aus den folgenden zwei Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="c4aa3-120">Die Ladestrategie festlegen</span><span class="sxs-lookup"><span data-stu-id="c4aa3-120">Set the loading strategy</span></span>

<span data-ttu-id="c4aa3-121">Sie müssen die Teilladung aktivieren, indem Sie die Ladestrategie festlegen.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="c4aa3-122">Sie können die Ladenstrategie festlegen, nachdem Sie eine Ladung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="c4aa3-123">Wählen Sie **Lagerortverwaltung** \> **Ladungen** \> **Alle Ladungen** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="c4aa3-124">Wählen Sie eine Ladung aus, und klicken Sie dann auf **Kopfzeile**.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="c4aa3-125">Wählen Sie im Feld **Ladungsstrategie** die Option **Teilladungslieferung zulässig** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="c4aa3-126">Erstellen Sie eine Menüoption für das Laden von Transportladungen</span><span class="sxs-lookup"><span data-stu-id="c4aa3-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="c4aa3-127">Sie müssen eine neue Menüoption erstellen, mit der Transportladungen geladen werden können.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="c4aa3-128">Mithilfe einer Transportladung können Sie Arbeitspositionen aus einer Ladung oder mehreren Ladungen gruppieren.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="c4aa3-129">Alles, was zur Transportladung hinzugefügt wird, kann dann mithilfe eines mobilen Scanners versendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="c4aa3-130">Wählen Sie **Lagerortverwaltung** \> **Setup** \> **Mobiles Gerät** \> **Menüoptionen für mobiles Gerät** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="c4aa3-131">Wählen Sie **Neu** aus und anschließend im Feld **Modus** die Option **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="c4aa3-132">Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="c4aa3-133">Wählen Sie auf der Registerkarte **Allgemein** im Feld **Angewiesen von** die Option **Transportverladung** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="c4aa3-134">Um die Lieferbestätigung auf einem mobilen Scanner zu aktivieren, wählen Sie im Feld **Zulässiger Lieferbestätigungstyp** die Option **Transportladung** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="c4aa3-135">Bestätigen der Lieferung einer Transportladung vom Client aus</span><span class="sxs-lookup"><span data-stu-id="c4aa3-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="c4aa3-136">Mit dieser Einstellung können Sie bestätigen, dass eine Transportladung, die eine vollständige Ladung oder eine teilweise geladene Ladung enthält, geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="c4aa3-137">Wählen Sie **Lagerortverwaltung** \> **Ladungen** \> **Transportladungen** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="c4aa3-138">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Liefern und empfangen** in der Gruppe **Bestätigen** die Option **Transport** aus.</span><span class="sxs-lookup"><span data-stu-id="c4aa3-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
