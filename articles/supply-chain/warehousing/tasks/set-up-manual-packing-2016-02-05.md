--- 
title: Manuelle Verpackung einrichten (nur Februar und Mai 2016)
description: "Der Verpackungsprozess ermöglicht es Ihnen, Produkte zu überprüfen und in Container zu verpacken."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 31b689b6c31563f24892525eed5911af3a35bd51
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="d8a1c-103">Manuelle Verpackung einrichten (nur Februar und Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="d8a1c-103">Set up manual packing (February & May 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8a1c-104">Der Verpackungsprozess ermöglicht es Ihnen, Produkte zu überprüfen und in Container zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="d8a1c-105">In diesem Prozess entnehmen Lagerarbeiter Produkte aus den Speicherorten und verschieben diese zu einer Verpackungsanlage, in der sie die Artikelmengen und Typen überprüfen, und weisen diese den entsprechenden Containern zu.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="d8a1c-106">Wenn ein Container vollständig gepackt ist, können sie ihn schließen und zu den Ausgangsrampen verschieben, und die Produkte sind bereit zum liefern.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="d8a1c-107">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="d8a1c-108">Lagerplatzprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="d8a1c-108">Set up location profiles</span></span>
1. <span data-ttu-id="d8a1c-109">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerort" > "Lagerplatzprofile".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="d8a1c-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-110">Click New.</span></span>
    * <span data-ttu-id="d8a1c-111">Das Lagerplatzprofil wird für Verpackungsanlagen verwendet und enthält Informationen und Regeln für einen Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="d8a1c-112">Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="d8a1c-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d8a1c-114">Geben Sie im Feld "Lagerplatzformat" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="d8a1c-115">Geben Sie im Feld "Lagerplatztyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="d8a1c-116">Wählen Sie "Ja" im Feld "Gemischte Artikel zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d8a1c-117">Wählen Sie "Ja" im Feld "Gemischte Bestandstatus zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d8a1c-118">Wählen Sie "Ja" im Feld "Überschreibungsregeln für Chargentage" aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="d8a1c-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="d8a1c-120">Richten Sie Parameter für Lagerortverwaltung ein</span><span class="sxs-lookup"><span data-stu-id="d8a1c-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="d8a1c-121">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="d8a1c-122">Klicken Sie auf die Registerkarte "Verpackung".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="d8a1c-123">Geben Sie im Feld "Profilkennung für Verpackungslagerplatz" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="d8a1c-124">Wählen Sie das Lagerplatzprofil aus, das Sie für das Packen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="d8a1c-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="d8a1c-126">Richten Sie Containertypen ein</span><span class="sxs-lookup"><span data-stu-id="d8a1c-126">Set up container types</span></span>
1. <span data-ttu-id="d8a1c-127">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containertypen".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="d8a1c-128">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-128">Click New.</span></span>
    * <span data-ttu-id="d8a1c-129">Sie können die Containertypen, die verwendet werden sollen, definieren.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-129">You can define the types of containers to use.</span></span> <span data-ttu-id="d8a1c-130">Sie können die physischen Dimensionen des Containers angeben, einschließlich Verpackungsgewicht, Höchstgewicht, maximales Volumen, Länge, Breite und Gewicht.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="d8a1c-131">Die Attribute sind angepasste Felder, die es Ihnen ermöglichen, zusätzliche Dimensionen zum Containertyp hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="d8a1c-132">Geben Sie im Feld "Containertypcode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="d8a1c-133">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8a1c-134">Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="d8a1c-135">Geben Sie im Feld "Höchstgewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="d8a1c-136">Geben Sie im Feld "Volumen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="d8a1c-137">Geben Sie im Feld Länge eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="d8a1c-138">Geben Sie im Feld "Breite" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="d8a1c-139">Geben Sie im Feld "Höhe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="d8a1c-140">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-140">Click Save.</span></span>
12. <span data-ttu-id="d8a1c-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="d8a1c-142">Richten Sie Verpackungsprofile ein</span><span class="sxs-lookup"><span data-stu-id="d8a1c-142">Set up packing profiles</span></span>
1. <span data-ttu-id="d8a1c-143">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Verpackung" > "Verpackungsprofile".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="d8a1c-144">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-144">Click New.</span></span>
3. <span data-ttu-id="d8a1c-145">Geben Sie im Feld "Verpackungsprofilkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d8a1c-146">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8a1c-147">Geben Sie im Feld "Containerabschlussprofil-Kennung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d8a1c-148">Eine Containerabschlussprofil-Kennung ist optional und ist das standardmäßige Profil zum Abschließen von Containern für dieses Verpackungsprofil.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="d8a1c-149">Wählen Sie im Feld "Containerkennungsmodus" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="d8a1c-150">Diese Option bestimmt, ob eine Containerkennung automatisch generiert wird, wenn ein Container erstellt wird, oder eine Containerkennung wird manuell erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="d8a1c-151">Geben Sie im Feld "Containertyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="d8a1c-152">Der Containertyp wird standardmäßig verwendet, wenn ein neuer Container erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="d8a1c-153">Aktivieren Sie das Kontrollkästchen "Container beim Schließen des Containers automatisch erstellen".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="d8a1c-154">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-154">Click Save.</span></span>
10. <span data-ttu-id="d8a1c-155">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="d8a1c-156">Richten Sie Containerabschlussprofile ein</span><span class="sxs-lookup"><span data-stu-id="d8a1c-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="d8a1c-157">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containerabschlussprofile".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="d8a1c-158">Containerabschlussprofile definieren, was passiert, wenn ein Container geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="d8a1c-159">Sie können mehrere Profile zum Abschließen von Containern einrichten.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="d8a1c-160">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-160">Click New.</span></span>
3. <span data-ttu-id="d8a1c-161">Geben Sie im Feld "Containerabschlussprofil-Kennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d8a1c-162">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8a1c-163">Wählen Sie im Feld "Manifestieren" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="d8a1c-164">Geben Sie an, ob Manifestierung geschieht, wenn Sie Container schließen oder wenn Sie die Lieferung bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="d8a1c-165">Beachten Sie, dass eine Manifestierung "Transportverwaltung" benötigt.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="d8a1c-166">Manifestierung muss in den Transportmodulen implementiert werden, damit sie funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="d8a1c-167">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="d8a1c-168">Geben Sie im Feld "Standardlagerplatz für letzte Lieferung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="d8a1c-169">Dies ist der Lagerplatz, zu dem Produkte verschoben werden, nachdem die Container geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="d8a1c-170">Dieser Lagerplatz muss ein Lagerplatzprofil haben, das auf Lagerortparametern definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="d8a1c-171">Geben Sie im Feld "Gewichtseinheit" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d8a1c-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="d8a1c-172">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d8a1c-172">Click Save.</span></span>


