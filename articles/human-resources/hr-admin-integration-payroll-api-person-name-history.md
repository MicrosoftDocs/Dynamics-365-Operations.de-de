---
title: Verlauf des Personennamens
description: Dieser Artikel enthält Details und eine Beispielabfrage für die Entität „Verlauf des Personennamens“ in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875770"
---
# <a name="person-name-history"></a>Verlauf des Personennamens


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird die Entität „Verlauf des Personennamens“ in Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Beschreibung

Diese Entität stellt Informationen über den den Namensverlauf für eine bestimmte Arbeitskraft bereit.

> [!IMPORTANT] 
> Die Felder **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** und **NameValidTo** sind für die Entität „Mitarbeiter der Lohnbuchhaltung“ nicht mehr verfügbar. Sie wurden entfernt, um sicherzustellen, dass es nur eine Datenquelle mit gültigem Datum gibt, die diese Entität unterstützt.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Vorname**</br>mshr_firstname</br>*Zeichenfolge* | Schreibgeschützt | Der Vorname. |
| **Präfix für Nachname**</br>mshr_lastnameprefix</br>*Zeichenfolge*) | Schreibgeschützt | Das Präfix des Nachnamens. |
| **Nachname**</br>mshr_lastname</br>*Zeichenfolge*) | Schreibgeschützt | De Nachname. |
| **Zweiter Vorname**</br>mshr_middlename</br>*Zeichenfolge*) | Schreibgeschützt | Der zweite Vorname. |
| **Gültig bis**</br>mshr_validto</br>*Zeichenfolge*) | Schreibgeschützt | Das Datum, bis zu dem der Name gültig ist. |
| **Parteinummer**</br>mshr_partynumber</br>*Zeichenfolge* | Schreibgeschützt | Ein vom Benutzer lesbarer und vom System generierter eindeutiger Bezeichner für die Person. |
| **Primärfeld**</br>mshr_primaryfield</br>*Zeichenfolge* | Schreibgeschützt | Der eindeutige Bezeichner des Quelldatensatzes. |
| **ID der Entität „Verlauf des Personennamens“**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert (Global Unique Identifier) zum eindeutigen Identifizieren des Datensatzes. |

## <a name="relations"></a>Referenzen

| Eigenschaftswert | Zugehörige Entität | Navigationseigenschaft | Erfassungstyp |
| --- | --- | --- | --- |
| Nicht zutreffend | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Nicht zutreffend | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Beispielabfrage für Mitarbeiter der Lohnbuchhaltung

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Antwort**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
