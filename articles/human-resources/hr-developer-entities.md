---
title: Common Data Service-Entitäten
description: Microsoft Dynamics 365 Human Resources verwendet Common Data Service, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009195"
---
# <a name="common-data-service-entities"></a>Common Data Service-Entitäten

Microsoft Dynamics 365 Human Resources verwendet Common Data Service, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.

Weitere Informationen zu Common Data Service finden Sie unter [Was ist Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Die folgenden Human Resources-Entitäten sind in Common Data Service verfügbar.

## <a name="benefit-entities"></a>Vorteilsentitäten

**Vorteilsberechnungshäufigkeit**

| **Felder**        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------|---------------|--------------|----------------|
| Beschreibung       | Text          |              | X              |
| Häufigkeitssteuerung | Option festgelegt    | X            | X              |
| Unveränderlich      | Zwei Optionen   |              | X              |
| Name              | Text          | X            | X              |


**Vergütungsberechnungssatz**

| **Felder**  | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------|---------------|--------------|----------------|
| Beschreibung | Text          |              | X              |
| Name        | Text          | X            | X              |
| TierType    | Option festgelegt    | X            | X              |


**Vergütungsberechnungssatz-Detail**

| **Felder**                             | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|----------------------------------------|----------------|--------------|----------------|
| Vergütungsberechnungssatz-Detailnummer | Text           | X            | X              |
| Berechnungssatz-ID                    | Suche         | X            | X              |
| Beitragsmethode                    | Option festgelegt     | X            | X              |
| Gültig                              | Nur Datum      | X            | X              |
| Arbeitgeberbeitrag                  | Dezimalzahl |              | X              |
| Ablaufdatum                             | Nur Datum      | X            | X              |
| WorkerDeduction                        | Dezimalzahl |              | X              |


**Vergütungstyp**

| **Felder**           | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Option festgelegt    |              | X              |
| Beschreibung          | Text          |              | X              |
| Name                 | Text          | X            | X              |
| PayrollCategory      | Option festgelegt    |              | X              |


**Vergütungsplan**

| **Felder**                               | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|------------------------------------------|----------------|--------------|----------------|
| Rückstandsbeschränkungsmethode                      | Option festgelegt     |              | X              |
| Vergütungstyp                             | Suche         | X            | X              |
| Beitragsbeschränkungsmethode                | Option festgelegt     |              | X              |
| Beitragsmethode                      | Option festgelegt     |              | X              |
| Währung                                 | Suche         |              | X              |
| Abzugspriorität                       | Ganzzahl   |              | X              |
| Limitbetrag für Standardbeitrag        | Währung       |              | X              |
| Limitbetrag für Standardbeitrag (Basis) | Währung       |              | X              |
| Limitperiode für Standardbeitrag        | Option festgelegt     |              | X              |
| Limitbetrag für Standardabzug           | Währung       |              | X              |
| Limitbetrag für Standardabzug (Basis)    | Währung       |              | X              |
| Limitperiode für Standardabzug           | Option festgelegt     |              | X              |
| Beschreibung                              | Text           |              | X              |
| Wechselkurs                            | Dezimalzahl |              | X              |
| Ist zusätzliche Lohnausführung                | Zwei Optionen    |              | X              |
| Ist meldepflichtig gemäß Affordable Care Act        | Zwei Optionen    |              | X              |
| Wird rückständig generiert                      | Zwei Optionen    |              | X              |
| Ist ein Bruttoausgleich                              | Zwei Optionen    |              | X              |
| Ist primär                               | Zwei Optionen    |              | X              |
| Name                                     | Text           | X            | X              |
| Lohnauswirkung                           | Option festgelegt     |              | X              |
| Pensionierungstyp                          | Option festgelegt     |              | X              |


**Beschäftigungsentität**

| **Felder**                     | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|--------------------------------|----------------|--------------|----------------|
| Angepasstes Startdatum der Arbeitskraft     | Datum und Uhrzeit  |              | X              |
| Firma                        | Suche         | X            | X              |
| Benachrichtigungsfrist Arbeitgebereinheit | Dezimalzahl |              | X              |
| Arbeitgebereinheit der Benachrichtigung        | Option festgelegt     |              | X              |
| Datum des Beschäftigungsendes            | Datum und Uhrzeit  |              | X              |
| Beschäftigtenzahl              | Text           | X            | X              |
| Datum des Beschäftigungsbeginns          | Datum und Uhrzeit  |              | X              |
| Letzter Arbeitstag              | Datum und Uhrzeit  |              | X              |
| Übergangsdatum                | Datum und Uhrzeit  |              | X              |
| Gültig ab                     | Datum und Uhrzeit  | X            | X              |
| Gültig bis                       | Datum und Uhrzeit  |              | X              |
| Arbeitskraft                         | Suche         | X            | X              |
| Kündigungsfrist der Arbeitskraft           | Dezimalzahl |              | X              |
| Startdatum der Arbeitskraft             | Datum und Uhrzeit  |              | X              |
| Arbeitskrafttyp                    | Option festgelegt     | X            | X              |
| Einheit – Kündigungsschreiben für Arbeitskraft          | Option festgelegt     |              | X              |

## <a name="worker-entities"></a>Arbeitskraftentitäten

**Nationalität**

| **Felder**         | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|--------------------|---------------|--------------|----------------|
| Beschreibung        | Text          |              | X              |
| Name der Nationalität | Text          | X            | X              |


**Sprache**

| **Felder**    | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|---------------|---------------|--------------|----------------|
| Beschreibung   | Text          |              | X              |
| Sprachenname | Text          | X            | X              |


**Veteranenstatus**

| **Felder**           | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|----------------------|---------------|--------------|----------------|
| Beschreibung          | Text          |              | X              |
| Ist geschützter Veteran | Zwei Optionen    |              | X              |
| Sprachenname        | Text          | X            | X              |


**Arbeitskraft**

| **Felder**                | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|---------------------------|---------------|--------------|----------------|
| Geburtstag                 | Nur Datum     |              | X              |
| Beschreibung               | Text          |              | X              |
| E-Mail-Adresse 1           | E-Mail         |              | X              |
| E-Mail-Adresse 2           | E-Mail         |              | X              |
| Facebook-Identität         | Text          |              | X              |
| Vorname                | Text          |              | X              |
| Vollständiger Name                 | Text          |              | X              |
| Geschlecht                    | Option festgelegt    |              | X              |
| Generierung                | Text          |              | X              |
| Ist E-Mail-Kontakt zulässig  | Zwei Optionen   |              | X              |
| Ist telefonischer Kontakt zulässig  | Zwei Optionen   |              | X              |
| Nachname                 | Text          |              | X              |
| LinkedIn-Identität         | Text          |              | X              |
| Vorgesetzter                   | Suche        |              | X              |
| Zweiter Vorname               | Text          |              | X              |
| Mobiltelefon              | Telefonnummer         |              | X              |
| Office Graph-Bezeichner   | Text          |              | X              |
| Primäre E-Mail-Adresse     | E-Mail         |              | X              |
| Primäres Telefon         | Telefonnummer         |              | X              |
| Beruf                | Text          |              | X              |
| Soziales Netzwerk 1          | Option festgelegt    |              | X              |
| Soziales Netzwerk 2          | Option festgelegt    |              | X              |
| Identität des sozialen Netzwerks 1 | Text          |              | X              |
| Identität des sozialen Netzwerks 2 | Text          |              | X              |
| Grundlage                    | Option festgelegt    | X            | X              |
| Status                    | Option festgelegt    | X            | X              |
| Telefon 1               | Telefonnummer         |              | X              |
| Telefon 2               | Telefonnummer         |              | X              |
| Telefon 3               | Telefonnummer         |              | X              |
| Twitter-Identität          | Text          |              | X              |
| Benutzer                      | Suche        |              | X              |
| Website-URL               | URL           |              | X              |
| Arbeitskraftnummer             | Text          | X            | X              |
| Arbeitskrafttyp               | Option festgelegt    | X            | X              |
| Yomi-Vorname           | Text          |              | X              |
| Vollständiger Yomi-Name            | Text          |              | X              |
| Yomi-Nachname            | Text          |              | X              |
| Zweiter Yomi-Vorname          | Text          |              | X              |


**Adresse Arbeitskraft**

| **Felder**           | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|----------------------|----------------|--------------|----------------|
| Hausnummer       | Text           | X            | X              |
| Adresstyp         | Option festgelegt     | X            | X              |
| Ort                 | Text           |              | X              |
| Land oder Region    | Text           |              | X              |
| Verwaltungsbezirk               | Text           |              | X              |
| Fax                  | Telefonnummer          |              | X              |
| Ist bevorzugt         | Zwei Optionen    |              | X              |
| Breite             | Dezimalzahl |              | X              |
| Position 1               | Text           |              | X              |
| Position 2               | Text           |              | X              |
| Position 3               | Text           |              | X              |
| Länge            | Dezimalzahl |              | X              |
| PLZ          | Text           |              | X              |
| Postfach      | Text           |              | X              |
| Code der Versandmethode | Ganzzahl   |              | X              |
| Bundesland oder Provinz    | Text           |              | X              |
| Telefon 1          | Telefonnummer          |              | X              |
| Telefon 2          | Telefonnummer          |              | X              |
| Telefon 3          | Telefonnummer          |              | X              |
| UPS-Zone             | Text           |              | X              |
| UTC-Verschiebung           | Ganzzahl   |              | X              |
| Arbeitskraft               | Suche         | X            | X              |


**Persönliches Detail der Arbeitskraft**

| Felder                             | Datentyp    | Erforderlich | Durchsuchbar |
|------------------------------------|--------------|----------|------------|
| Geburtsort                         | Text         |          | X          |
| Geburtsland/-region            | Option festgelegt   |          | X          |
| Geburtstag                          | Nur Datum    |          | X          |
| Staatsangehörigkeit (Land/Region)      | Option festgelegt   |          | X          |
| Todestag                      | Nur Datum    |          | X          |
| Datum der Überprüfung für arbeitsunfähigen Veteran | Nur Datum    |          | X          |
| Ausbildung                          | Text         |          | X          |
| Nationalität                     | Suche       |          | X          |
| ExpatriateEndDate                  | Nur Datum    |          | X          |
| ExpatriateStartDate                | Nur Datum    |          | X          |
| Geburtsland/-region des Vaters     | Option festgelegt   |          | X          |
| Geschlecht                             | Option festgelegt   |          | X          |
| Ist deaktiviert                        | Zwei Optionen  |          | X          |
| Ist arbeitsunfähiger Veteran                | Zwei Optionen  |          | X          |
| Gilt die Regel für ausländische Arbeitskräfte    | Zwei Optionen  |          | X          |
| Ist Vollzeitstudent               | Zwei Optionen  |          | X          |
| Familienstand                     | Option festgelegt   |          | X          |
| Datum des Austritts aus dem Militärdienst          | Nur Datum    |          | X          |
| Datum des Eintritts in den Militärdienst        | Nur Datum    |          | X          |
| Geburtsland/-region der Mutter     | Option festgelegt   |          | X          |
| Nationalitätsland/-region      | Option festgelegt   |          | X          |
| Muttersprache                    | Suche       |          | X          |
| Anzahl der Unterhaltsberechtigten               | Ganzzahl |          |            |
| Veteranenstatus                     | Suche       |          | X          |
| Arbeitskraft                             | Suche       | X        | X          |
| Persönliche Detailnummer der Arbeitskraft      | Text         | X        | X          |


**Arbeitskraftbankkonto**

| **Felder**                 | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|----------------------------|---------------|--------------|----------------|
| Kontoinhaber             | Text          |              | X              |
| Kontokennung     | Text          |              | X              |
| Adressbeschreibung        | Text          |              | X              |
| Bankkontotyp          | Option festgelegt    |              | X              |
| Ortscode der Bank         | Text          |              | X              |
| Zweigstellenname                | Text          |              | X              |
| Zweigstellennummer              | Text          |              | X              |
| Ort                       | Text          |              | X              |
| Land oder Region          | Text          |              | X              |
| Verwaltungsbezirk                     | Text          |              | X              |
| Beschreibung                | Text          |              | X              |
| Ortsteilname              | Text          |              | X              |
| E-Mail                      | Text          |              | X              |
| Durchwahl                  | Text          |              | X              |
| Fax                        | Text          |              | X              |
| IBAN                       | Text          |              | X              |
| Position 1                     | Text          |              | X              |
| Position 2                     | Text          |              | X              |
| Position 3                     | Text          |              | X              |
| Mobiltelefon               | Text          |              | X              |
| Name der Person             | Text          |              | X              |
| PLZ                | Text          |              | X              |
| Postfach            | Text          |              |                |
| Bankleitzahl             | Text          |              | X              |
| Bankleitzahltyp        | Option festgelegt    |              | X              |
| Bundesland oder Provinz          | Text          |              | X              |
| SWIFT-Code                 | Text          |              | X              |
| Telefon                  | Text          |              | X              |
| Telex               | Text          |              | X              |
| Website-URL                | Text          |              | X              |
| Arbeitskraft                     | Suche        | X            | X              |
| Unsere Bankkontonummer | Text          |              | X              |
| Unsere Bankkontonummer | Text          | X            | X              |

**Feste Vergütung für Arbeitskraft**

| Felder                                | Datentyp      | Erforderlich | Durchsuchbar |
|---------------------------------------|----------------|----------|------------|
| Firma                               | Suche         | X        | X          |
| Vergütungstyp                     | Option festgelegt     |          | X          |
| Währung                              | Suche         |          | X          |
| Gültigkeitsdatum                        | Nur Datum      |          | X          |
| Ereignis                                 | Suche         | X        | X          |
| Wechselkurs                         | Dezimalzahl |          | X          |
| Ablaufdatum                       | Nur Datum      |          | X          |
| Positionsnummer                           | Dezimalzahl |          | X          |
| Lohnzahlungshäufigkeit                         | Suche         | X        | X          |
| Lohnsatz                              | Währung       |          | X          |
| Lohnsatz (Basis)                       | Währung       |          | X          |
| Plan                                  | Suche         | X        | X          |
| Position                              | Suche         | X        | X          |
| Prozesstyp                          | Option festgelegt     | X        | X          |
| Referenzpunkt-Einstellungszeile            | Suche         |          | X          |
| Arbeitskraft                                | Suche         | X        | X          |
| Anzahl für feste Arbeitskraftvergütung      | Text           | X        | X          |

**Personenidentifikationsnummer Arbeitskraft**

| Felder                 | Datentyp   | Erforderlich | Durchsuchbar |
|------------------------|-------------|----------|------------|
| Beschreibung            | Text        |          | X          |
| Eintragstyp             | Text        |          | X          |
| Ablaufdatum        | Nur Datum   |          | X          |
| Kennnummer  | Text        | X        | X          |
| Ausweistyp    | Suche      | X        | X          |
| Ist primär             | Zwei Optionen |          | X          |
| Ausstellungsdatum             | Nur Datum   |          | X          |
| Ausstellende Behörde         | Suche      | X        | X          |
| Arbeitskraft                 | Suche      | X        | X          |


## <a name="position-entities"></a>Positionsentitäten

**Stellenposition**

| **Felder**               | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|--------------------------|----------------|--------------|----------------|
| Aktivierung               | Datum und Uhrzeit  |              | X              |
| Für eine Zuweisung verfügbar | Datum und Uhrzeit  |              | X              |
| Abteilung               | Suche         |              | X              |
| Beschreibung              | Text           |              | X              |
| Vollzeitäquivalent     | Dezimalzahl |              | X              |
| Auftrag                      | Suche         | X            | X              |
| Stellenpositionsnummer      | Text           | X            | X              |
| Übergeordnete Stellenposition      | Suche         |              | X              |
| Positionstyp            | Suche         |              | X              |
| Ruhestand               | Datum und Uhrzeit  |              | X              |
| Titel                    | Option festgelegt     |              | X              |
| Gültig ab               | Datum und Uhrzeit  | X            | X              |
| Gültig bis                 | Datum und Uhrzeit  |              | X              |


**Positionstyp**

| **Felder**         | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|--------------------|---------------|--------------|----------------|
| Kostenklassifizierung     | Option festgelegt    |              | X              |
| Beschreibung        | Text          |              | X              |
| Name des Positionstyps | Text          | X            | X              |


**Arbeitskraftzuweisung für die Position**

| **Felder**                        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------------------------|---------------|--------------|----------------|
| Stellenposition                      | Suche        | X            | X              |
| Position Arbeitskraftzuordnungsnummer | Text          | X            | X              |
| Gültig ab                        | Text          | X            | X              |
| Gültig bis                          |               |              | X              |
| Arbeitskraft                            |               | X            | X              |

## <a name="job-entities"></a>Stellenentitäten

**Job**

| **Felder**                   | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|------------------------------|----------------|--------------|----------------|
| Unbegrenzte Positionen zulassen    | Zwei Optionen    |              | X              |
| Standardmäßiges Vollzeitäquivalent | Dezimalzahl |              | X              |
| Beschreibung                  | Text           |              | X              |
| Stellenbeschreibung              | Text           |              | X              |
| Stellenfunktion                 | Suche         |              | X              |
| Stellentyp                     | Suche         |              | X              |
| Maximale Positionsanzahl  | Ganzzahl   |              | X              |
| Name                         | Text           | X            | X              |
| Titel                        | Option festgelegt     |              | X              |
| Gültig ab                   | Datum und Uhrzeit  | X            | X              |
| Gültig bis                     | Datum und Uhrzeit  |              | X              |


**Stellenfunktion**

| **Felder**        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------|---------------|--------------|----------------|
| Beschreibung       | Text          | X            | X              |
| Stellenfnktionsname | Text          | X            | X              |


**Stellentyp**

| **Felder**    | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|---------------|---------------|--------------|----------------|
| Beschreibung   | Text          | X            | X              |
| Befreiungsstatus | Option festgelegt    | X            | X              |
| Stellentypname | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Urlaubs- und Abwesenheitsentitäten

**Urlaubsregistrierung**

| **Felder**            | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------------|---------------|--------------|----------------|
| Grundlage des Abgrenzungsdatums    | Nur Datum     | X            | X              |
| Startdatum Abgrenzung    | Nur Datum     | X            | X              |
| Benutzerdefiniertes Datum           | Nur Datum     | X            | X              |
| Ist Abgrenzung ausgesetzt  | Zwei Optionen   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| Urlaubsplan            | Suche        | X            | X              |
| Startdatum            | Nur Datum     | X            | X              |
| Stufengrundlage            | Option festgelegt    | X            | X              |
| Arbeitskraft                | Suche        | X            | X              |


**Bankgeschäft verlassen**

| **Felder**                    | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|-------------------------------|----------------|--------------|----------------|
| Dauer                        | Dezimalzahl | X            | X              |
| Firma                       | Suche         | X            | X              |
| Nummer Bankgeschäft verlassen | Text           | X            | X              |
| Urlaubsplan                    | Suche         |              | X              |
| Urlaubstyp                    | Suche         | X            | X              |
| Buchungsdatum              | Nur Datum      | X            | X              |
| Buchungsnummer            | Dezimalzahl | X            | X              |
| Buchungstyp              | Option festgelegt     | X            | X              |
| Arbeitskraft                        | Suche         | X            | X              |


**Urlaubsplan**

| **Felder**        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------|---------------|--------------|----------------|
| Antizipierungshäufigkeit | Option festgelegt    | X            | X              |
| Firma           | Suche        | X            | X              |
| Beschreibung       | Text          |              | X              |
| Urlaubstyp        | Suche        | X            | X              |
| Name              | Text          | X            | X              |
| Startdatum        | Nur Datum     | X            | X              |


**Urlaubsanforderung**

| **Felder**           | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|----------------------|---------------|--------------|----------------|
| Kommentar              | Text          | X            | X              |
| Firma              | Suche        | X            | X              |
| Urlaubsanforderungsnummer | Text          |              | X              |
| Anforderungsdatum         | Datum und Uhrzeit | X            | X              |
| Status               | Option festgelegt    | X            | X              |
| Arbeitskraft               | Suche        | X            | X              |


**Urlaubsanforderungsdetail**

| **Felder**                  | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|-----------------------------|----------------|--------------|----------------|
| Dauer                      | Dezimalzahl | X            | X              |
| LeaveDate                  | Datum und Uhrzeit  | X            | X              |
| Urlaubsantrag               | Suche         | X            | X              |
| Urlaubsanforderung-Detailnummer | Text           | X            | X              |
| Urlaubstyp                  | Suche         | X            | X              |


**Urlaubstyp**

| **Felder**      | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------|---------------|--------------|----------------|
| Firma         | Suche        | X            | X              |
| Beschreibung     | Text          |              | X              |
| Einkommenscode    | Suche        |              | X              |
| Name des Urlaubstyps | Text          | X            | X              |


**Arbeitskalender**

| **Felder**  | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------|---------------|--------------|----------------|
| Firma     | Suche        | X            | X              |
| Beschreibung | Text          |              | X              |
| Name        | Text          | X            | X              |


**Arbeitskalendertag**

| **Felder**               | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|--------------------------|---------------|--------------|----------------|
| Kalenderdatum            | Nur Datum     | X            | X              |
| Firma                  | Suche        |              | X              |
| Status                   | Text          |              | X              |
| Arbeitskalender            | Suche        | X            | X              |
| Nummer Arbeitskalendertag | Text          | X            | X              |


**Arbeitskalenderurlaub**

| **Felder**  | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------|---------------|--------------|----------------|
| Name        | Text          |              | X              |
| Beschreibung | Text          | X            | X              |


**Arbeitskalender-Datumsposition**

| **Felder**                        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------------------------|---------------|--------------|----------------|
| Feiertagsdatum                      | Nur Datum     | X            | X              |
| Name                              | Text          |              | X              |
| Arbeitskalenderurlaub             | Suche        | X            | X              |
| Nummer Arbeitskalender-Datumsposition | Text          | X            | X              |


**Arbeitskalender-Zeitintervall**

| **Felder**                         | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|------------------------------------|---------------|--------------|----------------|
| Firma                            | Suche        |              | X              |
| Endzeit                           | Ganzzahl  |              | X              |
| Startzeit                         | Ganzzahl  |              | X              |
| Arbeitskalender                      | Suche        | X            | X              |
| Arbeitskalendertag                  | Suche        | X            | X              |
| Nummer Arbeitskalender-Zeitintervall | Text          | X            | X              |

## <a name="organization-entities"></a>Organisationsentitäten

**Unternehmen**

| **Felder**   | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|--------------|---------------|--------------|----------------|
| Unternehmenscode | Text          | X            | X              |
| Name         | Text          | X            | X              |


**Abteilung**

| **Felder**        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------|---------------|--------------|----------------|
| Abteilungsnummer | Text          | X            | X              |
| Beschreibung       | Text          |              | X              |
| Name              | Text          | X            | X              |
| Übergeordnete Abteilung | Suche        |              | X              |


**Währung**

| **Felder**         | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|--------------------|----------------|--------------|----------------|
| Währungscode      | Text           | X            | X              |
| Währungsname      | Text           | X            | X              |
| Währungsgenauigkeit | Ganzzahl   | X            | X              |
| Währungssymbol    | Text           | X            | X              |
| Entitätsbild       | Bild          |              |                |
| Wechselkurs      | Dezimalzahl | X            | X              |
| Organisation       | Suche         | X            | X              |
| Status             | Option festgelegt     |              | X              |

## <a name="payroll-entities"></a>Lohnentitäten

**Lohnzyklus**

| **Felder**  | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------|---------------|--------------|----------------|
| Beschreibung | Text          | X            | X              |
| Häufigkeit   | Option festgelegt    | X            | X              |
| Name        | Text          | X            | X              |


**Lohnperiode**

| **Felder**           | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|----------------------|---------------|--------------|----------------|
| Standardmäßiges Zahlungsdatum | Nur Datum     |              | X              |
| Beschreibung          | Text          |              | X              |
| Lohnzyklus            | Aussehen          | X            | X              |
| Lohnperiodennummer    | Text          | X            | X              |
| Enddatum der Periode      | Nur Datum     | X            | X              |
| Startdatum der Periode    | Nur Datum     | X            | X              |
| Status               | Option festgelegt    |              | X              |


**Einkommenscode**

| **Felder**              | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------------|---------------|--------------|----------------|
| Beschreibung             | Text          | X            | X              |
| In Zahlungstyp einschließen | Option festgelegt    | X            | X              |
| Ist produktiv           | Zwei Optionen   | X            | X              |
| Name                    | Text          |              | X              |
| Mengeneinheit           | Option festgelegt    |              | X              |
| FMLA-Stunden verfolgen        | Zwei Optionen   |              | X              |


**Steuerregion**

| **Felder**        | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------|---------------|--------------|----------------|
| Ort              | Text          |              | X              |
| Land oder Region | Text          |              | X              |
| Verwaltungsbezirk            | Text          |              | X              |
| Name              | Text          | X            | X              |
| Bundesland oder Provinz | Text          |              | X              |


**Berechnungshäufigkeit Lohnperiode für Vergütungen**

| **Felder**                                      | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-------------------------------------------------|---------------|--------------|----------------|
| Vorteilsberechnungshäufigkeit                   | Suche        | X            | X              |
| Nummer Berechnungshäufigkeit Lohnperiode für Vergütungen | Text          | X            | X              |
| Lohnperiode                                      | Suche        | X            | X              |


**Bankkontoauszahlungen**

| **Felder**                       | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|----------------------------------|----------------|--------------|----------------|
| Dauer                           | Währung       |              | X              |
| Betrag (Basis)                    | Währung       |              | X              |
| Bankkonto                     | Suche         | X            | X              |
| Nummer Bankkontoauszahlungen | Text           | X            | X              |
| Firma                          | Suche         | X            | X              |
| Währung                         | Suche         |              | X              |
| Wechselkurs                    | Dezimalzahl |              | X              |
| Ist Rest                     | Zwei Optionen    |              | X              |
| Priorität                         | Ganzzahl   |              | X              |

**Ausstellende Agentur für Personenidentifikation**

| **Felder**           | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|----------------------|---------------|--------------|----------------|
| Adressbeschreibung  | Text          |              | X              |
| Adresszeile 1       | Text          |              | X              |
| Adresszeile 2       | Text          |              | X              |
| Adresszeile 3       | Text          |              | X              |
| Ort                 | Text          |              | X              |
| Land oder Region    | Option festgelegt    |              | X              |
| Verwaltungsbezirk               | Text          |              | X              |
| Beschreibung          | Text          |              | X              |
| E-Mail                | Text          |              | X              |
| Durchwahl            | Text          |              | X              |
| Fax                  | Text          |              | X              |
| Name der ausstellenden Behörde  | Text          | X            | X              |
| Mobiltelefon         | Text          |              | X              |
| Seite                 | Text          |              | X              |
| PLZ          | Text          |              | X              |
| Postfach      | Text          |              | X              |
| SMS                  | Text          |              | X              |
| Bundesland oder Provinz    | Text          |              | X              |
| Telefon            | Text          |              | X              |
| Telex                | Text          |              | X              |
| Website-URL          | Text          |              | X              |

**Personenidentifikationstyp Arbeitskraft**

| **Felder**                        | **Datentyp**  | **Erforderlich** | **Durchsuchbar** |
|-----------------------------------|----------------|--------------|----------------|
| Zulässige Werte                    | Option festgelegt     |              | X              |
| Land oder Region                 | Text           |              | X              |
| Beschreibung                       | Text           |              | X              |
| Feste Länge                      | Ganzzahl   |              | X              |
| Steuernummerformat      | Text           |              | X              |
| Typ                              | Option festgelegt     |              | X              |
| Personenidentifikationstyp Arbeitskraft | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Entitäten für feste Vergütung

**Plan für feste Vergütung**

| **Felder**                  | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------------------|---------------|--------------|----------------|
| Firma                     | Suche        | X            | X              |
| Vergütungsraster           | Suche        |              | X              |
| Währung                    | Suche        | X            | X              |
| Beschreibung                 | Text          | X            | X              |
| Gültigkeitsdatum              | Nur Datum     | X            | X              |
| Ablaufdatum             | Nur Datum     | X            | X              |
| Einstellungsregel                   | Option festgelegt    | X            | X              |
| Name                        | Text          | X            | X              |
| Außerhalb des zulässigen Bereichs (Toleranz)      | Option festgelegt    | X            | X              |
| Lohnzahlungshäufigkeit               | Suche        | X            | X              |
| Empfehlung zulässig      | Zwei Optionen   | X            | X              |
| Referenzpunkt-Positionseinstellung  | Suche        |              | X              |
| Typ                        | Option festgelegt    | X            | X              |

**Vergütungsraster**

| **Felder**                  | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------------------|---------------|--------------|----------------|
| Firma                     | Suche        | X            | X              |
| Währung                    | Suche        |              | X              |
| Beschreibung                 | Text          | X            | X              |
| Gültigkeitsdatum              | Nur Datum     |              | X              |
| Ablaufdatum             | Nur Datum     |              | X              |
| Name                        | Text          | X            | X              |
| Referenzpunkteinstellung       | Suche        | X            | X              |
| Typ                        | Option festgelegt    | X            | X              |

**Vergütungsstufe**

| **Felder**      | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------|---------------|--------------|----------------|
| Beschreibung     | Text          |              | X              |
| Name            | Text          | X            | X              |
| Typ            | Option festgelegt     | X            | X              |

**Häufigkeit der Vergütungszahlung**

| **Felder**                  | **Datentyp**   | **Erforderlich** | **Durchsuchbar** |
|-----------------------------|-----------------|--------------|----------------|
| Jährlicher Umrechnungsfaktor    | Dezimalzahl  |              | X              |
| Firma                     | Suche          | X            | X              |
| Beschreibung                 | Text            |              | X              |
| Stündlicher Umrechnungsfaktor    | Dezimalzahl  |              | X              |
| Monatlicher Umrechnungsfaktor   | Dezimalzahl  |              | X              |
| Name                        | Text            | X            | X              |
| Periode                      | Option festgelegt      |              | X              |
| Wöchentlicher Umrechnungsfaktor    | Option festgelegt      |              | X              |


**Vergütungsreferenzpunkten einrichten**

| **Felder**          | **Datentyp**   | **Erforderlich** | **Durchsuchbar** |
|---------------------|-----------------|--------------|----------------|
| Firma             | Suche          | X            | X              |
| Vergütungstyp   | Option festgelegt      | X            | X              |
| Beschreibung         | Text            | X            | X              |
| Name                | Text            | X            | X              |

**Vergütungsreferenzpunktzeile einrichten**

| **Felder**            | **Datentyp**   | **Erforderlich** | **Durchsuchbar** |
|-----------------------|-----------------|--------------|----------------|
| Firma               | Suche          | X            | X              |
| Beschreibung           | Text            | X            | X              |
| Positionsnummer           | Dezimalzahl  | X            | X              |
| Name                  | Text            | X            | X              |
| Referenzpunkteinstellung | Suche          | X            | X              |

**Kompensationsregion**

| **Felder**      | **Datentyp** | **Erforderlich** | **Durchsuchbar** |
|-----------------|---------------|--------------|----------------|
| Beschreibung     | Text          | X            | X              |
| Name            | Text          | X            | X              |

**Vergütungsstruktur**

| **Felder**                    | **Datentyp**   | **Erforderlich** | **Durchsuchbar** |
|-------------------------------|---------------  |--------------|----------------|
| Dauer                        | Währung        |              | X              |
| Grundbetrag                   | Währung        |              | X              |
| Firma                       | Suche          | X            | X              |
| Vergütungsstrukturnummer | Text            | X            | X              |
| Währung                      | Suche          |              | X              |
| Wechselkurs                 | Dezimalzahl  |              | X              |
| Raster                          | Suche          | X            | X              |
| Stufe                         | Suche          | X            | X              |
| Referenzpunkt               | Suche          | X            | X              |
| Referenzpunkt-Positionseinstellung    | Suche          | X            | X              |

**Ereignis für feste Vergütung**

| **Felder**            | **Datentyp**   | **Erforderlich** | **Durchsuchbar** |
|-----------------------|-----------------|--------------|----------------|
| Firma               | Suche          | X            | X              |
| Beschreibung           | Text            | X            | X              |
| Ereignistyp            | Option festgelegt      | X            | X              |
| Ist aktiv             | Zwei Optionen     | X            |                |
| Name                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Entitätsbeziehungsmodelle

### <a name="worker"></a>Arbeitskraft
![Arbeitskraft](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Stelle und Stellenposition
![Stelle und Stellenposition](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Vergütungen
![Vergütungen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensation
![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Verlasen
![Verlasen](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbeitskalender
![Arbeitskalender](./media/HCMCommon-work-calendar-entity-diagram.png)
