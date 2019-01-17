---
title: "Arbeitsaufträge von Finance and Operations mit Field Service synchronisieren"
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Aufträge mit Projektnummer aus Microsoft Dynamics 365 for Field Service mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren."
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Arbeitsaufträge mit Projekt von Field Service zu Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Aufträge mit Projektnummer aus Microsoft Dynamics 365 for Field Service mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Die verwendete Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** basiert auf der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** aus Interessenten zu Bargeld. Weitere Informationen finden Sie unter [Produkte (Finance and Operations nach Sales) – Direkt](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

In diesem Thema wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Finance and Operations nach Field Service)** und **Produkte (Finance and Operations nach Sales) – Direkt** beschrieben.

Der Hauptunterschied ist, dass diese Vorlage Zuordnung der Projektnummer enthalten, die dem Arbeitsauftrag im Field SErvice zugewiesen sind, um sicherzustellen, dass der Auftrag, der im Bereich Finance and Operations erstellt wird, die Projektnummer enthalten und die Rechnungsstellung auf das zugehörige Projekt ausgeführt kann. Zudem verwendet diese Vorlage erweiterte Abfrage und Filtern.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

**Name der Vorlage in der Datenintegration:**

- Arbeitsaufträge mit Projekct (Field SErvice zu Finance and Operations)

**Name der Aufgabe im Datenintegrationsprojekt:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Das Feld **Externes Projekt** ist der Arbeitsauftragsentität hinzugefügt worden. Dieses Feld ist ein Suchfeld und  verbindet den Arbeitsauftrag mit einem Projekt. Der Auftrag wird dann mit dem Projekt in Finance and Operations verbunden. Wenn der **Systemstatus** von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderHeader

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderHeaderProject

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderProduct

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderService

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP4.png)](./media/FSWOP4.png)

