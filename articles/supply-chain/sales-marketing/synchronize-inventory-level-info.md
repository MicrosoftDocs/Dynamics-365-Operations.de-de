---
title: Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsinformationen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535697"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="863a4-103">Lagerebeneninformationen aus Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="863a4-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="863a4-104">In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsinformationen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="863a4-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="863a4-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="863a4-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="863a4-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="863a4-106">Templates and tasks</span></span>
<span data-ttu-id="863a4-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsdaten von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="863a4-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="863a4-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="863a4-108">**Template in Data integration**</span></span>
- <span data-ttu-id="863a4-109">Produktbestand (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="863a4-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="863a4-110">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="863a4-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="863a4-111">Produktbestand</span><span class="sxs-lookup"><span data-stu-id="863a4-111">Product inventory</span></span>

<span data-ttu-id="863a4-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Bestandlisten erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="863a4-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="863a4-113">Lagerorte (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="863a4-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="863a4-114">Field Service Produkte mit Bestand (Finance and Operations zu Sales)</span><span class="sxs-lookup"><span data-stu-id="863a4-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="863a4-115">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="863a4-115">Entity set</span></span>

| <span data-ttu-id="863a4-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="863a4-116">Field Service</span></span>                      | <span data-ttu-id="863a4-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="863a4-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="863a4-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="863a4-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="863a4-119">Verfügbarer CDS-Lagerbestand nach Lagerort</span><span class="sxs-lookup"><span data-stu-id="863a4-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="863a4-120">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="863a4-120">Entity flow</span></span>
<span data-ttu-id="863a4-121">Bestandebeneninformationen aus Finance and Operations mit Field Service für ausgewählte Produkte synchronisieren</span><span class="sxs-lookup"><span data-stu-id="863a4-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="863a4-122">Die Betandsinformationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="863a4-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="863a4-123">Verfügbare Menge (Aktuell erfasste Menge am Lagerort physisch)</span><span class="sxs-lookup"><span data-stu-id="863a4-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="863a4-124">Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - h. Aufträge)</span><span class="sxs-lookup"><span data-stu-id="863a4-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="863a4-125">Bestellte Menge (Gesamtsumme erfasste Menge in Aufträgen - d.h. Bestellungen)</span><span class="sxs-lookup"><span data-stu-id="863a4-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="863a4-126">Diese Informationen werden pro freigegebenes Produkt für jeden Lagerort aufgezeichnet und synchronisiert auf Grundlage der Änderungsnachverfolgung, wenn der Lagerbestand ändert.</span><span class="sxs-lookup"><span data-stu-id="863a4-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="863a4-127">Im Field Service erstellt die Integrationslösung Bestanderfassungen für das Delta, um die Stufen im Fielöd Service abzurufen, die den Stufen im Bereich Finance and Operations abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="863a4-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="863a4-128">Finance and Operations dient als Master für die Bestandebenen.</span><span class="sxs-lookup"><span data-stu-id="863a4-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="863a4-129">Daher ist es wichtig, die Integration für Arbeitsaufträge, Übertragungen und Regulierungen von Field Service zu Finance and Operations einzurichen, wenn diese Funktionen in Field Service zusammen mit dem Synchronisieren von Lagerbeständen von Finane and Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="863a4-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="863a4-130">Die Produkte und die Lagerorte, in denen Lagerbestände verwaltet werden von Finance and Operations können mit der erweiterten Abfrage und Filterung (Power-Abfrage) gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="863a4-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="863a4-131">Es ist möglich, mehrere Lagerorte in Field Service zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="863a4-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="863a4-132">Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="863a4-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="863a4-133">In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="863a4-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="863a4-134">Siehe zusätzliche Informationen unter [Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) und [synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="863a4-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="863a4-135">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="863a4-135">Field Service CRM solution</span></span>
<span data-ttu-id="863a4-136">Die **externe Produktbestandslistenentität** ist eine neue Entität, die nur für Back-End der Integration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="863a4-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="863a4-137">Sie erhalten die Lagerbestandswerte von Finance and Operations in der Integdration und transformiert dann jene Werte manuell zur Bestanderfassung, welche dann die Bestandprodukte am Lagerort ändert.</span><span class="sxs-lookup"><span data-stu-id="863a4-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="863a4-138">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="863a4-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="863a4-139">Datenintegration</span><span class="sxs-lookup"><span data-stu-id="863a4-139">Data integration</span></span>
<span data-ttu-id="863a4-140">Damit das Projekt funktioniert, müssen Sie sicherstellen, dass der Integrationsschlüssel für msdynce_externalproductinventories aktualisiert ist.</span><span class="sxs-lookup"><span data-stu-id="863a4-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="863a4-141">Wechseln Sie zu **Datenintegration > Verbindungssätze**.</span><span class="sxs-lookup"><span data-stu-id="863a4-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="863a4-142">Wählen Sie den verwendeten Verbindungssatz aus.</span><span class="sxs-lookup"><span data-stu-id="863a4-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="863a4-143">In der Registerkarte **Integrationsschlüssel** stellen Sie sicher, dass die folgenden Schlüssel zu msdynce_externalproductinventories hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="863a4-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="863a4-144">msdynce_productnumber (Produktnummer)</span><span class="sxs-lookup"><span data-stu-id="863a4-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="863a4-145">msdynce_warehouseid (Warehouse-Kennung)</span><span class="sxs-lookup"><span data-stu-id="863a4-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="863a4-146">Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="863a4-146">Data integration project</span></span>
<span data-ttu-id="863a4-147">Wenden Sie Filter mit der erweiterten Abfrage und Filterung an, um zu steuern, dass nur gewünschte Produkte und Lagerorte Lagerbestandsinformationen von Finance and Operations zu Field Service sendet.</span><span class="sxs-lookup"><span data-stu-id="863a4-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="863a4-148">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="863a4-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="863a4-149">Produktbestand (Finance and Operations zu Field Service): Produktbestand</span><span class="sxs-lookup"><span data-stu-id="863a4-149">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="863a4-150">[![Vorlagenzuordnung in Datenintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="863a4-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
