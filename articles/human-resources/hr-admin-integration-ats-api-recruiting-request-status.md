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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125953"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="09cc5-103">Status des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="09cc5-103">Recruiting request status</span></span>

<span data-ttu-id="09cc5-104">In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="09cc5-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="09cc5-105">Physischer Name: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="09cc5-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="09cc5-106">Diese Aufzählung bietet den Optionssatz für die Statuswerte eines RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="09cc5-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="09cc5-107">Wert</span><span class="sxs-lookup"><span data-stu-id="09cc5-107">Value</span></span> | <span data-ttu-id="09cc5-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="09cc5-108">Label</span></span> | <span data-ttu-id="09cc5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09cc5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="09cc5-110">200000000</span><span class="sxs-lookup"><span data-stu-id="09cc5-110">200000000</span></span> | <span data-ttu-id="09cc5-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="09cc5-111">Draft</span></span> | <span data-ttu-id="09cc5-112">Die Anfrage befindet sich im Entwurf und ist nicht für die aktive Rekrutierung bereit.</span><span class="sxs-lookup"><span data-stu-id="09cc5-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="09cc5-113">200000001</span><span class="sxs-lookup"><span data-stu-id="09cc5-113">200000001</span></span> | <span data-ttu-id="09cc5-114">In Überprüfung</span><span class="sxs-lookup"><span data-stu-id="09cc5-114">In Review</span></span> | <span data-ttu-id="09cc5-115">Die Anforderung wurde gesendet und wird zur Genehmigung durch den Workflow weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="09cc5-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="09cc5-116">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="09cc5-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="09cc5-117">200000002</span><span class="sxs-lookup"><span data-stu-id="09cc5-117">200000002</span></span> | <span data-ttu-id="09cc5-118">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="09cc5-118">Pending</span></span> | <span data-ttu-id="09cc5-119">Die Anfrage wartet auf die Workflow-Aktion.</span><span class="sxs-lookup"><span data-stu-id="09cc5-119">The request is pending workflow action.</span></span> <span data-ttu-id="09cc5-120">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="09cc5-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="09cc5-121">200000003</span><span class="sxs-lookup"><span data-stu-id="09cc5-121">200000003</span></span> | <span data-ttu-id="09cc5-122">Storniert</span><span class="sxs-lookup"><span data-stu-id="09cc5-122">Canceled</span></span> | <span data-ttu-id="09cc5-123">Die Anforderung wurde storniert.</span><span class="sxs-lookup"><span data-stu-id="09cc5-123">The request has been canceled.</span></span> <span data-ttu-id="09cc5-124">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="09cc5-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="09cc5-125">200000004</span><span class="sxs-lookup"><span data-stu-id="09cc5-125">200000004</span></span> | <span data-ttu-id="09cc5-126">Verweigert</span><span class="sxs-lookup"><span data-stu-id="09cc5-126">Denied</span></span> | <span data-ttu-id="09cc5-127">Die Anforderung wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="09cc5-127">The request has been denied.</span></span> <span data-ttu-id="09cc5-128">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="09cc5-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="09cc5-129">200000005</span><span class="sxs-lookup"><span data-stu-id="09cc5-129">200000005</span></span> | <span data-ttu-id="09cc5-130">Aktiv</span><span class="sxs-lookup"><span data-stu-id="09cc5-130">Active</span></span> | <span data-ttu-id="09cc5-131">Jeder Workflow wird abgeschlossen und genehmigt, und die Anfrage ist für die aktive Rekrutierung bereit.</span><span class="sxs-lookup"><span data-stu-id="09cc5-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="09cc5-132">200000006</span><span class="sxs-lookup"><span data-stu-id="09cc5-132">200000006</span></span> | <span data-ttu-id="09cc5-133">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="09cc5-133">Closed</span></span> | <span data-ttu-id="09cc5-134">Der Personalbeschaffungsantrage wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="09cc5-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="09cc5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09cc5-135">See also</span></span>

[<span data-ttu-id="09cc5-136">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="09cc5-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="09cc5-137">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="09cc5-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
