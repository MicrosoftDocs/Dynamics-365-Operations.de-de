---
title: Bescheinigungstyp
description: In diesem Thema wird die Zertifikatstyp-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125712"
---
# <a name="certificate-type"></a>Bescheinigungstyp

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

