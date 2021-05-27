---
title: Integrationsbeispiel für Steuererfassungsdienst für Deutschland
description: In diesem Thema erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Deutschland.
author: josaw
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Germany
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e3ce5bca45e9439983c8db3c2c332fea317bd055
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020297"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Integrationsbeispiel für Steuererfassungsdienst für Deutschland

[!include[banner](../includes/banner.md)]

## <a name="introduction"></a>Einführung

Um die lokalen fiskalischen Anforderungen für Registrierkassen in Deutschland zu erfüllen, enthält die Microsoft Dynamics 365 Commerce-Funktionalität für Deutschland eine Beispielintegration der Kasse mit einem externen fiskalischen Registrierungsdienst. Das Beispiel erweitert die [steuerliche Integrationsfunktionen](fiscal-integration-for-retail-channel.md). Es basiert auf der [EFR (Electronisches Fiskalregister)](https://www.efsta.eu/de/fiskalloesungen/deutschland)-Lösung von [EFSTA](https://www.efsta.eu/de/) und ermöglicht die Kommunikation mit dem EFR-Service über das HTTPS-Protokoll. Der EFR-Dienst sollte entweder in der Retail Hardware station oder auf einem separaten Computer gehostet werden, zu dem von der Hardarestation aus eine Verbindung hergestellt werden kann. Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Retail Software Development Kit (SDK).

Microsoft gibt keine Hardware, Software oder Dokumentation von EFSTA aus frei. Um Informationen darüber zu erhalten, wie Sie die EFR-Lösung beziehen und betreiben, wenden Sie sich an [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Szenarien

Die folgenden Szenarien werden im Beispiel für die Integration des Steuerregistrierungsservice für Deutschland abgedeckt:

### <a name="sales-operations"></a>Verkaufsvorgänge

- **Registrierung von Cash-and-Carry-Verkäufen und -Rückgaben im Steuerregistrierungsdienst:**

Die Registrierung von Verkaufsvorgängen umfasst die folgenden Schritte:

  1. Erfassung des Startdatums

Der Start jeder Transaktion wird in einem technischen Sicherheitselement (TSE) registriert, das mit dem EFR-Dienst verbunden ist. Als Ergebnis der Registrierung weist eine TSE eine Transaktions-ID (TID) zu.

  2. Erfassung des Enddatums

Wenn eine Transaktion am POS abgeschlossen wird, wird sie mit derselben TID registriert, die bei der Registrierung des Transaktionsstarts zugewiesen wurde. Zu diesem Zeitpunkt werden detaillierte Buchungsdaten dem Steuererfassungsdienst zugestellt. Diese Daten beinhalten Informationen zu Verkaufspositionen sowie Informationen über Rabatte, Zahlungen und Steuern.

  3. Erfassen einer Antwort vom Steuererfassungsdienst

Sicherheitsdaten werden von einer TSE als Teil einer Antwort empfangen und in der Transaktion in der Kanaldatenbank gespeichert. Die Sicherheitsdaten bestehen aus folgenden Informationen: – TID – Datum und Uhrzeit des Transaktionsstarts – Datum und Uhrzeit des Transaktionsendes – Signaturzähler – Prüfwert – Seriennummer des TSE

- **Registrierung von Kundenbestellungen im Steuerregistrierungsdienst:** Der Registrierungsprozess ist der gleiche wie der Prozess für Cash-and-Carry-Verkäufe und -Rückgaben.
- **Registrierung von Vorgängen im Zusammenhang mit Geschenkkarten und Einzahlungen** Der Registrierungsprozess ist der gleiche wie der Prozess für Cash-and-Carry-Verkäufe und -Rückgaben.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Benachrichtigen von Benutzern über Fehler bei der Steuerregistrierung

Es gibt zwei Möglichkeiten, wie der Steuerregistrierungsdienst Benutzer über Fehler informieren kann, die während der Steuerregistrierung aufgetreten sind:

- Drucken Sie zusätzliche Informationen aus der Antwort im Feld **Info Nachricht** auf Quittungen.
- Benachrichtigungen des Finanzdienstes als Benutzernachrichten am POS anzeigen.

    > [!NOTE]
    > Dieser Benachrichtigungsmechanismus erfordert, dass die **Steuerregistrierungsbenachrichtigungen anzeigen** Parameter auf der Seite **Technische Profile der Steckverbinder** eingeschaltet werden.

#### <a name="printing-receipts"></a>Quittungen werden gedruckt

Der Belegdruck ist in Deutschland obligatorisch. Alle Belege müssen mindestens folgende Angaben enthalten:

- Name und Anschrift des Unternehmens
- Informationen über Waren, einschließlich deren Preise und Mengen
- Informationen zu eingegangenen Zahlungen
- Informationen zu Steuern, einschließlich Gesamtbeträgen pro Steuersatz
- Datensicherheit:

    - TID
    - Das Datum und die Zeit des Transaktionsstarts
    - Das Datum und die Zeit des Transaktionsende
    - Signaturzähler
    - Wert prüfen
    - Seriennummer der TSE

- Informationsnachricht

> [!NOTE]
> Ein QR-Code kann auch auf Quittungen gedruckt werden. Obwohl der QR-Code optional ist, wird er dringend empfohlen. Weitere Informationen dazu, wie Sie QR-Code als Teil einer Antwort vom Steuerregistrierungsdienst erhalten, finden Sie im „EFR-Handbuch \[DE\]“-Dokument, das auf der Website [EFSTA-Dokumentation](https://public.efsta.net/efr/) veröffentlicht wird.
>
> Das Feld **Info Nachricht** auf den Belegen zeigt eine Benachrichtigung des Steuerregistrierungsdienstes. Wenn beispielsweise ein Signaturgerät defekt ist, kann ein spezieller Text auf eine Quittung gedruckt werden.

#### <a name="voided-suspended-and-recalled-transactions"></a>Stornierte, suspendierte und zurückgerufene Transaktionen

- Eine stornierte Transaktion wird als Anforderung zum Beenden einer Transaktion im Steuerregistrierungsdienst registriert.
- Eine stornierte Transaktion wird als Anforderung zum Beenden einer Transaktion im Steuerregistrierungsdienst registriert.
- Eine stornierte Transaktion wird als Anforderung zum Beginn einer Transaktion im Steuerregistrierungsdienst registriert.

### <a name="non-sales-transactions-and-shift-closing"></a>Nichtverkaufstransaktionen und Schichtabschluss

Die folgenden Nichtverkaufstransaktionen werden im Steuerregistrierungsdienst unter Verwendung von als nicht steuerliche Vorgänge mithilfe dem **NFS** Etikett registriert:

- Ausgangsbetrag deklarieren
- Mittelzugang
- Zahlungsmittel entfernen
- Ablage in Tresor
- Bankeinzahlung
- Ertragskonten
- Aufwandskonten

Der Vorgang **Nichtverkaufstransaktionen** werden im Steuerregistrierungsdienst mithilfe dem **NFS** Etikett als nicht steuerliche Vorgänge registriert.

### <a name="data-export-and-audit"></a>Datenexport und Audit

Alle Transaktionen müssen von einem TSE signiert werden, um ihre Integrität, Authentizität und Vollständigkeit sicherzustellen und um die Manipulation aufgezeichneter Daten zu verhindern.

> [!WARNING]
> Es kann nur ein zertifizierter TSE verwendet werden. Informationen zu den Typen und Modellen von TSEs, die von der EFR-Lösung unterstützt werden, finden Sie im „EFR-Handbuch \[DE\]“-Dokument, das auf der Website [EFSTA-Dokumentation](https://public.efsta.net/efr/) veröffentlicht wird. Informationen zur Auswahl und zum Erhalt eines TSE erhalten Sie von [EFSTA](https://www.efsta.eu/at/kontakt).

Vorschriften in Deutschland erfordern Unterstützung für den DSFinV-K-Export. Der DSFinV-K-Export kann in der EFR-Lösung ausgelöst werden. Weitere Informationen zum DSFinV-K-Export finden Sie im „EFR-Handbuch \[DE\]“-Dokument, das auf der Website [EFSTA-Dokumentation](https://public.efsta.net/efr/) veröffentlicht wird.

### <a name="default-data-mapping"></a>Standarddatenzuordnung

Die folgende Standarddatenzuordnung ist in der Steuerbeleganbieter-Konfiguration enthalten, die als Teil des Steuerintegrationsbeispiels bereitgestellt wird.

- **Ausschreibungstypzuordnung** 1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1

    > [!NOTE]
    > In jedem Wertepaar, das durch ein Semikolon (;) getrennt ist, bezieht sich die erste Zahl auf eine Zahlungsmethode, die für das Geschäft eingerichtet wurde. Die zweite Nummer bezieht sich auf eine entsprechende Zahlungsgruppe im EFR-Dienst, dargestellt durch das **PayG** Attribut.

- **Zuordnung der Mehrwertsteuersätze:** A: 19.00; B: 7,00; C: 10,70; D: 5,50; E: 0,00

    > [!NOTE]
    > In jedem Wertepaar, das durch ein Semikolon (;) getrennt ist, bezieht sich der Buchstabe auf eine Steuergruppe im EFR-Dienst, dargestellt durch das **TaxG** Attribut. Die Zahl bezieht sich auf den Steuerprozentsatz.

- **Steuergruppe für Geschenkkarten und Einzahlungen:** G
- **Steuergruppe für Mehrwertsteuer befreit:** F

> [!WARNING]
> Die Steuereinstellungen in der Standarddatenzuordnung sind für die Übereinstimmung der Steuereinstellungen im System und der Steuergruppen im EFR-Dienst verantwortlich. Steuergruppen können nur dann auf Quittungen gedruckt werden, wenn das Feld **Code zum Drucken** auf der Seite **Umsatzsteuerkennzeichen** festgelegt ist.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

Der Steuererfassungsdienst unterstützt nur Szenarien, bei denen die Mehrwertsteuer in den Preisen enthalten sind. Daher muss die Option **Preise in Mehrwertsteuer enthalten** auf **Ja** sowohl für Geschäfte als auch Debitoren festgelegt werden.

Der Finanzdienst unterstützt keine Situationen, in denen mehr als ein Umsatzsteuerkennzeichen auf dieselbe Transaktionszeile angewendet wird.

Das Rahmenwerk für die steuerliche Integration unterstützt keine Angebote. Daher sind diese Vorgänge nicht im Finanzdienst registriert.

## <a name="set-up-commerce-for-germany"></a>Commerce für Deutschland einrichten

In diesem Abschnitt werden die Commerce-Einstellungen beschrieben, die für Deutschland spezifisch und empfohlen sind. Weitere Informationen für das Einrichten finden Sie unter [Commerce-Homepage](../index.md).

Um die Deutschland-spezifischen Funktionen zu verwenden, müssen Sie die folgenden Einstellungen angeben.

- Legen Sie in der primären Adresse der juristischen Person das Feld **Land/Region** auf **DEU** (Deutschland) fest.
- Legen Sie im POS-Funktionsprofil jedes einzelnen Einzelhandelsgeschäfts in Österreich das Feld **ISO-Code** auf **DE** (Deutschland) fest.

Sie müssen auch die folgenden Einstellungen für Deutschland angeben. Stellen Sie sicher, dass Sie entsprechende Verteilungseinzelvorgänge ausführen müssen, nachdem Sie die Einrichtung abschließen.

### <a name="set-up-vat-per-german-requirements"></a>MwSt. nach deutschen Anforderungen einrichten

Sie müssen Mehrwertsteuercodes, Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen erstellen. Sie müssen auch Mehrwertsteuerinformationen für Produkte und Dienstleistungen einrichten. Weitere Informationen dazu, wie die Mehrwertsteuer in eingerichtet und verwendet wird, finden Sie unter [Mehrwertsteuerüberblick](../../finance/general-ledger/indirect-taxes-overview.md).

Auf Verkaufsbelegen können Sie einen abgekürzten Code für einen Mehrwertsteuercode drucken (beispielsweise „A“ oder „B”). Um diese Funktionalität verfügbar zu machen, legen Sie das Feld **Code zum Drucken** auf der Seite **Mehrwertsteuercodes** fest.

### <a name="set-up-stores"></a>Shops einrichten

Aktualisieren Sie auf der Seite **Alle Geschäfte** die Details der Geschäfte. Legen Sie genauer die folgenden Parameter fest:

- Geben Sie im Feld **Mehrwertsteuergruppe** die Mehrwertsteuergruppe an, die für Verkäufe an den Standarddebitoren verwendet werden soll.
- Legen Sie die Option **Preis enthält Mehrwertsteuersatz** auf **Ja** fest.
- Legen Sie das Feld **Name** auf den Unternehmensnamen fest. Durch diese Änderung wird sichergestellt, dass der Unternehmensname auf dem Verkaufsbeleg angezeigt wird. Alternativ können Sie den Unternehmensnamen im Verkaufsbeleglayout als Freiformtext hinzufügen.
- Legen Sie das Feld **Steuernummer (TIN)** auf die Unternehmenskennnummer fest. Durch diese Änderung wird sichergestellt, dass die Identifikationsnummer auf dem Verkaufsbeleg angezeigt wird. Alternativ können Sie Unternehmenskennnummer dem Verkaufsbeleglayout als Freiformtext hinzufügen.

### <a name="set-up-functionality-profiles"></a>Einrichten von Funktionsprofilen

POS-Funktionsprofile einrichten. Richten Sie im Inforegister **Belegnummerierung** die Belegnummerierung ein, indem Sie Datensätzen für die Belegbuchungstypen **Verkauf**, **Auftrag** und **Retoure** erstellen oder aktualisieren.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurieren Sie benutzerdefinierte Felder, damit sie in Belegformate für Verkaufsbelege verwendet werden können

Sie können den Sprachtext und die benutzerdefinierten Felder konfigurieren, die in den POS-Belegformaten verwendet werden. Das Standardunternehmen des Benutzers, der die Boneinrichtung erstellt, sollte die gleiche juristische Person sein, in dem die Sprachtexteinstellung erstellt wird. Alternativ sollten dieselben Sprachtexte im Standardunternehmen des Benutzers und in der juristischen Person des Shops verwendet werden, für den das Setup erstellt wird.

Fügen Sie auf der Seite **Sprachentext** die folgenden Datensätze für die Beschriftungen der benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass **Sprachen-ID**, **Text-ID** und **Text**-Werte, die in der Tabelle angezeigt werden, nur Beispiele sind. Sie können sie ändern, damit sie Ihre Anforderungen erfüllen. Allerdings müssen die **Text-ID**-Werte, die Sie verwenden, eindeutig sein und gleich oder größer als 900001 sein.

Fügen Sie dem Abschnitt **POS** der Seite **Sprachentext** aus der Tabelle die folgenden POS-Beschriftungen hinzu:

| Sprachkennung | Textkennung | Text                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR-Code                               |
| en-US       | 900002  | Transaktions-ID                        |
| en-US       | 900003  | Einzelhandelsdruckcode für Steuer                 |
| en-US       | 900004  | Steuerbetrag (Umsatz)                    |
| en-US       | 900005  | Steuergrundlage (Umsatz)                     |
| en-US       | 900006  | Datum und Uhrzeit des Buchungsstarts           |
| en-US       | 900007  | Datum und Uhrzeit des Buchungsendes             |
| en-US       | 900008  | Seriennummer des Sicherheitselements |
| en-US       | 900009  | Signaturzähler                     |
| en-US       | 900010  | Wert prüfen                           |
| en-US       | 900011  | Infomeldung                          |

Fügen Sie auf der Seite **Benutzerdefinierte Felder** die folgenden Datensätze für die benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass die Werte für **Textkennung Titel** den Werten **Textkennung** entsprechen müssen, die Sie auf der Seite **Sprachentext** angegeben haben.

| Name                            | Typ    | Textkennung Titel |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Zugang | 900001          |
| TRANSACTIONID\_DE               | Zugang | 900002          |
| RETAILPRINTCODE\_DE             | Zugang | 900003          |
| SALESTAXAMOUNT\_DE              | Zugang | 900004          |
| SALESTAXBASIS\_DE               | Zugang | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Zugang | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Zugang | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Zugang | 900008          |
| SIGNCOUNTER\_DE                 | Zugang | 900009          |
| SIGN\_DE                        | Zugang | 900010          |
| INFOMESSAGE\_DE                 | Zugang | 900011          |

### <a name="configure-receipt-formats"></a>Bonformate konfigurieren

Ändern Sie für jedes erforderliche Format den Wert des Felds **Druckverhalten** auf **Immer drucken**.

In Designer für Bonformat fügen Sie die folgenden benutzerdefinierten Felder den entsprechenden Bonabschnitten hinzu. Beachten Sie, dass die Feldnamen den Sprachtexten entsprechen, die Sie im vorherigen Abschnitt definiert haben.

- **Kopfzeile:** Fügen Sie die folgenden Felder hinzu:

    - Die Felder **Shopname** und **Steueridentifikationsnummer**, die zum Drucken des Unternehmensnamens und der Kennungsnummer auf Belegen verwendet werden. Alternativ können Sie den Unternehmensnamen und die Kennungsnummer im Layout als Freiformtext hinzufügen.
    - **Shopadresse**, **Datum**, **Zeit 24 h**, **Bonnummer** und **Registernummer**

- **Positionen:** Fügen Sie die folgenden Felder hinzu:

    - **Artikelname** Feld
    - **Menge** Feld
    - Feld **Gesamtpreis mit Steuer**
    - Das Feld **Steuereinzelhandels-Druckcode**, das verwendet wird, um den abgekürzten Code zu drucken, der dem Mehrwertsteuercode entspricht, der für den Artikel gilt

- **Fußzeile:** Fügen Sie die folgenden Felder hinzu:

    - Ändern Sie die Zahlungsfelder, damit die Zahlungsbeträge für jede Zahlungsmethode gedruckt werden. Beispiel: Fügen Sie die Felder **Name des Zahlungsmittels** und **Betrag des Zahlungsmittels** einer Position des Layouts hinzu.
    - Felder in der **Steueraufschlüsselung** Feldgruppe. Die Felder in dieser Feldgruppe müssen in einer separaten Position gedruckt werden.

        - Feld **Steuerkennung**, das ein Standardfeld ist, das den Druck einer Mehrwertsteuerzusammenfassung für jeden Mehrwertsteuercode aktiviert. Das Feld muss einer neuen Position hinzugefügt werden.
        - **Steuerprozentsatz**-Feld, das ein Standardfeld ist, das zum Drucken des tatsächlichen Steuersatzes für den Mehrwertsteuercode verwendet wird.
        - Feld **Steuerbasis (Verkauf)**, das verwendet wird, um den Gesamtbarverkaufsbetrag für den Mehrwertsteuercode des Belegs zu drucken. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
        - Feld **Steuerbetrag (Verkauf)**, das verwendet wird, um den Steuerbetrag für Barverkäufe des Belegs für den Mehrwertsteuercode zu drucken.
        - Feld **Steuereinzelhandels-Druckcode**, das verwendet wird, um den abgekürzten Code zu drucken, der dem Mehrwertsteuercode entspricht.

    - Felder, die gesicherte Transaktionsdaten enthalten, die vom Steuerregistrierungsdienst zurückgegeben werden:

        - Feldr **Transaktions-ID**, um die Nummer der Bargeldbuchungen im Steuererfassungsdienst zu identifizieren
        - **Transaktionsstartdatum** Feld
        - **Transaktionsenddatum** Feld
        - Feld **Seriennummer des Sicherheitselements**
        - **Signaturzähler** Feld
        - **Wert prüfen** Feld
        - Feld **QR-Code**, das verwendet wird, um den Verweis auf die erfasste Bargeldbuchung in der Form eines QR-Codes zu drucken

    - Das Feld **Info Nachricht** auf den Belegen zeigt eine Benachrichtigungsnachricht des Steuerregistrierungsdienstes. Wenn beispielsweise ein Signaturgerät defekt ist, kann ein spezieller Text auf eine Quittung gedruckt werden.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Einrichten und Entwerfen von Bonformaten](../receipt-templates-printing.md).

### <a name="configure-fiscal-integration"></a>Steuerintegration konfigurieren

Schließen Sie die Schritte zur Einrichtung der steuerlichen Integration ab, wie unter [Einrichtung der steuerlichen Integration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) beschrieben sind:

  1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Beachten Sie bitte auch die Einstellungen für den Steuererfassungsprozess, die [für dieses Steuererfassungsdienst-Integrationsbeispiel spezifisch sind](#set-up-the-registration-process).
  2. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

> [!WARNING]
> Die Fehlerbehandlungsfunktionen des Rahmens für die steuerliche Integration sind möglicherweise nicht vollständig an die örtlichen steuerlichen Vorschriften angepasst.
>
> - Wir empfehlen Ihnen, die Option **Fahren Sie mit dem Fehler fort** auf der **Steuerlicher Registrierungsprozess** zu verlassen, da alle Transaktionen korrekt registriert werden müssen, auch wenn der erste Versuch der Steuerregistrierung nicht erfolgreich war.
> - Bevor Sie die Option **Überspringen** oder **Als registriert markieren** auf der Seite **Steuerlicher Registrierungsprozess** aktivieren, sollten Sie diese Änderungen des Steuerregistrierungsprozesses mit Ihrem Steuerberater oder dem örtlichen Finanzamt besprechen.

  3. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

## <a name="deployment-guidelines-for-cash-registers-for-germany"></a>Bereitstellungsrichtlinien für Kassen für Deutschland

Das Steuererfassungsdienst-Integrationsbeispiel für Deutschland ist Teil des Retail SDK. Mehr Informationen zur Installation und Verwendung des Retail SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Dieses Beispiel besteht aus Erweiterungen für die Commerce Runtime (CRT) und Hardwarestation. Um dieses Beispiel auszuführen, müssen Sie die CRT und Hardwarestation-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Thema beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps, bei dem noch keine Dateien geändert wurden.

Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.

### <a name="enable-crt-extensions"></a>Aktivieren der CRT Erweiterungen

Die CRT-Erweiterungskomponenten sind in den CRT-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die CRT-Lösung, **CommerceRuntimeSamples.sln**, unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample-Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.EFRSample**, und erstellen Sie es.
2. Im Ordner **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** suchen Sie die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce Scale Unit** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem Microsoft Internet Information Services (IIS) Commerce Scale Unit Standort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei:

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR-Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.DataModelEFR**, und erstellen Sie es.
2. Im Ordner **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** suchen Sie die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce-Skalierungseinheit:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="update-the-extension-configuration-file"></a>Die Erweiterungskonfigurationsdatei aktualisieren

1. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

2. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-hardware-station-extensions"></a>Hardware station-Erweiterungen aktivieren

Die Hardware station-Erweiterungskomponenten sind in den Hardware station-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung **HardwareStationSamples.sln.sln** unter **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample-Komponente

1. Suchen Sie das Projekt **HardwareStation.Extension.EFRSample**, und erstellen Sie es.
2. Im Ordner **Extension.EFRSample\\bin\\Debug** suchen Sie folgende Montage-Dateien:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopieren Sie die Assembly-Dateien in den Hardware stations-Erweiterungsordner:

    - **Freigegebene Hardware station:** Kopieren Sie die Dateien in den Ordner **Lagerfach** unter dem IIS Hardware stations-Websitespeicherort.
    - **Dedizierte Hardware station auf Modern POS:** Kopieren Sie die Dateien zum Modern POS-Client-Broker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für die Erweiterungen der Hardware station. Die Datei hat den Namen **HardwareStation.Extension.config**.

    - **Freigegebene Hardware station:** Die Datei befindet sich unter dem IIS Hardware station-Websitespeicherort.
    - **Dedizierte Hardware station auf Modern POS:** Die Datei befindet sich unter dem Modern POS-Client-Broker-Speicherort.

5. Fügen Sie die folgende Position zum Abschnitt **Anordnung** der Konfigurationsdatei hinzu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Erfassungsprozess zu aktivieren, führen Sie diese Schritte aus, um die Commerce Zentralverwaltung einzurichten. Weitere Einzelheiten finden Sie unter [Steuerliche Integration für Commerce-Kanäle einrichten](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
2. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektoren**, und laden Sie die Konnektorkonfiguration. Der Dateispeicherort ist **RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml**.
3. Wechseln Sie zu **Retail and Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerdokumentanbieter**, und laden Sie die Dokumentanbieterkonfigurationen. Die Konfigurationsdateien befinden sich unter **RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml**.
4. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie ein neues funktionales Konnektorprofil, und wählen Sie den Dokumentanbieter und den Konnektor aus, den Sie vorher geladen haben. Aktualisieren Sie die Datenzuordnungseinstellungen nach Bedarf.

    > [!NOTE]
    > Standardmäßig ist die **Kundendaten einschließen** Option auf **Ja** festgelegt. Wenn Sie nicht möchten, dass Kundeninformationen wie Namen und Adressen an den Steuerregistrierungsdienst gesendet werden, können Sie die Einstellung auf **Nein** ändern.

5. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Konnektorprofil, und wählen Sie den Konnektor aus, den Sie vorher geladen haben. Aktualisieren Sie die Verbindungseinstellungen nach Bedarf.

    > [!WARNING]
    > Standardmäßig ist der **Steuerregistrierungsbenachrichtigungen anzeigen** Parameter eingeschaltet. Wir empfehlen, dass Sie es aktiviert lassen, da der Steuerregistrierungsdienst Benachrichtigungen über bestimmte Fehler sendet, die bei der Steuerregistrierung auftreten können (z. B. wurde eine Transaktion zum Zeitpunkt der Registrierung nicht signiert).

6. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**. Erstellen Sie eine neue Steuerkonnektorgruppen für das funktionale Konnektorfunktionsprofil, das Sie vorher erstellt haben.
7. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Steuererfassungsprozess, zwei Steuererfassungsprozess-Schritte, und wählen Sie die Steuerkonnektorgruppe aus, die Sie vorher erstellt haben.
8. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben.
9. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**. Wählen Sie ein Hardwareprofil aus, das mit der Hardware station verknüpft ist, mit der der Belegdrucker verbunden wird. Im Inforegister **Peripheriegeräte für die Steuerverwaltung** aktivieren Sie das technische Konnektorprofil, das Sie vorher erstellt haben.
10. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**, und wählen Sie Jobs **1070** und **1090** ausführen, um Daten zur Kanaldatenbank zu übertragen.

### <a name="production-environment"></a>Produktionsumgebung

In der vorherigen Prozedur aktivieren Sie die Erweiterungen, die Komponenten des Steuererfassungsdienst-Integrationsbeispiels sind. Darüber hinaus müssen Sie diese Schritte ausführen, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden.

1. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    - In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Zeilen dem Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Nehmen Sie die folgenden Änderungen in der Paketanpassungs-Konfigurationsdatei **BuildTools\\Customization.settings** vor:

    - Fügen Sie die folgenden Zeilen hinzu, um die CRT-Erweiterungen in die bereitstellbaren Paketen einzuschließen.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Fügen Sie die folgende Zeilen hinzu, um die Hardwarestation-Erweiterung in die bereitstellbaren Pakete einzuschließen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
4. Übernehmen Sie die Pakete über Microsoft Dynamics Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Schließen Sie alle erforderlichen Setupaufgaben ab, die früher im Abschnitt [Commerce für Deutschland einrichten](#set-up-commerce-for-germany) beschrieben sind.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

### <a name="crt-extension-design"></a>CRT Erweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.EFRSample**. Weitere Einzelheiten über das Design der Lösung für die steuerliche Integration finden Sie unter [Überblick über die steuerliche Integration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Anforderungshandler

Es gibt einen Anforderungshandler für den Dokumentanbieter: **DocumentProviderEFRFiscalDEU**. Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen. Er wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Diese Anfrage gibt die Antwort zusammen mit erweiterten Daten zurück.

#### <a name="configuration"></a>Variante

Die **DocumentProviderFiscalEFRSampleGermany** Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck dieser Datei ist es, Einstellungen zu aktivieren, damit der Dokumentanbieter von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

Die folgenden Einstellungen werden hinzugefügt:

- **Zuordnung der Mehrwertsteuersätze** – Die Zuordnung von Steuerprozentsatzwerten, die für die Umsatzsteuerkennzeichen eingerichtet wurden, zu Werten der **TaxG** Attribute (Steuergruppe) in Anforderungen, die an den Finanzdienst gesendet werden.
- **Steuergruppe für Geschenkkarten und Einzahlungen** – Der Wert der **TaxG** Attribut in Anfragen, die an den Finanzdienst gesendet werden, basierend auf Vorgängen, die Geschenkkarten oder Einzahlungen beinhalten.
- **Ausschreibungstypzuordnung** – Die Zuordnung von Zahlungsmethoden zu Werten der **PayG** Attribute (Zahlungsgruppe) in Anforderungen, die an den Finanzdienst gesendet werden.
- **Steuergruppe für Mehrwertsteuer befreit** – Der Wert der **TaxG** Attribute in Anforderungen, die an den Finanzdienst gesendet werden, basierend auf Vorgängen, die von steuerlichen Verpflichtungen befreit sind.
- **Kundendaten einschließen** – Wenn dieser Parameter aktiviert ist, enthalten Anfragen an den Finanzdienst Kundeninformationen wie Namen und Adressen, wenn ein Kunde zu einer Transaktion hinzugefügt wird.

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuererfassungsdienst.

Die Hardware station-Erweiterung ist **HardwareStation.Extension.EFRSample**. Sie verwendet das HTTP-Protokoll, um Dokumente, die die CRT-Erweiterung generiert, zum Steuererfassungsdienst zu übermitteln. Sie handhabt auch die Antworten, die vom Steuererfassungsdienst empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EFRHandler** ist der Einstiegspunkt für die Handhabung von Anforderungen an den Steuererfassungsdienst. Dieser Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Steuererfassungsdienst und gibt eine Antwort von ihm zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsdiensts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Steuererfassungsdiensts verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck dieser Datei ist es, Einstellungen zu aktivieren, damit der Steuerkonnektor von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

Die folgenden Einstellungen werden hinzugefügt:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Zeitlimit** – Die Zeitdauer in Millisekunden (ms), die der Treiber auf eine Antwort vom Steuererfassungsdienst wartet.
- **Steuerregistrierungsbenachrichtigungen anzeigen** – Wenn dieser Parameter aktiviert ist, werden Benachrichtigungen vom Finanzdienst als Benutzermeldungen am POS angezeigt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]