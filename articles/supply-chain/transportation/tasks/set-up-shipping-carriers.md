---
title: Einrichten von Spediteuren
description: In diesem Verfahren wird gezeigt, wie einen Spediteur eingerichtet wird und Details wie Dienst, Lieferart, Transportzahlungsmittel, Transporteinschränkungen und Versandsatz definiert werden.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "314485"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="6e17e-103">Einrichten von Spediteuren</span><span class="sxs-lookup"><span data-stu-id="6e17e-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e17e-104">In diesem Verfahren wird gezeigt, wie einen Spediteur eingerichtet wird und Details wie Dienst, Lieferart, Transportzahlungsmittel, Transporteinschränkungen und Versandsatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e17e-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="6e17e-105">Ein Transportkoordinator kann dann einen Spediteur einer ein- und ausgehenden Ladung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="6e17e-106">Neuen Spediteur erstellen</span><span class="sxs-lookup"><span data-stu-id="6e17e-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="6e17e-107">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Spediteure" > "Spediteure".</span><span class="sxs-lookup"><span data-stu-id="6e17e-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="6e17e-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6e17e-108">Click New.</span></span>
3. <span data-ttu-id="6e17e-109">Geben Sie im Feld "Spediteur " einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="6e17e-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6e17e-111">Klicken Sie im Feld "Transportart" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6e17e-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6e17e-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="6e17e-114">Füllen Sie die allgemeinen Informationen für den Spediteur aus</span><span class="sxs-lookup"><span data-stu-id="6e17e-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="6e17e-115">Schalten Sie die Erweiterung des Abschnitts "Überblick" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="6e17e-116">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Spediteur aktivieren".</span><span class="sxs-lookup"><span data-stu-id="6e17e-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="6e17e-117">Klicken Sie im Feld "Händler" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6e17e-118">Wählen Sie das Kreditorenkonto aus, das dem Spediteur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e17e-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="6e17e-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6e17e-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6e17e-121">Wählen Sie im Feld "Typ der Transportausschreibung" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="6e17e-122">Wählen Sie "Manuell" aus, um die Seite "Transportausschreibung" zu verwenden, oder wählen Sie "EDI" aus, um das Zahlungsmittel zu aktualisieren, indem Sie elektronischen Datenaustausch (Electronic Data Interchange, EDI) verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e17e-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="6e17e-123">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Spediteursbewertung aktivieren".</span><span class="sxs-lookup"><span data-stu-id="6e17e-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="6e17e-124">Erstellen Sie die erforderlichen Dienstleistungen für den Spediteur</span><span class="sxs-lookup"><span data-stu-id="6e17e-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="6e17e-125">Schalten Sie die Erweiterung des Abschnitts "Dienstleistungen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="6e17e-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6e17e-126">Click New.</span></span>
3. <span data-ttu-id="6e17e-127">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6e17e-128">Geben Sie im Feld "Spediteurdienstleistung " einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="6e17e-129">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6e17e-130">Klicken Sie im Feld "Transportmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6e17e-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6e17e-132">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="6e17e-133">Richten Sie die Adresse für den Spediteur ein (optional)</span><span class="sxs-lookup"><span data-stu-id="6e17e-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="6e17e-134">Schalten Sie die Erweiterung des Abschnitts "Adressen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="6e17e-135">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6e17e-135">Click New.</span></span>
3. <span data-ttu-id="6e17e-136">Geben Sie im Feld "Name oder Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="6e17e-137">Klicken Sie im Feld "Land/Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6e17e-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6e17e-139">Klicken Sie im Feld "Postleitzahl" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6e17e-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6e17e-141">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6e17e-142">Geben Sie im Feld "Straße" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="6e17e-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6e17e-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="6e17e-144">Richten Sie das Bewertungsprofil für den Spediteur ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="6e17e-145">Schalten Sie die Erweiterung des Abschnitts "Bewertungsprofile" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="6e17e-146">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6e17e-146">Click New.</span></span>
3. <span data-ttu-id="6e17e-147">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6e17e-148">Geben Sie im Feld "Bewertungsprofil" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="6e17e-149">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e17e-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6e17e-150">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6e17e-151">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6e17e-152">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6e17e-153">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="6e17e-154">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="6e17e-155">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="6e17e-156">Klicken Sie im Feld "Tarifmodul" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6e17e-157">Wählen Sie das Tarifmodul aus, das in Übereinstimmung mit dem Vertrag steht, den Sie mit dem Spediteur haben.</span><span class="sxs-lookup"><span data-stu-id="6e17e-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="6e17e-158">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="6e17e-159">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="6e17e-160">Klicken Sie im Feld "Satzmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="6e17e-161">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6e17e-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="6e17e-162">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="6e17e-163">Klicken Sie im Feld "Transitzeitmodul" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e17e-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="6e17e-164">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6e17e-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="6e17e-165">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6e17e-165">Click Save.</span></span>

