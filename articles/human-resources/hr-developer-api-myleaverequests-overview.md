---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115535"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="fe36c-103">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="fe36c-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="fe36c-104">Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="fe36c-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="fe36c-105">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="fe36c-105">Key</span></span>

  | <span data-ttu-id="fe36c-106">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fe36c-106">Property Name</span></span> | <span data-ttu-id="fe36c-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fe36c-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="fe36c-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="fe36c-108">dataAreaId</span></span>    | <span data-ttu-id="fe36c-109">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-109">String</span></span>    |
  | <span data-ttu-id="fe36c-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="fe36c-110">RequestId</span></span>     | <span data-ttu-id="fe36c-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-111">String</span></span>    |
  | <span data-ttu-id="fe36c-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="fe36c-112">LeaveType</span></span>     | <span data-ttu-id="fe36c-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-113">String</span></span>    |
  | <span data-ttu-id="fe36c-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="fe36c-114">LeaveDate</span></span>     | <span data-ttu-id="fe36c-115">Datum</span><span class="sxs-lookup"><span data-stu-id="fe36c-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="fe36c-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe36c-116">Properties</span></span>

  | <span data-ttu-id="fe36c-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fe36c-117">Property Name</span></span>     | <span data-ttu-id="fe36c-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fe36c-118">Data Type</span></span> | <span data-ttu-id="fe36c-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fe36c-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="fe36c-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="fe36c-120">dataAreaId</span></span>        | <span data-ttu-id="fe36c-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-121">String</span></span>    | <span data-ttu-id="fe36c-122">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-122">X</span></span>        |
  | <span data-ttu-id="fe36c-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="fe36c-123">RequestId</span></span>         | <span data-ttu-id="fe36c-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-124">String</span></span>    | <span data-ttu-id="fe36c-125">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-125">X</span></span>        |
  | <span data-ttu-id="fe36c-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="fe36c-126">LeaveType</span></span>         | <span data-ttu-id="fe36c-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-127">String</span></span>    | <span data-ttu-id="fe36c-128">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-128">X</span></span>        |
  | <span data-ttu-id="fe36c-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="fe36c-129">LeaveDate</span></span>         | <span data-ttu-id="fe36c-130">Datum</span><span class="sxs-lookup"><span data-stu-id="fe36c-130">Date</span></span>      | <span data-ttu-id="fe36c-131">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-131">X</span></span>        |
  | <span data-ttu-id="fe36c-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="fe36c-132">ReasonCodeId</span></span>      | <span data-ttu-id="fe36c-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-133">String</span></span>    |          |
  | <span data-ttu-id="fe36c-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="fe36c-134">PersonnelNumber</span></span>   | <span data-ttu-id="fe36c-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-135">String</span></span>    | <span data-ttu-id="fe36c-136">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-136">X</span></span>        |
  | <span data-ttu-id="fe36c-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="fe36c-137">RequestDate</span></span>       | <span data-ttu-id="fe36c-138">Datum</span><span class="sxs-lookup"><span data-stu-id="fe36c-138">Date</span></span>      | <span data-ttu-id="fe36c-139">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-139">X</span></span>        |
  | <span data-ttu-id="fe36c-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="fe36c-140">Comment</span></span>           | <span data-ttu-id="fe36c-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe36c-141">String</span></span>    |          |
  | <span data-ttu-id="fe36c-142">Status</span><span class="sxs-lookup"><span data-stu-id="fe36c-142">Status</span></span>            | <span data-ttu-id="fe36c-143">Option</span><span class="sxs-lookup"><span data-stu-id="fe36c-143">Enum</span></span>      | <span data-ttu-id="fe36c-144">X</span><span class="sxs-lookup"><span data-stu-id="fe36c-144">X</span></span>        |
  | <span data-ttu-id="fe36c-145">Dauer</span><span class="sxs-lookup"><span data-stu-id="fe36c-145">Amount</span></span>            | <span data-ttu-id="fe36c-146">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="fe36c-146">Real</span></span>      |          |
  | <span data-ttu-id="fe36c-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="fe36c-147">HalfDayDefinition</span></span> | <span data-ttu-id="fe36c-148">Option</span><span class="sxs-lookup"><span data-stu-id="fe36c-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="fe36c-149">Aktionen</span><span class="sxs-lookup"><span data-stu-id="fe36c-149">Actions</span></span>

 | <span data-ttu-id="fe36c-150">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="fe36c-150">Action Name</span></span>                               | <span data-ttu-id="fe36c-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe36c-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="fe36c-152">Übermitteln</span><span class="sxs-lookup"><span data-stu-id="fe36c-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="fe36c-153">Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe36c-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fe36c-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe36c-154">See also</span></span>

- [<span data-ttu-id="fe36c-155">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="fe36c-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="fe36c-156">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fe36c-156">Authentication</span></span>](hr-developer-api-authentication.md)