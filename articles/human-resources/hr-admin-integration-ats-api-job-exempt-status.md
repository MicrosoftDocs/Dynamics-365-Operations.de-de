---
title: Stellenbefreiungsstatus
description: In diesem Thema wird der Optionssatz Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053850"
---
# <a name="job-exempt-status"></a><span data-ttu-id="82714-103">Stellenbefreiungsstatus</span><span class="sxs-lookup"><span data-stu-id="82714-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="82714-104">In diesem Thema wird der Optionssatz Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82714-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="82714-105">Physischer Name: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="82714-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="82714-106">Diese Aufzählung gibt den Optionssatz für FLSA-Stellenbefreiungsstatuswerte an.</span><span class="sxs-lookup"><span data-stu-id="82714-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="82714-107">Dies wird im vorhandenen Optionssatz cdm_jobexemptstatus bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="82714-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="82714-108">Wert</span><span class="sxs-lookup"><span data-stu-id="82714-108">Value</span></span> | <span data-ttu-id="82714-109">Etikett</span><span class="sxs-lookup"><span data-stu-id="82714-109">Label</span></span> | <span data-ttu-id="82714-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82714-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="82714-111">200000000</span><span class="sxs-lookup"><span data-stu-id="82714-111">200000000</span></span> | <span data-ttu-id="82714-112">Befreit</span><span class="sxs-lookup"><span data-stu-id="82714-112">Exempt</span></span> | <span data-ttu-id="82714-113">Die Stelle hat einen Ausnahmestatus basierend auf den FLSA-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="82714-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="82714-114">200000001</span><span class="sxs-lookup"><span data-stu-id="82714-114">200000001</span></span> | <span data-ttu-id="82714-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="82714-115">NonExempt</span></span> | <span data-ttu-id="82714-116">Die Stelle hat einen Nicht-Ausnahmestatus basierend auf den FLSA-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="82714-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="82714-117">200000002</span><span class="sxs-lookup"><span data-stu-id="82714-117">200000002</span></span> | <span data-ttu-id="82714-118">Trifft nicht zu</span><span class="sxs-lookup"><span data-stu-id="82714-118">Does Not Apply</span></span> | <span data-ttu-id="82714-119">Die FLSA-Statusrichtlinien gelten nicht für die Stelle.</span><span class="sxs-lookup"><span data-stu-id="82714-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="82714-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82714-120">See also</span></span>

[<span data-ttu-id="82714-121">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="82714-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="82714-122">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="82714-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]