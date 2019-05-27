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
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535858"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Produkte mit Lagereinheit aus Finance and Operations mit Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Die verwendete Vorlage **Field Service Produkte mit Bestandeinheit (Finance and Operations mit Field Service)** basiert auf der Vorlage **Field Service Produkte (Finance and Operations zu Field Service)**. Weitere Informationen finden Sie unter [Field Service-Produkte (Finance and Operations zu Field Service)](field-service-product.md).

In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben: 
- **Field Service Produkte mit Bestandeinheit (Finance and Operations zu Sales)**
- **Field Service-Produkte (Finance and Operations nach Field Service)** 

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

**Name der Vorlage in der Datenintegration:**

- Field Service Produkte mit Bestandeinheit (Finance and Operations zu Sales)

**Name der Aufgabe im Datenintegrationsprojekt:**

- Produkte

Die Vorlage umfasst **Field Service Produkte mit Bestandeinheit (Finance and Operation zu Field Service)** und umfasst eine Zuordnung, die nicht in der Vorlage **Field Service Produkte (Finance and Operations zu Field Service)** enthalten ist. Diese Zuordnung stellt sicher, so dass die Lagereinheit, die für Lagerbestandssynchronisierung erforderlich ist, enthalten ist.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Field Service Produkte mit Bestandeinheit (Finance and Operations mit Field Service): Produkte

[![Vorlagenzuordnung in Datenintegration](./media/FSProduct1.png)](./media/FSProduct1.png)
