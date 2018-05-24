---
title: Produkte in Finance and Operations mit Produkten in Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="75f40-103">Produkte in Finance and Operations mit Produkten in Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="75f40-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="75f40-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="75f40-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="75f40-105">Die verwendete Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** basiert auf der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** aus Interessenten zu Bargeld.</span><span class="sxs-lookup"><span data-stu-id="75f40-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="75f40-106">Weitere Informationen finden Sie unter [Produkte (Finance and Operations nach Sales) – Direkt](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="75f40-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="75f40-107">In diesem Thema wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Finance and Operations nach Field Service)** und **Produkte (Finance and Operations nach Sales) – Direkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75f40-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="75f40-108">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="75f40-108">Templates and tasks</span></span>

<span data-ttu-id="75f40-109">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="75f40-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="75f40-110">Field Service-Produkte (Finance and Operations nach Field Service)</span><span class="sxs-lookup"><span data-stu-id="75f40-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="75f40-111">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="75f40-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="75f40-112">Produkte - Produkte</span><span class="sxs-lookup"><span data-stu-id="75f40-112">Products - Products</span></span>

<span data-ttu-id="75f40-113">Die Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** umfasst eine Zuordnung, die in der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="75f40-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="75f40-114">Diese Zuordnung gewährleistet, dass das erforderliche Field Service-spezifische Feld **Serviceprodukttyp** richtig festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75f40-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="75f40-115">Die folgende Wertzuordnung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="75f40-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="75f40-116">In Finance and Operations wird der Wert **Field Service-Produkttyp** in der Datenentität **Verkäufliche freigegebene Produkte** wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="75f40-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="75f40-117">**Bestand:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = True</span><span class="sxs-lookup"><span data-stu-id="75f40-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="75f40-118">**NonInventory:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = False</span><span class="sxs-lookup"><span data-stu-id="75f40-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="75f40-119">**Service:** Produkttyp = Dienstleistung</span><span class="sxs-lookup"><span data-stu-id="75f40-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="75f40-120">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="75f40-120">Template mapping in Data integration</span></span>

<span data-ttu-id="75f40-121">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="75f40-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="75f40-122">Field Service-Produkte (Finance and Operations nach Field Service): Produkte - Produkte</span><span class="sxs-lookup"><span data-stu-id="75f40-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="75f40-123">[![Vorlagenzuordnung in Datenintegration](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="75f40-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>

