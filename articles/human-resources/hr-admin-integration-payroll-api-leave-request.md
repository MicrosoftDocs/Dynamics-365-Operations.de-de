---
title: Urlaubsantrag
description: Dieser Artikel enthält Details und eine Beispielabfrage für die Entität „Urlaubsantrag“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899671"
---
# <a name="leave-request"></a>Urlaubsantrag


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird die Entität „Urlaubsantrag“ für Dynamics 365 Human Resources beschrieben.

### <a name="description"></a>Description

Diese Entität stellt Informationen für eine Urlaubsanforderung bereit.

Physischer Name: mshr_essleaverequestentity.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Anforderungskennung**</br>mshr_requestid</br>*Zeichenfolge* | Schreibgeschützt | Die Anforderungs-ID. |
| **Kennung des Urlaubstyps**</br>mshr_leavetypeid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung des Urlaubstyps. |
| **Datum**</br>mshr_leavedate</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum der Urlaubsanforderung. |
| **Betrag**</br>mshr_amount</br>*Dezimal* | Schreibgeschützt | Die Menge der Urlaubsanforderung. |
| **Typ „halber Tag“**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition-Optionssatz* | Schreibgeschützt | Die Typ des halbtägigen Urlaubs. |
| **Kommentar**</br>mshr_comments</br>*Zeichenfolge* | Schreibgeschützt | Kommentar zur Anforderung. |
| **Status**</br>mshr_status</br>*mshr_status-Optionssatz* | Schreibgeschützt | Der Status der Anfrage. |
| **Datum**</br>mshr_requestdate</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum der Anforderung. |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt | Die eindeutige Personalnummer des Mitarbeiters. |
| **Ursachencodekennung**</br>mshr_reasoncodeid</br>*Zeichenfolge* | Schreibgeschützt | Die Ursachencodekennung. |
| **Datenbereichskennung**</br>mshr_dataareaid</br>*Zeichenfolge* | Schreibgeschützt | Gibt die juristische Person (Firma) an. |
| **Primärfeld**</br>mshr_primaryfield</br>*GUID* | Schreibgeschützt</br>Vom System generiert | |
| **Urlaubsanforderungsentität**</br>mshr_essleaverequestentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Urlaubsanforderung. |

## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Antwort**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
