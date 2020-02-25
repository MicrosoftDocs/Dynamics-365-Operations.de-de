---
title: Mitarbeiter-Self-Service konfigurieren
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009157"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="1246b-102">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1246b-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1246b-103">In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1246b-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="1246b-104">Vorteilsplan-Kacheln führen Benutzer zu Vorteilsplänen, für die sie sich registrieren können.</span><span class="sxs-lookup"><span data-stu-id="1246b-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="1246b-105">Rollencenter-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="1246b-105">Set up a role center tile</span></span>

1. <span data-ttu-id="1246b-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="1246b-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1246b-107">Wählen Sie die Registerkarte **Rollencenter-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1246b-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1246b-108">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="1246b-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1246b-109">Feld</span><span class="sxs-lookup"><span data-stu-id="1246b-109">Field</span></span> | <span data-ttu-id="1246b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1246b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1246b-111">Kachelkennung</span><span class="sxs-lookup"><span data-stu-id="1246b-111">Tile ID</span></span> | <span data-ttu-id="1246b-112">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1246b-113">Beschriftungstext für Kacheln</span><span class="sxs-lookup"><span data-stu-id="1246b-113">Tile label text</span></span> | <span data-ttu-id="1246b-114">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1246b-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1246b-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1246b-115">Description</span></span> | <span data-ttu-id="1246b-116">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-116">A description of the tile.</span></span> |
   | <span data-ttu-id="1246b-117">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="1246b-117">Internet address</span></span> | <span data-ttu-id="1246b-118">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="1246b-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1246b-119">Kachelgröße</span><span class="sxs-lookup"><span data-stu-id="1246b-119">Tile size</span></span> | <span data-ttu-id="1246b-120">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="1246b-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1246b-121">Vorgabe</span><span class="sxs-lookup"><span data-stu-id="1246b-121">Target</span></span> | <span data-ttu-id="1246b-122">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1246b-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1246b-123">Kachelhintergrundbild</span><span class="sxs-lookup"><span data-stu-id="1246b-123">Tile background image</span></span> | <span data-ttu-id="1246b-124">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="1246b-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1246b-125">Start</span><span class="sxs-lookup"><span data-stu-id="1246b-125">Start</span></span> | <span data-ttu-id="1246b-126">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1246b-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="1246b-127">End</span></span> | <span data-ttu-id="1246b-128">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1246b-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1246b-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="1246b-130">Vorteilsplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="1246b-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="1246b-131">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="1246b-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1246b-132">Wählen Sie die Registerkarte **Vorteilsplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1246b-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1246b-133">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="1246b-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1246b-134">Feld</span><span class="sxs-lookup"><span data-stu-id="1246b-134">Field</span></span> | <span data-ttu-id="1246b-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1246b-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1246b-136">Kachelkennung</span><span class="sxs-lookup"><span data-stu-id="1246b-136">Tile ID</span></span> | <span data-ttu-id="1246b-137">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1246b-138">Beschriftungstext für Kacheln</span><span class="sxs-lookup"><span data-stu-id="1246b-138">Tile label text</span></span> | <span data-ttu-id="1246b-139">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1246b-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1246b-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1246b-140">Description</span></span> | <span data-ttu-id="1246b-141">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-141">A description of the tile.</span></span> |
   | <span data-ttu-id="1246b-142">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="1246b-142">Internet address</span></span> | <span data-ttu-id="1246b-143">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="1246b-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1246b-144">Kachelgröße</span><span class="sxs-lookup"><span data-stu-id="1246b-144">Tile size</span></span> | <span data-ttu-id="1246b-145">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="1246b-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1246b-146">Vorgabe</span><span class="sxs-lookup"><span data-stu-id="1246b-146">Target</span></span> | <span data-ttu-id="1246b-147">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1246b-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1246b-148">Kachelhintergrundbild</span><span class="sxs-lookup"><span data-stu-id="1246b-148">Tile background image</span></span> | <span data-ttu-id="1246b-149">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="1246b-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1246b-150">Start</span><span class="sxs-lookup"><span data-stu-id="1246b-150">Start</span></span> | <span data-ttu-id="1246b-151">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1246b-152">Beenden</span><span class="sxs-lookup"><span data-stu-id="1246b-152">End</span></span> | <span data-ttu-id="1246b-153">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1246b-154">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1246b-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="1246b-155">Flexguthabenplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="1246b-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="1246b-156">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="1246b-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1246b-157">Wählen Sie die Registerkarte **Flexguthabenplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1246b-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1246b-158">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="1246b-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1246b-159">Feld</span><span class="sxs-lookup"><span data-stu-id="1246b-159">Field</span></span> | <span data-ttu-id="1246b-160">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1246b-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1246b-161">Kachelkennung</span><span class="sxs-lookup"><span data-stu-id="1246b-161">Tile ID</span></span> | <span data-ttu-id="1246b-162">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1246b-163">Beschriftungstext für Kacheln</span><span class="sxs-lookup"><span data-stu-id="1246b-163">Tile label text</span></span> | <span data-ttu-id="1246b-164">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1246b-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1246b-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1246b-165">Description</span></span> | <span data-ttu-id="1246b-166">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-166">A description of the tile.</span></span> |
   | <span data-ttu-id="1246b-167">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="1246b-167">Internet address</span></span> | <span data-ttu-id="1246b-168">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="1246b-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1246b-169">Kachelgröße</span><span class="sxs-lookup"><span data-stu-id="1246b-169">Tile size</span></span> | <span data-ttu-id="1246b-170">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="1246b-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1246b-171">Vorgabe</span><span class="sxs-lookup"><span data-stu-id="1246b-171">Target</span></span> | <span data-ttu-id="1246b-172">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1246b-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1246b-173">Kachelhintergrundbild</span><span class="sxs-lookup"><span data-stu-id="1246b-173">Tile background image</span></span> | <span data-ttu-id="1246b-174">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="1246b-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1246b-175">Start</span><span class="sxs-lookup"><span data-stu-id="1246b-175">Start</span></span> | <span data-ttu-id="1246b-176">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1246b-177">Beenden</span><span class="sxs-lookup"><span data-stu-id="1246b-177">End</span></span> | <span data-ttu-id="1246b-178">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="1246b-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1246b-179">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1246b-179">Select **Save**.</span></span>
