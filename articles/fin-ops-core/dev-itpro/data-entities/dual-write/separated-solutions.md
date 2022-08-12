---
title: Getrenntes Dual-write Application Orchestration Paket
description: Das Paket Dual-write Application Orchestration ist nicht mehr ein einzelnes Paket, sondern wurde in kleinere Pakete aufgeteilt. Dieser Artikel erklärt die Lösungen und Zuordnungen, die jedes Paket enthält, sowie seine Abhängigkeit von anderen Paketen.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 28c321ee2815b2886c07bfb0996870e536458145
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111659"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Getrenntes Dual-write Application Orchestration Paket

[!include [banner](../../includes/banner.md)]



Zuvor war das Dual-write Application Orchestration-Paket ein einzelnes Paket, das die folgenden Lösungen enthielt:

- Dynamics 365 Notes
- Dynamics 365 Finance and Operations Allgemeiner Anker
- Dynamics 365 Finance and Operations Dual-write Entity Maps
- Dynamics 365 Asset-Management App
- Dynamics 365 Asset-Management
- HCM Common
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations Allgemein
- Dynamics 365 Company
- Währungswechselsätze
- Field Service Common

Da es sich um ein einziges Paket handelte, erstellte dieses Paket eine „Alles-oder-Nichts“-Situation für Kunden. Microsoft hat sie jedoch jetzt in kleinere Pakete aufgeteilt. Kunden können also nur die Pakete für die Lösungen auswählen, die sie benötigen. Wenn Sie zum Beispiel ein Microsoft Dynamics 365 Supply Chain Management-Kunde sind und keine Integration mit Dynamics 365 Human Resources, Notizen und Asset-Management benötigen, können Sie diese Lösungen aus den installierten Lösungen ausschließen. Da die zugrundeliegenden Lösungsnamen, Publisher und Zuordnungsversionen gleich bleiben, ist diese Änderung nicht bahnbrechend. Bestehende Installationen können aktualisiert werden.

![Getrenntes Paket.](media/separated-package-1.png)

Dieser Artikel erklärt die Lösungen und Zuordnungen, die jedes Paket enthält, sowie seine Abhängigkeit von anderen Paketen.

## <a name="dual-write-application-core"></a>Dual-write Application Core

Mit dem Dual-write Application Core-Paket können Benutzer Dual-write ohne eine Customer-Engagement-App installieren und konfigurieren. Es enthält die folgenden fünf Lösungen.

| Eindeutiger Name                           | Anzeigename                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations – Allgemein |
| CurrencyExchangeRates                 | Währungswechselsätze                    |
| msdyn_DualWriteAppCoreMaps            | Dual-write Applications Core Zuordnung von Entitäten   |
| msdyn_DualWriteAppCoreAnchor          | Dual-write Application Core Anker        |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanz- und Betriebs-Apps     | Customer Engagement-Apps                    |
|---------------------------------|---------------------------------------------|
| Organisationseinheit                  | msdyn_internalorganizations                 |
| Organisationshierarchie          | msdyn_internalorganizationhierarchies       |
| Juristische Personen                  | msdyn_internalorganizations                 |
| Juristische Personen                  | cdm_companies                               |
| Organisationshierarchiezwecke | msdyn_internalorganizationhierarchypurposes |
| Währungspaar für Wechselkurs     | msdyn_currencyexchangeratepairs             |
| Namensaffixe                    | msdyn_nameaffixes                           |
| Wechselkurstyp              | msdyn_exchangeratetypes                     |
| CDS-Wechselkurse              | msdyn_currencyexchangerates                 |
| Organisationshierarchietyp     | msdyn_internalorganizationhierarchytypes    |
| Währungen                      | transactioncurrencies                       |
| Mixed Reality-Anleitungsentität     | msmrw_guides                                |

**Abhängigkeitsinformationen**

Das Dual-write Application Core-Paket ist nicht von anderen Paketen abhängig.

## <a name="dual-write-human-resources"></a>Dual-write Human Resources

Das Dual-write Human Resources Paket enthält die Lösungen und Zuordnungen, die für die Synchronisierung von Human Resources Daten erforderlich sind. Es enthält die folgenden drei Lösungen.

| Eindeutiger Name                | Anzeigename                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM Common                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources Entitäten-Zuordnungen |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources Anker      |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanz- und Betriebs-Apps | Customer Engagement-Apps         |
|-----------------------------|----------------------------------|
| Nationalitäten              | cdm_ethnicorigins                |
| Vergütung (Stellenfunktion)   | cdm_jobfunctions                 |
| Positionen V2                | cdm_jobpositions                 |
| Stellen                        | cdm_jobs                         |
| Vergütung (Stellentyp)       | cdm_jobtypes                     |
| Sprachcodes              | cdm_languages                    |
| Positionstyp               | cdm_positiontypes                |
| Arbeitskraftzuweisungen für die Position | cdm_positionworkerassignmentmaps |
| Veteranenstatus              | cdm_veteranstatuses              |
| Worker                      | cdm_workers                      |
| Beschäftigung pro Unternehmen      | cdm_employments                  |

**Abhängigkeitsinformationen**

Das Dual-write Human Resources Paket hängt vom Dual-write Application Core Paket ab. Daher sollten Sie das Paket Dual-write Application Core installieren, bevor Sie das Paket Dual-write Human Resources installieren.

## <a name="dual-write-supply-chain"></a>Dual-write Supply Chain

Das Dual-write Supply Chain Paket enthält die Lösungen und Zuordnungen, die für die Synchronisierung von Supply Chain Management Daten erforderlich sind. Es enthält die folgenden drei Lösungen.

| Eindeutiger Name                                | Anzeigename                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management erweiterte Zuordnung von Entitäten |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management erweiterter Anker      |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanz- und Betriebs-Apps                 | Customer Engagement-Apps                      |
|---------------------------------------------|-----------------------------------------------|
| Einheiten                                       | uoms                                          |
| Auftragskopfzeilen CDS                     | salesorders                                   |
| CDS-Auftragspositionen                       | salesorderdetails                             |
| CDS-Verkaufsangebotskopf                  | Angebote                                        |
| CDS-Verkaufsangebotspositionen                   | quotedetails                                  |
| Von CDS freigegebene eindeutig identifizierbare Produkte              | Produkte                                      |
| Lagerortzonen                             | msdyn_warehousezones                          |
| Lagerortzonengruppen                       | msdyn_warehousezonegroups                     |
| Lagerort-Arbeitspositionen                        | msdyn_warehouseworklines                      |
| Lagerort-Arbeitskopfzeilen                      | msdyn_warehouseworkheaders                    |
| Lager                                  | msdyn_warehouses                              |
| Gang im Lager                             | msdyn_warehouseaisles                         |
| Einheitenumrechnungen                            | msdyn_unitofmeasureconversions                |
| Lieferbedingungen                           | msdyn_termsofdeliveries                       |
| Lieferarten                           | msdyn_shipvias                                |
| Produktmasterstile                       | msdyn_sharedproductstyles                     |
| Verkaufsrechnungspositionen V2                      | Rechnungsdetails                                |
| Verkaufsrechnungskopfzeilen V2                    | Rechnungen                                      |
| Produktmastergrößen                        | msdyn_sharedproductsizes                      |
| Freigegebene Produkte V2                        | msdyn_sharedproductdetails                    |
| Produktmasterkonfigurationen               | msdyn_sharedproductconfigurations             |
| Produktmasterfarben                       | msdyn_sharedproductcolors                     |
| Auftragsgrundlagencodes                    | msdyn_salesorderorigins                       |
| Produktzugangskopfzeile                      | msdyn_purchaseorderreceipts                   |
| Produktzugangsposition                        | msdyn_purchaseorderreceiptproducts            |
| Bestellungskopfzeilen V2                   | msdyn_purchaseorders                          |
| Entität einer CDS-Auftragsposition vorläufig gelöscht | msdyn_purchaseorderproducts                   |
| CDS-Bestellpositionsentität              | msdyn_purchaseorderproducts                   |
| Rückverfolgungsangabengruppen                   | msdyn_producttrackingdimensiongroups          |
| Stile                                      | msdyn_productstyles                           |
| Lagerdimensionsgruppen                    | msdyn_productstoragedimensiongroups           |
| Produktspezifische Einheitenumrechnungen           | msdyn_productspecificunitofmeasureconversions |
| Standardmäßige Produktauftragseinstellungen V2           | msdyn_productspecificdefaultordersettings     |
| Größen                                       | msdyn_productsizes                            |
| Produktdimensionsgruppen                    | msdyn_productdimensiongroups                  |
| Standardauftragseinstellungen                      | msdyn_productdefaultordersettings             |
| Konfigurationen                              | msdyn_productconfigurations                   |
| Alle Produkte                                | msdyn_globalproducts                          |
| Farben                                      | msdyn_productcolors                           |
| Produktkategoriehierarchie-Rollen            | msdyn_productcategoryhierarchyrole           |
| Produktkategoriehierarchien                | msdyn_productcategoryhierarchies              |
| Produktkategoriezuweisungen                | msdyn_productcategoryassignments              |
| Produktkategorien                          | msdyn_productcategories                       |
| Lagerorte                         | msdyn_inventorylocations                      |
| CDS Bestand an                            | msdyn_inventoryonhandentries                  |
| Produktkategorien                          | msdyn_productcategories                       |
| CDS Bestand an                            | msdyn_inventoryonhandrequests                 |
| Durch Produktnummer identifizierter Strichcode           | msdyn_productbarcodes                         |
| Treuekarte                                | msdyn_loyaltycards                            |
| Treuebelohnungspunkte                       | msdyn_loyaltyrewardpoints                     |
| Preis für Debitorengruppen                       | msdyn_pricecustomergroups                     |
| Standorte                                       | msdyn_operationalsites                        |
| CDS-Verkaufsangebotspositionen                   | quotedetails                                  |
| CDS-Auftragspositionen                       | salesorderdetails                             |

**Abhängigkeitsinformationen**

Das Dual-write Supply Chain-Paket hängt von den folgenden drei Paketen ab. Daher sollten Sie diese Pakete installieren, bevor Sie das Paket Dual-write Supply Chain installieren.

- Dual-write Application Core Paket
- Dual-write Finance-Paket
- Dual-write Human Resources Paket

## <a name="dual-write-finance"></a>Dual-write Finance

Das Finance-Paket für duales Schreiben enthält die Lösungen und Zuordnungen, die für die Synchronisierung von Dynamics 365 Finance-Daten erforderlich sind. Es enthält die folgenden vier Lösungen.

| Eindeutiger Name                            | Anzeigename                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance Extended – Entitätszuordnungen |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance Extended – Anker      |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanz- und Betriebs-Apps             | Customer Engagement-Apps        |
|-----------------------------------------|---------------------------------|
| Quellensteuergruppen                  | msdyn_withholdingtaxgroups      |
| CDS Kontakte V2 (Kunde)              | Kontakte                        |
| CDS Kontakte V2 (Anbieter)                | Kontakte                        |
| Debitoren V3                            | Kontakte                        |
| Quellensteuercodes                   | msdyn_withholdingtaxcodes       |
| Kreditoren V2                              | msdyn_vendors                   |
| Kreditorzahlungsmethode                   | msdyn_vendorpaymentmethods      |
| Kreditorengruppen                           | msdyn_vendorgroups              |
| Kontenplan                       | msdyn_chartofaccountses         |
| Mehrwertsteuer-Sachkontobuchungsgruppen V2      | msdyn_taxpostinggroups          |
| Artikel-Mehrwertsteuergruppe                    | msdyn_taxitemgroups             |
| Mehrwertsteuergruppen                        | msdyn_taxgroups                 |
| Entität „Mehrwertsteuer-Befreiungscode“ in CDS        | msdyn_taxexemptcodes            |
| Debitorengruppen                         | msdyn_customergroups            |
| Zahlungsmethode für Debitoren                 | msdyn_customerpaymentmethods    |
| Finanzdimensionen                    | msdyn_dimensionattributes       |
| Mehrwertsteuer-Behörden                   | msdyn_taxauthorities            |
| Finanzdimensionsformat              | msdyn_financialdimensionformats |
| Steuerkalenderperiode                  | msdyn_fiscalcalendarperiods     |
| Entität „Steuerkalenderintegration“      | msdyn_fiscalcalendars           |
| Entität „Steuerkalender-Jahresintegration“ | msdyn_fiscalcalendaryears       |
| Zahlungsbedingungen                        | msdyn_paymentterms              |
| Zahlungsplan                        | msdyn_paymentschedules          |
| Zahlungsplanpositionen                  | msdyn_paymentschedulelines      |
| Zahlungstage CDS                        | msdyn_paymentdays               |
| Zahlungstagpositionen CDS V2                | msdyn_paymentdaylines           |
| Hauptkonto                            | msdyn_mainaccounts              |
| Hauptkontokategorien                 | msdyn_mainaccountcategories     |
| Unternehmen                                  | msdyn_ledgers                   |
| Debitoren V3                            | Konten                        |

**Abhängigkeitsinformationen**

Das Dual-write Finance-Paket hängt vom Dual-write Application Core-Paket ab. Daher sollten Sie das Dual-write Application Core Paket installieren, bevor Sie das Dual-write Finance Paket installieren.

## <a name="dual-write-notes"></a>Dual-write Notes

Das Dual-write Notes-Paket enthält die Lösungen und Zuordnungen, die für die Synchronisierung von Notiz- oder Anmerkungsdaten erforderlich sind. Es enthält die folgenden vier Lösungen.

| Eindeutiger Name                  | Anzeigename                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 Notizen erweitert    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 Notes Zuordnung von Entitäten |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 Notes Anker      |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanzen und Betrieb                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Auftragskopfdokument-Anhänge    | Anmerkungen         |
| Debitorenanhänge                       | Anmerkungen         |
| Kreditorendokumentanhänge                | Anmerkungen         |
| Anhänge des Bestellkopfdokuments | Anmerkungen         |

**Abhängigkeitsinformationen**

Das Dual-write Notes-Paket hängt von den folgenden beiden Paketen ab. Daher sollten Sie diese Pakete installieren, bevor Sie das Paket Dual-write Notes installieren.

- Dual-write Application Core Paket
- Dual-write Finance-Paket

## <a name="dual-write-asset-management"></a>Dual-write Asset-Management

Das Paket Dual-write Anlagenverwaltung enthält die Lösungen und Zuordnungen, die für die Synchronisierung von Asset-Daten aus dem Supply Chain Management oder Dynamics 365 Field Service erforderlich sind. Es enthält die folgenden vier Lösungen.

| Eindeutiger Name                          | Anzeigename                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 Asset-Management             |
| Dynamics365AssetManagementApp        | Dynamics365 Asset-Management App          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Anlagenverwaltung Zuordnung von Entitäten |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Asset-Management-Anker      |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanz- und Betriebs-Apps                           | Customer Engagement-Apps                |
|-------------------------------------------------------|-----------------------------------------|
| Anlagenverwaltungsgarantie                             | msdyn_warranties                        |
| Anlagenverwaltungsmodelle                               | msdyn_models                            |
| Anlagenverwaltungshersteller                        | msdyn_manufacturers                     |
| Anlageverwaltung und funktionale Standorttypen            | msdyn_functionallocationtypes           |
| Anlageverwaltung und funktionale Standorte                 | msdyn_functionallocations               |
| Anlagenverwaltung funktionale Standorte Lebenszyklusstatus | msdyn_functionallocationlifecyclestates |
| Anlagenverwaltung funktionale StandortevLebenszyklusmodelle | msdyn_functionallocationlifecyclemodels |
| Anlagenverwaltungs-Anlagen                               | msdyn_customerassets                    |
| Anlagenverwaltungs-Anlagentypen                          | msdyn_customerassetcategories           |
| Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusstatus               | msdyn_assetlifecyclestates              |
| Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusmodelle               | msdyn_assetlifecyclemodels              |

**Abhängigkeitsinformationen**

Das Paket Dual-write Anlagenverwaltung hängt von dem Paket Dual-write Application Core ab. Daher sollten Sie das Dual-write Application Core-Paket installieren, bevor Sie das Dual-write Anlagenverwaltung-Paket installieren.

## <a name="packages-required-for-project-operations"></a>Erforderliche Pakete für Project Operations
Project Operations hängt von den folgenden Paketen ab. Daher sollten Sie diese Pakete installieren, bevor Sie Project Operations installieren.

- Dual-write Application Core Paket
- Dual-write Finance-Paket
- Dual-write Supply Chain Paket
- Dual-write Asset-Management-Paket
- Dual-write Human Resources Paket

## <a name="dual-write-party-and-global-address-book-solutions"></a>Partei- und globale Adressbuchlösungen mit dualem Schreiben

Das Partei- und globale Adressbuchpaket mit dualem Schreiben enthält die folgenden Lösungen und Zuordnungen, die zum Synchronisieren von Party- und globalen Adressbuchdaten erforderlich sind. 

| Eindeutiger Name                       | Anzeigename                            |
|-----------------------------------|-----------------------------------------|
| Partei                             | Partei                                   |
| Dynamics365GABExtended            | Dynamics 365 – GAB, erweitert               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 – GAB, Entitätszuordnungen für duales Schreiben |
| Dynamics365GABParty_Anchor        | Dynamics 365 – GAB und Partei              |

Die folgenden Zuordnungen sind in diesem Paket enthalten.

| Finanz- und Betriebs-Apps | Customer Engagement-Apps | 
|-----------------------------|--------------------------|
| CDS-Parteien | msdyn_parties | 
| CDS Postadressorte | msdyn_postaladdresscollections | 
| CDS-Verlauf der Postanschrift V2 | msdyn_postaladdresses | 
| CDS Postadressorte der Partei | msdyn_partypostaladdresses | 
| Parteikontakte V3 | msdyn_partyelectronicaddresses | 
| Debitoren V3 | Konten | 
| Debitoren V3 | Kontakte | 
| Kreditoren V2 | msdyn_vendors | 
| Titel von Kontaktpersonen | msdyn_salescontactpersontitles | 
| Schlussformeln | msdyn_complimentaryclosings | 
| Anreden | msdyn_salutations | 
| Entscheidungsfunktionen | msdyn_decisionmakingroles | 
| Stellenfunktionen | msdyn_employmentjobfunctions | 
| Treueebenen | msdyn_loyaltylevels | 
| Arten von Persönlichkeitsmerkmalen | msdyn_personalcharactertypes | 
| Kontakte V2 | msdyn_contactforparties | 
| CDS-Verkaufsangebotskopf | Angebote | 
| Auftragskopfzeilen CDS | salesorders | 
| Verkaufsrechnungskopfzeilen V2 | Rechnungen | 
| CDS-Adressrollen | msdyn_addressroles |

**Abhängigkeitsinformationen**

Die Partei- und globale Adressbuchlösungen mit dualem Schreiben hängen von den folgenden drei Paketen ab. Daher sollten Sie diese Pakete installieren, bevor Sie das Paket „Partei- und globale Adressbuchlösungen mit dualem Schreiben“ installieren.

- Dual-write Application Core Paket
- Dual-write Finance-Paket
- Dual-write Supply Chain Paket

