---
title: Häufigkeit der Vergütungszahlung
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Häufigkeit der Vergütungszahlung“ in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b864d0db8ff1b380749b6099fa74a40045932b67
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559650"
---
# <a name="compensation-pay-frequency"></a>Häufigkeit der Vergütungszahlung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Häufigkeit der Vergütungszahlung“ in Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpayrateconversionentity

### <a name="description"></a>Beschreibung

Diese Entität stellt Informationen zur Lohnsatzumwandlung für eine bestimmte Häufigkeit der Vergütungszahlung bereit.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Jährliche Lohnsatzumwandlung**</br>mshr_annualconversionfactor</br>*Dezimal* | Schreibgeschützt | Der jährliche Umrechnungsfaktor für die Zahlungshäufigkeit. |
| **Beschreibung**</br>mshr_description</br>*Zeichenfolge* | Schreibgeschützt | Die Beschreibung des Umrechnungsrate |
| **Stündliche Lohnsatzumwandlung**</br>mshr_hourlyconversionfactor</br>*Dezimal* | Schreibgeschützt | Der stündliche Umrechnungsfaktor für die Zahlungshäufigkeit. |
| **Monatliche Lohnsatzumwandlung**</br>mshr_monthlyconversionfactor</br>*Dezimal* | Schreibgeschützt | Der monatliche Umrechnungsfaktor für die Zahlungshäufigkeit. |
| **Lohnsatzkonvertierung**</br>mshr_payrateconversion</br>*Zeichenfolge* | Schreibgeschützt | Eine eindeutige Zeichenfolge zur Identifizierung der Umwandlungsrate |
| **Periode**</br>mshr_period</br>*Perioden-Optionssatz* | Schreibgeschützt | Die Hauptperiode für die angegebene Lohnsatzumwandlung |
| **Wöchentliche Lohnsatzumwandlung**</br>mshr_weeklyconversionfactor</br>*Dezimal* | Schreibgeschützt | Der wöchentliche Umrechnungsfaktor für die Zahlungshäufigkeit. |
| **Datenbereichs-ID**</br>mshr_dataareaid</br>*Zeichenfolge* | Schreibgeschützt | Die juristische Person (Unternehmen) |
| **ID der Entität „Häufigkeit der Vergütungszahlung“**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Vom System generiert | Ein vom System generierter GUID-Wert (Global Unique Identifier) zum eindeutigen Identifizieren des Datensatzes. |

## <a name="example-query-for-payroll-employee"></a>Beispielabfrage für Mitarbeiter der Lohnbuchhaltung

**Anforderung**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Antwort**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
