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

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="9d3a9-103">Arbeitsaufträge mit Projekt von Field Service zu Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="9d3a9-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9d3a9-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Aufträge mit Projektnummer aus Microsoft Dynamics 365 for Field Service mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="9d3a9-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="9d3a9-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="9d3a9-106">Die verwendete Vorlage **Field Service-Produkte (Finance and Operations nach Field Service)** basiert auf der Vorlage **Produkte (Finance and Operations nach Sales) – Direkt** aus Interessenten zu Bargeld.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="9d3a9-107">Weitere Informationen finden Sie unter [Produkte (Finance and Operations nach Sales) – Direkt](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="9d3a9-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="9d3a9-108">In diesem Thema wird nur der Unterschied zwischen den Vorlagen **Field Service-Produkte (Finance and Operations nach Field Service)** und **Produkte (Finance and Operations nach Sales) – Direkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="9d3a9-109">Der Hauptunterschied ist, dass diese Vorlage Zuordnung der Projektnummer enthalten, die dem Arbeitsauftrag im Field SErvice zugewiesen sind, um sicherzustellen, dass der Auftrag, der im Bereich Finance and Operations erstellt wird, die Projektnummer enthalten und die Rechnungsstellung auf das zugehörige Projekt ausgeführt kann.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="9d3a9-110">Zudem verwendet diese Vorlage erweiterte Abfrage und Filtern.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9d3a9-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="9d3a9-111">Templates and tasks</span></span>

<span data-ttu-id="9d3a9-112">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="9d3a9-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="9d3a9-113">Arbeitsaufträge mit Projekct (Field SErvice zu Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="9d3a9-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="9d3a9-114">**Name der Aufgabe im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="9d3a9-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="9d3a9-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="9d3a9-115">WorkOrderHeader</span></span>
- <span data-ttu-id="9d3a9-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="9d3a9-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="9d3a9-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="9d3a9-117">WorkOrderProduct</span></span>
- <span data-ttu-id="9d3a9-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="9d3a9-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="9d3a9-119">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="9d3a9-119">Field Service CRM solution</span></span>
<span data-ttu-id="9d3a9-120">Das Feld **Externes Projekt** ist der Arbeitsauftragsentität hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="9d3a9-121">Dieses Feld ist ein Suchfeld und  verbindet den Arbeitsauftrag mit einem Projekt. Der Auftrag wird dann mit dem Projekt in Finance and Operations verbunden.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="9d3a9-122">Wenn der **Systemstatus** von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9d3a9-123">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="9d3a9-123">Template mapping in Data integration</span></span>

<span data-ttu-id="9d3a9-124">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="9d3a9-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="9d3a9-125">Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="9d3a9-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="9d3a9-126">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="9d3a9-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="9d3a9-127">Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="9d3a9-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="9d3a9-128">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="9d3a9-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="9d3a9-129">Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="9d3a9-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="9d3a9-130">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="9d3a9-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="9d3a9-131">Arbeitsaufträge mit Projekct (Field Service zu Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="9d3a9-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="9d3a9-132">[![Vorlagenzuordnung in Datenintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="9d3a9-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

