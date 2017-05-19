---
title: Deutsche Protokolldatei (GDPdU/GoBD)
description: "Unternehmen in Deutschland und in einigen anderen Ländern/Regionen sind gesetzlich verpflichtet, einen Export von Finanzdaten in einer maschinenlesbaren Form bereitzustellen. In diesem Artikel wird beschrieben, wie die aktuelle Version von Microsoft Dynamics 365 for Operations Anforderungen für die GDPdU/GoBD-Protokolldatei unterstützt. Er enthält außerdem Tabellen, die als Beispiele in elektronischen Berichterstellungskonfigurationen eingerichtet wurden."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59201
ms.assetid: 0f885fd8-5425-48df-bc4d-a83c3789dd59
ms.search.region: Austria, Germany
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a221664d23bbbc95caf6ffd306ab675b70e80df4
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="german-audit-file-gdpdugobd"></a>Deutsche Protokolldatei (GDPdU/GoBD)

[!include[banner](../includes/banner.md)]


Unternehmen in Deutschland und in einigen anderen Ländern/Regionen sind gesetzlich verpflichtet, einen Export von Finanzdaten in einer maschinenlesbaren Form bereitzustellen. In diesem Artikel wird beschrieben, wie die aktuelle Version von Microsoft Dynamics 365 for Operations Anforderungen für die GDPdU/GoBD-Protokolldatei unterstützt. Er enthält außerdem Tabellen, die als Beispiele in elektronischen Berichterstellungskonfigurationen eingerichtet wurden.

Unternehmen in Deutschland und in einigen anderen Ländern/Regionen sind gesetzlich verpflichtet, Daten für alle Buchungen und Masterdaten aus einem Geschäftsjahr zu exportieren und diese Daten den Wirtschaftsprüfern innerhalb eines angemessenen Zeitraums bereitzustellen. Die Daten müssen in einem bestimmten Dateiformat gesammelt werden, damit sie in die Auditumgebung des Wirtschaftsprüfers importiert werden können. Diese Vorgehensweise wird von den Steuerbehörden gesteuert. Die Daten, die exportiert werden müssen, hängen von den Anforderungen für ein Audit ab. Zum Beispiel umfasst ein typischer Satz an exportierten Daten die folgenden Masterdaten und Buchungstabellen:

-   Hauptkonten
-   Sachkontobuchungen
-   Steuercodes
-   Steuerbuchungen
-   Kundenmasterdaten
-   Debitorenbuchungen
-   Kreditorenmasterdaten
-   Kreditorenbuchungen
-   Artikelmasterdaten
-   Artikelbuchungen
-   Anlagenmasterdaten
-   Anlagenbuchungen

In der aktuellen Version von Microsoft Dynamics 365 for Operations werden Funktionen, die dem Benutzer das Exportieren der erforderlichen Daten ermöglichen, als GDPdU-spezifische elektronische Berichterstellungskonfigurationen implementiert. Aufgabenleitfäden, die zeigen, wie GDPdU-spezifische Konfigurationen importiert werden, eine andere Tabellengruppe für den Export hinzugefügt wird und der Export ausführt wird, sind ebenfalls verfügbar.

## <a name="table-groups-and-table-definitions"></a>Tabellengruppen und Tabellendefinitionen
In den folgenden Abschnitten werden die Tabellen aufgelistet, die als Beispiele in der elektronischen GDPdU-Datenmodellkonfiguration eingerichtet sind. Sie können diese Tabellen standardmäßig verwenden, um die Daten zu exportieren. Sie können auch vorhandene Tabellengruppen anpassen und die Liste der unterstützten Tabellengruppen in der Konfiguration des elektronischen GDPdU-Berichterstellungsdatenmodells erweitern.

### <a name="general-ledger"></a>Hauptbuch

In den folgenden Tabellen werden die allgemeinen Sachdatenstrukturdefinitionen angezeigt.

#### <a name="sachkonten"></a>Sachkonten

|     | Feldname                  | Feldtyp | Beschreibung                                      | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|---------------------------|---------|---------------------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | SACHKONTONUMMER           | Zeichen | Nummer des Sachkontos                             | MainAccount                          | MainAccountId                                  |
| 2   | SACHKONTONAME             | Zeichen | Bezeichnung des Sachkontos                        | MainAccount                          | Name                                           |
| 3   | SACHKONTOTYP              | Zeichen | Typ des Sachkontos                                | MainAccount                          | Typ                                           |
| 4   | SACHKONTOSPERRE           | Zeichen | Gesperrt für manuelle Buchungen                   | MainAccount                          | isBlockedForManualEntry()                      |
| 5   | SACHKONTOEXCLUSIVBENUTZER | Zeichen | Exklusiver Benutzer dieses Sachkontos             | MainAccount                          | UserInfoId                                     |
| 6   | SACHKONTOBENUTZUNG        | Zeichen | Einstellung für einzelnen Benutzer des Sachkontos | MainAccount                          | ValidateUser                                   |
| 7   | KONTENART                 | Zeichen | Kontenart                                         | MainAccount                          | Typ                                           |

#### <a name="sachkontobuchungen"></a>Sachkontobuchungen

|     | Feldname               | Feldtyp   | Beschreibung                                      | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|------------------------|-----------|---------------------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | SACHKONTONUMMER        | Zeichen   | Nummer des Sachkontos                             | DiensionAttributeValueCombination    | DisplayValue                                   |
| 2   | BUCHUNGSDATUM          | Datum     | Datum der Wertstellung                            | GeneralJournalEntry                  | AccountingDate                                 |
| 3   | BUCHUNGSNUMMER         | Zeichen   | Interne Belegnummer der Buchung                   | GeneralJournalEntry                  | SubledgerVoucher                               |
| 4   | BUCHUNGSTEXT           | Zeichen   | Text der Buchung                                  | GeneralJournalAccountEntry           | Text                                           |
| 5   | BUCHUNGSBETRAG         | Num(2Dez) | Betrag der Buchung in Buchungswährung             | GeneralJournalAccountEntry           | TransactionCurrencyAmount                      |
| 6   | BUCHUNGSWAHRUNG        | Zeichen   | Währung der Buchung                               | GeneralJournalAccountEntry           | TransactionCurrencyCode                        |
| 7   | BUCHUNGSWERT           | Num(2Dez) | Wert der Buchung in Firmenwährung                 | GeneralJournalAccountEntry           | AccountingCurrencyAmount                       |
| 8   | BELEGDATUM             | Datum     | Datum des Belegs                                  | GeneralJournalEntry                  | DocumentDate                                   |
| 9   | BELEGNUMMER            | Zeichen   | Externe Belegnummer der Buchung                   | GeneralJournalEntry                  | DocumentNumber                                 |
| 10  | SPEZIALBUCHUNG         | Zeichen   | 0-Steuerbil.; andere Buchungsebene: int. Buchung  | GeneralJournalEntry                  | PostingLayer                                   |
| 11  | STEUERBUCHUNGSREFERENZ | Numerisch | Gibt es hierzu eine Mehrwertsteuerbuchung?-lfd Nr | GeneralJournalAccountEntry           | displaySalesTaxTransId()                       |
| 12  | PERIODENZUGEHORIGKEIT  | Zeichen   | Vortrag, Normal oder Abschlussbuchung             | FiscalCalendarPeriod                 | Typ                                           |
| 13  | ERFASSUNGSNUMMER       | Zeichen   | Nummer der Erfassung                              | LedgerEntryJournalizing              | Erfassung                                        |
| 14  | JOURNALZEILE           | Numerisch | Zeile des Journals                                | LedgerEntryJournalizing              | SequenceNumber                                 |
| 15  | GEGENKONTO             | Zeichen   | Nummer des Gegenkontos                            | GeneralJournalAccountEntry           | RecId                                          |
| 16  | BUCHUNGSTYP            | Zeichen   | Buchungstyp                                       | GeneralJournalAccountEntry           | PostingType                                    |
| 17  | KORREKTUR              | Zeichen   | Korrektur                                         | GeneralJournalAccountEntry           | IsCorrection                                   |
| 18  | HABENBUCHUNG           | Zeichen   | Habenbuchung                                      | GeneralJournalAccountEntry           | IsCredit                                       |
| 19  | PERIODENCODE           | Zeichen   | Periodencode                                      | FiscalCalendarPeriod                 | Typ                                           |
| 20  | DOKUMENT               | Zeichen   | Dokument                                          | GeneralJournalEntry                  | DocumentNumber                                 |

### <a name="tax-ledger"></a>Steuersachkonto

In den folgenden Tabellen werden die allgemeinen Steuerdatenstrukturdefinitionen angezeigt.

#### <a name="umsatzsteuercodes"></a>Umsatzsteuercodes

|     | Feldname          | Feldtyp   | Beschreibung      | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|-------------------|-----------|-------------------|--------------------------------------|------------------------------------------------|
| 1   | NAME              | Zeichen   | Name              | TaxTable                             | TaxName                                        |
| 2   | BUCHUNGSGRUNDLAGE | Zeichen   | Buchungsgrundlage | TaxTable                             | TaxBase                                        |
| 3   | PROZENTSATZ       | Num(2Dez) | Prozentsatz       | TaxData                              | TaxValue                                       |
| 4   | GULTIGAB          | Datum     | Gültig ab         | TaxData                              | TaxFromDate                                    |
| 5   | GULTIGBIS         | Datum     | Gültig bis        | TaxData                              | TaxToDate                                      |

#### <a name="mehrwertsteuergruppen"></a>MehrwertsteuerGruppen

|     | Feldname                      | Feldtyp | Beschreibung               | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|-------------------------------|---------|----------------------------|--------------------------------------|------------------------------------------------|
| 1   | MEHRWERTSTEUERGRUPPE          | Zeichen | Mehrwertsteuergruppe       | TaxGroupData                         | TaxGroup                                       |
| 2   | BESCHREIBUNG                  | Zeichen | Beschreibung               | TaxGroupHeading                      | TaxGroupName                                   |
| 3   | MWST\_AUF\_SKONTO\_STORNIEREN | Zeichen | MWSt auf Skonto stornieren | TaxGroupHeading                      | TaxReverseOnCashDisc                           |
| 4   | MEHRWERTSTEUERCODE            | Zeichen | Mehrwertsteuercode         | TaxGroupData                         | TaxCode                                        |
| 5   | MWST\_CODE\_NAME              | Zeichen | MWSt Code Name             | TaxTable                             | TaxName                                        |
| 6   | ERWERBSSTEUER                 | Zeichen | Erwerbssteuer              | TaxGroupData                         | UseTax                                         |

#### <a name="umsatzsteuerbuchungen"></a>Umsatzsteuerbuchungen

|     | Feldname               | Feldtyp   | Beschreibung                                | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|------------------------|-----------|---------------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | STEUERART              | Zeichen   | Beschreibung der Steuerart                  | TaxTrans                             | TaxName()                                      |
| 2   | CODE\_ MWST             | Zeichen   | MWST Bezeichung                             | TaxTrans                             | TaxCode                                        |
| 3   | WERTSTELLUNG           | Datum     | Datum der Wertstellung der Buchung          | TaxTrans                             | TransDate                                      |
| 4   | BELEGNUMMER            | Zeichen   | Interne Nummer des Buchungsbelegs           | TaxTrans                             | Beleg                                        |
| 5   | BUCHUNGSWAHRUNG        | Zeichen   | Währung der Buchung                         | TaxTrans                             | CurrencyCode                                   |
| 6   | BUCHUNGSBETRAG         | Num(2Dez) | Betrag der Buchung                          | TaxTrans                             | TaxAmountCur                                   |
| 7   | BUCHUNGSWERT           | Num(2Dez) | Wert der Buchung in Firmenwährung           | TaxTrans                             | TaxAmount                                      |
| 8   | STEUERBUCHUNGSREFERENZ | Numerisch | Gibt es hierzu eine MWST-Buchung? - lfd Nr. | TaxTrans                             | RecId                                          |
| 9   | QUELLE                 | Zeichen   | Quelle                                      | TaxTrans                             | Grundlage                                         |
| 10  | BUCHUNGSGRUNDLAGE      | Zeichen   | Buchungsgrundlage                           | TaxTrans                             | TaxDirection                                   |
| 11  | MEHRWERTSTEUERART      | Zeichen   | Mehrwertsteuerart                           | Nicht zutreffend                       | Nicht zutreffend                                 |
| 12  | BELEGWAHRUNG           | Zeichen   | Belegwährung                                | TaxTrans                             | SourceCurrencyCode                             |
| 13  | GRUNDLAGE              | Num(2Dez) | Grundlage                                   | TaxTrans                             | SourceBaseAmountCur                            |
| 14  | PROZENTSATZ            | Num(2Dez) | Prozentsatz                                 | TaxTrans                             | TaxValue                                       |
| 15  | MWST\_GRUPPE           | Zeichen   | MwSt Gruppe                                 | TaxTrans                             | TaxGroup                                       |
| 16  | KONTO\_MWST\_AUSGABEN  | Zeichen   | Konto MwSt Ausgaben                         | TaxTrans                             | mainAccountTaxRef ()                           |
| 17  | SACHKONTO              | Zeichen   | Sachkonto                                   | TaxTrans                             | mainAccountOperation()                         |
| 18  | ARTIKEL\_MWST\_GRUPPE  | Zeichen   | Artikel-Mehrwertsteuergruppe                | TaxTrans                             | TaxItemGroup                                   |

### <a name="accounts-receivable"></a>Debitoren

In den folgenden Tabellen werden die allgemeinen Debitorendatenstrukturdefinitionen angezeigt.

#### <a name="kunden"></a>Kunden

|     | Feldname             | Feldtyp | Beschreibung                          | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|----------------------|---------|---------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | KUNDENKONTONUMMER    | Zeichen | Nummer des Kundenkontos               | CustTable                            | AccountNum                                     |
| 2   | KUNDENNAME           | Zeichen | Name des Kunden                       | DirPartyTable                        | Name                                           |
| 3   | KUNDENSTRASSE        | Zeichen | Straße des Kunden                     | LogisticsPostalAddress               | Straße                                         |
| 4   | KUNDENPLZ            | Zeichen | Postleitzahl des Kunden               | LogisticsPostalAddress               | ZipCode                                        |
| 5   | KUNDENORT            | Zeichen | Ort des Kunden                        | LogisticsPostalAddress               | Ort                                           |
| 6   | KUNDENSTAAT          | Zeichen | Staat des Kunden                      | LogisticsPostalAddress               | CountryRegionId                                |
| 7   | KUNDENGRUPPE         | Zeichen | Gruppe, der der Kunde zugeordnet ist  | CustTable                            | CustGroup                                      |
| 8   | KUNDENUSTIDNR        | Zeichen | USt-IdNr des Kunden                   | CustTable                            | VATNum                                         |
| 9   | KUNDENEIGENEKONTONR  | Zeichen | Eigene Kontonummer beim Kunden        | CustTable                            | OurAccountNum                                  |
| 10  | KUNDENLIEFERANTENNR  | Zeichen | Lieferantenkonto bei uns              | CustTable                            | VendAccount                                    |
| 11  | KUNDENRECHNUNGSKONTO | Zeichen | Kundenkonto für Rechnungen            | CustTable                            | InvoiceAccount                                 |
| 12  | MWST\_GRUPPE         | Zeichen | MWSt Gruppe - Inland / EU / Drittland | CustTable                            | TaxGroup                                       |
| 13  | WÄHRUNG              | Zeichen | Währung                               | CustTable                            | Währung                                       |

#### <a name="kundenbuchungen"></a>Kundenbuchungen

|     | Feldname                 | Feldtyp   | Beschreibung                          | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|--------------------------|-----------|---------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | KUNDENKONTONUMMER        | Zeichen   | Kontonummer des Kundenkontos          | CustTrans                            | AccountNum                                     |
| 2   | BUCHUNGSNUMMER           | Zeichen   | Interne Belegnummer der Buchung       | CustTrans                            | Beleg                                        |
| 3   | BUCHUNGSDATUM            | Datum     | Wertstellung der Buchung              | CustTrans                            | TransDate                                      |
| 4   | BELEGNUMMER              | Zeichen   | Externe Belegnummer der Buchung       | CustTrans                            | DocumentNum                                    |
| 5   | BELEGDATUM               | Datum     | Datum des externen Belegs             | CustTrans                            | DocumentDate                                   |
| 6   | BUCHUNGSTEXT             | Zeichen   | Buchungstext der Buchung              | CustTrans                            | Txt                                            |
| 7   | BUCHUNGSBETRAG           | Num(2Dez) | Betrag der Buchung in Buchungswährung | CustTrans                            | AmountCur                                      |
| 8   | BUCHUNGSWAHRUNG          | Zeichen   | Währung der Buchung                   | CustTrans                            | CurrencyCode                                   |
| 9   | BUCHUNGSWERT             | Num(2Dez) | Wert der Buchung in Firmenwährung     | CustTrans                            | AmountMST                                      |
| 10  | LETZTER\_AUSGLEICHSBELEG | Zeichen   | Letzter Ausgleichsbeleg               | CustTrans                            | LastSettleVoucher                              |
| 11  | LETZTER\_AUSGLEICH       | Datum     | Letzter Ausgleich                     | CustTrans                            | LastSettleDate                                 |
| 12  | BUCHUNGSART              | Zeichen   | Buchungsart                           | CustTrans                            | TransType                                      |

### <a name="accounts-payable"></a>Kreditorenkonten

In den folgenden Tabellen werden die allgemeinen Kreditorendatenstrukturdefinitionen angezeigt.

#### <a name="lieferanten"></a>Lieferanten

|     | Feldname                  | Feldtyp | Beschreibung                             | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|---------------------------|---------|------------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | LIEFERANTENKONTONUMMER    | Zeichen | Nummer des Lieferantenkontos             | VendTable                            | AccountNum                                     |
| 2   | LIEFERANTENNAME           | Zeichen | Name des Lieferanten                     | DirPartyTable                        | Name                                           |
| 3   | LIEFERANTENSTRASSE        | Zeichen | Straße des Lieferanten                   | LogisticsPostalAddress               | Straße                                         |
| 4   | LIEFERANTENPLZ            | Zeichen | Postleitzahl des Lieferanten             | LogisticsPostalAddress               | ZipCode                                        |
| 5   | LIEFERANTENORT            | Zeichen | Ort des Lieferanten                      | LogisticsPostalAddress               | Ort                                           |
| 6   | LIEFERANTENSTAAT          | Zeichen | Staat des Lieferanten                    | LogisticsPostalAddress               | CountryRegionId                                |
| 7   | LIEFERANTENGRUPPE         | Zeichen | Gruppe, der der Lieferant zugeordnet ist | VendTable                            | VendGroup                                      |
| 8   | LIEFERANTENUSTIDNR        | Zeichen | USt-IdNr des Lieferanten                 | VendTable                            | VATNum                                         |
| 9   | LIEFERANTENKUNDENKONTO    | Zeichen | Kundenkonto des Lieferanten bei uns      | Nicht zutreffend                       | Nicht zutreffend                                 |
| 10  | LIEFERANTENRECHNUNGSKONTO | Zeichen | Lieferantenkonto für Rechnungsstellung   | VendTable                            | InvoiceAccount                                 |
| 11  | MWST\_GRUPPE              | Zeichen | MWSt Gruppe - Inland / EU / Drittland    | VendTable                            | TaxGroup                                       |
| 12  | WAHRUNG                   | Zeichen | Währung                                  | VendTable                            | Währung                                       |

#### <a name="lieferantenbuchungen"></a>Lieferantenbuchungen

|     | Feldname                 | Feldtyp   | Beschreibung                          | Tabellen in Dynamics 365 for Operations | Feld oder Methode in Dynamics 365 for Operations |
|-----|--------------------------|-----------|---------------------------------------|--------------------------------------|------------------------------------------------|
| 1   | LIEFERANTENKONTONUMMER   | Zeichen   | Nummer des Lieferantenkontos          | VendTrans                            | AccountNum                                     |
| 2   | BUCHUNGSNUMMER           | Zeichen   | Interne Belegnummer der Buchung       | VendTrans                            | Beleg                                        |
| 3   | BUCHUNGSDATUM            | Datum     | Wertstellung der Buchung              | VendTrans                            | TransDate                                      |
| 4   | BELEGNUMMER              | Zeichen   | Externe Belegnummer der Buchung       | VendTrans                            | DocumentNum                                    |
| 5   | BELEGDATUM               | Datum     | Datum des externen Belegs             | VendTrans                            | DocumentDate                                   |
| 6   | BUCHUNGSTEXT             | Zeichen   | Buchungstext der Buchung              | VendTrans                            | Txt                                            |
| 7   | BUCHUNGSBETRAG           | Num(2Dez) | Betrag der Buchung in Buchungswährung | VendTrans                            | AmountCur                                      |
| 8   | BUCHUNGSWAHRUNG          | Zeichen   | Währung der Buchung                   | VendTrans                            | CurrencyCode                                   |
| 9   | BUCHUNGSWERT             | Num(2Dez) | Wert der Buchung in Firmenwährung     | VendTrans                            | AmountMST                                      |
| 10  | LETZTER\_AUSGLEICHSBELEG | Zeichen   | Letzter Ausgleichsbeleg               | VendTrans                            | LastSettleVoucher                              |
| 11  | LETZTER\_AUSGLEICH       | Datum     | Letzter Ausgleich                     | VendTrans                            | LastSettleDate                                 |
| 12  | BUCHUNGSART              | Zeichen   | Buchungsart                           | VendTrans                            | TransType                                      |
| 13  | STATUS                   | Zeichen   | Status                                | VendTrans                            | Genehmigt                                       |



<a name="see-also"></a>Siehe auch
--------

[Überblick über die elektronische Berichterstellung](/dynamics365/operations/dev-itpro/analytics/general-electronic-reporting)




