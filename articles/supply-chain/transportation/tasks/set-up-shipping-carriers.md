---
title: Spediteure einrichten
description: In diesem Thema erfahren Sie, wie Sie einen Spediteur einrichten und Details wie Service, Versandart, Transportausschreibung, Transportbeschränkungen und Frachtrate definieren.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429073"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="b11b6-103">Spediteure einrichten</span><span class="sxs-lookup"><span data-stu-id="b11b6-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b11b6-104">In diesem Thema erfahren Sie, wie Sie einen Spediteur einrichten und Details wie Service, Versandart, Transportausschreibung, Transportbeschränkungen und Frachtrate definieren.</span><span class="sxs-lookup"><span data-stu-id="b11b6-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="b11b6-105">Ein Transportkoordinator kann dann einen Spediteur einer ein- und ausgehenden Ladung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b11b6-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="b11b6-106">Neuen Spediteur erstellen</span><span class="sxs-lookup"><span data-stu-id="b11b6-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="b11b6-107">Gehen Sie zu **Navigationsbereich > Module > Transportmanagement > Einrichtung > Spediteur > Spediteur > Spediteur**.</span><span class="sxs-lookup"><span data-stu-id="b11b6-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="b11b6-108">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="b11b6-109">Geben Sie in das Feld **Spediteur** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="b11b6-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b11b6-111">Wählen Sie im Feld **Modus** eine Option aus dem Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="b11b6-112">Füllen Sie die allgemeinen Informationen für den Spediteur aus</span><span class="sxs-lookup"><span data-stu-id="b11b6-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="b11b6-113">Schaltet die Erweiterung des Abschnitts **Übersicht** um.</span><span class="sxs-lookup"><span data-stu-id="b11b6-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="b11b6-114">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Spediteur aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="b11b6-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="b11b6-115">Wählen Sie im Feld **Lieferantenkonto** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="b11b6-116">Wählen Sie das Kreditorenkonto aus, das dem Spediteur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b11b6-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="b11b6-117">Wählen Sie im Feld **Transportausschreibungstyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="b11b6-118">Wählen Sie **Manuell**, um die Seite Transportausschreibung zu verwenden, oder wählen Sie **EDI**, um die Ausschreibung über Electronic Data Interchange (EDI) zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b11b6-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="b11b6-119">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Spediteur-Rating aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="b11b6-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="b11b6-120">Erstellen Sie die erforderlichen Dienstleistungen für den Spediteur</span><span class="sxs-lookup"><span data-stu-id="b11b6-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="b11b6-121">Schaltet die Erweiterung des Abschnitts **Dienste** um.</span><span class="sxs-lookup"><span data-stu-id="b11b6-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="b11b6-122">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-122">Select **New**.</span></span>
3. <span data-ttu-id="b11b6-123">Geben Sie im Feld **Spediteurservice** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="b11b6-124">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b11b6-125">Wählen Sie im Feld **Transportmethode** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="b11b6-126">Richten Sie die Adresse für den Spediteur ein (optional)</span><span class="sxs-lookup"><span data-stu-id="b11b6-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="b11b6-127">Schaltet die Erweiterung des Abschnitts **Adressen** um.</span><span class="sxs-lookup"><span data-stu-id="b11b6-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="b11b6-128">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-128">Select **New**.</span></span>
3. <span data-ttu-id="b11b6-129">Geben Sie in das Feld **Name oder Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="b11b6-130">Wählen Sie im Feld **Land/Region** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="b11b6-131">Wählen Sie im Feld **ZIP/Postleitzahl** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="b11b6-132">Geben Sie im Feld **Straße** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="b11b6-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b11b6-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="b11b6-134">Richten Sie das Bewertungsprofil für den Spediteur ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="b11b6-135">Schaltet die Erweiterung des Abschnitts **Bewertungsprofile** ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="b11b6-136">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-136">Select **New**.</span></span>
3. <span data-ttu-id="b11b6-137">Geben Sie im Feld **Bewertungsprofil** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="b11b6-138">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b11b6-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b11b6-139">Wählen Sie im Feld **Lagerort** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="b11b6-140">Wählen Sie im Feld **Lager** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="b11b6-141">Wählen Sie im Feld **Rate-Engine** eine Option aus dem Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="b11b6-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="b11b6-142">Wählen Sie das Tarifmodul aus, das in Übereinstimmung mit dem Vertrag steht, den Sie mit dem Spediteur haben.</span><span class="sxs-lookup"><span data-stu-id="b11b6-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="b11b6-143">Wählen Sie im Feld **Rate-Master** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="b11b6-144">Wählen Sie im Feld **Transitzeit-Engine** eine Option aus dem Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="b11b6-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="b11b6-145">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b11b6-145">Select **Save**.</span></span>

