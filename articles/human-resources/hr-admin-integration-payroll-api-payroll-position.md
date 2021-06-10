---
title: Lohndetails für Positionen
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056779"
---
# <a name="payroll-position"></a><span data-ttu-id="0e3bb-103">Lohnposition</span><span class="sxs-lookup"><span data-stu-id="0e3bb-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0e3bb-104">Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="0e3bb-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e3bb-105">Properties</span></span>

| <span data-ttu-id="0e3bb-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0e3bb-106">Property</span></span><br><span data-ttu-id="0e3bb-107">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-107">**Physical name**</span></span><br><span data-ttu-id="0e3bb-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-108">**_Type_**</span></span> | <span data-ttu-id="0e3bb-109">Verwenden</span><span class="sxs-lookup"><span data-stu-id="0e3bb-109">Use</span></span> | <span data-ttu-id="0e3bb-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e3bb-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0e3bb-111">**Normale Stunden pro Jahr**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-111">**Annual regular hours**</span></span><br><span data-ttu-id="0e3bb-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="0e3bb-112">annualregularhours</span></span><br><span data-ttu-id="0e3bb-113">*Dezimal*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-113">*Decimal*</span></span> | <span data-ttu-id="0e3bb-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-114">Read-only</span></span><br><span data-ttu-id="0e3bb-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-115">Required</span></span> | <span data-ttu-id="0e3bb-116">Für die Position festgelegte jährliche Regelarbeitszeit.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="0e3bb-117">**ID Entität „Lohndetails für Position“**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="0e3bb-118">Payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="0e3bb-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="0e3bb-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-119">*Guid*</span></span> | <span data-ttu-id="0e3bb-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-120">Required</span></span><br><span data-ttu-id="0e3bb-121">Vom System generiert.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-121">System generated.</span></span> | <span data-ttu-id="0e3bb-122">Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Position.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="0e3bb-123">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-123">**Primary field**</span></span><br><span data-ttu-id="0e3bb-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0e3bb-124">mshr_primaryfield</span></span><br><span data-ttu-id="0e3bb-125">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-125">*String*</span></span> | <span data-ttu-id="0e3bb-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-126">Required</span></span><br><span data-ttu-id="0e3bb-127">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="0e3bb-127">System generated</span></span> |  |
| <span data-ttu-id="0e3bb-128">**Stellen-ID-Wert der Position**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-128">**Position job ID value**</span></span><br><span data-ttu-id="0e3bb-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="0e3bb-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="0e3bb-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-130">*GUID*</span></span> | <span data-ttu-id="0e3bb-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-131">Read-only</span></span><br><span data-ttu-id="0e3bb-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-132">Required</span></span><br><span data-ttu-id="0e3bb-133">Fremdschlüssel: mshr_PayrollPositionJobEntity der mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="0e3bb-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="0e3bb-134">Die Kennung der Stelle, die der Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="0e3bb-135">**ID-Wert für festen Vergütungsplan**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="0e3bb-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="0e3bb-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="0e3bb-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-137">*GUID*</span></span> | <span data-ttu-id="0e3bb-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-138">Read-only</span></span><br><span data-ttu-id="0e3bb-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-139">Required</span></span><br><span data-ttu-id="0e3bb-140">Fremdschlüssel: mshr_FixedCompPlan_id von mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="0e3bb-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="0e3bb-141">Die Kennung des festen Vergütungsplans, der der Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="0e3bb-142">**Lohnzyklus-ID**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-142">**Pay cycle ID**</span></span><br><span data-ttu-id="0e3bb-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0e3bb-143">mshr_primaryfield</span></span><br><span data-ttu-id="0e3bb-144">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-144">*String*</span></span> | <span data-ttu-id="0e3bb-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-145">Read-only</span></span><br><span data-ttu-id="0e3bb-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-146">Required</span></span> | <span data-ttu-id="0e3bb-147">Der auf der Position definierte Lohnzyklus.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="0e3bb-148">**Gezahlt von juristischer Person**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-148">**Paid by legal entity**</span></span><br><span data-ttu-id="0e3bb-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="0e3bb-149">paidbylegalentity</span></span><br><span data-ttu-id="0e3bb-150">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-150">*String*</span></span> | <span data-ttu-id="0e3bb-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-151">Read-only</span></span><br><span data-ttu-id="0e3bb-152">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-152">Required</span></span> | <span data-ttu-id="0e3bb-153">Die juristische Person, die für die Zahlung für die Position verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="0e3bb-154">**Positionskennung**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-154">**Position ID**</span></span><br><span data-ttu-id="0e3bb-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="0e3bb-155">mshr_positionid</span></span><br><span data-ttu-id="0e3bb-156">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-156">*String*</span></span> | <span data-ttu-id="0e3bb-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-157">Read-only</span></span><br><span data-ttu-id="0e3bb-158">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-158">Required</span></span> | <span data-ttu-id="0e3bb-159">Die Kennung der Position.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-159">The ID of the position.</span></span> |
| <span data-ttu-id="0e3bb-160">**Gültig bis**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-160">**Valid to**</span></span><br><span data-ttu-id="0e3bb-161">validto</span><span class="sxs-lookup"><span data-stu-id="0e3bb-161">validto</span></span><br><span data-ttu-id="0e3bb-162">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-162">*Date Time Offset*</span></span> | <span data-ttu-id="0e3bb-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-163">Read-only</span></span><br><span data-ttu-id="0e3bb-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-164">Required</span></span> |<span data-ttu-id="0e3bb-165">Das Datum, ab dem die Positionsdetails gültig sind.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="0e3bb-166">**Gültig ab**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-166">**Valid from**</span></span><br><span data-ttu-id="0e3bb-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="0e3bb-167">validfrom</span></span><br><span data-ttu-id="0e3bb-168">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="0e3bb-168">*Date Time Offset*</span></span> | <span data-ttu-id="0e3bb-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e3bb-169">Read-only</span></span><br><span data-ttu-id="0e3bb-170">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e3bb-170">Required</span></span> |<span data-ttu-id="0e3bb-171">Das Datum, bis zu dem die Positionsdetails gültig sind.</span><span class="sxs-lookup"><span data-stu-id="0e3bb-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="0e3bb-172">**Abfrage**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-172">**Query**</span></span>

<span data-ttu-id="0e3bb-173">**Anforderung**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="0e3bb-174">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="0e3bb-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
