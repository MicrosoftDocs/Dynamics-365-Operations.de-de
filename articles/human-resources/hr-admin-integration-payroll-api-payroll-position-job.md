---
title: Lohnpositionsstelle
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohnpositionsstelle“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 349479d9e77861b54d879bcfd93f7af0e38cff95
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069831"
---
# <a name="payroll-position-job"></a>Lohnpositions-Einzelvorgang


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt die Entität „Lohnpositionsstelle“ in Dynamics 365 Human Resources.

### <a name="description"></a>Beschreibung

Diese Entität stellt die Beziehung zwischen Position und einer Stelle für einen bestimmten festen Vergütungsplan bereit.

Physischer Name: mshr_payrollpositionjobentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Positionskennung**</br>mshr_positionid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung der Position. |
| **Gültig ab**</br>mshr_validto</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum, ab dem die Position und das Arbeitsverhältnis gültig sind. |
| **Gültig bis**</br>mshr_validto</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum, bis zu dem die Position und das Arbeitsverhältnis gültig sind. |
| **Einzelvorgangskennung**</br>mshr_jobid</br>*Zeichenfolge* | Schreibgeschützt | Der ID der Stelle. |
| **Primärfeld**</br>mshr_primaryfield</br>*Zeichenfolge* | Vom System generiert | Das Primärfeld. |
| **ID der Entität „Lohnpositions-Stelle“**</br>mshr_payrollpositionjobentityid</br>*Guid* | Vom System generiert. | Ein vom System generierter GUID-Wert (Global Unique Identifier) zum eindeutigen Identifizieren des Einzelvorgangs. |

## <a name="relations"></a>Referenzen

| Eigenschaftswert | Zugehörige Entität | Navigationseigenschaft | Erfassungstyp |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Nicht zutreffend |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Antwort**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
