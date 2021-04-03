---
title: Personalbeschaffungsantragsposition
description: In diesem Thema wird der die Entität für die Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 4892dc0801a47ab7c219df00b997fa469f56b7fc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464693"
---
# <a name="recruiting-request-position"></a>Personalbeschaffungsantragsposition

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird der die Entität für die Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>Beschreibung

Beschreibt die Position oder Positionen, die für einen Personalbeschaffungsantrag besetzt werden sollen. Das Hinzufügen einer Position zum Personalbeschaffungsantrag ist optional. Die Eigenschaften der Position sind schreibgeschützt, da die Positionseigenschaften im Personalbeschaffungsantrag nicht anders sein sollten als im Positionsstammsatz. Wenn sich die Eigenschaften ändern müssen, sollte dies im Positionsstammdatensatz erfolgen, bevor die Position zum Personalbeschaffungsantrag hinzugefügt wird.

### <a name="json-representation"></a>JSON-Darstellung
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kennung der Personalbeschaffungsantragspositions-Entität**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich |    Vom System generierter Bezeichner des Positionsdatensatzes für den Personalbeschaffungsantrag. |
| **Personalbeschaffungsantragskennung**<br>mshr_recruitingrequestid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Der vom Benutzer lesbare eindeutige Bezeichner des Personalbeschaffungsantrags. |
| **Wert der Personalbeschaffungsantragskennung**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmrecruitingrequestentityid der Entität mshr_hcmrecruitingrequestentity | Vom System generierter Bezeichner des Personalbeschaffungsantrags, dem die Position zugeordnet ist. |
| **Positionskennung**<br>mshr_positionid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Der vom Benutzer lesbare eindeutige Bezeichner der Position. |
| **Positions-ID-Wert**<br>_mshr_fk_position_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmpositionv2entityid von mshr_hcmpositionv2entity-Entität | Vom System generierte Bezeichner der Position. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Positionsbeschreibung. |
| **Positionstypkennung**<br>mshr_positiontypeid<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Der vom Benutzer lesbare eindeutige Bezeichner des Positionstyps für diese Position. |
| **Wert der Positionstypkennung**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmpositiontypeentityid der mshr_hcmpositiontypeentity-Entität | Ein vom System generierter eindeutiger Bezeichner des Positionstyps für diese Position. |
| **Status**<br>mshr_status<br>*RecruitingRequestPositionStatus*-Optionssatz | Lesen/Schreiben<br>Erforderlich | Status der Position für den Personalbeschaffungsantrag. |
| **Abteilungsnummer**<br>mshr_departmentnumber<br>*Zeichenfolge* | Schreibgeschützt<br>Optional<br> | Die Abteilungsnummer der Position. |
| **Wert der Abteilungskennung**<br>_mshr_fk_department_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_omdepartmententityid der Entität mshr_omdepartmententity | Vom System generierter eindeutiger Bezeichnung der Abteilung der Position. |
| **Berichte an Positionskennung**<br>mshr_reportstopositionid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die vom Benutzer lesbare Kennung der Position, an die die rekrutierte Position in der Organisationshierarchie berichtet. |
| **Wert für Berichte an Positionskennung**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmpositionv2entityid von mshr_hcmpositionv2entity-Entität | Die vom System generierte Kennung der Position, an die die rekrutierte Position berichtet. |
| **Berichte an Personalnummer**<br>mshr_reportstopersonnelnumber<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Arbeitskraftkennung der Arbeitskraft, dem der eingestellte Kandidat Bericht erstatten wird. |
| **Wert für Berichte an Arbeitskraftkennung**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmworkerbaseentityid der Entität mshr_hcmworkerbaseentity | Vom System generierte Kennung der Arbeitskraft, der der eingestellte Kandidat Bericht erstatten wird. |
| **Finanzdimension**<br>mshr_financialdimension<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Die Finanzdimension (z. B. Kostenstelle), die der Position zugewiesen ist. Die Finanzdimension wird für jede Position pro juristischer Person zugewiesen. Auf Kostenstellen, die in Dimensionen definiert sind, kann über die Entität mshr_dimattributeomcostcenterentity zugegriffen werden. |
| **Datenbereichskennung**<br>mshr_dataareaid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Gibt die juristische Person (Firma) für den Personalbeschaffungsantragsposition an. |
| **Wert der Datenbereichskennung**<br>_mshr_dataareaid_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: cdm_companyid der Entität cdm_company | Systemgenerierter GUID-Wert, der die juristische Person (Firma) für den Personalbeschaffungsantragsposition identifiziert. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Verkettung des Werts des Personalbeschaffungsantrags und der Positionskennung als weitere Methode zur eindeutigen Identifizierung des Datensatzes. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]