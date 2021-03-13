---
title: Lagerortaufträge für Cloud- und Edge-Skalierungseinheiten
description: Dieses Thema enthält Informationen zur Lagerortauftragsfunktion, die als Teil der Arbeitsauslastung der Lagerort-Skalierungseinheit verwendet wird.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105708"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="66242-103">Lagerortaufträge für Cloud- und Edge-Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="66242-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="66242-104">In der öffentlichen Vorschau werden nicht alle Geschäftsfunktionen vollständig unterstützt, wenn Arbeitsauslastungen von Skalierungseinheiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66242-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="66242-105">Wenn Sie Skalierungseinheiten verwenden, achten Sie darauf, nur die Prozesse zu verwenden, die in diesem Thema ausdrücklich als unterstützt beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="66242-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="66242-106">Was sind Lagerortaufträge?</span><span class="sxs-lookup"><span data-stu-id="66242-106">What are warehouse orders?</span></span>

<span data-ttu-id="66242-107">*Lagerortaufträge* sind ein Auftragstyp, der erstellt wurde, um Lagerortbereitstellungen von Hubs und Skalierungseinheiten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="66242-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="66242-108">Mit ihnen können Sie Bestand erhalten, wenn Sie eine Arbeitsauslastung des Lagerorts auf einer Skalierungseinheit ausführen.</span><span class="sxs-lookup"><span data-stu-id="66242-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="66242-109">Sie werden derzeit nur bei Bestellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="66242-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="66242-110">Lagerortaufträge werden im Rahmen der Lagerverwaltungsverarbeitung verwendet, z. B. wenn die Lagerort-App zum Registrieren des physischen Lagerbestands während der Verarbeitung einer eingehenden Bestellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66242-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="66242-111">Lagerortaufträge werden im Rahmen des Prozesses *Freigabe an Lager* erstellt, der für Bestellungen verfügbar ist, die einen Lagerort mit Skalierungseinheit angeben, und Artikel, die für die Verwendung von Lagerverwaltungsprozessen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="66242-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66242-112">Lagerortaufträge sind nur in Bereitstellungen verfügbar, die [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="66242-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="66242-113">Einen Lagerortauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="66242-113">Create a warehouse order</span></span>

<span data-ttu-id="66242-114">Gehen Sie folgendermaßen vor, um einen Lagerortauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="66242-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="66242-115">Melden Sie sich auf der Instanz von Microsoft Dynamics 365 Supply Chain Management an, die auf dem Hub ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66242-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="66242-116">(Sie müssen den Prozess *Freigabe an Lager* initiieren, während Sie am Hub angemeldet sind.)</span><span class="sxs-lookup"><span data-stu-id="66242-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="66242-117">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="66242-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="66242-118">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="66242-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="66242-119">Um die zugehörigen Lagerortauftragspositionen anzuzeigen, öffnen Sie die entsprechende Bestellung und wählen eine Position im Abschnitt **Bestellpositionen** und dann in der Symbolleiste die Option **Lagerort \> Lagerortauftragspositionen** aus.</span><span class="sxs-lookup"><span data-stu-id="66242-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="66242-120">Um alle Positionen anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerauftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="66242-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="66242-121">Stornieren eines Lagerortauftrags</span><span class="sxs-lookup"><span data-stu-id="66242-121">Cancel a warehouse order</span></span>

<span data-ttu-id="66242-122">Im Rahmen des Prozesses *Freigabe an Lager* werden Bestandsvorgänge für Bestellungen mit Lageraufträgen verknüpft und für die Aktualisierung durch den Hub gesperrt.</span><span class="sxs-lookup"><span data-stu-id="66242-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="66242-123">Wenn Sie versehentlich in das Lager freigegeben wurden oder wenn Sie einen anderen Grund haben, die Erstellung von Lagerortauftragspositionen rückgängig zu machen, können Sie die Stornierung von Lagerortauftragspositionen anfordern.</span><span class="sxs-lookup"><span data-stu-id="66242-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="66242-124">Gehen Sie folgendermaßen vor, um Lagerortauftragspositionen zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="66242-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="66242-125">Melden Sie sich bei der Instanz von Supply Chain Management an, die auf dem Hub ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66242-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="66242-126">Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerauftragspositionen**.</span><span class="sxs-lookup"><span data-stu-id="66242-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="66242-127">Wählen Sie die zutreffende Position aus.</span><span class="sxs-lookup"><span data-stu-id="66242-127">Select the relevant line.</span></span>
1. <span data-ttu-id="66242-128">Wählen Sie im Aktionsbereich die Option **Lagerortauftragspositionen stornieren** aus.</span><span class="sxs-lookup"><span data-stu-id="66242-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="66242-129">Die Anforderung zum Stornieren von Positionen wird für alle Positionen abgelehnt, deren Stornierung bereits aussteht oder die aktiv in einem Lagerort verarbeitet werden, in dem die Arbeitslastung auf einer Skalierungseinheit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66242-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="66242-130">Überwachen eines Lagerortauftrags</span><span class="sxs-lookup"><span data-stu-id="66242-130">Monitor a warehouse order</span></span>

<span data-ttu-id="66242-131">In der Ansicht **Lagerortauftragspositionen** können Sie den Fortschritt des eingehenden Empfangs überwachen, indem Sie die Werte in der Spalte **Noch zu empfangende Menge** prüfen.</span><span class="sxs-lookup"><span data-stu-id="66242-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="66242-132">Führen Sie einen dieser Schritte aus, um Details anzuzeigen, die sich auf Arbeiten beziehen, die mit der Lagerort-App ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="66242-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="66242-133">Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerortauftragspositionen**, und verwenden Sie den Filter, um die gesuchten Positionen zu finden.</span><span class="sxs-lookup"><span data-stu-id="66242-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="66242-134">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**, und öffnen Sie die relevante Bestellung.</span><span class="sxs-lookup"><span data-stu-id="66242-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="66242-135">In dem Abschnitt **Bestellpositionen** wählen Sie eine oder mehrere Zeilen aus, und wählen Sie dann in der Symbolleiste **Lagerort \> Lagerort-Empfangseinträge**.</span><span class="sxs-lookup"><span data-stu-id="66242-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
