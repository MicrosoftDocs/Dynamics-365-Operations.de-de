---
title: Fester Vergütungsplan für Lohnabrechnung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Fester Vergütungsplan für Lohnabrechnung“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: f1e5345d9f27106bdf3a3a60cb0480a9b072e340c01236e4d48c5e2ae592ddbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738390"
---
# <a name="payroll-fixed-compensation-plan"></a>Fester Vergütungsplan für Lohnabrechnung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Fester Vergütungsplan für Lohnabrechnung“ für Dynamics 365 Human Resources beschrieben.

### <a name="description"></a>Beschreibung

Diese Entität stellt den festen Vergütungsplan bereit, der einer bestimmten Position eines Mitarbeiters zugewiesen ist.

Physischer Name: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Mitarbeiterkennung**<br>mshr_fk_employee_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_Employee_id von mshr_payrollemployeeentity entity  | Mitarbeiterkennung |
| **Lohnsatz**<br>mshr_payrate<br>*Dezimal* | Schreibgeschützt<br>Erforderlich | Im festen Vergütungsplan definierter Lohnsatz. |
| **Plankennung**<br>mshr_planid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |Gibt den Vergütungsplan an.  |
| **Gültig ab**<br>mshr_validfrom<br>*Datum-/Uhrzeit-Offset* |  Schreibgeschützt<br>Erforderlich |Datum, ab dem der feste Vergütungsplan für den Mitarbeiter gültig sind.  |
| **Entität „Fester Vergütungsplan für Lohnabrechnung“**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Erforderlich<br>Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Vergütungsplans. |
| **Lohnzahlungshäufigkeit**<br>mshr_payfrequency<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |Die Häufigkeit, mit der der Mitarbeiter bezahlt wird.  |
| **Gültig bis**<br>mshr_validto<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Datum, bis zu dem der feste Vergütungsplan für den Mitarbeiter gültig ist. |
| **Positionskennung**<br>mshr_positionid<br>*Zeichenfolge* | Schreibgeschützt <br>Erforderlich | Positionskennung, die mit dem Mitarbeiter und dem Beitritt zum festen Vergütungsplan verknüpft ist. |
| **Währung**<br>mshr_currency<br>*Zeichenfolge* | Schreibgeschützt <br>Erforderlich |Die für den festen Vergütungsplan definierte Währung   |
| **Personalnummer**<br>mshr_personnelnumber<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich |Die eindeutige Personalnummer des Mitarbeiters.  |

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
