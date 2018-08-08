--- 
title: Einrichten von Spediteuren
description: "In diesem Verfahren wird gezeigt, wie einen Spediteur eingerichtet wird und Details wie Dienst, Lieferart, Transportzahlungsmittel, Transporteinschränkungen und Versandsatz definiert werden."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="8cef3-103">Einrichten von Spediteuren</span><span class="sxs-lookup"><span data-stu-id="8cef3-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8cef3-104">In diesem Verfahren wird gezeigt, wie einen Spediteur eingerichtet wird und Details wie Dienst, Lieferart, Transportzahlungsmittel, Transporteinschränkungen und Versandsatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8cef3-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="8cef3-105">Ein Transportkoordinator kann dann einen Spediteur einer ein- und ausgehenden Ladung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="8cef3-106">Neuen Spediteur erstellen</span><span class="sxs-lookup"><span data-stu-id="8cef3-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="8cef3-107">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Spediteure" > "Spediteure".</span><span class="sxs-lookup"><span data-stu-id="8cef3-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="8cef3-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8cef3-108">Click New.</span></span>
3. <span data-ttu-id="8cef3-109">Geben Sie im Feld "Spediteur " einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="8cef3-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8cef3-111">Klicken Sie im Feld "Transportart" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8cef3-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8cef3-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="8cef3-114">Füllen Sie die allgemeinen Informationen für den Spediteur aus</span><span class="sxs-lookup"><span data-stu-id="8cef3-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="8cef3-115">Schalten Sie die Erweiterung des Abschnitts "Überblick" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="8cef3-116">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Spediteur aktivieren".</span><span class="sxs-lookup"><span data-stu-id="8cef3-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="8cef3-117">Klicken Sie im Feld "Händler" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8cef3-118">Wählen Sie das Kreditorenkonto aus, das dem Spediteur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cef3-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="8cef3-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8cef3-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8cef3-121">Wählen Sie im Feld "Typ der Transportausschreibung" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="8cef3-122">Wählen Sie "Manuell" aus, um die Seite "Transportausschreibung" zu verwenden, oder wählen Sie "EDI" aus, um das Zahlungsmittel zu aktualisieren, indem Sie elektronischen Datenaustausch (Electronic Data Interchange, EDI) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8cef3-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="8cef3-123">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Spediteursbewertung aktivieren".</span><span class="sxs-lookup"><span data-stu-id="8cef3-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="8cef3-124">Erstellen Sie die erforderlichen Dienstleistungen für den Spediteur</span><span class="sxs-lookup"><span data-stu-id="8cef3-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="8cef3-125">Schalten Sie die Erweiterung des Abschnitts "Dienstleistungen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="8cef3-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8cef3-126">Click New.</span></span>
3. <span data-ttu-id="8cef3-127">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8cef3-128">Geben Sie im Feld "Spediteurdienstleistung " einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="8cef3-129">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="8cef3-130">Klicken Sie im Feld "Transportmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8cef3-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8cef3-132">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="8cef3-133">Richten Sie die Adresse für den Spediteur ein (optional)</span><span class="sxs-lookup"><span data-stu-id="8cef3-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="8cef3-134">Schalten Sie die Erweiterung des Abschnitts "Adressen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="8cef3-135">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8cef3-135">Click New.</span></span>
3. <span data-ttu-id="8cef3-136">Geben Sie im Feld "Name oder Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="8cef3-137">Klicken Sie im Feld "Land/Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8cef3-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8cef3-139">Klicken Sie im Feld "Postleitzahl" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8cef3-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8cef3-141">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8cef3-142">Geben Sie im Feld "Straße" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="8cef3-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8cef3-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="8cef3-144">Richten Sie das Bewertungsprofil für den Spediteur ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="8cef3-145">Schalten Sie die Erweiterung des Abschnitts "Bewertungsprofile" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="8cef3-146">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8cef3-146">Click New.</span></span>
3. <span data-ttu-id="8cef3-147">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8cef3-148">Geben Sie im Feld "Bewertungsprofil" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="8cef3-149">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cef3-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="8cef3-150">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8cef3-151">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8cef3-152">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8cef3-153">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8cef3-154">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="8cef3-155">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8cef3-156">Klicken Sie im Feld "Tarifmodul" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8cef3-157">Wählen Sie das Tarifmodul aus, das in Übereinstimmung mit dem Vertrag steht, den Sie mit dem Spediteur haben.</span><span class="sxs-lookup"><span data-stu-id="8cef3-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="8cef3-158">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8cef3-159">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="8cef3-160">Klicken Sie im Feld "Satzmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="8cef3-161">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8cef3-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="8cef3-162">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="8cef3-163">Klicken Sie im Feld "Transitzeitmodul" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cef3-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="8cef3-164">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cef3-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="8cef3-165">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8cef3-165">Click Save.</span></span>


