---
title: Manuelle Verpackung einrichten (Februar 2016 und Mai 2016)
description: Der Verpackungsprozess ermöglicht es Ihnen, Produkte zu überprüfen und in Container zu verpacken.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec4d86673555f594bb2f81010235fd7eb6e83f27
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148284"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="26e35-103">Manuelle Verpackung einrichten (Februar 2016 und Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="26e35-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26e35-104">Der Verpackungsprozess ermöglicht es Ihnen, Produkte zu überprüfen und in Container zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="26e35-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="26e35-105">In diesem Prozess entnehmen Lagerarbeiter Produkte aus den Speicherorten und verschieben diese zu einer Verpackungsanlage, in der sie die Artikelmengen und Typen überprüfen, und weisen diese den entsprechenden Containern zu.</span><span class="sxs-lookup"><span data-stu-id="26e35-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="26e35-106">Wenn ein Container vollständig gepackt ist, können sie ihn schließen und zu den Ausgangsrampen verschieben, und die Produkte sind bereit zum liefern.</span><span class="sxs-lookup"><span data-stu-id="26e35-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="26e35-107">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="26e35-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="26e35-108">Diese Prozedur ist nur für die Dynamics 365 for Operations-Versionen Februar 2016 und Mai 2016 gedacht.</span><span class="sxs-lookup"><span data-stu-id="26e35-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="26e35-109">Lagerplatzprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="26e35-109">Set up location profiles</span></span>
1. <span data-ttu-id="26e35-110">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerort" > "Lagerplatzprofile".</span><span class="sxs-lookup"><span data-stu-id="26e35-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="26e35-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="26e35-111">Click New.</span></span>
    * <span data-ttu-id="26e35-112">Das Lagerplatzprofil wird für Verpackungsanlagen verwendet und enthält Informationen und Regeln für einen Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="26e35-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="26e35-113">Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="26e35-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="26e35-115">Geben Sie im Feld "Lagerplatzformat" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="26e35-116">Geben Sie im Feld "Lagerplatztyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="26e35-117">Wählen Sie "Ja" im Feld "Gemischte Artikel zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="26e35-118">Wählen Sie "Ja" im Feld "Gemischte Bestandstatus zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="26e35-119">Wählen Sie "Ja" im Feld "Überschreibungsregeln für Chargentage" aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="26e35-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="26e35-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="26e35-121">Richten Sie Parameter für Lagerortverwaltung ein</span><span class="sxs-lookup"><span data-stu-id="26e35-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="26e35-122">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".</span><span class="sxs-lookup"><span data-stu-id="26e35-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="26e35-123">Klicken Sie auf die Registerkarte "Verpackung".</span><span class="sxs-lookup"><span data-stu-id="26e35-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="26e35-124">Geben Sie im Feld "Profilkennung für Verpackungslagerplatz" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="26e35-125">Wählen Sie das Lagerplatzprofil aus, das Sie für das Packen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="26e35-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="26e35-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="26e35-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="26e35-127">Richten Sie Containertypen ein</span><span class="sxs-lookup"><span data-stu-id="26e35-127">Set up container types</span></span>
1. <span data-ttu-id="26e35-128">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containertypen".</span><span class="sxs-lookup"><span data-stu-id="26e35-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="26e35-129">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="26e35-129">Click New.</span></span>
    * <span data-ttu-id="26e35-130">Sie können die Containertypen, die verwendet werden sollen, definieren.</span><span class="sxs-lookup"><span data-stu-id="26e35-130">You can define the types of containers to use.</span></span> <span data-ttu-id="26e35-131">Sie können die physischen Dimensionen des Containers angeben, einschließlich Verpackungsgewicht, Höchstgewicht, maximales Volumen, Länge, Breite und Gewicht.</span><span class="sxs-lookup"><span data-stu-id="26e35-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="26e35-132">Die Attribute sind angepasste Felder, die es Ihnen ermöglichen, zusätzliche Dimensionen zum Containertyp hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="26e35-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="26e35-133">Geben Sie im Feld "Containertypcode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="26e35-134">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="26e35-135">Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="26e35-136">Geben Sie im Feld "Höchstgewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="26e35-137">Geben Sie im Feld "Volumen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="26e35-138">Geben Sie im Feld Länge eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="26e35-139">Geben Sie im Feld "Breite" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="26e35-140">Geben Sie im Feld "Höhe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="26e35-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="26e35-141">Click Save.</span></span>
12. <span data-ttu-id="26e35-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="26e35-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="26e35-143">Richten Sie Verpackungsprofile ein</span><span class="sxs-lookup"><span data-stu-id="26e35-143">Set up packing profiles</span></span>
1. <span data-ttu-id="26e35-144">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Verpackung" > "Verpackungsprofile".</span><span class="sxs-lookup"><span data-stu-id="26e35-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="26e35-145">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="26e35-145">Click New.</span></span>
3. <span data-ttu-id="26e35-146">Geben Sie im Feld "Verpackungsprofilkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="26e35-147">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="26e35-148">Geben Sie im Feld "Containerabschlussprofil-Kennung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="26e35-149">Eine Containerabschlussprofil-Kennung ist optional und ist das standardmäßige Profil zum Abschließen von Containern für dieses Verpackungsprofil.</span><span class="sxs-lookup"><span data-stu-id="26e35-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="26e35-150">Wählen Sie im Feld "Containerkennungsmodus" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="26e35-151">Diese Option bestimmt, ob eine Containerkennung automatisch generiert wird, wenn ein Container erstellt wird, oder eine Containerkennung wird manuell erstellt.</span><span class="sxs-lookup"><span data-stu-id="26e35-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="26e35-152">Geben Sie im Feld "Containertyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="26e35-153">Der Containertyp wird standardmäßig verwendet, wenn ein neuer Container erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="26e35-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="26e35-154">Aktivieren Sie das Kontrollkästchen "Container beim Schließen des Containers automatisch erstellen".</span><span class="sxs-lookup"><span data-stu-id="26e35-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="26e35-155">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="26e35-155">Click Save.</span></span>
10. <span data-ttu-id="26e35-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="26e35-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="26e35-157">Richten Sie Containerabschlussprofile ein</span><span class="sxs-lookup"><span data-stu-id="26e35-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="26e35-158">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containerabschlussprofile".</span><span class="sxs-lookup"><span data-stu-id="26e35-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="26e35-159">Containerabschlussprofile definieren, was passiert, wenn ein Container geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="26e35-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="26e35-160">Sie können mehrere Profile zum Abschließen von Containern einrichten.</span><span class="sxs-lookup"><span data-stu-id="26e35-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="26e35-161">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="26e35-161">Click New.</span></span>
3. <span data-ttu-id="26e35-162">Geben Sie im Feld "Containerabschlussprofil-Kennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="26e35-163">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="26e35-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="26e35-164">Wählen Sie im Feld "Manifestieren" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="26e35-165">Geben Sie an, ob Manifestierung geschieht, wenn Sie Container schließen oder wenn Sie die Lieferung bestätigen.</span><span class="sxs-lookup"><span data-stu-id="26e35-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="26e35-166">Beachten Sie, dass eine Manifestierung "Transportverwaltung" benötigt.</span><span class="sxs-lookup"><span data-stu-id="26e35-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="26e35-167">Manifestierung muss in den Transportmodulen implementiert werden, damit sie funktioniert.</span><span class="sxs-lookup"><span data-stu-id="26e35-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="26e35-168">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="26e35-169">Geben Sie im Feld "Standardlagerplatz für letzte Lieferung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="26e35-170">Dies ist der Lagerplatz, zu dem Produkte verschoben werden, nachdem die Container geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="26e35-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="26e35-171">Dieser Lagerplatz muss ein Lagerplatzprofil haben, das auf Lagerortparametern definiert ist.</span><span class="sxs-lookup"><span data-stu-id="26e35-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="26e35-172">Geben Sie im Feld "Gewichtseinheit" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="26e35-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="26e35-173">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="26e35-173">Click Save.</span></span>

