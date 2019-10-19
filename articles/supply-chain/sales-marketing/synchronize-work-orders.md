---
title: Arbeitsaufträge mit Projekt von Field Service mit Supply Chain Management synchronisieren
description: Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Dynamics 365 Field Service mit Aufträgen in Dynamics 365 Supply Chain Management zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 3678fbca8244ae6dcd050f6a91ff3b35d90e1064
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251706"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="3f3f2-103">Arbeitsaufträge mit Projekt von Field Service mit Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3f3f2-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3f3f2-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Dynamics 365 Field Service mit Aufträgen in Dynamics 365 Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="3f3f2-105">[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="3f3f2-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="3f3f2-106">Die verwendete Vorlage **Arbeitsaufträge mit Projekt (Field Serivce zu Supply Chain Management)** basiert auf der Vorlage **Arbeitsaufträge (Field Service zu Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="3f3f2-107">Weitere Informationen finden Sie unter [Arbeitsaufträge in Field Service mit Aufträgen in Supply Chain Management synchronisieren](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="3f3f2-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="3f3f2-108">In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3f3f2-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="3f3f2-109">**Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="3f3f2-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="3f3f2-110">**Arbeitsaufträge (Field Service zu Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="3f3f2-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="3f3f2-111">Der Hauptunterschied ist, dass diese Vorlage Zuordnung der Projektnummer enthalten, die dem Arbeitsauftrag im Field Service zugewiesen sind, um sicherzustellen, dass der Auftrag, der im Bereich Supply Chain Management erstellt wird, die Projektnummer enthalten und die Rechnungsstellung auf das zugehörige Projekt ausgeführt kann.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="3f3f2-112">Zudem verwendet diese Vorlage erweiterte Abfrage und Filtern.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3f3f2-113">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="3f3f2-113">Templates and tasks</span></span>

<span data-ttu-id="3f3f2-114">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="3f3f2-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="3f3f2-115">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="3f3f2-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="3f3f2-116">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="3f3f2-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="3f3f2-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="3f3f2-117">WorkOrderHeader</span></span>
- <span data-ttu-id="3f3f2-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="3f3f2-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="3f3f2-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="3f3f2-119">WorkOrderProduct</span></span>
- <span data-ttu-id="3f3f2-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="3f3f2-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="3f3f2-121">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="3f3f2-121">Field Service CRM solution</span></span>
<span data-ttu-id="3f3f2-122">Das Feld **Externes Projekt** ist der Arbeitsauftragsentität hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="3f3f2-123">Dieses Feld ist ein Suchfeld. Durch das Markieren des Arbeitsauftrags mit einem Projekt wird der Auftrag mit dem Projekt in Supply Chain Management verbunden.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="3f3f2-124">Wenn der **Systemstatus** von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3f3f2-125">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="3f3f2-125">Template mapping in Data integration</span></span>

<span data-ttu-id="3f3f2-126">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="3f3f2-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="3f3f2-127">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="3f3f2-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="3f3f2-128">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="3f3f2-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="3f3f2-129">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="3f3f2-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="3f3f2-130">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="3f3f2-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="3f3f2-131">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="3f3f2-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="3f3f2-132">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="3f3f2-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="3f3f2-133">Arbeitsaufträge mit Projekt (Field Service zu Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="3f3f2-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="3f3f2-134">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="3f3f2-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
