---
title: "Materialverbrauch mithilfe eines mobilen Geräts registrieren"
description: "In diesem Thema wird ein Workflow beschrieben, der die Erfassung des Rohmaterialverbrauchs in der Produktion verwendet, indem eine mobiles Gerät verwendet wird."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: de-de
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="22934-103">Materialverbrauch mithilfe eines mobilen Geräts registrieren</span><span class="sxs-lookup"><span data-stu-id="22934-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="22934-104">In diesem Thema wird ein Workflow beschrieben, der die Erfassung des Rohmaterialverbrauchs in der Produktion verwendet, indem eine mobiles Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22934-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="22934-105">Einführung</span><span class="sxs-lookup"><span data-stu-id="22934-105">Introduction</span></span>
------------

<span data-ttu-id="22934-106">Dieser Workflow ist relevant, wenn es eine stringente Anforderung für die Nachweisbarkeit gibt.</span><span class="sxs-lookup"><span data-stu-id="22934-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="22934-107">In diesen Fällen muss die exakte Zeit und die Menge für den der Verbrauch gemeldet werden, um die Nachweisbarkeit der Materialien zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="22934-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="22934-108">Dieser Prozess kann im Vergleich zu den vor- oder Arbeitsgängen Rückfluss angezeigt werden, in denen ein Gegenkonto zwischen dem Zeitpunkt der Erfassung und dem Zeitpunkt vorhanden ist, ab der tatsächliche Verbrauch erfolgt.</span><span class="sxs-lookup"><span data-stu-id="22934-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="22934-109">Dies erläutert, weshalb eine Strategie des automatischen Verbrauch für einige Materialien mit Nachweisbarkeitsanforderungen nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="22934-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="22934-110">Wir schauen ein einfaches Szenario an, das erklärt, wie Sie einen Workflow einrichten, um die Erfassung des Rohmaterialverbrauchs in der Produktion mithilfe einem mobilen Gerät zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="22934-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="22934-111">Szenariodetails</span><span class="sxs-lookup"><span data-stu-id="22934-111">Scenario details</span></span>

<span data-ttu-id="22934-112">Ein fortlaufender Produktionsrozess (5) verbraucht das Rohmaterial in der RM-100.</span><span class="sxs-lookup"><span data-stu-id="22934-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="22934-113">Das Material ist am Lagerplatz Bulk-001 (1) beim (1) PL-Kennzeichen mit zwei Chargen, B1 und, B2, für eine Menge von 100 Kilogramm verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22934-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="22934-114">Lagerortarbeit (2) ist für RM-100 freigegeben und verarbeitet, und das Material ist von dem Bulk-001 Produktionseingangslagerplatzes (3) PIL-01 entnommen, der al ein nicht von einem Ladungsträger gesteuerter Lagerplatz definiert ist.</span><span class="sxs-lookup"><span data-stu-id="22934-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="22934-115">Der Bediener wiegt Material vom Produktionseingangsstandort (3) aus und erfasst das Gewicht und die Chargennummer entspredhend dem Verbrauch (4).</span><span class="sxs-lookup"><span data-stu-id="22934-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="22934-116">Über einen Produktionseingangslagerplatz wird ein Teil des Materials manuell dem Produktionsprozess in festgelegten Zeitintervallen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="22934-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="22934-117">Wenn Bediener Material hinzufügt, wird dieses auf einer Waage gewogen und die Chargennummer wird erfasst.</span><span class="sxs-lookup"><span data-stu-id="22934-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="22934-118">Einrichten des Workflows, um den Verbrauchs unter Verwenden eines tragbaren Geräts mit laufender Erfassung zu erfassen</span><span class="sxs-lookup"><span data-stu-id="22934-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="22934-119">Erstellen Sie ein Endproduktprodukt, FG-100, mit einer Stückliste, die das Chargen kontrollierte Rohmaterial RM-100 hat.</span><span class="sxs-lookup"><span data-stu-id="22934-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="22934-120">Fügen Sie zwei Chargen, B1 und B2 von RM-100 in einer Menge von 100 dem Lagerplatz hinzu: Bulk-001 mit Kennzeichnungsplatte: PL-1.</span><span class="sxs-lookup"><span data-stu-id="22934-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="22934-121">Das Stücklisten-Bezugsprinzip für die Stücklistenposition für RM-100 wird auf **Manuell** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22934-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="22934-122">Der Produktions-Wareneingang wird auf PIL-01 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="22934-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="22934-123">Sie können das tun, indem Sie diesen Speicherort als den Standardproduktionswareneingangs-Lagerplatz auf Lagerort 51 auswählen.</span><span class="sxs-lookup"><span data-stu-id="22934-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="22934-124">Erstellen eines neuen Menüelements für ein mobiles Geräts:</span><span class="sxs-lookup"><span data-stu-id="22934-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="22934-125">**Menüartikelname** – Materialverbrauch registrieren.</span><span class="sxs-lookup"><span data-stu-id="22934-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="22934-126">**Titel** – Materialverbrauch registrieren.</span><span class="sxs-lookup"><span data-stu-id="22934-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="22934-127">**Modus** - Indirekt.</span><span class="sxs-lookup"><span data-stu-id="22934-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="22934-128">**Aktivitätscode** – Erfassen des tatsächlichen Materialverbrauchs.</span><span class="sxs-lookup"><span data-stu-id="22934-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="22934-129">Menüartikel Gerätemenü **Produktion Mobile** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="22934-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="22934-130">Wählen Sie diese Option aus, um einen Produktionsauftrag für ein fertiges Produkt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22934-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="22934-131">**Artikelnummer** – FG-100</span><span class="sxs-lookup"><span data-stu-id="22934-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="22934-132">**Standort** - 5</span><span class="sxs-lookup"><span data-stu-id="22934-132">**Site** - 5</span></span> 
-    <span data-ttu-id="22934-133">**Lagerort** - 51</span><span class="sxs-lookup"><span data-stu-id="22934-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="22934-134">**Menge** - 150</span><span class="sxs-lookup"><span data-stu-id="22934-134">**Quantity** - 150</span></span>

<span data-ttu-id="22934-135">Der Produktionsauftrag ist **Vorkalkuliert** und **Freigegeben** und Lagerortarbeit wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="22934-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="22934-136">Schließen Sie die Arbeit unter Verwendung des Workflows für Rohmaterialentnahme für das tragbaren Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="22934-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="22934-137">Dadurch wird das Material vom Sammellagerplatz zum Lagerplatz für Produktions-Wareneingang PIL-01 verschoben.</span><span class="sxs-lookup"><span data-stu-id="22934-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="22934-138">Nachdem die Arbeit abgeschlossen wurde, verfügt das Material den Status **Entnommen dem Produktionseingangslagerplatz**.</span><span class="sxs-lookup"><span data-stu-id="22934-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="22934-139">Der Status nach der Arbeit wird entweder als **Entnommen** oder **Physisch reserviert** verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="22934-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="22934-140">Diese wird mit dem Parameter **Status, nachdem es auf dem Lagerhausformular erfasst wurde** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="22934-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="22934-141">Startet den Produktionsauftrag entweder vom Client oder dem tragbaren Gerät, indem Sie  **Produktionsanfang** verwenden.</span><span class="sxs-lookup"><span data-stu-id="22934-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="22934-142">Nachdem der Produktionsauftrag gestartet wurde, können Sie mit Materialentnahme den Workflow zum tragbaren Gerät erfassen.</span><span class="sxs-lookup"><span data-stu-id="22934-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="22934-143">Beginnen wir damit, indem wir den Verbrauch von 25 Kilogramm von Charge B1 erfassen.</span><span class="sxs-lookup"><span data-stu-id="22934-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="22934-144">Wählen Sie die Menüoption **Erfassen Sie Material** **Verbrauch** im Menü für das tragbaren Gerät aus, geben Sie die folgenden Details ein:</span><span class="sxs-lookup"><span data-stu-id="22934-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="22934-145">Die Produktionsauftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="22934-145">The production order number.</span></span> 
-    <span data-ttu-id="22934-146">Der Lagerplatz, an dem das Material verbraucht wird, in diesem Fall PIL-01.</span><span class="sxs-lookup"><span data-stu-id="22934-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="22934-147">Artikelnummer RM-100.</span><span class="sxs-lookup"><span data-stu-id="22934-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="22934-148">Chargennummer B1.</span><span class="sxs-lookup"><span data-stu-id="22934-148">Batch number B1.</span></span> 
-    <span data-ttu-id="22934-149">Eine Menge von 25.</span><span class="sxs-lookup"><span data-stu-id="22934-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="22934-150">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="22934-150">Select **OK**.</span></span>

<span data-ttu-id="22934-151">Beachten Sie, dass die Meldung "Erfassungsposition" auf der Anzeige erscheint.</span><span class="sxs-lookup"><span data-stu-id="22934-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="22934-152">Auf dem Produktionsauftrag liegt eine offene Erfassung vom Typ **Produktionskommissionierliste** für Artikelnummer RM-100 und Chargennummer B1 vor.</span><span class="sxs-lookup"><span data-stu-id="22934-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="22934-153">Sie können nun entscheiden, ob die Sie Erfassung fortzusetzen, beispielsweise auf Chargennummer B2 und jedes Mal wenn Sie **OK.** auswählen, wird eine neue Erfassungsposition der offenen Erfassung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="22934-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="22934-154">Nachdem Sie Ihre Erfassung abgeschlossen haben, wählen Sie **Fertig**, um die Erfassung zu buchen und der Workflow zu beenden.</span><span class="sxs-lookup"><span data-stu-id="22934-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="22934-155">Zusätzliche Kommentare</span><span class="sxs-lookup"><span data-stu-id="22934-155">Additional comments</span></span> 

-   <span data-ttu-id="22934-156">Wenn ein Benutzer den Workflow storniert, nachdem eine Erfassungsposition erstellt wurde, ist die Erfassung ungebucht, aber wenn der Benutzer zu einem späteren Zeitpunkt des Workflows für denselben Produktionsauftrag verwendet, dann werden die Positionen der offenen Erfassung hinzugefügt anstatt einer neuen Erfassung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="22934-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="22934-157">Der neue Workflow unterstützt auch die Erfassung von Seriennummern.</span><span class="sxs-lookup"><span data-stu-id="22934-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="22934-158">Es ist nur möglich, eine Artikelnummer zu erfassen, die in der Stückliste oder in der Formel für den ausgewählten Produktionsauftrag oder den Chargenauftrag definiert wird.</span><span class="sxs-lookup"><span data-stu-id="22934-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="22934-159">Material kann bereits verbraucht sein.</span><span class="sxs-lookup"><span data-stu-id="22934-159">Material can be overconsumed.</span></span> <span data-ttu-id="22934-160">Wenn beispielsweise das Material mit einem Mengenverbrauch von 100 Kilogramm geschätzt wird, dann kann es mit einer Menge von beispielsweise 105 kg bereits verbraucht sein.</span><span class="sxs-lookup"><span data-stu-id="22934-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



