---
title: Serviceobjektbeziehungen
description: "Zwischen einem Serviceobjekt und einer Servicevereinbarung oder einem Serviceauftrag können Serviceobjektbeziehungen erstellt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 90c16653dee0614beaad8e4693c012b67a54b297
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="2e002-103">Serviceobjektbeziehungen</span><span class="sxs-lookup"><span data-stu-id="2e002-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e002-104">Zwischen einem Serviceobjekt und einer Servicevereinbarung oder einem Serviceauftrag können Serviceobjektbeziehungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2e002-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="2e002-105">Durch Erstellen einer Beziehung wird das Serviceobjekt der Servicevereinbarung oder dem Serviceauftrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2e002-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="2e002-106">Nach Erstellung der Beziehung kann das Serviceobjekt den Positionen einer Servicevereinbarung oder eines Serviceauftrags zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2e002-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="2e002-107">Vorlagenstücklisten</span><span class="sxs-lookup"><span data-stu-id="2e002-107">Template BOMs</span></span>

<span data-ttu-id="2e002-108">Für die Objektbeziehung kann auch eine Vorlagenstückliste angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e002-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="2e002-109">Bei der Vorlagenstückliste handelt es sich um eine Stückliste für das Objekt, für die Leistung erbracht wird.</span><span class="sxs-lookup"><span data-stu-id="2e002-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="2e002-110">Wird während eines Servicebesuchs eine Komponente des Serviceobjekts ausgetauscht, können Sie diese Änderung mithilfe des Formulars Serviceobjekte in der Servicestückliste erfassen.</span><span class="sxs-lookup"><span data-stu-id="2e002-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="2e002-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e002-111">Example</span></span>

<span data-ttu-id="2e002-112">Sie erstellen eine Servicevereinbarung für die Wartung zweier Aufzüge am Standort des Debitors.</span><span class="sxs-lookup"><span data-stu-id="2e002-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="2e002-113">Die Servicevereinbarung hat den Bezeichner "ID SAL-001".</span><span class="sxs-lookup"><span data-stu-id="2e002-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="2e002-114">Die Aufzüge wurden im Formular Serviceobjekte als Objekte mit der Bezeichnung "EL-S/1000" und "EL-L/1000" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="2e002-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="2e002-115">Die Serviceobjekte ("EL-S/1000" und "EL-L/1000") werden der Servicevereinbarung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2e002-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="2e002-116">Da Änderungen, die sich durch den Austausch von Komponenten des Serviceobjekts ergeben, in der Stückliste für das Serviceobjekt erfasst werden sollen, ordnen Sie der Serviceobjektbeziehung eine Servicestückliste zu. Weitere Informationen hierzu finden Sie in der folgenden Tabelle:</span><span class="sxs-lookup"><span data-stu-id="2e002-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="2e002-117">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="2e002-117">Service object</span></span> | <span data-ttu-id="2e002-118">Beziehung – Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="2e002-118">Relation – Service agreement</span></span> | <span data-ttu-id="2e002-119">Servicestückliste</span><span class="sxs-lookup"><span data-stu-id="2e002-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="2e002-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-120">EL-S/1000</span></span>      | <span data-ttu-id="2e002-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="2e002-121">ID SAL-001</span></span>                   | <span data-ttu-id="2e002-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="2e002-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-123">EL-L/1000</span></span>      | <span data-ttu-id="2e002-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="2e002-124">ID SAL-001</span></span>                   | <span data-ttu-id="2e002-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="2e002-126">Da für die Vereinbarung Serviceobjektbeziehungen vorhanden sind, lassen sich nun Vereinbarungspositionen mit diesen Objekten erstellen. Weitere Informationen hierzu finden Sie in der folgenden Tabelle:</span><span class="sxs-lookup"><span data-stu-id="2e002-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="2e002-127">Buchungstyp</span><span class="sxs-lookup"><span data-stu-id="2e002-127">Transaction type</span></span> | <span data-ttu-id="2e002-128">Kategorie</span><span class="sxs-lookup"><span data-stu-id="2e002-128">Category</span></span>           | <span data-ttu-id="2e002-129">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="2e002-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="2e002-130">Stunde</span><span class="sxs-lookup"><span data-stu-id="2e002-130">Hour</span></span>             | <span data-ttu-id="2e002-131">Prüfung</span><span class="sxs-lookup"><span data-stu-id="2e002-131">Inspection</span></span>         | <span data-ttu-id="2e002-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-132">EL-S/1000</span></span>      |
| <span data-ttu-id="2e002-133">Stunde</span><span class="sxs-lookup"><span data-stu-id="2e002-133">Hour</span></span>             | <span data-ttu-id="2e002-134">Reinigung des Getriebes</span><span class="sxs-lookup"><span data-stu-id="2e002-134">Gear box cleaning</span></span>  | <span data-ttu-id="2e002-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-135">EL-S/1000</span></span>      |
| <span data-ttu-id="2e002-136">Artikel</span><span class="sxs-lookup"><span data-stu-id="2e002-136">Item</span></span>             | <span data-ttu-id="2e002-137">Reinigungsmaterial</span><span class="sxs-lookup"><span data-stu-id="2e002-137">Cleaning materials</span></span> | <span data-ttu-id="2e002-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-138">EL-S/1000</span></span>      |
| <span data-ttu-id="2e002-139">Stunde</span><span class="sxs-lookup"><span data-stu-id="2e002-139">Hour</span></span>             | <span data-ttu-id="2e002-140">Prüfung</span><span class="sxs-lookup"><span data-stu-id="2e002-140">Inspection</span></span>         | <span data-ttu-id="2e002-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-141">EL-L/1000</span></span>      |
| <span data-ttu-id="2e002-142">Stunde</span><span class="sxs-lookup"><span data-stu-id="2e002-142">Hour</span></span>             | <span data-ttu-id="2e002-143">Reinigung des Getriebes</span><span class="sxs-lookup"><span data-stu-id="2e002-143">Gearbox cleaning</span></span>   | <span data-ttu-id="2e002-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-144">EL-L/1000</span></span>      |
| <span data-ttu-id="2e002-145">Artikel</span><span class="sxs-lookup"><span data-stu-id="2e002-145">Item</span></span>             | <span data-ttu-id="2e002-146">Reinigungsmaterial</span><span class="sxs-lookup"><span data-stu-id="2e002-146">Cleaning materials</span></span> | <span data-ttu-id="2e002-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="2e002-147">EL-L/1000</span></span>      |

<span data-ttu-id="2e002-148">Bei einem Servicebesuch muss beim Aufzug "EL-S/1000" ein Austausch des Getriebes vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="2e002-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="2e002-149">Rufen Sie mithilfe der für die aktuelle Servicevereinbarung eingerichteten Serviceobjektbeziehung den Stücklisten-Designer auf, um eine Komponente des Objekts auszutauschen.</span><span class="sxs-lookup"><span data-stu-id="2e002-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="2e002-150">Aufrufen des Stücklisten-Designers mithilfe einer Serviceobjektbeziehung</span><span class="sxs-lookup"><span data-stu-id="2e002-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="2e002-151">Serviceverträge</span><span class="sxs-lookup"><span data-stu-id="2e002-151">Service agreements</span></span>
2. <span data-ttu-id="2e002-152">Doppelklicken Sie auf einen Servicevertrag, oder klicken Sie auf , um einen neuen Servicevertrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e002-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="2e002-153">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="2e002-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="2e002-154">Klicken Sie auf Serviceobjekte und anschließend auf Stückliste, um der Servicevereinbarung eine Vorlagenstückliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2e002-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="2e002-155">Klicken Sie zum Öffnen des Formulars Serviceobjekte im Formular Designer auf Designe und aktualisieren Sie die Vorlagenstückliste.</span><span class="sxs-lookup"><span data-stu-id="2e002-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="2e002-156">Automatisch erstellte Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="2e002-156">Automatically created service orders</span></span>

<span data-ttu-id="2e002-157">Werden Serviceaufträge für eine Servicevereinbarung automatisch erstellt, werden die Serviceobjektbeziehungen aus der Vereinbarung auch in den Serviceaufträgen erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e002-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


