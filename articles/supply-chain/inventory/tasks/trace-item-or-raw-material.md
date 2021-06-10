---
title: Artikel oder Rohmaterial nachverfolgen
description: Dieses Verfahren zeigt, wie die Artikelverfolgung angewendet wird, um zu erkennen, wo Artikel oder Rohmaterial verwendet wurden oder verwendet werden.
author: sherry-zheng
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46e46d75ecab3ec2e94372aecfd2c29783756446
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102854"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="cf787-103">Artikel oder Rohmaterial nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="cf787-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf787-104">Dieses Verfahren zeigt, wie die Artikelverfolgung angewendet wird, um zu erkennen, wo Artikel oder Rohmaterial verwendet wurden oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf787-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="cf787-105">Mit dieser Prozedur können Sie einen Artikel identifizieren, ihn zur Quelle zurückverfolgen und dann die Abläufe vorwärts verfolgen über die Produktion und den Vertrieb des fertigen Produkts.</span><span class="sxs-lookup"><span data-stu-id="cf787-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="cf787-106">Der Prozess kann verwendet werden, um die Debitoren, die beeinflusst werden, die betroffenen Aufträge usw. zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cf787-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="cf787-107">Für diese Prozedur wird das Demodatunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf787-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="cf787-108">Einen Artikel rückwärts mithilfe einer bekannten Chargennummer verfolgen</span><span class="sxs-lookup"><span data-stu-id="cf787-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="cf787-109">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Bestandsmanagement > Anfragen und Berichte > Verfolgungsdimensionen > Artikelverfolgung**.</span><span class="sxs-lookup"><span data-stu-id="cf787-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="cf787-110">Wählen Sie im Feld **Artikelnummer**'P9100'.</span><span class="sxs-lookup"><span data-stu-id="cf787-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="cf787-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="cf787-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cf787-112">Wählen Sie im Feld **Vorwärts oder Rückwärts** die Option'Rückwärts'.</span><span class="sxs-lookup"><span data-stu-id="cf787-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="cf787-113">Wählen Sie im Feld **Chargennummer** die Option'as-12-344-01'.</span><span class="sxs-lookup"><span data-stu-id="cf787-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="cf787-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="cf787-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="cf787-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf787-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="cf787-116">Einen Artikel festlegen, vorwärts verfolgen und analysieren</span><span class="sxs-lookup"><span data-stu-id="cf787-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="cf787-117">Der oberste Knoten der Struktur stellt die verfügbare Menge des ausgewählten Artikels und der Charge dar.</span><span class="sxs-lookup"><span data-stu-id="cf787-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="cf787-118">Sie müssen die Knoten der Struktur erweitern, um den Artikel zu finden, bei dem die Vorwärtsablaufverfolgung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf787-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="cf787-119">Erweitern Sie in der Struktur "die unten beschriebenen Knoten und wählen Sie dann den letzten Knoten aus".</span><span class="sxs-lookup"><span data-stu-id="cf787-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="cf787-120">Erweitern Sie: "P9100 / 1 / 10 / as-12-344-01 ● 117 Liter ● 26,4 Liter  \P9100 ● Entnommen ● Auftrag 000072 ● 22.12.2015 ● -58,6 Liter ● -15 Liter ● Standort=1, Lagerort=10, Chargennummer=als-12-344-01   \P9100 ● Produktion B-000050 ● 9.12.2015● 410,72 Liter ● 102,21 Liter ● Standort=1, Lagerort=10, Chargennummer=als-12-344-01 ● Co-Produkte: P9101" und wählen Sie dann diesen Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="cf787-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="cf787-121">Erweitern Sie in der Struktur "den unten beschriebenen Knoten und wählen Sie dann diesen Knoten aus".</span><span class="sxs-lookup"><span data-stu-id="cf787-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="cf787-122">Beginnend am Knoten, den Sie soeben ausgewählt haben, erweitern Sie „M9103 ● Produktionsposition B-000050 ● 09.12.2015 ● -72,57 kg ● Größe=70, Farbe=OK, Standort=1, Lagerort=10, Charennummer=App01“ und wählen Sie dann diesen Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="cf787-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="cf787-123">Klicken Sie auf **Trace vom Knoten**.</span><span class="sxs-lookup"><span data-stu-id="cf787-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="cf787-124">Klicken Sie auf **Vorwärts**.</span><span class="sxs-lookup"><span data-stu-id="cf787-124">Click **Forward**.</span></span>
5. <span data-ttu-id="cf787-125">Klicken Sie im **Aktionsbereich** auf **Verfolgung**.</span><span class="sxs-lookup"><span data-stu-id="cf787-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="cf787-126">Es gibt mehrere Ablaufverfolgungsoptionen, die Informationen zu Debitoren bereitstellen, die vom Artikel betroffen sind, den Sie nachverfolgen, sowie von den Aufträgen, die sich auf den Artikel beziehen, der versendet wurde oder nicht versendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf787-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="cf787-127">Klicken Sie auf **Kunden**.</span><span class="sxs-lookup"><span data-stu-id="cf787-127">Click **Customers**.</span></span>
7. <span data-ttu-id="cf787-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cf787-128">Close the page.</span></span>
8. <span data-ttu-id="cf787-129">Klicken Sie im **Aktionsbereich** auf **Verfolgung**.</span><span class="sxs-lookup"><span data-stu-id="cf787-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="cf787-130">Klicken Sie auf **Versendete Kundenaufträge**.</span><span class="sxs-lookup"><span data-stu-id="cf787-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="cf787-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cf787-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]