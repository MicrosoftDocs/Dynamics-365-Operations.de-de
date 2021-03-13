---
title: Personenidentifikationsnummer
description: In diesem Thema wird die Personenidentifikationsnummern-Entität für Dynamics 365 Human Resources beschrieben.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 054547c4f33e50d2dc0fa275559ba6ed44c27971
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125400"
---
# <a name="person-identification-number"></a>Personenidentifikationsnummer

In diesem Thema wird die Personenidentifikationsnummern-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>Beschreibung

In dieser Entität werden die Identifikationsnummern für den Kandidaten beschrieben. Es ermöglicht dem API-Nutzer, Identifikationsnummern wie Sozialversicherungsnummern oder Passnummern in den Kandidatendatensatz zu schreiben. Identifikationsnummern sind im Arbeitsdatensatz aufgeführt, jedoch nicht im Kandidatendatensatz. Eine integrierende Anwendung kann die Werte in die Personaldatenbank schreiben, aber die Nummern werden in der Personalabteilung erst angezeigt, wenn der Mitarbeiterdatensatz des Bewerbers erstellt wurde.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personenidentifikationsnummer-Entitätskennung**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Eindeutiger primäre Bezeichner für den Datensatz der Personenidentifikationsnummer. |
| **Eintragstyp**<br>mshr_entrytype<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Freier Wert zum Verweis auf die Art der Eingabe für die Identifikationsnummer. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Beschreibung der Kennnummer. |
| **Ablaufdatum**<br>mshr_expirationdate<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Datum, an dem die Identifikationsnummer oder das zugehörige Dokument abläuft. |
| **Ist primär**<br>mshr_isprimary<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Definiert, ob die Identifikationsnummer der primäre Datensatz für die Person für diesen Identifikationstyp ist. |
| **Kennnummer**<br>mshr_identificationnumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Kennnummer |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Bezeichner der Partei (Person) im Besitz der Identifikationsnummer. |
| **Personenkennungswert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid der Entität mshr_dirpersonentity | Der eindeutige Bezeichner der Partei (Person). |
| **Identifikationstypkennung**<br>mshr_identificationtypeid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Typ der Identifikationsnummer. |
| **Wert der Identifikationstypkennung**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmidentificationtypeentityid der Entität mshr_hcmidentificationtypeentity | Systemgenerierter eindeutiger Bezeichner des Identifikationstyps. |
| **Kennung der ausstellenden Behörde**<br>mshr_issuingagencyid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Behörde oder Organisation, die die Identifikationsnummer ausstellt. |
| **Wert der Kennung der ausstellenden Behörde**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmissuingagencyentityid der Entität mshr_hcmissuingagencyentity | Systemgenerierter eindeutiger Bezeichner der Behörde, die die Identifikationsnummer ausstellt. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann. Kombination aus Parteinummer, Kennung des Identifikationstyps und Identifikationsnummer. |
| **Ausstellungsdatum**<br>mshr_issuedate<br>*Datum* | Lesen/Schreiben<br>Optional | Das Datum, an dem die Identifikationsnummer ausgestellt wurde. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

