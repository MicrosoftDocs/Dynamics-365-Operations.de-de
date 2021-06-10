---
title: Mitarbeiter-Self-Service konfigurieren
description: In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f0d39b30b7c8d0a5729ebe3b1ed9e0d569a6660
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052984"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="5dd0d-103">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="5dd0d-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5dd0d-104">In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="5dd0d-105">Vorteilsplan-Kacheln führen Benutzer zu Vorteilsplänen, auf die Sie Anrecht haben.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="5dd0d-106">Vorteilsplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="5dd0d-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="5dd0d-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5dd0d-108">Wählen Sie die Registerkarte **Vorteilsplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5dd0d-109">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="5dd0d-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5dd0d-110">Feld</span><span class="sxs-lookup"><span data-stu-id="5dd0d-110">Field</span></span> | <span data-ttu-id="5dd0d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dd0d-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5dd0d-112">**Kachelkennung**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-112">**Tile ID**</span></span> | <span data-ttu-id="5dd0d-113">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5dd0d-114">**Beschriftungstext für Kacheln**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-114">**Tile label text**</span></span> | <span data-ttu-id="5dd0d-115">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="5dd0d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-116">**Description**</span></span> | <span data-ttu-id="5dd0d-117">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-117">A description of the tile.</span></span> |
   | <span data-ttu-id="5dd0d-118">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-118">**Internet address**</span></span> | <span data-ttu-id="5dd0d-119">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5dd0d-120">**Kachelgröße**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-120">**Tile size**</span></span> | <span data-ttu-id="5dd0d-121">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5dd0d-122">**Vorgabe**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-122">**Target**</span></span> | <span data-ttu-id="5dd0d-123">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5dd0d-124">**Kachelhintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-124">**Tile background image**</span></span> | <span data-ttu-id="5dd0d-125">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="5dd0d-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5dd0d-126">**Start**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-126">**Start**</span></span> | <span data-ttu-id="5dd0d-127">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5dd0d-128">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-128">**End**</span></span> | <span data-ttu-id="5dd0d-129">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5dd0d-130">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="5dd0d-131">Flexguthabenplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="5dd0d-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="5dd0d-132">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5dd0d-133">Wählen Sie die Registerkarte **Flexguthabenplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5dd0d-134">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="5dd0d-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5dd0d-135">Feld</span><span class="sxs-lookup"><span data-stu-id="5dd0d-135">Field</span></span> | <span data-ttu-id="5dd0d-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dd0d-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5dd0d-137">**Kachelkennung**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-137">**Tile ID**</span></span> | <span data-ttu-id="5dd0d-138">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5dd0d-139">**Beschriftungstext für Kacheln**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-139">**Tile label text**</span></span> | <span data-ttu-id="5dd0d-140">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="5dd0d-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-141">**Description**</span></span> | <span data-ttu-id="5dd0d-142">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-142">A description of the tile.</span></span> |
   | <span data-ttu-id="5dd0d-143">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-143">**Internet address**</span></span> | <span data-ttu-id="5dd0d-144">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5dd0d-145">**Kachelgröße**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-145">**Tile size**</span></span> | <span data-ttu-id="5dd0d-146">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5dd0d-147">**Vorgabe**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-147">**Target**</span></span> | <span data-ttu-id="5dd0d-148">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5dd0d-149">**Kachelhintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-149">**Tile background image**</span></span> | <span data-ttu-id="5dd0d-150">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="5dd0d-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5dd0d-151">**Start**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-151">**Start**</span></span> | <span data-ttu-id="5dd0d-152">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5dd0d-153">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="5dd0d-153">**End**</span></span> | <span data-ttu-id="5dd0d-154">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5dd0d-155">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]