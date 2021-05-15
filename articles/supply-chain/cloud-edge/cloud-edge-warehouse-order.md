---
title: Lagerortaufträge für Cloud- und Edge-Skalierungseinheiten
description: Dieses Thema enthält Informationen zur Lagerortauftragsfunktion, die als Teil der Arbeitsauslastung der Lagerort-Skalierungseinheit verwendet wird.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ff1f13198a7acc35897252f3ca8f6c2b1f56852e
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938275"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="dfa05-103">Lagerortaufträge für Cloud- und Edge-Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="dfa05-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="dfa05-104">In der öffentlichen Vorschau werden nicht alle Geschäftsfunktionen vollständig unterstützt, wenn Arbeitsauslastungen von Skalierungseinheiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfa05-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="dfa05-105">Wenn Sie Skalierungseinheiten verwenden, achten Sie darauf, nur die Prozesse zu verwenden, die in diesem Thema ausdrücklich als unterstützt beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dfa05-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="dfa05-106">Was sind Lagerortaufträge?</span><span class="sxs-lookup"><span data-stu-id="dfa05-106">What are warehouse orders?</span></span>

<span data-ttu-id="dfa05-107">*Lagerortaufträge* sind ein Auftragstyp, der erstellt wurde, um Lagerortbereitstellungen von Hubs und Skalierungseinheiten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="dfa05-108">Mit ihnen können Sie Bestand erhalten, wenn Sie eine Arbeitsauslastung des Lagerorts auf einer Skalierungseinheit ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="dfa05-109">Sie werden derzeit nur bei Bestellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dfa05-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="dfa05-110">Lagerortaufträge werden im Rahmen der Lagerverwaltungsverarbeitung verwendet, z. B. wenn die Warehouse Management Mobile App zum Registrieren des physischen Lagerbestands während der Verarbeitung einer eingehenden Bestellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfa05-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="dfa05-111">Lagerortaufträge werden im Rahmen des Prozesses *Freigabe an Lager* erstellt, der für Bestellungen verfügbar ist, die einen Lagerort mit Skalierungseinheit angeben, und Artikel, die für die Verwendung von Lagerverwaltungsprozessen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="dfa05-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfa05-112">Lagerortaufträge sind nur in Bereitstellungen verfügbar, die [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="dfa05-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="dfa05-113">Einen Lagerortauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="dfa05-113">Create a warehouse order</span></span>

<span data-ttu-id="dfa05-114">Gehen Sie folgendermaßen vor, um einen Lagerortauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="dfa05-115">Melden Sie sich auf der Instanz von Microsoft Dynamics 365 Supply Chain Management an, die auf dem Hub ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfa05-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="dfa05-116">(Sie müssen den Prozess *Freigabe an Lager* initiieren, während Sie am Hub angemeldet sind.)</span><span class="sxs-lookup"><span data-stu-id="dfa05-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="dfa05-117">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="dfa05-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="dfa05-118">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="dfa05-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="dfa05-119">Um die zugehörigen Lagerortauftragspositionen anzuzeigen, öffnen Sie die entsprechende Bestellung und wählen eine Position im Abschnitt **Bestellpositionen** und dann in der Symbolleiste die Option **Lagerort \> Lagerortauftragspositionen** aus.</span><span class="sxs-lookup"><span data-stu-id="dfa05-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="dfa05-120">Um alle Positionen anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerauftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="dfa05-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="dfa05-121">Sie können den Prozess *Freigabe an Lagerort* auch aus einem Batch-Job heraus auslösen, indem Sie zu **Lagerortverwaltung > Freigabe an Lagerort > Automatische Freigabe von Einkaufsbestellungen** gehen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="dfa05-122">Wenn Sie den Batch-Job festlegen, können Sie bestimmte Zeilen der Einkaufsbestellung anhand einer Abfrage auswählen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="dfa05-123">Ein typisches Szenario wäre, einen wiederkehrenden Batch-Job festzulegen, der alle bestätigten Zeilen der Einkaufsbestellung freigibt, die voraussichtlich am nächsten Tag eintreffen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="dfa05-124">Stornieren eines Lagerortauftrags</span><span class="sxs-lookup"><span data-stu-id="dfa05-124">Cancel a warehouse order</span></span>

<span data-ttu-id="dfa05-125">Im Rahmen des Prozesses *Freigabe an Lager* werden Bestandsvorgänge für Bestellungen mit Lageraufträgen verknüpft und für die Aktualisierung durch den Hub gesperrt.</span><span class="sxs-lookup"><span data-stu-id="dfa05-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="dfa05-126">Wenn Sie versehentlich in das Lager freigegeben wurden oder wenn Sie einen anderen Grund haben, die Erstellung von Lagerortauftragspositionen rückgängig zu machen, können Sie die Stornierung von Lagerortauftragspositionen anfordern.</span><span class="sxs-lookup"><span data-stu-id="dfa05-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="dfa05-127">Gehen Sie folgendermaßen vor, um Lagerortauftragspositionen zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="dfa05-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="dfa05-128">Melden Sie sich bei der Instanz von Supply Chain Management an, die auf dem Hub ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfa05-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="dfa05-129">Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerauftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="dfa05-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="dfa05-130">Wählen Sie die zutreffende Position aus.</span><span class="sxs-lookup"><span data-stu-id="dfa05-130">Select the relevant line.</span></span>
1. <span data-ttu-id="dfa05-131">Wählen Sie im Aktionsbereich die Option **Lagerortauftragspositionen stornieren** aus.</span><span class="sxs-lookup"><span data-stu-id="dfa05-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="dfa05-132">Die Anforderung zum Stornieren von Positionen wird für alle Positionen abgelehnt, deren Stornierung bereits aussteht oder die aktiv in einem Lagerort verarbeitet werden, in dem die Arbeitslastung auf einer Skalierungseinheit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfa05-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="dfa05-133">Überwachen eines Lagerortauftrags</span><span class="sxs-lookup"><span data-stu-id="dfa05-133">Monitor a warehouse order</span></span>

<span data-ttu-id="dfa05-134">In der Ansicht **Lagerortauftragspositionen** können Sie den Fortschritt des eingehenden Empfangs überwachen, indem Sie die Werte in der Spalte **Noch zu empfangende Menge** prüfen.</span><span class="sxs-lookup"><span data-stu-id="dfa05-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="dfa05-135">Führen Sie einen dieser Schritte aus, um Details anzuzeigen, die sich auf Arbeiten beziehen, die mit der Warehouse Management Mobile App ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dfa05-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="dfa05-136">Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerortauftragspositionen**, und verwenden Sie den Filter, um die gesuchten Positionen zu finden.</span><span class="sxs-lookup"><span data-stu-id="dfa05-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="dfa05-137">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**, und öffnen Sie die relevante Bestellung.</span><span class="sxs-lookup"><span data-stu-id="dfa05-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="dfa05-138">In dem Abschnitt **Bestellpositionen** wählen Sie eine oder mehrere Zeilen aus, und wählen Sie dann in der Symbolleiste **Lagerort \> Lagerort-Empfangseinträge**.</span><span class="sxs-lookup"><span data-stu-id="dfa05-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
