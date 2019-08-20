---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835717"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="b4e62-103">Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b4e62-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b4e62-104">In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e62-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b4e62-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="b4e62-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b4e62-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b4e62-106">Templates and tasks</span></span>
<span data-ttu-id="b4e62-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsanpassungen und Übertragungen von Microsoft Dynamics 365 for Field Service auf Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b4e62-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b4e62-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="b4e62-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="b4e62-109">Bestandregulierung (Field Service zu Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b4e62-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="b4e62-110">Bestandübertragung (Field Service zu Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b4e62-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="b4e62-111">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="b4e62-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="b4e62-112">Lagerbestandsregulierungen</span><span class="sxs-lookup"><span data-stu-id="b4e62-112">Inventory Adjustments</span></span>
- <span data-ttu-id="b4e62-113">Lagerumlagerungen</span><span class="sxs-lookup"><span data-stu-id="b4e62-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="b4e62-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="b4e62-114">Entity set</span></span>
| <span data-ttu-id="b4e62-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="b4e62-115">Field Service</span></span>                     | <span data-ttu-id="b4e62-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b4e62-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="b4e62-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="b4e62-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="b4e62-118">Kopfzeilen und Positionen zur CDS-Bestandsanpassungserfassung</span><span class="sxs-lookup"><span data-stu-id="b4e62-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="b4e62-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="b4e62-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="b4e62-120">Kopfzeilen und Positionen zur CDS-Bestandsübertragungserfassung</span><span class="sxs-lookup"><span data-stu-id="b4e62-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="b4e62-121">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="b4e62-121">Entity flow</span></span>
<span data-ttu-id="b4e62-122">Bestandsanpassungen und Umbuchungen in Field Service werden mit Finance and Operations synchronisiert, nachdem sich der **Buchungsstatus** von **Erstellt** auf **Gebucht** geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b4e62-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="b4e62-123">In diesem Fall wird die Anpassung oder der Transportauftrag gesperrt und wird schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b4e62-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="b4e62-124">Dies bedeutet, dass Korrekturen und Umbuchungen in Finance and Operations gebucht werden können, aber nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b4e62-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="b4e62-125">In Finance and Operations können Sie einen Batch-Job einrichten, um die bei der Integration erzeugten Korrekturen und Transferbestandsjournale automatisch zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b4e62-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="b4e62-126">In den folgenden Voraussetzungen erfahren Sie, wie Sie den Batch-Job aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="b4e62-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b4e62-127">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="b4e62-127">Field Service CRM solution</span></span> 
<span data-ttu-id="b4e62-128">Das Feld **Bestandseinheit** wurde der **Produktentität** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b4e62-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="b4e62-129">Dieses Feld wird benötigt, da die Verkaufs- und Lagereinheit in Finance and Operations nicht immer gleich ist und die Lagereinheit für den Lagerbestand in Finance and Operations benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b4e62-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="b4e62-130">Wenn Sie das Produkt auf einem Bestandskorrekturprodukt sowohl für Bestandskorrekturen als auch für Bestandsumlagerungen einstellen, wird die Einheit aus dem Bestandsproduktwert geholt.</span><span class="sxs-lookup"><span data-stu-id="b4e62-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="b4e62-131">Wenn ein Wert gefunden wird, wird das Feld **Einheit** für das Bestandskorrekturprodukt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b4e62-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="b4e62-132">Das Feld **Buchungsstatus** wurde sowohl bei der **Bestandskorrektureinheit** als auch bei der **Bestandsumlagerungseinheit** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b4e62-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="b4e62-133">Dieses Feld wird als Filter verwendet, wenn eine Anpassung oder Übertragung an Finance and Operations gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4e62-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="b4e62-134">Der Standard für dieses Feld ist Erstellt (1), es wird jedoch nicht an Finance and Operations gesendet.</span><span class="sxs-lookup"><span data-stu-id="b4e62-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="b4e62-135">Wenn Sie den Wert auf Gebucht (2) aktualisieren, wird er an Finance and Operations gesendet, aber danach können Sie die Anpassung nicht mehr ändern, übertragen oder neue Zeilen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b4e62-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="b4e62-136">Die Entität **Bestandskorrekturprodukt** wurde um das Feld **Nummernfolge** erweitert.</span><span class="sxs-lookup"><span data-stu-id="b4e62-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="b4e62-137">Dieses Feld stellt sicher, dass die Integration eine eindeutige Nummer hat, damit die Integration den Abgleich erstellen und aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="b4e62-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="b4e62-138">Wenn Sie Ihr erstes Bestandsanpassungsprodukt erstellen, erstellt es einen neuen Datensatz in der Entität **P2C AutoNumber**, um die Nummernkreise und das verwendete Präfix zu pflegen.</span><span class="sxs-lookup"><span data-stu-id="b4e62-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b4e62-139">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="b4e62-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="b4e62-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b4e62-140">Finance and Operations</span></span>
<span data-ttu-id="b4e62-141">Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="b4e62-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="b4e62-142">Diese wird aktiviert von: **Lagerverwaltung > periodische Aufgaben > CD-Integration > Beitragsintegrationslagererfassungen**</span><span class="sxs-lookup"><span data-stu-id="b4e62-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b4e62-143">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="b4e62-143">Template mapping in Data integration</span></span>

<span data-ttu-id="b4e62-144">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="b4e62-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="b4e62-145">Bestandregulierung (Field Service zu Finance and Operations): Bestandregulierung</span><span class="sxs-lookup"><span data-stu-id="b4e62-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="b4e62-146">[![Vorlagenzuordnung in Datenintegration](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="b4e62-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="b4e62-147">Bestandandübertragung (Field Service zu Finance and Operations): Bestandübertragung</span><span class="sxs-lookup"><span data-stu-id="b4e62-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="b4e62-148">[![Vorlagenzuordnung in Datenintegration](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="b4e62-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
