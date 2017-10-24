---
title: Ausgangsprozess
description: "Dieses Thema enthält einen Überblick über den ausgehenden Prozess in der Lagerverwaltung."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: de-de
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="f13db-103">Ausgangsprozess</span><span class="sxs-lookup"><span data-stu-id="f13db-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f13db-104">Dieses Thema enthält einen Überblick über den ausgehenden Prozess in der Lagerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="f13db-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="f13db-105">Abgangsaufträge</span><span class="sxs-lookup"><span data-stu-id="f13db-105">Output orders</span></span>

<span data-ttu-id="f13db-106">Abgangsaufträge werden auch verwendet, um Auftragspositionen und Umlagerungsauftragspositionen mit den ausgehenden Entnahmevorgängen zu verknüpfen, die die Kommissionierlisten verwenden.</span><span class="sxs-lookup"><span data-stu-id="f13db-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="f13db-107">Wenn Kommissionierlisten entweder von Aufträgen oder von Umlagerungsaufträgen generiert werden, werden Abgangsaufträge und Lieferungen automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="f13db-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="f13db-108">Eine Kommissionierliste hat eine 1:1-Beziehung mit einer Lieferung.</span><span class="sxs-lookup"><span data-stu-id="f13db-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="f13db-109">Umlagerungsauftragslieferung oder der Lieferschein der Lieferung können von der Lieferung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f13db-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="f13db-110">Bei der folgenden Abbildung handelt es sich um eine Übersicht über den Prozess bei ausgehenden Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="f13db-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="f13db-111">[![Hier wird ein Überblick über die ausgehende Auftragsbearbeitung angezeigt](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="f13db-112">Sie können anhand von Ausgangsregeln festlegen, wie der Ausgangsprozess verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f13db-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="f13db-113">Sie können einen Workflow zur Steuerung des Überprüfungsverfahrens verwenden.</span><span class="sxs-lookup"><span data-stu-id="f13db-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="f13db-114">Sie können die Regeln verwenden, um zu steuern, in welcher Phase in der Fertigung gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f13db-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="f13db-115">Die folgenden Einstellungen legen fest, wie ausgehende Verarbeitungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f13db-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="f13db-116">Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden</span><span class="sxs-lookup"><span data-stu-id="f13db-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="f13db-117">Gehen Sie zu **Debitor** \> **Einstellungen** \> **Debitorenparameter**, und dann **Aktualisierungen** und wählen Sie einen Wert im Feld **Status der Entnahmeroute** aus.</span><span class="sxs-lookup"><span data-stu-id="f13db-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="f13db-118">[![Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="f13db-119">Wenn das Feld **Status der Entnahmeroute** auf **Abgeschlossen** festgelegt ist, findet die Entnahme automatisch als Teil des Prozesses Generieren von Kommissionierlisten statt.</span><span class="sxs-lookup"><span data-stu-id="f13db-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="f13db-120">Ist das Feld auf **Aktiviert** festgelegt, müssen die Kommissionierlistenpositionen manuell aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f13db-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="f13db-121">Die gleiche Einrichtung gilt für Umlagerungsaufträge.</span><span class="sxs-lookup"><span data-stu-id="f13db-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="f13db-122">Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung**, und dann **Transport** und wählen Sie einen Wert im Feld **Status der Entnahmeroute** aus.</span><span class="sxs-lookup"><span data-stu-id="f13db-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="f13db-123">[![Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="f13db-124">Lagerabgangsauftrag beenden</span><span class="sxs-lookup"><span data-stu-id="f13db-124">End output inventory orders</span></span>

<span data-ttu-id="f13db-125">Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung** und klicken Sie dann auf der Registerkarte **Allgemeines**, wählen Sie die Option **Lagerabgangsauftrag beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="f13db-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="f13db-126">[![Lagerabgangsauftragsoption beenden](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="f13db-127">Manchmal können einige Artikel im Lager nicht als Bestandteil des Kommissionierlistenprozesses entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="f13db-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="f13db-128">Beispielsweise kann möglicherweise diese Situation auftretenb, wenn ein Lagerarbeiter die Mengen auf Entnahmepositionen verringert und die Kommissionierliste verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f13db-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="f13db-129">Wenn die Option **Lagerabgangsauftrag beenden** auf **Ja** festgelegt wird, werden nicht abgeholte, verbleibende Mengen auf der Auftragsebene gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f13db-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="f13db-130">Ist die Option auf **Nein** festgelegt, werden die verbleibenden, nicht abgeholten Mengen als offene Abgangsauftragsmenge betrachtet.</span><span class="sxs-lookup"><span data-stu-id="f13db-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="f13db-131">In diesem Fall sind die Mengen am Lagerort freigegeben und müssen einer neuen Kommissionierliste als Teil der Funktionen **Abgangsaufträge erstellen** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f13db-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="f13db-132">[![Öffnen Sie Abgangsauftragsbefehl im Feld Funktionsmenü](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="f13db-133">[![Öffnen Sie Abgangsauftragsbefehl im Feld Funktionsmenü](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="f13db-134">Menge verringern</span><span class="sxs-lookup"><span data-stu-id="f13db-134">Reduce quantity</span></span>

<span data-ttu-id="f13db-135">Der dritte Parameter, den Sie als Teil des Prozesses Generieren von Kommissionierlisten verwenden können, ist der Parameter **Menge verringern**.</span><span class="sxs-lookup"><span data-stu-id="f13db-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="f13db-136">Die Einstellung dieses Parameters arbeitet mit den **Reservierungs**-Einstellungen, die den Reservierungsprozess als Teil der Freigabe am Lagerort auslösen.</span><span class="sxs-lookup"><span data-stu-id="f13db-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="f13db-137">[![Mengenparameter verringern](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="f13db-138">Beispiel eines ausgehenden Prozesses für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f13db-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="f13db-139">Bei diesem Beispiel gibt es einen Auftrag für zwei Artikel.</span><span class="sxs-lookup"><span data-stu-id="f13db-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="f13db-140">Während der Generierung von Kommissionierlisten legen Sie den Parameter **Menge verringern** fest.</span><span class="sxs-lookup"><span data-stu-id="f13db-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="f13db-141">Daher geben Sie Entnahmepositionen nur für verfügbaren Lagerbestand. frei und erstellen diese.</span><span class="sxs-lookup"><span data-stu-id="f13db-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="f13db-142">Die Entnahme muss über einen Registrierungsprozess für Kommissionierlisten (**Status der Entnahmeroute**)**Aktiviert** = gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="f13db-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="f13db-143">Der Lagerbestand, der noch nicht reserviert wurde, wird für die Generierung von Kommissionierlisten reserviert.</span><span class="sxs-lookup"><span data-stu-id="f13db-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="f13db-144">Der nicht verfügbare Bestand kann entweder vom Auftrag entfernt oder dem Lagerort für ausgehende Verarbeitung später freigegeben werden, wenn Artikel für Entnahme verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f13db-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="f13db-145">[![Kommissionierliste aktualisieren](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="f13db-146">Nachdem alle Entnahmepositionen **Entnahmelistenregistrierung** auf der Seite entnommen wurden, wird die zugehörige Lieferung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f13db-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="f13db-147">Der Prozess für Auftragslieferscheine kann dann basierend auf dem entnommenen Bestand initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f13db-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="f13db-148">[![Ausgehende Lieferungen aktualisieren](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="f13db-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

