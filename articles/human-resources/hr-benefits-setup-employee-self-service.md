---
title: Mitarbeiter-Self-Service konfigurieren
description: In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: d1534e37e83e22dd9860de54165c062935db3798
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430646"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="ebc5b-103">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ebc5b-103">Configure employee self service</span></span>

<span data-ttu-id="ebc5b-104">In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="ebc5b-105">Vorteilsplan-Kacheln führen Benutzer zu Vorteilsplänen, auf die Sie Anrecht haben.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="ebc5b-106">Vorteilsplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="ebc5b-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="ebc5b-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ebc5b-108">Wählen Sie die Registerkarte **Vorteilsplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ebc5b-109">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="ebc5b-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ebc5b-110">Feld</span><span class="sxs-lookup"><span data-stu-id="ebc5b-110">Field</span></span> | <span data-ttu-id="ebc5b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebc5b-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ebc5b-112">**Kachelkennung**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-112">**Tile ID**</span></span> | <span data-ttu-id="ebc5b-113">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ebc5b-114">**Beschriftungstext für Kacheln**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-114">**Tile label text**</span></span> | <span data-ttu-id="ebc5b-115">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="ebc5b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-116">**Description**</span></span> | <span data-ttu-id="ebc5b-117">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-117">A description of the tile.</span></span> |
   | <span data-ttu-id="ebc5b-118">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-118">**Internet address**</span></span> | <span data-ttu-id="ebc5b-119">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ebc5b-120">**Kachelgröße**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-120">**Tile size**</span></span> | <span data-ttu-id="ebc5b-121">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ebc5b-122">**Vorgabe**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-122">**Target**</span></span> | <span data-ttu-id="ebc5b-123">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ebc5b-124">**Kachelhintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-124">**Tile background image**</span></span> | <span data-ttu-id="ebc5b-125">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="ebc5b-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ebc5b-126">**Start**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-126">**Start**</span></span> | <span data-ttu-id="ebc5b-127">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ebc5b-128">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-128">**End**</span></span> | <span data-ttu-id="ebc5b-129">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ebc5b-130">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="ebc5b-131">Flexguthabenplan-Kachel einrichten</span><span class="sxs-lookup"><span data-stu-id="ebc5b-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="ebc5b-132">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ebc5b-133">Wählen Sie die Registerkarte **Flexguthabenplan-Kachel einrichten** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ebc5b-134">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="ebc5b-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ebc5b-135">Feld</span><span class="sxs-lookup"><span data-stu-id="ebc5b-135">Field</span></span> | <span data-ttu-id="ebc5b-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebc5b-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ebc5b-137">**Kachelkennung**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-137">**Tile ID**</span></span> | <span data-ttu-id="ebc5b-138">Der eindeutige Bezeichner für die Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ebc5b-139">**Beschriftungstext für Kacheln**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-139">**Tile label text**</span></span> | <span data-ttu-id="ebc5b-140">Der Text, der auf der Kachel im Self-Service angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="ebc5b-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-141">**Description**</span></span> | <span data-ttu-id="ebc5b-142">Eine Beschreibung der Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-142">A description of the tile.</span></span> |
   | <span data-ttu-id="ebc5b-143">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-143">**Internet address**</span></span> | <span data-ttu-id="ebc5b-144">Geben Sie die URL zur Mitarbeiter-Self-Service-Seite ein.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ebc5b-145">**Kachelgröße**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-145">**Tile size**</span></span> | <span data-ttu-id="ebc5b-146">Die Größe der Kachel: Klein, Mittel oder Groß.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ebc5b-147">**Vorgabe**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-147">**Target**</span></span> | <span data-ttu-id="ebc5b-148">Gibt an, ob die Seite in einem neuen Fenster oder im aktuellen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ebc5b-149">**Kachelhintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-149">**Tile background image**</span></span> | <span data-ttu-id="ebc5b-150">Die URL des Bildes, das für die Kachel verwendet werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="ebc5b-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ebc5b-151">**Start**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-151">**Start**</span></span> | <span data-ttu-id="ebc5b-152">Anfangsdatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ebc5b-153">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="ebc5b-153">**End**</span></span> | <span data-ttu-id="ebc5b-154">Enddatum und ‑uhrzeit für Verfügbarkeit der Kachel.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ebc5b-155">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-155">Select **Save**.</span></span>
