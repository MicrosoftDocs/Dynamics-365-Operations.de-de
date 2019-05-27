---
title: Ein neues Lagerortlayout erstellen
description: Diese Prozedur zeigt Ihnen an, wie die Informationen zu den Lagerplätzen in einem Lagerort eingerichtet werden.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572764"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="11cca-103">Ein neues Lagerortlayout erstellen</span><span class="sxs-lookup"><span data-stu-id="11cca-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11cca-104">Diese Prozedur zeigt Ihnen an, wie die Informationen zu den Lagerplätzen in einem Lagerort eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="11cca-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="11cca-105">Dies gilt nur für Lagerorte, die mithilfe von die mithilfe der "Standardlagerung" im Modul "Lagerverwaltung" erstellt wurden, nicht für Lagerorte, die im Modul "Lagerortverwaltung" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="11cca-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="11cca-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="11cca-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="11cca-107">Die Standardlagerplatzkapazität festlegen</span><span class="sxs-lookup"><span data-stu-id="11cca-107">Set the default location capacity</span></span>
1. <span data-ttu-id="11cca-108">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Lager- und Lagerortverwaltungsparameter".</span><span class="sxs-lookup"><span data-stu-id="11cca-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="11cca-109">Klicken Sie auf die Registerkarte "Lagerplätze".</span><span class="sxs-lookup"><span data-stu-id="11cca-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="11cca-110">Geben Sie im Feld "Standardbreite" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="11cca-111">Geben Sie im Feld "Standardtiefe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="11cca-112">Geben Sie im Feld "Standardhöhe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="11cca-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="11cca-113">Click Save.</span></span>
7. <span data-ttu-id="11cca-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="11cca-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="11cca-115">Das Format des Lagerplatznamens definieren</span><span class="sxs-lookup"><span data-stu-id="11cca-115">Define the location name format</span></span>
1. <span data-ttu-id="11cca-116">Wechseln Sie zu Bestandsverwaltung > Einstellungen > Lageraufschlüsselung > Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="11cca-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="11cca-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="11cca-117">Click New.</span></span>
3. <span data-ttu-id="11cca-118">Geben Sie im Feld "Lagerort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="11cca-119">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="11cca-120">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11cca-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="11cca-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="11cca-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11cca-122">Schalten Sie die Erweiterung des Abschnitts "Lagerplatznamen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="11cca-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="11cca-123">Die Optionen in diesem Abschnitt definieren das Standardformat für Lagerplatznamen.</span><span class="sxs-lookup"><span data-stu-id="11cca-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="11cca-124">In unserem Beispiel schließen wir die Gangnummer, Regalnummer und Regelbodennummer ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="11cca-125">Legen Sie die Option "Gang einschließen" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="11cca-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="11cca-126">Legen Sie die Option "Regal einschließen" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="11cca-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="11cca-127">Geben Sie im Feld "Format" für das Regal einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="11cca-128">Beispiel: -##</span><span class="sxs-lookup"><span data-stu-id="11cca-128">For example: -##</span></span>  
11. <span data-ttu-id="11cca-129">Legen Sie die Option "Regalboden einschließen" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="11cca-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="11cca-130">Geben Sie im Feld "Format" für den Regalboden einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11cca-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="11cca-131">Beispiel: -##</span><span class="sxs-lookup"><span data-stu-id="11cca-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="11cca-132">Lagerort-Lagerplätze definieren</span><span class="sxs-lookup"><span data-stu-id="11cca-132">Define warehouse locations</span></span>
1. <span data-ttu-id="11cca-133">Klicken Sie im Aktivitätsbereich auf "Lagerort".</span><span class="sxs-lookup"><span data-stu-id="11cca-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="11cca-134">Klicken Sie auf den Lagerplatz-Assistent.</span><span class="sxs-lookup"><span data-stu-id="11cca-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="11cca-135">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-135">Click Next.</span></span>
4. <span data-ttu-id="11cca-136">Heben Sie die Auswahl für die Option "Ausgangsrampen" auf.</span><span class="sxs-lookup"><span data-stu-id="11cca-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="11cca-137">Heben Sie die Auswahl für die Option "Sammellagerplätze" auf.</span><span class="sxs-lookup"><span data-stu-id="11cca-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="11cca-138">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-138">Click Next.</span></span>
7. <span data-ttu-id="11cca-139">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-139">Click Next.</span></span>
8. <span data-ttu-id="11cca-140">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-140">Click Next.</span></span>
9. <span data-ttu-id="11cca-141">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-141">Click Next.</span></span>
10. <span data-ttu-id="11cca-142">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-142">Click Next.</span></span>
11. <span data-ttu-id="11cca-143">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-143">Click Next.</span></span>
12. <span data-ttu-id="11cca-144">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-144">Click Next.</span></span>
    * <span data-ttu-id="11cca-145">Beachten Sie, dass die physischen Dimensionen, die auf dieser Seite angezeigt werden, die sind, die Sie zu Beginn dieser Prozedur festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="11cca-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="11cca-146">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="11cca-146">Click Next.</span></span>
14. <span data-ttu-id="11cca-147">Klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="11cca-147">Click Finish.</span></span>
15. <span data-ttu-id="11cca-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="11cca-148">Close the page.</span></span>
16. <span data-ttu-id="11cca-149">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="11cca-149">Refresh the page.</span></span>

