---
title: Kandidat, der eingestellt werden kann
description: In diesem Artikel wird die Entität „Einzustellender Kandidat“ für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 12/05/2021
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
ms.openlocfilehash: 7c243bdf81beabe9e1ee429227a6edf4d4864bfb
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831992"
---
# <a name="candidate-to-hire"></a>Kandidat, der eingestellt werden kann


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird die Entität „Einzustellender Kandidat“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmcandidatetohireentity

## <a name="description"></a>Beschreibung

Diese Entität bietet Kandidatendetails, die zum Erstellen einer Arbeitskraft in Dynamics 365 Human Resources verwendet wird. Sie wird verwendet, um alle Kandidatendatensätze zu lesen und interne und externe Kandidatendatensätze zu erstellen, sodass Sie persönliche Daten für den neuen Kandidaten erstellen können.

Wenn Sie einen externen Kandidatendatensatz erstellen, der ein neuer Personendatensatz im System sein wird, dürfen Sie keine Partei-(Personen-)Nummer definieren, für die Sie einen neuen Kandidatendatensatz veröffentlichen. Der neue Personenentitätsdatensatz wird mit dem neuen Kandidatendatensatz erstellt.

Wenn Sie einen internen Kandidatendatensatz erstellen (einen Kandidaten für die Position, der bereits einen Mitarbeiterdatensatz im Unternehmen hat), definieren Sie die Partei-(Personen-)Nummer des Datensatzes, der bereits für die Person für die Eigenschaft mshr_partynumber im Kandidatendatensatz vorhanden ist, statt persönliche Informationen (wie Name, Geschlecht oder Geburtsdatum) zu definieren, die zum Erstellen eines neuen Personendatensatzes verwendet werden.

## <a name="json-representation"></a>JSON-Darstellung

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
            "mshr_militaryserviceenddate": "Date",
            "mshr_militaryservicestartdate": "Date"
        }
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kandidat für die Einstellung-Entitätskennung**<br>mshr_hcmcandidatetohireentityid<br>GUID | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Ein vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz. |
| **Kandidatenkennung**<br>mshr_candidateid<br>Zeichenfolge | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Ein eindeutiger Bezeichner für die Entität. |
| **Parteinummer**<br>mshr_partynumber<br>Zeichenfolge | Schreibgeschützt<br>Erforderlich | Die Nummer der Partei (Person) des Personendatensatzes des Kandidaten. |
| **Personen-ID-Wert**<br>_mshr_fk_person_id_value<br>GUID | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_direpersonentity | Der vom System generierte eindeutige Bezeichner für den Partei-(Personen-)Datensatz des Kandidaten. |
| **Parteityp**<br>mshr_partytype<br>mshr_dirpartytype-Optionssatz | Schreibgeschützt<br>Erforderlich | Der Parteityp des Datensatzes, wie im Optionssatz mshr_dirpartytype definiert. Für diese Entität ist der Typ immer „Person“. |
| **Personalbeschaffungsantragskennung**<br>mshr_recruitingrequestid<br>Zeichenfolge | Einmal schreiben<br>Optional | Verweist auf den Personalbeschaffungsantrag, den dieser Kandidat erfüllt. |
| **Wert der Personalbeschaffungsantragskennung**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Lesen/Schreiben<br>Optional<br>Fremdschlüssel: mshr_hcmrecruitingrequestentityid von mshr_hcmrecruitingrequestentity | Der vom System generierte eindeutige Bezeichner für den Personalbeschaffungsantrag, den der Kandidat erfüllt. |
| **Positionskennung**<br>mshr_positionid<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Die ID der Position, für die der Kandidat berücksichtigt wird. |
| **Positions-ID-Wert**<br>_mshr_fk_Position_if_value<br>GUID | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmpositionv2entityid von mshr_hcmpositionv2entity | Der vom System generierte Bezeichner der Position, für die der Kandidat berücksichtigt wird. |
| **Vorname**<br>mshr_firstname<br>Zeichenfolge | Lesen/Schreiben<br>Erforderlich | Vorname des Kandidaten. |
| **Zweiter Vorname**<br>mshr_middlename<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Zweitname des Kandidaten. |
| **Präfix für Nachname**<br>mshr_lastnameprefix<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Präfix für den Nachnamen des Kandidaten. |
| **Nachname**<br>mshr_lastname<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Nachname des Kandidaten. |
| **Geschlecht**<br>mshr_gender<br>mshr_hcmpersongender-Optionssatz | Lesen/Schreiben<br>Optional | Das Geschlecht des Kandidaten. |
| **Geburtstag**<br>mshr_birthdate<br>Datetime | Lesen/Schreiben<br>Optional | Das Geburtsdatum des Kandidaten. |
| **Staatsbürgerschafts-Ländercode**<br>mshr_citizenshipcountrycode<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Gibt das Land an, in dem der Kandidat die Staatsbürgerschaft besitzt. Gültige Ländercodes befinden sich in mshr_logisticaddresscountryregionentity. |
| **Veteranenstatuskennung**<br>mshr_veteranstatusid<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Gibt den Veteranenstatus des Kandidaten an. |
| **Wert der Veteranenstatuskennung**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmveteranstatusentityid von mshr_hcmveteranstatusentity | Vom System generierter eindeutiger Bezeichner für den Veteranenstatusdatensatz. |
| **Datum des Eintritts in den Militärdienst**<br>mshr_militaryservicestartdate<br>Datetime | Lesen/Schreiben<br>Optional | Das Startdatum des Militärdienstes des Kandidaten. |
| **Datum des Austritts aus dem Militärdienst**<br>mshr_militaryserviceenddate<br>Datetime | Lesen/Schreiben<br>Optional | Das Enddatum des Militärdienstes des Kandidaten. |
| **Ist behinderter Veteran**<br>mshr_isdisabledveteran<br>mshr_noyes-Optionssatz | Lesen/Schreiben<br>Optional | Gibt an, ob der Kandidat den Veteranenstatus deaktiviert hat. |
| **Verfügbarkeitsdatum**<br>mshr_availabilitydate<br>Datetime | Lesen/Schreiben<br>Optional | Das früheste Datum, an dem der Kandidat für die Arbeit zur Verfügung stehen würde. |
| **Ist bereit umzuziehen**<br>mshr_iswillingtorelocate<br>mshr_noyes-Optionssatz | Lesen/Schreiben<br>Optional | Gibt an, ob der Kandidat bereit ist, für die Position umzuziehen. |
| **Kommentare**<br>mshr_comments<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Kommentare, die vom Personalvermittler oder Einstellungsmanager verwendet werden sollen. |
| **Ergebnis der Bewerbungsintegration**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult-Optionssatz | Lesen/Schreiben<br>Erforderlich | Der Status des Kandidaten im Einstellungsprozess im Zusammenhang mit der Integration. |
| **Kennung für den Ursachencode der Nichteinstellung**<br>mshr_donothirereasoncodeid<br>Zeichenfolge | Lesen/Schreiben<br>Optional | Ein Ursachencode, der optional angegeben werden kann, wenn der Status (Ergebnis der Bewerbungsintegration) auf „Nicht eingestellt“ festgelegt wird. |
| **Wert der Ursachencodekennung**<br>_mshr_fk_reasoncode_id_value<br>GUID | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_hcmreasoncodeentityid der Entität mshr_hcmreasoncodeentity | Vom System generierter eindeutiger Bezeichner für den **Nicht einstellen**-Ursachencode. |
| **Datenbereichskennung**<br>mshr_dataareaid<br>Zeichenfolge | Lesen/Schreiben<br>Optional |  Gibt die juristische Person (Firma) an. |
| **Wert der Datenbereichskennung**<br>_mshr_dataareaid_id_value<br>GUID | Schreibgeschützt<br>Optional<br>Fremdschlüssel: cdm_companyid der Entität cdm_company | Vom System generierter GUID-Wert, der die juristische Person (Firma) identifiziert. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
