---
title: Lohndetails für Positionen
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069806"
---
# <a name="payroll-position"></a>Lohnposition


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt die Entität „Lohnposition“ in Dynamics 365 Human Resources.

Physischer Name: mshr_payrollpositionentity.

### <a name="description"></a>Beschreibung

Diese Entität stellt positionsbezogene Informationen für einen bestimmten Mitarbeiter bereit.

Physischer Name: mshr_payrollpositionentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Positionskennung**</br>mshr_positionid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung der Position. |
| **Lohnzyklus-ID**</br>mshr_paycycleid</br>*Zeichenfolge* | Schreibgeschützt | Der für die Position definierte Lohnzyklus. |
| **Normale Stunden pro Jahr**</br>annualregularhours</br>*Dezimal* | Schreibgeschützt | Die normalen Stunden pro Jahr, die für die Position definiert sind. |
| **Gezahlt von juristischer Person**</br>paidbylegalentity</br>*Zeichenfolge* | Schreibgeschützt | Die juristische Person, die für die Position definiert und für die Zahlung verantwortlich ist. |
| **Gültig bis**</br>validto</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum, bis zu dem die Positionsdetails gültig sind. |
| **Gültig ab**</br>validfrom</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum, ab dem die Positionsdetails gültig sind. |
| **Primärfeld**</br>mshr_primaryfield</br>*Zeichenfolge* | Vom System generiert | Das Primärfeld. |
| **ID Entität „Lohndetails für Position“**</br>Payrollpositiondetailsentityid</br>*Guid* | Erforderlich</br>Vom System generiert. | Ein vom System generierter GUID-Wert (Global Unique Identifier) zum eindeutigen Identifizieren der Position. |

## <a name="relations"></a>Referenzen

| Eigenschaftswert | Zugehörige Entität | Navigationseigenschaft | Erfassungstyp |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Nicht zutreffend |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Nicht zutreffend |

## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Antwort**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
