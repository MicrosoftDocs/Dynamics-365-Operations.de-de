---
title: Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren 

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

**Name der Vorlage in der Datenintegration:**
- Produktbestand (Finance and Operations zu Field Service)
  
**Namen der Aufgaben im Datenintegrationsprojekt:**
- Produktbestand

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Bestandlisten erfolgen kann:
- Projekte (Finance and Operations zu Field Service) 
- Field Service Produkte mit Lagereinheit (Finance and Operations zu Sales) 

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

Hinweis: Es ist möglich, mehrere Lagerorte in Field Services zu erstellen (mit wird extern verwaltet = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll. Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren. In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations. Siehe zusätzliche Informationen unter Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Die externe Produktbestandslistenentität ist eine neue Entität, die nur für Back-End der Integration verwendet wird. Sie erhalten die Lagerbestandswerte von Finance and Operations in der Integdration und transformiert dann jene Werte manuell zur Bestanderfassung, welche dann die Bestandprodukte am Lagerort ändert. 

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="in-the-data-integration-project"></a>Im Datenenintegrationsprojekt
Wenden Sie Filter mit der erweiterten Abfrage und Filterung an, um zu steuern, dass nur gewünschte Produkte und Lagerorte Lagerbestandsinformationen von Finance and Operations zu Field Service sendet.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Produktbestand (Finance and Operations zu Field Service): Produktbestand

[![Vorlagenzuordnung in Datenintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

