---
title: Zertifkat der Person
description: In diesem Thema wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125352"
---
# <a name="person-certificate"></a><span data-ttu-id="f07e8-103">Zertifkat der Person</span><span class="sxs-lookup"><span data-stu-id="f07e8-103">Person certificate</span></span>

<span data-ttu-id="f07e8-104">In diesem Thema wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f07e8-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f07e8-105">Physischer Name: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="f07e8-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="f07e8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f07e8-106">Description</span></span>

<span data-ttu-id="f07e8-107">Diese Entität beschreibt die Berufszertifikate eines Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="f07e8-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f07e8-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="f07e8-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="f07e8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f07e8-109">Properties</span></span>

| <span data-ttu-id="f07e8-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f07e8-110">Property</span></span><br><span data-ttu-id="f07e8-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="f07e8-111">**Physical name**</span></span><br><span data-ttu-id="f07e8-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="f07e8-112">**_Type_**</span></span> | <span data-ttu-id="f07e8-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="f07e8-113">Use</span></span> | <span data-ttu-id="f07e8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f07e8-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f07e8-115">**Personenzertifikatsentitätskennung**</span><span class="sxs-lookup"><span data-stu-id="f07e8-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="f07e8-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="f07e8-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="f07e8-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f07e8-117">*GUID*</span></span> | <span data-ttu-id="f07e8-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f07e8-118">Read-only</span></span><br><span data-ttu-id="f07e8-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-119">Required</span></span> | <span data-ttu-id="f07e8-120">Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz des Personenzertifikats.</span><span class="sxs-lookup"><span data-stu-id="f07e8-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="f07e8-121">**Parteinummer**</span><span class="sxs-lookup"><span data-stu-id="f07e8-121">**Party Number**</span></span><br><span data-ttu-id="f07e8-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="f07e8-122">mshr_partynumber</span></span><br><span data-ttu-id="f07e8-123">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f07e8-123">*String*</span></span> | <span data-ttu-id="f07e8-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f07e8-124">Read/write</span></span><br><span data-ttu-id="f07e8-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-125">Required</span></span> | <span data-ttu-id="f07e8-126">Die Partei-(Personen-)Kennung des Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="f07e8-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="f07e8-127">**Personenkennungswert**</span><span class="sxs-lookup"><span data-stu-id="f07e8-127">**Person ID Value**</span></span><br><span data-ttu-id="f07e8-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="f07e8-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="f07e8-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f07e8-129">*GUID*</span></span> | <span data-ttu-id="f07e8-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f07e8-130">Read-only</span></span><br><span data-ttu-id="f07e8-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-131">Required</span></span><br><span data-ttu-id="f07e8-132">Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="f07e8-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="f07e8-133">Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person).</span><span class="sxs-lookup"><span data-stu-id="f07e8-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="f07e8-134">**Zertifikatstypkennung**</span><span class="sxs-lookup"><span data-stu-id="f07e8-134">**Certificate Type ID**</span></span><br><span data-ttu-id="f07e8-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="f07e8-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="f07e8-136">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f07e8-136">*String*</span></span> | <span data-ttu-id="f07e8-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f07e8-137">Read/write</span></span><br><span data-ttu-id="f07e8-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-138">Required</span></span> |  <span data-ttu-id="f07e8-139">Der Bezeichner des Zertifikatstyps, der in Human Resources definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f07e8-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="f07e8-140">**Wert der Zertifikatstypkennung**</span><span class="sxs-lookup"><span data-stu-id="f07e8-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="f07e8-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="f07e8-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="f07e8-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f07e8-142">*GUID*</span></span> | <span data-ttu-id="f07e8-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f07e8-143">Read-only</span></span><br><span data-ttu-id="f07e8-144">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-144">Required</span></span><br><span data-ttu-id="f07e8-145">Fremdschlüssel: mshr_hcmcertificatetypeentityid von mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="f07e8-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="f07e8-146">Vom System generierter eindeutiger Bezeichner des Zertifikatstyps der zugeordneten Entität.</span><span class="sxs-lookup"><span data-stu-id="f07e8-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="f07e8-147">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="f07e8-147">**Start Date**</span></span><br><span data-ttu-id="f07e8-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="f07e8-148">mshr_startdate</span></span><br><span data-ttu-id="f07e8-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="f07e8-149">*Datetime*</span></span> | <span data-ttu-id="f07e8-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f07e8-150">Read/write</span></span><br><span data-ttu-id="f07e8-151">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-151">Required</span></span> | <span data-ttu-id="f07e8-152">Das Datum, an dem das Zertifikat ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f07e8-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="f07e8-153">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="f07e8-153">**End Date**</span></span><br><span data-ttu-id="f07e8-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="f07e8-154">mshr_enddate</span></span><br><span data-ttu-id="f07e8-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="f07e8-155">*Datetime*</span></span> | <span data-ttu-id="f07e8-156">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f07e8-156">Read/write</span></span><br><span data-ttu-id="f07e8-157">Optional</span><span class="sxs-lookup"><span data-stu-id="f07e8-157">Optional</span></span> | <span data-ttu-id="f07e8-158">Das Datum, an dem das Zertifikat abläuft.</span><span class="sxs-lookup"><span data-stu-id="f07e8-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="f07e8-159">**Notizen**</span><span class="sxs-lookup"><span data-stu-id="f07e8-159">**Notes**</span></span><br><span data-ttu-id="f07e8-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="f07e8-160">mshr_notes</span></span><br><span data-ttu-id="f07e8-161">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f07e8-161">*String*</span></span> | <span data-ttu-id="f07e8-162">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f07e8-162">Read/write</span></span><br><span data-ttu-id="f07e8-163">Optional</span><span class="sxs-lookup"><span data-stu-id="f07e8-163">Optional</span></span> | <span data-ttu-id="f07e8-164">Hinweise zur Verwendung durch den Personalbeschaffer oder Personalvermittler.</span><span class="sxs-lookup"><span data-stu-id="f07e8-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="f07e8-165">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="f07e8-165">**Primary Field**</span></span><br><span data-ttu-id="f07e8-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f07e8-166">mshr_primaryfield</span></span><br><span data-ttu-id="f07e8-167">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f07e8-167">*String*</span></span> | <span data-ttu-id="f07e8-168">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f07e8-168">Read-only</span></span><br><span data-ttu-id="f07e8-169">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f07e8-169">Required</span></span> |  <span data-ttu-id="f07e8-170">Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f07e8-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="f07e8-171">Kombination aus Parteinummer, Zertifikatstypkennung und Startdatum.</span><span class="sxs-lookup"><span data-stu-id="f07e8-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f07e8-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f07e8-172">See also</span></span>

[<span data-ttu-id="f07e8-173">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="f07e8-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f07e8-174">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="f07e8-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

