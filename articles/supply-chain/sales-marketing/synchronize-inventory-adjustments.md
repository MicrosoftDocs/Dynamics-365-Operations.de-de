---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Supply Chain Management synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.
author: ChristianRytt
ms.date: 04/30/2019
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
ms.openlocfilehash: 9f3bfe950446a6e87e34c32d2593cba0af84d8e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838980"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="c9618-103">Bestandsumlagerungen und Regulierungen von Field Service mit Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c9618-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c9618-104">In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9618-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="c9618-105">[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="c9618-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c9618-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c9618-106">Templates and tasks</span></span>
<span data-ttu-id="c9618-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsanpassungen und Übertragungen von Field Service zu Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c9618-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="c9618-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="c9618-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="c9618-109">Bestandsanpassung (Field Service zu Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="c9618-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="c9618-110">Bestandsübertragung (Field Service zu Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="c9618-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="c9618-111">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="c9618-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="c9618-112">Lagerbestandsregulierungen</span><span class="sxs-lookup"><span data-stu-id="c9618-112">Inventory Adjustments</span></span>
- <span data-ttu-id="c9618-113">Lagerumlagerungen</span><span class="sxs-lookup"><span data-stu-id="c9618-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="c9618-114">Tabellensatz</span><span class="sxs-lookup"><span data-stu-id="c9618-114">Table set</span></span>
| <span data-ttu-id="c9618-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c9618-115">Field Service</span></span>                     | <span data-ttu-id="c9618-116">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9618-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="c9618-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="c9618-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="c9618-118">Kopfzeilen und Positionen zur Dataverse-Bestandsanpassungserfassung</span><span class="sxs-lookup"><span data-stu-id="c9618-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="c9618-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="c9618-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="c9618-120">Kopfzeilen und Positionen zur Dataverse-Bestandsübertragungserfassung</span><span class="sxs-lookup"><span data-stu-id="c9618-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="c9618-121">Tabellenfluss</span><span class="sxs-lookup"><span data-stu-id="c9618-121">Table flow</span></span>
<span data-ttu-id="c9618-122">Bestandsanpassungen und Umbuchungen in Field Service werden mit Supply Chain Management synchronisiert, nachdem sich der **Buchungsstatus** von **Erstellt** auf **Gebucht** geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c9618-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="c9618-123">In diesem Fall wird die Anpassung oder der Transportauftrag gesperrt und wird schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c9618-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="c9618-124">Dies bedeutet, dass Korrekturen und Umbuchungen in Supply Chain Management gebucht werden können, aber nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c9618-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="c9618-125">In Supply Chain Management können Sie einen Batch-Job einrichten, um die bei der Integration erzeugten Korrekturen und Transferbestandsjournale automatisch zu buchen.</span><span class="sxs-lookup"><span data-stu-id="c9618-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="c9618-126">In den folgenden Voraussetzungen erfahren Sie, wie Sie den Batch-Job aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="c9618-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c9618-127">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="c9618-127">Field Service CRM solution</span></span> 
<span data-ttu-id="c9618-128">Die Spalte **Bestandseinheit** wurde der Tabelle **Produkt** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c9618-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="c9618-129">Diese Spalte wird benötigt, da die Verkaufs- und Bestandseinheit in Supply Chain Management nicht immer gleich ist und die Bestandseinheit für den Lagerortbestand in Supply Chain Management benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c9618-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="c9618-130">Wenn Sie das Produkt auf einem Bestandskorrekturprodukt sowohl für Bestandskorrekturen als auch für Bestandsumlagerungen einstellen, wird die Einheit aus dem Bestandsproduktwert geholt.</span><span class="sxs-lookup"><span data-stu-id="c9618-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="c9618-131">Wenn ein Wert gefunden wird, wird die Spalte **Einheit** für das Bestandskorrekturprodukt gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c9618-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="c9618-132">Die Spalte **Buchungsstatus** wurde sowohl der Tabelle **Bestandsregulierung** als auch der Tabelle **Bestandsumlagerung** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c9618-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="c9618-133">Diese Spalte wird als Filter verwendet, wenn eine Anpassung oder Übertragung an Supply Chain Management gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9618-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="c9618-134">Der Standard für diese Spalte ist „Erstellt (1)“, er wird jedoch nicht an Supply Chain Management gesendet.</span><span class="sxs-lookup"><span data-stu-id="c9618-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="c9618-135">Wenn Sie den Wert auf Gebucht (2) aktualisieren, wird er an Supply Chain Management gesendet, aber danach können Sie die Anpassung nicht mehr ändern, übertragen oder neue Zeilen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c9618-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="c9618-136">Die Spalte **Nummernkreis** wurde zur Tabelle **Bestandskorrekturprodukt** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c9618-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="c9618-137">Diese Spalte stellt sicher, dass die Integration eine eindeutige Nummer hat, damit die Integration den Abgleich erstellen und aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="c9618-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="c9618-138">Wenn Sie Ihr erstes Bestandsanpassungsprodukt erstellen, erstellt es einen neuen Datensatz in der Tabelle **P2C AutoNumber**, um die Nummernkreise und das verwendete Präfix zu pflegen.</span><span class="sxs-lookup"><span data-stu-id="c9618-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c9618-139">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="c9618-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="c9618-140">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9618-140">Supply Chain Management</span></span>
<span data-ttu-id="c9618-141">Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c9618-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="c9618-142">Diese wird aktiviert über **Bestandsverwaltung > Periodische Aufgaben > Dataverse-Integration > Bestandserfassung nach Integration**.</span><span class="sxs-lookup"><span data-stu-id="c9618-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c9618-143">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="c9618-143">Template mapping in Data integration</span></span>

<span data-ttu-id="c9618-144">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="c9618-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="c9618-145">Lagerregulierung (Field Service zu Supply Chain Management): Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="c9618-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="c9618-146">[![Vorlagenzuordnung in Datenintegration](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="c9618-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="c9618-147">Lagerumlagerung (Field Service zu Supply Chain Management): Lagerumlagerung</span><span class="sxs-lookup"><span data-stu-id="c9618-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="c9618-148">[![Vorlagenzuordnung in Datenintegration](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="c9618-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]