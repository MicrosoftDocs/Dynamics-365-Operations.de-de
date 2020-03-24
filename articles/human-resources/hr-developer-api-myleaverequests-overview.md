---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092036"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="6168e-103">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="6168e-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="6168e-104">Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6168e-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="6168e-105">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6168e-105">Key</span></span>

  | <span data-ttu-id="6168e-106">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6168e-106">Property Name</span></span> | <span data-ttu-id="6168e-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6168e-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="6168e-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="6168e-108">dataAreaId</span></span>    | <span data-ttu-id="6168e-109">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-109">String</span></span>    |
  | <span data-ttu-id="6168e-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="6168e-110">RequestId</span></span>     | <span data-ttu-id="6168e-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-111">String</span></span>    |
  | <span data-ttu-id="6168e-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="6168e-112">LeaveType</span></span>     | <span data-ttu-id="6168e-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-113">String</span></span>    |
  | <span data-ttu-id="6168e-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="6168e-114">LeaveDate</span></span>     | <span data-ttu-id="6168e-115">Datum</span><span class="sxs-lookup"><span data-stu-id="6168e-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="6168e-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6168e-116">Properties</span></span>

  | <span data-ttu-id="6168e-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6168e-117">Property Name</span></span>     | <span data-ttu-id="6168e-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6168e-118">Data Type</span></span> | <span data-ttu-id="6168e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6168e-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="6168e-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="6168e-120">dataAreaId</span></span>        | <span data-ttu-id="6168e-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-121">String</span></span>    | <span data-ttu-id="6168e-122">X</span><span class="sxs-lookup"><span data-stu-id="6168e-122">X</span></span>        |
  | <span data-ttu-id="6168e-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="6168e-123">RequestId</span></span>         | <span data-ttu-id="6168e-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-124">String</span></span>    | <span data-ttu-id="6168e-125">X</span><span class="sxs-lookup"><span data-stu-id="6168e-125">X</span></span>        |
  | <span data-ttu-id="6168e-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="6168e-126">LeaveType</span></span>         | <span data-ttu-id="6168e-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-127">String</span></span>    | <span data-ttu-id="6168e-128">X</span><span class="sxs-lookup"><span data-stu-id="6168e-128">X</span></span>        |
  | <span data-ttu-id="6168e-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="6168e-129">LeaveDate</span></span>         | <span data-ttu-id="6168e-130">Datum</span><span class="sxs-lookup"><span data-stu-id="6168e-130">Date</span></span>      | <span data-ttu-id="6168e-131">X</span><span class="sxs-lookup"><span data-stu-id="6168e-131">X</span></span>        |
  | <span data-ttu-id="6168e-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="6168e-132">ReasonCodeId</span></span>      | <span data-ttu-id="6168e-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-133">String</span></span>    |          |
  | <span data-ttu-id="6168e-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="6168e-134">PersonnelNumber</span></span>   | <span data-ttu-id="6168e-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-135">String</span></span>    | <span data-ttu-id="6168e-136">X</span><span class="sxs-lookup"><span data-stu-id="6168e-136">X</span></span>        |
  | <span data-ttu-id="6168e-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="6168e-137">RequestDate</span></span>       | <span data-ttu-id="6168e-138">Datum</span><span class="sxs-lookup"><span data-stu-id="6168e-138">Date</span></span>      | <span data-ttu-id="6168e-139">X</span><span class="sxs-lookup"><span data-stu-id="6168e-139">X</span></span>        |
  | <span data-ttu-id="6168e-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="6168e-140">Comment</span></span>           | <span data-ttu-id="6168e-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6168e-141">String</span></span>    |          |
  | <span data-ttu-id="6168e-142">Status</span><span class="sxs-lookup"><span data-stu-id="6168e-142">Status</span></span>            | <span data-ttu-id="6168e-143">Option</span><span class="sxs-lookup"><span data-stu-id="6168e-143">Enum</span></span>      | <span data-ttu-id="6168e-144">X</span><span class="sxs-lookup"><span data-stu-id="6168e-144">X</span></span>        |
  | <span data-ttu-id="6168e-145">Dauer</span><span class="sxs-lookup"><span data-stu-id="6168e-145">Amount</span></span>            | <span data-ttu-id="6168e-146">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="6168e-146">Real</span></span>      |          |
  | <span data-ttu-id="6168e-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="6168e-147">HalfDayDefinition</span></span> | <span data-ttu-id="6168e-148">Option</span><span class="sxs-lookup"><span data-stu-id="6168e-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="6168e-149">Aktionen</span><span class="sxs-lookup"><span data-stu-id="6168e-149">Actions</span></span>

 | <span data-ttu-id="6168e-150">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="6168e-150">Action Name</span></span>                               | <span data-ttu-id="6168e-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6168e-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="6168e-152">Übermitteln</span><span class="sxs-lookup"><span data-stu-id="6168e-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="6168e-153">Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6168e-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6168e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6168e-154">See also</span></span>

- [<span data-ttu-id="6168e-155">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="6168e-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="6168e-156">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6168e-156">Authentication</span></span>](hr-developer-api-authentication.md)