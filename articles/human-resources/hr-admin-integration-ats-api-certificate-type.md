---
title: Bescheinigungstyp
description: In diesem Thema wird die Zertifikatstyp-Entität für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054691"
---
# <a name="certificate-type"></a><span data-ttu-id="a2137-103">Bescheinigungstyp</span><span class="sxs-lookup"><span data-stu-id="a2137-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a2137-104">In diesem Thema wird die Zertifikatstyp-Entität für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a2137-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a2137-105">Physischer Name: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="a2137-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="a2137-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2137-106">Description</span></span>

<span data-ttu-id="a2137-107">Diese Entität definiert die Liste der in Human Resources eingerichteten Berufszertifikatstypen.</span><span class="sxs-lookup"><span data-stu-id="a2137-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="a2137-108">Die Entität ist nicht spezifisch für eine juristische Person (Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="a2137-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="a2137-109">JSON-Darstellung</span><span class="sxs-lookup"><span data-stu-id="a2137-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="a2137-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2137-110">Properties</span></span>

| <span data-ttu-id="a2137-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2137-111">Property</span></span><br><span data-ttu-id="a2137-112">**Physikalischer Name**</span><span class="sxs-lookup"><span data-stu-id="a2137-112">**Physical name**</span></span><br><span data-ttu-id="a2137-113">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="a2137-113">**_Type_**</span></span> | <span data-ttu-id="a2137-114">Verwenden</span><span class="sxs-lookup"><span data-stu-id="a2137-114">Use</span></span> | <span data-ttu-id="a2137-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2137-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a2137-116">**Zertifikatstypentitätskennung**</span><span class="sxs-lookup"><span data-stu-id="a2137-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="a2137-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="a2137-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="a2137-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a2137-118">*GUID*</span></span> | <span data-ttu-id="a2137-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2137-119">Read-only</span></span><br><span data-ttu-id="a2137-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a2137-120">Required</span></span> 
<span data-ttu-id="a2137-121">Vom System generiert</span><span class="sxs-lookup"><span data-stu-id="a2137-121">System-generated</span></span> | <span data-ttu-id="a2137-122">Eindeutiger primärer Bezeichner für den Zertifikatstyp.</span><span class="sxs-lookup"><span data-stu-id="a2137-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="a2137-123">**Zertifikatstyp**</span><span class="sxs-lookup"><span data-stu-id="a2137-123">**Certificate Type**</span></span><br><span data-ttu-id="a2137-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="a2137-124">mshr_certificatetype</span></span><br><span data-ttu-id="a2137-125">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a2137-125">*String*</span></span> | <span data-ttu-id="a2137-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2137-126">Read/write</span></span><br><span data-ttu-id="a2137-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a2137-127">Required</span></span> | <span data-ttu-id="a2137-128">Eindeutiger vom Benutzer lesbarer Bezeichner für den Zertifikatstyp.</span><span class="sxs-lookup"><span data-stu-id="a2137-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="a2137-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a2137-129">**Description**</span></span><br><span data-ttu-id="a2137-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="a2137-130">mshr_description</span></span><br><span data-ttu-id="a2137-131">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a2137-131">*String*</span></span> | <span data-ttu-id="a2137-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2137-132">Read/write</span></span><br><span data-ttu-id="a2137-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a2137-133">Required</span></span> | <span data-ttu-id="a2137-134">Beschreibung des Zertifikatstyps.</span><span class="sxs-lookup"><span data-stu-id="a2137-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="a2137-135">**Erneuerung anfordern**</span><span class="sxs-lookup"><span data-stu-id="a2137-135">**Require Renewal**</span></span><br><span data-ttu-id="a2137-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="a2137-136">mshr_requirerenewal</span></span><br><span data-ttu-id="a2137-137">*mshr_noyes-Optionssatz*</span><span class="sxs-lookup"><span data-stu-id="a2137-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="a2137-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2137-138">Read/write</span></span><br><span data-ttu-id="a2137-139">Optional</span><span class="sxs-lookup"><span data-stu-id="a2137-139">Optional</span></span> | <span data-ttu-id="a2137-140">Gibt an, ob für das Zertifikat eine Erneuerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a2137-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a2137-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2137-141">See also</span></span>

[<span data-ttu-id="a2137-142">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="a2137-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a2137-143">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="a2137-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]