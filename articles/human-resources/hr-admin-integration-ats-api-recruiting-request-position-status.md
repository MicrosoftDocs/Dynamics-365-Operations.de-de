---
title: Positionsstatus ders Personalbeschaffungsantrags
description: In diesem Thema wird der Optionssatz zum Status der Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051880"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="8fe4e-103">Positionsstatus ders Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="8fe4e-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8fe4e-104">In diesem Thema wird der Optionssatz zum Status der Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8fe4e-105">Physischer Name: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="8fe4e-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="8fe4e-106">Diese Aufzählung bietet den Optionssatz für die Statuswerte jeder Position eines Personalbeschaffungsantrags in der Entität RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="8fe4e-107">Wert</span><span class="sxs-lookup"><span data-stu-id="8fe4e-107">Value</span></span> | <span data-ttu-id="8fe4e-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="8fe4e-108">Label</span></span> | <span data-ttu-id="8fe4e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fe4e-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8fe4e-110">200000000</span><span class="sxs-lookup"><span data-stu-id="8fe4e-110">200000000</span></span> | <span data-ttu-id="8fe4e-111">Öffentlich</span><span class="sxs-lookup"><span data-stu-id="8fe4e-111">Open</span></span> | <span data-ttu-id="8fe4e-112">Die Position im Personalbeschaffungsantrag ist offen für die Rekrutierung.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="8fe4e-113">Dies bedeutet nicht, dass für die Position derzeit keine Positionszuweisung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="8fe4e-114">Zum Zeitpunkt der Einstellung befindet sich möglicherweise ein Mitarbeiter in der Position.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="8fe4e-115">Es wird nur angezeigt, dass die Position im Rahmen des Personalbeschaffungsantrags für die Rekrutierung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="8fe4e-116">200000001</span><span class="sxs-lookup"><span data-stu-id="8fe4e-116">200000001</span></span> | <span data-ttu-id="8fe4e-117">Besetzt</span><span class="sxs-lookup"><span data-stu-id="8fe4e-117">Filled</span></span> | <span data-ttu-id="8fe4e-118">Eine Arbeitskraft wurde für die Zuordnung zur Position ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="8fe4e-119">200000002</span><span class="sxs-lookup"><span data-stu-id="8fe4e-119">200000002</span></span> | <span data-ttu-id="8fe4e-120">Storniert</span><span class="sxs-lookup"><span data-stu-id="8fe4e-120">Canceled</span></span> | <span data-ttu-id="8fe4e-121">Der Antrag auf Einstellung für diese Position wurde storniert.</span><span class="sxs-lookup"><span data-stu-id="8fe4e-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8fe4e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fe4e-122">See also</span></span>

[<span data-ttu-id="8fe4e-123">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="8fe4e-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8fe4e-124">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="8fe4e-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]