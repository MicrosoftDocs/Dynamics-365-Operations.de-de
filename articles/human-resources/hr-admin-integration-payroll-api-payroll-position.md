---
title: Lohndetails für Positionen
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881988"
---
# <a name="payroll-position"></a>Lohnposition

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohndetails für Positionen“ in Dynamics 365 Human Resources.

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Normale Stunden pro Jahr**<br>annualregularhours<br>*Dezimal* | Schreibgeschützt<br>Erforderlich | Für die Position festgelegte jährliche Regelarbeitszeit.  |
| **ID Entität „Lohndetails für Position“**<br>Payrollpositiondetailsentityid<br>*Guid* | Erforderlich<br>Vom System generiert. | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Position.  |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Erforderlich<br>Vom System generiert |  |
| **Stellen-ID-Wert der Position**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_PayrollPositionJobEntity der mshr_payrollpositionjobentity |Die Kennung der Stelle, die der Position zugeordnet ist.|
| **ID-Wert für festen Vergütungsplan**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_FixedCompPlan_id von mshr_payrollfixedcompensationplanentity  | Die Kennung des festen Vergütungsplans, der der Position zugeordnet ist. |
| **Lohnzyklus-ID**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Der auf der Position definierte Lohnzyklus. |
| **Gezahlt von juristischer Person**<br>paidbylegalentity<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die juristische Person, die für die Zahlung für die Position verantwortlich ist. |
| **Positionskennung**<br>mshr_positionid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Kennung der Position. |
| **Gültig bis**<br>validto<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt<br>Erforderlich |Das Datum, ab dem die Positionsdetails gültig sind.  |
| **Gültig ab**<br>validfrom<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt<br>Erforderlich |Das Datum, bis zu dem die Positionsdetails gültig sind.  |

**Abfrage**

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
