---
title: Personenprüfung
description: In diesem Thema wird die Screening-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798032"
---
# <a name="person-screening"></a><span data-ttu-id="3685d-103">Personenprüfung</span><span class="sxs-lookup"><span data-stu-id="3685d-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3685d-104">In diesem Thema wird die Screening-Entität für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3685d-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3685d-105">Physischer Name: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="3685d-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="3685d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3685d-106">Description</span></span>

<span data-ttu-id="3685d-107">Diese Entität beschreibt Screenings, die ein Kandidat bestanden hat oder für eine Anstellung bestehen muss.</span><span class="sxs-lookup"><span data-stu-id="3685d-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3685d-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="3685d-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="3685d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3685d-109">Properties</span></span>

| <span data-ttu-id="3685d-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3685d-110">Property</span></span><br><span data-ttu-id="3685d-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="3685d-111">**Physical name**</span></span><br><span data-ttu-id="3685d-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="3685d-112">**_Type_**</span></span> | <span data-ttu-id="3685d-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="3685d-113">Use</span></span> | <span data-ttu-id="3685d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3685d-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3685d-115">**Personen-Screening-Entitätskennung**</span><span class="sxs-lookup"><span data-stu-id="3685d-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="3685d-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="3685d-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="3685d-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3685d-117">*GUID*</span></span> | <span data-ttu-id="3685d-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3685d-118">Read-only</span></span><br><span data-ttu-id="3685d-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3685d-119">Required</span></span><br><span data-ttu-id="3685d-120">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="3685d-120">System-generated</span></span> | <span data-ttu-id="3685d-121">Eindeutiger primärer Bezeichner für den Personen-Screening-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="3685d-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="3685d-122">**Parteinummer**</span><span class="sxs-lookup"><span data-stu-id="3685d-122">**Party Number**</span></span><br><span data-ttu-id="3685d-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="3685d-123">mshr_partynumber</span></span><br><span data-ttu-id="3685d-124">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3685d-124">*String*</span></span> | <span data-ttu-id="3685d-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3685d-125">Read/write</span></span><br><span data-ttu-id="3685d-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3685d-126">Required</span></span> | <span data-ttu-id="3685d-127">Die dem Kandidaten zugeordnete Partei-(Personen-)Nummer.</span><span class="sxs-lookup"><span data-stu-id="3685d-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="3685d-128">**Personenkennungswert**</span><span class="sxs-lookup"><span data-stu-id="3685d-128">**Person ID Value**</span></span><br><span data-ttu-id="3685d-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="3685d-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="3685d-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3685d-130">*GUID*</span></span> | <span data-ttu-id="3685d-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3685d-131">Read-only</span></span><br><span data-ttu-id="3685d-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3685d-132">Required</span></span><br><span data-ttu-id="3685d-133">Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="3685d-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="3685d-134">Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person).</span><span class="sxs-lookup"><span data-stu-id="3685d-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="3685d-135">**Screening-Typ-Kennung**</span><span class="sxs-lookup"><span data-stu-id="3685d-135">**Screening Type ID**</span></span><br><span data-ttu-id="3685d-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="3685d-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="3685d-137">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3685d-137">*String*</span></span> | <span data-ttu-id="3685d-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3685d-138">Read/write</span></span><br><span data-ttu-id="3685d-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3685d-139">Required</span></span><br><span data-ttu-id="3685d-140">Fremdschlüssel: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="3685d-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="3685d-141">Der Bezeichner des Screening-Typs, der in Human Resources definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3685d-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="3685d-142">**Wert der Screening-Typ-Kennung**</span><span class="sxs-lookup"><span data-stu-id="3685d-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="3685d-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="3685d-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="3685d-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3685d-144">*GUID*</span></span> | <span data-ttu-id="3685d-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3685d-145">Read-only</span></span><br><span data-ttu-id="3685d-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3685d-146">Required</span></span><br><span data-ttu-id="3685d-147">Fremdschlüssel: mshr_hcmscreeningtypeentityid von mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="3685d-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="3685d-148">Vom System generierter Bezeichner für den Screening-Typ-Datensatz der zugeordneten Entität.</span><span class="sxs-lookup"><span data-stu-id="3685d-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="3685d-149">**Erforderlich bis**</span><span class="sxs-lookup"><span data-stu-id="3685d-149">**Required By**</span></span><br><span data-ttu-id="3685d-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="3685d-150">mshr_requiredby</span></span><br><span data-ttu-id="3685d-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="3685d-151">*Datetime*</span></span> | <span data-ttu-id="3685d-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3685d-152">Read/write</span></span><br><span data-ttu-id="3685d-153">Optional</span><span class="sxs-lookup"><span data-stu-id="3685d-153">Optional</span></span> | <span data-ttu-id="3685d-154">Das Datum, bis zu dem das Screening abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="3685d-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="3685d-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="3685d-155">**Status**</span></span><br><span data-ttu-id="3685d-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="3685d-156">mshr_status</span></span><br><span data-ttu-id="3685d-157">*mshr_hcmcompletionstatus-Optionssatz*</span><span class="sxs-lookup"><span data-stu-id="3685d-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="3685d-158">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3685d-158">Read/write</span></span><br><span data-ttu-id="3685d-159">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3685d-159">Required</span></span> | <span data-ttu-id="3685d-160">Gibt den Status des Kandidaten für das Screening an.</span><span class="sxs-lookup"><span data-stu-id="3685d-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="3685d-161">**Abschlussdatum**</span><span class="sxs-lookup"><span data-stu-id="3685d-161">**Completed Date**</span></span><br><span data-ttu-id="3685d-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="3685d-162">mshr_completeddate</span></span><br><span data-ttu-id="3685d-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="3685d-163">*Datetime*</span></span> | <span data-ttu-id="3685d-164">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3685d-164">Read/write</span></span><br><span data-ttu-id="3685d-165">Optional</span><span class="sxs-lookup"><span data-stu-id="3685d-165">Optional</span></span> | <span data-ttu-id="3685d-166">Das Datum, an dem das Screening abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3685d-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="3685d-167">**Notizen**</span><span class="sxs-lookup"><span data-stu-id="3685d-167">**Notes**</span></span><br><span data-ttu-id="3685d-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="3685d-168">mshr_note</span></span><br><span data-ttu-id="3685d-169">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3685d-169">*String*</span></span> | <span data-ttu-id="3685d-170">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3685d-170">Read/write</span></span><br><span data-ttu-id="3685d-171">Optional</span><span class="sxs-lookup"><span data-stu-id="3685d-171">Optional</span></span> | <span data-ttu-id="3685d-172">Hinweise zur Verwendung durch den Personalbeschaffer oder Personalvermittler.</span><span class="sxs-lookup"><span data-stu-id="3685d-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3685d-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3685d-173">See also</span></span>

[<span data-ttu-id="3685d-174">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="3685d-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3685d-175">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="3685d-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]