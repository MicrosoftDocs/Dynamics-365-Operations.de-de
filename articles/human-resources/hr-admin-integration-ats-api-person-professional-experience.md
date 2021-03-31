---
title: Berufserfahrung der Person
description: In diesem Thema wird die Entität „Berufserfahrung der Person“ für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 51dd993e2d43174e96c062e142021cc0f6e3a288
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125280"
---
# <a name="person-professional-experience"></a><span data-ttu-id="89275-103">Berufserfahrung der Person</span><span class="sxs-lookup"><span data-stu-id="89275-103">Person professional experience</span></span>

<span data-ttu-id="89275-104">In diesem Thema wird die Entität „Berufserfahrung der Person“ für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="89275-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="89275-105">Physischer Name: mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="89275-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="89275-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89275-106">Description</span></span>

<span data-ttu-id="89275-107">Diese Entität beschreibt die Berufserfahrung oder de Arbeitsverlauf eines Bewerbers.</span><span class="sxs-lookup"><span data-stu-id="89275-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="89275-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="89275-108">JSON representation</span></span>

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="89275-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89275-109">Properties</span></span>

| <span data-ttu-id="89275-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="89275-110">Property</span></span><br><span data-ttu-id="89275-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="89275-111">**Physical name**</span></span><br><span data-ttu-id="89275-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="89275-112">**_Type_**</span></span> | <span data-ttu-id="89275-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="89275-113">Use</span></span> | <span data-ttu-id="89275-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89275-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="89275-115">**Kennung der Entität „Berufserfahrung der Person“**</span><span class="sxs-lookup"><span data-stu-id="89275-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="89275-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="89275-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="89275-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="89275-117">*GUID*</span></span> | <span data-ttu-id="89275-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89275-118">Read-only</span></span><br><span data-ttu-id="89275-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-119">Required</span></span> | <span data-ttu-id="89275-120">Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz.</span><span class="sxs-lookup"><span data-stu-id="89275-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="89275-121">**Parteinummer**</span><span class="sxs-lookup"><span data-stu-id="89275-121">**Party Number**</span></span><br><span data-ttu-id="89275-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="89275-122">mshr_partynumber</span></span><br><span data-ttu-id="89275-123">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-123">*String*</span></span> | <span data-ttu-id="89275-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-124">Read/write</span></span><br><span data-ttu-id="89275-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-125">Required</span></span> | <span data-ttu-id="89275-126">Der eindeutige Bezeichner des Personendatensatzes für den Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="89275-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="89275-127">**Personenkennungswert**</span><span class="sxs-lookup"><span data-stu-id="89275-127">**Person ID Value**</span></span><br><span data-ttu-id="89275-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="89275-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="89275-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="89275-129">*GUID*</span></span> | <span data-ttu-id="89275-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89275-130">Read-only</span></span><br><span data-ttu-id="89275-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-131">Required</span></span><br><span data-ttu-id="89275-132">Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="89275-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="89275-133">Vom System generierter eindeutiger Bezeichner des Personenentitätsdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="89275-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="89275-134">**Mitarbeiterposition**</span><span class="sxs-lookup"><span data-stu-id="89275-134">**Employer Position**</span></span><br><span data-ttu-id="89275-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="89275-135">mshr_employerposition</span></span><br><span data-ttu-id="89275-136">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-136">*String*</span></span> | <span data-ttu-id="89275-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-137">Read/write</span></span><br><span data-ttu-id="89275-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-138">Required</span></span> | <span data-ttu-id="89275-139">Der Positionstitel, den der Kandidat während seiner Beschäftigung innehat.</span><span class="sxs-lookup"><span data-stu-id="89275-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="89275-140">**Arbeitgebername**</span><span class="sxs-lookup"><span data-stu-id="89275-140">**Employer Name**</span></span><br><span data-ttu-id="89275-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="89275-141">mshr_employername</span></span><br><span data-ttu-id="89275-142">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-142">*String*</span></span> | <span data-ttu-id="89275-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-143">Read/write</span></span><br><span data-ttu-id="89275-144">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-144">Required</span></span> | <span data-ttu-id="89275-145">Der Name des Arbeitgebers.</span><span class="sxs-lookup"><span data-stu-id="89275-145">The name of the employer.</span></span> |
| <span data-ttu-id="89275-146">**Standort des Arbeitgebers**</span><span class="sxs-lookup"><span data-stu-id="89275-146">**Employer Location**</span></span><br><span data-ttu-id="89275-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="89275-147">mshr_employerlocation</span></span><br><span data-ttu-id="89275-148">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-148">*String*</span></span> | <span data-ttu-id="89275-149">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-149">Read/write</span></span><br><span data-ttu-id="89275-150">Optional</span><span class="sxs-lookup"><span data-stu-id="89275-150">Optional</span></span> | <span data-ttu-id="89275-151">Der Standort des Arbeitgebers.</span><span class="sxs-lookup"><span data-stu-id="89275-151">The employer’s location.</span></span> <span data-ttu-id="89275-152">Maximale Länge: 60.</span><span class="sxs-lookup"><span data-stu-id="89275-152">Max length: 60.</span></span> <span data-ttu-id="89275-153">Kein bestimmtes Format definiert oder erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89275-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="89275-154">**Telefonnummer**</span><span class="sxs-lookup"><span data-stu-id="89275-154">**Phone**</span></span><br><span data-ttu-id="89275-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="89275-155">mshr_phone</span></span><br><span data-ttu-id="89275-156">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-156">*String*</span></span> | <span data-ttu-id="89275-157">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-157">Read/write</span></span><br><span data-ttu-id="89275-158">Optional</span><span class="sxs-lookup"><span data-stu-id="89275-158">Optional</span></span> | <span data-ttu-id="89275-159">Die Telefonnummer des Arbeitgebers.</span><span class="sxs-lookup"><span data-stu-id="89275-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="89275-160">**URL**</span><span class="sxs-lookup"><span data-stu-id="89275-160">**URL**</span></span><br><span data-ttu-id="89275-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="89275-161">mshr_url</span></span><br><span data-ttu-id="89275-162">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-162">*String*</span></span> | <span data-ttu-id="89275-163">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-163">Read/write</span></span><br><span data-ttu-id="89275-164">Optional</span><span class="sxs-lookup"><span data-stu-id="89275-164">Optional</span></span> | <span data-ttu-id="89275-165">Die URL der Website des Arbeitgebers.</span><span class="sxs-lookup"><span data-stu-id="89275-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="89275-166">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="89275-166">**Start Date**</span></span><br><span data-ttu-id="89275-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="89275-167">mshr_startdate</span></span><br><span data-ttu-id="89275-168">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="89275-168">*Datetime*</span></span> | <span data-ttu-id="89275-169">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-169">Read/write</span></span><br><span data-ttu-id="89275-170">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-170">Required</span></span> | <span data-ttu-id="89275-171">Das Startdatum der Anstellung des Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="89275-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="89275-172">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="89275-172">**End Date**</span></span><br><span data-ttu-id="89275-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="89275-173">mshr_enddate</span></span><br><span data-ttu-id="89275-174">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="89275-174">*Datetime*</span></span> | <span data-ttu-id="89275-175">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-175">Read/write</span></span><br><span data-ttu-id="89275-176">Optional</span><span class="sxs-lookup"><span data-stu-id="89275-176">Optional</span></span> | <span data-ttu-id="89275-177">Das Enddatum der Anstellung des Kandidaten oder null, wenn der Kandidat noch hier beschäftigt ist.</span><span class="sxs-lookup"><span data-stu-id="89275-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="89275-178">**Arbeitgeberkontakt zulassen**</span><span class="sxs-lookup"><span data-stu-id="89275-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="89275-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="89275-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="89275-180">*mshr_hrmblankyesno-Optionssatz*</span><span class="sxs-lookup"><span data-stu-id="89275-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="89275-181">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-181">Read/write</span></span><br><span data-ttu-id="89275-182">Optional</span><span class="sxs-lookup"><span data-stu-id="89275-182">Optional</span></span> | <span data-ttu-id="89275-183">Gibt an, ob der Kandidat die Kontaktaufnahme mit dem vorherigen Arbeitgeber zulässt.</span><span class="sxs-lookup"><span data-stu-id="89275-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="89275-184">**Notizen**</span><span class="sxs-lookup"><span data-stu-id="89275-184">**Notes**</span></span><br><span data-ttu-id="89275-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="89275-185">mshr_note</span></span><br><span data-ttu-id="89275-186">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-186">*String*</span></span> | <span data-ttu-id="89275-187">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89275-187">Read/write</span></span><br><span data-ttu-id="89275-188">Optional</span><span class="sxs-lookup"><span data-stu-id="89275-188">Optional</span></span> | <span data-ttu-id="89275-189">Hinweise zur Verwendung durch den Personalvermittler oder Einstellungsmanager.</span><span class="sxs-lookup"><span data-stu-id="89275-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="89275-190">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="89275-190">**Primary Field**</span></span><br><span data-ttu-id="89275-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="89275-191">mshr_primaryfield</span></span><br><span data-ttu-id="89275-192">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="89275-192">*String*</span></span> | <span data-ttu-id="89275-193">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89275-193">Read-only</span></span><br><span data-ttu-id="89275-194">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89275-194">Required</span></span> | <span data-ttu-id="89275-195">Feld, das als ein primärer Bezeichner des Entitätsdatensatzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89275-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="89275-196">Kombination aus Parteinummer, Startdatum, Arbeitgeberposition und Name des Arbeitgebers.</span><span class="sxs-lookup"><span data-stu-id="89275-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="89275-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89275-197">See also</span></span>

[<span data-ttu-id="89275-198">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="89275-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="89275-199">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="89275-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
