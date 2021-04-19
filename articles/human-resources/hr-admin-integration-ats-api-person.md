---
title: Person
description: In diesem Thema wird die Person-Entität für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 448be7ada2825d3cdd846650821579d1d6797d00
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800356"
---
# <a name="person"></a>Person

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Person-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_dirpersonentity

### <a name="description"></a>Beschreibung

Diese Entität stellt die persönlichen Informationen für die Person bereit, die der Kandidat ist.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Personenentitäts-ID**<br>mshr_dirpersonentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Ein vom System generierter eindeutiger Bezeichner für den Entitätsdatensatz. |
| **Parteinummer**<br>mshr_partynumber<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Ein vom Benutzer lesbarer und vom System generierter eindeutiger Bezeichner für die Person.  |
| **Name**<br>mshr_name<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Der Feldwert ist eine Verkettung von Vorname, Zweitname, Nachnamepräfix und Nachname in der Reihenfolge, die im Feld **Namenssequenzanzeige als** definiert ist. |
| **Namensalias**<br>mshr_namealias<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Ein Namensalias, der für die Person bereitgestellt werden kann. |
| **Bekannt als**<br>mshr_knownas<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Ein Name, der für die Person verwendet werden kann, wenn sie normalerweise unter einem anderen Name bekannt ist. |
| **Sprachkennung**<br>mshr_languageid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Sprach-ID der Primärsprache der Person gemäß ISO 639-1-Format. |
| **Adressbücher**<br>mshr_addressbooks<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das Adressbuch, dem die Person zugeordnet werden kann. Die Adressbücher, die für die Organisation eingerichtet wurden, werden in der Entität mshr_diraddressbooksentity aufgelistet. |
| **Jahrestag-Tag**<br>mshr_anniversaryday<br>*Int* | Lesen/Schreiben<br>Optional | Der Tag des Datums des Jahrestags der Person. |
| **Jahrestag-Monat**<br>mshr_anniversarymonth<br>*mshr_monthsofyear-Optionssatz* | Lesen/Schreiben<br>Optional | Der Monat des Datums des Jahrestags der Person. |
| **Jahrestag-Jahr**<br>mshr_anniversaryyear<br>*Int* | Lesen/Schreiben<br>Optional | Der Jahr des Datums des Jahrestags der Person. |
| **Geburtstag**<br>mshr_birthday<br>*Int* | Lesen/Schreiben<br>Optional | Der Tag des Geburtstags der Person. |
| **Geburtsmonat**<br>mshr_birthmonth<br>*mshr_monthsofyear-Optionssatz* | Lesen/Schreiben<br>Optional | Der Monat des Geburtstags der Person. |
| **Geburtsjahr**<br>mshr_birthyear<br>*Int* | Lesen/Schreiben<br>Optional | Der Jahr des Geburtstags der Person. |
| **Kindernamen**<br>mshr_childrennames<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Zeichenfolge für die Namen der Kinder der Person. Es ist keine Abgrenzung erforderlich. |
| **Geschlecht**<br>mshr_gender<br>*mshr_hcmpersongender-Optionssatz* | Lesen/Schreiben<br>Optional | Das Geschlecht der Person. |
| **Hobbys**<br>mshr_hobbies<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Hobbys der Person. |
| **Initialen**<br>mshr_initials<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Initialen des Namens der Person. |
| **Familienstand**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus-Optionssatz* | Lesen/Schreiben<br>Optional | Der Familienstand der Person. |
| **Phonetischer Vorname**<br>mshr_phoneticfirstname<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die phonetische Aussprache des Vornamens der Person. |
| **Phonetischer Nachname**<br>mshr_phoneticlastname<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die phonetische Aussprache des Nachnamens der Person. |
| **Phonetischer zweiter Vorname**<br>mshr_phoneticmiddlename<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die phonetische Aussprache des Nachnamens der Person. |
| **Persönliches Suffix**<br>mshr_personalsuffix<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das persönliche Suffix der Person. Gültige Werte in der Entität mshr_dirnameaffixentity, wobei mshr_type das Suffix (200000001) ist. |
| **Persönlicher Titel**<br>mshr_personaltitle<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Ein persönlicher Titel für die Person. Gültige Werte in der Entität mshr_dirnameaffixentity, wobei mshr_type der Titel (200000000) ist.
| **Professionelles Suffix**<br>mshr_professionalsuffix<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Ein professionelles Suffix. |
| **Professioneller Titel**<br>mshr_professionaltitle<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Ein professioneller Titel. |
| **Vollständige primäre Adresse**<br>mshr_fullprimaryaddress<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die vollständige primäre Adresse der Person, eine Verkettung der primären Adressfelder. |
| **Adresse - Ort**<br>mshr_addresscity<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Stadt der Hauptadresse der Person. In der Entität mshr_logisticsaddresscityentity einrichten. |
| **Land/Region der Adresse**<br>mshr_addresscountryregionid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das Land/die Region der Hauptadresse der Person. Gültige Werte in der Entität mshr_logisticsaddresscountryregionentity. |
| **ISO-Code für Land/Region der Adresse**<br>mshr_addresscountryregionisocode<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der ISO-Code für das Land/die Region der Hauptadresse der Person. |
| **Land der Adresse**<br>mshr_addresscounty<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das Land der Hauptadresse der Person. In der Entität mshr_logisticsaddresscountyentity einrichten. |
| **Bezirksname der Adresse**<br>mshr_addressdistrictname<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Bezirk der Hauptadresse der Person. In der Entität mshr_logisticsaddressdistrictentity einrichten. |
| **Breitengrad der Adresse**<br>mshr_addresslatitude<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Breitengrad der Hauptadresse der Person. |
| **Standortkennung der Adresse**<br>mshr_addresslocationid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die eindeutige Bezeichner für den Standort der primären Adresse der Person. Gültige Werte in der Entität mshr_logisticspostaladdresslocationcdsentity. |
| **Standortrollen der Adresse**<br>mshr_addresslocationroles<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Standortrolle der Hauptadresse der Person. In der Entität mshr_logisticslocationrolecdsentity einrichten. |
| **Längengrad der Adresse**<br>mshr_addresslongitude<br>*Zeichenfolge* |  Lesen/Schreiben<br>Optional | Der Längengrad der Hauptadresse der Person. |
| **Staat der Adresse**<br>mshr_addressstate<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Staat der Hauptadresse der Person. In der Entität mshr_logisticsaddressstateentity einrichten. |
| **Straße der Adresse**<br>mshr_addressstreet<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Straße der Hauptadresse der Person. |
| **Adresse gültig ab**<br>mshr_addressvalidfrom<br>*Datum* | Lesen/Schreiben<br>Optional | Das Datum, ab dem die primäre Adresse der Person gültig ist. |
| **Adresse gültig bis**<br>mshr_addressvalidto<br>*Datum* | Lesen/Schreiben<br>Optional | Das Datum, bis zu dem die primäre Adresse der Person gültig ist. |
| **Postleitzahl der Adresse**<br>mshr_addresszipcode<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Postleitzahl der Hauptadresse der Person. In der Entität mshr_logisticsaddresspostalcodeentity einrichten. |
| **Adresse ist privat**<br>mshr_addressisprivate<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Dies legt fest, ob die primäre Adresse der Person für andere Personen in der Organisation freigegeben wird. |
| **Adressbeschreibung**<br>mshr_addressdescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Beschreibung der Hauptadresse der Person. |
| **Primäre Kontakt-E-Mail**<br>mshr_primarycontactemail<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die primäre E-Mail-Adresse der Person. |
| **Beschreibung der primären Kontakt-E-Mail**<br>mshr_primarycontactemaildescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Eine Beschreibung der primäre E-Mail-Adresse. |
| **Primäre Kontakt-E-Mail ist IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Dies legt fest, ob die primäre E-Mail-Adresse für Sofortnachrichten verfügbar ist. |
| **Zweck der primären Kontakt-E-Mail**<br>mshr_primarycontactemailpurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Zweck der primären E-Mail-Adresse. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Primäres Kontakt-Fax**<br>mshr_primarycontactfax<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Primäre Faxnummer. |
| **Beschreibung des primären Kontakt-Faxes**<br>mshr_primarycontactfaxdescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Beschreibung der primären Faxnummer. |
| **Durchwahl des primären Kontakt-Faxes**<br>mshr_primarycontactfaxextension<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Durchwahl der primären Faxnummer. |
| **Zweck des primären Kontakt-Faxes**<br>mshr_primarycontactfaxpurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Zweck der primären Faxnummer. In der Entität mshr_logisticslocationroleentity einrichten.
| **Primäres Kontakt-Telefon**<br>mshr_primarycontactphone<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Primäre Telefonnummer |
| **Beschreibung des primären Kontakt-Telefons**<br>mshr_primarycontactphonedescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Beschreibung der primären Telefonnummer. |
| **Durchwahl des primären Kontakt-Telefons**<br>mshr_primarycontactphoneextension<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Durchwahl der primären Telefonnummer. |
| **Primäres Kontakt-Telefon ist mobil**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Legt fest, ob die primäre Telefonnummer ein Mobiltelefon ist. |
| **Zweck des primären Kontakt-Telefons**<br>mshr_primarycontactphonepurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Zweck der primären Telefonnummer. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Primäres Kontakt-Telex**<br>mshr_primarycontacttelex<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Primäre Telexnummer. |
| **Beschreibung des primären Kontakt-Telexes**<br>mshr_primarycontacttelexdescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Beschreibung der primären Telexnummer der Person. |
| **Zweck des primären Kontakt-Telex**<br>mshr_primarycontacttelexpurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Zweck für die primäre Telexnummer der Person. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Primäre Kontakt-URL**<br>mshr_primarycontacturl<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die primäre URL. |
| **Beschreibung des primären Kontakt-URL**<br>mshr_primarycontacturldescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Beschreibung der primären URL der Person. |
| **Zweck der primären Kontakt-URL**<br>mshr_primarycontacturldescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Zweck der primären URL der Person. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Primäres Kontakt-Facebook**<br>mshr_primarycontactfacebook<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Primäres Facebook-Konto. Identifiziert durch Benutzer-ID. |
| **Beschreibung des primären Kontakt-Facebook**<br>mshr_primarycontactfacebookdescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Beschreibung des primären Facebook-Kontos der Person. |
| **Primäres Kontakt-Facebook ist privat**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Bestimmt, ob das primäre Facebook-Konto für andere Benutzer sichtbar ist. |
| **Zweck des primären Kontakt-Facebook**<br>mshr_primarycontactfacebookpurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Zweck des primären Facebook-Kontos der Person. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Primäres Kontakt-LinkedIn**<br>mshr_primarycontactlinkedin<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Primäres LinkedIn-Konto. Identifiziert durch Benutzername. |
| **Beschreibung des primären Kontakt-LinkedIn**<br>mshr_primarycontactlinkedindescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Beschreibung des primären LinkedIn-Kontos der Person. |
| **Primäres Kontakt-LinkedIn ist privat**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Dies legt fest, ob die primäre LinkedIn-Kontoinformation für andere Benutzer in der Organisation freigegeben wird. |
| **Zweck des primären Kontakt-LinkedIn**<br>mshr_primarycontactlinkedinpurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Zweck des primären LinkedIn-Kontos der Person. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Primäres Kontakt-Twitter**<br>mshr_primarycontacttwitter<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das primäre Twitter-Konto der Person. Identifiziert durch @Benutzername. |
| **Beschreibung des primären Kontakt-Twitter**<br>mshr_primarycontacttwitterdescription<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Beschreibung des primären Twitter-Kontos der Person. |
| **Primäres Kontakt-Twitter ist privat**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes-Optionssatz* | Lesen/Schreiben<br>Optional | Dies legt fest, ob die primäre Twitter-Kontoinformation für andere Benutzer in der Organisation freigegeben wird. |
| **Zweck des primären Kontakt-Twitter**<br>mshr_primarycontacttwitterpurpose<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Zweck des primären Twitter-Kontos der Person. In der Entität mshr_logisticslocationroleentity einrichten. |
| **Parteityp**<br>mshr_partytype<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Parteityp der Person. Ist für Kandidaten immer **Person**. |
| **Namenssequenzanzeige als**<br>mshr_namesequencedisplayas<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Reihenfolge, in der die Namenseigenschaften der Person verbunden sind, um die Namenseigenschaft (mshr_name) zu ergeben. |
| **Vorname**<br>mshr_firstname<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Der Vorname der Person. |
| **Zweiter Vorname**<br>mshr_middlename<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der zweite Vorname der Person. |
| **Präfix für Nachname**<br>mshr_lastnameprefix<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Das Präfix des Nachnamens der Person. |
| **Nachname**<br>mshr_lastname<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Der Nachname der Person. |
| **Elektronische Standortkennung**<br>mshr_electroniclocationid<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Die Kennung des elektronischen Standorts der Person. |
| **Zeitzone der Adresse**<br>mshr_addresstimezone<br>*Int* | Lesen/Schreiben<br>Optional | Der Zeitzone der Hauptadresse der Person. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]