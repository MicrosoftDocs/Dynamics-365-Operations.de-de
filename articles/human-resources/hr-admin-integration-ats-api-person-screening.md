---
title: Personenprüfung
description: In diesem Thema wird die Screening-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059279"
---
# <a name="person-screening"></a>Personenprüfung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Screening-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersonscreeningentity

## <a name="description"></a>Beschreibung

Diese Entität beschreibt Screenings, die ein Kandidat bestanden hat oder für eine Anstellung bestehen muss.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personen-Screening-Entitätskennung**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Eindeutiger primärer Bezeichner für den Personen-Screening-Datensatz. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die dem Kandidaten zugeordnete Partei-(Personen-)Nummer. |
| **Personenkennungswert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person). |
| **Screening-Typ-Kennung**<br>mshr_screeningtypeid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich<br>Fremdschlüssel: ScreeningType | Der Bezeichner des Screening-Typs, der in Human Resources definiert ist. |
| **Wert der Screening-Typ-Kennung**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmscreeningtypeentityid von mshr_hcmscreeningtypeentity | Vom System generierter Bezeichner für den Screening-Typ-Datensatz der zugeordneten Entität. |
| **Erforderlich bis**<br>mshr_requiredby<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Datum, bis zu dem das Screening abgeschlossen sein muss. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus-Optionssatz*<br>Lesen/Schreiben<br>Erforderlich | Gibt den Status des Kandidaten für das Screening an. |
| **Abschlussdatum**<br>mshr_completeddate<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Datum, an dem das Screening abgeschlossen wurde. |
| **Notizen**<br>mshr_note<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Hinweise zur Verwendung durch den Personalbeschaffer oder Personalvermittler. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]