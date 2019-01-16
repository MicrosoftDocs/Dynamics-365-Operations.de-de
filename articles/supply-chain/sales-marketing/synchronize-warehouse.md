---
title: Lagerorte von Finance and Operations mit Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c938a-103">Lagerorte von Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c938a-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c938a-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c938a-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c938a-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="c938a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c938a-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c938a-106">Templates and tasks</span></span>
<span data-ttu-id="c938a-107">Die folgende Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c938a-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c938a-108">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="c938a-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="c938a-109">Projekte (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="c938a-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="c938a-110">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="c938a-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="c938a-111">Lagerort</span><span class="sxs-lookup"><span data-stu-id="c938a-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="c938a-112">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="c938a-112">Entity set</span></span>
| <span data-ttu-id="c938a-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="c938a-113">Field Service</span></span>    | <span data-ttu-id="c938a-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c938a-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="c938a-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="c938a-115">msdyn_warehouses</span></span> | <span data-ttu-id="c938a-116">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="c938a-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="c938a-117">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="c938a-117">Entity flow</span></span>
<span data-ttu-id="c938a-118">Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Finance and Operations über ein Common Data Service (CDS)-Datenintegrationsprojekt synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c938a-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="c938a-119">Die gewünschten Lagerorte, die mit Field Service synchronisieren, können mit der Abfrage und der erweiterten Filterung im Projekt gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="c938a-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="c938a-120">Lagerorte, die von Finance and Operations synchronisieren, werden im Field Service mit dem Feld erstellt und extern auf Ja festgelegt und der Datensatz wird als schreibgeschützt erstellt.</span><span class="sxs-lookup"><span data-stu-id="c938a-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="c938a-121">Field Service CRM Lösung um die Integration zwischen Field Service und Finance and Operations zu unterstützen, sind zusätzliche Funktionen aus der Field Service CRM-Lösung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c938a-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="c938a-122">Die Lösung enthält die folgenden Änderungen.</span><span class="sxs-lookup"><span data-stu-id="c938a-122">The solution includes the following changes.</span></span>
<span data-ttu-id="c938a-123">Das Feld **Wird extern verwaltet** wurde der Entität **Lagerort (msdyn_warehouses)** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c938a-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="c938a-124">Dieses Feld hilft zu ermitteln, ob der Lagerort von Operations behandelt wird oder ob es nur in Field Service vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c938a-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="c938a-125">Ja – Der Lagerort stammt aus Finance and Operations und wird nicht in Sales bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="c938a-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="c938a-126">Nwin - Der Lagerort wurde direkt in Field Service eingegeben und wird hier verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c938a-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="c938a-127">Das Feld wird **Extern verwaltet** hilft, die Synchronisierung von Bestandebenen, Regulierunmgen, Überträgen und der Verwendung von Arbeitsaufträgen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c938a-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="c938a-128">Nur Lagerorte mit **Werden exern verwaltet** = Ja können verwendet werden, um direkt den gleichen Lagerort im anderen System zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c938a-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="c938a-129">Hinweis: Es ist möglich, mehrere Lagerorte in Field Services zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort im Bereich Finance and Operations mit den erweiterten Abfragen und Filterfunktionen dann zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c938a-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="c938a-130">Diese Aufgabe wird in von Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Finance and Operations zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c938a-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="c938a-131">In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c938a-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="c938a-132">Siehe zusätzliche Informationen unter Synchronisierung von Bestandanpassungen von Field Service zu Finance and Operations synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c938a-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c938a-133">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="c938a-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="c938a-134">Im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="c938a-134">In the Data Integration project</span></span>
<span data-ttu-id="c938a-135">Vor der Synchronisierung der Lagerorte stellen Sie sicher, die erweiterte Abfrage und Filterung im Projekt zu aktualisieren, die nur Lagerorte einbeziehen, die mithilfe von Finance and Operations mit Field Service vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c938a-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="c938a-136">Beachten Sie, dass Sie den Lagerort im Field Service benötigen, um sie in Arbeitsaufträgen, Übertragungen und Regulierungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="c938a-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="c938a-137">Stellen Sie sicher, dass der **Integrationsschlüssel** für **msdyn_workorders** vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="c938a-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="c938a-138">Gehen Sie zu Datenintegration</span><span class="sxs-lookup"><span data-stu-id="c938a-138">Go to Data Integration</span></span>
2. <span data-ttu-id="c938a-139">Wählen Sie **Verbindungssatz** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="c938a-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="c938a-140">Wählen Sie das für die Synchronisation der Arbeitsaufträge verwendete Verbindungsset aus.</span><span class="sxs-lookup"><span data-stu-id="c938a-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="c938a-141">Wählen Sie **Integrationsschlüssel** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="c938a-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="c938a-142">Suchen Sie msdyn_workorders und überprüfen Sie, ob der Schlüssel **msdyn_name (Name)** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c938a-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="c938a-143">Wenn es nicht angezeigt wird, fügen Sie es durch Klicken auf **Schlüssel hinzufügen** und klicken Sie auf **Speichern** im oberen Bereich der Seite.</span><span class="sxs-lookup"><span data-stu-id="c938a-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c938a-144">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="c938a-144">Template mapping in Data integration</span></span>

<span data-ttu-id="c938a-145">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="c938a-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="c938a-146">Lagerorte (Finance and Operations zu Field Service): Lagerorte</span><span class="sxs-lookup"><span data-stu-id="c938a-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="c938a-147">[![Vorlagenzuordnung in Datenintegration](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="c938a-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

