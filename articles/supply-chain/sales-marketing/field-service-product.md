---
title: Produkte in Finance and Operations mit Produkten in Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "316325"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Produkte von Finance and Operations mit Produkten in Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgabe, die verwendet werden, um die Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

Die verwendete Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** basiert auf der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** aus Interessenten zu Bargeld. Weitere Informationen finden Sie unter [Produkte (Finance and Operations nach Sales) – Direkt](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

In diesem Thema wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Finance and Operations nach Field Service)** und **Produkte (Finance and Operations nach Sales) – Direkt** beschrieben.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

**Name der Vorlage in der Datenintegration:**

- Field Service-Produkte (Finance and Operations nach Field Service)

**Name der Aufgabe im Datenintegrationsprojekt:**

- Produkte - Produkte

Die Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** umfasst eine Zuordnung, die in der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** nicht enthalten ist. Diese Zuordnung gewährleistet, dass das erforderliche Field Service-spezifische Feld **Serviceprodukttyp** richtig festgelegt ist.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Die folgende Wertzuordnung wird verwendet.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

In Finance and Operations wird der Wert **Field Service-Produkttyp** in der Datenentität **Verkäufliche freigegebene Produkte** wie folgt berechnet:

- **Bestand:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = True
- **NonInventory:** = Produkttyp = Produkt- und Artikelmodellgruppe, Gelagertes Produkt = False
- **Service:** Produkttyp = Dienstleistung

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service-Produkte (Finance and Operations nach Field Service): Produkte - Produkte

[![Vorlagenzuordnung in Datenintegration](./media/FSProduct.png)](./media/FSProduct.png)
