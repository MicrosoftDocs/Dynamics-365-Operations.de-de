---
title: Lagerebeneninformationen aus Supply Chain Management mit Field Service synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsinformationen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 0822bf4bdbb687e040e2ce04842ef263b8dc0e1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243080"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Lagerebeneninformationen aus Supply Chain Management mit Field Service synchronisieren 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsinformationen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.

[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsdaten von Supply Chain Management auf Field Service zu synchronisieren.

**Vorlagen in der Datenintegration**
- Produktbestand (Supply Chain Management zu Field Service)
  
**Aufgaben im Datenintegrationsprojekt**
- Produktbestand

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Bestandlisten erfolgen kann:
- Lagerorte (Supply Chain Management zu Field Service) 
- Field Service-Produkte mit Bestand (Supply Chain Management zu Sales) 

## <a name="entity-set"></a>Entitätssatz

| Field Service                      | Lieferkettenverwaltung                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Verfügbarer Dataverse-Bestand nach Lagerort     |

## <a name="entity-flow"></a>Entitätsfluss
Bestandebeneninformationen aus Finance and Operations mit Field Service für ausgewählte Produkte synchronisieren Die Betandsinformationen enthalten: 
- Verfügbare Menge (Aktuell erfasste Menge am Lagerort physisch)
- Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - h. Aufträge)
- Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - d.h. Bestellungen)

Diese Informationen werden pro freigegebenes Produkt für jeden Lagerort aufgezeichnet und synchronisiert auf Grundlage der Änderungsnachverfolgung, wenn der Lagerbestand ändert.

In Field Service erstellt die Integrationslösung Bestanderfassungen für das Delta, um die Stufen Field Service abzurufen, die mit den Stufen in Supply Chain Management übereinstimmen.

Supply Chain Management dient als Master für die Bestandebenen. Daher ist es wichtig, die Integration für Arbeitsaufträge, Übertragungen und Regulierungen von Field Service zu Supply Chain Management einzurichen, wenn diese Funktionen in Field Service zusammen mit dem Synchronisieren von Lagerbeständen von Supply Chain Management verwendet werden.

Die Produkte und die Lagerorte, in denen Lagerbestände verwaltet werden von Supply Chain Management können mit der erweiterten Abfrage und Filterung (Power-Abfrage) gesteuert werden.

> [!NOTE]
> Es ist möglich, mehrere Lagerorte in Field Service zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort in Supply Chain Management mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll. Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Supply Chain Management zu aktualisieren. In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Supply Chain Management. Siehe zusätzliche Informationen unter [Synchronisierung von Bestandanpassungen von Field Service zu Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) und [Synchronisieren von Arbeitsaufträgen in Field Service zu Arbeitsaufträgen, die mit Projekten in Supply Chain Management verknüpft sind](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Die **externe Produktbestandslistenentität** ist eine neue Entität, die nur für Back-End der Integration verwendet wird. Sie erhalten die Lagerbestandswerte von Supply Chain Management in der Integdration und transformiert dann jene Werte manuell zur Bestanderfassung, welche dann die Bestandprodukte am Lagerort ändert.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="data-integration"></a>Datenintegration
Damit das Projekt funktioniert, müssen Sie sicherstellen, dass der Integrationsschlüssel für msdynce_externalproductinventories aktualisiert ist.
1.  Wechseln Sie zu **Datenintegration > Verbindungssätze**.
2.  Wählen Sie den verwendeten Verbindungssatz aus.
3.  In der Registerkarte **Integrationsschlüssel** stellen Sie sicher, dass die folgenden Schlüssel zu msdynce_externalproductinventories hinzugefügt werden:
      - msdynce_productnumber (Produktnummer)
      - msdynce_warehouseid (Warehouse-Kennung)
      
### <a name="data-integration-project"></a>Datenenintegrationsprojekt
Wenden Sie Filter mit der erweiterten Abfrage und Filterung an, um zu steuern, dass nur gewünschte Produkte und Lagerorte Lagerbestandsinformationen von Supply Chain Management zu Field Service sendet.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Produktbestand (Supply Chain Management zu Field Service): Produktbestand

[![Vorlagenzuordnung in Datenintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]