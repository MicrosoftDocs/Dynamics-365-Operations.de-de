---
title: Produkte von Supply Chain Management mit Produkten in Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d3dc21a39c9866d09e500e2f14ff810bac7d57fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261044"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="6fcbe-103">Produkte von Supply Chain Management mit Produkten in Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6fcbe-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6fcbe-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="6fcbe-105">Die verwendete Vorlage **Field Service-Produkte (Supply Chain Management nach Field Service)** basiert auf der Vorlage **Produkte (Supply Chain Management nach Sales) – Direkt** aus Interessenten zu Bargeld.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="6fcbe-106">Weitere Informationen finden Sie unter [Produkte (Supply Chain Management nach Sales) – Direkt](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="6fcbe-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="6fcbe-107">In diesem Thema wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Supply Chain Management nach Field Service)** und **Produkte (Supply Chain Management nach Sales) – Direkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6fcbe-108">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6fcbe-108">Templates and tasks</span></span>

<span data-ttu-id="6fcbe-109">**Name der Vorlage in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="6fcbe-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="6fcbe-110">Field Service-Produkte (Supply Chain Management nach Field Service)</span><span class="sxs-lookup"><span data-stu-id="6fcbe-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="6fcbe-111">**Name der Aufgabe im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="6fcbe-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="6fcbe-112">Produkte - Produkte</span><span class="sxs-lookup"><span data-stu-id="6fcbe-112">Products - Products</span></span>

<span data-ttu-id="6fcbe-113">Die Vorlage **Field Service-Produkte (Supply Chain Management nach Field Service)** umfasst eine Zuordnung, die nicht in der Vorlage **Produkte (Supply Chain Management nach Sales) – Direkt** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="6fcbe-114">Diese Zuordnung gewährleistet, dass das erforderliche Field Service-spezifische Feld **Serviceprodukttyp** richtig festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="6fcbe-115">Die folgende Wertzuordnung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="6fcbe-116">In Supply Chain Management wird der Wert **Field Service-Produkttyp** in der Datenentität **Verkäufliche freigegebene Produkte** wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="6fcbe-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="6fcbe-117">**Bestand:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = True</span><span class="sxs-lookup"><span data-stu-id="6fcbe-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="6fcbe-118">**NonInventory:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = False</span><span class="sxs-lookup"><span data-stu-id="6fcbe-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="6fcbe-119">**Service:** Produkttyp = Dienstleistung</span><span class="sxs-lookup"><span data-stu-id="6fcbe-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6fcbe-120">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="6fcbe-120">Template mapping in Data integration</span></span>

<span data-ttu-id="6fcbe-121">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="6fcbe-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="6fcbe-122">Field Service-Produkte (Supply Chain Management nach Field Service): Produkte - Produkte</span><span class="sxs-lookup"><span data-stu-id="6fcbe-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="6fcbe-123">[![Vorlagenzuordnung in Datenintegration](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="6fcbe-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]