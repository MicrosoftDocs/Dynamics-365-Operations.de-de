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
ms.openlocfilehash: 62b9caf94f1c9aa8bb5758e62565fe57dfdd245a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055027"
---
# <a name="payroll-position-job"></a>Lohnpositionsstelle

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Lohnposition-Arbeitsverhältnis“ in Dynamics 365 Human Resources.

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Stellenkennung**<br>mshr_jobid<br>*Zeichenfolge* | Readp-only<br>Erforderlich |Der ID der Stelle. |
| **Gültig ab**<br>mshr_validto<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Datum, ab dem die Position und das Arbeitsverhältnis gültig sind. |
| **Gültig bis**<br>mshr_validto<br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt <br>Erforderlich | Datum, bis zu dem die Position und das Arbeitsverhältnis gültig sind.  |
| **Positionskennung**<br>mshr_positionid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Die Kennung der Position. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Erforderlich<br>Vom System generiert |  |
| **Stellen-ID-Wert der Position**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_PayrollPositionJobEntity der mshr_payrollpositionjobentity |Die Kennung der Stelle, die der Position zugeordnet ist.|
| **ID-Wert für festen Vergütungsplan**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_FixedCompPlan_id von mshr_payrollfixedcompensationplanentity  | Die Kennung des festen Vergütungsplans, der der Position zugeordnet ist. |
| **ID der Entität „Lohnpositions-Stelle“**<br>mshr_payrollpositionjobentityid<br>*Guid* | Erforderlich<br>Vom System generiert. | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Stelle.  |

