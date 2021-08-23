---
title: Urlaubstyp
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Urlaubstyp“ in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e64b533ad7be23060701e8826a25736a078b59d1ecf824bee0e2dd05c9c78f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713101"
---
# <a name="leave-type"></a>Urlaubstyp

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Urlaubstyp“ für Dynamics 365 Human Resources beschrieben.

### <a name="description"></a>Beschreibung

Diese Entität stellt Informationen für einen bestimmten Urlaubstyp bereit.

Physischer Name: mshr_essleavetypeentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kennung des Urlaubstyps**</br>mshr_leavetypeid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung des Urlaubstyps. |
| **Beschreibung**</br>mshr_description</br>*Zeichenfolge* | Schreibgeschützt | Eine Beschreibung des Urlaubstyps. |
| **Kategorie**</br>mshr_category</br>*mshr_LeaveTypeCategory-Optionssatz* | Schreibgeschützt | Die Kategorie des Urlaubstyps. |
| **Erforderlicher Ursachencode**</br>mshr_isreasoncoderequired</br>*mshr_NoYes-Optionssatz* | Schreibgeschützt | Definiert, ob ein Ursachencode für den Urlaubstyp erforderlich ist. |
| **Urlaubseinheit**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit-Optionssatz* | Schreibgeschützt | Die Einheit dieses Urlaubstyps. |
| **Halben Tag aktivieren**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes-Optionssatz* | Legt fest, ob halber Tag für den Urlaubstyp aktiviert ist. |
| **Datenbereichskennung**</br>mshr_dataareaid_id</br>*Zeichenfolge* | Schreibgeschützt | Gibt die juristische Person (Firma) an. |
| **Urlaubsanforderungsentität**</br>mshr_essleavetypeentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung des Urlaubstyps. |

## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Antwort**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
