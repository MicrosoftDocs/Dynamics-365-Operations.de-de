---
title: Prüfungstypen
description: In diesem Thema wird die Screening-Typen-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126169"
---
# <a name="screening-types"></a><span data-ttu-id="248a3-103">Prüfungstypen</span><span class="sxs-lookup"><span data-stu-id="248a3-103">Screening types</span></span>

<span data-ttu-id="248a3-104">In diesem Thema wird die Screening-Typen-Entität für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="248a3-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="248a3-105">Physischer Name: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="248a3-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="248a3-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="248a3-106">Description</span></span>

<span data-ttu-id="248a3-107">Diese Einheit beschreibt die vom Unternehmen eingerichteten Screening-Typen vor der Einstellung und laufende Mitarbeiter-Screening-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="248a3-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="248a3-108">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="248a3-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="248a3-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="248a3-109">Properties</span></span>

| <span data-ttu-id="248a3-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="248a3-110">Property</span></span><br><span data-ttu-id="248a3-111">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="248a3-111">**Physical name**</span></span><br><span data-ttu-id="248a3-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="248a3-112">**_Type_**</span></span> | <span data-ttu-id="248a3-113">Verwenden</span><span class="sxs-lookup"><span data-stu-id="248a3-113">Use</span></span> | <span data-ttu-id="248a3-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="248a3-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="248a3-115">**Screening-Typ-Entitätskennung**</span><span class="sxs-lookup"><span data-stu-id="248a3-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="248a3-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="248a3-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="248a3-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="248a3-117">*GUID*</span></span> | <span data-ttu-id="248a3-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248a3-118">Read-only</span></span><br><span data-ttu-id="248a3-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="248a3-119">Required</span></span><br><span data-ttu-id="248a3-120">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="248a3-120">System-generated</span></span> | <span data-ttu-id="248a3-121">Eindeutiger primärer Bezeichner für den Screening-Typ-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="248a3-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="248a3-122">**Screening-Typ-Kennung**</span><span class="sxs-lookup"><span data-stu-id="248a3-122">**Screening Type ID**</span></span><br><span data-ttu-id="248a3-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="248a3-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="248a3-124">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="248a3-124">*String*</span></span> | <span data-ttu-id="248a3-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="248a3-125">Read/write</span></span><br><span data-ttu-id="248a3-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="248a3-126">Required</span></span> | <span data-ttu-id="248a3-127">Benutzerdefinierter eindeutiger Bezeichner für den Screening-Typ.</span><span class="sxs-lookup"><span data-stu-id="248a3-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="248a3-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="248a3-128">**Description**</span></span><br><span data-ttu-id="248a3-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="248a3-129">mshr_description</span></span><br><span data-ttu-id="248a3-130">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="248a3-130">*String*</span></span> | <span data-ttu-id="248a3-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="248a3-131">Read/write</span></span><br><span data-ttu-id="248a3-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="248a3-132">Required</span></span> | <span data-ttu-id="248a3-133">Die Beschreibung des Screening-Typs.</span><span class="sxs-lookup"><span data-stu-id="248a3-133">The description of the screening type.</span></span> |
| <span data-ttu-id="248a3-134">**Einheit der Häufigkeit**</span><span class="sxs-lookup"><span data-stu-id="248a3-134">**Frequency Unit**</span></span><br><span data-ttu-id="248a3-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="248a3-135">mshr_frequencyunit</span></span><br><span data-ttu-id="248a3-136">*mshr_hcmfrequencyunit-Optionssatz*</span><span class="sxs-lookup"><span data-stu-id="248a3-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="248a3-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="248a3-137">Read/write</span></span><br><span data-ttu-id="248a3-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="248a3-138">Required</span></span> | <span data-ttu-id="248a3-139">Beschreibt die Häufigkeit, mit der das Screening für die zugewiesene Person durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="248a3-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="248a3-140">**Formular erstellen**</span><span class="sxs-lookup"><span data-stu-id="248a3-140">**Generate From**</span></span><br><span data-ttu-id="248a3-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="248a3-141">mshr_generatefrom</span></span><br><span data-ttu-id="248a3-142">*mshr_hcmfrequencygeneratefrom-Optionssatz*</span><span class="sxs-lookup"><span data-stu-id="248a3-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="248a3-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="248a3-143">Read-write</span></span><br><span data-ttu-id="248a3-144">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="248a3-144">Required</span></span> | <span data-ttu-id="248a3-145">Wenn der Häufigkeitswert ein anderer Wert als „Nur einmalig“ ist, bestimmt der GenerateFrom-Wert das Datum, ab dem das nächste Screening-Ereignis berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="248a3-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="248a3-146">**Häufigkeitsintervall**</span><span class="sxs-lookup"><span data-stu-id="248a3-146">**Frequency Interval**</span></span><br><span data-ttu-id="248a3-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="248a3-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="248a3-148">*Ganzzahl*</span><span class="sxs-lookup"><span data-stu-id="248a3-148">*Integer*</span></span> | <span data-ttu-id="248a3-149">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="248a3-149">Read-write</span></span><br><span data-ttu-id="248a3-150">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="248a3-150">Required</span></span> | <span data-ttu-id="248a3-151">Wenn der Häufigkeitswert ein anderer Wert als „Nur einmalig“ ist, müssen Sie ein Intervall für die Zeiteinheiten zwischen den einzelnen Screening-Ereignissen definieren.</span><span class="sxs-lookup"><span data-stu-id="248a3-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="248a3-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="248a3-152">See also</span></span>

[<span data-ttu-id="248a3-153">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="248a3-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="248a3-154">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="248a3-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)