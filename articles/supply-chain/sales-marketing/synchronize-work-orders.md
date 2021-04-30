---
title: Arbeitsaufträge mit Projekt von Field Service mit Supply Chain Management synchronisieren
description: Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Dynamics 365 Field Service mit Aufträgen in Dynamics 365 Supply Chain Management zu synchronisieren.
author: ChristianRytt
ms.date: 03/12/2019
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
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 0956e7aa51973014ee474d97829d3d15dfdea3b3
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909942"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="0c4de-103">Arbeitsaufträge mit Projekt von Field Service mit Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="0c4de-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0c4de-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Dynamics 365 Field Service mit Aufträgen in Dynamics 365 Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0c4de-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0c4de-105">[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="0c4de-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="0c4de-106">Die verwendete Vorlage **Arbeitsaufträge mit Projekt (Field Serivce zu Supply Chain Management)** basiert auf der Vorlage **Arbeitsaufträge (Field Service zu Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="0c4de-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="0c4de-107">Weitere Informationen finden Sie unter [Arbeitsaufträge in Field Service mit Aufträgen in Supply Chain Management synchronisieren](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="0c4de-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="0c4de-108">In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="0c4de-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="0c4de-109">**Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="0c4de-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="0c4de-110">**Arbeitsaufträge (Field Service zu Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="0c4de-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="0c4de-111">Der Hauptunterschied ist, dass diese Vorlage Zuordnung der Projektnummer enthalten, die dem Arbeitsauftrag im Field Service zugewiesen sind, um sicherzustellen, dass der Auftrag, der im Bereich Supply Chain Management erstellt wird, die Projektnummer enthalten und die Rechnungsstellung auf das zugehörige Projekt ausgeführt kann.</span><span class="sxs-lookup"><span data-stu-id="0c4de-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="0c4de-112">Zudem verwendet diese Vorlage erweiterte Abfrage und Filtern.</span><span class="sxs-lookup"><span data-stu-id="0c4de-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0c4de-113">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="0c4de-113">Templates and tasks</span></span>

<span data-ttu-id="0c4de-114">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="0c4de-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="0c4de-115">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="0c4de-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="0c4de-116">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="0c4de-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="0c4de-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0c4de-117">WorkOrderHeader</span></span>
- <span data-ttu-id="0c4de-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="0c4de-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="0c4de-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="0c4de-119">WorkOrderProduct</span></span>
- <span data-ttu-id="0c4de-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="0c4de-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="0c4de-121">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="0c4de-121">Field Service CRM solution</span></span>
<span data-ttu-id="0c4de-122">Das Feld **Externes Projekt** ist der Arbeitsauftragsentität hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="0c4de-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="0c4de-123">Dieses Feld ist ein Suchfeld. Durch das Markieren des Arbeitsauftrags mit einem Projekt wird der Auftrag mit dem Projekt in Supply Chain Management verbunden.</span><span class="sxs-lookup"><span data-stu-id="0c4de-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="0c4de-124">Wenn der **Systemstatus** von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="0c4de-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0c4de-125">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="0c4de-125">Template mapping in Data integration</span></span>

<span data-ttu-id="0c4de-126">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="0c4de-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="0c4de-127">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0c4de-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="0c4de-128">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="0c4de-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="0c4de-129">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="0c4de-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="0c4de-130">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="0c4de-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="0c4de-131">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="0c4de-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="0c4de-132">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="0c4de-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="0c4de-133">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="0c4de-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="0c4de-134">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="0c4de-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]