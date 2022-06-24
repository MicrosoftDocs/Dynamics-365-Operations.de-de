---
title: Produkte mit Bestand von Supply Chain Management zu Field Service synchronisieren
description: Dieser Artikel beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887253"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Produkte mit Bestand von Supply Chain Management zu Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieser Artikel beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte mit Bestandseinheit aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Die verwendete Vorlage **Field Service Produkte mit Bestandeinheit (Supply Chain Management zu Field Service)** basiert auf der Vorlage **Field Service Produkte (Supply Chain Management zu Field Service)**. Weitere Informationen finden Sie unter [Produkte im Supply Chain Management mit Produkten im Field Service](field-service-product.md) synchronisieren.

In diesem Artikel werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben: 
- **Field Service-Produkte mit Bestand (Supply Chain Management zu Sales)**
- **Field Service-Produkte (Supply Chain Management nach Field Service)** 

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

**Name der Vorlage in der Datenintegration:**

- Field Service-Produkte mit Bestand (Supply Chain Management zu Sales)

**Name der Aufgabe im Datenintegrationsprojekt:**

- Produkte

Die Vorlage **Field Service-Produkte mit Lagereinheit (Supply Chain Management zu Field Service)** enthält eine Zuordnung, die nicht in der Vorlage **Field Service-Produkte (Supply Chain Management zu Field Service)** enthalten ist. Diese Zuordnung stellt sicher, so dass die Lagereinheit, die für Lagerbestandssynchronisierung erforderlich ist, enthalten ist.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service Produkte mit Bestandeinheit (Supply Chain Management zu Field Service): Produkte

[![Vorlagenzuordnung in Datenintegration.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]