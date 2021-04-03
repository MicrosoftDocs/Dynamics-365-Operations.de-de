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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465509"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="eb9da-103">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="eb9da-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eb9da-104">Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="eb9da-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="eb9da-105">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="eb9da-105">Key</span></span>

  | <span data-ttu-id="eb9da-106">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="eb9da-106">Property Name</span></span> | <span data-ttu-id="eb9da-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eb9da-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="eb9da-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="eb9da-108">dataAreaId</span></span>    | <span data-ttu-id="eb9da-109">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-109">String</span></span>    |
  | <span data-ttu-id="eb9da-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="eb9da-110">RequestId</span></span>     | <span data-ttu-id="eb9da-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-111">String</span></span>    |
  | <span data-ttu-id="eb9da-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="eb9da-112">LeaveType</span></span>     | <span data-ttu-id="eb9da-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-113">String</span></span>    |
  | <span data-ttu-id="eb9da-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="eb9da-114">LeaveDate</span></span>     | <span data-ttu-id="eb9da-115">Datum</span><span class="sxs-lookup"><span data-stu-id="eb9da-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="eb9da-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb9da-116">Properties</span></span>

  | <span data-ttu-id="eb9da-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="eb9da-117">Property Name</span></span>     | <span data-ttu-id="eb9da-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eb9da-118">Data Type</span></span> | <span data-ttu-id="eb9da-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="eb9da-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="eb9da-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="eb9da-120">dataAreaId</span></span>        | <span data-ttu-id="eb9da-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-121">String</span></span>    | <span data-ttu-id="eb9da-122">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-122">X</span></span>        |
  | <span data-ttu-id="eb9da-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="eb9da-123">RequestId</span></span>         | <span data-ttu-id="eb9da-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-124">String</span></span>    | <span data-ttu-id="eb9da-125">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-125">X</span></span>        |
  | <span data-ttu-id="eb9da-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="eb9da-126">LeaveType</span></span>         | <span data-ttu-id="eb9da-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-127">String</span></span>    | <span data-ttu-id="eb9da-128">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-128">X</span></span>        |
  | <span data-ttu-id="eb9da-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="eb9da-129">LeaveDate</span></span>         | <span data-ttu-id="eb9da-130">Datum</span><span class="sxs-lookup"><span data-stu-id="eb9da-130">Date</span></span>      | <span data-ttu-id="eb9da-131">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-131">X</span></span>        |
  | <span data-ttu-id="eb9da-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="eb9da-132">ReasonCodeId</span></span>      | <span data-ttu-id="eb9da-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-133">String</span></span>    |          |
  | <span data-ttu-id="eb9da-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="eb9da-134">PersonnelNumber</span></span>   | <span data-ttu-id="eb9da-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-135">String</span></span>    | <span data-ttu-id="eb9da-136">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-136">X</span></span>        |
  | <span data-ttu-id="eb9da-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="eb9da-137">RequestDate</span></span>       | <span data-ttu-id="eb9da-138">Datum</span><span class="sxs-lookup"><span data-stu-id="eb9da-138">Date</span></span>      | <span data-ttu-id="eb9da-139">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-139">X</span></span>        |
  | <span data-ttu-id="eb9da-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="eb9da-140">Comment</span></span>           | <span data-ttu-id="eb9da-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eb9da-141">String</span></span>    |          |
  | <span data-ttu-id="eb9da-142">Status</span><span class="sxs-lookup"><span data-stu-id="eb9da-142">Status</span></span>            | <span data-ttu-id="eb9da-143">Option</span><span class="sxs-lookup"><span data-stu-id="eb9da-143">Enum</span></span>      | <span data-ttu-id="eb9da-144">X</span><span class="sxs-lookup"><span data-stu-id="eb9da-144">X</span></span>        |
  | <span data-ttu-id="eb9da-145">Dauer</span><span class="sxs-lookup"><span data-stu-id="eb9da-145">Amount</span></span>            | <span data-ttu-id="eb9da-146">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="eb9da-146">Real</span></span>      |          |
  | <span data-ttu-id="eb9da-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="eb9da-147">HalfDayDefinition</span></span> | <span data-ttu-id="eb9da-148">Option</span><span class="sxs-lookup"><span data-stu-id="eb9da-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="eb9da-149">Aktionen</span><span class="sxs-lookup"><span data-stu-id="eb9da-149">Actions</span></span>

 | <span data-ttu-id="eb9da-150">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="eb9da-150">Action Name</span></span>                               | <span data-ttu-id="eb9da-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb9da-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="eb9da-152">Übermitteln</span><span class="sxs-lookup"><span data-stu-id="eb9da-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="eb9da-153">Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb9da-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="eb9da-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb9da-154">See also</span></span>

- [<span data-ttu-id="eb9da-155">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="eb9da-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="eb9da-156">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="eb9da-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]