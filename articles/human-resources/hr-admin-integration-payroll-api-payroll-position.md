---
title: Lohndetails für Positionen
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019321"
---
# <a name="payroll-position"></a><span data-ttu-id="0d767-103">Lohnposition</span><span class="sxs-lookup"><span data-stu-id="0d767-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d767-104">Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0d767-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="0d767-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d767-105">Properties</span></span>

| <span data-ttu-id="0d767-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0d767-106">Property</span></span><br><span data-ttu-id="0d767-107">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="0d767-107">**Physical name**</span></span><br><span data-ttu-id="0d767-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="0d767-108">**_Type_**</span></span> | <span data-ttu-id="0d767-109">Verwenden</span><span class="sxs-lookup"><span data-stu-id="0d767-109">Use</span></span> | <span data-ttu-id="0d767-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d767-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0d767-111">**Normale Stunden pro Jahr**</span><span class="sxs-lookup"><span data-stu-id="0d767-111">**Annual regular hours**</span></span><br><span data-ttu-id="0d767-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="0d767-112">annualregularhours</span></span><br><span data-ttu-id="0d767-113">*Dezimal*</span><span class="sxs-lookup"><span data-stu-id="0d767-113">*Decimal*</span></span> | <span data-ttu-id="0d767-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-114">Read-only</span></span><br><span data-ttu-id="0d767-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-115">Required</span></span> | <span data-ttu-id="0d767-116">Für die Position festgelegte jährliche Regelarbeitszeit.</span><span class="sxs-lookup"><span data-stu-id="0d767-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="0d767-117">**ID Entität „Lohndetails für Position“**</span><span class="sxs-lookup"><span data-stu-id="0d767-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="0d767-118">Payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="0d767-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="0d767-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="0d767-119">*Guid*</span></span> | <span data-ttu-id="0d767-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-120">Required</span></span><br><span data-ttu-id="0d767-121">Vom System generiert.</span><span class="sxs-lookup"><span data-stu-id="0d767-121">System generated.</span></span> | <span data-ttu-id="0d767-122">Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Position.</span><span class="sxs-lookup"><span data-stu-id="0d767-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="0d767-123">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="0d767-123">**Primary field**</span></span><br><span data-ttu-id="0d767-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0d767-124">mshr_primaryfield</span></span><br><span data-ttu-id="0d767-125">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0d767-125">*String*</span></span> | <span data-ttu-id="0d767-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-126">Required</span></span><br><span data-ttu-id="0d767-127">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="0d767-127">System generated</span></span> |  |
| <span data-ttu-id="0d767-128">**Stellen-ID-Wert der Position**</span><span class="sxs-lookup"><span data-stu-id="0d767-128">**Position job ID value**</span></span><br><span data-ttu-id="0d767-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="0d767-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="0d767-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d767-130">*GUID*</span></span> | <span data-ttu-id="0d767-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-131">Read-only</span></span><br><span data-ttu-id="0d767-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-132">Required</span></span><br><span data-ttu-id="0d767-133">Fremdschlüssel: mshr_PayrollPositionJobEntity der mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="0d767-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="0d767-134">Die Kennung der Stelle, die der Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0d767-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="0d767-135">**ID-Wert für festen Vergütungsplan**</span><span class="sxs-lookup"><span data-stu-id="0d767-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="0d767-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="0d767-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="0d767-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d767-137">*GUID*</span></span> | <span data-ttu-id="0d767-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-138">Read-only</span></span><br><span data-ttu-id="0d767-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-139">Required</span></span><br><span data-ttu-id="0d767-140">Fremdschlüssel: mshr_FixedCompPlan_id von mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="0d767-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="0d767-141">Die Kennung des festen Vergütungsplans, der der Position zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0d767-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="0d767-142">**Lohnzyklus-ID**</span><span class="sxs-lookup"><span data-stu-id="0d767-142">**Pay cycle ID**</span></span><br><span data-ttu-id="0d767-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0d767-143">mshr_primaryfield</span></span><br><span data-ttu-id="0d767-144">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0d767-144">*String*</span></span> | <span data-ttu-id="0d767-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-145">Read-only</span></span><br><span data-ttu-id="0d767-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-146">Required</span></span> | <span data-ttu-id="0d767-147">Der auf der Position definierte Lohnzyklus.</span><span class="sxs-lookup"><span data-stu-id="0d767-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="0d767-148">**Gezahlt von juristischer Person**</span><span class="sxs-lookup"><span data-stu-id="0d767-148">**Paid by legal entity**</span></span><br><span data-ttu-id="0d767-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="0d767-149">paidbylegalentity</span></span><br><span data-ttu-id="0d767-150">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0d767-150">*String*</span></span> | <span data-ttu-id="0d767-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-151">Read-only</span></span><br><span data-ttu-id="0d767-152">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-152">Required</span></span> | <span data-ttu-id="0d767-153">Die juristische Person, die für die Zahlung für die Position verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="0d767-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="0d767-154">**Positionskennung**</span><span class="sxs-lookup"><span data-stu-id="0d767-154">**Position ID**</span></span><br><span data-ttu-id="0d767-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="0d767-155">mshr_positionid</span></span><br><span data-ttu-id="0d767-156">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0d767-156">*String*</span></span> | <span data-ttu-id="0d767-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-157">Read-only</span></span><br><span data-ttu-id="0d767-158">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-158">Required</span></span> | <span data-ttu-id="0d767-159">Die Kennung der Position.</span><span class="sxs-lookup"><span data-stu-id="0d767-159">The ID of the position.</span></span> |
| <span data-ttu-id="0d767-160">**Gültig bis**</span><span class="sxs-lookup"><span data-stu-id="0d767-160">**Valid to**</span></span><br><span data-ttu-id="0d767-161">validto</span><span class="sxs-lookup"><span data-stu-id="0d767-161">validto</span></span><br><span data-ttu-id="0d767-162">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="0d767-162">*Date Time Offset*</span></span> | <span data-ttu-id="0d767-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-163">Read-only</span></span><br><span data-ttu-id="0d767-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-164">Required</span></span> |<span data-ttu-id="0d767-165">Das Datum, ab dem die Positionsdetails gültig sind.</span><span class="sxs-lookup"><span data-stu-id="0d767-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="0d767-166">**Gültig ab**</span><span class="sxs-lookup"><span data-stu-id="0d767-166">**Valid from**</span></span><br><span data-ttu-id="0d767-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="0d767-167">validfrom</span></span><br><span data-ttu-id="0d767-168">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="0d767-168">*Date Time Offset*</span></span> | <span data-ttu-id="0d767-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d767-169">Read-only</span></span><br><span data-ttu-id="0d767-170">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0d767-170">Required</span></span> |<span data-ttu-id="0d767-171">Das Datum, bis zu dem die Positionsdetails gültig sind.</span><span class="sxs-lookup"><span data-stu-id="0d767-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="0d767-172">**Abfrage**</span><span class="sxs-lookup"><span data-stu-id="0d767-172">**Query**</span></span>

<span data-ttu-id="0d767-173">**Anforderung**</span><span class="sxs-lookup"><span data-stu-id="0d767-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="0d767-174">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="0d767-174">**Response**</span></span>

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
