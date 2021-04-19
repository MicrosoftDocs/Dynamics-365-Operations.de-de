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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803632"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="22408-103">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="22408-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="22408-104">Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="22408-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="22408-105">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="22408-105">Key</span></span>

  | <span data-ttu-id="22408-106">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="22408-106">Property Name</span></span> | <span data-ttu-id="22408-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="22408-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="22408-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="22408-108">dataAreaId</span></span>    | <span data-ttu-id="22408-109">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-109">String</span></span>    |
  | <span data-ttu-id="22408-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="22408-110">RequestId</span></span>     | <span data-ttu-id="22408-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-111">String</span></span>    |
  | <span data-ttu-id="22408-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="22408-112">LeaveType</span></span>     | <span data-ttu-id="22408-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-113">String</span></span>    |
  | <span data-ttu-id="22408-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="22408-114">LeaveDate</span></span>     | <span data-ttu-id="22408-115">Datum</span><span class="sxs-lookup"><span data-stu-id="22408-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="22408-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22408-116">Properties</span></span>

  | <span data-ttu-id="22408-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="22408-117">Property Name</span></span>     | <span data-ttu-id="22408-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="22408-118">Data Type</span></span> | <span data-ttu-id="22408-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="22408-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="22408-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="22408-120">dataAreaId</span></span>        | <span data-ttu-id="22408-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-121">String</span></span>    | <span data-ttu-id="22408-122">X</span><span class="sxs-lookup"><span data-stu-id="22408-122">X</span></span>        |
  | <span data-ttu-id="22408-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="22408-123">RequestId</span></span>         | <span data-ttu-id="22408-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-124">String</span></span>    | <span data-ttu-id="22408-125">X</span><span class="sxs-lookup"><span data-stu-id="22408-125">X</span></span>        |
  | <span data-ttu-id="22408-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="22408-126">LeaveType</span></span>         | <span data-ttu-id="22408-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-127">String</span></span>    | <span data-ttu-id="22408-128">X</span><span class="sxs-lookup"><span data-stu-id="22408-128">X</span></span>        |
  | <span data-ttu-id="22408-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="22408-129">LeaveDate</span></span>         | <span data-ttu-id="22408-130">Datum</span><span class="sxs-lookup"><span data-stu-id="22408-130">Date</span></span>      | <span data-ttu-id="22408-131">X</span><span class="sxs-lookup"><span data-stu-id="22408-131">X</span></span>        |
  | <span data-ttu-id="22408-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="22408-132">ReasonCodeId</span></span>      | <span data-ttu-id="22408-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-133">String</span></span>    |          |
  | <span data-ttu-id="22408-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="22408-134">PersonnelNumber</span></span>   | <span data-ttu-id="22408-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-135">String</span></span>    | <span data-ttu-id="22408-136">X</span><span class="sxs-lookup"><span data-stu-id="22408-136">X</span></span>        |
  | <span data-ttu-id="22408-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="22408-137">RequestDate</span></span>       | <span data-ttu-id="22408-138">Datum</span><span class="sxs-lookup"><span data-stu-id="22408-138">Date</span></span>      | <span data-ttu-id="22408-139">X</span><span class="sxs-lookup"><span data-stu-id="22408-139">X</span></span>        |
  | <span data-ttu-id="22408-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="22408-140">Comment</span></span>           | <span data-ttu-id="22408-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22408-141">String</span></span>    |          |
  | <span data-ttu-id="22408-142">Status</span><span class="sxs-lookup"><span data-stu-id="22408-142">Status</span></span>            | <span data-ttu-id="22408-143">Option</span><span class="sxs-lookup"><span data-stu-id="22408-143">Enum</span></span>      | <span data-ttu-id="22408-144">X</span><span class="sxs-lookup"><span data-stu-id="22408-144">X</span></span>        |
  | <span data-ttu-id="22408-145">Dauer</span><span class="sxs-lookup"><span data-stu-id="22408-145">Amount</span></span>            | <span data-ttu-id="22408-146">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="22408-146">Real</span></span>      |          |
  | <span data-ttu-id="22408-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="22408-147">HalfDayDefinition</span></span> | <span data-ttu-id="22408-148">Option</span><span class="sxs-lookup"><span data-stu-id="22408-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="22408-149">Aktionen</span><span class="sxs-lookup"><span data-stu-id="22408-149">Actions</span></span>

 | <span data-ttu-id="22408-150">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="22408-150">Action Name</span></span>                               | <span data-ttu-id="22408-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22408-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="22408-152">Übermitteln</span><span class="sxs-lookup"><span data-stu-id="22408-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="22408-153">Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22408-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="22408-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22408-154">See also</span></span>

- [<span data-ttu-id="22408-155">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="22408-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="22408-156">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="22408-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]