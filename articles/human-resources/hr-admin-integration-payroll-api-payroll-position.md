---
title: Lohndetails für Positionen
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881988"
---
# <a name="payroll-position"></a><span data-ttu-id="25208-103">Lohnposition</span><span class="sxs-lookup"><span data-stu-id="25208-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="25208-104">Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="25208-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="25208-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25208-105">Properties</span></span>

| <span data-ttu-id="25208-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="25208-106">Property</span></span><br><span data-ttu-id="25208-107">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="25208-107">**Physical name**</span></span><br><span data-ttu-id="25208-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="25208-108">**_Type_**</span></span> | <span data-ttu-id="25208-109">Verwenden</span><span class="sxs-lookup"><span data-stu-id="25208-109">Use</span></span> | <span data-ttu-id="25208-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25208-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="25208-111">**Normale Stunden pro Jahr**</span><span class="sxs-lookup"><span data-stu-id="25208-111">**Annual regular hours**</span></span><br><span data-ttu-id="25208-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="25208-112">annualregularhours</span></span><br><span data-ttu-id="25208-113">*Dezimal*</span><span class="sxs-lookup"><span data-stu-id="25208-113">*Decimal*</span></span> | <span data-ttu-id="25208-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-114">Read-only</span></span><br><span data-ttu-id="25208-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-115">Required</span></span> | <span data-ttu-id="25208-116">Für die Position festgelegte jährliche Regelarbeitszeit.</span><span class="sxs-lookup"><span data-stu-id="25208-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="25208-117">**ID Entität „Lohndetails für Position“**</span><span class="sxs-lookup"><span data-stu-id="25208-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="25208-118">Payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="25208-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="25208-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="25208-119">*Guid*</span></span> | <span data-ttu-id="25208-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-120">Required</span></span><br><span data-ttu-id="25208-121">Vom System generiert.</span><span class="sxs-lookup"><span data-stu-id="25208-121">System generated.</span></span> | <span data-ttu-id="25208-122">Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Position.</span><span class="sxs-lookup"><span data-stu-id="25208-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="25208-123">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="25208-123">**Primary field**</span></span><br><span data-ttu-id="25208-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="25208-124">mshr_primaryfield</span></span><br><span data-ttu-id="25208-125">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="25208-125">*String*</span></span> | <span data-ttu-id="25208-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-126">Required</span></span><br><span data-ttu-id="25208-127">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="25208-127">System generated</span></span> |  |
| <span data-ttu-id="25208-128">**Stellen-ID-Wert der Position**</span><span class="sxs-lookup"><span data-stu-id="25208-128">**Position job ID value**</span></span><br><span data-ttu-id="25208-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="25208-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="25208-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="25208-130">*GUID*</span></span> | <span data-ttu-id="25208-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-131">Read-only</span></span><br><span data-ttu-id="25208-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-132">Required</span></span><br><span data-ttu-id="25208-133">Fremdschlüssel: mshr_PayrollPositionJobEntity der mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="25208-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="25208-134">Die Kennung der Stelle, die der Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="25208-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="25208-135">**ID-Wert für festen Vergütungsplan**</span><span class="sxs-lookup"><span data-stu-id="25208-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="25208-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="25208-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="25208-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="25208-137">*GUID*</span></span> | <span data-ttu-id="25208-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-138">Read-only</span></span><br><span data-ttu-id="25208-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-139">Required</span></span><br><span data-ttu-id="25208-140">Fremdschlüssel: mshr_FixedCompPlan_id von mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="25208-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="25208-141">Die Kennung des festen Vergütungsplans, der der Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="25208-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="25208-142">**Lohnzyklus-ID**</span><span class="sxs-lookup"><span data-stu-id="25208-142">**Pay cycle ID**</span></span><br><span data-ttu-id="25208-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="25208-143">mshr_primaryfield</span></span><br><span data-ttu-id="25208-144">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="25208-144">*String*</span></span> | <span data-ttu-id="25208-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-145">Read-only</span></span><br><span data-ttu-id="25208-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-146">Required</span></span> | <span data-ttu-id="25208-147">Der auf der Position definierte Lohnzyklus.</span><span class="sxs-lookup"><span data-stu-id="25208-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="25208-148">**Gezahlt von juristischer Person**</span><span class="sxs-lookup"><span data-stu-id="25208-148">**Paid by legal entity**</span></span><br><span data-ttu-id="25208-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="25208-149">paidbylegalentity</span></span><br><span data-ttu-id="25208-150">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="25208-150">*String*</span></span> | <span data-ttu-id="25208-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-151">Read-only</span></span><br><span data-ttu-id="25208-152">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-152">Required</span></span> | <span data-ttu-id="25208-153">Die juristische Person, die für die Zahlung für die Position verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="25208-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="25208-154">**Positionskennung**</span><span class="sxs-lookup"><span data-stu-id="25208-154">**Position ID**</span></span><br><span data-ttu-id="25208-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="25208-155">mshr_positionid</span></span><br><span data-ttu-id="25208-156">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="25208-156">*String*</span></span> | <span data-ttu-id="25208-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-157">Read-only</span></span><br><span data-ttu-id="25208-158">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-158">Required</span></span> | <span data-ttu-id="25208-159">Die Kennung der Position.</span><span class="sxs-lookup"><span data-stu-id="25208-159">The ID of the position.</span></span> |
| <span data-ttu-id="25208-160">**Gültig bis**</span><span class="sxs-lookup"><span data-stu-id="25208-160">**Valid to**</span></span><br><span data-ttu-id="25208-161">validto</span><span class="sxs-lookup"><span data-stu-id="25208-161">validto</span></span><br><span data-ttu-id="25208-162">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="25208-162">*Date Time Offset*</span></span> | <span data-ttu-id="25208-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-163">Read-only</span></span><br><span data-ttu-id="25208-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-164">Required</span></span> |<span data-ttu-id="25208-165">Das Datum, ab dem die Positionsdetails gültig sind.</span><span class="sxs-lookup"><span data-stu-id="25208-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="25208-166">**Gültig ab**</span><span class="sxs-lookup"><span data-stu-id="25208-166">**Valid from**</span></span><br><span data-ttu-id="25208-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="25208-167">validfrom</span></span><br><span data-ttu-id="25208-168">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="25208-168">*Date Time Offset*</span></span> | <span data-ttu-id="25208-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25208-169">Read-only</span></span><br><span data-ttu-id="25208-170">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="25208-170">Required</span></span> |<span data-ttu-id="25208-171">Das Datum, bis zu dem die Positionsdetails gültig sind.</span><span class="sxs-lookup"><span data-stu-id="25208-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="25208-172">**Abfrage**</span><span class="sxs-lookup"><span data-stu-id="25208-172">**Query**</span></span>

<span data-ttu-id="25208-173">**Anforderung**</span><span class="sxs-lookup"><span data-stu-id="25208-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="25208-174">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="25208-174">**Response**</span></span>

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
