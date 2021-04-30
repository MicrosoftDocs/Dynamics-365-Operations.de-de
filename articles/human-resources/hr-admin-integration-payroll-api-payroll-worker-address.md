---
title: Lohn – Adresse der Arbeitskraft
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Adresse der Arbeitskraft“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881990"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="a49db-103">Lohn – Adresse der Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="a49db-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a49db-104">Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Adresse der Arbeitskraft“ in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a49db-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="a49db-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49db-105">Properties</span></span>

| <span data-ttu-id="a49db-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a49db-106">Property</span></span><br><span data-ttu-id="a49db-107">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="a49db-107">**Physical name**</span></span><br><span data-ttu-id="a49db-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="a49db-108">**_Type_**</span></span> | <span data-ttu-id="a49db-109">Verwenden</span><span class="sxs-lookup"><span data-stu-id="a49db-109">Use</span></span> | <span data-ttu-id="a49db-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a49db-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a49db-111">**Ort**</span><span class="sxs-lookup"><span data-stu-id="a49db-111">**City**</span></span><br><span data-ttu-id="a49db-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="a49db-112">mshr_city</span></span><br><span data-ttu-id="a49db-113">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-113">*String*</span></span> | <span data-ttu-id="a49db-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-114">Read-only</span></span><br><span data-ttu-id="a49db-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-115">Required</span></span> | <span data-ttu-id="a49db-116">Die für die Adresse festgelegte Stadt.</span><span class="sxs-lookup"><span data-stu-id="a49db-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="a49db-117">**Personalnummer**</span><span class="sxs-lookup"><span data-stu-id="a49db-117">**Personnel number**</span></span><br><span data-ttu-id="a49db-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="a49db-118">mshr_personnelnumber</span></span><br><span data-ttu-id="a49db-119">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-119">*String*</span></span> | <span data-ttu-id="a49db-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-120">Read-only</span></span><br><span data-ttu-id="a49db-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-121">Required</span></span> | <span data-ttu-id="a49db-122">Die eindeutige Personalnummer des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="a49db-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="a49db-123">**Land bzw Region**</span><span class="sxs-lookup"><span data-stu-id="a49db-123">**Country region**</span></span><br><span data-ttu-id="a49db-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="a49db-124">mshr_countryregionid</span></span><br><span data-ttu-id="a49db-125">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-125">*String*</span></span> | <span data-ttu-id="a49db-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-126">Read-only</span></span><br><span data-ttu-id="a49db-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-127">Required</span></span> | <span data-ttu-id="a49db-128">Das für die Adresse festgelegte Land bzw. die Region</span><span class="sxs-lookup"><span data-stu-id="a49db-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="a49db-129">**Gültig ab**</span><span class="sxs-lookup"><span data-stu-id="a49db-129">**Valid from**</span></span><br><span data-ttu-id="a49db-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="a49db-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="a49db-131">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="a49db-131">*Date Time Offset*</span></span> | <span data-ttu-id="a49db-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-132">Read-only</span></span> <br><span data-ttu-id="a49db-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-133">Required</span></span> | <span data-ttu-id="a49db-134">Das Datum, ab dem die Adresse gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a49db-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="a49db-135">**Arbeitsadresse**</span><span class="sxs-lookup"><span data-stu-id="a49db-135">**Worked in address**</span></span><br><span data-ttu-id="a49db-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="a49db-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="a49db-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-137">Read-only</span></span><br><span data-ttu-id="a49db-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-138">Required</span></span> | <span data-ttu-id="a49db-139">Gibt an, ob die Adresse der Ort ist, an dem der Mitarbeiter arbeitet.</span><span class="sxs-lookup"><span data-stu-id="a49db-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="a49db-140">**Landkreis**</span><span class="sxs-lookup"><span data-stu-id="a49db-140">**County**</span></span><br><span data-ttu-id="a49db-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="a49db-141">mshr_county</span></span><br><span data-ttu-id="a49db-142">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-142">*String*</span></span> | <span data-ttu-id="a49db-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-143">Read-only</span></span><br><span data-ttu-id="a49db-144">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-144">Required</span></span> | <span data-ttu-id="a49db-145">Der für die Adresse festgelegte Landkreis.</span><span class="sxs-lookup"><span data-stu-id="a49db-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="a49db-146">**ID der Adresse der Arbeitskraft**</span><span class="sxs-lookup"><span data-stu-id="a49db-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="a49db-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="a49db-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="a49db-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a49db-148">*GUID*</span></span> | <span data-ttu-id="a49db-149">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-149">Required</span></span><br><span data-ttu-id="a49db-150">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="a49db-150">System generated</span></span> | <span data-ttu-id="a49db-151">Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Adresse.</span><span class="sxs-lookup"><span data-stu-id="a49db-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="a49db-152">**Primärfeld**</span><span class="sxs-lookup"><span data-stu-id="a49db-152">**Primary field**</span></span><br><span data-ttu-id="a49db-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a49db-153">mshr_primaryfield</span></span><br><span data-ttu-id="a49db-154">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-154">*String*</span></span> | <span data-ttu-id="a49db-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-155">Read-only</span></span><br><span data-ttu-id="a49db-156">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-156">Required</span></span> |  |
| <span data-ttu-id="a49db-157">**Straße**</span><span class="sxs-lookup"><span data-stu-id="a49db-157">**Street**</span></span><br><span data-ttu-id="a49db-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="a49db-158">mshr_street</span></span><br><span data-ttu-id="a49db-159">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-159">*String*</span></span> | <span data-ttu-id="a49db-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-160">Read-only</span></span><br><span data-ttu-id="a49db-161">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-161">Required</span></span> | <span data-ttu-id="a49db-162">Der für die Adresse festgelegte Straße.</span><span class="sxs-lookup"><span data-stu-id="a49db-162">The street defined for the address.</span></span> |
| <span data-ttu-id="a49db-163">**Gültig bis**</span><span class="sxs-lookup"><span data-stu-id="a49db-163">**Valid to**</span></span><br><span data-ttu-id="a49db-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="a49db-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="a49db-165">*Datum-/Uhrzeit-Offset*</span><span class="sxs-lookup"><span data-stu-id="a49db-165">*Date Time Offset*</span></span> | <span data-ttu-id="a49db-166">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-166">Read-only</span></span> <br><span data-ttu-id="a49db-167">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-167">Required</span></span> | <span data-ttu-id="a49db-168">Das Datum, bis zu dem die Adresse gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a49db-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="a49db-169">**Lagerplatzkennung**</span><span class="sxs-lookup"><span data-stu-id="a49db-169">**Location ID**</span></span><br><span data-ttu-id="a49db-170">mshr_locationidbr>*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="a49db-171">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-171">Read-only</span></span> <br><span data-ttu-id="a49db-172">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-172">Required</span></span> | <span data-ttu-id="a49db-173">Die Kennung für Adresse.</span><span class="sxs-lookup"><span data-stu-id="a49db-173">The ID for the address.</span></span>  |
| <span data-ttu-id="a49db-174">**PLZ**</span><span class="sxs-lookup"><span data-stu-id="a49db-174">**Postal code**</span></span><br><span data-ttu-id="a49db-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="a49db-175">mshr_zipcode</span></span><br><span data-ttu-id="a49db-176">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-176">*String*</span></span> | <span data-ttu-id="a49db-177">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-177">Read-only</span></span> <br><span data-ttu-id="a49db-178">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-178">Required</span></span> |<span data-ttu-id="a49db-179">Die für den Mitarbeiter festgelegte Kennungsnummer.</span><span class="sxs-lookup"><span data-stu-id="a49db-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="a49db-180">**Wohnadresse**</span><span class="sxs-lookup"><span data-stu-id="a49db-180">**Lived in address**</span></span><br><span data-ttu-id="a49db-181">mshr_islivedinaddressbr>*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="a49db-182">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-182">Read-only</span></span><br><span data-ttu-id="a49db-183">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-183">Required</span></span> | <span data-ttu-id="a49db-184">Gibt an, ob die Adresse der Ort ist, an dem der Mitarbeiter wohnt.</span><span class="sxs-lookup"><span data-stu-id="a49db-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="a49db-185">**Bundesstaat**</span><span class="sxs-lookup"><span data-stu-id="a49db-185">**State**</span></span><br><span data-ttu-id="a49db-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="a49db-186">mshr_state</span></span><br><span data-ttu-id="a49db-187">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a49db-187">*String*</span></span> | <span data-ttu-id="a49db-188">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a49db-188">Read-only</span></span><br><span data-ttu-id="a49db-189">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a49db-189">Required</span></span> | <span data-ttu-id="a49db-190">Der für die Adresse festgelegte Bundesstaat.</span><span class="sxs-lookup"><span data-stu-id="a49db-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="a49db-191">Beispielabfrage</span><span class="sxs-lookup"><span data-stu-id="a49db-191">Example query</span></span>

<span data-ttu-id="a49db-192">**Anforderung**</span><span class="sxs-lookup"><span data-stu-id="a49db-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="a49db-193">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="a49db-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
