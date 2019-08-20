---
title: Projektliste von Finance and Operations mit Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843552"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Projektliste von Finance and Operations mit Field Service synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisation von Projekten von Microsoft Dynamics 365 for Finance and Operations nach Microsoft Dynamics 365 for Field Service durchzuführen.

**Vorlagen in der Datenintegration**
- Projects (Finance and Operations zu Field Service)

**Aufgaben im Datenintegrationsprojekt**
- Projekte

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Projektlisten erfolgen kann:
- Konten (Sales nach Finance and Operations) 

## <a name="entity-set"></a>Entitätssatz
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekte                |

## <a name="entity-flow"></a>Entitätsfluss
Projekte werden in Finance and Operations erstellt. Projekte mit **Projekttyp** **Zeit und -material** und **Projektphase** **Prozess** synchronisiert mit **Externer Projekt** Entität in Field Service, einschließlich Projektnummeren-, Projektnamen-, und Projektphasen und Debitorenkontoinformationen. Die Liste **Externes Projekt** wird verwendet, um Field Service Arbeitsaufträge mit Finance and Operations Projekte zu verbinden.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Die Entität ruft **Externes Projekt** alle Projekte von der erhaltenen Finanzierung und Arbeitsgängen ab. Das Feld **Externes Projekt** ist der **Arbeitsauftragsentität** hinzugefügt worden. Dieses Feld ist ein Suchfeld. Durch das Markieren des Arbeitsauftrags mit einem Projekt wird der Auftrag dem Projekt in Finance and Operations verbunden. Wenn der **Systemstatus** von **Offen auf In Verarbeitung (690.970.000)** auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung
### <a name="finance-and-operations"></a>Finance and Operations
Änderungsnachverfolgung für Datentitätprojekte nachverfolgen

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Projects (Finance and Operations zu Field Service): Projects

[![Vorlagenzuordnung in Datenintegration](./media/FSProject1.png)](./media/FSProject1.png)
