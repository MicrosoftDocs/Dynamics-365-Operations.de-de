---
title: Mitarbeiter der Lohnbuchhaltung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Mitarbeiter der Lohnbuchhaltung“ in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 57501d07f6b9cffdff9f37737df8c278c574cf30
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314284"
---
# <a name="payroll-employee"></a>Mitarbeiter der Lohnbuchhaltung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Adresse des Mitarbeiters der Lohnbuchhaltung“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_payrollemployeeentity.

### <a name="description"></a>Beschreibung

Diese Entität stellt Informationen über den Mitarbeiter bereit. Sie müssen die [Lohnintegrationsparameter](hr-admin-integration-payroll-api-parameters.md) festlegen, bevor Sie diese Entität verwenden.

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personalnummer**<br>mshr_personnelnumber<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die eindeutige Personalnummer des Mitarbeiters. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Erforderlich<br>Vom System generiert |  |
| **Nachname**<br>mshr_lastname<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Nachname des Mitarbeiters. |
| **Kennung der juristischen Person**<br>mshr_legalentityID<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Gibt die juristische Person (Firma) an. |
| **Gültig ab**<br>mshr_namevalidfrom<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Datum, ab dem die Mitarbeiterinformationen gültig sind.  |
| **Geschlecht**<br>mshr_gender<br>[mshr_hcmpersongender-Optionssatz](hr-admin-integration-payroll-api-gender.md) | Schreibgeschützt<br>Erforderlich | Das Geschlecht des Mitarbeiters. |
| **ID der Entität „Mitarbeiter der Lohnbuchhaltung“**<br>mshr_payrollemployeeentityid<br>*GUID* | Erforderlich<br>Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Mitarbeiters. |
| **Datum des Beschäftigungsbeginns**<br>mshr_employmentstartdate<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt<br>Erforderlich | Das Startdatum der Anstellung des Mitarbeiters. |
| **Identifikationstypkennung**<br>mshr_identificationtypeid<br>*Zeichenfolge* |Schreibgeschützt<br>Erforderlich | Der für den Mitarbeiter festgelegte Identifikationstyp. |
| **Datum des Beschäftigungsendes**<br>mshr_employmentenddate<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt<br>Erforderlich |Das Enddatum der Anstellung des Mitarbeiters.  |
| **Datenbereichskennung**<br>mshr_dataareaid_id<br>*GUID* | Erforderlich <br>Vom System generiert | Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert. |
| **Gültig bis**<br>mshr_namevalidto<br>*Datum-/Uhrzeit-Offset* |  Schreibgeschützt<br>Erforderlich | Datum, bis zu dem die Mitarbeiterinformationen gültig sind. |
| **Geburtstag**<br>mshr_birthdate<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Das Geburtsdatum des Mitarbeiters |
| **Kennungsnummer**<br>mshr_identificationnumber<br>*Zeichenfolge* | Schreibgeschützt <br>Erforderlich |Die für den Mitarbeiter festgelegte Kennungsnummer.  |
| **Vorname**<br>mshr_firstname<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Vorname des Mitarbeiters. |
| **Zweiter Vorname**<br>mshr_middlename<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |Zweiter Vorname des Mitarbeiters.  |

## <a name="example-query-for-payroll-employee"></a>Beispielabfrage für Mitarbeiter der Lohnbuchhaltung

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Antwort**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_firstname": "Cassie",
    "mshr_middlename": "Lassie",
    "mshr_lastname": "Hicks",
    "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
    "mshr_namevalidto": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]