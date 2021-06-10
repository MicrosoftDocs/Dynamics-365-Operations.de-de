---
title: Qualifikation des Personalbeschaffungsantrags
description: In diesem Thema wird die „Qualifikation für Personalbeschaffungsanträge“-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 52dc7a839249ad8d55bb1f52cc5efe15cdf18e13
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059207"
---
# <a name="recruiting-request-skill"></a>Qualifikation des Personalbeschaffungsantrags

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die „Qualifikation für Personalbeschaffungsanträge“-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>Beschreibung

Beschreibt die Qualifikationsanforderungen für eine RecruitingRequest.

### <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kennung der Personalbeschaffungsantragsqualifikations-Entität**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Datensatz **Personalbeschaffungsantragsqualifikation**. |
| **Personalbeschaffungsantragskennung**<br>mshr_recruitingrequestid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Der vom Benutzer lesbare eindeutige Bezeichner des zugehörigen Personalbeschaffungsantrags. |
| **Wert der Personalbeschaffungsantragskennung**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br> Fremdschlüssel: mshr_hcmrecruitingrequestentityid der Entität mshr_hcmrecruitingrequestentity | Vom System generierter eindeutiger Bezeichner des zugehörigen Personalbeschaffungsantrags. |
| **Qualifikationskennung**<br>mshr_skillid<br>*Zeichenfolge*<br> | Einmal schreiben<br>Erforderlich | Der vom Benutzer lesbare eindeutige Bezeichner des erforderlichen Qualifikation. |
| **Wert der Qualifikationskennung**<br>_mshr_fk_skill_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmskillentityid der Entität mshr_hcmskillentity | Vom System generierter eindeutiger Bezeichner der erforderlichen Qualifikation. |
| **Bewertungsstufenkennung**<br>mshr_ratinglevelid<br>*Zeichenfolge* | Einmal schreiben<br>Optional | Der Wert der erforderlichen Qualifikationsstufe, die für die Stelle ausgewählt wurde, basierend auf dem der Qualifikation zugewiesenen Bewertungsmodell. |
| **Wert der Bewertungsstufenkennung**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmratinglevelentityid der Entität mshr_hcmratinglevelentity | Vom System generierter eindeutiger Bezeichner der Stufe. |
| **Qualifikationsbeschreibung**<br>mshr_skilldescription<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Qualifikationsbeschreibung. |
| **Beschreibung der Bewertungsstufe**<br>mshr_ratingleveldescription<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Die Beschreibung der ausgewählten Qualifikationsstufe. |
| **Datenbereichskennung**<br>mshr_dataareaid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Gibt die juristische Person (Firma) an. |
| **Wert der Datenbereichskennung**<br>_mshr_dataareaid_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: cdm_companyid der Entität cdm_company | Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Verkettung des Werts des Personalbeschaffungsantrags und der Qualifikationskennung als weitere Methode zur eindeutigen Identifizierung des Datensatzes. |
| **Bewertungsmodellkennung**<br>mshr_ratingmodelid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Das Bewertungsmodell zur Bewertung der Qualifikation. |
| **Wert der Bewertungsmodellkennung**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmratingmodelentityid der Entität mshr_hcmratingmodelentity | Vom System generierter eindeutiger Bezeichner des Bewertungsmodells, das zur Bewertung der Qualifikation verwendet wird. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]