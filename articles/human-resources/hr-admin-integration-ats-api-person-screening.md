---
title: Personenprüfung
description: In diesem Thema wird die Screening-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467240"
---
# <a name="person-screening"></a><span data-ttu-id="e64ce-103">Personenprüfung</span><span class="sxs-lookup"><span data-stu-id="e64ce-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e64ce-104">In diesem Thema wird die Screening-Entität für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e64ce-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e64ce-105">Physischer Name: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="e64ce-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="e64ce-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e64ce-106">Description</span></span>

<span data-ttu-id="e64ce-107">Diese Entität beschreibt Screenings, die ein Kandidat bestanden hat oder für eine Anstellung bestehen muss.</span><span class="sxs-lookup"><span data-stu-id="e64ce-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e64ce-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="e64ce-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="e64ce-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64ce-109">Properties</span></span>

| <span data-ttu-id="e64ce-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e64ce-110">Property</span></span><br><span data-ttu-id="e64ce-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="e64ce-111">**Physical name**</span></span><br><span data-ttu-id="e64ce-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="e64ce-112">**_Type_**</span></span> | <span data-ttu-id="e64ce-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="e64ce-113">Use</span></span> | <span data-ttu-id="e64ce-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e64ce-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e64ce-115">**Personen-Screening-Entitätskennung**</span><span class="sxs-lookup"><span data-stu-id="e64ce-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="e64ce-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="e64ce-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="e64ce-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e64ce-117">*GUID*</span></span> | <span data-ttu-id="e64ce-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64ce-118">Read-only</span></span><br><span data-ttu-id="e64ce-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e64ce-119">Required</span></span><br><span data-ttu-id="e64ce-120">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="e64ce-120">System-generated</span></span> | <span data-ttu-id="e64ce-121">Eindeutiger primärer Bezeichner für den Personen-Screening-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="e64ce-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="e64ce-122">**Parteinummer**</span><span class="sxs-lookup"><span data-stu-id="e64ce-122">**Party Number**</span></span><br><span data-ttu-id="e64ce-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="e64ce-123">mshr_partynumber</span></span><br><span data-ttu-id="e64ce-124">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e64ce-124">*String*</span></span> | <span data-ttu-id="e64ce-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e64ce-125">Read/write</span></span><br><span data-ttu-id="e64ce-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e64ce-126">Required</span></span> | <span data-ttu-id="e64ce-127">Die dem Kandidaten zugeordnete Partei-(Personen-)Nummer.</span><span class="sxs-lookup"><span data-stu-id="e64ce-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="e64ce-128">**Personenkennungswert**</span><span class="sxs-lookup"><span data-stu-id="e64ce-128">**Person ID Value**</span></span><br><span data-ttu-id="e64ce-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="e64ce-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="e64ce-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e64ce-130">*GUID*</span></span> | <span data-ttu-id="e64ce-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64ce-131">Read-only</span></span><br><span data-ttu-id="e64ce-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e64ce-132">Required</span></span><br><span data-ttu-id="e64ce-133">Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="e64ce-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="e64ce-134">Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person).</span><span class="sxs-lookup"><span data-stu-id="e64ce-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="e64ce-135">**Screening-Typ-Kennung**</span><span class="sxs-lookup"><span data-stu-id="e64ce-135">**Screening Type ID**</span></span><br><span data-ttu-id="e64ce-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="e64ce-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="e64ce-137">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e64ce-137">*String*</span></span> | <span data-ttu-id="e64ce-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e64ce-138">Read/write</span></span><br><span data-ttu-id="e64ce-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e64ce-139">Required</span></span><br><span data-ttu-id="e64ce-140">Fremdschlüssel: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="e64ce-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="e64ce-141">Der Bezeichner des Screening-Typs, der in Human Resources definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e64ce-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="e64ce-142">**Wert der Screening-Typ-Kennung**</span><span class="sxs-lookup"><span data-stu-id="e64ce-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="e64ce-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="e64ce-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="e64ce-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e64ce-144">*GUID*</span></span> | <span data-ttu-id="e64ce-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64ce-145">Read-only</span></span><br><span data-ttu-id="e64ce-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e64ce-146">Required</span></span><br><span data-ttu-id="e64ce-147">Fremdschlüssel: mshr_hcmscreeningtypeentityid von mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="e64ce-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="e64ce-148">Vom System generierter Bezeichner für den Screening-Typ-Datensatz der zugeordneten Entität.</span><span class="sxs-lookup"><span data-stu-id="e64ce-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="e64ce-149">**Erforderlich bis**</span><span class="sxs-lookup"><span data-stu-id="e64ce-149">**Required By**</span></span><br><span data-ttu-id="e64ce-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="e64ce-150">mshr_requiredby</span></span><br><span data-ttu-id="e64ce-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="e64ce-151">*Datetime*</span></span> | <span data-ttu-id="e64ce-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e64ce-152">Read/write</span></span><br><span data-ttu-id="e64ce-153">Optional</span><span class="sxs-lookup"><span data-stu-id="e64ce-153">Optional</span></span> | <span data-ttu-id="e64ce-154">Das Datum, bis zu dem das Screening abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="e64ce-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="e64ce-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="e64ce-155">**Status**</span></span><br><span data-ttu-id="e64ce-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="e64ce-156">mshr_status</span></span><br><span data-ttu-id="e64ce-157">*mshr_hcmcompletionstatus-Optionssatz*</span><span class="sxs-lookup"><span data-stu-id="e64ce-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="e64ce-158">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e64ce-158">Read/write</span></span><br><span data-ttu-id="e64ce-159">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e64ce-159">Required</span></span> | <span data-ttu-id="e64ce-160">Gibt den Status des Kandidaten für das Screening an.</span><span class="sxs-lookup"><span data-stu-id="e64ce-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="e64ce-161">**Abschlussdatum**</span><span class="sxs-lookup"><span data-stu-id="e64ce-161">**Completed Date**</span></span><br><span data-ttu-id="e64ce-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="e64ce-162">mshr_completeddate</span></span><br><span data-ttu-id="e64ce-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="e64ce-163">*Datetime*</span></span> | <span data-ttu-id="e64ce-164">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e64ce-164">Read/write</span></span><br><span data-ttu-id="e64ce-165">Optional</span><span class="sxs-lookup"><span data-stu-id="e64ce-165">Optional</span></span> | <span data-ttu-id="e64ce-166">Das Datum, an dem das Screening abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e64ce-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="e64ce-167">**Notizen**</span><span class="sxs-lookup"><span data-stu-id="e64ce-167">**Notes**</span></span><br><span data-ttu-id="e64ce-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="e64ce-168">mshr_note</span></span><br><span data-ttu-id="e64ce-169">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e64ce-169">*String*</span></span> | <span data-ttu-id="e64ce-170">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e64ce-170">Read/write</span></span><br><span data-ttu-id="e64ce-171">Optional</span><span class="sxs-lookup"><span data-stu-id="e64ce-171">Optional</span></span> | <span data-ttu-id="e64ce-172">Hinweise zur Verwendung durch den Personalbeschaffer oder Personalvermittler.</span><span class="sxs-lookup"><span data-stu-id="e64ce-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e64ce-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e64ce-173">See also</span></span>

[<span data-ttu-id="e64ce-174">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="e64ce-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e64ce-175">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="e64ce-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]