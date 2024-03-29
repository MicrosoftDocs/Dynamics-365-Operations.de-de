---
title: Registrierungskennungen
description: Unter den Themen in diesem Artikel finden Sie Informationen zum Einrichten und Verwalten von Anmelde-IDs.
author: kfend
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264824
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
ms.openlocfilehash: 380cb1d2b52d5d0debffdbe73183be2f5e783f21
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274550"
---
# <a name="registration-ids"></a>Registrierungskennungen

[!include [banner](../includes/banner.md)]

Unter den Themen in diesem Artikel finden Sie Informationen zum Einrichten und Verwalten von Anmelde-IDs.

Viele Länder und Regionen haben unterschiedliche Bestimmungen und Anforderungen für das Erfassen Registrierungsnummern oder IDs. Dieser Artikel enthält einen Überblick der erforderlichen Einstellungen und über die Verarbeitung der unterstützten Erfassungstypen für Parteien in verschiedenen europäischen Ländern/Regionen. Alle Länder/Regionen habe Ihre Anforderungen zur Unterstützung von verschiedenen landesspezifischen Funktionen, die Registrierungsnummern zugeordnet werden, die von verschiedenen Stellen bereitgestellt werden. Beispiele für Registrierungsnummern enthalten Sozialversicherungsnummer (SSN), Steuerkennungsnummer (TIN) und die Kennung der MwSt-Kennung (EU MwSt. ID). Diese Funktion bietet ein einheitliches Framework für alle Länder in allen Regionen, die Anforderungen von einigen landesspezifischen europäischen Ländern berücksichtigen. Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für die Einrichtung und Verwaltung der Registrations-IDs verwendet wird.

## <a name="registration-type-creation"></a>Registrationstyperfassung
Bevor Sie Registrierungsnummern-IDs einrichten können, müssen Sie die Registrierungstypen für die unterschiedlichen Arten von Registrierungsnummern, denen die einzelnen Parteien unterworfen sind. Gehen Sie zu **Organisationsverwaltung** &gt; **Globales Adressbuch** &gt; **Erfassungstypen** &gt;, um die **Erfassungstypen** für Kreditoren, Debitoren, Arbeitskräfte und juristischen Personen in verschiedenen Ländern/Region zu erstellen und zu verwalten.

|Feld                 |Beschreibung      |
|------------------------------|----------------------------|                                                                           
| Name                | Hier können Sie den Namen des Registrationstyps eingeben. |                                                                           
| Beschreibung         | Beschreibung des Reigstrationstyps. |
| Land/Region      | Die eindeutige Kennung für Land/Region.|
| Steuerbehörde       | Die Steuerbehörte, die dem Registrationstyp zugeordnet ist|
| Beschränkt auf       | Der Typ der Einschränkung, die auf den Steuererfassungstyp gilt: Keine, Organisation, Person.|
| Formate              | Das Überprüfungsformat für den Steuerregistrierungstyp.|
| Aktualisierbar      | Wenn dieses Kontrollkästchen aktiviert ist, kann die Registrierungsnummer aktualisiert werden, nachdem sie für den Steuerregistrierungstyp eingegeben wurde.|
| Eindeutig              | Wenn dieses Kontrollkästchen aktiviert ist, ist die Registrierungsnummer für den Steuerregistrierungstyp eindeutig. |
| Primär für Land | Wenn eine Partei Ländern mit einer oder mehreren Lieferverarbeitungs-Adressen zugeordnet ist und die Erfassungskennung für alle Adressen gültig ist, müssen Sie eine Hauptadresse für das Land auswählen. Sie können nur eine Kennung als primär erfassen. Definiert, wenn die Registrierungsnummer nur promär für Landadresse eingegeben werden kann. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Zuweisen eines Typs für eine Kategoriehierarchie.
Erfassungskategorie ist die Land/Regionskennung, die für Länder/Regionen für Steuer, Zoll und insbesondere anderen Zwecken verwendet wird. Diese Kategorie definiert Validierungsregeln bestimmter Erfassungskennung (einschließlich Prüfzifferenvusw.) und unter Einbeziehung der Erfassungskennung in den unterschiedlichen Berichten. Verwenden Sie die Seite **Organisationsverwaltung** &gt; **Globales Adressbuch** &gt; **Erfassungstypen** &gt; **Erfassungskategorien**, Erfassungstypen des bestimmtes Land zuzuweisen, um die Erfassungskategorie zu unterstützen.

| Feld            | Beschreibung|
|-----------------------|----------------|
| Registrierungstyp     | Das Land/Region des Erfassungstyps|
| Beschränkt auf         | Der Typ der Einschränkung, die auf den Steuererfassungstyp gilt: Keine, Organisation, Person.|
| Registrierungskategorie | Die eindeutige Erfassungskennung genehmigt für die Verwendung im Land. Die vollständige Liste der unterstützten Kategorien wird später in diesem Artikel gezeigt. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Geben die Erfassung-ID für globale Adressbuchdatensätze ein

Das globale Adressbuch (GAB) enthält konsolidierte Adressinformationen für Debitoren, Kreditoren, Kontakte, Geschäftsbeziehungen und juristischen Personen. Weitere Informationen finden Sie unter [Globales Adressbuch](../../fin-ops-core/fin-ops/organization-administration/overview-global-address-book.md). Die Parteidatensätze, die im globalen Adressbuch gespeichert sind, können einen oder mehrere Adressdatensätze enthalten. Diese Adressen werden für verschiedene Zwecke verwendet, z. B. für Rechnungsstellung oder Lieferung. Sie können Erfassungs-IDs für Adressinformationen für Debitoren, Kreditoren, Arbeitskräfte und juristische Personen einrichten. Suchen Sie den Datensatz für die Partei (juristische Personen, Kreditoren, Debitoren, Arbeitskraft) für die Sie die Registerkennung eingeben möchten, und klicken dann **Erfassungs-IDs** in den Formularen, die mit der Partei, juristischen Personen, Kreditoren, Debitoren, Arbeitskraft verknüpft ist, um die Seite **Adresse verwalten** zu öffnen. Auf der **Steuerregistrierung** Registerkarte klicken Sie **Hinzufüge** und geben folgende Informationen zur Erfassungs-ID ein


|Feld                |Beschreibung                                                |
|---------------------|-----------------------------------------------------------|
| Registrierungstyp   | Der Erfassungstyp des ausgewählten Lands/Region.     |
| Registrierungsnummer | Die Partei-Kennungs-ID.                                |
| Beschreibung         | Beschreibung des Reigstrationsnummer.               |
| Abschnitt             | Die zusätzlichen Informationen über die Registrationsnummer. |
| Ausstellende Behörde      | Die Behörde, von der die Registrierungsnummer stammt.        |
| Ausstellungsdatum         | Das Ausgabedatum für die Steuernummer.              |
| Gültig           | Das effektive Datum für die Steuernummer.           |
| Ablauf          | Das Ablaufdatum für die Registrationsnummer.          |

> [!NOTE]
> Die Umsatzsteuernummer der juristischen Person, Kreditor, Debitor kann von der Registrations-IDs ausgewählt werden, die der MwSt.-ID zugeordnet sind und für die Partei eingegeben wurden.

## <a name="search-for-records-by-registration-id"></a>Suche für Datensätze nach Erfassungskennung
Suche für Parteidatensätze auf einer Erfassungskennung ist in die Steuerformulare verfügbar, die für die Partei, zur juristischen Person, den Kreditor, z Debitor und der Arbeitskraft zugeordnet werden. Klicken Sie auf **Erfassung ID-Suche**, um die Seite **Erfassung ID-Suchkriterien** zu öffnen. Definieren Sie die Suchkriterien und klicken Sie auf **Suchen**. Im System werden die ausgewählten Datensätze aus dem globalen Adressbuch zugeordnet und die Typen des Parteidatensatzes angezeigt.

## <a name="supported-registration-categories"></a>Unterstützte Registrierungskategorien
In der folgenden Tabelle werden die unterstützten Registrierungstypen aufgeführt. Wenn Sie mit den Microsoft Dynamics AX 2012-Feldern für Registrierungskennungen vertraut sind: Diese Tabelle ordnet diese Felder auch den Registrierungskategorien von Dynamics 365 Finance zu.

| Finance-Registrierungskategorie         |Land/Region  | Dynamics AX 2012 – Begriff/Feld|
|---------------------------------------------------------------|---------------------|---------------------------------|
| MwSt.-Kennung                                                        | Alle Länder der Europäischen Union (EU)|  Umsatzsteuernummer (Gesetzgebungstyp STEUER-ID in AX 2012 R3)|
| Enterprise-ID (COID)                                          | Belgien, Tschechische Republik, Estland, Ungarn, Lettland, Litauen, Polen, Schweiz | Unternehmensnummer (EnterpriseNumber) Registrierungsnummer (RegNum\_W) Registrierungsnummer (RegNum\_W) Registrierungsnummer (RegNum\_W) Registrierungsnummer (RegNum\_W) Unternehmenscode (EnterpriseCode) Registrierungsnummer (RegNum\_W) UID (Gesetzgebungstyp UID in AX 2012 R3) |
| Zweigstellenkennung                                                     | Belgien            | Zweigstellennummer (BranchNumber)|
| (Spisová-značka Registrierungsnummer, ausgebende Behörde, Abschnitt) | Tschechische Republik     | Einsatznummer (CommercialRegisterInsetNumber). Im Handelsregister (CommercialRegister) Abschnitt des Handelsregisters (CommercialRegisterSection )|
| Zolldebitorkennung                                           | Finnland | Zolldebitorennummer (CustomsCustomerNumber\_FI)|
| INN                                                           | Russische Föderation| INN (Gesetzgebungstyp INN in AX 2012 R3)|
| RRC                                                           | Russische Föderation| RRC (Gesetzgebungstyp RRC in AX 2012 R3)|
| OKDP                                                          | Russische Föderation| OKDP (Gesetzgebungstyp OKDP in AX 2012 R3)|
| OKPO                                                          | Russische Föderation| OKPO (Gesetzgebungstyp OKPO in AX 2012 R3)|
| RCOAD                                                         | Russische Föderation| RCOAD (Gesetzgebungstyp RCOAD in AX 2012 R3)|
| OGRN                                                          | Russische Föderation| OGRN (Gesetzgebungstyp OGRN in AX 2012 R3) |
| SNILS                                                         | Russische Föderation| SNILS (Gesetzgebungstyp SNILS in AX 2012 R3)|
| CIFTS                                                         | Russische Föderation| CIFTS (Gesetzgebungstyp CIFTS in AX 2012 R3)|
| Ausweis                                                      | Spanien             | Ausweis|
| Offizielles Ausweisdokument                              | Spanien             | Offizielles Ausweisdokument|
| Wohnsitzbescheinigung                                         | Spanien             | Wohnsitzbescheinigung|
| Anderes Ausweisdokument                                 | Spanien             | Anderes Ausweisdokument|
| Nicht erfasst                                                  | Spanien             | Nicht in AX 2012 R3 verfügbar|


Weitere Informationen zum Zuordnen von Erfaassungskennungen einschließlich erforderliche Voraussetzungen, finden Sie in den folgenden Aufgabenaufzeichnungen für Mehrwertsteuer-IDs in den Lebenszyklus-Dienstleistungen (LCS):

-   Einrichten der MwSt Kennung
-   MwSt-Registrierungs-ID des der Kreditors
-    Suche nach Partei per MwSt.-Kennung






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
