---
title: Projektliste von Finance and Operations mit Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Projektliste von Finance and Operations mit Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

**Name der Vorlage in der Datenintegration:**
- Projekte (Finance and Operations zu Field Service)

**Namen der Aufgaben im Datenintegrationsprojekt:**
- Projekte

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Projektlisten erfolgen kann:
- Konten (Sales zu Finance and Operations) 

## <a name="entity-set"></a>Entitätssatz
Field Service  Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekte                |

## <a name="entity-flow"></a>Entitätsfluss
Projekte werden in Finance and Operations erstellt. Projekte mit **Projekttyp** Zeit und -material und **Projektphase** Prozess synchronisiert mit **Externer Projekt** Entität in Field Service, einschließlich Projektnummeren-, Projektnamen-, und Projektphasen und Debitorenkontoinformationen. Die Liste **Externes Projekt** wird verwendet, um Field Service Arbeitsaufträge mit Finance and Operations Projekte zu verbinden.
Field Service CRM Lösund The External Project ist eine neue Entität, die alle Projekte aus Operations abruft.
Das Feld Externes Projekt ist der Arbeitsauftragsentität hinzugefügt worden. Dieses Feld ist ein Suchfeld und  verbindet den Arbeitsauftrag mit einem Projekt. Der Auftrag wird dann mit dem Projekt in Operations verbunden. Wenn der Systemstatus von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status das Feld für externe Projekttypen wird gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung
### <a name="in-finance-and-operations"></a>In Finance and Operations
Änderungsnachverfolgung für Datentitätprojekte nachverfolgen

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projekte (Finance and Operations zu Field Service): Projekte

[![Vorlagenzuordnung in Datenintegration](./media/FSProject1.png)](./media/FSProject1.png)

