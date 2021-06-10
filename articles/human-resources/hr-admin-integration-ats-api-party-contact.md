---
title: Parteikontakt
description: In diesem Thema wird die Parteikontakt-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: b37910f10c0d89e2659aa0bfbdc601c3592f896c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053802"
---
# <a name="party-contact"></a>Parteikontakt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Parteikontakt-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_dirpartycontactentities

## <a name="description"></a>Beschreibung

Diese Entität beschreibt die Kontaktinformationen des Kandidaten, einschließlich Telefon-, E-Mail- und Social Media-Konten.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Parteikontaktentitätskennung**<br>mshr_dirpartycontactentityid<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Kennung des Datensatzes der zugeordneten Partei (Person). |
| **Personen-ID-Wert**<br>_mshr_fk_person_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_dirpersonentityid von mshr_dirpersonentity | Der vom System generierte Bezeichner des Entitätsdatensatzes der Partei (Person). |
| **Lagerplatzkennung**<br>mshr_locationid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Standortkennung des Adressdatensatzes. Wird in der Entität mshr_logisticspostaladdresslocationcdsentity eingerichtet. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Beschreibung der Kontaktdaten. |
| **Typ**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Der Kontaktdetailtyp. |
| **Länder-/Regionscode**<br>mshr_countryregioncode<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Land oder Region der Adresse. |
| **Locator**<br>mshr_locator<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Kontaktdetails. Wenn zum Beispiel der Typ **E-Mail-Addresse** ist, dann enthält dieses Feld die E-Mail-Adresse des Kandidaten. |
| **Locator-Erweiterung**<br>mshr_locatorextension<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Locator-Erweiterung. Wenn zum Beispiel der Typ **Telefon** ist, dann würde diese Eigenschaft die Telefonnummernerweiterung enthalten. |
| **Ist Mobil**<br>mshr_ismobile<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Gibt an, ob das Telefon eine mobile Nummer ist. |
| **Ist Sofortnachricht**<br>mshr_isinstantmessage<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Gibt an, ob das Telefon für Sofortnachrichten aktiviert ist. |
| **Ist primär**<br>mshr_isprimary<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Bestimmt den primären Kontakt des Kontakttyps. Pro Kontakttyp darf nur ein Primärdatensatz vorhanden sein. |
| **Ist Privat**<br>mshr_isprivate<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Identifiziert, ob diese Adresse eine private Adresse für die Person ist. |
| **Kostenträger**<br>mshr_purpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Zweck/die Rolle der Kontaktdaten. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als ein primärer Bezeichner des Entitätsdatensatzes verwendet wird. Kombination aus Parteinummer, Typ, Beschreibung und Locator. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]