---
title: Personenausbildung
description: In diesem Thema wird die Personenausbildungs-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 5e24188674c7746794c0e531dea21aa9b7f57b3534d4b67298cad19b6bec2a53
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731366"
---
# <a name="person-education"></a>Personenausbildung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Personenausbildungs-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersoneducationentity

## <a name="description"></a>Beschreibung

Diese Entität enthält den Bildungsverlauf der Person, die der Kandidat ist. Die Ausbildung ist mit dem Personendatensatz verknüpft, sodass die Ausbildung zusätzlich zum Kandidatendatensatz (Arbeitnehmer, Auftragnehmer usw.) mit anderen Rollen verknüpft werden kann, die für die Person erstellt wurden.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personenausbildungsentitätskennung**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner des Entitätsdatensatzes der Personenausbildung. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der eindeutige Bezeichner des Partei-(Personen-)Datensatzes für den Kandidaten. |
| **Personen-ID-Wert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte eindeutige Bezeichner des Personendatensatzes des Kandidaten. |
| **Punktebasis**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis-Optionssatz* | Lesen/Schreiben<br>Optional | Die Punktebasis des Bildungsabschlusses. |
| **Punktzahl erreicht**<br>mshr_creditscompleted<br>*Dezimal* | Lesen/Schreiben<br>Optional | Die Anzahl der Punkte, die für die Ausbildung abgeschlossen wurden. |
| **Verdiente Punkte**<br>mshr_creditsearned<br>*Dezimal* | Lesen/Schreiben<br>Optional | Die Anzahl der Punkte, die für den Bildungsnachweis für einen laufenden Abschluss erworben wurden. |
| **Benötigte Punkte**<br>mshr_creditsneeded<br>*Dezimal* | Lesen/Schreiben<br>Optional | Die Anzahl der Punkte, die für einen laufenden Abschluss erforderlich sind. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Eine Beschreibung des Abschlusses des Kandidaten. |
| **Ausbildungsgradskennung**<br>mshr_educationlevelid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Ausbildungsgradkennung. | 
| **Wert der Ausbildungsgradskennung**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmeducationdegreeentityid der Entität mshr_hcmeducationdegreeentity | Vom System generierter Bezeichner für den Ausbildungsgraddatensatz. Dieser Bezeichner gibt die für die Organisation definierten Abschlüsse und Bildungsstufen an. |
| **Ausbildungsfachkennung**<br>mshr_educationdisciplineid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich<br>Fremdschlüssel: EducationDiscipline | Die Kennung des Ausbildungsfachs. |
| **Wert der Ausbildungsfachkennung**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmeducationdisciplineentityid von mshr_hcmeducationdisciplineentity | Der vom System generierte eindeutige Bezeichner des Ausbildungsfachs des Ausbildungsdatensatzes. |
| **Nebenfach**<br>mshr_secondaryemphasis<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das Nebenfach des erworbenen Abschlusses. |
| **Kennung der Bildungseinrichtung**<br>mshr_educationinstitutionid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Kennung der besuchten Bildungseinrichtung. |
| **Wert der Kennung der Bildungseinrichtung**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmeducationinstitutionentityid der Entität mshr_hcmeducationinstitutionentity | Vom System generierter Bezeichner der Bildungseinrichtung. |
| **Startdatum**<br>mshr_startdate<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Startdatum der Ausbildung für den erworbenen Abschluss. |
| **Enddatum**<br>mshr_enddate<br>*Datetime* | Lesen/Schreiben<br>Erforderlich | Das Datum, an dem der Berechtigungsnachweis ausgestellt wurde. |
| **Dauer**<br>mshr_duration<br>*Dezimal* | Lesen/Schreiben<br>Optional | Die Dauer des Ausbildungsdatensatzes. |
| **Einheit für Dauer**<br>mshr_durationunit<br>*mshr_periodunit-Optionssatz* | Lesen/Schreiben<br>Optional | Die Zeiteinheit, die mit der Dauer des Ausbildungsdatensatzes verbunden ist. |
| **Durchschnitt der Abschlussnoten**<br>mshr_gradepointaverage<br>*Dezimal* | Lesen/Schreiben<br>Optional | Der erreichte Notendurchschnitt in den Abschluss. |
| **Notenskala**<br>mshr_gradescale<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Sie für den Notendurchschnitt verwendete Skala. |
| **Notizen**<br>mshr_notes<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Hinweise zur Verwendung durch den Personalvermittler oder Einstellungsmanager. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als weiterer primärer Bezeichner des Entitätsdatensatzes verwendet wird. Kombination aus Parteinummer, Kennung der Ausbildungsdisziplin, Kennung der Bildungseinrichtung und Kennung der Ausbildungsstufe. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]