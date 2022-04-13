---
title: Lohnentitäten generieren und überprüfen
description: In diesem Thema wird beschrieben, wie Sie Lohnentitäten generieren und überprüfen.
author: twheeloc
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8b69216a2b864645447f27f54319014cb166791c
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533851"
---
# <a name="generate-payroll-entities"></a>Lohnentitäten generieren


[!INCLUDE [PEAP](../includes/peap-1.md)]

Verwenden Sie diese OData-Funktion, um die Entitäten zu generieren, die für die Lohnintegration erforderlich sind. Wenn an diesen Entitäten in Human Resources Änderungen vorgenommen werden, z. B. das Hinzufügen benutzerdefinierter Felder, kann diese Funktion erneut aufgerufen werden, um die Metadaten jeder Entität zu aktualisieren. Die Antwort enthält eine Vorgangskennung, die Sie überwachen können, damit Sie wissen, wann der Generierungsprozess abgeschlossen ist.

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/RefreshHumanResourcesVirtualEntities
```

**Text**

```json
{
    "PhysicalNames" : ["PayrollEmployeeEntity", "HcmWorkerBaseEntity", "PayrollPositionEntity", "PayrollPositionJobEntity", "PayrollWorkerAddressEntity", "HcmJobDetailEntity", "HcmCompFixedPlanTableEntity", "PayrollFixedCompensationPlanEntity", "HcmEmploymentDetailEntity"]
}
```

**Antwort**

```json
{
    "AsyncOperationId": "8b98d338-f939-4c86-9a91-80b76b6ab2ea"
}
```

## <a name="review-payroll-entities"></a>Lohnentitäten überprüfen

Verwenden Sie diese API, um eine Liste der Entitäten abzurufen, die erfolgreich generiert wurden und zur Verwendung bereit sind.

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hrvirtualentitycatalogs?$filter=mshr_hasbeengenerated eq true
```

**Antwort**

```json
{
      "value": [
        {
            "mshr_physicalname": "PayrollWorkerAddressEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-1c00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmJobDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6400-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmCompFixedPlanTableEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6b00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollEmployeeEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6d00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmEmploymentDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-7e00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollFixedCompensationPlanEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-9300-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmWorkerBaseEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-c000-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollPositionJobEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-e700-005001000000",
            "mshr_refresh": null
        }
    ]
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
