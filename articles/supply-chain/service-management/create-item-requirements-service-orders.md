---
title: "Erstellen von Artikelbedarf für Serviceaufträge"
description: "Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e76b0c636470a89ba2091363efe2f34eb3d58f88
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="2358c-103">Erstellen von Artikelbedarf für Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="2358c-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2358c-104">Sie können einen Serviceauftrag erstellen, um Dienstleistungen nachzuverfolgen und zu verwalten, die Sie Ihren Debitoren anbieten.</span><span class="sxs-lookup"><span data-stu-id="2358c-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="2358c-105">Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen.</span><span class="sxs-lookup"><span data-stu-id="2358c-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="2358c-106">Eine Artikelanforderung kann sofort aus dem Bestand verbraucht werden, oder einen Produktionsauftrag für den Artikel initiieren.</span><span class="sxs-lookup"><span data-stu-id="2358c-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="2358c-107">Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="2358c-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="2358c-108">Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2358c-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="2358c-109">Zum Erstellen von Artikelbedarf für einen Serviceauftrag muss der Serviceauftrag einem Projekt zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2358c-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="2358c-110">Nachdem Sie einen Artikelbedarfs für einen Serviceauftrag erstellen, können Sie den Artikelbedarf in dem Formular **Projekte** für das ausgewählte Projekt anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2358c-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="2358c-111">Erstellen eines Artikelbedarfs für einem Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="2358c-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="2358c-112">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="2358c-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="2358c-113">Wählen Sie den Serviceauftrag aus, für den ein Artikelbedarf erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2358c-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="2358c-114">Klicken Sie im **Aktivitätsbereich** auf der Registerkarte **Ausführung** auf **Artikelanforderung**.</span><span class="sxs-lookup"><span data-stu-id="2358c-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="2358c-115">Geben Sie im Formular **Artikelanforderungen** die Informationen für den erforderlichen Artikel ein.</span><span class="sxs-lookup"><span data-stu-id="2358c-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="2358c-116">Weitere Informationen zu bestimmten Feldern finden Sie unter [Formular "Artikelbedarf"](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="2358c-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="2358c-117">Erstellen eines Artikelbedarfs für eine Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="2358c-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="2358c-118">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="2358c-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="2358c-119">Öffnen Sie die Servicevereinbarung, für die ein Artikelbedarf erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2358c-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="2358c-120">Klicken Sie im Inforegister **Positionen** auf **Hinzufügen**, um eine neue Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2358c-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="2358c-121">Wählen Sie im Feld **Transaktionstyp** **Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="2358c-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="2358c-122">Wählen Sie im Feld **Artikeleinstellungen** **Artikelbedarf** aus.</span><span class="sxs-lookup"><span data-stu-id="2358c-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="2358c-123">Wählen Sie im Feld **Artikelnummer** den Artikel aus, der für die Servicevereinbarung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2358c-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="2358c-124">Wählen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Produktdimensionen**, im Feld **Standort**, wählen Sie hier den Standort für den Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="2358c-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="2358c-125">Um einen Serviceauftrag aus der Vereinbarungsposition zu erstellen, klicken Sie im Inforegister **Positionen** auf **Erstellen von Serviceaufträgen**, und geben dann die relevanten Informationen im Formular **Erstellen von Serviceaufträgen** ein.</span><span class="sxs-lookup"><span data-stu-id="2358c-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="2358c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2358c-126">See also</span></span>

<span data-ttu-id="2358c-127">[Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="2358c-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  



