---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054955"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="71f59-103">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="71f59-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="71f59-104">Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="71f59-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="71f59-105">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="71f59-105">Key</span></span>

  | <span data-ttu-id="71f59-106">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="71f59-106">Property Name</span></span> | <span data-ttu-id="71f59-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="71f59-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="71f59-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="71f59-108">dataAreaId</span></span>    | <span data-ttu-id="71f59-109">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-109">String</span></span>    |
  | <span data-ttu-id="71f59-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="71f59-110">RequestId</span></span>     | <span data-ttu-id="71f59-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-111">String</span></span>    |
  | <span data-ttu-id="71f59-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="71f59-112">LeaveType</span></span>     | <span data-ttu-id="71f59-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-113">String</span></span>    |
  | <span data-ttu-id="71f59-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="71f59-114">LeaveDate</span></span>     | <span data-ttu-id="71f59-115">Datum</span><span class="sxs-lookup"><span data-stu-id="71f59-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="71f59-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71f59-116">Properties</span></span>

  | <span data-ttu-id="71f59-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="71f59-117">Property Name</span></span>     | <span data-ttu-id="71f59-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="71f59-118">Data Type</span></span> | <span data-ttu-id="71f59-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="71f59-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="71f59-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="71f59-120">dataAreaId</span></span>        | <span data-ttu-id="71f59-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-121">String</span></span>    | <span data-ttu-id="71f59-122">X</span><span class="sxs-lookup"><span data-stu-id="71f59-122">X</span></span>        |
  | <span data-ttu-id="71f59-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="71f59-123">RequestId</span></span>         | <span data-ttu-id="71f59-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-124">String</span></span>    | <span data-ttu-id="71f59-125">X</span><span class="sxs-lookup"><span data-stu-id="71f59-125">X</span></span>        |
  | <span data-ttu-id="71f59-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="71f59-126">LeaveType</span></span>         | <span data-ttu-id="71f59-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-127">String</span></span>    | <span data-ttu-id="71f59-128">X</span><span class="sxs-lookup"><span data-stu-id="71f59-128">X</span></span>        |
  | <span data-ttu-id="71f59-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="71f59-129">LeaveDate</span></span>         | <span data-ttu-id="71f59-130">Datum</span><span class="sxs-lookup"><span data-stu-id="71f59-130">Date</span></span>      | <span data-ttu-id="71f59-131">X</span><span class="sxs-lookup"><span data-stu-id="71f59-131">X</span></span>        |
  | <span data-ttu-id="71f59-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="71f59-132">ReasonCodeId</span></span>      | <span data-ttu-id="71f59-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-133">String</span></span>    |          |
  | <span data-ttu-id="71f59-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="71f59-134">PersonnelNumber</span></span>   | <span data-ttu-id="71f59-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-135">String</span></span>    | <span data-ttu-id="71f59-136">X</span><span class="sxs-lookup"><span data-stu-id="71f59-136">X</span></span>        |
  | <span data-ttu-id="71f59-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="71f59-137">RequestDate</span></span>       | <span data-ttu-id="71f59-138">Datum</span><span class="sxs-lookup"><span data-stu-id="71f59-138">Date</span></span>      | <span data-ttu-id="71f59-139">X</span><span class="sxs-lookup"><span data-stu-id="71f59-139">X</span></span>        |
  | <span data-ttu-id="71f59-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="71f59-140">Comment</span></span>           | <span data-ttu-id="71f59-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71f59-141">String</span></span>    |          |
  | <span data-ttu-id="71f59-142">Status</span><span class="sxs-lookup"><span data-stu-id="71f59-142">Status</span></span>            | <span data-ttu-id="71f59-143">Option</span><span class="sxs-lookup"><span data-stu-id="71f59-143">Enum</span></span>      | <span data-ttu-id="71f59-144">X</span><span class="sxs-lookup"><span data-stu-id="71f59-144">X</span></span>        |
  | <span data-ttu-id="71f59-145">Dauer</span><span class="sxs-lookup"><span data-stu-id="71f59-145">Amount</span></span>            | <span data-ttu-id="71f59-146">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="71f59-146">Real</span></span>      |          |
  | <span data-ttu-id="71f59-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="71f59-147">HalfDayDefinition</span></span> | <span data-ttu-id="71f59-148">Option</span><span class="sxs-lookup"><span data-stu-id="71f59-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="71f59-149">Aktionen</span><span class="sxs-lookup"><span data-stu-id="71f59-149">Actions</span></span>

 | <span data-ttu-id="71f59-150">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="71f59-150">Action Name</span></span>                               | <span data-ttu-id="71f59-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71f59-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="71f59-152">Übermitteln</span><span class="sxs-lookup"><span data-stu-id="71f59-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="71f59-153">Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="71f59-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="71f59-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71f59-154">See also</span></span>

- [<span data-ttu-id="71f59-155">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="71f59-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="71f59-156">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="71f59-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]