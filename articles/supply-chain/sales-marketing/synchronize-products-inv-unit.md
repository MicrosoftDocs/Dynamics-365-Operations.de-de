---
title: Produkte mit Lagereinheit aus Finance and Operations mit Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/14/2019
ms.locfileid: "842461"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="13664-103">Produkte mit Lagereinheit aus Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="13664-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="13664-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="13664-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="13664-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="13664-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="13664-106">Die verwendete Vorlage **Field Service Produkte mit Bestandeinheit (Finance and Operations mit Field Service)** basiert auf der Vorlage **Field Service Produkte (Finance and Operations zu Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="13664-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="13664-107">Weitere Informationen finden Sie unter [Field Service-Produkte (Finance and Operations zu Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="13664-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="13664-108">In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="13664-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="13664-109">**Field Service Produkte mit Bestandeinheit (Finance and Operations zu Sales)**</span><span class="sxs-lookup"><span data-stu-id="13664-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="13664-110">**Field Service-Produkte (Finance and Operations nach Field Service)**</span><span class="sxs-lookup"><span data-stu-id="13664-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="13664-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="13664-111">Templates and tasks</span></span>

<span data-ttu-id="13664-112">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="13664-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="13664-113">Field Service Produkte mit Bestandeinheit (Finance and Operations zu Sales)</span><span class="sxs-lookup"><span data-stu-id="13664-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="13664-114">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="13664-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="13664-115">Produkte</span><span class="sxs-lookup"><span data-stu-id="13664-115">Products</span></span>

<span data-ttu-id="13664-116">Die Vorlage umfasst **Field Service Produkte mit Bestandeinheit (Finance and Operation zu Field Service)** und umfasst eine Zuordnung, die nicht in der Vorlage **Field Service Produkte (Finance and Operations zu Field Service)** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="13664-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="13664-117">Diese Zuordnung stellt sicher, so dass die Lagereinheit, die für Lagerbestandssynchronisierung erforderlich ist, enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="13664-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="13664-118">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="13664-118">Template mapping in Data integration</span></span>

<span data-ttu-id="13664-119">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="13664-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="13664-120">Field Service Produkte mit Bestandeinheit (Finance and Operations mit Field Service): Produkte</span><span class="sxs-lookup"><span data-stu-id="13664-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="13664-121">[![Vorlagenzuordnung in Datenintegration](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="13664-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
