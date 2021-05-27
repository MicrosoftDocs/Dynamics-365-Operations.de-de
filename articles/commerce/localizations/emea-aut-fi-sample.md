---
title: Beispiel der Steuerregistrierungsserviceintegration für Österreich
description: In diesem Thema erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Österreich.
author: josaw
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Austria
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-3-1
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 973047b5e904a3b684e287cbe39dde9d4008c7ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020301"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Integrationsbeispiel für Steuererfassungsdienst für Österreich

[!include[banner](../includes/banner.md)]

## <a name="introduction"></a>Einführung

Um die lokalen steuerlichen Anforderungen für Kassen in Österreich zu erfüllen, umfassen die Dynamics 365 Retail-Funktionen für Österreich eine Beispielintegration der Verkaufsstelle (POS) in einen externen Steuerregistrierungsservice. Das Beispiel erweitert die [steuerliche Integrationsfunktionen](fiscal-integration-for-retail-channel.md). Es basiert auf der [EFR (Electronisches Fiskalregister)](https://www.efsta.eu/at/fiskalloesungen/oesterreich)-Lösung von [EFSTA](https://www.efsta.eu/at/) und ermöglicht die Kommunikation mit dem EFR-Service über das HTTPS-Protokoll. Der EFR-Dienst sollte entweder in der Retail Hardware station oder auf einem separaten Computer gehostet werden, zu dem von der Hardare station aus eine Verbindung hergestellt werden kann. Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Retail Software Development Kit (SDK).

Microsoft gibt keine Hardware, Software oder Dokumentation von EFSTA aus frei. Um Informationen darüber zu erhalten, wie Sie die EFR-Lösung beziehen und betreiben, wenden Sie sich an [EFSTA](https://www.efsta.eu/at/kontakt).


## <a name="scenarios"></a>Szenarien

Die folgenden Szenarien werden im Beispiel für die Integration des Steuerregistrierungsservice für Österreich abgedeckt:

- Registrierung der Bargeldbuchungen im Steuererfassungsdienst:

    - Senden Sie detaillierte Buchungsdaten zum Steuererfassungsdienst. Diese Daten beinhalten Informationen zu Verkaufspositionen sowie Informationen über Rabatte, Zahlungen und Steuern.
    - Erfassen Sie eine Antwort vom Steuererfassungsdienst. Diese Antwort beinhaltet eine digitale Signatur und einen Link zur erfassten Buchung.
    - Erfassen Sie Steuern und ordnen Sie diese den Steuercodes des Erfassungsdiensts zu.
    - Drucken Sie den QR-Code für eine erfasste Buchung auf den Beleg.

- Die Erfassung von Geschenkkartenvorgängen und Debitoreneinzahlungen als Sachbuchungen im Steuererfassungsdienst.

    - Stellen Sie eine Geschenkkarte aus oder laden Sie sie mit Geld auf.
    - Erfassen Sie eine Debitorenkonto-Einzahlung.
    - Erfassen Sie eine Debitorenauftragseinzahlung.

- Die Erfassung von Sachbuchungen und Ereignissen im Steuererfassungsdienst:

    - Schlicht öffnen und Schicht schließen
    - Anfangsbetrag, Bareinlage und Zahlungsmittelentfernung
    - Preisüberschreibung
    - MwSt.-Überschreibung
    - Belegkopie drucken
    - Kassenlade öffnen
    - X-Bericht drucken
    - Z-Bericht drucken

- Drucken von Tagesendabrechnungen (X/Z-Berichte) die spezifische Felder für Österreich enthalten:

    - Gesamtanzahl von Produkten oder Dienstleistungen, die an Debitoren geliefert wurden
    - Aufschlüsselung von Verkäufen nach Steuersatz
    - Aufschlüsselung von Zahlungen nach Kassierer-/Kassenoperator
    - Preisrabatte und Retouren, die Tagesumsatz verringern
    - Nullverkäufe (Geschenke)

- Fehlerbehebung, wie beispielsweise die folgenden Optionen:

    - Versuchen Sie die Steuererfassung erneut, falls ein Neuversuch möglich ist, wie z. B. wenn der Steuererfassungsdienst nicht verfügbar ist, nicht bereit ist oder nicht reagiert.
    - Verschieben Sie die Steuererfassung.
    - Überspringen Sie Steuererfassung, oder markieren Sie die Buchung als erfasst, und schließen Sie Infocodes ein, um den Grund für den Fehler und zusätzliche Informationen zu erfassen.
    - Überprüfen Sie die Verfügbarkeit des Steuererfassungsdiensts, bevor eine neue Verkaufsbuchung geöffnet wird oder eine Verkaufsbuchung abgeschlossen wird.

### <a name="default-data-mapping"></a>Standarddatenzuordnung

Die folgende Standarddatenzuordnung ist in der Steuerbeleganbieter-Konfiguration enthalten, die als Teil des Steuerintegrationsbeispiels bereitgestellt wird:

- Mehrwertsteuer-(MwSt.)-Satzzuordnung:

    *A: 20,00; B: 10,00; C: 13,00; D: 0,00; E: 19,00; F: 7,00*

### <a name="gift-cards"></a>Geschenkkarten

Das Steuererfassungsdienst-Integrationsbeispiel implementiert die folgenden Regeln bezüglich Geschenkkarten:

- Schließen Sie Verkaufspositionen aus, die sich auf die Vorgänge *Geschenkkarte ausstellen* und *Zu Geschenkkarte hinzufügen* aus einer Bargeldbuchung beziehen. Anstatt diese Positionen als Teil einer Bargeldbuchung zu erfassen, erfassen Sie sie als getrennte Sachbuchung im Steuererfassungsdienst.
- Drucken Sie keine Steuergruppenaufschlüsselung und keinen QR-Code auf einen Beleg, wenn der Beleg nur aus Geschenkkartenpositionen besteht.
- Drucken Sie den Gesamtbetrag von Geschenkkarten, die in einer Buchung getrennt vom Bargeldbuchungsbetrag auf dem Beleg ausgestellt oder erneut belastet wurden.
- Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanaldatenbank mit einem Verweis auf eine entsprechende Steuerbuchung.
- Zahlung per Geschenkkarte wird als eine normale Zahlung betrachtet.

### <a name="customer-deposits-and-customer-order-deposits"></a>Debitoreneinzahlungen und Debitorenauftragseinzahlungen

Das Integrationsbeispiel des Steuererfassungsdiensts implementiert die folgenden Regeln in Bezug auf Debitoreneinzahlungen und Debitorenauftragseinzahlungen:

- Erfassen Sie eine Sachbuchung, wenn eine Buchung eine Debitoreneinzahlung ist.
- Erfassen Sie eine Bargeldbuchung, wenn eine Buchung nur eine Debitorenauftragseinzalung oder eine Debitoren-Auftragseinzahlungsrückerstattung enthält.
- Ziehen Sie den Debitorenauftragseinzahlungsbetrag von den Zahlungspositionen ab, wenn ein hybrider Kundenauftrag erstellt wird.
- Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanaldatenbank mit einem Verweis auf eine Steuerbuchung für einen hybriden Debitorenauftrag.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

Der Steuererfassungsdienst unterstützt nur Szenarien, bei denen die Mehrwertsteuer im Preis enthalten ist. Daher muss die Option **Preis in Mehrwertsteuer enthalten** auf **Ja** sowohl für Geschäfte als auch Debitoren festgelegt werden.

## <a name="set-up-commerce-for-austria"></a>Commerce für Österreich einrichten

In diesem Abschnitt werden die Commerce-Einstellungen beschrieben, die für Österreich spezifisch und empfohlen sind. Weitere Informationen zum Einrichten finden Sie unter [Commerce-Homepage](../index.md).

Um die Österreich-spezifischen Funktionen zu verwenden, müssen Sie die folgenden Einstellungen angeben:

- Legen Sie in der primären Adresse der juristischen Person das Feld **Land/Region** auf **AUT** (Österreich) fest.
- Legen Sie im POS-Funktionsprofil jedes einzelnen Einzelhandelsgeschäfts in Österreich das Feld **ISO-Code** auf **AT** (Österreich) fest.

Sie müssen auch die folgenden Einstellungen für Österreich angeben. Beachten Sie, dass Sie entsprechende Verteilungseinzelvorgänge ausführen müssen, nachdem Sie die Einrichtung abschließen.

### <a name="set-up-vat-per-austrian-requirements"></a>MwSt. nach österreichischen Anforderungen einrichten


Sie müssen Mehrwertsteuercodes, Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen erstellen. Sie müssen auch Mehrwertsteuerinformationen für Produkte und Dienstleistungen einrichten. Weitere Informationen dazu, wie die Mehrwertsteuer in eingerichtet und verwendet wird, finden Sie unter [Mehrwertsteuerüberblick](../../finance/general-ledger/indirect-taxes-overview.md).


Auf Verkaufsbelegen können Sie einen abgekürzten Code für einen Mehrwertsteuercode drucken (beispielsweise „A“ oder „B”). Um diese Funktionalität verfügbar zu machen, legen Sie das Feld **Code drucken** auf der Seite **Mehrwertsteuercodes** fest.

### <a name="set-up-stores"></a>Shops einrichten

Aktualisieren Sie auf der Seite **Alle Geschäfte** die Details der Geschäfte. Legen Sie genauer die folgenden Parameter fest:

- Geben Sie im Feld **Mehrwertsteuergruppe** die Mehrwertsteuergruppe an, die für Verkäufe an den Standarddebitoren verwendet werden soll.
- Legen Sie die Option **Preis enthält Mehrwertsteuersatz** auf **Ja** fest.
- Legen Sie das Feld **Name** auf den Unternehmensnamen fest. Durch diese Änderung wird sichergestellt, dass der Unternehmensname auf dem Verkaufsbeleg erscheint. Alternativ können Sie den Unternehmensnamen im Verkaufsbeleglayout als Freiformtext hinzufügen.
- Legen Sie das Feld **Steuernummer (TIN)** auf die Unternehmenskennnummer fest. Durch diese Änderung wird sichergestellt, dass die Identifikationsnummer auf dem Verkaufsbeleg erscheint. Alternativ können Sie Unternehmenskennnummer dem Verkaufsbeleglayout als Freiformtext hinzufügen.

### <a name="set-up-functionality-profiles"></a>Einrichten von Funktionsprofilen

POS-Funktionsprofile einrichten:

- Richten Sie im Inforegister **Belegnummerierung** die Belegnummerierung ein, indem Sie Datensätzen für die Belegbuchungstypen **Verkauf**, **Auftrag** und **Retoure** erstellen oder aktualisieren.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurieren Sie benutzerdefinierte Felder, damit sie in Belegformate für Verkaufsbelege verwendet werden können

Sie können den Sprachtext und die benutzerdefinierten Felder konfigurieren, die in den POS-Belegformaten verwendet werden. Das Standardunternehmen des Benutzers, der die Boneinrichtung erstellt, sollte die gleiche juristische Person sein, in dem die Sprachtexteinstellung erstellt wird. Alternativ sollten dieselben Sprachtexte im Standardunternehmen des Benutzers und in der juristischen Person des Shops verwendet werden, für den das Setup erstellt wird.

Fügen Sie auf der Seite **Sprachentext** die folgenden Datensätze für die Beschriftungen der benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass **Sprachen-ID**, **Text-ID** und **Text**-Werte, die in der Tabelle angezeigt werden, nur Beispiele sind. Sie können sie ändern, damit sie Ihre Anforderungen erfüllen. Allerdings müssen die **Text-ID**-Werte, die Sie verwenden, eindeutig sein und gleich oder größer als 900001 sein.

Fügen Sie dem Abschnitt **POS** des **Sprachentext** aus der Tabelle die folgenden POS-Beschriftungen hinzu:

| Sprachkennung | Textkennung | Text                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR-Code                   |
| en-US       | 900002  | Forlaufende Nummer         |
| en-US       | 900003  | Einzelhandelsdruckcode für Steuer     |
| en-US       | 900004  | Gesamt (Umsatz)             |
| en-US       | 900005  | Gesamte Steuern (Umsatz)         |
| en-US       | 900006  | Gesamte enthaltene Steuern (Umsatz) |
| en-US       | 900007  | Steuerbetrag (Umsatz)        |
| en-US       | 900008  | Steuergrundlage (Umsatz)         |

Fügen Sie auf der Seite **Benutzerdefinierte Felder** die folgenden Datensätze für die benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass die Werte für **Textkennung Titel** den Werten **Textkennung** entsprechen müssen, die Sie auf der Seite **Sprachentext** angegeben haben:

| Name                 | Typ    | Textkennung Titel |
|----------------------|---------|-----------------|
| QRCODE               | Zugang | 900001          |
| CONTINUOUSNUMBER     | Zugang | 900002          |
| RETAILPRINTCODE      | Zugang | 900003          |
| SALESTOTAL           | Zugang | 900004          |
| SALESTOTALTAX        | Zugang | 900005          |
| SALESTOTALINCLUDETAX | Zugang | 900006          |
| SALESTAXAMOUNT       | Zugang | 900007          |
| SALESTAXBASIS        | Zugang | 900008          |

### <a name="configure-receipt-formats"></a>Bonformate konfigurieren

Ändern Sie für jedes erforderliche Belegformat den Wert des Felds **Druckverhalten** auf **Immer drucken**.

In Designer für Bonformat fügen Sie die folgenden benutzerdefinierten Felder den entsprechenden Bonabschnitten hinzu. Beachten Sie, dass die Feldnamen den Sprachtexten entsprechen, die Sie im vorherigen Abschnitt definiert haben.

- **Kopfzeile:** Fügen Sie die folgenden Felder hinzu:

    - Die Felder **Shopname** und **Steueridentifikationsnummer**, die zum Drucken des Unternehmensnamens und der Identitätsnummer auf Belegen verwendet werden. Alternativ können Sie den Unternehmensnamen und die Identitätsnummer im Layout als Freiformtext hinzufügen.
    - **Shopadresse**, **Datum**, **Zeit 24 h**, **Bonnummer** und **Registernummer**
    - Felder **Fortlaufende Zahl**, um die Nummer der Bargeldbuchungen im Steuererfassungsdienst zu identifizieren.

- **Positionen:** Fügen Sie die folgenden Felder hinzu:

    - **Artikelname**.
    - **Menge**.
    - **Gesamtpreis mit USt.**.
    - **Steuereinzelhandels-Druckcode**, der verwendet wird, um den abgekürzten Code zu drucken, der dem Mehrwertsteuercode entspricht, der für den Artikel gilt.

- **Fußzeile:** Fügen Sie die folgenden Felder hinzu:

    - Ändern Sie die Zahlungsfelder, damit die Zahlungsbeträge für jede Zahlungsmethode gedruckt werden. Beispiel: Fügen Sie die Felder **Name des Zahlungsmittels** und **Betrag des Zahlungsmittels** einer Position des Layouts hinzu.
    - **Verkaufssumme**-Feldgruppe:

        - Feld **Summe (Verkauf)**, das verwendet wird, um den Gesamt-Barverkaufsbetrag des Belegs zu drucken. Der Betrag enthält keine Steuer. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
        - Feld **Summe einschließlich Steuer (Verkauf)**, das verwendet wird, um den Gesamt-Barverkaufsbetrag des Belegs zu drucken. Der Betrag enthält Steuer. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
        - Feld **Gesamtsteuer (Verkauf)**, das verwendet wird, um den Gesamtsteuerbetrag für Barverkäufe des Belegs zu drucken. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.

    - **Steueraufschlüsselung**-Feldgruppe. Die Felder in dieser Feldgruppe müssen in einer separaten Position gedruckt werden.

        - Feld **Steuerkennung**, das ein Standardfeld ist, das den Druck einer Mehrwertsteuerzusammenfassung für jeden Mehrwertsteuercode aktiviert. Das Feld muss einer neuen Position hinzugefügt werden.
        - **Steuerprozentsatz**-Feld, das ein Standardfeld ist, das zum Drucken des tatsächlichen Steuersatzes für den Mehrwertsteuercode verwendet wird.
        - Feld **Steuerbasis (Verkauf)**, das verwendet wird, um den Gesamtbarverkaufsbetrag für den Mehrwertsteuercode des Belegs zu drucken. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
        - Feld **Steuerbetrag (Verkauf)**, das verwendet wird, um den Steuerbetrag für Barverkäufe des Belegs für den Mehrwertsteuercode zu drucken.
        - Feld **Steuereinzelhandels-Druckcode**, das verwendet wird, um den abgekürzten Code zu drucken, der dem Mehrwertsteuercode entspricht.

    - Feld **QR-Code**, das verwendet wird, um den Verweis auf die erfasste Bargeldbuchung in der Form eines QR-Codes zu drucken.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Einrichten und Entwerfen von Bonformaten](../receipt-templates-printing.md).

### <a name="configure-fiscal-integration"></a>Steuerintegration konfigurieren

Schließen Sie die Schritte zur Einrichtung der steuerlichen Integration ab, wie unter [Einrichtung der steuerlichen Integration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) beschrieben:

- [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Beachten Sie auch die Einstellungen für den Steuererfassungsprozess, die [für dieses Steuererfassungsdienst-Integrationsbeispiel spezifisch sind](#set-up-the-registration-process).
- [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
- [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

## <a name="deployment-guidelines-for-cash-registers-for-austria"></a>Bereitstellungsrichtlinien für Kassen für Österreich

Das Steuererfassungsdienst-Integrationsbeispiel für Österreich ist Teil des Retail SDK. Informationen zur Installation und Verwendung des SDK finden Sie in der [Retail Software Development Kit (SDK)-Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Dieses Beispiel besteht aus Erweiterungen für CRT, Hardwarestation und POS. Um dieses Beispiel auszuführen, müssen Sie CRT, Hardwarestation und POS-Projekte ändern und erstellen. Es wird empfohlen, dass Sie ein unverändertes Retail SDK verwenden, um die Änderungen vorzunehmen, die in diesem Thema beschrieben werden. Es wird außerdem empfohlen, dass Sie ein Quellsteuerungssystem verwenden, wie Azure DevOps, bei dem noch keine Dateien geändert wurden.

Gehen Sie folgendermaßen vor, um eine Entwicklungsumgebung einzurichten, damit Sie das Beispiel testen und erweitern können.

### <a name="enable-commerce-runtime-extensions"></a>Commerce-Laufzeiterweiterungen aktivieren

Die CRT-Erweiterungskomponenten sind in den CRT-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die CRT-Lösung, **CommerceRuntimeSamples.sln**, unter **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample-Komponente

1. Suchen Sie das Projekt **Runtime.Extensions.DocumentProvider.EFRSample**, und erstellen Sie es.
2. Im Ordner **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** suchen Sie die Assembly-Datei **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Kopieren Sie die Assemblydatei in den CRT-Erweiterungsordner:

    - **Commerce-Skalierungseinheit:** Kopieren Sie die Assembly in den Ordner **\\bin\\ext** unter dem Microsoft Internet Information Services (IIS) Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT i Modern POS:** Kopieren Sie die Assembly in den Ordner **\\ext** unter dem lokalen CRT-Clientbroker-Speicherort.

4. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

5. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

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

#### <a name="update-extension-configuration-file"></a>Erweiterungskonfigurationsdatei aktualisieren

1. Suchen Sie die Erweiterungskonfigurationsdatei für CRT:

    - **Commerce-Skalierungseinheit:** Die Datei hat den Namen **commerceruntime.ext.config**, und sie befindet sich im Ordner **bin\\ext** unter dem IIS Commerce-Skalierungseinheit-Websitespeicherort.
    - **Lokales CRT in Modern POS:** Die Datei hat den Namen **CommerceRuntime.MPOSOffline.Ext.config**, und sie befindet sich unter dem lokalen CRT-Clientbroker-Speicherort.

2. Erfassen Sie die CRT-Änderung in der Erweiterungskonfigurationsdatei.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-hardware-station-extensions"></a>Hardware station-Erweiterungen aktivieren

Die Hardware station-Erweiterungskomponenten sind in den Hardware station-Beispielen enthalten. Um die folgenden Prozeduren abzuschließen, öffnen Sie die Lösung, **HardwareStationSamples.sln.sln**, unter **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample-Komponente

1. Suchen Sie das Projekt **HardwareStation.Extension.EFRSample**, und erstellen Sie es.
2. Im Ordner **Extension.EFRSample\\bin\\Debug** suchen Sie folgende Dateien:

    - Die **Contoso.Commerce.HardwareStation.EFRSample.dll**-Assembly
    - Die **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**-Assembly

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

### <a name="enable-modern-pos-extension-components"></a>Modern POS-Erweiterungskomponenten aktivieren

1. Öffnen Sie die Lösung unter **RetailSdk\\POS\\ModernPOS.sln**, und stellen Sie sicher, dass sie fehlerfrei kompiliert werden kann. Außerdem stellen Sie sicher, dass Sie Modern POS von Microsoft Visual Studio aus ausführen können, indem Sie den Befehl **Run** verwenden.

    > [!NOTE]
    > Modern POS darf nicht angepasst werden. Sie müssen die Benutzerkontensteuerung (UAC) aktivieren, und Sie müssen zuvor installierte Instanzen von Modern POS bei Bedarf deinstallieren.

2. Aktivieren Sie das Laden der Instanzen, indem Sie die folgenden Zeilen in **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

3. Erstellen Sie die Lösung neu.
4. Führen Sie Modern POS im Debugger aus, und testen Sie die Funktionen.

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS-Erweiterungskomponenten aktivieren

1. Öffnen Sie die Lösung unter **RetailSdk\\POS\\CloudPOS.sln**, und stellen Sie sicher, dass sie fehlerfrei kompiliert werden kann.
2. Aktivieren Sie das Laden der Instanzen, indem Sie die folgenden Zeilen in **extensions.json** hinzufügen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Weitere Informationen und Beispiele, die zeigen, wie Quellcodeordner einbezogen werden und das Laden von Erweiterungen ermöglicht wird, finden Sie in den Anleitungen in der readme.md-Datei im Projekt **Pos.Extensions**.

3. Erstellen Sie die Lösung neu.
4. Führen Sie Lösung aus, indem Sie den Befehl **Run** verwenden, und folgen Sie den Schritten im Retail SDK-Handbuch.

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Erfassungsprozess zu aktivieren, führen Sie diese Schritte aus, um die Zentralverwaltung einzurichten. Weitere Einzelheiten finden Sie unter [Steuerliche Integration für Commerce-Kanäle einrichten](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
2. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektoren**, und laden Sie die Konnektorkonfiguration. Der Dateispeicherort ist **RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml**.
3. Wechseln Sie zu **Retail and Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerdokumentanbieter**, und laden Sie die Dokumentanbieterkonfigurationen. Die Konfigurationsdateien befinden sich unter **RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration**:

    - DocumentProviderEFRSampleAustria.xml
    - DocumentProviderNonFiscalEFRSampleAustria.xml

4. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie zwei Konnektorfunktionsprofile, eines für jeden Dokumentanbieter, den Sie zuvor geladen haben, und wählen Sie den Konnektor aus, den Sie zuvor geladen haben. Aktualisieren Sie die Datenzuordnungseinstellungen nach Bedarf.
5. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Konnektorprofil, und wählen Sie den Konnektor aus, den Sie vorher geladen haben. Aktualisieren Sie die Verbindungseinstellungen nach Bedarf.
6. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**. Erstellen Sie zwei neue Steuerkonnektorgruppen, eine für jedes Konnektorfunktionsprofil, das Sie vorher erstellt haben.
7. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Steuererfassungsprozess, zwei Steuererfassungsprozess-Schritte, und wählen Sie die Steuerkonnektorgruppen aus, die Sie vorher erstellt haben.
8. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben. Um die Erfassung von nicht-steuerlichen Ereignisse im POS zu ermöglichen, legen Sie im Inforegister **Funktionen** unter **POS** die Option **Überwachen** auf **Ja** fest.
9. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**. Wählen Sie ein Hardwareprofil aus, das mit der Hardware station verknüpft ist, mit der der Belegdrucker verbunden wird. Im Inforegister **Peripheriegeräte für die Steuerverwaltung** aktivieren Sie das technische Konnektorprofil, das Sie vorher erstellt haben.
10. Öffnen Sie den Vertriebsplan (**Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**), und wählen Sie Jobs **1070** und **1090** aus, um Daten zur Kanaldatenbank zu übertragen.

### <a name="production-environment"></a>Produktionsumgebung

Die vorherige Prozedur aktiviert die Erweiterungen, die Komponenten des Steuererfassungsdienst-Integrationsbeispiels sind. Darüber hinaus müssen Sie diese Schritte ausführen, um bereitstellbare Pakete zu erstellen, die Commerce-Komponenten enthalten, und diese Pakete in einer Produktionsumgebung anzuwenden.

1. Nehmen Sie die folgenden Änderungen in den Paketkonfigurationsdateien unter dem Ordner **RetailSdk\\Assets** vor:

    - In den Konfigurationsdateien **commerceruntime.ext.config** und **CommerceRuntime.MPOSOffline.Ext.config** fügen Sie die folgenden Positionen zum Abschnitt **Anordnung** hinzu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - In der Konfigurationsdatei **HardwareStation.Extension.config** fügen Sie die folgende Position dem Abschnitt **Anordnung** hinzu.

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

    - Fügen Sie die folgende Zeilen hinzu, um die Hardware station-Erweiterung in die bereitstellbaren Pakete einzuschließen.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Starten Sie die MSBuild-Eingabeaufforderung für Visual Studio-Hilfsprogramm und führen Sie **msbuild** unter dem Ordner Retail SDK aus, um bereitstellbare Pakete zu erstellen.
4. Übernehmen Sie die Pakete über Microsoft Dynamics Lifecycle Services (LCS) oder manuell. Weitere Informationen finden Sie unter [Bereitstellbare Pakete erstellen](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Schließen Sie alle erforderlichen Setupaufgaben ab, die im Abschnitt [Commerce für Österreich einrichten](#set-up-commerce-for-austria) beschrieben sind.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

Die CRT-Erweiterung ist **Runtime.Extensions.DocumentProvider.EFRSample**.

Weitere Einzelheiten über das Design der Lösung für die steuerliche Integration finden Sie unter [Überblick über die steuerliche Integration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Anforderungshandler

Es gibt zwei Anforderungshandler für Dokumentanbieter:

- **DocumentProviderEFRFiscalAUT** – Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.
- **DocumentProviderEFRNonFiscalAUT** – Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.

Diese Handler werden von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetNonFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches nicht-steuerliche Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Aktuell werden die folgenden Ereignisse unterstützt: Vertrieb, Drucken von X-Bericht, Drucken von Z-Bericht, Debitorenkonto-Einzahlungen, Debitorenauftragseinzahlungen, Überwachungsereignisse und Nicht-Vertriebsbuchungen.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Diese Anforderung gibt die Antwort vom Steuererfassungsdienst zurück. Diese Antwort wird serialisiert, um eine Zeichenfolge zu bilden, sodass sie bereit zum Speichern ist.

#### <a name="configuration"></a>Variante

Die Konfigurationsdateien befinden sich im Ordner **Konfiguration** des Erweiterungsprojekts:

- **DocumentProviderFiscalEFRSampleAustria** – Für Steuerdokumente.
- **DocumentProviderNonFiscalEFRSampleAustria** – Für nicht-steuerliche Dokumente.

Der Zweck dieser Dateien ist es, Einstellungen zu aktivieren, damit der Dokumentanbieter von der Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgende Einstellung wird hinzugefügt:

- Zuordnung von MwSt.-Sätzen

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuererfassungsdienst.

Die Hardware station-Erweiterung ist **HardwareStation.Extension.EFRSample**. Die Hardwarestation-Erweiterung verwendet das HTTP-Protokoll, um Dokumente, die die CRT-Erweiterung generiert, zum Steuererfassungsdienst zu übermitteln. Sie handhabt auch die Antworten, die vom Steuererfassungsdienst empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EFRHandler** ist der Einstiegspunkt für die Handhabung von Anforderungen an den Steuererfassungsdienst.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Steuererfassungsdienst und gibt eine Antwort von ihm zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsdiensts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Steuererfassungsdiensts verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **Konfiguration** des Erweiterungsprojekts. Der Zweck dieser Datei ist es, Einstellungen zu aktivieren, damit der Steuerkonnektor von der Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Zeitlimit** – Die Zeitdauer in Millisekunden, die der Treiber auf eine Antwort vom Steuererfassungsdienst wartet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]