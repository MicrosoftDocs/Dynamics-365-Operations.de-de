---
title: Bewerberintegrationsergebnis
description: In diesem Thema wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467552"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="8115d-103">Bewerberintegrationsergebnis</span><span class="sxs-lookup"><span data-stu-id="8115d-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8115d-104">In diesem Thema wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8115d-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8115d-105">Physischer Name: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="8115d-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="8115d-106">Diese Aufzählung liefert den Status für einen Kandidatendatensatz.</span><span class="sxs-lookup"><span data-stu-id="8115d-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="8115d-107">Wert</span><span class="sxs-lookup"><span data-stu-id="8115d-107">Value</span></span> | <span data-ttu-id="8115d-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="8115d-108">Label</span></span> | <span data-ttu-id="8115d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8115d-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8115d-110">200000000</span><span class="sxs-lookup"><span data-stu-id="8115d-110">200000000</span></span> | <span data-ttu-id="8115d-111">Nicht verarbeitet</span><span class="sxs-lookup"><span data-stu-id="8115d-111">Not processed</span></span> | <span data-ttu-id="8115d-112">Der Kandidat wird noch geprüft.</span><span class="sxs-lookup"><span data-stu-id="8115d-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="8115d-113">200000001</span><span class="sxs-lookup"><span data-stu-id="8115d-113">200000001</span></span> | <span data-ttu-id="8115d-114">Eingestellt</span><span class="sxs-lookup"><span data-stu-id="8115d-114">Hired</span></span> | <span data-ttu-id="8115d-115">Der Kandidat wurde eingestellt.</span><span class="sxs-lookup"><span data-stu-id="8115d-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="8115d-116">200000002</span><span class="sxs-lookup"><span data-stu-id="8115d-116">200000002</span></span> | <span data-ttu-id="8115d-117">Nicht eingestellt</span><span class="sxs-lookup"><span data-stu-id="8115d-117">Not hired</span></span> | <span data-ttu-id="8115d-118">Es wurde beschlossen, den Kandidaten nicht einzustellen.</span><span class="sxs-lookup"><span data-stu-id="8115d-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="8115d-119">200000003</span><span class="sxs-lookup"><span data-stu-id="8115d-119">200000003</span></span> | <span data-ttu-id="8115d-120">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="8115d-120">Dismissed</span></span> | <span data-ttu-id="8115d-121">Der Kandidat wurde von der Prüfung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8115d-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8115d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8115d-122">See also</span></span>

[<span data-ttu-id="8115d-123">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="8115d-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8115d-124">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="8115d-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]