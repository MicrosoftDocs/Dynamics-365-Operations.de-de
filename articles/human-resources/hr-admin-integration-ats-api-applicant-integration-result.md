---
title: Bewerberintegrationsergebnis
description: In diesem Thema wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 8bef974abff18d7c07ecd679b7e01b31ea1459c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053898"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="059a6-103">Bewerberintegrationsergebnis</span><span class="sxs-lookup"><span data-stu-id="059a6-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="059a6-104">In diesem Thema wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="059a6-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="059a6-105">Physischer Name: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="059a6-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="059a6-106">Diese Aufzählung liefert den Status für einen Kandidatendatensatz.</span><span class="sxs-lookup"><span data-stu-id="059a6-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="059a6-107">Wert</span><span class="sxs-lookup"><span data-stu-id="059a6-107">Value</span></span> | <span data-ttu-id="059a6-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="059a6-108">Label</span></span> | <span data-ttu-id="059a6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="059a6-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="059a6-110">200000000</span><span class="sxs-lookup"><span data-stu-id="059a6-110">200000000</span></span> | <span data-ttu-id="059a6-111">Nicht verarbeitet</span><span class="sxs-lookup"><span data-stu-id="059a6-111">Not processed</span></span> | <span data-ttu-id="059a6-112">Der Kandidat wird noch geprüft.</span><span class="sxs-lookup"><span data-stu-id="059a6-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="059a6-113">200000001</span><span class="sxs-lookup"><span data-stu-id="059a6-113">200000001</span></span> | <span data-ttu-id="059a6-114">Eingestellt</span><span class="sxs-lookup"><span data-stu-id="059a6-114">Hired</span></span> | <span data-ttu-id="059a6-115">Der Kandidat wurde eingestellt.</span><span class="sxs-lookup"><span data-stu-id="059a6-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="059a6-116">200000002</span><span class="sxs-lookup"><span data-stu-id="059a6-116">200000002</span></span> | <span data-ttu-id="059a6-117">Nicht eingestellt</span><span class="sxs-lookup"><span data-stu-id="059a6-117">Not hired</span></span> | <span data-ttu-id="059a6-118">Es wurde beschlossen, den Kandidaten nicht einzustellen.</span><span class="sxs-lookup"><span data-stu-id="059a6-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="059a6-119">200000003</span><span class="sxs-lookup"><span data-stu-id="059a6-119">200000003</span></span> | <span data-ttu-id="059a6-120">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="059a6-120">Dismissed</span></span> | <span data-ttu-id="059a6-121">Der Kandidat wurde von der Prüfung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="059a6-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="059a6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="059a6-122">See also</span></span>

[<span data-ttu-id="059a6-123">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="059a6-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="059a6-124">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="059a6-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]