---
title: Entitätsabhängigkeitskette (Synchronisationsreihenfolge)
description: In diesem Thema wird die Synchronisierungsreihenfolge angegeben, die Sie beim Erstellen der anfänglichen Daten befolgen müssen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275486"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Entitätsabhängigkeitskette (Synchronisationsreihenfolge)

[!include [banner](../../includes/banner.md)]

In diesem Thema wird die Reihenfolge der Synchronisierung angegeben, die Sie zum Erstellen der Anfangsdaten befolgen müssen, wenn Sie nicht die von der Funktion **Erstsynchronisierung** bereitgestellten Entitätsabhängigkeiten verwenden. Wenn Sie **Erstsynchronisierung** nicht verwenden, müssen Sie jede Entitätszuordnung einzeln ausführen.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management-Entitäten

Zwei der folgenden Entitäten für Supply Chain Management sind in der Reihenfolge aufgeführt, in der Sie sie aktivieren müssen.

| Zuordnungsnahme auf der Seite Duales Schreiben | Name der Entitätsmetadaten in Supply Chain Management | Name der Entitätsmetadaten in Common Data Service | Notizen |
|---|---|---|---|
| Einheiten ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Einheitenumrechnungen ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Alle Produkte ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Produktdimensionsgruppen ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Lagerdimensionsgruppen ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Rückverfolgungsangabengruppen ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Farben ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Größen ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stile ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfigurationen ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Freigegebene Produkte V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service freigegebene eindeutig identifizierbare Produkte ... Produkten                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | Produkt                                      | |
| Produktnummer-Strichcode ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Standardauftragseinstellungen ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Standardmäßige Produktbestellungseinstellungen V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Produktspezifische Einheitenumrechnungen ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Sites ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Lagerhäuser ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Siehe [Hinweis 1](#scm-notes). |
| Produktmasterfarben ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Produktmastergrößen ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Produktmasterstile ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Produktmasterkonfigurationen ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Produktkategorien ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategorie                        | Siehe [Hinweis 2](#scm-notes). |
| Produktkategoriezuweisungen ... productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Produktkategoriehierarchien ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierachyEntity                   | msdyn_productcategoryhierarchy               | |
| Produktkategoriehierarchie-Rollen ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierachyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Inventargang ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Lagerhäuserzonen ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Lagerhäuserzonengruppen ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Lagerorte ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Siehe [Hinweis 3](#scm-notes). |
| Lagerortarbeitsplatz-Kopfzeile ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Lagerortarbeitslinien ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Siehe [Hinweis 4](#scm-notes). |
| Versandarten ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Lieferbedingungen ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Kundenauftragsursprungscodes ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service Kundenauftragskopfzeilen ... Kundenaufträge                             | SalesOrderHeaderCommon Data ServiceEntität              | Auftrag                                   | |
| Common Data Service Auftragspositionen ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service Verkaufsangebotskopf ... Angebote                               | SalesQuotationHeaderCommon Data ServiceEntity          | Kostenvoranschlag                                        | |
| Common Data Service Verkaufsangebotspositionen ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Verkaufsrechnungskopfzeilen V2 ... Rechnungen                                               | SalesInvoiceHeaderV2Entity                             | Rechnung                                      | |
| Verkaufsrechnungspositionen V2 ... Rechnungsdetails                                           | SalesInvoiceLineV2Entity                               | Invoicedetails                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Zuordnungs-spezifische Notizen

1. Aufgrund der Selbstabhängigkeit müssen Sie die anfängliche Synchronisierung möglicherweise zweimal ausführen.
2. Standardmäßig ist die anfängliche Synchronisierung aufgrund der Über-Untergeordneten-Beziehung deaktiviert (intelligente Bestellungen werden von der Plattform nicht verarbeitet). Daher müssen die vorhandenen Produktkategorien manuell in der richtigen Reihenfolge synchronisiert werden (z. B. durch Aktualisieren der Beschreibung der Kategorie) (zuerst Stammkategorie, dann Untergeordnete Elemente und dann die ihnen untergeordneten Elemente). Wechseln Sie zu **Produktinformationsverwaltung \> Einrichtung \> Kategorien und Attribute \> Kategoriehierarchie**. Auf der Seite **Kategoriehierarchien** können Sie jede Hierarchie auswählen und die Produktkategorien darin anzeigen.
3. Die Zuordnung von leer **ItemNumberInLocation** Nachschlagefelder und die erste, zweite und dritte zusätzliche Lagerzone führen dazu, dass die anfängliche Synchronisierung fehlschlägt. Daher werden diese Zuordnungen vorerst entfernt.
4. Die Zuordnung des leeren Felds **CaptureWeight** führt dazu, dass die anfängliche Synchronisierung fehlschlägt. Daher werden diese Zuordnungen entfernt.

### <a name="setup-related-information"></a>Zugehörige Informationen

+ Wenn Datensätze zum ersten Mal in der Entität **Produkte** in modellgesteuerten Apps in Dynamics 365 erstellt werden, haben sie den Status **Entwurf**. So ändern Sie den Status in **Aktiv**, gehen Sie zu **Einstellungen \> Verwaltung \> Systemeinstellungen \> Umsatz** in der modellgesteuerten App und stellen Sie die Option **Erstellen Sie Produkte im aktiven Zustand** auf **Ja**.
+ Wenn Sie Datensätze in der Entität **Produkte** in modellgesteuerten Apps in Dynamics 365 oder in Common Data Service erstellen, bevor Sie Duales Schreiben aktivieren, werden diese Datensätze nur aktualisiert, wenn der gesamte Schlüssel einschließlich **Unternehmen** mit den Daten in der Finance and Operations App übereinstimmt.
+ Synchronisation der **Produkte** Entität ist unidirektional, von Finance and Operations Apps zu Common Data Service. Wenn ein zugeordnetes Feld in der **Produkte** Entität in modellgesteuerten Apps in Dynamics 365 aktualisiert wird, wird das Update bei der nächsten Synchronisation von der Finance and Operations App überschrieben.

### <a name="known-issues"></a>Bekannte Probleme

- Ein Fehler tritt auf, wenn eine Einheit in einer Finance and Operations App gelöscht wird. Wenn Maßeinheiten von der Finance and Operations App zu Common Data Service synchronisiert wird, wird die erste Einheit einer bestimmten Klasse als primäre Einheit erstellt und verhindert das Löschen.

    **Minderung:** Löschen Sie zuerst die Einheit in Common Data Service. Es kann dann in der Finance and Operations App gelöscht werden.

- Ein Fehler tritt auf, wenn eine operationelle Site in einer Common Data Service App gelöscht wird. In der Fehlermeldung heißt es: Infolog: Warnung: Die primäre Adresse kann nicht gelöscht werden. Warnung: Der Entitätsdatensatz konnte nicht gelöscht werden, da die Validierung für die folgende Datenquelle fehlgeschlagen ist: InventSiteLogisticsLocation (InventSiteLogisticsLocation). Dieser Fehler wird durch ein Problem in der Datenentität in der Finance and Operations App verursacht.

    **Minderung:** Sie können die Site in der Finance and Operations App löschen. Die Seite wird dann in Common Data Service gelöscht, wenn die entsprechende Zuordnung Duales schreiben ausgeführt wird.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance-Entitäten

Die Entitäten für Dynamics 365 Finance sind in der Reihenfolge aufgeführt, in der Sie sie aktivieren müssen.

| Zuordnungsnahme auf der Seite Duales Schreiben | Name der Entitätsmetadaten in Finance | Name der Entitätsmetadaten in Common Data Service | Notizen |
|---|---|---|---|
| Währungen ... transactioncurrencies                                            | CurrencyEntity                              | Währung                                   | |
| Wechselkurstyp ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Währungspaar für Wechselkurs ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyncurrencyexchangeratepair             | |
| Common Data Service Wechselkurse ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Siehe [Hinweis 1](#fin-notes). |
| Integrationsentität Steuerkalender ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Integrationsentität Steuerkalenderjahr ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Steuerkalenderperiode ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organisationshierarchietyp ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Siehe [Hinweis 1](#fin-notes). |
| Organisationshierarchiezwecke ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Siehe [Hinweis 1](#fin-notes). |
| Juristische Personen ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Siehe [Hinweis 1](#fin-notes). |
| Juristische Personen ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Organisationseinheit ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Siehe [Hinweis 1](#fin-notes). |
| Organisationshierarchie – veröffentlicht ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Siehe [Hinweis 1](#fin-notes). |
| Namenszusätze ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffixe                            | |
| Zahlungstage Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Zahlungstagpositionen Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Zahlungsplan ... msdyn_paymentschedule                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Zahlungsplanpositionen ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Zahlungsbedingungen ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Zahlungsmethode für Debitoren ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Kreditorenzahlungsmethode ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Debitorengruppen ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Kreditorengruppen ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Mehrwertsteuergruppen ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Artikel-Mehrwertsteuergruppen ... msdyn_taxgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Mehrwertsteuer-Sachkontobuchungsgruppen V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Entität Mehrwertsteuer-Befreiungscode Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Mehrwertsteuer-Behörden ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Mehrwertsteuercodes ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Siehe [Hinweis 1](#fin-notes). |
| Finanzdimensionsformat ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Finanzdimensionen ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Quellensteuergruppen ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Quellensteuercodes ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Kontenplan ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Sachkonto ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Siehe [Hinweis 1](#fin-notes). |
| Hauptkontokategorien ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Hauptkonto ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Debitoren V3 ... Konten                                                       | CustCustomerV3Entity                        | Konto                                    | Siehe [Hinweis 2](#fin-notes). |
| Debitoren V3 ... Kontakten                                                       | CustCustomerV3Entity                        | Kontakt                                    | Siehe [Hinweis 3](#fin-notes). |
| Kreditoren V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Siehe [Hinweis 2](#fin-notes). |
| Common Data Service Kontakte V2 ... Kontakten                                    | smmContactPersonCommon Data ServiceV2Entity | Kontakt                                    | Siehe [Hinweis 4](#fin-notes). |
| Common Data Service Kontakte V2 ... Kontakten                                    | smmContactPersonCommon Data ServiceV2Entity | Kontakt                                    | Siehe [Hinweis 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Zuordnungs-spezifische Notizen

1. Einweg-Synchronisation erfolgt ab Finance and Operations Apps zu Common Data Service.
2. Aufgrund der Selbstabhängigkeit müssen Sie die anfängliche Synchronisierung möglicherweise mehr als einmal ausführen. Stellen Sie sicher, dass Sie **Kunde** als Beziehungstyp auswählen, wenn Sie ein Konto mit der Seite **Konten** in Common Data Service erstellen. Wenn Sie Probleme mit dem Feld **Hauptansprechpartner** während der anfänglichen Synchronisierung haben, entfernen Sie aus der Zuordnung das Feld und führen Sie die anfängliche Synchronisierung erneut aus. Beenden Sie nach erfolgreichem Abschluss der ersten Synchronisierung die Zuordnung und fügen Sie das Feld **Hauptansprechpartner** wieder dazu. Starten Sie dann die Zuordnung, überspringen Sie jedoch die anfängliche Synchronisation. Der Wert des Felds **Hauptansprechpartner** wird bei der anfänglichen Synchronisierung nicht berücksichtigt, und Sie müssen die Werte manuell migrieren.
3. Stellen Sie sicher, dass die Oprion **Verkaufbar** auf **Ja** auf der Seite **Kontakte** in Common Data Service gesetzt ist, wenn Sie versuchen, einen Kunden der Art **Person** zu erstellen.
4. Diese Zuordnung verfügt auf beiden Seiten über einen Filter zum Verknüpfen von Kundenkontakten. Öffnen Sie die Zuordnungs-Details und wählen Sie die Filter-Schaltfläche (Trichtersymbol) neben dem **Sales.Contact** Entitätsname, und stellen Sie sicher, dass die Dateikriterien **msdyn_contactforvendor eq true und msdyn_sellable eq false** enthalten sind.
5. Diese Zuordnung verfügt auf beiden Seiten über einen Filter zum Verknüpfen von Lieferantenkontakten. Öffnen Sie die Zuordnungs-Details und wählen Sie die Filter-Schaltfläche (Trichtersymbol) neben dem **Sales.Contact** Entitätsnamen und stellen Sie sicher, dass die Dateikriterien **msdyn_contactforvendor eq true und msdyn_sellable eq false** enthalten sind. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources-Entitäten

Die Entitäten für Dynamics 365 Human Resources sind in der Reihenfolge aufgeführt, in der Sie sie aktivieren müssen.

| Zuordnungsnahme auf der Seite Duales Schreiben | Name der Entitätsmetadaten in der Personalabteilung | Name der Entitätsmetadaten in Common Data Service | Notizen |
|---|---|---|---|
| cdm_jobfunction – Stellenfunktion                                |                                   | cdm_jobfunction                  | |
| cdm_Jobtypes – Stellentypen                                      |                                   | cdm_jobtypes                     | |
| cdm_Jobs – Jobs                                               |                                   | cdm_jobs                         | |
| cdm_Jobs – Stellendetails                                        |                                   | cdm_jobs                         | |
| cdm_positiontype – PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Grundposition                              | HcmPositionBaseEntity             | cdm_jobposition                  | Siehe [Hinweis 1](#hr-notes). |
| cdm_jobposition - Stellendetails                            | HcmPositionDetailEntity           | cdm_jobposition                  | Siehe [Hinweis 1](#hr-notes). |
| cdm_jobposition - Stellendauer                           | HcmPositionDurationEntity         | cdm_jobposition                  | Siehe [Hinweis 1](#hr-notes). |
| cdm_jobposition - Stellenhierarchien                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Siehe [Hinweis 1](#hr-notes). |
| cdm_veteranstatus – Veteranenstatus                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin – Ethnische Herkunft                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode – Sprachcode                              |                                   | cdm_languagecode                 | |
| cdm_worker – Arbeitskraft                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Beschäftigungen                                 |                                   | cdm_employments                  | |
| cdm_employments - Beschäftigungsdetail                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Position Arbeitskraftzuweisung | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Siehe [Hinweis 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Zuordnungs-spezifische Notizen

1. Eine Entität Common Data Service ist mehreren Finance and Operations App-Entitäten zugeordnet.
2. Diese Zuordnung hat eine Selbstreferenz.

## <a name="asset-management-entities"></a>Anlagenverwaltungsentitäten

Zwei der folgenden Entitäten für die Anlageverwaltung für Dynamics 365 Supply Chain Management sind in der Reihenfolge aufgeführt, in der Sie sie aktivieren müssen.

| Zuordnungsnahme auf der Seite Duales Schreiben | Name der Entitätsmetadaten in der Anlagenverwaltung | Name der Entitätsmetadaten in Common Data Service | Notizen |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusstatus               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusmodelle               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Anlagenverwaltung funktionale StandortevLebenszyklusmodelle | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Anlagenverwaltung funktionale Standorte Lebenszyklusstatus | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Anlagenverwaltungs-Anlagentypen                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Anlageverwaltung und funktionale Standorttypen            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Anlageverwaltung und funktionale Standorte                 | msdyn_functionallocations                | [die Notiz](#am-notes) ansehen. |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Anlagenverwaltungs-Anlagen                               | msdyn_customerassets                     | [die Notiz](#am-notes) ansehen. |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Anlagenverwaltungshersteller                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Anlagenverwaltungsmodelle                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Anlagenverwaltungsgarantie                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Zuordnungs-spezifische Notizen

- Aufgrund der Selbstabhängigkeit müssen Sie die anfängliche Synchronisierung möglicherweise mehr als einmal ausführen.
