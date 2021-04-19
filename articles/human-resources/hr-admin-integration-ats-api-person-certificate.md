---
title: Zertifkat der Person
description: In diesem Thema wird die Personenzertifikats-Entität für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 796a57a5f97de08ff8c8440bc00d4dc5ced18f58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798128"
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