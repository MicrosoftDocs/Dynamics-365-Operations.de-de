---
title: MyLeaveRequests-Überblick
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009143"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="264c3-102">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="264c3-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="264c3-103">Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="264c3-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="264c3-104">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="264c3-104">Key</span></span>

  | <span data-ttu-id="264c3-105">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="264c3-105">Property Name</span></span> | <span data-ttu-id="264c3-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="264c3-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="264c3-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="264c3-107">dataAreaId</span></span>    | <span data-ttu-id="264c3-108">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-108">String</span></span>    |
  | <span data-ttu-id="264c3-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="264c3-109">RequestId</span></span>     | <span data-ttu-id="264c3-110">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-110">String</span></span>    |
  | <span data-ttu-id="264c3-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="264c3-111">LeaveType</span></span>     | <span data-ttu-id="264c3-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-112">String</span></span>    |
  | <span data-ttu-id="264c3-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="264c3-113">LeaveDate</span></span>     | <span data-ttu-id="264c3-114">Datum</span><span class="sxs-lookup"><span data-stu-id="264c3-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="264c3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="264c3-115">Properties</span></span>

  | <span data-ttu-id="264c3-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="264c3-116">Property Name</span></span>     | <span data-ttu-id="264c3-117">Datentyp</span><span class="sxs-lookup"><span data-stu-id="264c3-117">Data Type</span></span> | <span data-ttu-id="264c3-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="264c3-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="264c3-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="264c3-119">dataAreaId</span></span>        | <span data-ttu-id="264c3-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-120">String</span></span>    | <span data-ttu-id="264c3-121">X</span><span class="sxs-lookup"><span data-stu-id="264c3-121">X</span></span>        |
  | <span data-ttu-id="264c3-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="264c3-122">RequestId</span></span>         | <span data-ttu-id="264c3-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-123">String</span></span>    | <span data-ttu-id="264c3-124">X</span><span class="sxs-lookup"><span data-stu-id="264c3-124">X</span></span>        |
  | <span data-ttu-id="264c3-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="264c3-125">LeaveType</span></span>         | <span data-ttu-id="264c3-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-126">String</span></span>    | <span data-ttu-id="264c3-127">X</span><span class="sxs-lookup"><span data-stu-id="264c3-127">X</span></span>        |
  | <span data-ttu-id="264c3-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="264c3-128">LeaveDate</span></span>         | <span data-ttu-id="264c3-129">Datum</span><span class="sxs-lookup"><span data-stu-id="264c3-129">Date</span></span>      | <span data-ttu-id="264c3-130">X</span><span class="sxs-lookup"><span data-stu-id="264c3-130">X</span></span>        |
  | <span data-ttu-id="264c3-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="264c3-131">ReasonCodeId</span></span>      | <span data-ttu-id="264c3-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-132">String</span></span>    |          |
  | <span data-ttu-id="264c3-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="264c3-133">PersonnelNumber</span></span>   | <span data-ttu-id="264c3-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-134">String</span></span>    | <span data-ttu-id="264c3-135">X</span><span class="sxs-lookup"><span data-stu-id="264c3-135">X</span></span>        |
  | <span data-ttu-id="264c3-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="264c3-136">RequestDate</span></span>       | <span data-ttu-id="264c3-137">Datum</span><span class="sxs-lookup"><span data-stu-id="264c3-137">Date</span></span>      | <span data-ttu-id="264c3-138">X</span><span class="sxs-lookup"><span data-stu-id="264c3-138">X</span></span>        |
  | <span data-ttu-id="264c3-139">Kommentar</span><span class="sxs-lookup"><span data-stu-id="264c3-139">Comment</span></span>           | <span data-ttu-id="264c3-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="264c3-140">String</span></span>    |          |
  | <span data-ttu-id="264c3-141">Status</span><span class="sxs-lookup"><span data-stu-id="264c3-141">Status</span></span>            | <span data-ttu-id="264c3-142">Option</span><span class="sxs-lookup"><span data-stu-id="264c3-142">Enum</span></span>      | <span data-ttu-id="264c3-143">X</span><span class="sxs-lookup"><span data-stu-id="264c3-143">X</span></span>        |
  | <span data-ttu-id="264c3-144">Dauer</span><span class="sxs-lookup"><span data-stu-id="264c3-144">Amount</span></span>            | <span data-ttu-id="264c3-145">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="264c3-145">Real</span></span>      |          |
  | <span data-ttu-id="264c3-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="264c3-146">HalfDayDefinition</span></span> | <span data-ttu-id="264c3-147">Option</span><span class="sxs-lookup"><span data-stu-id="264c3-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="264c3-148">Aktionen</span><span class="sxs-lookup"><span data-stu-id="264c3-148">Actions</span></span>

 | <span data-ttu-id="264c3-149">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="264c3-149">Action Name</span></span>                               | <span data-ttu-id="264c3-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="264c3-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="264c3-151">Übermitteln</span><span class="sxs-lookup"><span data-stu-id="264c3-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="264c3-152">Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="264c3-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="264c3-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="264c3-153">See also</span></span>

- [<span data-ttu-id="264c3-154">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="264c3-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="264c3-155">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="264c3-155">Authentication</span></span>](hr-developer-api-authentication.md)