---
title: Grundeinrichtung eines veröffentlichten Produktmasters abschließen
description: In diesem Thema wird gezeigt, wie Sie die Mindesteinstellungen abschließen, die erforderlich sind, bevor der Produktmaster in den Stücklistenversionen verwendet werden kann.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd7e02c9aea17fbc3312660d0e50cd8bbf39aa3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845016"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="2c97f-103">Grundeinrichtung eines veröffentlichten Produktmasters abschließen</span><span class="sxs-lookup"><span data-stu-id="2c97f-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c97f-104">In diesem Thema wird gezeigt, wie Sie die Mindesteinstellungen abschließen, die erforderlich sind, bevor der Produktmaster in den Stücklistenversionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c97f-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="2c97f-105">Dies ist die dritte von acht Prozeduren, die beschreibt, wie Kombinationen für eine dimensionsbasierte Konfiguration erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c97f-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="2c97f-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="2c97f-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2c97f-107">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="2c97f-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c97f-109">Wählen Sie den Produktmaster aus, der in der zweiten Verfahren freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2c97f-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="2c97f-110">Dieser Produktmaster wird mit der Technologie der dimensionsbasierten Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c97f-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="2c97f-111">Klicken Sie im Aktivitätsbereich auf **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="2c97f-112">Klicken Sie auf **Dimensionsgruppen**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="2c97f-113">Wählen Sie im Feld **Lagerdimensionsgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2c97f-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c97f-115">Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen für Produktbuchung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c97f-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="2c97f-116">Wählen Sie **Standort** für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="2c97f-117">Wählen Sie im Feld **Rückverfolgungsgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2c97f-118">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c97f-119">Die Nachverfolgung der Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen für Produktbuchung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c97f-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="2c97f-120">Wählen Sie **Keine** für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="2c97f-121">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-121">Click **OK**.</span></span>
10. <span data-ttu-id="2c97f-122">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-122">Click **Edit**.</span></span>
11. <span data-ttu-id="2c97f-123">Wählen Sie im Feld **Artikelmodellgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="2c97f-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c97f-125">Lagersteuerungsgruppen enthalten Einstellungen, die bestimmen, wie Artikel beim Artikelzugang und -abgang gesteuert und gehandhabt werden.</span><span class="sxs-lookup"><span data-stu-id="2c97f-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="2c97f-126">Sie bestimmen auch, wie der Artikelverbrauch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="2c97f-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="2c97f-127">Wählen Sie **FIFO** für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="2c97f-128">Erweitern Sie den Abschnitt **Kosten verwalten**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="2c97f-129">Wählen Sie im Feld **Artikelgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2c97f-130">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c97f-131">Artikelgruppen werden verwendet, um Lagerartikel in Gruppen zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="2c97f-132">Wählen Sie **CarAudio** für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="2c97f-133">Wählen Sie im Aktivitätsbereich **Plan** aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="2c97f-134">Wählen Sie **Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="2c97f-135">Wählen Sie im Feld **Standardauftragstyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="2c97f-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="2c97f-136">Wählen Sie **Produktion** aus, um anzugeben, dass die standardmäßige Lieferoption für diesen Produktmaster ist, ihn zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="2c97f-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="2c97f-137">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-137">Select **Save**.</span></span>
20. <span data-ttu-id="2c97f-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c97f-138">Close the page.</span></span>
21. <span data-ttu-id="2c97f-139">Schließen Sie das Formular **Details für freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="2c97f-139">Close the **Released product details** form.</span></span>

