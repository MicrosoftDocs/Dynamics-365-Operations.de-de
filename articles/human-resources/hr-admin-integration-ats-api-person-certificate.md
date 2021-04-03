---
title: Zertifkat der Person
description: In diesem Thema wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466519"
---
# <a name="person-certificate"></a>Zertifkat der Person

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersoncertificateentity

## <a name="description"></a>Beschreibung

Diese Entität beschreibt die Berufszertifikate eines Kandidaten.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personenzertifikatsentitätskennung**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz des Personenzertifikats. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Partei-(Personen-)Kennung des Kandidaten. |
| **Personenkennungswert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person). |
| **Zertifikatstypkennung**<br>mshr_certificatetypeid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich |  Der Bezeichner des Zertifikatstyps, der in Human Resources definiert ist. |
| **Wert der Zertifikatstypkennung**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmcertificatetypeentityid von mshr_hcmcertificatetypeentity | Vom System generierter eindeutiger Bezeichner des Zertifikatstyps der zugeordneten Entität. |
| **Startdatum**<br>mshr_startdate<br>*Datetime* | Lesen/Schreiben<br>Erforderlich | Das Datum, an dem das Zertifikat ausgestellt wurde. |
| **Enddatum**<br>mshr_enddate<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Datum, an dem das Zertifikat abläuft. |
| **Notizen**<br>mshr_notes<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Hinweise zur Verwendung durch den Personalbeschaffer oder Personalvermittler. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |  Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann. Kombination aus Parteinummer, Zertifikatstypkennung und Startdatum. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]