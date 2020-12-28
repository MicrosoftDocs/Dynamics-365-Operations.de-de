---
title: Projektliste von Supply Chain Management zu Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428371"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Projektliste von Supply Chain Management zu Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekte von Supply Chain Management auf Field Service zu synchronisieren.

**Vorlagen in der Datenintegration**
- Projekte (Supply Chain Management zu Field Service)

**Aufgaben im Datenintegrationsprojekt**
- Projekte

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Projektlisten erfolgen kann:
- Konten (Sales zu Supply Chain Management) 

## <a name="entity-set"></a>Entitätssatz
| Field Service           | Lieferkettenverwaltung  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekte                |

## <a name="entity-flow"></a>Entitätsfluss
Projekte werden in Supply Chain Management erstellt. Projekte mit **Projekttyp** **Zeit und -material** und **Projektphase** **Prozess** synchronisiert mit **Externer Projekt** Entität in Field Service, einschließlich Projektnummeren-, Projektnamen-, und Projektphasen und Debitorenkontoinformationen. Die Liste **Externes Projekt** wird verwendet, um Field Service Arbeitsaufträge mit Supply Chain Management-Projekten zu verbinden.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Die Entität **Externes Projekt** ruft alle Projekte aus Supply Chain Management ab. Das Feld **Externes Projekt** ist der **Arbeitsauftragsentität** hinzugefügt worden. Dieses Feld ist ein Suchfeld. Durch das Markieren des Arbeitsauftrags mit einem Projekt wird der Auftrag dem Projekt in Supply Chain Management verbunden. Wenn der **Systemstatus** von **Offen auf In Verarbeitung (690.970.000)** auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung
### <a name="supply-chain-management"></a>Lieferkettenverwaltung
Änderungsnachverfolgung für Datentitätprojekte nachverfolgen

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projekte (Supply Chain Management zu Field Service): Projekt

[![Vorlagenzuordnung in Datenintegration](./media/FSProject1.png)](./media/FSProject1.png)
