---
title: Lagerorte von Finance and Operations mit Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Lagerorte von Finance and Operations mit Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

**Name der Vorlage in der Datenintegration:**
- Projekte (Finance and Operations zu Field Service)

**Namen der Aufgaben im Datenintegrationsprojekt:**
- Lagerort

## <a name="entity-set"></a>Entitätssatz
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagerorte                             |

## <a name="entity-flow"></a>Entitätsfluss
Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Finance and Operations über ein Common Data Service (CDS)-Datenintegrationsprojekt synchronisiert werden. Die gewünschten Lagerorte, die mit Field Service synchronisieren, können mit der Abfrage und der erweiterten Filterung im Projekt gesteuert werden. Lagerorte, die von Finance and Operations synchronisieren, werden im Field Service mit dem Feld erstellt und extern auf Ja festgelegt und der Datensatz wird als schreibgeschützt erstellt.
Field Service CRM Lösung um die Integration zwischen Field Service und Finance and Operations zu unterstützen, sind zusätzliche Funktionen aus der Field Service CRM-Lösung erforderlich. Die Lösung enthält die folgenden Änderungen.
Das Feld **Wird extern verwaltet** wurde der Entität **Lagerort (msdyn_warehouses)** hinzugefügt. Dieses Feld hilft zu ermitteln, ob der Lagerort von Operations behandelt wird oder ob es nur in Field Service vorhanden ist.
- Ja – Der Lagerort stammt aus Finance and Operations und wird nicht in Sales bearbeitet.
- Nwin - Der Lagerort wurde direkt in Field Service eingegeben und wird hier verwaltet.

Das Feld wird **Extern verwaltet** hilft, die Synchronisierung von Bestandebenen, Regulierunmgen, Überträgen und der Verwendung von Arbeitsaufträgen zu synchronisieren. Nur Lagerorte mit **Werden exern verwaltet** = Ja können verwendet werden, um direkt den gleichen Lagerort im anderen System zu synchronisieren. 

Hinweis: Es ist möglich, mehrere Lagerorte in Field Services zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll. Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren. In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations. Siehe zusätzliche Informationen unter Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung
### <a name="in-the-data-integration-project"></a>Im Datenenintegrationsprojekt
Vor der Synchronisierung der Lagerorte stellen Sie sicher, die erweiterte Abfrage und Filterung im Projekt zu aktualisieren, die nur Lagerorte einbeziehen, die mithilfe von Finance and Operations mit Field Service vorhanden sind. Beachten Sie, dass Sie den Lagerort im Field Service benötigen, um sie in Arbeitsaufträgen, Übertragungen und Regulierungen zu übernehmen.  

Stellen Sie sicher, dass der **Integrationsschlüssel** für **msdyn_workorders** vorhanden ist
1. Gehen Sie zu Datenintegration
2. Wählen Sie **Verbindungssatz** Registerkarte
3. Wählen Sie das für die Synchronisation der Arbeitsaufträge verwendete Verbindungsset aus.
4. Wählen Sie **Integrationsschlüssel** Registerkarte
5. Suchen Sie msdyn_workorders und überprüfen Sie, ob der Schlüssel **msdyn_name (Name)** hinzugefügt wurde. Wenn es nicht angezeigt wird, fügen Sie es durch Klicken auf **Schlüssel hinzufügen** und klicken Sie auf **Speichern** im oberen Bereich der Seite.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Lagerorte (Finance and Operations zu Field Service): Lagerorte

[![Vorlagenzuordnung in Datenintegration](./media/Warehouse1.png)](./media/Warehouse1.png)

