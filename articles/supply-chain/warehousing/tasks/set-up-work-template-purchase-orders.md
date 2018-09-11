--- 
title: "Arbeitsvorlage für Bestellungen einrichten"
description: Ziel dieser Prozedur ist es, eine einfache Arbeitsvorlage einzurichten, die verwendet wird, wenn empfangene Artikel eingelagert werden sollen.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4c388a8ed6a852a92caa3a1eff2d0e8017694bcd
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="a04d4-103">Arbeitsvorlage für Bestellungen einrichten</span><span class="sxs-lookup"><span data-stu-id="a04d4-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a04d4-104">Ziel dieser Prozedur ist es, eine einfache Arbeitsvorlage einzurichten, die verwendet wird, wenn empfangene Artikel eingelagert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a04d4-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="a04d4-105">Arbeitsvorlagen bestimmen die Sammlung von Anweisungen, die dem Lagerarbeiter auf einem mobilen Gerät dargestellt wird, wenn Artikel aus dem Wareneingangsbereich umgelagert werden.</span><span class="sxs-lookup"><span data-stu-id="a04d4-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="a04d4-106">Sie können diese Prozedur mit dem Daten des Demodatenunternehmen USMF oder mit eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a04d4-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="a04d4-107">Bevor Sie dieses Handbuch starten, erstellen Sie eine Arbeitspool-ID.</span><span class="sxs-lookup"><span data-stu-id="a04d4-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="a04d4-108">In diesem Beispiel wird eine Arbeitspool-ID mit der Bezeichnung "Eingehend" verwendet.</span><span class="sxs-lookup"><span data-stu-id="a04d4-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="a04d4-109">Diese Prozedur ist für die Lagerverwaltung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a04d4-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="a04d4-110">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".</span><span class="sxs-lookup"><span data-stu-id="a04d4-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="a04d4-111">Wählen Sie im Feld "Standardauftragstyp" die Option "Bestellung" aus.</span><span class="sxs-lookup"><span data-stu-id="a04d4-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="a04d4-112">Kopfzeile der Arbeitsvorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="a04d4-112">Create a work template header</span></span>
1. <span data-ttu-id="a04d4-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a04d4-113">Click New.</span></span>
2. <span data-ttu-id="a04d4-114">Geben Sie im Feld "Laufende Nummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="a04d4-115">Dies ist die Sequenz, in der die Arbeitsvorlagen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="a04d4-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="a04d4-116">Sie können die Reihenfolge bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="a04d4-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="a04d4-117">Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="a04d4-118">Dies ist eindeutige Bezeichner für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="a04d4-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="a04d4-119">Geben Sie im Feld "Arbeitsvorlagenbeschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="a04d4-120">Die Option "Gültig" wird nicht aktiviert, bis Sie alle Informationen, die für die Vorlage erforderlich sind, angegeben und gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="a04d4-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="a04d4-121">Ein Arbeitsauftrag vom Typ "Bestellung" kann nicht automatisch verarbeitet werden, daher legen Sie die Option "Automatisch verarbeiten" auf "Nein" fest.</span><span class="sxs-lookup"><span data-stu-id="a04d4-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="a04d4-122">Geben Sie im Feld "Arbeitspool-ID" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="a04d4-123">Mithilfe der Arbeitspool-IDs können Sie die Arbeit in Gruppen organisieren.</span><span class="sxs-lookup"><span data-stu-id="a04d4-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="a04d4-124">Der Wert, der hier festgelegt ist, ist der Standardwert für jede Arbeit, die anhand dieser Vorlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a04d4-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="a04d4-125">Geben Sie im Feld "Arbeitspriorität" 1 ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="a04d4-126">Dadurch wird die Wichtigkeit der Arbeit angegeben. Der hier festgelegte Wert wird als Standard für jede Arbeit festgelegt, die anhand dieser Vorlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a04d4-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="a04d4-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a04d4-127">Click Save.</span></span>
    * <span data-ttu-id="a04d4-128">Sie müssen die Kopfzeile der Arbeitsvorlagen speichern, damit die Schaltfläche "Abfrage bearbeiten" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a04d4-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="a04d4-129">Abfrage für Arbeitsvorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="a04d4-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="a04d4-130">(Zum Bearbeiten klicken)</span><span class="sxs-lookup"><span data-stu-id="a04d4-130">Click Edit query.</span></span>
    * <span data-ttu-id="a04d4-131">Wir legen eine Einschränkung fest, damit die Vorlage nur innerhalb eines bestimmten Lagerorts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a04d4-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="a04d4-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a04d4-132">Click Add.</span></span>
3. <span data-ttu-id="a04d4-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a04d4-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a04d4-134">Geben Sie im Feld "Lagerort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="a04d4-135">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="a04d4-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a04d4-136">Click OK.</span></span>
7. <span data-ttu-id="a04d4-137">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a04d4-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="a04d4-138">Arbeitsvorlagendetails einrichten</span><span class="sxs-lookup"><span data-stu-id="a04d4-138">Set work template details</span></span>
1. <span data-ttu-id="a04d4-139">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a04d4-139">Click New.</span></span>
2. <span data-ttu-id="a04d4-140">Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.</span><span class="sxs-lookup"><span data-stu-id="a04d4-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="a04d4-141">Geben Sie im Feld "Arbeitsklassen-ID" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="a04d4-142">Die hier festgelegte Arbeitsklasse ist der Standard für alle Arbeitspositionen vom Typ "Entnahme", die anhand dieser Vorlage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a04d4-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="a04d4-143">Die Arbeitsklasse kann nicht von den Arbeitsauftragspositionen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a04d4-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="a04d4-144">Arbeitsklassen werden verwendet, um den Typ der Arbeitsauftragspositionen zuzuweisen und/oder einzuschränken, die ein Lagerarbeiter auf einem mobilen Gerät verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="a04d4-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="a04d4-145">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a04d4-145">Click New.</span></span>
5. <span data-ttu-id="a04d4-146">Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.</span><span class="sxs-lookup"><span data-stu-id="a04d4-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="a04d4-147">Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a04d4-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="a04d4-148">Die Entnahme- und Einlagerungsanweisungen sind ein Satz.</span><span class="sxs-lookup"><span data-stu-id="a04d4-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="a04d4-149">Jede Entnahme/Einlagerung muss dieselbe Arbeitsklasse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a04d4-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="a04d4-150">Verwenden Sie die gleiche Arbeitsklasse, die Sie für die Entnahmeanweisung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a04d4-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="a04d4-151">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a04d4-151">Click Save.</span></span>
    * <span data-ttu-id="a04d4-152">Beachten Sie, dass das Kontrollkästchen "Gültig" nun aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a04d4-152">Note that the Valid checkbox is now checked.</span></span>  


