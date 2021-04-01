---
title: Arbeitsauslastungskapazität planen
description: In diesem Thema wird erläutert, wie Sie die Auslastung der Mitarbeiter in einem Lager oder für ein ganzes Lager einrichten und einplanen.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4eac4838a4df8f1f5863f1ce1895e7aded5fb08b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239277"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="f3c5c-103">Arbeitsauslastungskapazität planen</span><span class="sxs-lookup"><span data-stu-id="f3c5c-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f3c5c-104">Sie können die Arbeitsauslastungskapazität für Lagerorte planen und auch die aktuelle und zukünftige Arbeitsauslastungen für die Arbeitskräfte in einzelnen Lagerorten prognostizieren.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="f3c5c-105">Sie können die Arbeitsauslastung für das gesamte Lager prognostizieren, oder Sie können die Arbeitsauslastung für ein- und ausgehende Arbeitsauslastungen separat prognostizieren.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="f3c5c-106">Um Arbeitsauslastung das Projekt für ausgewählte Lagerorte zu prognostizieren, müssen Produktprogrammplanungslaufdaten für die ausgewählten Lagerorte verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="f3c5c-107">Weitere Informationen finden Sie unter [Masterplanübersicht](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="f3c5c-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="f3c5c-108">Arbeitsauslastungen für einen Lagerort planen und anzeigen</span><span class="sxs-lookup"><span data-stu-id="f3c5c-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="f3c5c-109">Um die Arbeitsauslastungskapazität für einen Lagerort zu planen, erstellen Sie eine Arbeitsauslastungseinstellung für einen oder mehrere Lagerorte, und ordnen die Arbeitsauslastungseinstellung einem Produktprogrammplan zu.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="f3c5c-110">In der Arbeitsauslastungskapazitätseinstellung können Sie Limits für Paletten, Gewicht oder Volumen für ein- und ausgehende Transaktionen definieren.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="f3c5c-111">Sie können auch mehr als eine Einrichtung für jeden Lagerort erstellen, und dann die Einstellung einzelnen Produktprogrammplänen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="f3c5c-112">Sie können diesen Ansatz beispielsweise verwenden, um saisonale Veränderungen in der Belegschaft zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="f3c5c-113">Wenn die Arbeitskräfte für einen Lagerort mit Buchungen für ein- und ausgehende Arbeitsauslastungen arbeiten, können Sie die Lagerortkapazitätseinstellung so konfigurieren, dass die Arbeitsauslastung in einer kombinierten Ansicht geplant wird.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="f3c5c-114">Um Arbeitsauslastungen für Lagerorte zu planen und anzuzeigen, müssen Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="f3c5c-115">Erstellen Sie eine Arbeitsauslastungskapazitätseinstellung und definieren Sie Arbeitsauslastungskapazitätsgrenzen für einen oder mehrere Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="f3c5c-116">Ordnen Sie die Arbeitsauslastungskapazitätseinstellung einem Produktprogrammplan zu, um Arbeitsauslastungsprojektionen zu erstellen und anzugeben, wie lange die Prognosen gelten.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="f3c5c-117">Erstellen einer Arbeitsauslastungskapazitätseinstellung für einen Lagerort</span><span class="sxs-lookup"><span data-stu-id="f3c5c-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="f3c5c-118">Wählen Sie **Lagerverwaltung** \> **Einrichten** \> **Lagerortüberwachung** \> **Arbeitsauslastungskapazität**.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="f3c5c-119">Wählen Sie im Aktionsbereich **Neu**, um eine Konfiguration der Arbeitslastkapazität zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="f3c5c-120">Wählen Sie auf dem Inforegister **Lagerorte** die Option **Neu**, und geben Sie dann in der Zeile Werte ein, um ein Lager mit der Einstellung der Auslastung zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="f3c5c-121">Aktivieren Sie das Kontrollkästchen **Kombinierte ein- und ausgehende Arbeitsauslastung**, wenn der Bericht **Arbeitsauslastungskapazität** die Gesamtlast für eingehende und ausgehende Transaktionen in einer Ansicht anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="f3c5c-122">Wählen Sie auf dem Inforegister **Transaktionsarten** die Arten von ein- und ausgehenden Transaktionen aus, für die die Arbeitslastgrenzen gelten sollen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3c5c-123">Sie müssen sowohl für die eingehende als auch für die ausgehende Arbeitslast mindestens eine Transaktionsart auswählen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="f3c5c-124">Grenzen für Volumen oder Gewicht festlegen</span><span class="sxs-lookup"><span data-stu-id="f3c5c-124">Define limits for volume or weight</span></span>

<span data-ttu-id="f3c5c-125">Sie können Limits für Volumen oder Gewicht einrichten, je nachdem, welche Limits für die Lagerbelegschaft relevant sind.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="f3c5c-126">Die Limits, die Sie angeben, sind in der Lastprognose enthalten, die Sie im Bericht **Arbeitsauslastung** einsehen können.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="f3c5c-127">Um Informationen zu Volumen und Gewicht für Artikel zu prognostizieren, müssen Lagerartikel, Volumen eines Lagerartikels und Gewicht eines Lagerartikels für alle Produkte spezifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="f3c5c-128">Die erforderlichen Felder sind in den folgenden Feldgruppen auf dem Inforegister **Lagerbestand verwalten** der Seite **Details für freigegebene Produkte** verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="f3c5c-129">Handhabung</span><span class="sxs-lookup"><span data-stu-id="f3c5c-129">Handling</span></span>
- <span data-ttu-id="f3c5c-130">Physische Dimensionen</span><span class="sxs-lookup"><span data-stu-id="f3c5c-130">Physical dimensions</span></span>
- <span data-ttu-id="f3c5c-131">Gewichtsmessungen</span><span class="sxs-lookup"><span data-stu-id="f3c5c-131">Weight measurements</span></span>

<span data-ttu-id="f3c5c-132">Wenn diese Informationen nicht korrekt angegeben sind, erhalten Sie eine Meldung, wenn Sie den Bericht zur **Arbeitsauslastungskapazität** generieren.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="f3c5c-133">Aus dem Bericht heraus können Sie dann die fehlenden Informationen aufschlüsseln, die für die Projektion der zukünftigen Arbeitsbelastung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="f3c5c-134">Zuordnen einer Arbeitsauslastungskapazitätseinstellung zu einer Produktprogrammplanung</span><span class="sxs-lookup"><span data-stu-id="f3c5c-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="f3c5c-135">Wählen Sie **Lagerverwaltung** \> **Periodisch** \> **Arbeitslast planen**.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="f3c5c-136">Wählen Sie im Feld **Masterplan** den Masterplan aus, der für die Arbeitslastprognose verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="f3c5c-137">Geben Sie im Feld **Anzahl Tage** die Anzahl der Tage an, die die Arbeitslastprognose abdeckt.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="f3c5c-138">Wählen Sie im Feld **Arbeitslast** die Arbeitslast, die mit dem Masterplan verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="f3c5c-139">Arbeitsauslastungskapazität anzeigen</span><span class="sxs-lookup"><span data-stu-id="f3c5c-139">View workload capacity</span></span>

1. <span data-ttu-id="f3c5c-140">Wählen Sie **Lagerverwaltung** \> **Anfragen und Berichte** \> **Physische Bestandsberichte** \> **Arbeitsauslastungskapazität**.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="f3c5c-141">Geben Sie im Feld **Anzahl der Spalten** die Anzahl der Spalten an, die im Bericht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="f3c5c-142">Wählen Sie im Feld **Auftragsart** die Option **Geplant und bestätigt**, **Geplant** oder **Bestätigt**, um die Art der zu projizierenden Aufträge auf dem Bericht anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="f3c5c-143">Wählen Sie im Feld **Auslastungstyp** eine Auslastungstyp aus, um festzulegen, ob die Auslastungskapazität für Volumen oder Gewicht hochgerechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="f3c5c-144">Wählen Sie im Feld **Arbeitslastkapazität** eine Auslastungskapazitätseinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]