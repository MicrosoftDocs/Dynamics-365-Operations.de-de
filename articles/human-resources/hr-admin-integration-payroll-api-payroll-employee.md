---
title: Mitarbeiter der Lohnbuchhaltung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Mitarbeiter der Lohnbuchhaltung“ in Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: e853a8a5730d397f253c8ce3a330794594dfd907
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068483"
---
# <a name="payroll-employee"></a>Mitarbeiter der Lohnbuchhaltung


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Adresse des Mitarbeiters der Lohnbuchhaltung“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_payrollemployeeentity.

### <a name="description"></a>Beschreibung

Diese Entität stellt Informationen über den Mitarbeiter bereit. Sie müssen die [Lohnintegrationsparameter](hr-admin-integration-payroll-api-parameters.md) festlegen, bevor Sie diese Entität verwenden.

>[!IMPORTANT] 
>Die Felder **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** und **NameValidTo** sind für diese Entität nicht mehr verfügbar. Dadurch wird sichergestellt, dass es nur eine Datenquelle mit gültigem Datum gibt, die diese Entität unterstützt.
>Diese Felder werden auf der **DirPersonNameHistoricalEntity** verfügbar sein, die im Plattform-Update 43 veröffentlicht wurde. Es gibt eine OData-Beziehung von **PayrollEmployeeEntity** zu **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kennung der juristischen Person**</br>mshr_legalentityid</br>*Zeichenfolge* | Schreibgeschützt | Gibt die juristische Person (Firma) an. |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt | Die eindeutige Personalnummer des Mitarbeiters. |
| **Datum des Beschäftigungsbeginns**</br>mshr_employmentstartdate</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Startdatum der Anstellung des Mitarbeiters. |
| **Datum des Beschäftigungsendes**</br>mshr_employmentenddate</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt |Das Enddatum der Anstellung des Mitarbeiters.  |
| **Geburtstag**</br>mshr_birthdate</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Geburtsdatum des Mitarbeiters. |
| **Geschlecht**</br>mshr_gender</br>[mshr_hcmpersongender-Optionssatz](hr-admin-integration-payroll-api-gender.md) | Schreibgeschützt | Das Geschlecht des Mitarbeiters. |
| **Beschäftigungstyp**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype option set](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Schreibgeschützt | Der Beschäftigungstyp. |
| **Identifikationstypkennung**</br>mshr_identificationtypeid</br>*Zeichenfolge* |Schreibgeschützt | Der für den Mitarbeiter festgelegte Identifikationstyp. |
| **Kennungsnummer**</br>mshr_identificationnumber</br>*Zeichenfolge* | Schreibgeschützt |Die für den Mitarbeiter festgelegte Kennungsnummer. |
| **Für Zahlung bereit**</br>mshr_readytopay</br>[mshr_noyes-Optionssatz](hr-admin-integration-payroll-api-no-yes.md) | Schreibgeschützt | Gibt an, ob der Mitarbeiter als zahlungsbereit gekennzeichnet ist. |
| **ID der Entität „Mitarbeiter der Lohnbuchhaltung“**</br>mshr_payrollemployeeentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert (Global Unique Identifier) zum eindeutigen Identifizieren des Mitarbeiters. |

## <a name="relations"></a>Referenzen

|Eigenschaftswert | Zugehörige Entität | Navigationseigenschaft | Erfassungstyp |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Beispielabfrage für Mitarbeiter der Lohnbuchhaltung

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Antwort**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
