---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="d1e06-103">Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="d1e06-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d1e06-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d1e06-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d1e06-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="d1e06-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d1e06-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="d1e06-106">Templates and tasks</span></span>
<span data-ttu-id="d1e06-107">Die folgende Vorlage und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Field Service mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d1e06-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d1e06-108">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="d1e06-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="d1e06-109">Bestandanpassung (Field Service zu Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d1e06-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="d1e06-110">Bestandübertragung (Field Service zu Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d1e06-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="d1e06-111">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="d1e06-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="d1e06-112">Lagerbestandsregulierungen</span><span class="sxs-lookup"><span data-stu-id="d1e06-112">Inventory Adjustments</span></span>
- <span data-ttu-id="d1e06-113">Lagerumlagerungen</span><span class="sxs-lookup"><span data-stu-id="d1e06-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="d1e06-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="d1e06-114">Entity set</span></span>
| <span data-ttu-id="d1e06-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="d1e06-115">Field Service</span></span>                     | <span data-ttu-id="d1e06-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1e06-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="d1e06-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="d1e06-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="d1e06-118">Kopfzeilen und Positionen zur CDS-Bestandsanpassungserfassung</span><span class="sxs-lookup"><span data-stu-id="d1e06-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="d1e06-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="d1e06-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="d1e06-120">Kopfzeilen und Positionen zur CDS-Bestandsübertragungserfassung</span><span class="sxs-lookup"><span data-stu-id="d1e06-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="d1e06-121">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="d1e06-121">Entity flow</span></span>
<span data-ttu-id="d1e06-122">Die Lagerregulierungen und Übertragungen, die im Field Service vorgenommen werden, Synchronisieren mit Finance and Operations, wenn der **Beitragsstatus** von erstellt auf buchen geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d1e06-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="d1e06-123">Wenn dies eroflt, wird die Regulierung oder der Umlagerungsauftrag gesperrt und wird schreibgeschützt, da  Regulierungen und Überträge in Finance and Operations gebucht werden können und deshalb nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d1e06-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="d1e06-124">In Finance and Operations können Sie eine Stapelverarbeitung einrichten, die die Übergangslagererfassungen automatisch bucht, die bei der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1e06-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="d1e06-125">Voraussetzung finden Sie unten, wie der Stapelverarbeitungsauftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1e06-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d1e06-126">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="d1e06-126">Field Service CRM solution</span></span> 
<span data-ttu-id="d1e06-127">Das Feld Lagereinheit wurde der Produktentität hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d1e06-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="d1e06-128">Dieses Feld ist erforderlich, da Sales und Bestandeinheit nicht unbedingt gleich ist in Operations und für den Lagerort-Bestand in Operations benötigne wir die Lagereinheit.</span><span class="sxs-lookup"><span data-stu-id="d1e06-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="d1e06-129">Wenn Sie das Produkt in einem Lagerregulierungs-Produkt für beide Lagerregulierungen und Umlagerungen festsetzen, ruft die Einheit aus dem Produkt-Bestand den Produktwert ab.</span><span class="sxs-lookup"><span data-stu-id="d1e06-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="d1e06-130">Wenn ein Wert vorhanden ist, wird das Einheitsfeld im Feld Lagerregulierungs-Produkt gesperrt</span><span class="sxs-lookup"><span data-stu-id="d1e06-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="d1e06-131">Das Beitrags-Statusfeld wurde der Lagerregulierungsentität und der Umlagerungsentität hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d1e06-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="d1e06-132">Dieses Feld dient als Filter und wird verwendet, wenn eine Niedrigerbewertung oder eine Übertragung mit Vorgängen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e06-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="d1e06-133">Das Feld wird als Standard auf erstellt (1) festgelegt und wird dann nicht von Operations übernommen.</span><span class="sxs-lookup"><span data-stu-id="d1e06-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="d1e06-134">Wenn Sie eine Änderung machen, wird diese auf gebucht (2) an Operations gesendet, aber Sie können dann nichts mehr in der Regulierung anpassen oder Übertragen oder neue Zeilen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d1e06-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="d1e06-135">Das Nummernsequenzfeld wurde der Bestand-Produktentität hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d1e06-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="d1e06-136">Dieses Feld ermöglicht der Integration, eine eindeutige Nummer zuzuweisen, damit die Integration weiss, wann sie erstellen und wann aktualisieren muss.</span><span class="sxs-lookup"><span data-stu-id="d1e06-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="d1e06-137">Wenn Sie das Lagerregulierungs-Produkt zuerst erstellen, erstellt sie ein neuer Datensatz in der P2C-AutoWertentität, um den Präfix Nummernkreis und den verwendeten Präfix zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d1e06-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d1e06-138">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="d1e06-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="d1e06-139">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1e06-139">In Finance and Operations</span></span>
<span data-ttu-id="d1e06-140">Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="d1e06-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="d1e06-141">Diese wird aktiviert von: Lagerverwaltung > periodische Aufgaben > CD-Integration > Beitragsintegrationslagererfassungen</span><span class="sxs-lookup"><span data-stu-id="d1e06-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d1e06-142">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="d1e06-142">Template mapping in Data integration</span></span>

<span data-ttu-id="d1e06-143">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="d1e06-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="d1e06-144">Bestandanpassung (Field Service zu Finance and Operations): Bestandregulierung</span><span class="sxs-lookup"><span data-stu-id="d1e06-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="d1e06-145">[![Vorlagenzuordnung in Datenintegration](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="d1e06-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="d1e06-146">Bestandandübertragung (Field Service zu Finance and Operations): Bestandübertragung</span><span class="sxs-lookup"><span data-stu-id="d1e06-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="d1e06-147">[![Vorlagenzuordnung in Datenintegration](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="d1e06-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

