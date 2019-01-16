---
title: Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="01f6a-103">Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="01f6a-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="01f6a-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="01f6a-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="01f6a-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="01f6a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="01f6a-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="01f6a-106">Templates and tasks</span></span>
<span data-ttu-id="01f6a-107">Die folgende Vorlage und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="01f6a-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="01f6a-108">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="01f6a-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="01f6a-109">Produktbestand (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="01f6a-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="01f6a-110">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="01f6a-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="01f6a-111">Produktbestand</span><span class="sxs-lookup"><span data-stu-id="01f6a-111">Product inventory</span></span>

<span data-ttu-id="01f6a-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Bestandlisten erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="01f6a-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="01f6a-113">Projekte (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="01f6a-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="01f6a-114">Field Service Produkte mit Lagereinheit (Finance and Operations zu Sales)</span><span class="sxs-lookup"><span data-stu-id="01f6a-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="01f6a-115">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="01f6a-115">Entity set</span></span>

| <span data-ttu-id="01f6a-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="01f6a-116">Field Service</span></span>                      | <span data-ttu-id="01f6a-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="01f6a-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="01f6a-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="01f6a-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="01f6a-119">Verfügbarer CDS-Lagerbestand nach Lagerort</span><span class="sxs-lookup"><span data-stu-id="01f6a-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="01f6a-120">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="01f6a-120">Entity flow</span></span>
<span data-ttu-id="01f6a-121">Bestandebeneninformationen aus Finance and Operations mit Field Service für ausgewählte Produkte synchronisieren</span><span class="sxs-lookup"><span data-stu-id="01f6a-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="01f6a-122">Die Betandsinformationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="01f6a-122">The inventory level information include:</span></span> 
- <span data-ttu-id="01f6a-123">Verfügbare Menge (Aktuell erfasste Menge am Lagerort physisch)</span><span class="sxs-lookup"><span data-stu-id="01f6a-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="01f6a-124">Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - h. Aufträge)</span><span class="sxs-lookup"><span data-stu-id="01f6a-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="01f6a-125">Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - d.h. Bestellungen)</span><span class="sxs-lookup"><span data-stu-id="01f6a-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="01f6a-126">Diese Informationen werden pro freigegebenes Produkt für jeden Lagerort aufgezeichnet und synchronisiert auf Grundlage der Änderungsnachverfolgung, wenn der Lagerbestand ändert.</span><span class="sxs-lookup"><span data-stu-id="01f6a-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="01f6a-127">Im Field Service erstellt die Integrationslösung Bestanderfassungen für das Delta, um die Stufen im Fielöd Service abzurufen, die den Stufen im Bereich Finance and Operations abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="01f6a-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="01f6a-128">Finance and Operations dient als Master für die Bestandebenen.</span><span class="sxs-lookup"><span data-stu-id="01f6a-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="01f6a-129">Daher ist es wichtig, die Integration für Arbeitsaufträge, Übertragungen und Regulierungen von Field Service zu Finance and Operations einzurichen, wenn diese Funktionen in Field Service zusammen mit dem Synchronisieren von Lagerbeständen von Finane and Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01f6a-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="01f6a-130">Die Produkte und die Lagerorte, in denen Lagerbestände verwaltet werden von Finance and Operations können mit der erweiterten Abfrage und Filterung (Power-Abfrage) gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="01f6a-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="01f6a-131">Hinweis: Es ist möglich, mehrere Lagerorte in Field Services zu erstellen (mit wird extern verwaltet = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01f6a-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="01f6a-132">Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="01f6a-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="01f6a-133">In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="01f6a-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="01f6a-134">Siehe zusätzliche Informationen unter Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="01f6a-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="01f6a-135">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="01f6a-135">Field Service CRM solution</span></span>
<span data-ttu-id="01f6a-136">Die externe Produktbestandslistenentität ist eine neue Entität, die nur für Back-End der Integration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01f6a-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="01f6a-137">Sie erhalten die Lagerbestandswerte von Finance and Operations in der Integdration und transformiert dann jene Werte manuell zur Bestanderfassung, welche dann die Bestandprodukte am Lagerort ändert.</span><span class="sxs-lookup"><span data-stu-id="01f6a-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="01f6a-138">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="01f6a-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="01f6a-139">Im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="01f6a-139">In the Data Integration project</span></span>
<span data-ttu-id="01f6a-140">Wenden Sie Filter mit der erweiterten Abfrage und Filterung an, um zu steuern, dass nur gewünschte Produkte und Lagerorte Lagerbestandsinformationen von Finance and Operations zu Field Service sendet.</span><span class="sxs-lookup"><span data-stu-id="01f6a-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="01f6a-141">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="01f6a-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="01f6a-142">Produktbestand (Finance and Operations zu Field Service): Produktbestand</span><span class="sxs-lookup"><span data-stu-id="01f6a-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="01f6a-143">[![Vorlagenzuordnung in Datenintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="01f6a-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

