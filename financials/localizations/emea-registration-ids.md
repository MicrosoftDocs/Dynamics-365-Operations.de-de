---
title: Registrierungskennungen
description: "Dieses Thema enthält Informationen zum Einrichten und Verwenden der Erfassung auf."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Registrierungskennungen

Dieses Thema enthält Informationen zum Einrichten und Verwenden der Erfassung auf.

Viele Länder und Regionen der Erde Bestimmungen und Anforderungen für das Erfassen von Registrierungsnummern von oder auf. Dieses Thema enthält einen Überblick der erforderlichen Einstellungen und Verarbeiten der unterstützten Erfassungstypen für Parteien in verschiedenen europäischer Länder/in Regionen verfügbar. Alle Länder/Regionen sind die Anforderungen zur Unterstützung von verschiedenen Funktionen landesspezifischen, die Registrierungsnummern zugeordnet werden, die von der Behörde des unterschiedlichen Zustandes bereitgestellt werden. Beispiele für Registrierungsnummern enthalten, Sozialversicherungsnummer (SSN), MwSt europäische Steuerkennungsnummer (TIN) und die Kennung der Ergebnisgruppe. Kennung (EU MwSt.). Diese Funktion bietet einheitliches Framework für alle Länder in allen Regionen verfügbar, die Anforderungen von einigen landesspezifische europäischer Länder berücksichtigen. In den folgenden Abschnitten wird der Gesamtinformationsfluss, der für Einrichtung und Verarbeitung von Kennungen Erfassung verwendet wird.

## <a name="registration-type-creation"></a>Erfassungstyperstellung
Bevor Sie Erfassungskennung eingeben können, müssen Sie für die Erfassungstypen unterschiedlichen Arten von Registrierungsnummern ein, die die einzelnen Parteien aus abhängig ist. Wechseln ** Organisationsverwaltung ** ** &gt; globales Adressbuch ** ** &gt; Erfassungstypen ** ** &gt; Erfassungstypen ** die Seite, um mit Erfassungstypen für Kreditoren, Debitoren, Arbeitskräfte und juristischen Personen in verschiedenen Land/Region erstellen und verwalten.

|Feld                 |Beschreibung      |
|------------------------------|----------------------------|                                                                           
| Name                | Der Name des Erfassungstyps. |                                                                           
| Beschreibung         | Die Beschreibung des Erfassungstyps. |
| Land/Region      | Die eindeutige Kennung für Land/Region.|
| Steuerbehörde       | Die Steuerbehörde, die dem Typ zugeordnet ist.|
| Beschränkt auf       | Der Typ der Einschränkung, die auf den Steuererfassungstyp gilt: Keine, Organisation, Person.|
| Formate              | Das Prüfungsformat für den Erfassungstyp.|
| Aktualisierbar      | Definiert, wenn die Bankleitzahl für den Erfassungstyp aktualisiert werden kann, nachdem diese eingegeben wurde.|
| Eindeutig              | Definiert, wenn die Bankleitzahl für den Erfassungstyp eindeutig ist. |
| Primär für Land | Wenn eine Partei Länder mit einer oder mehrerer der Lieferverarbeitung Adressen zugeordnet ist und die Erfassungskennung für alle Adressen diese gültig ist, müssen Sie eine auswählen, Adresse primär für das Land. Sie können nur eine Kennung erfassen, primär. Definiert, wenn die Registrierungsnummer nur für Landadresse primäres für eingegeben werden kann. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Zuweisen einer Erfassungskategorie einen Erfassungstyp zu
Erfassungskategorie ist die Land/Regions- kennung, die für Länder/Regionen für Steuer, Zoll und insbesondere anderen Zwecken verwenden genehmigt wird. Diese Kategorie definiert Validierungsregeln bestimmter Erfassungskennung (einschließlich Prüfzifferenusw.) und der Einbeziehungs erfassung Kennung in den unterschiedlichen Berichten. Verwenden Sie die Seite ** Organisationsverwaltung ** ** &gt; globales Adressbuch ** ** &gt; Erfassungstypen ** ** &gt; Erfassungskategorien ** Der Erfassungstyp des bestimmtes Land zugewiesen der unterstützten Erfassungskategorie.

| Feld            | Beschreibung|
|-----------------------|----------------|
| Registrierungstyp     | Das Land/Region des Erfassungstyps insbesondere.|
| Beschränkt auf         | Der Typ der Einschränkung gilt für den Steuererfassungstyp zu: Keine, Organisation, Person.|
| Registrierungskategorie | Die eindeutige Erfassungskennung genehmigt für die Verwendung im Land. Die vollständige Liste der unterstütztem in den Kategorien AX7.1 befindet sich unten. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Geben Erfassung Sie Kennungen für Datensätze des globalen Adressbuchs ein
Das globale Adressbuch (GAB) in Microsoft Dynamics 365 für Arbeitsgänge enthält konsolidierte Adressinformationen für Debitoren, Kreditoren, Kontakte, Geschäftsbeziehungen und juristischen Personen. Weitere Informationen finden Sie, [Übersicht des globalen Adressbuchs] (/dynamics365/operations/organization-administration/overview-global-address-book). Die, die Parteidatensätze im globalen Adressbuch gespeichert werden, können eine oder mehrere der Adressdatensätze enthalten. Diese Adressen werden für verschiedene Zwecke verwendet, z. B. für Rechnungsstellung oder Lieferung. Erfassung können Sie Kennungen für Adressinformationen für Debitoren, Kreditoren, Arbeitskräfte und juristische Personen einrichten. Durchsuchen der Partei (juristische Personen, Kreditoren, Debitoren, Arbeitskraft" Datensatz für die, das Sie der Register Kennung eingeben möchten, und klicken dann Erfassungs-IDs ** ** in den Formularen, die für die Partei, juristische Personen, Kreditoren, Debitoren, Arbeitskraft zugeordnet werden, die Sie verwalten ** Adressen ** Seite zu öffnen. Auf der Steuerregistrierung ** ** Registerkarte geben Sie ** Hinzufügen ** und folgende Informationen zum Erfassungs- Kennung ein

|Feld                |Beschreibung                                                |
|---------------------|-----------------------------------------------------------|
| Registrierungstyp   | Der Erfassungstyp im Formular ausgewählten Landes/der Region.     |
| Registrierungsnummer | Die Kennung Parteienerfassung                                |
| Beschreibung         | Die Beschreibung zur Erfassungsnummer.               |
| Abschnitt             | Die zusätzliche Information zur Erfassungsnummer. |
| Ausstellende Behörde      | Die Regierungsbehörde, die ausgestellt der Erfassungsnummer.        |
| Ausstellungsdatum         | Das Datum für die ausgegebene Nummer.              |
| Gültig           | Das Gültigkeitsdatum für die Registrierungsnummer.           |
| Ablauf          | Das Ablaufdatum für die Registrierungsnummer.          |

> [!NOTE]
> Die Umsatzsteuernummer der juristischen Person, Kreditor, Debitor kann von Erfassung IDs ausgewählt werden, die der MwSt. -ID zugeordnet sind und für die Partei eingegeben wurden.

## <a name="search-for-records-by-registration-id"></a>Suche für Datensätze nach Erfassungskennung
Suche für Parteidatensätze auf einer Erfassungskennung ist in die Steuerformulare verfügbar, die für die Partei, zur juristischen Person, den Kreditor, z Debitor und der Arbeitskraft zugeordnet werden. ** Auf Erfassung ID-Suche ** um die Erfassung ID-Suchkriterien ** ** Seite zu öffnen. Geben Sie Suchkriterien angezeigt und klicken Sie ** ** Suche. Im System werden die ausgewählten Datensätze aus dem globalen Adressbuch zugeordnete und die Typen des Parteidatensatzes angezeigt.

## <a name="supported-registration-categories"></a>Unterstützte Erfassungskategorien
In der folgenden Tabelle werden die unterstützten Erfassungstypen in Dynamics 365 für Arbeitsgänge auf. Wenn Sie mit den Microsoft Dynamics AX 2012-Feldern für IDs Erfassung kennen, ordnet diese Tabelle auch diesen Feldern in Dynamics 365 für Arbeitsgangserfassungskategorien zu.

| Dynamics 365 für Arbeitsgangs-Erfassungskategorie         |Land/Region  | Bedingung/Feld Dynamics AX 2012|
|---------------------------------------------------------------|---------------------|---------------------------------|
| MwSt.-Kennung                                                        | Alle Länder der Europäischen Union (EU)|  Steuernummer (Gesetzgebungstyp in STEUER-ID AX2012 R3)|
| Enterprise-ID (COID)                                          | Tschechische Republik Estland Ungarn Lettland Litauen Polen die Schweiz Belgiens | Registrierungsnummer der Unternehmensnummeren- (EnterpriseNumber) (RegNum Registrierungsnummer \_W) (RegNum Registrierungsnummer\_W) (RegNum Registrierungsnummer\_W) (Code RegNum\_W) (Enterprise EnterpriseCode) Registrierungsnummer (UID RegNum\_W) (Gesetzgebungstyp UID in AX2012 R3) |
| Zweigstellenkennung                                                     | Belgien            | Nummer (BranchNumber)|
| (Spisová-značka Registrierungsnummer, Behörde, Abschnitt ausgebend) | Tschechische Republik     | Abgesenkte Nummer (CommercialRegisterInsetNumber) an einem Handelsregister () CommercialRegister Abschnitt des Handelsregisters (CommercialRegisterSection )|
| Zolldebitorkennung                                           | Finnland | Gewohnheitsdebitornummer (CustomsCustomerNumber \_"|
| INN                                                           | Russische Föderation| INN (Gesetzgebungstyp in INN AX2012 R3)|
| RRC                                                           | Russische Föderation| RRC (Gesetzgebungstyp in RRC AX2012 R3)|
| OKDP                                                          | Russische Föderation| OKDP (Gesetzgebungstyp in OKDP AX2012 R3)|
| OKPO                                                          | Russische Föderation| OKPO (Gesetzgebungstyp in OKPO AX2012 R3)|
| RCOAD                                                         | Russische Föderation| RCOAD (Gesetzgebungstyp in RCOAD AX2012 R3)|
| OGRN                                                          | Russische Föderation| OGRN (Gesetzgebungstyp in OGRN AX2012 R3) |
| SNILS                                                         | Russische Föderation| SNILS (Gesetzgebungstyp in SNILS AX2012 R3)|
| CIFTS                                                         | Russische Föderation| CIFTS (Gesetzgebungstyp in CIFTS AX2012 R3)|

Weitere Informationen zum Zuordnen Erfassung Kennungen, einschließlich erforderliche Voraussetzungen, werden die folgenden Aufgabenaufzeichnungen für Mehrwertsteuer. -ID in den Lebenszyklus-Dienstleistungen (LCS):

-   Einrichten der MwSt Kennung
-   MwSt.-ID-Erfassung des Kreditors
-    Suche nach Partei per MwSt.-Kennung



