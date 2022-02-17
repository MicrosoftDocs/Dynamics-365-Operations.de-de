---
title: Bescheinigungstyp
description: In diesem Thema wird die Zertifikatstyp-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 3d01c7f01657af1501aed14f63dfb2cfbc133f8b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067200"
---
# <a name="certificate-type"></a>Bescheinigungstyp


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Zertifikatstyp-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmcertificatetypeentity

## <a name="description"></a>Beschreibung

Diese Entität definiert die Liste der in Human Resources eingerichteten Berufszertifikatstypen. Die Entität ist nicht spezifisch für eine juristische Person (Unternehmen).

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Zertifikatstypentitätskennung**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich 
Vom System generiert | Eindeutiger primärer Bezeichner für den Zertifikatstyp. |
| **Zertifikatstyp**<br>mshr_certificatetype<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Eindeutiger vom Benutzer lesbarer Bezeichner für den Zertifikatstyp. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Beschreibung des Zertifikatstyps. |
| **Erneuerung anfordern**<br>mshr_requirerenewal<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Gibt an, ob für das Zertifikat eine Erneuerung erforderlich ist. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
