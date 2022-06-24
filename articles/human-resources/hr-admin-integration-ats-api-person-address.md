---
title: Personenadresse
description: In diesem Artikel wird die Personendressen-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: be5cf649771eaddcb4f2198821530e61b76b2cd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871015"
---
# <a name="person-address"></a>Personenadresse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird die Personendressen-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmpersonaddressentities

## <a name="description"></a>Beschreibung

Diese Entität enthält die Liste der Postanschriften für Kandidatendatensätze.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personenadressen-Entitäts-ID**<br>mshr_hcmpersonaddressentityid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Kennung des Datensatzes der zugeordneten Partei (Person). |
| **Personen-ID-Wert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person). |
| **Lagerplatzkennung**<br>mshr_locationid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Standortkennung des Adressdatensatzes. Wird in der Entität mshr_logisticspostaladdresslocationcdsentity eingerichtet. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Eine Beschreibung der Adresse des Kandidaten. |
| **Rollen**<br>mshr_roles<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die für diese Adresse zugewiesenen Rollen. Sie können mehrere Rollen zuweisen. Jede Rolle sollte durch ein Semikolon getrennt werden. Gültige Werte in der Entität mshr_logisticslocationroleentity. |
| **Straße**<br>mshr_street<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Hausnummer. |
| **Ort**<br>mshr_city<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Stadt der Adresse. In der Entität mshr_logisticsaddresscityentity einrichten. |
| **Bundesstaat**<br>mshr_state<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das Bundesland der Adresse. In der Entität mshr_logisticsaddressstateentity einrichten. |
| **Landkreis**<br>mshr_county<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Landkreis der Adresse. In der Entität mshr_logisticsaddresscountyentity einrichten. |
| **PLZ**<br>mshr_zipcode<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Postleitzahl der Adresse. In der Entität mshr_logisticsaddresspostalcodeentity einrichten. |
| **Kennung für Land/Region**<br>mshr_countryregionid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Land oder Region der Adresse. |
| **Wert der Kennung für Land/Region**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Schreibgeschützt<br>Optional<br>Fremdschlüssel: mshr_logisticaddresscountryregionentityid von mshr_logisticsaddresscountryregionentity | Vom System generierter eindeutiger Bezeichner des Landes/der Region der Adresse. |
| **Ist primär**<br>mshr_isprimary<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Gibt an, ob diese Adresse die primäre Adresse für die Person der definierten Rolle ist. |
| **Ist Privat**<br>mshr_isprivate<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Identifiziert, ob diese Adresse eine private Adresse für die Person ist. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als ein primärer Bezeichner des Entitätsdatensatzes verwendet wird. Kombination aus Parteinummer und Standortkennung. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
