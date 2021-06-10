---
title: Beispielabfrage für Kandidaten zur Einstellung
description: Dieses Thema enthält eine Beispielabfrage für die Entität Kandidat zur Einstellung, in Dynamics 365 Human Resources.
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
ms.openlocfilehash: efec8c0a8eb75f818acd4ed02632f1db96719d81
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054715"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="2bf45-103">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="2bf45-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2bf45-104">Dieses Thema enthält eine Beispielabfrage für die Entität Kandidat zur Einstellung, in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2bf45-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="2bf45-105">Dieses Thema enthält ein Beispiel, das zeigt, wie Sie *tiefes Einfügen* verwenden können, um alle Details eines neuen Kandidatendatensatzes in einer einzigen API-Operation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bf45-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="2bf45-106">Weitere Informationen zu tiefen Einfügen finden Sie unter [Erstellen verwandter Entitätsdatensätze in einem Vorgang](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="2bf45-106">For more information about deep inserts, see [Create related entity records in one operation](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="2bf45-107">Die **mshr_hcmcandidatetohireentity**-Entität ist aufgrund seiner Beziehung zur **mshr_dirpersonentity**-Entität einzigartig.</span><span class="sxs-lookup"><span data-stu-id="2bf45-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="2bf45-108">Viele der Eigenschaften von **mshr_hcmcandidatetohireentity** (zum Beispiel **mshr_firstname**, **mshr_lastname** und **mshr_birthdate**) sind vom **mshr_dirpersonentity**-Datensatz abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2bf45-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="2bf45-109">Wenn Sie einen neuen Kandidatendatensatz ohne tiefes Einfügen an **mshr_hcmcandidatetohireentity** senden, können Sie Werte für diese Eigenschaften direkt im **mshr_hcmcandidatetohireentity**-Datensatz definieren.</span><span class="sxs-lookup"><span data-stu-id="2bf45-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="2bf45-110">Der zugehörige **mshr_dirpersonentity**-Datensatz wird implizit mit den definierten Werten für die Eigenschaften erstellt.</span><span class="sxs-lookup"><span data-stu-id="2bf45-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="2bf45-111">Sie können dann alle anderen zugehörigen Entitätsdatensätze (z. B. Qualifikationen oder Ausbildung) als separate API-Aufrufe erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bf45-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="2bf45-112">Wenn Sie jedoch tiefes Einfügen verwenden möchten, um alle zugehörigen Entitäten in einem Vorgang zu erstellen, müssen die spezifischen Eigenschaften der **mshr_dirpersonentity**-Entität auf dieser verschachtelten Ebene des Vorgangs definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2bf45-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="2bf45-113">Dieses Beispiel zeigt, wie Sie einen Kandidatendatensatz, den zugehörigen Personendatensatz sowie die Qualifikationen und die Ausbildung der Person mithilfe von tiefem Einfügen in drei verschachtelten Ebenen in einer einzigen API-Operation erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2bf45-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="2bf45-114">Das Beispiel enthält nicht alle Eigenschaften der einzelnen API-Entitäten.</span><span class="sxs-lookup"><span data-stu-id="2bf45-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="2bf45-115">Es ist zu Demonstrationszwecken vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2bf45-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="2bf45-116">**Anforderung**</span><span class="sxs-lookup"><span data-stu-id="2bf45-116">**Request**</span></span>

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

<span data-ttu-id="2bf45-117">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="2bf45-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="2bf45-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bf45-118">See also</span></span>

[<span data-ttu-id="2bf45-119">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="2bf45-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]