---
title: Produkte mit Bestand von Supply Chain Management zu Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 741b823d6cc5dbd23cda4f07e463f28d6bbe77d6
ms.sourcegitcommit: a2f9dce06322dada6b5f1c82051ef2359f8c0f12
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/24/2020
ms.locfileid: "3081863"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="a234f-103">Produkte mit Bestand von Supply Chain Management zu Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="a234f-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a234f-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a234f-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="a234f-105">[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="a234f-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="a234f-106">Die verwendete Vorlage **Field Service Produkte mit Bestandeinheit (Supply Chain Management zu Field Service)** basiert auf der Vorlage **Field Service Produkte (Supply Chain Management zu Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="a234f-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="a234f-107">Weitere Informationen finden Sie unter [Produkte im Supply Chain Management mit Produkten im Field Service](field-service-product.md) synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a234f-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="a234f-108">In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a234f-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="a234f-109">**Field Service-Produkte mit Bestand (Supply Chain Management zu Sales)**</span><span class="sxs-lookup"><span data-stu-id="a234f-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="a234f-110">**Field Service-Produkte (Supply Chain Management nach Field Service)**</span><span class="sxs-lookup"><span data-stu-id="a234f-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="a234f-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="a234f-111">Templates and tasks</span></span>

<span data-ttu-id="a234f-112">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="a234f-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a234f-113">Field Service-Produkte mit Bestand (Supply Chain Management zu Sales)</span><span class="sxs-lookup"><span data-stu-id="a234f-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="a234f-114">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="a234f-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="a234f-115">Produkte</span><span class="sxs-lookup"><span data-stu-id="a234f-115">Products</span></span>

<span data-ttu-id="a234f-116">Die Vorlage **Field Service Produkte mit Bestandeinheit (Supply Chain Management zu Field Service)** enthält eine Zuordnung, die nicht in der Vorlage **Field Service Produkte (Supply Chain Management zu Field Service)** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a234f-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="a234f-117">Diese Zuordnung stellt sicher, so dass die Lagereinheit, die für Lagerbestandssynchronisierung erforderlich ist, enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a234f-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a234f-118">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="a234f-118">Template mapping in Data integration</span></span>

<span data-ttu-id="a234f-119">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="a234f-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="a234f-120">Field Service Produkte mit Bestandeinheit (Supply Chain Management zu Field Service): Produkte</span><span class="sxs-lookup"><span data-stu-id="a234f-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="a234f-121">[![Vorlagenzuordnung in Datenintegration](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="a234f-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
