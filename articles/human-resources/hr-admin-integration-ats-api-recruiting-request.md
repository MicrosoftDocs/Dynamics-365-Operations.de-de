---
title: Personalbeschaffungsantrag
description: In diesem Thema wird die Personalbeschaffungsantrag-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 572ee0755e331d19b41442e3614effb92db95a92
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125424"
---
# <a name="recruiting-request"></a>Personalbeschaffungsantrag

In diesem Thema wird die Personalbeschaffungsantrag-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequestentity

### <a name="description"></a>Beschreibung

Beschreibt einen Personalbeschaffungsantrag für eine Stelle.

### <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personalbeschaffungsantragskennung**<br>mshr_recruitingrequestid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Ein vom Benutzer lesbarer eindeutiger Bezeichner für die in der HR-Anwendung angezeigte Anforderung. Nummernkreis. |
| **Kennung der Personalbeschaffungsentität**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Personalbeschaffungsantrags. |
| **Datenbereichskennung**<br>mshr_dataareaid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional<br> | Gibt die juristische Person (Firma) für den Personalbeschaffungsantrag an. |
| **Wert der Datenbereichskennung**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Schreibgeschützt<br>Optional<br>Fremdschlüssel: cdm_companyid der Entität cdm_company | Systemgenerierter GUID-Wert, der die juristische Person (Firma) für den Personalbeschaffungsantrag identifiziert. |
| **Einstellungsmanager-Personalnummer**<br>mshr_hiringmanagerpersonnelnumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Personalnummer des Einstellungsmanagers, der diesem Personalbeschaffungsantrag zugeordnet ist. |
| **Wert der Einstellungsmanagerkennung**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmworkerbaseentityid der Entität mshr_hcmworkerbaseentity | Vom System generierter GUID-Wert zur Identifizierung des Managers, der dem Personalbeschaffungsantrag zugeordnet ist. |
| **Personalvermittler-Parteinummer**<br>mshr_recruiterpartynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Personen(Partei)-Nummer des für die Anfrage ausgewählten Personalvermittlers. |
| **Wert der Personalvermittlerkennnung**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_dirpersonentityid der Entität mshr_dirpersonentity | Vom System generierter GUID-Wert zur Identifizierung des Personalvermittlers, der dem Personalbeschaffungsantrag zugeordnet ist. |
| **Status**<br>mshr_status<br>*RecruitingRequestStatus* Optionssatz | Lesen/Schreiben<br>Erforderlich<br> | Gibt den Status des Personalbeschaffungsantrags an. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Beschreibt die Anfrage. |
| **Personalbeschaffungsantragsstandort-Kennung**<br>mshr_recruitingrequestlocationid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der vom Benutzer lesbare eindeutige Bezeichner des mit dieser Anforderung verknüpften Stellenstandorts. |
| **Wert der Personalbeschaffungsstandort-Kennung**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmrecruitingrequestlocationentityid der Entität mshr_hcmrecruitingrequestlocationentity | Vom System generierter GUID-Wert zur Identifizierung des Personalbeschaffungsstandorts, der für diesen Antrag ausgewählt wurde. |
| **Kommentare**<br>mshr_comments<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Kommentare zum Antrag zur Verwendung durch Personalchefs und Personalvermittler. |
| **Einzelvorgangskennung**<br>mshr_jobid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich |   Der vom Benutzer lesbare eindeutige Bezeichner der Stelle, die für allen mit dieser Anforderung verknüpften Positionen freigegeben wird. |
| **Stellenkennungswert**<br>_mshr_fk_job_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmjobentityid der Entität mshr_hcmjobentity | Der vom System generierte eindeutige Bezeichner der Stelle, die für allen mit diesem Personalbeschaffungsantrag verknüpften Positionen freigegeben wird. |
| **Titel-ID**<br>mshr_titleid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Der vom Benutzer lesbare eindeutige Bezeichner der mit dieser Anforderung verknüpften Position. |
| **Titel-ID-Wert**<br>_mshr_fk_title_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmtitleid der Entität mshr_hcmtitleentity | Der vom System generierte eindeutige Bezeichner des Titels der Stelle, die für den Personalbeschaffungsantrag ausgewählt wurde. |
| **Stellenfunktionskennung**<br>mshr_jobfunctionid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_jobfunctionid der Entität mshr_hcmjobfunctionentity | Der vom Benutzer lesbare eindeutige Bezeichner der mit dieser Anforderung verknüpften Stellenfunktion. |
| **Standardmäßige Vollzeitäquivalenz**<br>mshr_defaultfulltimeequivalency<br>*Doppelt* | Schreibgeschützt<br>Erforderlich | Der äquivalente Vollzeitwert für die Stelle, wobei 1,0 einen Vollzeitbeschäftigten darstellt. |
| **Regulatorische Stellenkategorie**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory*-Optionssatz | Schreibgeschützt<br>Optional | Die EEO-Stellenkategorie der für die Stelle ausgewählten Stellenfunktion. Gültige Werte, die im Optionssatz HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) enthalten sind. |
| **Stellentypskennung**<br>mshr_jobtypeid<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Der Typ der Stele, die der Position zugeordnet ist. Die Stellentypen sind benutzerdefinierte Werte, die in der Entität mshr_hcmjobtypeentity verfügbar sind. |
| **Wert der Stellentypkennung**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmjobtypeentityid der Entität mshr_hcmjobtypenentity | Der vom System generierte eindeutige Bezeichner des Stellentyps, der mit der Stelle für den Personalbeschaffungsantrag verknüpft ist. |
| **Befreiungsstatus**<br>mshr_exemptstatus<br>*JobExemptStatus*-Optionssatz | Schreibgeschützt<br>Optional | Der FLSA-Ausnahmestatus basierend auf dem Stellentyp. |
| **Geschätztes Startdatum**<br>mshr_estimatedstartdate<br>*Datum* | Lesen/Schreiben<br>Erforderlich | Das voraussichtliche Datum, an dem ein Kandidat seine Arbeit aufnehmen würde. |
| **Externe Beschreibung**<br>mshr_externaldescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Eine Beschreibung der Stelle/der Position für den Kandidaten. | Untergrenze der Vergütung<br>mshr_compensationlowthreshold<br>*Doppelt* | Lesen/Schreiben<br>Optional | Untergrenze für die Vergütungsstufe. |
| **Vergütungskontrollpunkt**<br>mshr_compensationcontrolpoint<br>*Doppelt* | Lesen/Schreiben<br>Optional | Kontrollpunkt für die Vergütungsstufe. |
| **Höchstgrenze der Vergütung**<br>mshr_compensationhighthreshold<br>*Doppelt* | Lesen/Schreiben<br>Optional | Höchstgrenze für die Vergütungsstufe. |
| **Vergütungsstufe**<br>mshr_compensationlevelid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Vergütungsstufe der Stelle. Eine Stelle kann mit mehreren Vergütungsstufen eingerichtet werden. Dieses Attribut gibt die ausgewählte Stellenvergütungsstufe für diese Anforderung an. |
| **Stellenvergütungskennung**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmjobcompensationentityid der Entität mshr_hcmjobcompensationentity | Der vom System generierte eindeutige Bezeichner für die Vergütungsstufe, die mit der Stele des Personalbeschaffungsantrags verknüpft ist. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]