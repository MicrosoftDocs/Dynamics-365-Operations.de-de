---
title: Berufserfahrung der Person
description: In diesem Thema wird die Entität „Berufserfahrung der Person“ für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 5672e32b157b46b6863f06fea123fd3d6a3d96d2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466423"
---
# <a name="person-professional-experience"></a>Berufserfahrung der Person

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Berufserfahrung der Person“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>Beschreibung

Diese Entität beschreibt die Berufserfahrung oder de Arbeitsverlauf eines Bewerbers.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Kennung der Entität „Berufserfahrung der Person“**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der eindeutige Bezeichner des Personendatensatzes für den Kandidaten. |
| **Personenkennungswert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Vom System generierter eindeutiger Bezeichner des Personenentitätsdatensatzes. |
| **Mitarbeiterposition**<br>mshr_employerposition<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Positionstitel, den der Kandidat während seiner Beschäftigung innehat. |
| **Arbeitgebername**<br>mshr_employername<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Name des Arbeitgebers. |
| **Standort des Arbeitgebers**<br>mshr_employerlocation<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Standort des Arbeitgebers. Maximale Länge: 60. Kein bestimmtes Format definiert oder erforderlich. |
| **Telefonnummer**<br>mshr_phone<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Telefonnummer des Arbeitgebers. |
| **URL**<br>mshr_url<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die URL der Website des Arbeitgebers. |
| **Startdatum**<br>mshr_startdate<br>*Datetime* | Lesen/Schreiben<br>Erforderlich | Das Startdatum der Anstellung des Kandidaten. |
| **Enddatum**<br>mshr_enddate<br>*Datetime* | Lesen/Schreiben<br>Optional | Das Enddatum der Anstellung des Kandidaten oder null, wenn der Kandidat noch hier beschäftigt ist. |
| **Arbeitgeberkontakt zulassen**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno-Optionssatz* | Lesen/Schreiben<br>Optional | Gibt an, ob der Kandidat die Kontaktaufnahme mit dem vorherigen Arbeitgeber zulässt. |
| **Notizen**<br>mshr_note<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Hinweise zur Verwendung durch den Personalvermittler oder Einstellungsmanager. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als ein primärer Bezeichner des Entitätsdatensatzes verwendet wird. Kombination aus Parteinummer, Startdatum, Arbeitgeberposition und Name des Arbeitgebers. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]