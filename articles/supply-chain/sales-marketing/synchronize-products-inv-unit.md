---
title: Produkte mit Lagereinheit aus Finance and Operations mit Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e633b-103">Produkte mit Lagereinheit aus Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e633b-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e633b-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e633b-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e633b-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="e633b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="e633b-106">Die verwendete Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** basiert auf der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** aus Interessenten zu Bargeld.</span><span class="sxs-lookup"><span data-stu-id="e633b-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="e633b-107">Weitere Informationen finden Sie unter [Produkte (Finance and Operations nach Sales) – Direkt](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="e633b-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="e633b-108">In diesem Thema wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Finance and Operations nach Field Service)** und **Produkte (Finance and Operations nach Sales) – Direkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e633b-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e633b-109">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e633b-109">Templates and tasks</span></span>

<span data-ttu-id="e633b-110">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="e633b-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="e633b-111">Field Service Produkte mit Lagereinheit (Finance and Operations zu Sales)</span><span class="sxs-lookup"><span data-stu-id="e633b-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="e633b-112">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="e633b-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="e633b-113">Produkte</span><span class="sxs-lookup"><span data-stu-id="e633b-113">Products</span></span>

<span data-ttu-id="e633b-114">Die Vorlage umfasst **Field Service-Produkte mit Bestand (Finance and Operation zu Field Service)** und umfasst eine Zuordnung, die nicht in der Vorlage **Field Service Produkte (Finance and Operations zu Field Service)** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e633b-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="e633b-115">Diese Zuordnung stellt sicher, so dass die Lagereinheit, die für Lagerbestandssynchronisierung erforderlich ist, enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e633b-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e633b-116">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="e633b-116">Template mapping in Data integration</span></span>

<span data-ttu-id="e633b-117">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="e633b-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="e633b-118">Field SErvice Produkte mit Bestandeinheit (Finance and Operations mit Field Service): Produkte</span><span class="sxs-lookup"><span data-stu-id="e633b-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="e633b-119">[![Vorlagenzuordnung in Datenintegration](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="e633b-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>

