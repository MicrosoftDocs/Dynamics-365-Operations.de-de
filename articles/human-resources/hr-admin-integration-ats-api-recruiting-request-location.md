---
title: Personalbeschaffungsantragsstandort
description: In diesem Thema wird die Entität für den Standort des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59b625bded2116007b353e7a6b697c30a62550d5b25d05185ecffe1401fbff27
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759742"
---
# <a name="recruiting-request-location"></a>Personalbeschaffungsantragsstandort

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität für den Standort des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>Beschreibung

Die Liste der Standorte, die als Standorte definiert sind, an denen rekrutierte Mitarbeiter nach der Einstellung arbeiten. Hierbei handelt es sich um Standorte, die zwischen juristischen Personen erstellt wurden.

### <a name="json-representation"></a>JSON-Darstellung

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Lagerplatzkennung**<br>mshr_locationid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Der vom System generierte, vom Benutzer lesbare eindeutige Bezeichner für den Standort der Personalbeschaffung. |
| **Personalbeschaffungsantragsstandort**<br>mshr_recruitingrequestlocationid<br>*Zeichenfolge* | Einmal schreiben<br>Erforderlich | Benutzerdefinierter eindeutiger Bezeichner für den Standort der Personalbeschaffung. |
| **Kennung der Personalbeschaffungsstandort-Entität**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Datensatz des Standorts des Personalbeschaffungsantrags. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Beschreibung des Standorts. |
| **Kennung für Land/Region**<br>mshr_countryregionid<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Gibt das Land oder die Region an, in dem der Kandidat die Staatsbürgerschaft besitzt. |
| **Wert der Kennung für Land/Region**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_logisticaddresscountryregionentityid von mshr_logisticsaddresscountryregionentity | Vom System generierter eindeutiger Bezeichner des Landes/der Region der Adresse. |
| **ZipCode**<br>mshr_zipcode<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Postleitzahl. |
| **Straße**<br>mshr_street<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Straßenadresse. |
| **Ort**<br>mshr_city<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Ort. |
| **Bundesstaat**<br>mshr_state<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Bundesland/Kanton. |
| **Landkreis**<br>mshr_county<br>*Zeichenfolge* | Schreibgeschützt<br>Optional | Landkreis. |
| **Telefon**<br>mshr_telephone<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Telefonnummer für den Standort. |
| **E-Mail**<br>mshr_email<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | E-Mail-Adresse. |
| **InternetAddress**<br>mshr_internetaddress<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | URL für die Standortwebsite. |
| **Datenbereichskennung**<br>mshr_dataareaid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Gibt die juristische Person (Firma) an. |
| **Wert der Datenbereichskennung**<br>_mshr_dataareaid_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: cdm_companyid der Entität cdm_company | Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]