---
title: Mitarbeiter-Self-Service konfigurieren
description: In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092659"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="09783-103">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="09783-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="09783-104">In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="09783-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="09783-105">Vorteilsplan-Kacheln führen Benutzer zu Vorteilsplänen, für die sie sich registrieren können.</span><span class="sxs-lookup"><span data-stu-id="09783-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="09783-106">Rollencenter-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="09783-106">Set up a role center tile</span></span>

1. <span data-ttu-id="09783-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="09783-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="09783-108">Wählen Sie die Registerkarte **Rollencenter-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="09783-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="09783-109">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="09783-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="09783-110">Feld</span><span class="sxs-lookup"><span data-stu-id="09783-110">Field</span></span> | <span data-ttu-id="09783-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09783-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09783-112">Kachelkennung</span><span class="sxs-lookup"><span data-stu-id="09783-112">Tile ID</span></span> | <span data-ttu-id="09783-113">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="09783-114">Beschriftungstext für Kacheln</span><span class="sxs-lookup"><span data-stu-id="09783-114">Tile label text</span></span> | <span data-ttu-id="09783-115">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09783-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="09783-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09783-116">Description</span></span> | <span data-ttu-id="09783-117">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-117">A description of the tile.</span></span> |
   | <span data-ttu-id="09783-118">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="09783-118">Internet address</span></span> | <span data-ttu-id="09783-119">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="09783-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="09783-120">Kachelgröße</span><span class="sxs-lookup"><span data-stu-id="09783-120">Tile size</span></span> | <span data-ttu-id="09783-121">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="09783-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="09783-122">Vorgabe</span><span class="sxs-lookup"><span data-stu-id="09783-122">Target</span></span> | <span data-ttu-id="09783-123">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09783-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="09783-124">Kachelhintergrundbild</span><span class="sxs-lookup"><span data-stu-id="09783-124">Tile background image</span></span> | <span data-ttu-id="09783-125">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="09783-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="09783-126">Start</span><span class="sxs-lookup"><span data-stu-id="09783-126">Start</span></span> | <span data-ttu-id="09783-127">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="09783-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="09783-128">End</span></span> | <span data-ttu-id="09783-129">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="09783-130">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="09783-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="09783-131">Vorteilsplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="09783-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="09783-132">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="09783-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="09783-133">Wählen Sie die Registerkarte **Vorteilsplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="09783-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="09783-134">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="09783-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="09783-135">Feld</span><span class="sxs-lookup"><span data-stu-id="09783-135">Field</span></span> | <span data-ttu-id="09783-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09783-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09783-137">Kachelkennung</span><span class="sxs-lookup"><span data-stu-id="09783-137">Tile ID</span></span> | <span data-ttu-id="09783-138">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="09783-139">Beschriftungstext für Kacheln</span><span class="sxs-lookup"><span data-stu-id="09783-139">Tile label text</span></span> | <span data-ttu-id="09783-140">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09783-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="09783-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09783-141">Description</span></span> | <span data-ttu-id="09783-142">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-142">A description of the tile.</span></span> |
   | <span data-ttu-id="09783-143">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="09783-143">Internet address</span></span> | <span data-ttu-id="09783-144">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="09783-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="09783-145">Kachelgröße</span><span class="sxs-lookup"><span data-stu-id="09783-145">Tile size</span></span> | <span data-ttu-id="09783-146">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="09783-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="09783-147">Vorgabe</span><span class="sxs-lookup"><span data-stu-id="09783-147">Target</span></span> | <span data-ttu-id="09783-148">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09783-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="09783-149">Kachelhintergrundbild</span><span class="sxs-lookup"><span data-stu-id="09783-149">Tile background image</span></span> | <span data-ttu-id="09783-150">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="09783-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="09783-151">Start</span><span class="sxs-lookup"><span data-stu-id="09783-151">Start</span></span> | <span data-ttu-id="09783-152">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="09783-153">Beenden</span><span class="sxs-lookup"><span data-stu-id="09783-153">End</span></span> | <span data-ttu-id="09783-154">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="09783-155">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="09783-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="09783-156">Flexguthabenplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="09783-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="09783-157">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="09783-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="09783-158">Wählen Sie die Registerkarte **Flexguthabenplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="09783-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="09783-159">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="09783-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="09783-160">Feld</span><span class="sxs-lookup"><span data-stu-id="09783-160">Field</span></span> | <span data-ttu-id="09783-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09783-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09783-162">Kachelkennung</span><span class="sxs-lookup"><span data-stu-id="09783-162">Tile ID</span></span> | <span data-ttu-id="09783-163">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="09783-164">Beschriftungstext für Kacheln</span><span class="sxs-lookup"><span data-stu-id="09783-164">Tile label text</span></span> | <span data-ttu-id="09783-165">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09783-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="09783-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09783-166">Description</span></span> | <span data-ttu-id="09783-167">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-167">A description of the tile.</span></span> |
   | <span data-ttu-id="09783-168">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="09783-168">Internet address</span></span> | <span data-ttu-id="09783-169">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="09783-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="09783-170">Kachelgröße</span><span class="sxs-lookup"><span data-stu-id="09783-170">Tile size</span></span> | <span data-ttu-id="09783-171">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="09783-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="09783-172">Vorgabe</span><span class="sxs-lookup"><span data-stu-id="09783-172">Target</span></span> | <span data-ttu-id="09783-173">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09783-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="09783-174">Kachelhintergrundbild</span><span class="sxs-lookup"><span data-stu-id="09783-174">Tile background image</span></span> | <span data-ttu-id="09783-175">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="09783-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="09783-176">Start</span><span class="sxs-lookup"><span data-stu-id="09783-176">Start</span></span> | <span data-ttu-id="09783-177">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="09783-178">Beenden</span><span class="sxs-lookup"><span data-stu-id="09783-178">End</span></span> | <span data-ttu-id="09783-179">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="09783-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="09783-180">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="09783-180">Select **Save**.</span></span>
