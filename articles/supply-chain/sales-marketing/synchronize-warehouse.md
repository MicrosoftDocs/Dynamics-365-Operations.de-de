---
title: Lagerorte von Supply Chain Management zu Field Service synchronisieren
description: Dieser Artikel beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Lager aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
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
ms.openlocfilehash: 8b86b6a59344299a7a2d277543c3186ed2b8cee4
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103232"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Lagerorte von Supply Chain Management zu Field Service synchronisieren

[!include[banner](../includes/banner.md)]



Dieser Artikel beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Lager aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Lagerorte von Supply Chain Management auf Field Service zu synchronisieren.

**Vorlagen in der Datenintegration**
- Lagerorte (Supply Chain Management zu Field Service)

**Aufgaben im Datenintegrationsprojekt**
- Lagerort

## <a name="table-set"></a>Tabellensatz
| Field Service    | Lieferkettenverwaltung                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagerorte                             |

## <a name="table-flow"></a>Tabellenfluss
Lagerorte, die in Supply Chain Management erstellt und verwaltet werden, können über ein Microsoft Dataverse-Datenintegrationsprojekt nach Field Service synchronisiert werden. Die gewünschten Lagerorte, die mit Field Service synchronisieren, können mit der Abfrage und der erweiterten Filterung im Projekt gesteuert werden. Von Supply Chain Management synchronisierte Lagerorte werden in Field Service erstellt, wobei die Spalte **Wird extern verwaltet** auf **Ja** festgelegt wird und der Datensatz schreibgeschützt ist.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Um die Integration zwischen Field Service und Supply Chain Management zu unterstützen, sind zusätzliche Funktionen aus der Field Service CRM-Lösung erforderlich. In der Lösung wurde die Spalte **Wird extern verwaltet** zur Tabelle **Lagerort (msdyn_warehouses)** hinzugefügt. Mit dieser Spalte kann ermittelt werden, ob der Lagerort über Supply Chain Management gehandhabt wird oder ob er nur in Field Service existiert. Zu den Einstellungen für diese Spalte gehören:
- **Ja** – Das Lager stammt aus Supply Chain Management und wird nicht in Sales bearbeitet.
- **Nein** - Der Lagerort wurde direkt in Field Service eingegeben und wird hier verwaltet.

Die Spalte **Wird extern verwaltet** hilft, die Synchronisierung von Bestandsebenen, Regulierungen, Überträgen und der Verwendung von Arbeitsaufträgen zu steuern. Nur Lagerorte mit **Werden exern verwaltet** = **Ja** können verwendet werden, um direkt den gleichen Lagerort im anderen System zu synchronisieren. 

> [!NOTE]
> Es ist möglich, mehrere Lagerorte in Field Service zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort mit den erweiterten Abfragen und Filterfunktionen zuzuordnen. Dies wird in Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Supply Chain Management zu aktualisieren. In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Supply Chain Management. Siehe zusätzliche Informationen unter [Synchronisierung von Bestandanpassungen von Field Service zu Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) und [Synchronisieren von Arbeitsaufträgen in Field Service zu Arbeitsaufträgen, die mit Projekten in Supply Chain Management verknüpft sind](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung
### <a name="data-integration-project"></a>Datenenintegrationsprojekt
Vor der Synchronisierung der Lagerorte stellen Sie sicher, die erweiterte Abfrage und Filterung im Projekt zu aktualisieren, die nur Lagerorte einbeziehen, die mithilfe von Supply Chain Management mit Field Service vorhanden sind. Beachten Sie, dass Sie den Lagerort im Field Service benötigen, um sie in Arbeitsaufträgen, Übertragungen und Regulierungen zu übernehmen.  

Stellen Sie sicher, dass der **Integrationsschlüssel** für **msdyn_workorders** vorhanden ist:
1. Gehen Sie zu Datenintegration.
2. Wählen Sie **Verbindungssatz** Registerkarte
3. Wählen Sie das für die Synchronisation der Arbeitsaufträge verwendete Verbindungsset aus.
4. Wählen Sie **Integrationsschlüssel** Registerkarte
5. Suchen Sie msdyn_workorders und überprüfen Sie, ob der Schlüssel **msdyn_name (Name)** hinzugefügt wurde. Wenn es nicht angezeigt wird, fügen Sie es durch Klicken auf **Schlüssel hinzufügen** und klicken Sie auf **Speichern** im oberen Bereich der Seite.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Lagerorte (Supply Chain Management zu Field Service): Lagerort

[![Vorlagenzuordnung in Datenintegration.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
