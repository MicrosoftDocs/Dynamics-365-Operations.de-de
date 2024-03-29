---
title: Beispielabfrage für Kandidaten zur Einstellung
description: Dieser Artikel enthält eine Beispielabfrage für die Entität Kandidat zur Einstellung in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2dd744665d4f0b6c64f4ee45a01c237081018514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848341"
---
# <a name="example-query-for-candidate-to-hire"></a>Beispielabfrage für Kandidaten zur Einstellung


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel enthält eine Beispielabfrage für die Entität Kandidat zur Einstellung in Dynamics 365 Human Resources.

Dieser Artikel enthält ein Beispiel, das zeigt, wie Sie *tiefes Einfügen* verwenden können, um alle Details eines neuen Kandidatendatensatzes in einer einzigen API-Operation zu erstellen. Weitere Informationen zu tiefen Einfügen finden Sie unter [Erstellen verwandter Entitätsdatensätze in einem Vorgang](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Die **mshr_hcmcandidatetohireentity**-Entität ist aufgrund seiner Beziehung zur **mshr_dirpersonentity**-Entität einzigartig. Viele der Eigenschaften von **mshr_hcmcandidatetohireentity** (zum Beispiel **mshr_firstname**, **mshr_lastname** und **mshr_birthdate**) sind vom **mshr_dirpersonentity**-Datensatz abgeleitet. Wenn Sie einen neuen Kandidatendatensatz ohne tiefes Einfügen an **mshr_hcmcandidatetohireentity** senden, können Sie Werte für diese Eigenschaften direkt im **mshr_hcmcandidatetohireentity**-Datensatz definieren. Der zugehörige **mshr_dirpersonentity**-Datensatz wird implizit mit den definierten Werten für die Eigenschaften erstellt. Sie können dann alle anderen zugehörigen Entitätsdatensätze (z. B. Qualifikationen oder Ausbildung) als separate API-Aufrufe erstellen.

Wenn Sie jedoch tiefes Einfügen verwenden möchten, um alle zugehörigen Entitäten in einem Vorgang zu erstellen, müssen die spezifischen Eigenschaften der **mshr_dirpersonentity**-Entität auf dieser verschachtelten Ebene des Vorgangs definiert werden.

Dieses Beispiel zeigt, wie Sie einen Kandidatendatensatz, den zugehörigen Personendatensatz sowie die Qualifikationen und die Ausbildung der Person mithilfe von tiefem Einfügen in drei verschachtelten Ebenen in einer einzigen API-Operation erstellen können.

> [!NOTE]
> Das Beispiel enthält nicht alle Eigenschaften der einzelnen API-Entitäten. Es ist zu Demonstrationszwecken vereinfacht.

**Anforderung**

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

**Antwort**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
