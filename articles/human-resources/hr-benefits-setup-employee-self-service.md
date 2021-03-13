---
title: Mitarbeiter-Self-Service konfigurieren
description: In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112666"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="d221e-103">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d221e-103">Configure employee self service</span></span>

<span data-ttu-id="d221e-104">In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d221e-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="d221e-105">Vorteilsplan-Kacheln führen Benutzer zu Vorteilsplänen, auf die Sie Anrecht haben.</span><span class="sxs-lookup"><span data-stu-id="d221e-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="d221e-106">Vorteilsplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="d221e-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="d221e-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d221e-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d221e-108">Wählen Sie die Registerkarte **Vorteilsplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d221e-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d221e-109">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="d221e-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d221e-110">Feld</span><span class="sxs-lookup"><span data-stu-id="d221e-110">Field</span></span> | <span data-ttu-id="d221e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d221e-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d221e-112">**Kachelkennung**</span><span class="sxs-lookup"><span data-stu-id="d221e-112">**Tile ID**</span></span> | <span data-ttu-id="d221e-113">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d221e-114">**Beschriftungstext für Kacheln**</span><span class="sxs-lookup"><span data-stu-id="d221e-114">**Tile label text**</span></span> | <span data-ttu-id="d221e-115">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d221e-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d221e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d221e-116">**Description**</span></span> | <span data-ttu-id="d221e-117">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-117">A description of the tile.</span></span> |
   | <span data-ttu-id="d221e-118">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="d221e-118">**Internet address**</span></span> | <span data-ttu-id="d221e-119">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="d221e-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d221e-120">**Kachelgröße**</span><span class="sxs-lookup"><span data-stu-id="d221e-120">**Tile size**</span></span> | <span data-ttu-id="d221e-121">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="d221e-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d221e-122">**Vorgabe**</span><span class="sxs-lookup"><span data-stu-id="d221e-122">**Target**</span></span> | <span data-ttu-id="d221e-123">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d221e-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d221e-124">**Kachelhintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="d221e-124">**Tile background image**</span></span> | <span data-ttu-id="d221e-125">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="d221e-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d221e-126">**Start**</span><span class="sxs-lookup"><span data-stu-id="d221e-126">**Start**</span></span> | <span data-ttu-id="d221e-127">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d221e-128">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="d221e-128">**End**</span></span> | <span data-ttu-id="d221e-129">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d221e-130">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d221e-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="d221e-131">Flexguthabenplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="d221e-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="d221e-132">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d221e-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d221e-133">Wählen Sie die Registerkarte **Flexguthabenplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d221e-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d221e-134">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="d221e-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d221e-135">Feld</span><span class="sxs-lookup"><span data-stu-id="d221e-135">Field</span></span> | <span data-ttu-id="d221e-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d221e-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d221e-137">**Kachelkennung**</span><span class="sxs-lookup"><span data-stu-id="d221e-137">**Tile ID**</span></span> | <span data-ttu-id="d221e-138">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d221e-139">**Beschriftungstext für Kacheln**</span><span class="sxs-lookup"><span data-stu-id="d221e-139">**Tile label text**</span></span> | <span data-ttu-id="d221e-140">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d221e-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="d221e-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d221e-141">**Description**</span></span> | <span data-ttu-id="d221e-142">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-142">A description of the tile.</span></span> |
   | <span data-ttu-id="d221e-143">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="d221e-143">**Internet address**</span></span> | <span data-ttu-id="d221e-144">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="d221e-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d221e-145">**Kachelgröße**</span><span class="sxs-lookup"><span data-stu-id="d221e-145">**Tile size**</span></span> | <span data-ttu-id="d221e-146">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="d221e-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d221e-147">**Vorgabe**</span><span class="sxs-lookup"><span data-stu-id="d221e-147">**Target**</span></span> | <span data-ttu-id="d221e-148">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d221e-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d221e-149">**Kachelhintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="d221e-149">**Tile background image**</span></span> | <span data-ttu-id="d221e-150">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="d221e-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d221e-151">**Start**</span><span class="sxs-lookup"><span data-stu-id="d221e-151">**Start**</span></span> | <span data-ttu-id="d221e-152">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d221e-153">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="d221e-153">**End**</span></span> | <span data-ttu-id="d221e-154">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d221e-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d221e-155">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d221e-155">Select **Save**.</span></span>
