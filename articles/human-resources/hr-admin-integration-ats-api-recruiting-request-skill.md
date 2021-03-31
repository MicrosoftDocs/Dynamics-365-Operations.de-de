---
title: Qualifikation des Personalbeschaffungsantrags
description: In diesem Thema wird die „Qualifikation für Personalbeschaffungsanträge“-Entität für Dynamics 365 Human Resources beschrieben.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 83a9956b9aa820e8aca9bf6b2ab920a45c1061f6
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126001"
---
# <a name="recruiting-request-skill"></a><span data-ttu-id="c1f75-103">Qualifikation des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="c1f75-103">Recruiting request skill</span></span>

<span data-ttu-id="c1f75-104">In diesem Thema wird die „Qualifikation für Personalbeschaffungsanträge“-Entität für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c1f75-104">This topic describes the Recruiting request skill entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c1f75-105">Physischer Name: mshr_hcmrecruitingrequestskillentity</span><span class="sxs-lookup"><span data-stu-id="c1f75-105">Physical name: mshr_hcmrecruitingrequestskillentity</span></span>

### <a name="description"></a><span data-ttu-id="c1f75-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1f75-106">Description</span></span>

<span data-ttu-id="c1f75-107">Beschreibt die Qualifikationsanforderungen für eine RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="c1f75-107">Describes skill requirements for a RecruitingRequest.</span></span>

### <a name="json-representation"></a><span data-ttu-id="c1f75-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="c1f75-108">JSON representation</span></span>

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="c1f75-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1f75-109">Properties</span></span>

| <span data-ttu-id="c1f75-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1f75-110">Property</span></span><br><span data-ttu-id="c1f75-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="c1f75-111">**Physical name**</span></span><br><span data-ttu-id="c1f75-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="c1f75-112">**_Type_**</span></span> | <span data-ttu-id="c1f75-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="c1f75-113">Use</span></span> | <span data-ttu-id="c1f75-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1f75-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c1f75-115">**Kennung der Personalbeschaffungsantragsqualifikations-Entität**</span><span class="sxs-lookup"><span data-stu-id="c1f75-115">**Recruiting Request Skill Entity ID**</span></span><br><span data-ttu-id="c1f75-116">mshr_hcmrecruitingrequestskillentityid</span><span class="sxs-lookup"><span data-stu-id="c1f75-116">mshr_hcmrecruitingrequestskillentityid</span></span><br><span data-ttu-id="c1f75-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c1f75-117">*GUID*</span></span> | <span data-ttu-id="c1f75-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-118">Read-only</span></span><br><span data-ttu-id="c1f75-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-119">Required</span></span> | <span data-ttu-id="c1f75-120">Vom System generierter eindeutiger Bezeichner für den Datensatz **Personalbeschaffungsantragsqualifikation**.</span><span class="sxs-lookup"><span data-stu-id="c1f75-120">System-generated unique identifier for the **Recruiting Request Skill** record.</span></span> |
| <span data-ttu-id="c1f75-121">**Personalbeschaffungsantragskennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-121">**Recruiting Request ID**</span></span><br><span data-ttu-id="c1f75-122">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="c1f75-122">mshr_recruitingrequestid</span></span><br><span data-ttu-id="c1f75-123">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-123">*String*</span></span> | <span data-ttu-id="c1f75-124">Einmal schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f75-124">Write-once</span></span><br><span data-ttu-id="c1f75-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-125">Required</span></span> | <span data-ttu-id="c1f75-126">Der vom Benutzer lesbare eindeutige Bezeichner des zugehörigen Personalbeschaffungsantrags.</span><span class="sxs-lookup"><span data-stu-id="c1f75-126">The user-readable unique identifier of the associated recruiting request.</span></span> |
| <span data-ttu-id="c1f75-127">**Wert der Personalbeschaffungsantragskennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-127">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="c1f75-128">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="c1f75-128">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="c1f75-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c1f75-129">*GUID*</span></span> | <span data-ttu-id="c1f75-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-130">Read-only</span></span><br><span data-ttu-id="c1f75-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-131">Required</span></span><br> <span data-ttu-id="c1f75-132">Fremdschlüssel: mshr_hcmrecruitingrequestentityid der Entität mshr_hcmrecruitingrequestentity</span><span class="sxs-lookup"><span data-stu-id="c1f75-132">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity entity</span></span> | <span data-ttu-id="c1f75-133">Vom System generierter eindeutiger Bezeichner des zugehörigen Personalbeschaffungsantrags.</span><span class="sxs-lookup"><span data-stu-id="c1f75-133">System-generated unique identifier of the associated recruiting request.</span></span> |
| <span data-ttu-id="c1f75-134">**Qualifikationskennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-134">**Skill ID**</span></span><br><span data-ttu-id="c1f75-135">mshr_skillid</span><span class="sxs-lookup"><span data-stu-id="c1f75-135">mshr_skillid</span></span><br><span data-ttu-id="c1f75-136">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-136">*String*</span></span><br> | <span data-ttu-id="c1f75-137">Einmal schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f75-137">Write-once</span></span><br><span data-ttu-id="c1f75-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-138">Required</span></span> | <span data-ttu-id="c1f75-139">Der vom Benutzer lesbare eindeutige Bezeichner des erforderlichen Qualifikation.</span><span class="sxs-lookup"><span data-stu-id="c1f75-139">The user-readable unique identifier of the required skill.</span></span> |
| <span data-ttu-id="c1f75-140">**Wert der Qualifikationskennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-140">**Skill ID Value**</span></span><br><span data-ttu-id="c1f75-141">_mshr_fk_skill_id_value</span><span class="sxs-lookup"><span data-stu-id="c1f75-141">_mshr_fk_skill_id_value</span></span><br><span data-ttu-id="c1f75-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c1f75-142">*GUID*</span></span> | <span data-ttu-id="c1f75-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-143">Read-only</span></span><br><span data-ttu-id="c1f75-144">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-144">Required</span></span><br><span data-ttu-id="c1f75-145">Fremdschlüssel: mshr_hcmskillentityid der Entität mshr_hcmskillentity</span><span class="sxs-lookup"><span data-stu-id="c1f75-145">Foreign key: mshr_hcmskillentityid of mshr_hcmskillentity entity</span></span> | <span data-ttu-id="c1f75-146">Vom System generierter eindeutiger Bezeichner der erforderlichen Qualifikation.</span><span class="sxs-lookup"><span data-stu-id="c1f75-146">System-generated unique identifier of the required skill.</span></span> |
| <span data-ttu-id="c1f75-147">**Bewertungsstufenkennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-147">**Rating Level ID**</span></span><br><span data-ttu-id="c1f75-148">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="c1f75-148">mshr_ratinglevelid</span></span><br><span data-ttu-id="c1f75-149">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-149">*String*</span></span> | <span data-ttu-id="c1f75-150">Einmal schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f75-150">Write-once</span></span><br><span data-ttu-id="c1f75-151">Optional</span><span class="sxs-lookup"><span data-stu-id="c1f75-151">Optional</span></span> | <span data-ttu-id="c1f75-152">Der Wert der erforderlichen Qualifikationsstufe, die für die Stelle ausgewählt wurde, basierend auf dem der Qualifikation zugewiesenen Bewertungsmodell.</span><span class="sxs-lookup"><span data-stu-id="c1f75-152">The required skill level value selected for the job, based on the rating model assigned to the skill.</span></span> |
| <span data-ttu-id="c1f75-153">**Wert der Bewertungsstufenkennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-153">**Rating Level ID Value**</span></span><br><span data-ttu-id="c1f75-154">_mshr_fk_ratinglevel_id_value</span><span class="sxs-lookup"><span data-stu-id="c1f75-154">_mshr_fk_ratinglevel_id_value</span></span><br><span data-ttu-id="c1f75-155">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c1f75-155">*GUID*</span></span> | <span data-ttu-id="c1f75-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-156">Read-only</span></span><br><span data-ttu-id="c1f75-157">Optional</span><span class="sxs-lookup"><span data-stu-id="c1f75-157">Optional</span></span><br><span data-ttu-id="c1f75-158">Fremdschlüssel: mshr_hcmratinglevelentityid der Entität mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="c1f75-158">Foreign key: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity entity</span></span> | <span data-ttu-id="c1f75-159">Vom System generierter eindeutiger Bezeichner der Stufe.</span><span class="sxs-lookup"><span data-stu-id="c1f75-159">System-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="c1f75-160">**Qualifikationsbeschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-160">**Skill Description**</span></span><br><span data-ttu-id="c1f75-161">mshr_skilldescription</span><span class="sxs-lookup"><span data-stu-id="c1f75-161">mshr_skilldescription</span></span><br><span data-ttu-id="c1f75-162">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-162">*String*</span></span> | <span data-ttu-id="c1f75-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-163">Read-only</span></span><br><span data-ttu-id="c1f75-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-164">Required</span></span> | <span data-ttu-id="c1f75-165">Die Qualifikationsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="c1f75-165">The skill description.</span></span> |
| <span data-ttu-id="c1f75-166">**Beschreibung der Bewertungsstufe**</span><span class="sxs-lookup"><span data-stu-id="c1f75-166">**Rating Level Description**</span></span><br><span data-ttu-id="c1f75-167">mshr_ratingleveldescription</span><span class="sxs-lookup"><span data-stu-id="c1f75-167">mshr_ratingleveldescription</span></span><br><span data-ttu-id="c1f75-168">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-168">*String*</span></span> | <span data-ttu-id="c1f75-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-169">Read-only</span></span><br><span data-ttu-id="c1f75-170">Optional</span><span class="sxs-lookup"><span data-stu-id="c1f75-170">Optional</span></span> | <span data-ttu-id="c1f75-171">Die Beschreibung der ausgewählten Qualifikationsstufe.</span><span class="sxs-lookup"><span data-stu-id="c1f75-171">The description of the selected skill level.</span></span> |
| <span data-ttu-id="c1f75-172">**Datenbereichskennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-172">**Data Area ID**</span></span><br><span data-ttu-id="c1f75-173">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="c1f75-173">mshr_dataareaid</span></span><br><span data-ttu-id="c1f75-174">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-174">*String*</span></span> | <span data-ttu-id="c1f75-175">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f75-175">Read/write</span></span><br><span data-ttu-id="c1f75-176">Optional</span><span class="sxs-lookup"><span data-stu-id="c1f75-176">Optional</span></span> | <span data-ttu-id="c1f75-177">Gibt die juristische Person (Firma) an.</span><span class="sxs-lookup"><span data-stu-id="c1f75-177">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="c1f75-178">**Wert der Datenbereichskennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-178">**Data Area ID Value**</span></span><br><span data-ttu-id="c1f75-179">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="c1f75-179">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="c1f75-180">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c1f75-180">*GUID*</span></span> | <span data-ttu-id="c1f75-181">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-181">Read-only</span></span><br><span data-ttu-id="c1f75-182">Optional</span><span class="sxs-lookup"><span data-stu-id="c1f75-182">Optional</span></span><br><span data-ttu-id="c1f75-183">Fremdschlüssel: cdm_companyid der Entität cdm_company</span><span class="sxs-lookup"><span data-stu-id="c1f75-183">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="c1f75-184">Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c1f75-184">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="c1f75-185">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="c1f75-185">**Primary Field**</span></span><br><span data-ttu-id="c1f75-186">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="c1f75-186">mshr_primaryfield</span></span><br><span data-ttu-id="c1f75-187">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-187">*String*</span></span> | <span data-ttu-id="c1f75-188">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-188">Read-only</span></span><br><span data-ttu-id="c1f75-189">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-189">Required</span></span> | <span data-ttu-id="c1f75-190">Verkettung des Werts des Personalbeschaffungsantrags und der Qualifikationskennung als weitere Methode zur eindeutigen Identifizierung des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="c1f75-190">Concatenation of Recruiting Request value and Skill ID as another method to uniquely identify the record.</span></span> |
| <span data-ttu-id="c1f75-191">**Bewertungsmodellkennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-191">**Rating Model ID**</span></span><br><span data-ttu-id="c1f75-192">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="c1f75-192">mshr_ratingmodelid</span></span><br><span data-ttu-id="c1f75-193">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c1f75-193">*String*</span></span> | <span data-ttu-id="c1f75-194">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f75-194">Read-write</span></span><br><span data-ttu-id="c1f75-195">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-195">Required</span></span> | <span data-ttu-id="c1f75-196">Das Bewertungsmodell zur Bewertung der Qualifikation.</span><span class="sxs-lookup"><span data-stu-id="c1f75-196">The rating model used to rate the skill.</span></span> |
| <span data-ttu-id="c1f75-197">**Wert der Bewertungsmodellkennung**</span><span class="sxs-lookup"><span data-stu-id="c1f75-197">**Rating Model ID Value**</span></span><br><span data-ttu-id="c1f75-198">_mshr_fk_hcmratingmodel_id_value</span><span class="sxs-lookup"><span data-stu-id="c1f75-198">_mshr_fk_hcmratingmodel_id_value</span></span><br><span data-ttu-id="c1f75-199">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c1f75-199">*GUID*</span></span> | <span data-ttu-id="c1f75-200">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f75-200">Read-only</span></span><br><span data-ttu-id="c1f75-201">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1f75-201">Required</span></span><br><span data-ttu-id="c1f75-202">Fremdschlüssel: mshr_hcmratingmodelentityid der Entität mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="c1f75-202">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity entity</span></span> | <span data-ttu-id="c1f75-203">Vom System generierter eindeutiger Bezeichner des Bewertungsmodells, das zur Bewertung der Qualifikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1f75-203">System-generated unique identifier of the rating model used to rate the skill.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c1f75-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1f75-204">See also</span></span>

[<span data-ttu-id="c1f75-205">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="c1f75-205">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c1f75-206">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="c1f75-206">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)