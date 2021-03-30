---
title: Übersicht der Ausgangsprozesse
description: Dieses Thema enthält einen Überblick über den ausgehenden Prozess in der Lagerverwaltung.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 24406f107d796891c315b39d3eff4351ae0aa5be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209682"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="8e153-103">Übersicht der Ausgangsprozesse</span><span class="sxs-lookup"><span data-stu-id="8e153-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e153-104">Dieses Thema enthält einen Überblick über den ausgehenden Prozess in der Lagerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="8e153-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="8e153-105">Abgangsaufträge</span><span class="sxs-lookup"><span data-stu-id="8e153-105">Output orders</span></span>

<span data-ttu-id="8e153-106">Abgangsaufträge werden auch verwendet, um Auftragspositionen und Umlagerungsauftragspositionen mit den ausgehenden Entnahmevorgängen zu verknüpfen, die die Kommissionierlisten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e153-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="8e153-107">Wenn Kommissionierlisten entweder von Aufträgen oder von Umlagerungsaufträgen generiert werden, werden Abgangsaufträge und Lieferungen automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="8e153-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="8e153-108">Eine Kommissionierliste hat eine 1:1-Beziehung mit einer Lieferung.</span><span class="sxs-lookup"><span data-stu-id="8e153-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="8e153-109">Umlagerungsauftragslieferung oder der Lieferschein der Lieferung können von der Lieferung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8e153-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="8e153-110">Bei der folgenden Abbildung handelt es sich um eine Übersicht über den Prozess bei ausgehenden Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="8e153-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="8e153-111">[![Hier wird ein Überblick über die ausgehende Auftragsbearbeitung angezeigt](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="8e153-112">Sie können anhand von Ausgangsregeln festlegen, wie der Ausgangsprozess verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e153-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="8e153-113">Sie können einen Workflow zur Steuerung des Überprüfungsverfahrens verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e153-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="8e153-114">Sie können die Regeln verwenden, um zu steuern, in welcher Phase in der Fertigung gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e153-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="8e153-115">Die folgenden Einstellungen legen fest, wie ausgehende Verarbeitungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e153-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="8e153-116">Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden</span><span class="sxs-lookup"><span data-stu-id="8e153-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="8e153-117">Gehen Sie zu **Debitor** \> **Einstellungen** \> **Debitorenparameter**, und dann **Aktualisierungen** und wählen Sie einen Wert im Feld **Status der Entnahmeroute** aus.</span><span class="sxs-lookup"><span data-stu-id="8e153-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="8e153-118">[![Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="8e153-119">Wenn das Feld **Status der Entnahmeroute** auf **Abgeschlossen** festgelegt ist, findet die Entnahme automatisch als Teil des Prozesses Generieren von Kommissionierlisten statt.</span><span class="sxs-lookup"><span data-stu-id="8e153-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="8e153-120">Ist das Feld auf **Aktiviert** festgelegt, müssen die Kommissionierlistenpositionen manuell aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8e153-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="8e153-121">Die gleiche Einrichtung gilt für Umlagerungsaufträge.</span><span class="sxs-lookup"><span data-stu-id="8e153-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="8e153-122">Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung**, und dann **Transport** und wählen Sie einen Wert im Feld **Status der Entnahmeroute** aus.</span><span class="sxs-lookup"><span data-stu-id="8e153-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="8e153-123">[![Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="8e153-124">Lagerabgangsauftrag beenden</span><span class="sxs-lookup"><span data-stu-id="8e153-124">End output inventory orders</span></span>

<span data-ttu-id="8e153-125">Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung** und klicken Sie dann auf der Registerkarte **Allgemeines**, wählen Sie die Option **Lagerabgangsauftrag beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="8e153-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="8e153-126">[![Lagerabgangsauftragsoption beenden](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="8e153-127">Wenn der Lagerarbeiter die Kommissionierlistenmengen verringert, werden die entsprechenden Lagerauftragsmengen aus der Lieferung entfernt.</span><span class="sxs-lookup"><span data-stu-id="8e153-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="8e153-128">Wenn die Kommissionierliste zu einem bestimmten Zeitpunkt aktualisiert wird, werden die verbleibenden Mengen wieder an den Auftrag gemeldet, wenn die Option **Lagerabgangsauftrag beenden** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8e153-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="8e153-129">Wenn die Option **Lagerabgangsauftrag beenden** auf **Nein** festgelegt ist, werden die verbleibenden Mengen als offene Abgangsauftragsmenge betrachtet und müssen einer neuen Kommissionierliste als Teil der Funktion **Offene Abgangsaufträge** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8e153-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="8e153-130">[![Öffnen Sie Abgangsauftragsbefehl im Feld Funktionsmenü](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="8e153-131">[![Öffnen Sie Abgangsauftragsbefehl im Feld Funktionsmenü](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="8e153-132">Menge verringern</span><span class="sxs-lookup"><span data-stu-id="8e153-132">Reduce quantity</span></span>

<span data-ttu-id="8e153-133">Der dritte Parameter, den Sie als Teil des Prozesses Generieren von Kommissionierlisten verwenden können, ist der Parameter **Menge verringern**.</span><span class="sxs-lookup"><span data-stu-id="8e153-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="8e153-134">Die Einstellung dieses Parameters arbeitet mit den **Reservierungs**-Einstellungen, die den Reservierungsprozess als Teil der Freigabe am Lagerort auslösen.</span><span class="sxs-lookup"><span data-stu-id="8e153-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="8e153-135">[![Mengenparameter verringern](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="8e153-136">Beispiel eines ausgehenden Prozesses für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="8e153-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="8e153-137">Bei diesem Beispiel gibt es einen Auftrag für zwei Artikel.</span><span class="sxs-lookup"><span data-stu-id="8e153-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="8e153-138">Während der Generierung von Kommissionierlisten legen Sie den Parameter **Menge verringern** fest.</span><span class="sxs-lookup"><span data-stu-id="8e153-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="8e153-139">Daher geben Sie Entnahmepositionen nur für verfügbaren Lagerbestand. frei und erstellen diese.</span><span class="sxs-lookup"><span data-stu-id="8e153-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="8e153-140">Die Entnahme muss über einen Registrierungsprozess für Kommissionierlisten (**Status der Entnahmeroute**)**Aktiviert** = gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="8e153-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="8e153-141">Der Lagerbestand, der noch nicht reserviert wurde, wird für die Generierung von Kommissionierlisten reserviert.</span><span class="sxs-lookup"><span data-stu-id="8e153-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="8e153-142">Der nicht verfügbare Bestand kann entweder vom Auftrag entfernt oder dem Lagerort für ausgehende Verarbeitung später freigegeben werden, wenn Artikel für Entnahme verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8e153-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="8e153-143">[![Kommissionierliste aktualisieren](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="8e153-144">Nachdem alle Entnahmepositionen **Entnahmelistenregistrierung** auf der Seite entnommen wurden, wird die zugehörige Lieferung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8e153-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="8e153-145">Der Prozess für Auftragslieferscheine kann dann basierend auf dem entnommenen Bestand initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8e153-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="8e153-146">[![Ausgehende Lieferungen aktualisieren](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="8e153-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]