---
title: Lohn – Adresse der Arbeitskraft
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Adresse der Arbeitskraft“ in Dynamics 365 Human Resources.
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
ms.openlocfilehash: bf3fc5f333333b9a832ecb9c185473e476ac231d
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559508"
---
# <a name="payroll-worker-address"></a>Lohn – Adresse der Arbeitskraft

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Adresse der Arbeitskraft“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_payrollworkeraddressentity.

### <a name="description"></a>Beschreibung

Diese Entität gibt die Anschrift und den Arbeitsplatz für die Gehaltsabrechnung für einen bestimmten Mitarbeiter an.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt | Die eindeutige Personalnummer des Mitarbeiters. |
| **Lagerplatzkennung**</br>mshr_locationidbr>*Zeichenfolge* | Schreibgeschützt | Die Kennung für Adresse. |
| **Wohnadresse**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes-Optionssatz](hr-admin-integration-payroll-api-no-yes.md)* | Schreibgeschützt | Ein Wert, der angibt, ob die Adresse der Ort ist, an dem der Mitarbeiter wohnt. |
| **Arbeitsadresse** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes-Optionssatz](hr-admin-integration-payroll-api-no-yes.md)* | Schreibgeschützt | Ein Wert, der angibt, ob die Adresse der Ort ist, an dem der Mitarbeiter arbeitet. |
| **Land bzw Region**</br>mshr_countryregionid</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Das Land oder die Region, das/die für die Adresse definiert ist. |
| **Postleitzahl**</br>mshr_zipcode<br>*Zeichenfolge* | Schreibgeschützt | Die für den Mitarbeiter festgelegte Identifikationsnummer. |
| **Straße**</br>mshr_street</br>*Zeichenfolge* | Schreibgeschützt | Die für die Adresse definierte Straße. |
| **Ort**</br>mshr_city</br>*Zeichenfolge* | Schreibgeschützt | Die für die Adresse definierte Stadt. |
| **Bundesstaat**</br>mshr_state</br>*Zeichenfolge* | Schreibgeschützt | Das Bundesland oder der Kanton, das/die für die Adresse definiert ist. |
| **Verwaltungsbezirk**</br>mshr_county</br>*Zeichenfolge* | Schreibgeschützt | Das für die Adresse definierte Land. |
| **Gültig ab**</br>mshr_postaladdressvalidfrom</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum, ab dem die Adresse gültig ist. |
| **Gültig bis**</br>mshr_postaladdressvalidto</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Das Datum, bis zu dem die Adresse gültig ist. |
| **Primärfeld**</br>mshr_primaryfield</br>*Zeichenfolge* | Schreibgeschützt | Das Primärfeld. |
| **ID der Adresse der Arbeitskraft**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert (Global Unique Identifier) zum eindeutigen Identifizieren der Adresse. |

## <a name="relations"></a>Referenzen

| Eigenschaftswert | Zugehörige Entität | Navigationseigenschaft | Erfassungstyp |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Beispielabfrage

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Antwort**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
