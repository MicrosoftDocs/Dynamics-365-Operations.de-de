---
title: Variabler Vergütungsplan für Lohnabrechnung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Variabler Vergütungsplan für Lohnabrechnung“ in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5dc096c08ed808f577c8cdc96ca84000a0b80679
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314392"
---
# <a name="payroll-variable-compensation-plan"></a>Variabler Vergütungsplan für Lohnabrechnung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Variabler Vergütungsplan für Lohnabrechnung“ für Dynamics 365 Human Resources beschrieben.

### <a name="description"></a>Beschreibung

Diese Entität stellt den variablen Vergütungsplan bereit, der einer bestimmten Position eines Mitarbeiters zugewiesen ist.

Physischer Name: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich |Die eindeutige Personalnummer des Mitarbeiters.  |
| **Bewilligungsdatum**</br>mshr_awarddate</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt</br>Erforderlich | Datum der Prämie. |
| **Prämientyp**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType-Optionssatz](hr-admin-integration-payroll-api-award-type.md)* | Schreibgeschützt</br>Erforderlich | Der Typ der Prämie, der für den variablen Vergütungsplan definiert ist. |
| **Währung**</br>mshr_unitcurrencycode</br>*Zeichenfolge* | Schreibgeschützt </br>Erforderlich |Die für den variablen Vergütungsplan festgelegte Währung.   |
| **ID für festen Vergütungsplan**</br>mshr_fixedplanid</br>*Zeichenfolge* | Schreibgeschützt | Der feste Vergütungsplan, der als Basis für die Berechnung der Prämie verwendet wird. |
| **Einheitenwert**</br>mshr_awardamount</br>*Dezimal* | Schreibgeschützt | Der Wert der Einheit |
| **Prozesstyp**</br>mshr_processtype</br>*[mshr_hrmCompProcessType-Optionssatz](hr-admin-integration-payroll-api-process-type.md)* | Schreibgeschützt | Der Prozesstyp. |
| **Typ variabler Vergütungsplan**</br>Zeichenfolge</br>*mshr_typeid* | Schreibgeschützt | Der Typ des variablen Vergütungsplans. |
| **ID für variablen Vergütungsplan**</br>Zeichenfolge</br>*mshr_planid* | Schreibgeschützt | Die ID des variablen Vergütungsplans. |
| **Primärfeld**</br>mshr_primaryfield</br>*GUID* | Schreibgeschützt</br>Vom System generiert. | |
| **Mitarbeiterkennung**</br>mshr_fk_employee_id_value</br>*GUID* | Schreibgeschützt</br>Erforderlich</br>Fremdschlüssel: mshr_Employee_id von mshr_payrollemployeeentity entity  | Mitarbeiterkennung. |
| **Entität „Variabler Vergütungsplan für Lohnabrechnung“**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Erforderlich</br>Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Vergütungsplans. |


## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Antwort**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
