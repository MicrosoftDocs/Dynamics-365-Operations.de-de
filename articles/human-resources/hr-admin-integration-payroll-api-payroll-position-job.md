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
ms.openlocfilehash: 842c459acd8b5e1a8b6074243b3afa18dc6a13c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314236"
---
# <a name="payroll-position-job"></a>Lohnpositions-Einzelvorgang

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt die Entität „Lohnpositionsstelle“ in Dynamics 365 Human Resources.

### <a name="description"></a>Beschreibung

Diese Entität stellt die Beziehung zwischen Position und einer Stelle für einen bestimmten festen Vergütungsplan bereit.

Physischer Name: mshr_payrollpositionjobentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Einzelvorgangskennung**<br>mshr_jobid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |Der ID der Stelle. |
| **Gültig ab**<br>mshr_validto<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Datum, ab dem die Position und das Arbeitsverhältnis gültig sind. |
| **Gültig bis**<br>mshr_validto<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Datum, bis zu dem die Position und das Arbeitsverhältnis gültig sind.  |
| **Positionskennung**<br>mshr_positionid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Kennung der Position. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Erforderlich<br>Vom System generiert |  |
| **Stellen-ID-Wert der Position**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_PayrollPositionJobEntity der mshr_payrollpositionjobentity |Die Kennung der Stelle, die der Position zugeordnet ist.|
| **ID-Wert für festen Vergütungsplan**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_FixedCompPlan_id von mshr_payrollfixedcompensationplanentity  | Die Kennung des festen Vergütungsplans, der der Position zugeordnet ist. |
| **ID der Entität „Lohnpositions-Stelle“**<br>mshr_payrollpositionjobentityid<br>*Guid* | Erforderlich<br>Vom System generiert. | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Stelle.  |

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
