---
title: Ausbildung des Personalbeschaffungsantrags
description: In diesem Thema wird die Entität für die Ausbildung des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126073"
---
# <a name="recruiting-request-education"></a>Ausbildung des Personalbeschaffungsantrags

In diesem Thema wird die Entität für die Ausbildung des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>Beschreibung

Beschreibt die Ausbildungsanforderungen für eine RecruitingRequest.

### <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kennung der Personalbeschaffungsantragsausbildung-Entität**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Datensatz Personalbeschaffungsantragsausbildung. |
| **Personalbeschaffungsantragskennung**<br>mshr_recruitingrequestid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Der vom Benutzer lesbare eindeutige Bezeichner des zugehörigen Personalbeschaffungsantrags. |
| **Wert der Personalbeschaffungsantragskennung**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmrecruitingrequestentityid von mshr_hcmrecruitingrequestentity | Vom System generierter eindeutiger Bezeichner des zugehörigen Personalbeschaffungsantrags. |
| **Ausbildungsgradskennung**<br>mshr_educationlevelid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Die erforderliche Stufe der Ausbildung. |
| **Wert der Ausbildungsgradskennung**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmeducationlevelentityid von mshr_hcmeducationlevelentity | Vom System generierter eindeutiger Bezeichner der erforderlichen Stufe der Ausbildung. |
| **Beschreibung des Ausbildungsstufe**<br>mshr_educationleveldescription<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Beschreibung der erforderlichen Stufe für die Qualifikation. |
| **Ausbildungsfachkennung**<br>mshr_educationdisciplinedescription<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Der Bereich des Ausbildungsfachs. |
| **Wert der Ausbildungsfachkennung**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmeducationdisciplineentityid von mshr_hcmeducationdisciplineentity | Vom System generierter eindeutiger Bezeichner des Gebiets des Ausbildungsfachs. |
| **Beschreibung des Ausbildungsfachs**<br>mshr_educationdisciplinedescription<br>Zeichenfolge | Schreibgeschützt<br>Erforderlich | Die Beschreibung des Gebiets des Ausbildungsfachs. |
| **Datenbereichskennung**<br>mshr_dataareaid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Gibt die juristische Person (Firma) an.|
| **Wert der Datenbereichskennung**<br>_mshr_dataareaid_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: cdm_companyid der Entität cdm_company | Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Verkettung des Werts des Personalbeschaffungsantrags, der Ausbildungsstufenkennung und der Ausbildungsfachkennung als weitere Methode zur eindeutigen Identifizierung des Datensatzes. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]