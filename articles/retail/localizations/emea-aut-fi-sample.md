---
title: Beispiel der Steuerregistrierungsserviceintegration für Österreich
description: In diesem Thema erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Österreich.
author: josaw
manager: annbe
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Austria
ms.search.industry: Retail
ms.author: v-dmpere
ms.search.validFrom: 2019-3-1
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1278b9f631b61d115a092df4191c0dd7688d3df1
ms.sourcegitcommit: 70aeb93612ccd45ee88c605a1a4b87c469e3ff57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "773367"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Beispiel der Steuerregistrierungsserviceintegration für Österreich

[!include[banner](../includes/banner.md)]

Dieses Thema betrifft Dynamics 365 for Retail und Dynamics 365 for Finance and Operations. 

Die Microsoft Dynamics 365 for Retail-Funktionen für Österreich umfassen ein Beispiel der Integration von POS mit einem externen Steuerregistrierungsservice, um die lokalen steuerlichen Anforderungen von Kassen in Österreich abzudecken. Das Beispiel erweitert die [steuerliche Integrationsfunktionen](fiscal-integration-for-retail-channel.md). Es basiert auf der [EFR (Electronic Fiscal Register)](http://efsta.org/sicherheitsloesungen/)-Lösung von [EFSTA](http://efsta.org/) und ermöglicht die Kommunikation mit dem EFR-Service über das HTTPS-Protokoll. Das Beispiel wird in Form eines Quellcodes bereitgestellt und ist Teil der Retail SDK.
Microsoft liefert keine Hardware oder Software oder Dokumentation von EFSTA. Informationen dazu, wie Sie die EFR-Lösung erhalten und betreiben erhalten Sie von [EFSTA](http://efsta.org/kontakt/).

BEISPIELCODE-HINWEIS

DIESER BEISPIELCODE WIRD IM IST-ZUSTAND ZUR VERFÜGUNG GESTELLT. MICROSOFT ÜBERNIMMT KEINE GARANTIEN, WEDER AUSDRÜCKLICH NOCH ANGEDEUTET ZUR EIGNUNG FÜR EINEN BESTIMMTEN ZWECK, ZUR RICHTIGKEIT ODER VOLLSTÄNDIGKEIT VON ANTWORTEN, VON ERGEBNISSEN ODER BEDINGUNGEN DER HANDELSÜBLICHKEIT. DAS RISIKO DER VERWENDUNG ODER DER ERGEBNISSE BEI DER VERWENDUNG DIESES BEISPIELCODES LIEGT VOLLSTÄNDIG BEIM BENUTZER.
TECHNISCHER SUPPORT WIRD NICHT BEREITGESTELLT. DIESER CODE DARF NICHT WEITERGEGEBEN WERDEN, ES SEI ES DENN, ES LIEGT EIN LIZENZVERTRAG MIT MICROSOFT VOR, DER IHNEN DIES GESTATTET.

## <a name="overview"></a>Übersicht

Informationen zu allgemeinen POS-Szenarien und Funktionen, die für Debitoren in allen Ländern oder Regionen verfügbar sind, finden Sie in der [Microsoft Dynamics 365 for Retail Dokumentation](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/index).

### <a name="integration-retail-pos-with-the-efr"></a>Integration von Retail POS in das EFR

Retail enthält ein Beispiel für die Integration von POS mit spezifischem zertifizierten Steuerregistrierungsservice für Österreich. Es wird angenommen, dass der Service auf einem Computer in der Client-Infrastruktur gehostet wird und mit der POS-Hardwarestation gekoppelt ist. Das Beispiel wird als POS-Quellcode, Hardwarestation und Handelslaufzeiterweiterungen implementiert, und ist im Retail Software Development Kit (SDK) verfügbar.


### <a name="austria-specific-pos-scenarios-and-features"></a>POS-Szenarien und Funktionen spezifisch für Österreich

Die folgenden Szenarien werden im Beispiel für die Integration des Steuerregistrierungsservice für Österreich abgedeckt:
   - Registrierung der Bargeldbuchungen in der Steuerkasse (EFR):
      - Senden von detaillierten Buchungsdaten (Verkaufspositionsinformationen, Rabatte, Zahlungen, Steuern) an den Steuerregistrierungsservice;
      - Erfassen einer Antwort vom Steuerregistrierungsservice einschließlich einer digitalen Anmeldung und einem Link zur registrierten Transaktion;
      - Aufdrucken der Bonsteuergruppendaten und verweis auf die registrierte Transaktion in der Steuerregistersoftware als ein QR-Code.
  - Registrierung der Einlagen in der Steuerkasse (EFR) als eine bargeldlose Transaktion:
      - Ausstellen einer Geschenkkarte;
      - Erfassung der Debitorenkontoeinlage
      - Registrierung der Auftragseinlage.
  - Registrierung von POS-bezogenen Ereignissen oder Transaktionen bei der Steuerkasse (EFR) als eine bargeldlose Transaktion:
      - Schicht öffnen/schließen
      - Anfangsbetrag / Bareinlage / Zahlungsmittel entfernen;
      - Preisüberschreibung;
      - MwSt.-Überschreibung;
      - Bonkopie drucken;
      - Kassenlade öffnen;
      - X-Bericht drucken;
      - Z-Bericht drucken;
  - Erweiterung für Abrechnungen am Tagesende (X- und Z-Steuerberichte) durch spezifische Felder für Österreich:  
      - Gesamtanzahl der verkaufen Artikel, Produkte oder Dienstleistungen, die an den Debitor geliefert wurden;
      - Nach Steuersätzen aufgeschlüsselte Verkäufe;
      - Aufschlüsselung von Erträgen nach Kassierer-/Kassenoperator;
      - Buchungen für Buchungsstornierungen ausgeführt, Preisrabatte, Retouren, negativer Umsatz, um die tägliche Verkäufe verringert werden;
      - Nullverkäufe (Geschenke)
  - Fehlerbehebung einschließlich der folgenden Optionen:
      - Wiederholen der Steuerregistrierung, wenn möglich; z. B., wenn der Steuerregistrierungsservice nicht verfügbar ist;
      - Überspringen der Steuerregistrierung, einschließlich der Informationscodes, um den Grund des Fehlers und zusätzliche Informationen zu erfassen;
      - Integritätsprüfung des Steuerregistrierungsservice, vor der Buchung von Buchungsdaten in Dynamics 365 HQ.

## <a name="setting-up-retail-for-austria"></a>Einrichten von Retail für Österreich

In diesem Abschnitt werden die Retail-Einstellungen beschrieben, die für Österreich spezifisch und empfohlen sind. Weitere Informationen zum Einrichten von Retail finden Sie in der [Microsoft Dynamics 365 for Retail-Dokumentation](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/index).

Um die Österreich-spezifischen Retail-Funktionen zu verwenden, müssen Sie diese Aufgaben ausführen:
- Legen Sie das Feld **Land/Region** in der primären Adresse der juristischen Person auf AUT (Österreich) fest;
- Legen Sie das Feld **ISO-Code** im POS-Funktionsprofil der einzelnen Shops in Österreich auf AT (Österreich) fest.

Spezifische Einstellungen für Österreich können in zwei Gruppen eingeteilt werden:
- Allgemeine Einstellungen
- EFS-spezifische Einstellungen

### <a name="general-settings"></a>Allgemeine Einstellungen

Sie müssen die folgenden allgemeinen Einstellungen für Österreich angeben:
1. Richten Sie die folgenden Parameter für Mehrwertsteuer entsprechend der Anforderungen für Österreich ein:
    - Mehrwertsteuercodes;
    - Mehrwertsteuergruppen;
    - Artikel-Mehrwertsteuergruppen;
    - Mehrwertsteuereinstellungen in Artikeln (Artikel-Mehrwertsteuergruppen für Verkauf).

Weitere Informationen dazu, wie die Mehrwertsteuer in Microsoft Dynamics 365 for Finance and Operations und in Retail eingerichtet und verwendet wird, finden Sie unter [Mehrwertsteuerüberblick](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/general-ledger/indirect-taxes-overview).

2. Aktualisieren Sie auf der Seite **Alle Einzelhandelsgeschäfte** die Details der Einzelhandelsgeschäfte. Legen Sie genauer die folgenden Parameter fest:
    - Legen Sie im Feld **Mehrwertsteuergruppe** die Mehrwertsteuergruppe fest, die für Verkäufe an den Standardeinzelhändlerkunden verwendet werden soll.
    - Aktivieren Sie das Kontrollkästchen **Preise inkl. Mehrwertsteuer**
    - Legen Sie das Feld **Shopname** fest, damit der Unternehmensnamen enthalten ist. Durch diese Änderung wird sichergestellt, dass der Unternehmensname auf dem Verkaufsbeleg erscheint. Alternativ können Sie den Unternehmensnamen im Verkaufsbonlayout als Freiformattext hinzufügen.
    - Legen Sie das Feld **Steueridentifikationsnummer** fest, damit die Unternehmenskennnummer enthalten ist. Durch diese Änderung wird sichergestellt, dass die Identifikationsnummer auf dem Verkaufsbeleg erscheint. Alternativ können Sie die Identifikationsnummer im Verkaufsbonlayout als Freiformattext hinzufügen.

3. POS-Funktionsprofile einrichten:
    - Richten Sie im Inforegister **Bonnummerierung** die Belegnummerierung ein. 
    - Erstellen oder Aktualisieren Sie die Datensätzen für die Belegbuchungstypen **Verkauf**, **Auftrag** und **Retoure**.

4. Nehmen Sie die erforderlichen Änderungen an den **Bonlayouts** vor:
    - Ändern Sie den Wert des Felds **Druckverhalten** für das Bonlayout auf **Immer drucken**.
    - Im Bonlayoutdesigner nehmen Sie diese Änderungen vor:
        - Fügen Sie mindestens die folgenden Felder dem **Kopfzeile**-Abschnitt des Bonlayouts hinzu:
            - Ändern Sie die Felder **Shopname** und **Steueridentifikationsnummer**, sodass der Unternehmensname und die Identitätsnummer auf den Bons gedruckt werden. Alternativ können Sie den Unternehmensnamen und die Identitätsnummer im Vertriebszugangslayout als Freiformattext hinzufügen.
            - **Shopadresse**, **Datum**, **Zeit 24 h**, **Bonnummer** und **Registernummer**
    - Fügen Sie dem Abschnitt **Positionen** des Bonlayouts mindestens das folgende Feld hinzu: **Artikelname**, **Mge**, **Gesamtpreis mit Steuer**.
    - Fügen Sie mindestens die folgenden Felder dem **Fußzeile**-Abschnitt des Bonlayouts hinzu:
        - Ändern Sie Steuerfelder, damit die Bonsteuerbeträge für jeden Steuersatz gedruckt werden. Beispiel: Fügen Sie die Felder **Steuerkennung**, den **Steuersatz** und die **Steuerbeträge** einer Position des Layouts hinzu.
        - Ändern Sie die Zahlungsfelder, damit die Zahlungsbeträge für jede Zahlungsmethode gedruckt werden. Beispiel: Fügen Sie die Felder **Name des Zahlungsmittels** und **Betrag des Zahlungsmittels** einer Position des Layouts hinzu.

### <a name="efrspecific-settings"></a>EFS-spezifische Einstellungen

Bevor Sie mit der Definition EFR-spezifischer Einstellungen beginnen, achten Sie bitte darauf, dass alle Schritte der **Bereitstellungsrichtlinien für Kassen für Österreich** ausgeführt wurden.

1. Konfigurieren Sie die Mehrwertsteuersatzzuordnung: **Mehrwertsteuersatzzuordnung** ist als Teil des Steuerintegrationsbeispiels im **Funktionales Profil des Steuer-Connectors** enthalten:

    A: 20,00; B: 10,00; C: 13,00; D: 0,00; E: 19,00; F: 7,00

Überprüfen Sie die Standardzuordnungswerte und korrigieren Sie ihn falls erforderlich.

2. Richten Sie den Steuergruppencode zum Drucken auf den Bon ein: Zum Drucken des Steuergruppencodes auf dem Bon (zum Beispiel "A", "B") muss das Feld **Code drucken** für Mehrwertsteuer im Formular **Mehrwertsteuercodes** ausgefüllt werden.

3. Konfigurieren Sie benutzerdefinierte Felder, damit sie in den Bonlayouts für Verkaufsbons verwendet werden können: Sie können die Sprachtext- und benutzerdefinierte Felder konfigurieren, die in den POS-Bonlayouts verwendet werden. Das Standardunternehmen des Benutzers, der die Boneinrichtung erstellt, sollte die gleiche juristische Person sein, in dem die Sprachtexteinstellung erstellt wird. Alternativ sollten dieselben Sprachtexte im Standardunternehmen des Benutzers und in der juristischen Person des Shops verwendet werden, für den das Setup erstellt wird.

Fügen Sie auf der Seite **Sprachentext** die folgenden Datensätze für die Beschriftungen der benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass Sprach-ID, Textkennung und Textwerte, die in der Tabelle dargestellt werden, nur Beispiele sind. Sie können sie ändern, damit sie Ihre Anforderungen erfüllen. Allerdings müssen die Textkennungswerte, die Sie verwenden, eindeutig sein und größer oder gleich 900001 sein.

Fügen Sie dem Abschnitt **POS** des **Sprachentext** aus der Tabelle die folgenden POS-Beschriftungen hinzu:

| Sprachkennung | Textkennung | Text                      |
|-------------|---------|---------------------------|
| en-US       | 103174  | QR-Code                   |
| en-US       | 103175  | Forlaufende Nummer         |
| en-US       | 103176  | Einzelhandelsdruckcode für Steuer     |
| en-US       | 103177  | Gesamt (Umsatz)             |
| en-US       | 103178  | Gesamte Steuern (Umsatz)         |
| en-US       | 103179  | Gesamte enthaltene Steuern (Umsatz) |
| en-US       | 103180  | Steuerbetrag (Umsatz)        |
| en-US       | 103181  | Steuergrundlage (Umsatz)         |

Hinweis: Datensätze von **Sprachentext** müssen dem aktuellen Unternehmen und dem DAT-Unternehmen hinzugefügt werden.

Fügen Sie auf der Seite **Benutzerdefinierte Felder** die folgenden Datensätze für die benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass die Werte für **Textkennung Titel** den Werten **Textkennung** entsprechen müssen, die Sie auf der Seite **Sprachentext** angegeben haben:

| Name                 | Typ    | Textkennung Titel |
|----------------------|---------|-----------------|
| QRCODE               | Zugang | 103174          |
| CONTINUOUSNUMBER     | Zugang | 103175          |
| RETAILPRINTCODE      | Zugang | 103176          |
| SALESTOTAL           | Zugang | 103177          |
| SALESTOTALTAX        | Zugang | 103178          |
| SALESTOTALINCLUDETAX | Zugang | 103179          |
| SALESTAXAMOUNT       | Zugang | 103180          |
| SALESTAXBASIS        | Zugang | 103181          |

4. Bonformate konfigurieren

In **Designer für Bonformat** fügen Sie die folgenden benutzerdefinierten Felder den entsprechenden Bonabschnitten hinzu. Beachten Sie, dass die Feldnamen den Sprachtexten entsprechen, die Sie im vorherigen Abschnitt definiert haben.

   **Kopfzeile**: Fortlaufende Nummer. Dieses Feld zeigt die Nummer der Bargeldbuchungen in der Steuerregistrierung;
      
   **Positionen**: Einzelhandelsdruckcode für Steuer. Dieses Feld zeigt den Code entsprechend der Steuergruppe;
      
   **Fußzeile**: Feldergruppe **Gesamtzahl Verkäufe**: Summe (Umsatz) -; Gesamtbuchungsbetrag ohne Steuersumme; gesamte enthaltene Steuer (Umsatz) -; gesamter Buchungsbetrag mit Steuersumme; gesamte Steuern (Umsatz); Transaktionssteuersumme.    
      **Steueraufschlüsselung** (sollte eine separate Position sein): Besteuerungsgrundlage (Umsatz) - Gesamtbargeldbuchungsbetrag (ohne Steuern) ausgenommen Einlagen, Vorauszahlungen und Geschenkkarten; Steuerbetrag (Umsatz) - gesamter Steuerbetrag für Bargeschäfte ohne Einzahlungen, der Vorauszahlungen und Geschenkkarten; Summe enthaltener Steuer (Umsatz) - Gesamtbargeldbuchungsbetrag (mit Steuern) ausgenommen Einlagen, Vorauszahlungen und Geschenkkarten; Einzelhandelsdruckcode für Steuer - der Code entsprechend der Mehrwertsteuergruppe.        
      **QR-Code**: QR-Code - Verweis auf das registrierte Bargeschäft in Form eines QR-Codes.
      
5. Aktualisieren Sie POS-Berechtigungsgruppen und individuelle Berechtigungseinstellungen für Shoparbeitskräfte. Damit Arbeitskräfte, die der Berechtigungsgruppe zugewiesen sind, die Steuerregistrierung überspringen können, aktivieren Sie das Kontrollkästchen **Überspringen der Steuerregistrierung zulassen** (nicht empfohlen). 

### <a name="handling-gift-cards"></a>Behandeln von Geschenkkarten
Das Integrationsbeispiel des Steuerregistrierungsservice implementiert die folgenden Regeln zu Geschenkkarten:
  - Schließen Sie die Auftragspositionen, die sich auf die Vorgänge "Geschekkarte ausgeben" oder "Zu Geschenkkarte hinzufügen" aus der Registrierungsmeldung für Bargeldtransaktionen aus. Diese Vorgänge werden durch separate Meldungen als bargeldlose Vorgänge registriert.
  - Drucken Sie keine Steuergruppenaufschlüsselung und keinen QR-Code auf einen Bon, wenn er nur aus Geschenkkartenpositionen besteht.
  - Der Gesamtbetrag der ausgestellten oder aufgeladenen Geschenkkarten und ein Bargeldbuchungsbetrag werden auf dem Bon separat gedruckt.
  - Zahlung per Geschenkkarte wird als eine normale Zahlung betrachtet.

### <a name="handling-customer-deposits-and-customer-order-deposits"></a>Handhabung von Debitoreneinlagen und Debitorenauftragseinlagen
Das Integrationsbeispiel der Steuerregistrierung implementiert die folgenden Regeln in Bezug auf Debitorenkontoeinlagen und Debitorenauftragseinlagen:
  - Eine bargeldlose Transaktion wird registriert, wenn eine POS-Transaktion eine Debitoreneinlage ist.
  - Eine bargeldlose Transaktion wird registriert, wenn einer POS-Transaktion nur eine Auftragseinzahlung oder eine Auftragseinzahlungsrückerstattung enthält.
  - Drucken Sie die zuvor gezahlte Einzahlung in einem Steuerbeleg für eine Debitorenauftragsabholung.
  - Ziehen Sie den Debitorenauftragseinzahlungsbetrag von den Zahlungspositionen ab, wenn ein hybrider Kundenauftrag erstellt wird.
  - Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanal-DB mit einem Verweis auf eine Steuertransaktion für einen hybriden Auftrag.
