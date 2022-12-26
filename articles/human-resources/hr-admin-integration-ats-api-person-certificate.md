---
title: Zertifkat der Person
description: In diesem Artikel wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887316"
---
# <a name="person-certificate"></a>Zertifkat der Person


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.

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

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Description |
| --- | --- | --- |
| **Zertifikatstypkennung**<br>mshr_certificatetypeid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich |  Der Bezeichner des Zertifikatstyps, der in Human Resources definiert ist. |
| **Startdatum**<br>mshr_startdate<br>*Datetime* | Lesen/Schreiben<br>Erforderlich | Das Datum, an dem das Zertifikat ausgestellt wurde. |
| **Enddatum**<br>mshr_enddate<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Datum, an dem das Zertifikat abläuft. |
| **Notizen**<br>mshr_notes<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Hinweise zur Verwendung durch den Personalbeschaffer oder Personalvermittler. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Partei-(Personen-)Kennung des Kandidaten. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |  Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann. Kombination aus Parteinummer, Zertifikatstypkennung und Startdatum. |
| **Wert der Zertifikatstypkennung**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmcertificatetypeentityid von mshr_hcmcertificatetypeentity | Vom System generierter eindeutiger Bezeichner des Zertifikatstyps der zugeordneten Entität. |
| **Personen-ID-Wert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person). |
| **Personenzertifikatsentitätskennung**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz des Personenzertifikats. |




## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
