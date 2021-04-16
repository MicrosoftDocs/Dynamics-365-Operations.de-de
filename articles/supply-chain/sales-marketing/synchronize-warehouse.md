---
title: Lagerorte von Supply Chain Management zu Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Lager aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: ChristianRytt
ms.date: 03/13/2019
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
ms.openlocfilehash: b4503b0fea259d30e32dffe636bc0a7ac5528033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807775"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="6c9df-103">Lagerorte von Supply Chain Management zu Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6c9df-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6c9df-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Lager aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6c9df-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="6c9df-105">[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="6c9df-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6c9df-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6c9df-106">Templates and tasks</span></span>
<span data-ttu-id="6c9df-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Lagerorte von Supply Chain Management auf Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6c9df-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="6c9df-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="6c9df-108">**Template in Data integration**</span></span>
- <span data-ttu-id="6c9df-109">Lagerorte (Supply Chain Management zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="6c9df-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="6c9df-110">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="6c9df-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="6c9df-111">Lagerort</span><span class="sxs-lookup"><span data-stu-id="6c9df-111">Warehouse</span></span>

## <a name="table-set"></a><span data-ttu-id="6c9df-112">Tabellensatz</span><span class="sxs-lookup"><span data-stu-id="6c9df-112">Table set</span></span>
| <span data-ttu-id="6c9df-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="6c9df-113">Field Service</span></span>    | <span data-ttu-id="6c9df-114">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="6c9df-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="6c9df-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="6c9df-115">msdyn_warehouses</span></span> | <span data-ttu-id="6c9df-116">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="6c9df-116">Warehouses</span></span>                             |

## <a name="table-flow"></a><span data-ttu-id="6c9df-117">Tabellenfluss</span><span class="sxs-lookup"><span data-stu-id="6c9df-117">Table flow</span></span>
<span data-ttu-id="6c9df-118">Lagerorte, die in Supply Chain Management erstellt und verwaltet werden, können über ein Microsoft Dataverse-Datenintegrationsprojekt nach Field Service synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c9df-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="6c9df-119">Die gewünschten Lagerorte, die mit Field Service synchronisieren, können mit der Abfrage und der erweiterten Filterung im Projekt gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="6c9df-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="6c9df-120">Von Supply Chain Management synchronisierte Lagerorte werden in Field Service erstellt, wobei die Spalte **Wird extern verwaltet** auf **Ja** festgelegt wird und der Datensatz schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="6c9df-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** column set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6c9df-121">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="6c9df-121">Field Service CRM solution</span></span>
<span data-ttu-id="6c9df-122">Um die Integration zwischen Field Service und Supply Chain Management zu unterstützen, sind zusätzliche Funktionen aus der Field Service CRM-Lösung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c9df-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="6c9df-123">In der Lösung wurde die Spalte **Wird extern verwaltet** zur Tabelle **Lagerort (msdyn_warehouses)** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6c9df-123">In the solution, the **Is Maintained Externally** column has been added to the **Warehouse (msdyn_warehouses)** table.</span></span> <span data-ttu-id="6c9df-124">Mit dieser Spalte kann ermittelt werden, ob der Lagerort über Supply Chain Management gehandhabt wird oder ob er nur in Field Service existiert.</span><span class="sxs-lookup"><span data-stu-id="6c9df-124">This column helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="6c9df-125">Zu den Einstellungen für diese Spalte gehören:</span><span class="sxs-lookup"><span data-stu-id="6c9df-125">The settings for this column include:</span></span>
- <span data-ttu-id="6c9df-126">**Ja** – Das Lager stammt aus Supply Chain Management und wird nicht in Sales bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="6c9df-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="6c9df-127">**Nein** - Der Lagerort wurde direkt in Field Service eingegeben und wird hier verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6c9df-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="6c9df-128">Die Spalte **Wird extern verwaltet** hilft, die Synchronisierung von Bestandsebenen, Regulierungen, Überträgen und der Verwendung von Arbeitsaufträgen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="6c9df-128">The **Is Externally Maintained** column helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="6c9df-129">Nur Lagerorte mit **Werden exern verwaltet** = **Ja** können verwendet werden, um direkt den gleichen Lagerort im anderen System zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6c9df-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="6c9df-130">Es ist möglich, mehrere Lagerorte in Field Service zu erstellen (mit **wird extern verwaltet** = Nein) und diese zu einem bestimmten Lagerort mit den erweiterten Abfragen und Filterfunktionen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6c9df-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="6c9df-131">Dies wird in Fällen verwendet, in denen Sie Field Service verwenden, um die detaillierte Bestandebene zu steuern und Supply Chain Management zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6c9df-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="6c9df-132">In diesem Fall erhält Field Service keine Bestandebenenaktualisierung von Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6c9df-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="6c9df-133">Siehe zusätzliche Informationen unter Synchronisierung von Bestandanpassungen von Field Service zu [Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) und [Synchronisieren von Arbeitsaufträge in Field Service zu Arbeitsaufträgen, die mit Projekten in Finance and Operations verknüpft sind](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="6c9df-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6c9df-134">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="6c9df-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="6c9df-135">Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="6c9df-135">Data Integration project</span></span>
<span data-ttu-id="6c9df-136">Vor der Synchronisierung der Lagerorte stellen Sie sicher, die erweiterte Abfrage und Filterung im Projekt zu aktualisieren, die nur Lagerorte einbeziehen, die mithilfe von Supply Chain Management mit Field Service vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6c9df-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="6c9df-137">Beachten Sie, dass Sie den Lagerort im Field Service benötigen, um sie in Arbeitsaufträgen, Übertragungen und Regulierungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="6c9df-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="6c9df-138">Stellen Sie sicher, dass der **Integrationsschlüssel** für **msdyn_workorders** vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="6c9df-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="6c9df-139">Gehen Sie zu Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="6c9df-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="6c9df-140">Wählen Sie **Verbindungssatz** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="6c9df-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="6c9df-141">Wählen Sie das für die Synchronisation der Arbeitsaufträge verwendete Verbindungsset aus.</span><span class="sxs-lookup"><span data-stu-id="6c9df-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="6c9df-142">Wählen Sie **Integrationsschlüssel** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="6c9df-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="6c9df-143">Suchen Sie msdyn_workorders und überprüfen Sie, ob der Schlüssel **msdyn_name (Name)** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c9df-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="6c9df-144">Wenn es nicht angezeigt wird, fügen Sie es durch Klicken auf **Schlüssel hinzufügen** und klicken Sie auf **Speichern** im oberen Bereich der Seite.</span><span class="sxs-lookup"><span data-stu-id="6c9df-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6c9df-145">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="6c9df-145">Template mapping in Data integration</span></span>

<span data-ttu-id="6c9df-146">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="6c9df-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="6c9df-147">Lagerorte (Supply Chain Management zu Field Service): Lagerort</span><span class="sxs-lookup"><span data-stu-id="6c9df-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="6c9df-148">[![Vorlagenzuordnung in Datenintegration](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="6c9df-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]