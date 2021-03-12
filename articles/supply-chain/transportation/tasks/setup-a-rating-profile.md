---
title: Bewertungsprofile
description: Dieses Thema beschreibt, wie Sie die Daten für Bewertungsprofile festlegen.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973959"
---
# <a name="rating-profiles"></a><span data-ttu-id="2c9ff-103">Bewertungsprofile</span><span class="sxs-lookup"><span data-stu-id="2c9ff-103">Rating profiles</span></span>

<span data-ttu-id="2c9ff-104">Ein Tarifprofil ähnelt einem Logistikvertrag (aber nicht einem Rechtsvertrag).</span><span class="sxs-lookup"><span data-stu-id="2c9ff-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="2c9ff-105">Es wird verwendet, um Transporttarife für Ladungen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="2c9ff-106">Jedes Tarifprofil ist einzigartig für einen Spediteur.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="2c9ff-107">Im Profil verknüpfen Sie den Spediteur mit einem Tarifmaster.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="2c9ff-108">Der Tarifmaster definiert die Tarifbasiszuordnung und die Tarifbasis.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="2c9ff-109">Die Tarifbasis bestimmt den Satz des Spediteurs.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="2c9ff-110">Sie können ein Satzprofil über eine generische Seite festlegen, die eine Übersicht über alle vorhandenen Satzprofile anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="2c9ff-111">Alternativ können Sie ein Tarifprofil auch direkt vom Spediteur festlegen.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="2c9ff-112">In beiden Fällen sind die Informationen, die Sie für das Bewertungsprofil festlegen, die gleichen.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="2c9ff-113">Erstellen oder bearbeiten Sie ein Bewertungsprofil auf der Seite Bewertungsprofile</span><span class="sxs-lookup"><span data-stu-id="2c9ff-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="2c9ff-114">Auf der Seite **Bewertungsprofile** können Sie alle verfügbaren Bewertungsprofile einsehen.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="2c9ff-115">Sie können auch vorhandene Profile bearbeiten und neue Profile erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="2c9ff-116">Gehen Sie zu **Transportverwaltung \> Einrichten \> Bewertung \> Bewertungsprofil**.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="2c9ff-117">Wählen Sie im Aktivitätsbereich **Neu**, um ein neues Bewertungsprofil zum Raster hinzuzufügen, oder wählen Sie **Bearbeiten**, um ein vorhandenes Profil zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="2c9ff-118">Legen Sie in der Zeile für das neue oder bestehende Bewertungsprofil die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="2c9ff-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="2c9ff-119">**Bewertungsprofil** - Geben Sie einen eindeutigen Bezeichner (ID) für das Bewertungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="2c9ff-120">**Name** - Geben Sie einen beschreibenden Namen für das Bewertungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="2c9ff-121">**Spediteur** - Wählen Sie einen Spediteur aus.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="2c9ff-122">Das Bewertungsprofil, das Sie festlegen, wird auch auf der Seite **Versandunternehmen** für den gewählten Spediteur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="2c9ff-123">**Standort** und **Lagerort** - Wählen Sie einen Standort und einen Lagerort.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="2c9ff-124">**Tarifrechner** - Wählen Sie den Tarifrechner für das Tarifprofil.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="2c9ff-125">**Tarifmaster** - Wählen Sie den Tarifmaster für das Tarifprofil.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="2c9ff-126">Sie können den Tarifmaster verwenden, um einen Tarifbasistyp und eine Tarifbasis zu definieren.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="2c9ff-127">Für weitere Informationen siehe [Tarifmaster festlegen](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="2c9ff-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="2c9ff-128">**Transitzeit-Engine** - Wählen Sie die Transitzeit-Engine für das Rating-Profil.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="2c9ff-129">**Kraftstoffindex des Spediteurs** - Wählen Sie den Kraftstoffindex des Spediteurs für das Tarifprofil aus.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="2c9ff-130">**Effektives Startdatum und -uhrzeit** und **Effektives Enddatum und -uhrzeit** - Definieren Sie den Zeitraum, in dem das Bewertungsprofil aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="2c9ff-131">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="2c9ff-132">Erstellen Sie ein Bewertungsprofil direkt auf der Seite Spediteure</span><span class="sxs-lookup"><span data-stu-id="2c9ff-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="2c9ff-133">Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="2c9ff-134">Wählen Sie einen Spediteur in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="2c9ff-135">Wählen Sie auf dem Inforegister **Bewertungsprofile** die Option **Neu**, um ein Bewertungsprofil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="2c9ff-136">Legen Sie die Felder für das neue Bewertungsprofil fest.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="2c9ff-137">Diese Felder entsprechen den Feldern auf der Seite **Bewertungsprofile**, wie im vorherigen Abschnitt dieses Themas beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="2c9ff-138">Profile, die auf der Seite **Spediteure** erstellt werden, werden auch auf der Seite **Bewertungsprofile** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c9ff-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
