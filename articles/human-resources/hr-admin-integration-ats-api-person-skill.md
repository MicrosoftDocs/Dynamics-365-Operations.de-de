---
title: Qualifikation der Person
description: In diesem Thema wird die Entität „Qualifikation der Person“ für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 03181d6377fdacee0faa600551e8b7ad7c68a76d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059231"
---
# <a name="person-skill"></a>Qualifikation der Person

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Qualifikation der Person“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersonskillentity

## <a name="description"></a>Beschreibung

Diese Entität beschreibt die Qualifikationen eines Kandidaten.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **„Qualifikation der Person“-Entitäts-ID**<br>mshr_hcmpersonskillentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich |   Die Kennung des Datensatzes der zugeordneten Partei (Person). |
| **Personen-ID-Wert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person). |
| **Zertifizierer**<br>mshr_certifier<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Personalnummer der Arbeitskraft, der diese Qualifikation zertifiziert hat. |
| **Zertifizierer-ID-Wert**<br>_mshr_fk_certifier_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmworkerentityid von mshr_hcmworkerentity | Vom System generierter eindeutiger Bezeichner des Arbeitskraftdatensatzes für die Arbeitskraft, der die Qualifikation zertifiziert hat. |
| **Qualifikationskennung**<br>mshr_skillid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Bezeichner der Qualifikation, die in der Human Resources definiert ist. |
| **Wert der Qualifikationskennung**<br>_mshr_fk_skill_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmskillentityid von mshr_hcmskillentity | Der vom System generierte Bezeichner der ausgewählten Qualifikation. |
| **Jahre Erfahrung**<br>mshr_yearsofexperience<br>*Dezimal* | Lesen/Schreiben<br>Optional | Die Jahre Erfahrung des Kandidaten mit dieser Qualifikation. |
| **Bewertungskennung**<br>mshr_ratingid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Bewertungsskalentyp. Für diese Entität ist der Wert **Qualifikation**. |
| **Stufentyp**<br>mshr_leveltype<br>*mshr_hrmskillleveltype-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Eine Typkategorisierung für die Stufe, die der Qualifikation zugewiesen ist. |
| **Stufenkennung**<br>mshr_levelid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Kennung der Bewertungsstufe, die der Kandidat für diese Qualifikation hat. |
| **Wert der Bewertungsstufenkennung**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmratinglevelentityid von mshr_hcmratinglevelentity | Der vom System generierte Bezeichner der Bewertungsstufe. |
| **Stufendatum**<br>mshr_leveldate<br>*Datetime* | Lesen/Schreiben<br>Erforderlich | Das Datum, an dem der Kandidat in der Qualifikation bewertet wurde. |
| **Prüfer der Bewertungsstufe**<br>mshr_ratinglevelexaminer<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Personalnummer der Arbeitskraft, die diesen Kandidaten bewertet hat. |
| **Wert der Kennung des Prüfers der Bewertungsstufe**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmworkerentityid von mshr_hcmworkerentity | Der vom System generierte Bezeichner der Arbeitskraft, die die Qualifikationsstufe des Kandidaten bewertet hat. |
| **Überprüft**<br>mshr_verified<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Gibt an, ob die bewertete Qualifikationsstufe überprüft wurde. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann. Kombination aus Parteinummer, Stufentyp Qualifikationskennung und Stufendatum. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]