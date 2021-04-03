---
title: Status des Personalbeschaffungsantrags
description: In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464645"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="d8b7f-103">Status des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="d8b7f-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d8b7f-104">In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d8b7f-105">Physischer Name: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="d8b7f-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="d8b7f-106">Diese Aufzählung bietet den Optionssatz für die Statuswerte eines RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="d8b7f-107">Wert</span><span class="sxs-lookup"><span data-stu-id="d8b7f-107">Value</span></span> | <span data-ttu-id="d8b7f-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="d8b7f-108">Label</span></span> | <span data-ttu-id="d8b7f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8b7f-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d8b7f-110">200000000</span><span class="sxs-lookup"><span data-stu-id="d8b7f-110">200000000</span></span> | <span data-ttu-id="d8b7f-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d8b7f-111">Draft</span></span> | <span data-ttu-id="d8b7f-112">Die Anfrage befindet sich im Entwurf und ist nicht für die aktive Rekrutierung bereit.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="d8b7f-113">200000001</span><span class="sxs-lookup"><span data-stu-id="d8b7f-113">200000001</span></span> | <span data-ttu-id="d8b7f-114">In Überprüfung</span><span class="sxs-lookup"><span data-stu-id="d8b7f-114">In Review</span></span> | <span data-ttu-id="d8b7f-115">Die Anforderung wurde gesendet und wird zur Genehmigung durch den Workflow weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="d8b7f-116">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d8b7f-117">200000002</span><span class="sxs-lookup"><span data-stu-id="d8b7f-117">200000002</span></span> | <span data-ttu-id="d8b7f-118">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="d8b7f-118">Pending</span></span> | <span data-ttu-id="d8b7f-119">Die Anfrage wartet auf die Workflow-Aktion.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-119">The request is pending workflow action.</span></span> <span data-ttu-id="d8b7f-120">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d8b7f-121">200000003</span><span class="sxs-lookup"><span data-stu-id="d8b7f-121">200000003</span></span> | <span data-ttu-id="d8b7f-122">Storniert</span><span class="sxs-lookup"><span data-stu-id="d8b7f-122">Canceled</span></span> | <span data-ttu-id="d8b7f-123">Die Anforderung wurde storniert.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-123">The request has been canceled.</span></span> <span data-ttu-id="d8b7f-124">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d8b7f-125">200000004</span><span class="sxs-lookup"><span data-stu-id="d8b7f-125">200000004</span></span> | <span data-ttu-id="d8b7f-126">Verweigert</span><span class="sxs-lookup"><span data-stu-id="d8b7f-126">Denied</span></span> | <span data-ttu-id="d8b7f-127">Die Anforderung wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-127">The request has been denied.</span></span> <span data-ttu-id="d8b7f-128">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d8b7f-129">200000005</span><span class="sxs-lookup"><span data-stu-id="d8b7f-129">200000005</span></span> | <span data-ttu-id="d8b7f-130">Aktiv</span><span class="sxs-lookup"><span data-stu-id="d8b7f-130">Active</span></span> | <span data-ttu-id="d8b7f-131">Jeder Workflow wird abgeschlossen und genehmigt, und die Anfrage ist für die aktive Rekrutierung bereit.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="d8b7f-132">200000006</span><span class="sxs-lookup"><span data-stu-id="d8b7f-132">200000006</span></span> | <span data-ttu-id="d8b7f-133">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="d8b7f-133">Closed</span></span> | <span data-ttu-id="d8b7f-134">Der Personalbeschaffungsantrage wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d8b7f-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d8b7f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8b7f-135">See also</span></span>

[<span data-ttu-id="d8b7f-136">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="d8b7f-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d8b7f-137">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="d8b7f-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]