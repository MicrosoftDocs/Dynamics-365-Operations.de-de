---
title: Bewertungsebene
description: In diesem Thema wird die Entität „Bewertungsstufe“ für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800332"
---
# <a name="rating-level"></a><span data-ttu-id="dc801-103">Bewertungsebene</span><span class="sxs-lookup"><span data-stu-id="dc801-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dc801-104">In diesem Thema wird die Entität „Bewertungsstufe“ für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dc801-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="dc801-105">Physischer Name: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="dc801-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="dc801-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc801-106">Description</span></span>

<span data-ttu-id="dc801-107">Diese Entität stellt die verfügbaren Bewertungsstufen für Qualifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="dc801-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="dc801-108">Die Bewertungsstufen gelten für alle juristischen Personen.</span><span class="sxs-lookup"><span data-stu-id="dc801-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dc801-109">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="dc801-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="dc801-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc801-110">Properties</span></span>

| <span data-ttu-id="dc801-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc801-111">Property</span></span><br><span data-ttu-id="dc801-112">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="dc801-112">**Physical name**</span></span><br><span data-ttu-id="dc801-113">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="dc801-113">**_Type_**</span></span> | <span data-ttu-id="dc801-114">Verwenden</span><span class="sxs-lookup"><span data-stu-id="dc801-114">Use</span></span> | <span data-ttu-id="dc801-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc801-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dc801-116">**Bewertungsstufenentitätskennung**</span><span class="sxs-lookup"><span data-stu-id="dc801-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="dc801-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="dc801-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="dc801-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="dc801-118">*GUID*</span></span> | <span data-ttu-id="dc801-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc801-119">Read-only</span></span><br><span data-ttu-id="dc801-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-120">Required</span></span><br><span data-ttu-id="dc801-121">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="dc801-121">System-generated</span></span> | <span data-ttu-id="dc801-122">Der vom System generierte eindeutige Bezeichner der Stufe.</span><span class="sxs-lookup"><span data-stu-id="dc801-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="dc801-123">**Bewertungsstufenkennung**</span><span class="sxs-lookup"><span data-stu-id="dc801-123">**Rating Level ID**</span></span><br><span data-ttu-id="dc801-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="dc801-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="dc801-125">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="dc801-125">*String*</span></span> | <span data-ttu-id="dc801-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc801-126">Read/write</span></span><br><span data-ttu-id="dc801-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-127">Required</span></span> | <span data-ttu-id="dc801-128">Vom Benutzer lesbarer eindeutiger Bezeichner der Stufe.</span><span class="sxs-lookup"><span data-stu-id="dc801-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="dc801-129">**Bewertungsmodellkennung**</span><span class="sxs-lookup"><span data-stu-id="dc801-129">**Rating Model ID**</span></span><br><span data-ttu-id="dc801-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="dc801-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="dc801-131">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="dc801-131">*String*</span></span> | <span data-ttu-id="dc801-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc801-132">Read/write</span></span><br><span data-ttu-id="dc801-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-133">Required</span></span> | <span data-ttu-id="dc801-134">Das Bewertungsmodell, zu dem die Bewertungsstufe gehört.</span><span class="sxs-lookup"><span data-stu-id="dc801-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="dc801-135">**Bewertungsmodellentitätskennung**</span><span class="sxs-lookup"><span data-stu-id="dc801-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="dc801-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="dc801-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="dc801-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="dc801-137">*GUID*</span></span> | <span data-ttu-id="dc801-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc801-138">Read-only</span></span><br><span data-ttu-id="dc801-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-139">Required</span></span><br><span data-ttu-id="dc801-140">Fremdschlüssel: mshr_hcmratingmodelentityid von mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="dc801-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="dc801-141">Der vom System generierte Bezeichner für das Bewertungsmodell, zu dem die Bewertungsstufe gehört.</span><span class="sxs-lookup"><span data-stu-id="dc801-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="dc801-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc801-142">**Description**</span></span><br><span data-ttu-id="dc801-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="dc801-143">mshr_description</span></span><br><span data-ttu-id="dc801-144">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="dc801-144">*String*</span></span> | <span data-ttu-id="dc801-145">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc801-145">Read/write</span></span><br><span data-ttu-id="dc801-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-146">Required</span></span> | <span data-ttu-id="dc801-147">Die Beschreibung der Bewertungsstufe.</span><span class="sxs-lookup"><span data-stu-id="dc801-147">The description of the rating level.</span></span> |
| <span data-ttu-id="dc801-148">**Faktor**</span><span class="sxs-lookup"><span data-stu-id="dc801-148">**Factor**</span></span><br><span data-ttu-id="dc801-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="dc801-149">mshr_factor</span></span><br><span data-ttu-id="dc801-150">*Ganzzahl*</span><span class="sxs-lookup"><span data-stu-id="dc801-150">*Integer*</span></span> | <span data-ttu-id="dc801-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc801-151">Read/write</span></span><br><span data-ttu-id="dc801-152">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-152">Required</span></span> | <span data-ttu-id="dc801-153">Der Faktor für die Bewertungsstufe.</span><span class="sxs-lookup"><span data-stu-id="dc801-153">The factor for the rating level.</span></span> <span data-ttu-id="dc801-154">Hier wird ein Faktor eingegeben, durch den die Ergebnisse normalisiert werden, wenn Elemente mit einer unterschiedlichen Anzahl von Ebenen verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="dc801-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="dc801-155">Der Wert muss eine Ganzzahl zwischen 0 und 9 sein.</span><span class="sxs-lookup"><span data-stu-id="dc801-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="dc801-156">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="dc801-156">**Note**</span></span><br><span data-ttu-id="dc801-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="dc801-157">mshr_note</span></span><br><span data-ttu-id="dc801-158">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="dc801-158">*String*</span></span> | <span data-ttu-id="dc801-159">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc801-159">Read/write</span></span><br><span data-ttu-id="dc801-160">Optional</span><span class="sxs-lookup"><span data-stu-id="dc801-160">Optional</span></span> | <span data-ttu-id="dc801-161">Alle mit der Bewertungsstufe verbundenen Notizen.</span><span class="sxs-lookup"><span data-stu-id="dc801-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="dc801-162">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="dc801-162">**Primary Field**</span></span><br><span data-ttu-id="dc801-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="dc801-163">mshr_primaryfield</span></span><br><span data-ttu-id="dc801-164">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="dc801-164">*String*</span></span> | <span data-ttu-id="dc801-165">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc801-165">Read-only</span></span><br><span data-ttu-id="dc801-166">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc801-166">Required</span></span> | <span data-ttu-id="dc801-167">Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc801-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="dc801-168">Kombination aus Bewertungsstufenkennung und Bewertungsmodellkennung.</span><span class="sxs-lookup"><span data-stu-id="dc801-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="dc801-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc801-169">See also</span></span>

[<span data-ttu-id="dc801-170">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="dc801-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="dc801-171">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="dc801-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]