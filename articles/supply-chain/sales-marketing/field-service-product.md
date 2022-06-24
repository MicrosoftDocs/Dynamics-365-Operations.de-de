---
title: Produkte von Supply Chain Management mit Produkten in Field Service synchronisieren
description: Dieser Artikel beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: Henrikan
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860550"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Produkte von Supply Chain Management mit Produkten in Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieser Artikel beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.

Die verwendete Vorlage **Field Service-Produkte (Supply Chain Management nach Field Service)** basiert auf der Vorlage **Produkte (Supply Chain Management nach Sales) – Direkt** aus Interessenten zu Bargeld. Weitere Informationen finden Sie unter [Produkte (Supply Chain Management nach Sales) – Direkt](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

In diesem Artikel wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Supply Chain Management nach Field Service)** und **Produkte (Supply Chain Management nach Sales) – Direkt** beschrieben.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

**Name der Vorlage in der Datenintegration**

- Field Service-Produkte (Supply Chain Management nach Field Service)

**Name der Aufgabe im Datenintegrationsprojekt**

- Produkte - Produkte

Die Vorlage **Field Service-Produkte (Supply Chain Management nach Field Service)** umfasst eine Zuordnung, die nicht in der Vorlage **Produkte (Supply Chain Management nach Sales) – Direkt** enthalten ist. Diese Zuordnung gewährleistet, dass das erforderliche Field Service-spezifische Feld **Serviceprodukttyp** richtig festgelegt ist.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Die folgende Wertzuordnung wird verwendet.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

In Supply Chain Management wird der Wert **Field Service-Produkttyp** in der Datenentität **Verkäufliche freigegebene Produkte** wie folgt berechnet:

- **Bestand:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = True
- **NonInventory:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = False
- **Service:** Produkttyp = Dienstleistung

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service-Produkte (Supply Chain Management nach Field Service): Produkte - Produkte

[![Vorlagenzuordnung in Datenintegration.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]