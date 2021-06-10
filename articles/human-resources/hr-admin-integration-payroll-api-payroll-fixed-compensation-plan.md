---
title: Fester Vergütungsplan für Lohnabrechnung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Fester Vergütungsplan für Lohnabrechnung“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059087"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="e21d1-103">Fester Vergütungsplan für Lohnabrechnung</span><span class="sxs-lookup"><span data-stu-id="e21d1-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e21d1-104">Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Fester Vergütungsplan für Lohnabrechnung“ in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e21d1-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e21d1-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e21d1-105">Properties</span></span>

| <span data-ttu-id="e21d1-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e21d1-106">Property</span></span><br><span data-ttu-id="e21d1-107">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="e21d1-107">**Physical name**</span></span><br><span data-ttu-id="e21d1-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="e21d1-108">**_Type_**</span></span> | <span data-ttu-id="e21d1-109">Verwenden</span><span class="sxs-lookup"><span data-stu-id="e21d1-109">Use</span></span> | <span data-ttu-id="e21d1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e21d1-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e21d1-111">**Mitarbeiterkennung**</span><span class="sxs-lookup"><span data-stu-id="e21d1-111">**Employee ID**</span></span><br><span data-ttu-id="e21d1-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="e21d1-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="e21d1-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e21d1-113">*GUID*</span></span> | <span data-ttu-id="e21d1-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-114">Read-only</span></span><br><span data-ttu-id="e21d1-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-115">Required</span></span><br><span data-ttu-id="e21d1-116">Fremdschlüssel: mshr_Employee_id von mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="e21d1-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="e21d1-117">Mitarbeiterkennung</span><span class="sxs-lookup"><span data-stu-id="e21d1-117">Employee ID</span></span> |
| <span data-ttu-id="e21d1-118">**Lohnsatz**</span><span class="sxs-lookup"><span data-stu-id="e21d1-118">**Pay rate**</span></span><br><span data-ttu-id="e21d1-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="e21d1-119">mshr_payrate</span></span><br><span data-ttu-id="e21d1-120">*Dezimal*</span><span class="sxs-lookup"><span data-stu-id="e21d1-120">*Decimal*</span></span> | <span data-ttu-id="e21d1-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-121">Read-only</span></span><br><span data-ttu-id="e21d1-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-122">Required</span></span> | <span data-ttu-id="e21d1-123">Im festen Vergütungsplan definierter Lohnsatz.</span><span class="sxs-lookup"><span data-stu-id="e21d1-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="e21d1-124">**Plankennung**</span><span class="sxs-lookup"><span data-stu-id="e21d1-124">**Plan ID**</span></span><br><span data-ttu-id="e21d1-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="e21d1-125">mshr_planid</span></span><br><span data-ttu-id="e21d1-126">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e21d1-126">*String*</span></span> | <span data-ttu-id="e21d1-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-127">Read-only</span></span><br><span data-ttu-id="e21d1-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-128">Required</span></span> |<span data-ttu-id="e21d1-129">Gibt den Vergütungsplan an.</span><span class="sxs-lookup"><span data-stu-id="e21d1-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="e21d1-130">**Gültig ab**</span><span class="sxs-lookup"><span data-stu-id="e21d1-130">**Valid from**</span></span><br><span data-ttu-id="e21d1-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="e21d1-131">mshr_validfrom</span></span><br><span data-ttu-id="e21d1-132">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="e21d1-132">*Date Time Offset*</span></span> |  <span data-ttu-id="e21d1-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-133">Read-only</span></span><br><span data-ttu-id="e21d1-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-134">Required</span></span> |<span data-ttu-id="e21d1-135">Datum, ab dem der feste Vergütungsplan für den Mitarbeiter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="e21d1-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="e21d1-136">**Entität „Fester Vergütungsplan für Lohnabrechnung“**</span><span class="sxs-lookup"><span data-stu-id="e21d1-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="e21d1-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="e21d1-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="e21d1-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e21d1-138">*GUID*</span></span> | <span data-ttu-id="e21d1-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-139">Required</span></span><br><span data-ttu-id="e21d1-140">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="e21d1-140">Sytem generated</span></span> | <span data-ttu-id="e21d1-141">Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Vergütungsplans.</span><span class="sxs-lookup"><span data-stu-id="e21d1-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="e21d1-142">**Lohnzahlungshäufigkeit**</span><span class="sxs-lookup"><span data-stu-id="e21d1-142">**Pay frequency**</span></span><br><span data-ttu-id="e21d1-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="e21d1-143">mshr_payfrequency</span></span><br><span data-ttu-id="e21d1-144">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e21d1-144">*String*</span></span> | <span data-ttu-id="e21d1-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-145">Read-only</span></span><br><span data-ttu-id="e21d1-146">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-146">Required</span></span> |<span data-ttu-id="e21d1-147">Die Häufigkeit, mit der der Mitarbeiter bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="e21d1-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="e21d1-148">**Gültig bis**</span><span class="sxs-lookup"><span data-stu-id="e21d1-148">**Valid to**</span></span><br><span data-ttu-id="e21d1-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="e21d1-149">mshr_validto</span></span><br><span data-ttu-id="e21d1-150">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="e21d1-150">*Date Time Offset*</span></span> | <span data-ttu-id="e21d1-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-151">Read-only</span></span> <br><span data-ttu-id="e21d1-152">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-152">Required</span></span> | <span data-ttu-id="e21d1-153">Datum, bis zu dem der feste Vergütungsplan für den Mitarbeiter gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e21d1-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="e21d1-154">**Positionskennung**</span><span class="sxs-lookup"><span data-stu-id="e21d1-154">**Position ID**</span></span><br><span data-ttu-id="e21d1-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="e21d1-155">mshr_positionid</span></span><br><span data-ttu-id="e21d1-156">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e21d1-156">*String*</span></span> | <span data-ttu-id="e21d1-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-157">Read-only</span></span> <br><span data-ttu-id="e21d1-158">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-158">Required</span></span> | <span data-ttu-id="e21d1-159">Positionskennung, die mit dem Mitarbeiter und dem Beitritt zum festen Vergütungsplan verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e21d1-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="e21d1-160">**Währung**</span><span class="sxs-lookup"><span data-stu-id="e21d1-160">**Currency**</span></span><br><span data-ttu-id="e21d1-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="e21d1-161">mshr_currency</span></span><br><span data-ttu-id="e21d1-162">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e21d1-162">*String*</span></span> | <span data-ttu-id="e21d1-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-163">Read-only</span></span> <br><span data-ttu-id="e21d1-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-164">Required</span></span> |<span data-ttu-id="e21d1-165">Die für den festen Vergütungsplan definierte Währung</span><span class="sxs-lookup"><span data-stu-id="e21d1-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="e21d1-166">**Personalnummer**</span><span class="sxs-lookup"><span data-stu-id="e21d1-166">**Personnel number**</span></span><br><span data-ttu-id="e21d1-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="e21d1-167">mshr_personnelnumber</span></span><br><span data-ttu-id="e21d1-168">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e21d1-168">*String*</span></span> | <span data-ttu-id="e21d1-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e21d1-169">Read-only</span></span><br><span data-ttu-id="e21d1-170">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e21d1-170">Required</span></span> |<span data-ttu-id="e21d1-171">Die eindeutige Personalnummer des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="e21d1-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="e21d1-172">**Abfrage**</span><span class="sxs-lookup"><span data-stu-id="e21d1-172">**Query**</span></span>

<span data-ttu-id="e21d1-173">**Anforderung**</span><span class="sxs-lookup"><span data-stu-id="e21d1-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="e21d1-174">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="e21d1-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
