---
title: "Serviceaufträge stornieren"
description: "Sie können einen Serviceauftrag oder eine Serviceauftragsposition direkt im Serviceauftrag stornieren oder zum Stornieren mehrerer Serviceaufträge einen periodischen Einzelvorgang ausführen."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="d6ce6-103">Serviceaufträge stornieren</span><span class="sxs-lookup"><span data-stu-id="d6ce6-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d6ce6-104">Sie können einen Serviceauftrag oder eine Serviceauftragsposition direkt im Serviceauftrag stornieren oder zum Stornieren mehrerer Serviceaufträge einen periodischen Einzelvorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d6ce6-105">Serviceaufträge können nicht storniert werden, wenn die Phase des Serviceauftrags keine Stornierung zulässt, Artikelbedarf vorliegt oder der Serviceauftrag bereits gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="d6ce6-106">Stornieren eines Serviceauftrags im Formular "Serviceaufträge"</span><span class="sxs-lookup"><span data-stu-id="d6ce6-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="d6ce6-107">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="d6ce6-108">Wählen Sie den gewünschten Serviceauftrag aus, und klicken Sie im Aktivitätsbereich auf **Auftrag stornieren**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="d6ce6-109">Stornieren einer Serviceauftragsposition</span><span class="sxs-lookup"><span data-stu-id="d6ce6-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="d6ce6-110">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="d6ce6-111">Doppelklicken Sie auf den Serviceauftrag, der die zu stornierende Position enthält.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="d6ce6-112">Wählen Sie die Serviceauftragsposition aus, die Sie stornieren möchten, und klicken Sie auf **Auftragsposition stornieren**, um den Status der Position in **Storniert** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="d6ce6-113">Um die Stornierung einer Serviceauftragsposition zu widerrufen und den Status wieder in <STRONG>Erstellt</STRONG> zu ändern, klicken Sie auf <STRONG>Stornierung widerrufen</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="d6ce6-114">Stornieren mehrerer Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="d6ce6-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="d6ce6-115">Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Serviceaufträge** \> **Serviceaufträge stornieren**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="d6ce6-116">Klicken Sie auf die Schaltfläche **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="d6ce6-117">Wählen Sie im Formular **Abfrage** in der Spalte **Kriterien** die zu löschenden Serviceaufträge aus.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="d6ce6-118">Klicken Sie auf **OK**, um das **Abfrageformular** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="d6ce6-119">Aktivieren Sie zum Generieren eines Infologs mit den stornierten Serviceaufträgen das Kontrollkästchen **Infolog anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="d6ce6-120">Aktivieren Sie das Kontrollkästchen **Stornierung widerrufen**, wenn Sie den Status **Storniert** eines Serviceauftrags widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="d6ce6-121">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-121">Click **OK**.</span></span>

<span data-ttu-id="d6ce6-122">Die ausgewählten Serviceaufträge werden entweder storniert, oder der Status **Storniert** wird auf **In Bearbeitung ...** zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d6ce6-123">Wenn Sie das Kontrollkästchen <STRONG>Stornierung widerrufen</STRONG> aktivieren, werden Serviceaufträge mit dem Status <STRONG>Storniert</STRONG> widerrufen und Serviceaufträge mit dem Status <STRONG>In Bearbeitung ...</STRONG> nicht storniert.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



