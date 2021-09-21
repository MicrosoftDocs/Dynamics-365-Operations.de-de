---
title: Fester Vergütungsplan für Lohnabrechnung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Fester Vergütungsplan für Lohnabrechnung“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: dcb253fabbb183003048119c7a627bf0ab960050
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429227"
---
# <a name="payroll-fixed-compensation-plan"></a>Fester Vergütungsplan für Lohnabrechnung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Fester Vergütungsplan für Lohnabrechnung“ für Dynamics 365 Human Resources beschrieben.

### <a name="description"></a>Beschreibung

Diese Entität stellt den festen Vergütungsplan bereit, der einer bestimmten Position eines Mitarbeiters zugewiesen ist.

Physischer Name: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Plankennung**</br>mshr_planid</br>*Zeichenfolge* | Schreibgeschützt | Gibt den Vergütungsplan an.  |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt | Die eindeutige Personalnummer des Mitarbeiters. |
| **Lohnsatz**</br>mshr_payrate</br>*Dezimal* | Schreibgeschützt | Im festen Vergütungsplan definierter Lohnsatz. |
| **Positionskennung**</br>mshr_positionid</br>*Zeichenfolge* | Schreibgeschützt | Positionskennung, die mit dem Mitarbeiter und dem Beitritt zum festen Vergütungsplan verknüpft ist. |
| **Gültig ab**</br>mshr_validfrom</br>*Datum-/Uhrzeit-Offset* |  Schreibgeschützt | Datum, ab dem der feste Vergütungsplan für den Mitarbeiter gültig sind.  |
| **Gültig bis**</br>mshr_validto</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Datum, bis zu dem der feste Vergütungsplan für den Mitarbeiter gültig ist. |
| **Lohnzahlungshäufigkeit**</br>mshr_payfrequency</br>*Zeichenfolge* | Schreibgeschützt | Die Häufigkeit, mit der der Mitarbeiter bezahlt wird.  |
| **Währung**</br>mshr_currency</br>*Zeichenfolge* | Schreibgeschützt | Die für den festen Vergütungsplan definierte Währung. |
| **Entität „Fester Vergütungsplan für Lohnabrechnung“**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Vergütungsplans. |

## <a name="relations"></a>Referenzen

|Eigenschaftswert | Zugehörige Entität | Navigationseigenschaft | Erfassungstyp |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Antwort**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
