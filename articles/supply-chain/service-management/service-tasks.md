---
title: Serviceaufgaben
description: "Serviceaufgaben dienen zum Beschreiben der Aufgabe, die im Zuge eines Serviceauftrags auszuführen ist. Diese Informationen stehen sowohl dem Techniker als auch dem Debitor zur Verfügung."
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="service-tasks"></a><span data-ttu-id="beaae-104">Serviceaufgaben</span><span class="sxs-lookup"><span data-stu-id="beaae-104">Service tasks</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="beaae-105">Serviceaufgaben dienen zum Beschreiben der Aufgabe, die im Zuge eines Serviceauftrags auszuführen ist.</span><span class="sxs-lookup"><span data-stu-id="beaae-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="beaae-106">Diese Informationen stehen sowohl dem Techniker als auch dem Debitor zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="beaae-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="beaae-107">Die Erstellung von Serviceaufgaben erfolgt im Formular **Serviceaufgaben**. Durch Erstellen von Serviceaufgabenbeziehungen werden die Serviceaufgaben einer bestimmten Servicevereinbarung oder einem bestimmten Serviceauftrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="beaae-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="beaae-108">Zusammen mit einer Serviceaufgabenbeziehung können Sie auch Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="beaae-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="beaae-109">Interne Hinweise für die Aufgabe (beispielsweise ausführliche technische Informationen, die dem Techniker bekannt sein müssen).</span><span class="sxs-lookup"><span data-stu-id="beaae-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="beaae-110">Externe Hinweise für den Debitor.</span><span class="sxs-lookup"><span data-stu-id="beaae-110">External notes that the customer can see.</span></span> <span data-ttu-id="beaae-111">Hier kann beispielsweise eine allgemein verständlichere Beschreibung der Aufgabe angegeben werden, die im Rahmen der zwischen Debitor und Serviceunternehmen bestehenden Vereinbarung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beaae-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="beaae-112">Nach dem Einrichten einer Serviceaufgabenbeziehung zwischen einer Serviceaufgabe und einem Serviceauftrag oder einer Servicevereinbarung kann die entsprechende Serviceaufgabe beim Erstellen von Serviceauftrags- oder Servicevereinbarungspositionen für den aktuellen Serviceauftrag bzw. für die aktuelle Servicevereinbarung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="beaae-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="beaae-113">Wird ein Serviceauftrag auf Basis einer Servicevereinbarung erstellt, können Serviceauftragspositionen mithilfe der den einzelnen Servicevereinbarungspositionen zugewiesenen Serviceaufgaben zu Serviceaufträgen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="beaae-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="beaae-114">Erstellen von Serviceaufgaben</span><span class="sxs-lookup"><span data-stu-id="beaae-114">Create a service task</span></span>

1. <span data-ttu-id="beaae-115">Klicken Sie auf **Dienstleistungsverwaltung** \> **Einrichtung** \> **Dienstleistungsaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="beaae-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="beaae-116">Erstellen Sie eine neue Position.</span><span class="sxs-lookup"><span data-stu-id="beaae-116">Create a new line.</span></span>
3. <span data-ttu-id="beaae-117">Geben Sie die Servicekennung sowie eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="beaae-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="beaae-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="beaae-118">Example</span></span>

<span data-ttu-id="beaae-119">Ein Techniker soll vor Ort zwei Aufgaben an einem Getriebe ausführen (Serviceobjekt: "GB-1234").</span><span class="sxs-lookup"><span data-stu-id="beaae-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="beaae-120">Für den Debitor wird eine Servicevereinbarung erstellt, und den Aufgaben werden mehrere Buchungen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="beaae-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="beaae-121">Im Anschluss sind die Servicevereinbarung sowie die Vereinbarungspositionen für die beiden Aufgaben aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="beaae-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="beaae-122">Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="beaae-122">Service agreement</span></span>

| <span data-ttu-id="beaae-123">Project</span><span class="sxs-lookup"><span data-stu-id="beaae-123">Project</span></span> | <span data-ttu-id="beaae-124">Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="beaae-124">Service agreement</span></span> | <span data-ttu-id="beaae-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beaae-125">Description</span></span>                                  | <span data-ttu-id="beaae-126">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="beaae-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="beaae-127">9012</span><span class="sxs-lookup"><span data-stu-id="beaae-127">9012</span></span>    | <span data-ttu-id="beaae-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="beaae-128">000008\_001</span></span>       | <span data-ttu-id="beaae-129">Inspektion und routinemäßige Erneuerung – GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="beaae-130">Zulage</span><span class="sxs-lookup"><span data-stu-id="beaae-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="beaae-131">Servicevertragspositionen</span><span class="sxs-lookup"><span data-stu-id="beaae-131">Service agreement lines</span></span>

| <span data-ttu-id="beaae-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beaae-132">Description</span></span>             | <span data-ttu-id="beaae-133">Buchungsart</span><span class="sxs-lookup"><span data-stu-id="beaae-133">Transaction type</span></span> | <span data-ttu-id="beaae-134">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="beaae-134">Service object</span></span> | <span data-ttu-id="beaae-135">Serviceaufgabe</span><span class="sxs-lookup"><span data-stu-id="beaae-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="beaae-136">Inspektion und Reinigung</span><span class="sxs-lookup"><span data-stu-id="beaae-136">Inspection and cleaning</span></span> | <span data-ttu-id="beaae-137">Stunde</span><span class="sxs-lookup"><span data-stu-id="beaae-137">Hour</span></span>             | <span data-ttu-id="beaae-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-138">GB-1234</span></span>        | <span data-ttu-id="beaae-139">I/R – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-139">I/C - GB1234</span></span> |
| <span data-ttu-id="beaae-140">Anfahrt</span><span class="sxs-lookup"><span data-stu-id="beaae-140">Travel</span></span>                  | <span data-ttu-id="beaae-141">Expense</span><span class="sxs-lookup"><span data-stu-id="beaae-141">Expense</span></span>          | <span data-ttu-id="beaae-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-142">GB-1234</span></span>        | <span data-ttu-id="beaae-143">I/R – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-143">I/C - GB1234</span></span> |
| <span data-ttu-id="beaae-144">Material</span><span class="sxs-lookup"><span data-stu-id="beaae-144">Materials</span></span>               | <span data-ttu-id="beaae-145">Artikel</span><span class="sxs-lookup"><span data-stu-id="beaae-145">Item</span></span>             | <span data-ttu-id="beaae-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-146">GB-1234</span></span>        | <span data-ttu-id="beaae-147">I/R – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-147">I/C - GB1234</span></span> |
| <span data-ttu-id="beaae-148">Routinemäßige Erneuerung</span><span class="sxs-lookup"><span data-stu-id="beaae-148">Routine replacement</span></span>     | <span data-ttu-id="beaae-149">Stunde</span><span class="sxs-lookup"><span data-stu-id="beaae-149">Hour</span></span>             | <span data-ttu-id="beaae-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-150">GB-1234</span></span>        | <span data-ttu-id="beaae-151">RE – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-151">RR - GB1234</span></span>  |
| <span data-ttu-id="beaae-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="beaae-152">GR-1</span></span>                    | <span data-ttu-id="beaae-153">Artikel</span><span class="sxs-lookup"><span data-stu-id="beaae-153">Item</span></span>             | <span data-ttu-id="beaae-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-154">GB-1234</span></span>        | <span data-ttu-id="beaae-155">RE – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-155">RR - GB1234</span></span>  |
| <span data-ttu-id="beaae-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="beaae-156">GR-5</span></span>                    | <span data-ttu-id="beaae-157">Artikel</span><span class="sxs-lookup"><span data-stu-id="beaae-157">Item</span></span>             | <span data-ttu-id="beaae-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="beaae-158">GB-1234</span></span>        | <span data-ttu-id="beaae-159">RE – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-159">RR - GB1234</span></span>  |

<span data-ttu-id="beaae-160">Den Servicevereinbarungspositionen der beiden Einzelaufgaben sind zwei Serviceaufgaben zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="beaae-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="beaae-161">Durch diese Serviceaufgaben ergeben sich die Buchungen für den jeweiligen Einzelvorgang.</span><span class="sxs-lookup"><span data-stu-id="beaae-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="beaae-162">Im ersten Fall steht die Serviceaufgabe "I/R – GB1234" für alle Servicevereinbarungspositionen, die die Inspektion und Reinigung des Objekts "GB-1234" betreffen.</span><span class="sxs-lookup"><span data-stu-id="beaae-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="beaae-163">Im zweiten Fall sind steht die Serviceaufgabe "RA – GB1234" für alle Servicevereinbarungspositionen für die routinemäßige Erneuerung.</span><span class="sxs-lookup"><span data-stu-id="beaae-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="beaae-164">Die Verknüpfung der Serviceaufgaben mit der jeweiligen Vereinbarung erfolgt durch die folgenden Serviceaufgabenbeziehungen:</span><span class="sxs-lookup"><span data-stu-id="beaae-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="beaae-165">Serviceaufgaben</span><span class="sxs-lookup"><span data-stu-id="beaae-165">Service tasks</span></span>

| <span data-ttu-id="beaae-166">Serviceaufgabe</span><span class="sxs-lookup"><span data-stu-id="beaae-166">Service task</span></span> | <span data-ttu-id="beaae-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beaae-167">Description</span></span>                             | <span data-ttu-id="beaae-168">Interner Hinweis</span><span class="sxs-lookup"><span data-stu-id="beaae-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="beaae-169">Externer Hinweis</span><span class="sxs-lookup"><span data-stu-id="beaae-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="beaae-170">I/R – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-170">I/C - GB1234</span></span> | <span data-ttu-id="beaae-171">Inspektion des Getriebes "GB-1234"</span><span class="sxs-lookup"><span data-stu-id="beaae-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="beaae-172">Sichtprüfung sowie mechanische Prüfung und Reinigung des Getriebes "GB-1234"</span><span class="sxs-lookup"><span data-stu-id="beaae-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="beaae-173">Routinemäßige Getriebeinspektion</span><span class="sxs-lookup"><span data-stu-id="beaae-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="beaae-174">RE – GB1234</span><span class="sxs-lookup"><span data-stu-id="beaae-174">RR - GB1234</span></span>  | <span data-ttu-id="beaae-175">Routinemäßige Erneuerung von Teilen in "GB-1234"</span><span class="sxs-lookup"><span data-stu-id="beaae-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="beaae-176">Routinemäßige Erneuerung der Komponenten "GR-1" und "GR-5". Bei vor 2002 gefertigten Getrieben muss auch die Komponente "GR-2" getauscht werden.</span><span class="sxs-lookup"><span data-stu-id="beaae-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="beaae-177">Routinemäßige Erneuerung von Teilen</span><span class="sxs-lookup"><span data-stu-id="beaae-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="beaae-178">Gruppen-Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="beaae-178">Group service orders</span></span>

<span data-ttu-id="beaae-179">Bei der automatischen Erstellung von Serviceaufträgen können Serviceaufgaben als Gruppierungskriterien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="beaae-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="beaae-180">Sollen Serviceaufträge nach Serviceaufgaben gruppiert werden, legen Sie in der Servicevereinbarung fest, dass für die auf der Servicevereinbarung basierenden Serviceaufträge die Serviceaufgabenkennung als anfängliche Gruppierungskriterien verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="beaae-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="beaae-181">**Gruppieren nach Serviceaufgabe**</span><span class="sxs-lookup"><span data-stu-id="beaae-181">**Group by service task**</span></span>

1. <span data-ttu-id="beaae-182">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="beaae-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="beaae-183">Auf der Registerkarte **Einstellungen** wählen Sie **Nach Serviceaufgabe** im Feld **Serviceaufträge kombinieren** aus.</span><span class="sxs-lookup"><span data-stu-id="beaae-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>



