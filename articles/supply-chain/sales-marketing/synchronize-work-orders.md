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
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="4039f-103">Arbeitsaufträge mit Projekt von Field Service zu Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="4039f-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4039f-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Microsoft Dynamics 365 for Field Service mit Aufträgen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4039f-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="4039f-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="4039f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="4039f-106">Die verwendete Vorlage **Arbeitsaufträge mit Projekt (Field Serivce zu Fin and Ops)** basiert auf der Vorlage **Arbeitsaufträge (Field Service zu Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="4039f-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="4039f-107">Weitere Informationen finden Sie unter [Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations synchronisieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="4039f-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="4039f-108">In diesem Thema werden nur die Unterschiede zwischen den zwei Vorlagen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="4039f-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="4039f-109">**Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="4039f-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="4039f-110">**Arbeitsaufträge (Field Service zu Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="4039f-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="4039f-111">Der Hauptunterschied ist, dass diese Vorlage Zuordnung der Projektnummer enthalten, die dem Arbeitsauftrag im Field SErvice zugewiesen sind, um sicherzustellen, dass der Auftrag, der im Bereich Finance and Operations erstellt wird, die Projektnummer enthalten und die Rechnungsstellung auf das zugehörige Projekt ausgeführt kann.</span><span class="sxs-lookup"><span data-stu-id="4039f-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="4039f-112">Zudem verwendet diese Vorlage erweiterte Abfrage und Filtern.</span><span class="sxs-lookup"><span data-stu-id="4039f-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4039f-113">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="4039f-113">Templates and tasks</span></span>

<span data-ttu-id="4039f-114">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="4039f-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="4039f-115">Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4039f-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="4039f-116">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="4039f-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="4039f-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="4039f-117">WorkOrderHeader</span></span>
- <span data-ttu-id="4039f-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="4039f-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="4039f-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="4039f-119">WorkOrderProduct</span></span>
- <span data-ttu-id="4039f-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="4039f-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="4039f-121">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="4039f-121">Field Service CRM solution</span></span>
<span data-ttu-id="4039f-122">Das Feld **Externes Projekt** ist der Arbeitsauftragsentität hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="4039f-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="4039f-123">Dieses Feld ist ein Suchfeld und  verbindet den Arbeitsauftrag mit einem Projekt. Der Auftrag wird dann mit dem Projekt in Finance and Operations verbunden.</span><span class="sxs-lookup"><span data-stu-id="4039f-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="4039f-124">Wenn der **Systemstatus** von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="4039f-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4039f-125">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="4039f-125">Template mapping in Data integration</span></span>

<span data-ttu-id="4039f-126">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="4039f-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="4039f-127">Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="4039f-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="4039f-128">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="4039f-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="4039f-129">Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="4039f-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="4039f-130">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="4039f-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="4039f-131">Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="4039f-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="4039f-132">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="4039f-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="4039f-133">Arbeitsaufträge mit Projekt (Field Service zu Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="4039f-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="4039f-134">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="4039f-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
