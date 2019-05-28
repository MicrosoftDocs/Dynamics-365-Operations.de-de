---
title: Arbeitsaufträge mit Projekt von Field Service zu Finance and Operations synchronisieren
description: Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Microsoft Dynamics 365 for Field Service mit Aufträgen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536732"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Arbeitsaufträge mit Projekt von Field Service zu Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Microsoft Dynamics 365 for Field Service mit Aufträgen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Die verwendete Vorlage **Arbeitsaufträge mit Projekt (Field Serivce zu Fin and Ops)** basiert auf der Vorlage **Arbeitsaufträge (Field Service zu Fin and Ops)**. Weitere Informationen finden Sie unter [Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations synchronisieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben:
- **Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops)**
- **Arbeitsaufträge (Field Service zu Fin and Ops)**

Der Hauptunterschied ist, dass diese Vorlage Zuordnung der Projektnummer enthalten, die dem Arbeitsauftrag im Field SErvice zugewiesen sind, um sicherzustellen, dass der Auftrag, der im Bereich Finance and Operations erstellt wird, die Projektnummer enthalten und die Rechnungsstellung auf das zugehörige Projekt ausgeführt kann. Zudem verwendet diese Vorlage erweiterte Abfrage und Filtern.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

**Name der Vorlage in der Datenintegration:**

- Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops)

**Name der Aufgabe im Datenintegrationsprojekt:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung
Das Feld **Externes Projekt** ist der Arbeitsauftragsentität hinzugefügt worden. Dieses Feld ist ein Suchfeld und  verbindet den Arbeitsauftrag mit einem Projekt. Der Auftrag wird dann mit dem Projekt in Finance and Operations verbunden. Wenn der **Systemstatus** von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderHeader

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderHeaderProject

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderProduct

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderService

[![Vorlagenzuordnung in Datenintegration](./media/FSWOP4.png)](./media/FSWOP4.png)
