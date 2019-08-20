---
title: Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsinformationen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: 6b56eb545f87c31ef30d6a897f48539068583486
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843432"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren 

[!include[banner](../includes/banner.md)]

In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsinformationen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsdaten von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service zu synchronisieren.

**Vorlagen in der Datenintegration**
- Produktbestand (Finance and Operations zu Field Service)
  
**Aufgaben im Datenintegrationsprojekt**
- Produktbestand

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Bestandlisten erfolgen kann:
- Lagerorte (Finance and Operations zu Field Service) 
- Field Service Produkte mit Bestand (Finance and Operations zu Sales) 

## <a name="entity-set"></a>Entitätssatz

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Verfügbarer CDS-Lagerbestand nach Lagerort     |

## <a name="entity-flow"></a>Entitätsfluss
Bestandebeneninformationen aus Finance and Operations mit Field Service für ausgewählte Produkte synchronisieren Die Betandsinformationen enthalten: 
- Verfügbare Menge (Aktuell erfasste Menge am Lagerort physisch)
- Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - h. Aufträge)
- Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - d.h. Bestellungen)

Diese Informationen werden pro freigegebenes Produkt für jeden Lagerort aufgezeichnet und synchronisiert auf Grundlage der Änderungsnachverfolgung, wenn der Lagerbestand ändert.

Im Field Service erstellt die Integrationslösung Bestanderfassungen für das Delta, um die Stufen im Fielöd Service abzurufen, die den Stufen im Bereich Finance and Operations abzugleichen.

Finance and Operations dient als Master für die Bestandebenen. Daher ist es wichtig, die Integration für Arbeitsaufträge, Übertragungen und Regulierungen von Field Service zu Finance and Operations einzurichen, wenn diese Funktionen in Field Service zusammen mit dem Synchronisieren von Lagerbeständen von Finane and Operations verwendet werden.

Die Produkte und die Lagerorte, in denen Lagerbestände verwaltet werden von Finance and Operations können mit der erweiterten Abfrage und Filterung (Power-Abfrage) gesteuert werden.

> [!NOTE]
> Es ist möglich, mehrere Lagerorte in Field Service zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll. Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren. In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations. Siehe zusätzliche Informationen unter [Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) und [synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Die **externe Produktbestandslistenentität** ist eine neue Entität, die nur für Back-End der Integration verwendet wird. Sie erhalten die Lagerbestandswerte von Finance and Operations in der Integdration und transformiert dann jene Werte manuell zur Bestanderfassung, welche dann die Bestandprodukte am Lagerort ändert.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="data-integration"></a>Datenintegration
Damit das Projekt funktioniert, müssen Sie sicherstellen, dass der Integrationsschlüssel für msdynce_externalproductinventories aktualisiert ist.
1.  Wechseln Sie zu **Datenintegration > Verbindungssätze**.
2.  Wählen Sie den verwendeten Verbindungssatz aus.
3.  In der Registerkarte **Integrationsschlüssel** stellen Sie sicher, dass die folgenden Schlüssel zu msdynce_externalproductinventories hinzugefügt werden:
      - msdynce_productnumber (Produktnummer)
      - msdynce_warehouseid (Warehouse-Kennung)
      
### <a name="data-integration-project"></a>Datenenintegrationsprojekt
Wenden Sie Filter mit der erweiterten Abfrage und Filterung an, um zu steuern, dass nur gewünschte Produkte und Lagerorte Lagerbestandsinformationen von Finance and Operations zu Field Service sendet.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Produktbestand (Finance and Operations zu Field Service): Produktbestand

[![Vorlagenzuordnung in Datenintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
