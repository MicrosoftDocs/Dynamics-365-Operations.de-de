---
title: Vergütungsplan für Lohnarbeitskräfte
description: Dieses Thema enthält Details und eine Beispielabfrage für die Entität „Vergütungsplan für Lohnarbeitskräfte“ in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0837d9a153aba554d0a5293d16afb309bd37963c270da5b67e691558cae63b0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758711"
---
# <a name="payroll-worker-benefit-plan"></a>Vergütungsplan für Lohnarbeitskräfte

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Vergütungsplan für Lohnarbeitskräfte“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>Beschreibung

Diese Entität stellt Informationen über den Vergütungsplan für eine bestimmte Arbeitskraft bereit.

## <a name="properties"></a>Eigenschaften

| Eigenschaft</br>**Physikalischer Name**</br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Zeichenfolge* | Schreibgeschützt</br>Erforderlich | Die eindeutige Personalnummer des Mitarbeiters. |
| **Kennung der juristischen Person**</br>mshr_legalentityID</br>*Zeichenfolge* | Schreibgeschützt | Gibt die juristische Person (Firma) an. |
| **Periodenkennung**</br>mshr_periodid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung der Periode. |
| **Plankennung**</br>mshr_planid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung des Plans. |
| **Abdeckungsoption**</br>mshr_coverageoptionid</br>*Zeichenfolge* | Schreibgeschützt | Kennung der Deckungsoption. |
| **Startdatum der Abzugs**</br>mshr_deductionstartdatetime</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Startdatum der Abzugs. |
| **Enddatum des Abzugs**</br>mshr_deductionenddatetime</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Enddatum des Abzugs. |
| **Status**</br>mshr_status</br>*[Optionssatz des Status des Vergütungsplans für Mitarbeiter](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Schreibgeschützt | Status für den Vergütungsplans. |
| **Gültig ab**</br>mshr_validfrom</br>*Datum-/Uhrzeit-Offset* | Schreibgeschützt | Die Uhrzeit, ab der dieser Datensatz gültig ist. |
| **Gültig bis**</br>mshr_validto</br>*Datum-/Uhrzeit-Offset* |  Schreibgeschützt | Die Uhrzeit, bis zu der dieser Datensatz gültig ist. |
| **Kennung des Plantyps**</br>mshr_plantypeid</br>*Zeichenfolge* | Schreibgeschützt | Die Kennung des Plantyps. |
| **Code des Plantyps**</br>mshr_plantypecode</br>*[Optionssatz der Deckung des Vergütungsplantyps](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Schreibgeschützt | Die Spezifikation des Plantyps. |
| **Anzahl der Lohnzahlungsperioden**</br>mshr_payperiod</br>*Ganzzahl* | Schreibgeschützt | Die Anzahl der Zahlungsperioden, die angibt, wie oft der Vorteilsanbieter oder die Mitarbeiter bezahlt werden. Dieser Betrag wird zur Berechnung des Vorteilsjahresgehalts des Mitarbeiters verwendet. |
| **Mitarbeiterbetrag**</br>mshr_amountemployee</br>*Dezimal* | Schreibgeschützt | Der Mitarbeiterbetrag oder -prozentsatz. |
| **Arbeitgeberbetrag**</br>mshr_amountemployer</br>*Dezimal* | Schreibgeschützt | Der Arbeitgeberbetrag oder -prozentsatz. |
| **Primärfeld**</br>mshr_primaryfield</br>*Zeichenfolge* | Vom System generiert | Primärfeld. |
| **Wert der Arbeitskraftkennung** </br>_mshr_fk_worker_id_value</br>*GUID* | Fremdschlüssel: mshr_hcmworkerbaseentityid der mshr_hcmworkerbaseentity-Entität. | Vom System generierter eindeutiger Bezeichner der Arbeitskraft. |
| **Periodenkennung**</br> _mshr_fk_period_id_value</br>*GUID* | Fremdschlüssel: mshr_benefitperiodentityid der mshr_benefitperiodentity-Entität. | Vom System generierter eindeutiger Bezeichner der Periode. |
| **Plankennung**</br> _mshr_fk_plan_id_value</br>*GUID* | Fremdschlüssel: mshr_benefitplanentityid der mshr_benefitplanentity-Entität. | Vom System generierter eindeutiger Bezeichner des Plans. |
| **Plantypkennung**</br> _mshr_fk_plantype_id_value</br>*GUID* | Fremdschlüssel: mshr_benefitplantypeentityid der mshr_benefitplantypeentity-Entität. | Vom System generierter eindeutiger Bezeichner des Plans. |
| **Kennung der Deckungsoption**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Fremdschlüssel: mshr_benefitcoverageoptionentityid der mshr_benefitcoverageoptionentity-Entität. | Vom System generierter eindeutiger Bezeichner des Plans. |
| **Kennung der Entität „Vergütungsplan für Lohnarbeitskräfte“**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Schreibgeschützt </br> Vom System generiert | Vom System generierter eindeutiger Bezeichner für den Datensatz. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Beispielabfrage für Vergütungsplan für Lohnarbeitskräfte

**Anforderung**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Antwort**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
