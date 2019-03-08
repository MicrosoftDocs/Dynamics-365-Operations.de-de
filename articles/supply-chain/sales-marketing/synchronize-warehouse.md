---
title: Lagerorte von Finance and Operations mit Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Lager aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "340314"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="27b20-103">Lagerorte von Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="27b20-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27b20-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Lager aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="27b20-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="27b20-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="27b20-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="27b20-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="27b20-106">Templates and tasks</span></span>
<span data-ttu-id="27b20-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisation von Lagern von Microsoft Dynamics 365 for Finance and Operations nach Microsoft Dynamics 365 for Field Service durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="27b20-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="27b20-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="27b20-108">**Template in Data integration**</span></span>
- <span data-ttu-id="27b20-109">Projekte (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="27b20-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="27b20-110">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="27b20-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="27b20-111">Lagerort</span><span class="sxs-lookup"><span data-stu-id="27b20-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="27b20-112">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="27b20-112">Entity set</span></span>
| <span data-ttu-id="27b20-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="27b20-113">Field Service</span></span>    | <span data-ttu-id="27b20-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27b20-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="27b20-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="27b20-115">msdyn_warehouses</span></span> | <span data-ttu-id="27b20-116">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="27b20-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="27b20-117">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="27b20-117">Entity flow</span></span>
<span data-ttu-id="27b20-118">Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Finance and Operations über ein Common Data Service (CDS)-Datenintegrationsprojekt synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="27b20-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="27b20-119">Die gewünschten Lagerorte, die mit Field Service synchronisieren, können mit der Abfrage und der erweiterten Filterung im Projekt gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="27b20-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="27b20-120">Lagerorte, die von Finance and Operations synchronisieren, werden im Field Service **mit dem Feld erstellt und extern auf** **Ja** festgelegt und der Datensatz wird als schreibgeschützt erstellt.</span><span class="sxs-lookup"><span data-stu-id="27b20-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="27b20-121">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="27b20-121">Field Service CRM solution</span></span>
<span data-ttu-id="27b20-122">Um die Integration zwischen Field Service und Finance and Operations zu unterstützen, sind zusätzliche Funktionen aus der Field Service CRM-Lösung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="27b20-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="27b20-123">In der Lösung wurde das Feld **Is Maintained Externally** zur Entität **Warehouse (msdyn_warehouses)** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="27b20-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="27b20-124">Dieses Feld dient zur Identifizierung, ob das Lager aus Finance and Operations gehandhabt wird oder ob es nur in Field Service existiert.</span><span class="sxs-lookup"><span data-stu-id="27b20-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="27b20-125">Zu den Einstellungen für dieses Feld gehören:</span><span class="sxs-lookup"><span data-stu-id="27b20-125">The settings for this field include:</span></span>
- <span data-ttu-id="27b20-126">**Ja** – Der Lagerort stammt aus Finance and Operations und wird nicht in Sales bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="27b20-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="27b20-127">**Nein** - Der Lagerort wurde direkt in Field Service eingegeben und wird hier verwaltet.</span><span class="sxs-lookup"><span data-stu-id="27b20-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="27b20-128">Das Feld wird **Extern verwaltet** hilft, die Synchronisierung von Bestandebenen, Regulierunmgen, Überträgen und der Verwendung von Arbeitsaufträgen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="27b20-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="27b20-129">Nur Lagerorte mit **Werden exern verwaltet** = **Ja** können verwendet werden, um direkt den gleichen Lagerort im anderen System zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="27b20-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="27b20-130">Es ist möglich, mehrere Lagerorte in Field Service zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27b20-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="27b20-131">Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="27b20-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="27b20-132">In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27b20-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="27b20-133">Siehe zusätzliche Informationen unter [Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) und [synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="27b20-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="27b20-134">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="27b20-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="27b20-135">Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="27b20-135">Data Integration project</span></span>
<span data-ttu-id="27b20-136">Vor der Synchronisierung der Lagerorte stellen Sie sicher, die erweiterte Abfrage und Filterung im Projekt zu aktualisieren, die nur Lagerorte einbeziehen, die mithilfe von Finance and Operations mit Field Service vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="27b20-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="27b20-137">Beachten Sie, dass Sie den Lagerort im Field Service benötigen, um sie in Arbeitsaufträgen, Übertragungen und Regulierungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="27b20-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="27b20-138">Stellen Sie sicher, dass der **Integrationsschlüssel** für **msdyn_workorders** vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="27b20-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="27b20-139">Gehen Sie zu Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="27b20-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="27b20-140">Wählen Sie **Verbindungssatz** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="27b20-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="27b20-141">Wählen Sie das für die Synchronisation der Arbeitsaufträge verwendete Verbindungsset aus.</span><span class="sxs-lookup"><span data-stu-id="27b20-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="27b20-142">Wählen Sie **Integrationsschlüssel** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="27b20-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="27b20-143">Suchen Sie msdyn_workorders und überprüfen Sie, ob der Schlüssel **msdyn_name (Name)** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="27b20-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="27b20-144">Wenn es nicht angezeigt wird, fügen Sie es durch Klicken auf **Schlüssel hinzufügen** und klicken Sie auf **Speichern** im oberen Bereich der Seite.</span><span class="sxs-lookup"><span data-stu-id="27b20-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="27b20-145">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="27b20-145">Template mapping in Data integration</span></span>

<span data-ttu-id="27b20-146">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="27b20-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="27b20-147">Lagerorte (Finance and Operations zu Field Service): Lagerorte</span><span class="sxs-lookup"><span data-stu-id="27b20-147">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="27b20-148">[![Vorlagenzuordnung in Datenintegration](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="27b20-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
