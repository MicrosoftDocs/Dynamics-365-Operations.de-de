---
title: Ausbildung des Personalbeschaffungsantrags
description: In diesem Thema wird die Entität für die Ausbildung des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126073"
---
# <a name="recruiting-request-education"></a><span data-ttu-id="56476-103">Ausbildung des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="56476-103">Recruiting request education</span></span>

<span data-ttu-id="56476-104">In diesem Thema wird die Entität für die Ausbildung des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="56476-104">This topic describes the Recruiting request education entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="56476-105">Physischer Name: mshr_hcmrecruitingrequesteducationentity</span><span class="sxs-lookup"><span data-stu-id="56476-105">Physical name: mshr_hcmrecruitingrequesteducationentity</span></span>

### <a name="description"></a><span data-ttu-id="56476-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56476-106">Description</span></span>

<span data-ttu-id="56476-107">Beschreibt die Ausbildungsanforderungen für eine RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="56476-107">Describes educational requirements for a RecruitingRequest.</span></span>

### <a name="json-representation"></a><span data-ttu-id="56476-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="56476-108">JSON representation</span></span>

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="56476-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56476-109">Properties</span></span>

| <span data-ttu-id="56476-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56476-110">Property</span></span><br><span data-ttu-id="56476-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="56476-111">**Physical name**</span></span><br><span data-ttu-id="56476-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="56476-112">**_Type_**</span></span> | <span data-ttu-id="56476-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="56476-113">Use</span></span> | <span data-ttu-id="56476-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56476-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="56476-115">**Kennung der Personalbeschaffungsantragsausbildung-Entität**</span><span class="sxs-lookup"><span data-stu-id="56476-115">**Recruiting Request Education Entity ID**</span></span><br><span data-ttu-id="56476-116">mshr_hcmrecruitingrequesteducationentityid</span><span class="sxs-lookup"><span data-stu-id="56476-116">mshr_hcmrecruitingrequesteducationentityid</span></span><br><span data-ttu-id="56476-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="56476-117">*GUID*</span></span> | <span data-ttu-id="56476-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-118">Read-only</span></span><br><span data-ttu-id="56476-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-119">Required</span></span> | <span data-ttu-id="56476-120">Vom System generierter eindeutiger Bezeichner für den Datensatz Personalbeschaffungsantragsausbildung.</span><span class="sxs-lookup"><span data-stu-id="56476-120">System-generated unique identifier for the Recruiting Request Education record.</span></span> |
| <span data-ttu-id="56476-121">**Personalbeschaffungsantragskennung**</span><span class="sxs-lookup"><span data-stu-id="56476-121">**Recruiting Request ID**</span></span><br><span data-ttu-id="56476-122">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="56476-122">mshr_recruitingrequestid</span></span><br><span data-ttu-id="56476-123">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="56476-123">*String*</span></span> | <span data-ttu-id="56476-124">Einmal schreiben</span><span class="sxs-lookup"><span data-stu-id="56476-124">Write-once</span></span><br><span data-ttu-id="56476-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-125">Required</span></span> | <span data-ttu-id="56476-126">Der vom Benutzer lesbare eindeutige Bezeichner des zugehörigen Personalbeschaffungsantrags.</span><span class="sxs-lookup"><span data-stu-id="56476-126">The user-readable unique identifier of the related recruiting request.</span></span> |
| <span data-ttu-id="56476-127">**Wert der Personalbeschaffungsantragskennung**</span><span class="sxs-lookup"><span data-stu-id="56476-127">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="56476-128">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="56476-128">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="56476-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="56476-129">*GUID*</span></span> | <span data-ttu-id="56476-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-130">Read-only</span></span><br><span data-ttu-id="56476-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-131">Required</span></span><br><span data-ttu-id="56476-132">Fremdschlüssel: mshr_hcmrecruitingrequestentityid von mshr_hcmrecruitingrequestentity</span><span class="sxs-lookup"><span data-stu-id="56476-132">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity</span></span> | <span data-ttu-id="56476-133">Vom System generierter eindeutiger Bezeichner des zugehörigen Personalbeschaffungsantrags.</span><span class="sxs-lookup"><span data-stu-id="56476-133">System-generated unique identifier of the related recruiting request.</span></span> |
| <span data-ttu-id="56476-134">**Ausbildungsgradskennung**</span><span class="sxs-lookup"><span data-stu-id="56476-134">**Education Level ID**</span></span><br><span data-ttu-id="56476-135">mshr_educationlevelid</span><span class="sxs-lookup"><span data-stu-id="56476-135">mshr_educationlevelid</span></span><br><span data-ttu-id="56476-136">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="56476-136">*String*</span></span> | <span data-ttu-id="56476-137">Einmal schreiben</span><span class="sxs-lookup"><span data-stu-id="56476-137">Write-once</span></span><br><span data-ttu-id="56476-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-138">Required</span></span> | <span data-ttu-id="56476-139">Die erforderliche Stufe der Ausbildung.</span><span class="sxs-lookup"><span data-stu-id="56476-139">The level of education required.</span></span> |
| <span data-ttu-id="56476-140">**Wert der Ausbildungsgradskennung**</span><span class="sxs-lookup"><span data-stu-id="56476-140">**Educational Level ID Value**</span></span><br><span data-ttu-id="56476-141">_mshr_fk_educationlevel_id_value</span><span class="sxs-lookup"><span data-stu-id="56476-141">_mshr_fk_educationlevel_id_value</span></span><br><span data-ttu-id="56476-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="56476-142">*GUID*</span></span> | <span data-ttu-id="56476-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-143">Read-only</span></span><br><span data-ttu-id="56476-144">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-144">Required</span></span><br><span data-ttu-id="56476-145">Fremdschlüssel: mshr_hcmeducationlevelentityid von mshr_hcmeducationlevelentity</span><span class="sxs-lookup"><span data-stu-id="56476-145">Foreign key: mshr_hcmeducationlevelentityid of mshr_hcmeducationlevelentity</span></span> | <span data-ttu-id="56476-146">Vom System generierter eindeutiger Bezeichner der erforderlichen Stufe der Ausbildung.</span><span class="sxs-lookup"><span data-stu-id="56476-146">System-generated unique identifier of the level of education required.</span></span> |
| <span data-ttu-id="56476-147">**Beschreibung des Ausbildungsstufe**</span><span class="sxs-lookup"><span data-stu-id="56476-147">**Education Level Description**</span></span><br><span data-ttu-id="56476-148">mshr_educationleveldescription</span><span class="sxs-lookup"><span data-stu-id="56476-148">mshr_educationleveldescription</span></span><br><span data-ttu-id="56476-149">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="56476-149">*String*</span></span> | <span data-ttu-id="56476-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-150">Read-only</span></span><br><span data-ttu-id="56476-151">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-151">Required</span></span> | <span data-ttu-id="56476-152">Die Beschreibung der erforderlichen Stufe für die Qualifikation.</span><span class="sxs-lookup"><span data-stu-id="56476-152">The description of the level required for the skill.</span></span> |
| <span data-ttu-id="56476-153">**Ausbildungsfachkennung**</span><span class="sxs-lookup"><span data-stu-id="56476-153">**Education Discipline ID**</span></span><br><span data-ttu-id="56476-154">mshr_educationdisciplinedescription</span><span class="sxs-lookup"><span data-stu-id="56476-154">mshr_educationdisciplinedescription</span></span><br><span data-ttu-id="56476-155">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="56476-155">*String*</span></span> | <span data-ttu-id="56476-156">Einmal schreiben</span><span class="sxs-lookup"><span data-stu-id="56476-156">Write-once</span></span><br><span data-ttu-id="56476-157">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-157">Required</span></span> | <span data-ttu-id="56476-158">Der Bereich des Ausbildungsfachs.</span><span class="sxs-lookup"><span data-stu-id="56476-158">The area of educational discipline.</span></span> |
| <span data-ttu-id="56476-159">**Wert der Ausbildungsfachkennung**</span><span class="sxs-lookup"><span data-stu-id="56476-159">**Education Discipline ID Value**</span></span><br><span data-ttu-id="56476-160">_mshr_fk_educationdiscipline_id_value</span><span class="sxs-lookup"><span data-stu-id="56476-160">_mshr_fk_educationdiscipline_id_value</span></span><br><span data-ttu-id="56476-161">*GUID*</span><span class="sxs-lookup"><span data-stu-id="56476-161">*GUID*</span></span> | <span data-ttu-id="56476-162">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-162">Read-only</span></span><br><span data-ttu-id="56476-163">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-163">Required</span></span><br><span data-ttu-id="56476-164">Fremdschlüssel: mshr_hcmeducationdisciplineentityid von mshr_hcmeducationdisciplineentity</span><span class="sxs-lookup"><span data-stu-id="56476-164">Foreign key: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity</span></span> | <span data-ttu-id="56476-165">Vom System generierter eindeutiger Bezeichner des Gebiets des Ausbildungsfachs.</span><span class="sxs-lookup"><span data-stu-id="56476-165">System-generated unique identifier of the area of educational discipline.</span></span> |
| <span data-ttu-id="56476-166">**Beschreibung des Ausbildungsfachs**</span><span class="sxs-lookup"><span data-stu-id="56476-166">**Education Discipline Description**</span></span><br><span data-ttu-id="56476-167">mshr_educationdisciplinedescription</span><span class="sxs-lookup"><span data-stu-id="56476-167">mshr_educationdisciplinedescription</span></span><br><span data-ttu-id="56476-168">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="56476-168">String</span></span> | <span data-ttu-id="56476-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-169">Read-only</span></span><br><span data-ttu-id="56476-170">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-170">Required</span></span> | <span data-ttu-id="56476-171">Die Beschreibung des Gebiets des Ausbildungsfachs.</span><span class="sxs-lookup"><span data-stu-id="56476-171">The description of the area of educational discipline.</span></span> |
| <span data-ttu-id="56476-172">**Datenbereichskennung**</span><span class="sxs-lookup"><span data-stu-id="56476-172">**Data Area ID**</span></span><br><span data-ttu-id="56476-173">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="56476-173">mshr_dataareaid</span></span><br><span data-ttu-id="56476-174">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="56476-174">*String*</span></span> | <span data-ttu-id="56476-175">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="56476-175">Read/write</span></span><br><span data-ttu-id="56476-176">Optional</span><span class="sxs-lookup"><span data-stu-id="56476-176">Optional</span></span> | <span data-ttu-id="56476-177">Gibt die juristische Person (Firma) an.</span><span class="sxs-lookup"><span data-stu-id="56476-177">Specifies the legal entity (company).</span></span>|
| <span data-ttu-id="56476-178">**Wert der Datenbereichskennung**</span><span class="sxs-lookup"><span data-stu-id="56476-178">**Data Area ID Value**</span></span><br><span data-ttu-id="56476-179">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="56476-179">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="56476-180">*GUID*</span><span class="sxs-lookup"><span data-stu-id="56476-180">*GUID*</span></span> | <span data-ttu-id="56476-181">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-181">Read-only</span></span><br><span data-ttu-id="56476-182">Optional</span><span class="sxs-lookup"><span data-stu-id="56476-182">Optional</span></span><br><span data-ttu-id="56476-183">Fremdschlüssel: cdm_companyid der Entität cdm_company</span><span class="sxs-lookup"><span data-stu-id="56476-183">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="56476-184">Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56476-184">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="56476-185">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="56476-185">**Primary Field**</span></span><br><span data-ttu-id="56476-186">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="56476-186">mshr_primaryfield</span></span><br><span data-ttu-id="56476-187">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="56476-187">*String*</span></span> | <span data-ttu-id="56476-188">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56476-188">Read-only</span></span><br><span data-ttu-id="56476-189">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56476-189">Required</span></span> | <span data-ttu-id="56476-190">Verkettung des Werts des Personalbeschaffungsantrags, der Ausbildungsstufenkennung und der Ausbildungsfachkennung als weitere Methode zur eindeutigen Identifizierung des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="56476-190">Concatenation of Recruiting Request value, Education Level ID, and Education Discipline ID as another method to uniquely identify the record.</span></span> |

## <a name="see-also"></a><span data-ttu-id="56476-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56476-191">See also</span></span>

[<span data-ttu-id="56476-192">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="56476-192">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="56476-193">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="56476-193">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
