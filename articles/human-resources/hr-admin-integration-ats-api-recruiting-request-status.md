---
title: Status des Personalbeschaffungsantrags
description: In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059183"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="80c04-103">Status des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="80c04-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="80c04-104">In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="80c04-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="80c04-105">Physischer Name: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="80c04-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="80c04-106">Diese Aufzählung bietet den Optionssatz für die Statuswerte eines RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="80c04-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="80c04-107">Wert</span><span class="sxs-lookup"><span data-stu-id="80c04-107">Value</span></span> | <span data-ttu-id="80c04-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="80c04-108">Label</span></span> | <span data-ttu-id="80c04-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80c04-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="80c04-110">200000000</span><span class="sxs-lookup"><span data-stu-id="80c04-110">200000000</span></span> | <span data-ttu-id="80c04-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="80c04-111">Draft</span></span> | <span data-ttu-id="80c04-112">Die Anfrage befindet sich im Entwurf und ist nicht für die aktive Rekrutierung bereit.</span><span class="sxs-lookup"><span data-stu-id="80c04-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="80c04-113">200000001</span><span class="sxs-lookup"><span data-stu-id="80c04-113">200000001</span></span> | <span data-ttu-id="80c04-114">In Überprüfung</span><span class="sxs-lookup"><span data-stu-id="80c04-114">In Review</span></span> | <span data-ttu-id="80c04-115">Die Anforderung wurde gesendet und wird zur Genehmigung durch den Workflow weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="80c04-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="80c04-116">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80c04-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="80c04-117">200000002</span><span class="sxs-lookup"><span data-stu-id="80c04-117">200000002</span></span> | <span data-ttu-id="80c04-118">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="80c04-118">Pending</span></span> | <span data-ttu-id="80c04-119">Die Anfrage wartet auf die Workflow-Aktion.</span><span class="sxs-lookup"><span data-stu-id="80c04-119">The request is pending workflow action.</span></span> <span data-ttu-id="80c04-120">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80c04-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="80c04-121">200000003</span><span class="sxs-lookup"><span data-stu-id="80c04-121">200000003</span></span> | <span data-ttu-id="80c04-122">Storniert</span><span class="sxs-lookup"><span data-stu-id="80c04-122">Canceled</span></span> | <span data-ttu-id="80c04-123">Die Anforderung wurde storniert.</span><span class="sxs-lookup"><span data-stu-id="80c04-123">The request has been canceled.</span></span> <span data-ttu-id="80c04-124">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80c04-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="80c04-125">200000004</span><span class="sxs-lookup"><span data-stu-id="80c04-125">200000004</span></span> | <span data-ttu-id="80c04-126">Verweigert</span><span class="sxs-lookup"><span data-stu-id="80c04-126">Denied</span></span> | <span data-ttu-id="80c04-127">Die Anforderung wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="80c04-127">The request has been denied.</span></span> <span data-ttu-id="80c04-128">Nur verfügbar, wenn der Workflow aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80c04-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="80c04-129">200000005</span><span class="sxs-lookup"><span data-stu-id="80c04-129">200000005</span></span> | <span data-ttu-id="80c04-130">Aktiv</span><span class="sxs-lookup"><span data-stu-id="80c04-130">Active</span></span> | <span data-ttu-id="80c04-131">Jeder Workflow wird abgeschlossen und genehmigt, und die Anfrage ist für die aktive Rekrutierung bereit.</span><span class="sxs-lookup"><span data-stu-id="80c04-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="80c04-132">200000006</span><span class="sxs-lookup"><span data-stu-id="80c04-132">200000006</span></span> | <span data-ttu-id="80c04-133">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="80c04-133">Closed</span></span> | <span data-ttu-id="80c04-134">Der Personalbeschaffungsantrage wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="80c04-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="80c04-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c04-135">See also</span></span>

[<span data-ttu-id="80c04-136">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="80c04-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="80c04-137">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="80c04-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]