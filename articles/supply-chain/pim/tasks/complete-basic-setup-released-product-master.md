---
title: Grundeinrichtung eines veröffentlichten Produktmasters abschließen
description: Im folgenden Verfahren, wie die erforderlichen Mindesteinstellungen abschließt, die erforderlich ist, bevor der Produktmaster in den Stücklistenversionen verwendet werden kann.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354781"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="695e7-103">Grundeinrichtung eines veröffentlichten Produktmasters abschließen</span><span class="sxs-lookup"><span data-stu-id="695e7-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="695e7-104">Im folgenden Verfahren, wie die erforderlichen Mindesteinstellungen abschließt, die erforderlich ist, bevor der Produktmaster in den Stücklistenversionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="695e7-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="695e7-105">Dies ist die dritte von acht Prozeduren, die beschreibt, wie Kombinationen für eine dimensionsbasierte Konfiguration erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="695e7-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="695e7-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="695e7-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="695e7-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="695e7-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="695e7-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="695e7-109">Wählen Sie den Produktmaster aus, der in der zweiten Verfahren freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="695e7-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="695e7-110">Dieser Produktmaster wird mit der Technologie der dimensionsbasierten Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="695e7-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="695e7-111">Klicken Sie im Aktivitätsbereich auf "Produkt".</span><span class="sxs-lookup"><span data-stu-id="695e7-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="695e7-112">Klicken Sie auf "Dimensionsgruppen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="695e7-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="695e7-113">Klicken Sie im Feld "Lagerdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="695e7-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="695e7-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="695e7-115">Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen für Produktbuchung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="695e7-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="695e7-116">Wählen Sie Anforderungen dieser Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="695e7-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="695e7-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="695e7-118">Klicken Sie im Feld "Rückverfolgungsangaben-Gruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="695e7-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="695e7-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="695e7-120">Die Nachverfolgung der Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen für Produktbuchung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="695e7-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="695e7-121">Wählen Sie Anforderungen dieser Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="695e7-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="695e7-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="695e7-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="695e7-123">Click OK.</span></span>
12. <span data-ttu-id="695e7-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="695e7-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="695e7-125">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="695e7-125">Click Edit.</span></span>
    * <span data-ttu-id="695e7-126">Öffnen Sie die Details für freigegebene Produkte ", um die Einstellungsaufgabe fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="695e7-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="695e7-127">Klicken Sie im Feld "Artikelmodellgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="695e7-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="695e7-128">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="695e7-129">Lagersteuerungsgruppen enthalten Einstellungen, die bestimmen, wie Artikel beim Artikelzugang und -abgang gesteuert und gehandhabt werden.</span><span class="sxs-lookup"><span data-stu-id="695e7-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="695e7-130">Sie bestimmen auch, wie der Artikelverbrauch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="695e7-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="695e7-131">Wählen Sie FIFO für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="695e7-132">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="695e7-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="695e7-133">Erweitern oder reduzieren Sie den Abschnitt "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="695e7-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="695e7-134">Klicken Sie im Feld "Artikelgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="695e7-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="695e7-135">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="695e7-136">Artikelgruppen werden verwendet, um Lagerartikel in Gruppen zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="695e7-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="695e7-137">Wählen Sie   CarAudio für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="695e7-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="695e7-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="695e7-139">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="695e7-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="695e7-140">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="695e7-140">Click Default order settings.</span></span>
23. <span data-ttu-id="695e7-141">Wählen Sie im Feld "Arbeitsauftragstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="695e7-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="695e7-142">Wählen Sie Produktion aus, um anzugeben, dass die standardmäßige Zubehöroption für diesen Produktmaster, sie zu erzeugen ist.</span><span class="sxs-lookup"><span data-stu-id="695e7-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="695e7-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="695e7-143">Close the page.</span></span>
25. <span data-ttu-id="695e7-144">Schließen Sie das Formular 'Details für freigegebene Produkte'.</span><span class="sxs-lookup"><span data-stu-id="695e7-144">Close the Released product details form.</span></span>

