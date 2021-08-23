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
ms.openlocfilehash: 898ca7b33e39ec33990fecc4c3a7229620fbfddd5ce8ad14423af38047187e55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761973"
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
| **Ort**</br>mshr_city</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Die für die Adresse festgelegte Stadt.   |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Die eindeutige Personalnummer des Mitarbeiters.  |
| **Land bzw Region**</br>mshr_countryregionid</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Das für die Adresse festgelegte Land bzw. die Region.  |
| **Gültig ab**</br>mshr_postaladdressvalidfrom</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt </br>Erforderlich | Das Datum, ab dem die Adresse gültig ist. |
| **Arbeitsadresse** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes-Optionssatz](hr-admin-integration-payroll-api-no-yes.md)* | Schreibgeschützt</br>Erforderlich | Gibt an, ob die Adresse der Ort ist, an dem der Mitarbeiter arbeitet. |
| **Landkreis**</br>mshr_county</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Der für die Adresse festgelegte Landkreis.  |
| **ID der Adresse der Arbeitskraft**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Erforderlich</br>Vom System generiert | Ein vom System generierter GUID-Wert zur eindeutigen Identifizierung der Adresse.  |
| **Primärfeld**</br>mshr_primaryfield</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich |  |
| **Straße**</br>mshr_street</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Der für die Adresse festgelegte Straße. |
| **Gültig bis**</br>mshr_postaladdressvalidto</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt </br>Erforderlich | Das Datum, bis zu dem die Adresse gültig ist.  |
| **Lagerplatzkennung**</br>mshr_locationidbr>*Zeichenfolge* | Schreibgeschützt <br>Erforderlich | Die Kennung für Adresse.  |
| **PLZ**</br>mshr_zipcode<br>*Zeichenfolge* | Schreibgeschützt <br>Erforderlich |Die für den Mitarbeiter festgelegte Kennungsnummer.  |
| **Wohnadresse**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes-Optionssatz](hr-admin-integration-payroll-api-no-yes.md)* | Schreibgeschützt</br>Erforderlich | Gibt an, ob die Adresse der Ort ist, an dem der Mitarbeiter wohnt. |
| **Bundesstaat**</br>mshr_state</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Der für die Adresse festgelegte Bundesstaat.  |

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
