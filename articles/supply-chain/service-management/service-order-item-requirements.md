---
title: Artikelbedarf für Serviceauftrag
description: Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a0ce40c26e3d3028064b73a80a247180d6a9009
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226664"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="46928-103">Artikelbedarf für Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="46928-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="46928-104">Sie können einen Serviceauftrag erstellen, um Dienstleistungen nachzuverfolgen und zu verwalten, die Sie Ihren Debitoren anbieten.</span><span class="sxs-lookup"><span data-stu-id="46928-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="46928-105">Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen.</span><span class="sxs-lookup"><span data-stu-id="46928-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="46928-106">Eine Artikelanforderung kann sofort aus dem Bestand verbraucht werden, oder einen Produktionsauftrag für den Artikel initiieren.</span><span class="sxs-lookup"><span data-stu-id="46928-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="46928-107">Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="46928-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="46928-108">Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="46928-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="46928-109">Zum Erstellen von Artikelbedarf für einen Serviceauftrag muss der Serviceauftrag einem Projekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="46928-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="46928-110">Nach dem Erstellen eines Artikelbedarfs für einen Serviceauftrag kann dieser unter **Projekt** entweder im entsprechenden Serviceauftrag oder im Formular **Auftrag** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="46928-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="46928-111">Anzeigen eines Artikelbedarfs in einem Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="46928-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="46928-112">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="46928-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="46928-113">Klicken Sie **Versand** und **Artikelbedarf**, um das Formular **Artikelbedarf** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="46928-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="46928-114">Klicken Sie auf die Registerkarte **Projekt**, und aktivieren Sie das Kontrollkästchen **Serviceauftrag**, um die Serviceaufträge für den Artikelbedarf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="46928-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="46928-115">Löschen von Serviceaufträgen mit Artikelbedarf</span><span class="sxs-lookup"><span data-stu-id="46928-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="46928-116">Wurde für einen Serviceauftrag ein Artikelbedarf erstellt, kann der Serviceauftrag nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="46928-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="46928-117">Löschen Sie zunächst den Artikelbedarf, um den Serviceauftrag löschen zu können.</span><span class="sxs-lookup"><span data-stu-id="46928-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="46928-118">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="46928-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="46928-119">Klicken Sie **Versand** und **Artikelbedarf**, um das Formular **Artikelbedarf** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="46928-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="46928-120">Dieses Formular enthält eine Liste mit dem für den Serviceauftrag erstellten Artikelbedarf.</span><span class="sxs-lookup"><span data-stu-id="46928-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="46928-121">Wählen Sie die zu löschende Artikelanforderung aus, und klicken Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="46928-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="46928-122">-oder-</span><span class="sxs-lookup"><span data-stu-id="46928-122">–or–</span></span>

1.  <span data-ttu-id="46928-123">Klicken Sie auf **Projektverwaltung und -buchhaltung** \> **Allgemein** \> **Projekte** \> **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="46928-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="46928-124">Öffnen Sie das Projekt mit dem Serviceauftrag, in dem die Artikelanforderung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="46928-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="46928-125">In der **Projekte** Formular, im rechten Bereich **Artikelbedarf**.</span><span class="sxs-lookup"><span data-stu-id="46928-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="46928-126">Das Formular **Artikelbedarf** wird mit einer Liste des dem ausgewählten Projekt zugeordneten Artikelbedarfs geöffnet.</span><span class="sxs-lookup"><span data-stu-id="46928-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="46928-127">Wählen Sie die zu löschende Artikelanforderung aus, und klicken Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="46928-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="46928-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46928-128">See also</span></span>

<span data-ttu-id="46928-129">[Formular "Artikelbedarf"](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="46928-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]