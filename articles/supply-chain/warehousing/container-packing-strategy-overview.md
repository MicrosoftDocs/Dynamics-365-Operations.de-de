---
title: Container-Packstrategien
description: Dieses Thema beschreibt die Unterschiede zwischen den Container-Packstrategien und gibt Beispiele.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292760"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="8002f-103">Container-Packstrategien</span><span class="sxs-lookup"><span data-stu-id="8002f-103">Container packing strategies</span></span>

<span data-ttu-id="8002f-104">Eine *Behälter-Packstrategie* ist eine Strategie, die Sie verwenden können, um Element-Zuordnungen über Container hinweg zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8002f-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="8002f-105">In diesem Thema werden die Unterschiede zwischen den Strategien *Packen in alle offenen Container* und *Nur in den aktuellen Container packen* erläutert.</span><span class="sxs-lookup"><span data-stu-id="8002f-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="8002f-106">**In alle offenen Container packen** – Das System muss alle offenen Container prüfen, die während des Containerisierungszyklus bereits erstellt wurden, um sicherzustellen, dass das Element in einen von ihnen passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="8002f-107">Während des Packens prüft das System jedes Element, um festzustellen, ob es in einen der zuvor erstellten Container passen wird.</span><span class="sxs-lookup"><span data-stu-id="8002f-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="8002f-108">Wenn das Element nicht in einen vorhandenen Container passt, erstellt das System einen neuen Container und fährt fort, bis es den gesamten Auftrag gepackt hat.</span><span class="sxs-lookup"><span data-stu-id="8002f-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="8002f-109">Zum Beispiel erfordern *n* bestellte Elemente eine Containerisierung.</span><span class="sxs-lookup"><span data-stu-id="8002f-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="8002f-110">Im schlimmsten Fall führt das System jedes Mal, wenn es ein Element verarbeitet, das in keinen vorhandenen Container passt, insgesamt (\[(*n* – 1) × (*n* + 1) \] ÷ 2) Überprüfungen durch, um festzustellen, ob das Element in die vorhandenen Container passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="8002f-111">**Nur in aktuellen Container packen** – Das System muss nur den zuletzt erstellten Container prüfen, um sicherzustellen, dass das Element in diesen passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="8002f-112">Während des Packens prüft das System jedes Element, um festzustellen, ob es in den zuletzt erstellten Container passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="8002f-113">Wenn das Element nicht in diesen Container passt, erstellt das System einen neuen Container und fährt fort, bis es den gesamten Auftrag gepackt hat.</span><span class="sxs-lookup"><span data-stu-id="8002f-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="8002f-114">Zum Beispiel erfordern *n* bestellte Elemente eine Containerisierung.</span><span class="sxs-lookup"><span data-stu-id="8002f-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="8002f-115">Im schlimmsten Fall führt das System insgesamt (*n* – 1) Überprüfungen durch, um festzustellen, ob das Element in die Container passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="8002f-116">Beispiel für den Flow für Container-Packstrategien</span><span class="sxs-lookup"><span data-stu-id="8002f-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="8002f-117">Sie legen die folgenden Elemente für die Containerisierung fest.</span><span class="sxs-lookup"><span data-stu-id="8002f-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="8002f-118">Artikel</span><span class="sxs-lookup"><span data-stu-id="8002f-118">Item</span></span> | <span data-ttu-id="8002f-119">Physikalische Dimensionen (Breite × Tiefe × Höhe)</span><span class="sxs-lookup"><span data-stu-id="8002f-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="8002f-120">Gewicht</span><span class="sxs-lookup"><span data-stu-id="8002f-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="8002f-121">HDMI-Kabel 6'</span><span class="sxs-lookup"><span data-stu-id="8002f-121">HDMI Cable 6'</span></span> | <span data-ttu-id="8002f-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="8002f-122">1 × 1 × 1</span></span> | <span data-ttu-id="8002f-123">1</span><span class="sxs-lookup"><span data-stu-id="8002f-123">1</span></span> |
| <span data-ttu-id="8002f-124">HDMI-Kabel 12'</span><span class="sxs-lookup"><span data-stu-id="8002f-124">HDMI Cable 12'</span></span> | <span data-ttu-id="8002f-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="8002f-125">2 × 1 × 1</span></span> | <span data-ttu-id="8002f-126">1</span><span class="sxs-lookup"><span data-stu-id="8002f-126">1</span></span> |
| <span data-ttu-id="8002f-127">HDMI-Kabel 18'</span><span class="sxs-lookup"><span data-stu-id="8002f-127">HDMI Cable 18'</span></span> | <span data-ttu-id="8002f-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="8002f-128">3 × 1 × 1</span></span> | <span data-ttu-id="8002f-129">2</span><span class="sxs-lookup"><span data-stu-id="8002f-129">2</span></span> |

<span data-ttu-id="8002f-130">Sie legen auch den folgenden Karton fest, der für die Verpackung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8002f-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="8002f-131">Container</span><span class="sxs-lookup"><span data-stu-id="8002f-131">Container</span></span> | <span data-ttu-id="8002f-132">Physikalische Dimensionen (Länge × Breite × Höhe)</span><span class="sxs-lookup"><span data-stu-id="8002f-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="8002f-133">Gewicht</span><span class="sxs-lookup"><span data-stu-id="8002f-133">Weight</span></span> | <span data-ttu-id="8002f-134">Volumen</span><span class="sxs-lookup"><span data-stu-id="8002f-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="8002f-135">Medium-Box</span><span class="sxs-lookup"><span data-stu-id="8002f-135">Medium Box</span></span> | <span data-ttu-id="8002f-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="8002f-136">6 × 3 × 2</span></span> | <span data-ttu-id="8002f-137">10</span><span class="sxs-lookup"><span data-stu-id="8002f-137">10</span></span> | <span data-ttu-id="8002f-138">100</span><span class="sxs-lookup"><span data-stu-id="8002f-138">100</span></span> |

<span data-ttu-id="8002f-139">Schließlich legen Sie eine Bestellung mit den folgenden Produkten und Mengen fest.</span><span class="sxs-lookup"><span data-stu-id="8002f-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="8002f-140">Auftragsposition</span><span class="sxs-lookup"><span data-stu-id="8002f-140">Sales order line</span></span> | <span data-ttu-id="8002f-141">Leistung</span><span class="sxs-lookup"><span data-stu-id="8002f-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="8002f-142">HDMI-Kabel 12'</span><span class="sxs-lookup"><span data-stu-id="8002f-142">HDMI Cable 12'</span></span> | <span data-ttu-id="8002f-143">9</span><span class="sxs-lookup"><span data-stu-id="8002f-143">9</span></span> |
| <span data-ttu-id="8002f-144">HDMI-Kabel 18'</span><span class="sxs-lookup"><span data-stu-id="8002f-144">HDMI Cable 18'</span></span> | <span data-ttu-id="8002f-145">8</span><span class="sxs-lookup"><span data-stu-id="8002f-145">8</span></span> |
| <span data-ttu-id="8002f-146">HDMI-Kabel 6'</span><span class="sxs-lookup"><span data-stu-id="8002f-146">HDMI Cable 6'</span></span> | <span data-ttu-id="8002f-147">13</span><span class="sxs-lookup"><span data-stu-id="8002f-147">13</span></span> |

<span data-ttu-id="8002f-148">Die folgende Tabelle fasst zusammen, wie die Containerisierung funktioniert, wenn Sie die Strategie *In alle offenen Container packen* und wenn Sie die Strategie *Nur in den aktuellen Container packen* verwenden.</span><span class="sxs-lookup"><span data-stu-id="8002f-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="8002f-149">In alle offenen Container packen</span><span class="sxs-lookup"><span data-stu-id="8002f-149">Pack into all open containers</span></span> | <span data-ttu-id="8002f-150">In den aktuellen Container packen</span><span class="sxs-lookup"><span data-stu-id="8002f-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="8002f-151">HDMI-Kabel 12':</span><span class="sxs-lookup"><span data-stu-id="8002f-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="8002f-152">Erzeugen Sie einen neuen Container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="8002f-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="8002f-153">Legen Sie 9 ea in den Container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="8002f-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="8002f-154">HDMI-Kabel 12':</span><span class="sxs-lookup"><span data-stu-id="8002f-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="8002f-155">Erzeugen Sie einen neuen Container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="8002f-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="8002f-156">Legen Sie 9 ea in den Container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="8002f-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="8002f-157">HDMI-Kabel 18':</span><span class="sxs-lookup"><span data-stu-id="8002f-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="8002f-158">Prüfen Sie, ob das Element in den Container CONT0001 passen kann.</span><span class="sxs-lookup"><span data-stu-id="8002f-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="8002f-159">Erzeugen Sie einen neuen Container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="8002f-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="8002f-160">Legen Sie 5 Stk. in den Container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="8002f-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="8002f-161">Erstellen Sie einen neuen Container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="8002f-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="8002f-162">Legen Sie 3 Stk. in den Container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="8002f-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="8002f-163">HDMI-Kabel 18':</span><span class="sxs-lookup"><span data-stu-id="8002f-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="8002f-164">Prüfen Sie, ob das Element in den Container CONT0001 passen kann.</span><span class="sxs-lookup"><span data-stu-id="8002f-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="8002f-165">Erzeugen Sie einen neuen Container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="8002f-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="8002f-166">Legen Sie 5 Stk. in den Container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="8002f-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="8002f-167">Erstellen Sie einen neuen Container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="8002f-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="8002f-168">Legen Sie 3 Stk. in den Container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="8002f-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="8002f-169">HDMI-Kabel 6':</span><span class="sxs-lookup"><span data-stu-id="8002f-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="8002f-170">Prüfen Sie, ob das Element in den Container CONT0001 passen kann.</span><span class="sxs-lookup"><span data-stu-id="8002f-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="8002f-171">Legen Sie 1 ea in den Container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="8002f-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="8002f-172">Prüfen Sie, ob das Element in den Container CONT0002 passen kann.</span><span class="sxs-lookup"><span data-stu-id="8002f-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="8002f-173">Prüfen Sie, ob das Element in den Container CONT0003 passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="8002f-174">Legen Sie 4 ea in den Container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="8002f-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="8002f-175">Erzeugen Sie einen neuen Container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="8002f-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="8002f-176">Legen Sie 8 Stk. in den Container CONT0004.</span><span class="sxs-lookup"><span data-stu-id="8002f-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="8002f-177">HDMI-Kabel 6':</span><span class="sxs-lookup"><span data-stu-id="8002f-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="8002f-178">Prüfen Sie, ob das Element in den Container CONT0003 passt.</span><span class="sxs-lookup"><span data-stu-id="8002f-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="8002f-179">Legen Sie 4 ea in den Container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="8002f-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="8002f-180">Erzeugen Sie einen neuen Container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="8002f-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="8002f-181">Legen Sie 9 ea in den Container CONT0004.</span><span class="sxs-lookup"><span data-stu-id="8002f-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="8002f-182">Beispielszenario: Einzelne Aufträge pro Container verpacken</span><span class="sxs-lookup"><span data-stu-id="8002f-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="8002f-183">In diesem Abschnitt wird ein Szenario vorgestellt, bei dem das System so festgelegt ist, dass mehrere Bestellungen in einer Sendung zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="8002f-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="8002f-184">Daher wird die Containerisierung vom Verkaufsauftrag aus durchgeführt, um sicherzustellen, dass jeder Auftrag, der mehrere Produkte enthält, in einen eigenen Container gepackt wird.</span><span class="sxs-lookup"><span data-stu-id="8002f-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="8002f-185">Mit dieser Funktionalität können Sie Szenarien handhaben, in denen Sie nur einen Verkaufsauftrag in jeden Container packen müssen, damit das Distributionszentrum volle Container zwischen den Einzelhandelsgeschäften cross-docken kann.</span><span class="sxs-lookup"><span data-stu-id="8002f-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="8002f-186">Zusätzlich zu den Einzelhandelsszenarien (Auftrag pro Einzelhandelsgeschäft und Versand an ein Distributionszentrum für Cross-Docking) wird diese Technik auch allgemein in schlanken Vorratsketten (Verkaufsauftrag pro Just-in-Time-Produktionslinie) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8002f-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="8002f-187">Dieses Szenario zeigt, wie Sie die Anzahl der Container, die beim Packen ausgewertet werden, verringern können, indem Sie die Strategie *Nur in aktuellen Container packen* für die Containerisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8002f-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8002f-188">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8002f-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="8002f-189">Aktivieren Sie die Funktion „Sendungen konsolidieren“ in Ihrem System</span><span class="sxs-lookup"><span data-stu-id="8002f-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="8002f-190">Dieses Szenario verwendet die Funktion *Sendungen konsolidieren*.</span><span class="sxs-lookup"><span data-stu-id="8002f-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="8002f-191">Wenn diese Funktion in Ihrem System noch nicht vorhanden ist, müssen Sie sie mit [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) einschalten.</span><span class="sxs-lookup"><span data-stu-id="8002f-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="8002f-192">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="8002f-192">Make demo data available</span></span>

<span data-ttu-id="8002f-193">Dieses Szenario referenziert Werte und Datensätze, die in den Standard-Demodaten enthalten sind, die für Microsoft Dynamics 365 Supply Chain Management zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8002f-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8002f-194">Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="8002f-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="8002f-195">Containertypen inspizieren oder erstellen</span><span class="sxs-lookup"><span data-stu-id="8002f-195">Inspect or create container types</span></span>

<span data-ttu-id="8002f-196">Um Ihre Containertypen zu inspizieren oder bei Bedarf neue Containertypen zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="8002f-197">Gehen Sie zu **Lagerortverwaltung** \> **Einrichten** \> **Behälter** \> **Behältertypen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="8002f-198">Stellen Sie sicher, dass jeder der folgenden Container-Typen in Ihren Demo-Daten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8002f-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="8002f-199">Bearbeiten oder erstellen Sie die Containertypen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="8002f-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="8002f-200">Container-Typ 1:</span><span class="sxs-lookup"><span data-stu-id="8002f-200">Container type 1:</span></span>

        - <span data-ttu-id="8002f-201">**Containertyp-Code:** *Box-Large*</span><span class="sxs-lookup"><span data-stu-id="8002f-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="8002f-202">**Beschreibung:** *Große Box*</span><span class="sxs-lookup"><span data-stu-id="8002f-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="8002f-203">**Maximales Nettogewicht:** *100*</span><span class="sxs-lookup"><span data-stu-id="8002f-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="8002f-204">**Volumen:** *400*</span><span class="sxs-lookup"><span data-stu-id="8002f-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="8002f-205">**Länge:** *4*</span><span class="sxs-lookup"><span data-stu-id="8002f-205">**Length:** *4*</span></span>
        - <span data-ttu-id="8002f-206">**Breite:** *10*</span><span class="sxs-lookup"><span data-stu-id="8002f-206">**Width:** *10*</span></span>
        - <span data-ttu-id="8002f-207">**Höhe:** *10*</span><span class="sxs-lookup"><span data-stu-id="8002f-207">**Height:** *10*</span></span>

    - <span data-ttu-id="8002f-208">Container Typ 2:</span><span class="sxs-lookup"><span data-stu-id="8002f-208">Container type 2:</span></span>

        - <span data-ttu-id="8002f-209">**Container-Typ-Code:** *Box-Medium*</span><span class="sxs-lookup"><span data-stu-id="8002f-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="8002f-210">**Beschreibung:** *Medium Box*</span><span class="sxs-lookup"><span data-stu-id="8002f-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="8002f-211">**Maximales Nettogewicht:** *50*</span><span class="sxs-lookup"><span data-stu-id="8002f-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="8002f-212">**Volumen:** *200*</span><span class="sxs-lookup"><span data-stu-id="8002f-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="8002f-213">**Länge:** *2*</span><span class="sxs-lookup"><span data-stu-id="8002f-213">**Length:** *2*</span></span>
        - <span data-ttu-id="8002f-214">**Breite:** *10*</span><span class="sxs-lookup"><span data-stu-id="8002f-214">**Width:** *10*</span></span>
        - <span data-ttu-id="8002f-215">**Höhe:** *10*</span><span class="sxs-lookup"><span data-stu-id="8002f-215">**Height:** *10*</span></span>

    - <span data-ttu-id="8002f-216">Container-Typ 3:</span><span class="sxs-lookup"><span data-stu-id="8002f-216">Container type 3:</span></span>

        - <span data-ttu-id="8002f-217">**Containertyp-Code:** *Box-Small*</span><span class="sxs-lookup"><span data-stu-id="8002f-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="8002f-218">**Beschreibung:** *Kleine Box*</span><span class="sxs-lookup"><span data-stu-id="8002f-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="8002f-219">**Maximales Nettogewicht:** *20*</span><span class="sxs-lookup"><span data-stu-id="8002f-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="8002f-220">**Volumen:** *100*</span><span class="sxs-lookup"><span data-stu-id="8002f-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="8002f-221">**Länge:** *1*</span><span class="sxs-lookup"><span data-stu-id="8002f-221">**Length:** *1*</span></span>
        - <span data-ttu-id="8002f-222">**Breite:** *10*</span><span class="sxs-lookup"><span data-stu-id="8002f-222">**Width:** *10*</span></span>
        - <span data-ttu-id="8002f-223">**Höhe:** *10*</span><span class="sxs-lookup"><span data-stu-id="8002f-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="8002f-224">Containergruppen inspizieren oder erstellen</span><span class="sxs-lookup"><span data-stu-id="8002f-224">Inspect or create container groups</span></span>

<span data-ttu-id="8002f-225">Führen Sie die folgenden Schritte aus, um Ihre Container-Gruppen zu inspizieren oder neue Container-Gruppen zu erstellen, falls diese benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8002f-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="8002f-226">Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containergruppen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="8002f-227">Stellen Sie sicher, dass die folgende Containergruppe in Ihren Demodaten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8002f-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="8002f-228">Wenn sie nicht vorhanden ist, wählen Sie **Neu**, um sie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8002f-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="8002f-229">**Containergruppen-ID:** *Boxen*</span><span class="sxs-lookup"><span data-stu-id="8002f-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="8002f-230">**Beschreibung:** *Boxengrößen*</span><span class="sxs-lookup"><span data-stu-id="8002f-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="8002f-231">Stellen Sie im Inforegister **Details** für die Container-Gruppe *Boxen* sicher, dass die folgenden Zeilen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8002f-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="8002f-232">Wenn sie nicht vorhanden sind, wählen Sie **Neu**, um sie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8002f-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="8002f-233">Position 1:</span><span class="sxs-lookup"><span data-stu-id="8002f-233">Line 1:</span></span>

        - <span data-ttu-id="8002f-234">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="8002f-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="8002f-235">**Containertyp:** *Box-Groß*</span><span class="sxs-lookup"><span data-stu-id="8002f-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="8002f-236">**Container-Auslastung in Prozent:** *100*</span><span class="sxs-lookup"><span data-stu-id="8002f-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="8002f-237">Position 2:</span><span class="sxs-lookup"><span data-stu-id="8002f-237">Line 2:</span></span>

        - <span data-ttu-id="8002f-238">**Sequenznummer:** *2*</span><span class="sxs-lookup"><span data-stu-id="8002f-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="8002f-239">**Container-Typ:** *Box-Medium*</span><span class="sxs-lookup"><span data-stu-id="8002f-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="8002f-240">**Container-Auslastung in Prozent:** *100*</span><span class="sxs-lookup"><span data-stu-id="8002f-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="8002f-241">Position 3:</span><span class="sxs-lookup"><span data-stu-id="8002f-241">Line 3:</span></span>

        - <span data-ttu-id="8002f-242">**Sequenznummer:** *3*</span><span class="sxs-lookup"><span data-stu-id="8002f-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="8002f-243">**Container-Typ:** *Box-Small*</span><span class="sxs-lookup"><span data-stu-id="8002f-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="8002f-244">**Container-Auslastung in Prozent:** *100*</span><span class="sxs-lookup"><span data-stu-id="8002f-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="8002f-245">Erstellen einer neuen Container-Bauvorlage</span><span class="sxs-lookup"><span data-stu-id="8002f-245">Create a new container build template</span></span>

<span data-ttu-id="8002f-246">Um eine neue Container-Bauvorlage zu erstellen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="8002f-247">Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containererstellungsvorlage**.</span><span class="sxs-lookup"><span data-stu-id="8002f-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="8002f-248">Wählen Sie **Neu**, um eine Container-Vorlage zu erstellen, die die folgenden Einstellungen hat:</span><span class="sxs-lookup"><span data-stu-id="8002f-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="8002f-249">**Sequenznummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="8002f-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="8002f-250">**Container-Vorlagen-ID:** *Box*</span><span class="sxs-lookup"><span data-stu-id="8002f-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="8002f-251">**Containergruppen-ID:** *Boxen*</span><span class="sxs-lookup"><span data-stu-id="8002f-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="8002f-252">**Basisabfragetypen:** *Verkaufszuordnung Zeile*</span><span class="sxs-lookup"><span data-stu-id="8002f-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="8002f-253">**Wellenschritt-Code:** *234*</span><span class="sxs-lookup"><span data-stu-id="8002f-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="8002f-254">**Geteiltes Kommissionieren zulassen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="8002f-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="8002f-255">**Packstrategie für Container:** *Nur in den aktuellen Container packen*</span><span class="sxs-lookup"><span data-stu-id="8002f-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="8002f-256">**Packen nach Einheit der Richtlinie:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="8002f-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="8002f-257">Während die Zeile für die neue Vorlage noch ausgewählt ist, wählen Sie im Aktionsbereich **Abfrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8002f-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="8002f-258">Ein Standard-Dialogfeld für den Abfrage-Editor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8002f-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="8002f-259">Wählen Sie auf der Registerkarte **Sortierung** die Option **Hinzufügen**, um eine Zeile hinzuzufügen, die die folgenden Einstellungen hat:</span><span class="sxs-lookup"><span data-stu-id="8002f-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="8002f-260">**Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="8002f-261">**Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="8002f-262">**Feld:** *Bestellnummer*</span><span class="sxs-lookup"><span data-stu-id="8002f-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="8002f-263">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="8002f-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8002f-264">Um zu vermeiden, dass alle anderen geöffneten Container durchlaufen werden, und um den Vorgang zu beschleunigen, indem jeweils nur ein Container geprüft wird, verwenden Sie zusätzlich zur Sortierung nach Auftragsnummer die Strategie *Nur in aktuellen Container packen*.</span><span class="sxs-lookup"><span data-stu-id="8002f-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="8002f-265">Diese Kombination funktioniert wie eine Arbeitspause bei einer Arbeitsvorlage.</span><span class="sxs-lookup"><span data-stu-id="8002f-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="8002f-266">Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8002f-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8002f-267">Während die Zeile für die neue Vorlage noch ausgewählt ist, wählen Sie **Container-Mischbedingungen** im Aktionsbereich.</span><span class="sxs-lookup"><span data-stu-id="8002f-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="8002f-268">Sie fügen nun eine Beschränkung hinzu, die Elemente aus einem einzigen Auftrag in einen einzigen Container legt.</span><span class="sxs-lookup"><span data-stu-id="8002f-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="8002f-269">Elemente aus allen anderen Aufträgen werden in einen separaten Container gelegt.</span><span class="sxs-lookup"><span data-stu-id="8002f-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="8002f-270">Wählen Sie **Neu**, um eine Mischungsbeschränkung zu erstellen, die die folgenden Einstellungen hat:</span><span class="sxs-lookup"><span data-stu-id="8002f-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="8002f-271">**Tabelle:** *Aufträge*</span><span class="sxs-lookup"><span data-stu-id="8002f-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="8002f-272">**Feldauswahl:** *VerkaufsId* (Das Feld wird als *Verkaufsauftrag* im Raster angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="8002f-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="8002f-273">Wählen Sie **OK**, um die Einschränkung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8002f-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="8002f-274">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="8002f-275">Eine Wellenvorlage für die Containerisierung festlegen</span><span class="sxs-lookup"><span data-stu-id="8002f-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="8002f-276">Um eine Wellenvorlage festzulegen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="8002f-277">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="8002f-278">Legen Sie im Listenbereich das Feld **Wellenvorlagentyp** auf *Versand* fest.</span><span class="sxs-lookup"><span data-stu-id="8002f-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="8002f-279">Wählen Sie die Vorlage **63 Containerisierung** in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="8002f-280">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8002f-281">Suchen Sie im Inforegister **Methoden** in der Spalte **Ausgewählte Methoden** die folgende Position:</span><span class="sxs-lookup"><span data-stu-id="8002f-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="8002f-282">**Methodenname:** *Containerisierung*</span><span class="sxs-lookup"><span data-stu-id="8002f-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="8002f-283">**Name:** *Kontainerisierung*</span><span class="sxs-lookup"><span data-stu-id="8002f-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="8002f-284">Legen Sie das Feld **Wellenschrittcode** für die Zeile auf *234* fest.</span><span class="sxs-lookup"><span data-stu-id="8002f-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="8002f-285">Eine Arbeitsvorlage einrichten</span><span class="sxs-lookup"><span data-stu-id="8002f-285">Set up a work template</span></span>

<span data-ttu-id="8002f-286">Um eine Arbeitsvorlage festzulegen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="8002f-287">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8002f-288">Legen Sie das Feld **Arbeitsauftragstyp** auf *Verkaufsaufträge* fest.</span><span class="sxs-lookup"><span data-stu-id="8002f-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="8002f-289">Suchen Sie im Raster **Übersicht** die Arbeitsvorlage, die für das Verpacken einzelner Aufträge pro Container verwendet werden soll, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="8002f-290">Wählen Sie für dieses Szenario die Vorlage **63 In Container kommissionieren**.</span><span class="sxs-lookup"><span data-stu-id="8002f-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="8002f-291">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8002f-292">Ein Standard-Dialogfeld für den Abfrage-Editor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8002f-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="8002f-293">Fügen Sie auf der Registerkarte **Sortierung** die folgenden Zeilen ein:</span><span class="sxs-lookup"><span data-stu-id="8002f-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="8002f-294">Position 1:</span><span class="sxs-lookup"><span data-stu-id="8002f-294">Line 1:</span></span>

        - <span data-ttu-id="8002f-295">**Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8002f-296">**Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8002f-297">**Feld:** *Lieferungs-ID*</span><span class="sxs-lookup"><span data-stu-id="8002f-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="8002f-298">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="8002f-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="8002f-299">Position 2:</span><span class="sxs-lookup"><span data-stu-id="8002f-299">Line 2:</span></span>

        - <span data-ttu-id="8002f-300">**Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8002f-301">**Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8002f-302">**Feld:** *Bestellnummer*</span><span class="sxs-lookup"><span data-stu-id="8002f-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="8002f-303">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="8002f-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="8002f-304">Position 3:</span><span class="sxs-lookup"><span data-stu-id="8002f-304">Line 3:</span></span>

        - <span data-ttu-id="8002f-305">**Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8002f-306">**Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="8002f-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8002f-307">**Feld:** *Container-ID*</span><span class="sxs-lookup"><span data-stu-id="8002f-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="8002f-308">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="8002f-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8002f-309">Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8002f-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8002f-310">Die folgende Meldung wird angezeigt: „Gruppierung wird zurückgesetzt, fortfahren?“</span><span class="sxs-lookup"><span data-stu-id="8002f-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="8002f-311">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="8002f-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="8002f-312">Während die Vorlage **63 Entnahme in Container** noch immer kommissioniert ist, wählen Sie im Aktionsbereich **Arbeitskopfunterbrechungen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="8002f-313">Sie werden nun Einstellungen anwenden, um die Arbeit so zu unterbrechen, dass jeder Container im Auftrag mit einem Arbeitsauftrag verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8002f-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="8002f-314">Aktivieren Sie das Kontrollkästchen **Nach diesem Feld gruppieren** für jede Zeile auf der Seite **Arbeitskopf-Unterbrechungen** (**Sendungs-ID**, **Auftragsnummer** und **Container-ID**).</span><span class="sxs-lookup"><span data-stu-id="8002f-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="8002f-315">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="8002f-316">Richtlinien für die Sendungskonsolidierung festlegen</span><span class="sxs-lookup"><span data-stu-id="8002f-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="8002f-317">Um eine Richtlinie zur Sendungskonsolidierung festzulegen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="8002f-318">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.</span><span class="sxs-lookup"><span data-stu-id="8002f-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="8002f-319">Legen Sie im Listenbereich das Feld **Richtlinientyp** auf *Verkaufsaufträge* fest.</span><span class="sxs-lookup"><span data-stu-id="8002f-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="8002f-320">Wählen Sie die Richtlinie **Standard** in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="8002f-321">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8002f-322">Wählen Sie im Inforegister **Konsolidierungsfelder** in der Liste **Ausgewählte Felder** die Zeile, in der das Feld **Feldname** auf *Auftragsnummer* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8002f-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="8002f-323">Wählen Sie die Schaltfläche **Entfernen** ![Linker Pfeil ](media/backward-button.png), um das Feld in die Liste **Restliche Felder** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="8002f-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="8002f-324">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="8002f-325">Festlegen der physikalischen Dimensionen für das Produkt</span><span class="sxs-lookup"><span data-stu-id="8002f-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="8002f-326">Um die physikalischen Dimensionen für die Produkte festzulegen, die in diesem Szenario verwendet werden, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="8002f-327">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="8002f-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8002f-328">Wählen Sie das Produkt, bei dem das Feld **Artikelnummer** auf *A0001* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8002f-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="8002f-329">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** **Physische Dimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="8002f-330">Auf der Seite **Physikalische Dimensionen** sollten Sie die folgende Zeile im Raster sehen:</span><span class="sxs-lookup"><span data-stu-id="8002f-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="8002f-331">**Einheit:** *Stk*</span><span class="sxs-lookup"><span data-stu-id="8002f-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="8002f-332">**Bruttogewicht:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="8002f-333">**Breite:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="8002f-334">**Tiefe:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="8002f-335">**Höhe:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="8002f-336">**Volumen:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="8002f-337">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-337">Close the page.</span></span>
1. <span data-ttu-id="8002f-338">Wählen Sie das Produkt, bei dem das Feld **Artikelnummer** auf *A0002* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8002f-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="8002f-339">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** **Physische Dimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="8002f-340">Auf der Seite **Physikalische Dimensionen** sollten Sie die folgende Zeile im Raster sehen:</span><span class="sxs-lookup"><span data-stu-id="8002f-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="8002f-341">**Einheit:** *Stück*</span><span class="sxs-lookup"><span data-stu-id="8002f-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="8002f-342">**Bruttogewicht:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="8002f-343">**Breite:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="8002f-344">**Tiefe:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="8002f-345">**Höhe:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="8002f-346">**Volumen:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="8002f-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="8002f-347">Auftrag 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="8002f-347">Create sales order 1</span></span>

<span data-ttu-id="8002f-348">Gehen Sie folgendermaßen vor, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8002f-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="8002f-349">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="8002f-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8002f-350">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8002f-351">Es erscheint ein Dialogfenster zum Erstellen eines neuen Verkaufsauftrags.</span><span class="sxs-lookup"><span data-stu-id="8002f-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="8002f-352">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="8002f-352">Set the following values:</span></span>

    - <span data-ttu-id="8002f-353">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8002f-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8002f-354">**Lagerort:** *63*</span><span class="sxs-lookup"><span data-stu-id="8002f-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8002f-355">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8002f-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8002f-356">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8002f-356">The new sales order is opened.</span></span> <span data-ttu-id="8002f-357">Fügen Sie auf dem Inforegister **Verkaufsauftragszeilen** die folgenden Verkaufszeilen hinzu:</span><span class="sxs-lookup"><span data-stu-id="8002f-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="8002f-358">Position 1:</span><span class="sxs-lookup"><span data-stu-id="8002f-358">Line 1:</span></span>

        - <span data-ttu-id="8002f-359">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="8002f-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8002f-360">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="8002f-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="8002f-361">Position 2:</span><span class="sxs-lookup"><span data-stu-id="8002f-361">Line 2:</span></span>

        - <span data-ttu-id="8002f-362">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8002f-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8002f-363">**Menge** *2*</span><span class="sxs-lookup"><span data-stu-id="8002f-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="8002f-364">Markieren Sie die erste Zeile und wählen Sie dann **Bestand \> Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="8002f-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="8002f-365">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="8002f-366">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-366">Then close the page.</span></span>
1. <span data-ttu-id="8002f-367">Wiederholen Sie die beiden vorherigen Schritte für die zweite Zeile.</span><span class="sxs-lookup"><span data-stu-id="8002f-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="8002f-368">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="8002f-369">Auftrag 2 erstellen</span><span class="sxs-lookup"><span data-stu-id="8002f-369">Create sales order 2</span></span>

<span data-ttu-id="8002f-370">Um einen zweiten Verkaufsauftrag zu erstellen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="8002f-371">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="8002f-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8002f-372">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8002f-373">Es erscheint ein Dialogfenster zum Erstellen eines neuen Verkaufsauftrags.</span><span class="sxs-lookup"><span data-stu-id="8002f-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="8002f-374">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="8002f-374">Set the following values:</span></span>

    - <span data-ttu-id="8002f-375">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8002f-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8002f-376">**Lagerort:** *63*</span><span class="sxs-lookup"><span data-stu-id="8002f-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8002f-377">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8002f-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8002f-378">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8002f-378">The new sales order is opened.</span></span> <span data-ttu-id="8002f-379">Fügen Sie auf dem Inforegister **Verkaufsauftragszeilen** die folgenden Verkaufszeilen hinzu:</span><span class="sxs-lookup"><span data-stu-id="8002f-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="8002f-380">Position 1:</span><span class="sxs-lookup"><span data-stu-id="8002f-380">Line 1:</span></span>

        - <span data-ttu-id="8002f-381">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="8002f-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8002f-382">**Menge** *4*</span><span class="sxs-lookup"><span data-stu-id="8002f-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="8002f-383">Position 2:</span><span class="sxs-lookup"><span data-stu-id="8002f-383">Line 2:</span></span>

        - <span data-ttu-id="8002f-384">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8002f-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8002f-385">**Menge** *4*</span><span class="sxs-lookup"><span data-stu-id="8002f-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="8002f-386">Markieren Sie die erste Zeile und wählen Sie dann **Bestand \> Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="8002f-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="8002f-387">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="8002f-388">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-388">Then close the page.</span></span>
1. <span data-ttu-id="8002f-389">Wiederholen Sie die beiden vorherigen Schritte für die zweite Zeile.</span><span class="sxs-lookup"><span data-stu-id="8002f-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="8002f-390">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8002f-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="8002f-391">Erstellen Sie die Ladung</span><span class="sxs-lookup"><span data-stu-id="8002f-391">Create the load</span></span>

<span data-ttu-id="8002f-392">Um für jeden Auftrag, den Sie für dieses Szenario erstellt haben, eine Ladung zu erstellen und diese dann an den Lagerort freizugeben, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8002f-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="8002f-393">Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="8002f-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="8002f-394">Suchen Sie auf der Registerkarte **Verkaufszeilen** alle Verkaufsauftragszeilen aus den Kundenaufträgen, die Sie für dieses Szenario erstellt haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="8002f-395">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zu neuer Ladung** aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="8002f-396">Die ausgewählten Auftragszeilen werden zu einer neuen Ladung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8002f-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="8002f-397">Wählen Sie im Dialogfeld **Ladungsvorlagenzuordnung** im Feld **Ladungsvorlagen-ID** eine Ladungsvorlage, z. B. *40' Container*.</span><span class="sxs-lookup"><span data-stu-id="8002f-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="8002f-398">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8002f-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="8002f-399">Suchen Sie im Abschnitt **Ladungen** die Ladung, die Sie gerade erstellt haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="8002f-400">Wählen Sie **Freigabe \> Freigabe an Lagerort**.</span><span class="sxs-lookup"><span data-stu-id="8002f-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="8002f-401">Wählen Sie im Dialogfeld **Freigeben an Lager** die Option **OK**, um die ausgewählte Ladung an das Lagerort freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8002f-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="8002f-402">Überprüfen der Sendungen und Container</span><span class="sxs-lookup"><span data-stu-id="8002f-402">Verify the shipments and containers</span></span>

<span data-ttu-id="8002f-403">Mit dem folgenden Verfahren können Sie die erstellten Sendungen verifizieren.</span><span class="sxs-lookup"><span data-stu-id="8002f-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="8002f-404">Verwenden Sie es, um den Auftrag zu überprüfen, den Sie für dieses Szenario erstellt haben, um sicherzustellen, dass Sie die erwarteten Ergebnisse erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="8002f-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="8002f-405">Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="8002f-406">Suchen Sie die Sendung, die für die Ladung erstellt wurde, die Sie gerade freigegeben haben, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="8002f-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="8002f-407">Wählen Sie im Aktionsbereich auf der Registerkarte **Transportieren** die Option **Container anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="8002f-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="8002f-408">Bestätigen Sie, dass die Elemente aus den Verkaufsaufträgen in zwei verschiedene Container verpackt wurden.</span><span class="sxs-lookup"><span data-stu-id="8002f-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8002f-409">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8002f-409">Additional resources</span></span>

- [<span data-ttu-id="8002f-410">Containerisierung</span><span class="sxs-lookup"><span data-stu-id="8002f-410">Containerization</span></span>](wave-containerization.md)
