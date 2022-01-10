---
title: Integrationsbeispiel für Steuererfassungsdienst für Deutschland
description: In diesem Thema erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Deutschland in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: ca747215a8dfb85237365880ad5bdd49e57ec949
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944687"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Integrationsbeispiel für Steuererfassungsdienst für Deutschland

[!include[banner](../includes/banner.md)]

In diesem Thema erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Deutschland in Microsoft Dynamics 365 Commerce.

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

        Sicherheitsdaten werden von einer TSE als Teil einer Antwort empfangen und in der Transaktion in der Kanaldatenbank gespeichert. Die Sicherheitsdaten bestehen aus den folgenden Informationen:

        - TID
        - Das Datum und die Zeit des Transaktionsstarts
        - Das Datum und die Zeit des Transaktionsende
        - Signaturzähler
        - Wert prüfen
        - Seriennummer der TSE

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

Vorschriften in Deutschland erfordern Unterstützung für den DSFinV-K-Export. Der DSFinV-K-Export kann in der EFR-Lösung ausgelöst werden. Weitere Informationen zum DSFinV-K-Export finden Sie im EFR-Handbuch \[DE\]-Dokument, das auf der Website [EFSTA-Dokumentation](https://public.efsta.net/efr/) veröffentlicht wird.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

Der Steuererfassungsdienst unterstützt nur Szenarien, bei denen die Mehrwertsteuer in den Preisen enthalten sind. Daher muss die Option **Preise in Mehrwertsteuer enthalten** auf **Ja** sowohl für Geschäfte als auch Debitoren festgelegt werden.

Der Finanzdienst unterstützt keine Situationen, in denen mehr als ein Umsatzsteuerkennzeichen auf dieselbe Transaktionszeile angewendet wird.

Das Rahmenwerk für die steuerliche Integration unterstützt keine Angebote. Daher sind diese Vorgänge nicht im Finanzdienst registriert.

## <a name="set-up-commerce-for-germany"></a>Commerce für Deutschland einrichten

In diesem Abschnitt werden die Commerce-Einstellungen beschrieben, die für Deutschland spezifisch und empfohlen sind. Weitere Informationen für das Einrichten finden Sie unter [Commerce-Homepage](../index.md).

Um die Deutschland-spezifischen Funktionen zu verwenden, müssen Sie die folgenden Einstellungen angeben.

- Legen Sie in der primären Adresse der juristischen Person das Feld **Land/Region** auf **DEU** (Deutschland) fest.
- Legen Sie im POS-Funktionsprofil jedes einzelnen Einzelhandelsgeschäfts in Deutschland das Feld **ISO-Code** auf **DE** (Deutschland) fest.

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

> [!NOTE]
> Es ist wichtig, dass Sie die richtigen benutzerdefinierten Feldnamen angeben, wie in der vorherigen Tabelle aufgeführt. Ein falscher benutzerdefinierter Feldname führt zu fehlenden Daten in Belegen.

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
    - Felder in der **Steueraufschlüsselung** Feldgruppe. Alle Felder in dieser Feldgruppe müssen in einer separaten Position gedruckt werden.

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

        > [!NOTE]
        > Der **QR-Code** Wert wird aus der Antwort des Finanzregisters abgerufen. EFR gibt nur dann einen QR-Code in seiner Antwort zurück, wenn der Wert des Felds **Attribute** in der EFR-Konfiguration in der EFSTA-Dokumentation beschrieben ist. Das QR-Code-Format im **Attribut** Feld in der EFR-Konfiguration muss auf **BMP** festgelegt werden.

    - Das Feld **Info Nachricht** auf den Belegen zeigt eine Benachrichtigungsnachricht des Steuerregistrierungsdienstes. Wenn beispielsweise ein Signaturgerät defekt ist, kann ein spezieller Text auf eine Quittung gedruckt werden.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Einrichten und Entwerfen von Bonformaten](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Steuerintegration für Deutschland einrichten

Die Beispiele für diese steuerliche Integration für Deutschland basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil der Retail SDK. Die Probe befindet sich im Ordner **src\\Fiscallntegration\\Efr** des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [die Stichprobe in Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung der Commerce Runtime (CRT) ist, und einem fiskalischen Konnektor, der eine Erweiterung der Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die vorherige Version des Retail SDK auf einer virtuellen Maschine (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Deutschland (Legacy)](emea-deu-fi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

Schließen Sie die Schritte zur Einrichtung der steuerlichen Integration ab, wie unter [Einrichtung der steuerlichen Integration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) beschrieben:

1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Beachten Sie auch die Einstellungen für den Steuererfassungsprozess, die [für dieses Steuererfassungsdienst-Integrationsbeispiel spezifisch sind](#set-up-the-registration-process).
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Die Fehlerbehandlungsfunktionen des Rahmens für die steuerliche Integration sind möglicherweise nicht vollständig an die lokalen steuerlichen Vorschriften angepasst.
    >
    > - Wir empfehlen Ihnen, die Option **Fahren Sie mit dem Fehler fort** auf der **Steuerlicher Registrierungsprozess** zu verlassen, da alle Transaktionen korrekt registriert werden müssen, auch wenn der erste Versuch der Steuerregistrierung nicht erfolgreich war.
    > - Bevor Sie die Option **Überspringen** oder **Als registriert markieren** auf der Seite **Steuerlicher Registrierungsprozess** aktivieren, sollten Sie diese Änderungen des Steuerregistrierungsprozesses mit Ihrem Steuerberater oder dem örtlichen Finanzamt besprechen.

1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanal-Komponenten konfigurieren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Registrierungsprozess zu aktivieren, folgen Sie diesen Schritten, um die Commerce-Zentrale festzulegen. Weitere Informationen finden Sie unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Wählen Sie eine korrekte Version des Release Branches entsprechend Ihrer SDK-/Anwendungsversion (zum Beispiel **[Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Öffnen Sie **src \> FiscalIntegration \> Efr**.
    1. Laden Sie die Konfigurationsdatei des Steuerdokumentanbieters herunter unter **Konfigurationen \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (zum Beispiel, [die Datei für die Freigabe/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Laden Sie die Konnektor-Konfigurationsdatei des Fiskaldokumentanbieters herunter unter **Konfigurationen \> Konnektoren \> KonnektorEFRSample.xm.** (zum Beispiel, [die Datei für die Freigabe/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Die Konfigurationsdateien für dieses Beispiel zur Fiskalintegration befinden sich in den folgenden Ordnern des Retail SDK auf einer Entwickler-VM in LCS:
    >
    > - **Steuerdokument-Konfigurationsdatei-Anbieter:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
    > - **Steuer-Konnektr Konfigurationsdatei:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
1. Gehen Sie zu **Handel und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Belege**, und laden Sie die Konfigurationsdatei des Fiskalischen Belegs, die Sie zuvor heruntergeladen haben.
1. Gehen Sie zu **Retail und Commerce \> Channel Einrichtung \> Fiskalische Integration \> Fiskalische Konnektoren**, und laden Sie die Konfigurationsdatei für den Fiskalischen Konnektor, die Sie zuvor heruntergeladen haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie ein neues funktionales Profil für den Konnektor. Wählen Sie den Beleg-Anbieter und den Konnektor, den Sie zuvor geladen haben. Aktualisieren Sie die [Einstellungen für die Datenzuordnung](#default-data-mapping) nach Bedarf.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Profil für den Konnektor und wählen Sie den Fiskalkonnektor, den Sie zuvor erstellt haben. Aktualisieren Sie die [Konnektor-Einstellungen](#fiscal-connector-settings) nach Bedarf.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**. Erstellen Sie eine neue Steuerkonnektorgruppen für das funktionale Konnektorfunktionsprofil, das Sie vorher erstellt haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Fiskalregistrierungsprozess und einen Fiskalregistrierungsprozessschritt und wählen Sie die Fiskalkonnektorgruppe, die Sie zuvor erstellt haben.
1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**. Wählen Sie ein Hardwareprofil aus, das mit der Hardware station verknüpft ist, mit der der Belegdrucker verbunden wird. Im Inforegister **Peripheriegeräte für die Steuerverwaltung** aktivieren Sie das technische Konnektorprofil, das Sie vorher erstellt haben.
1. Öffnen Sie den Vertriebsplan (**Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**), und wählen Sie Jobs **1070** und **1090** aus, um Daten zur Kanaldatenbank zu übertragen.

#### <a name="default-data-mapping"></a>Standarddatenzuordnung

Die folgende Standarddatenzuordnung ist in der Steuerbeleganbieter-Konfiguration enthalten, die als Teil des Steuerintegrationsbeispiels bereitgestellt wird:

- **Ausschreibungstypzuordnung** – Die Zuordnung von Zahlungsmethoden zu Werten der **PayG** Attribute (Zahlungsgruppe) in Anforderungen, die an den Finanzdienst gesendet werden. Hier ist die Standardzuordnung:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Die erste Komponente in jedem Paar steht für eine Zahlungsmethode, die für den Store festgelegt ist. Die zweite Komponente stellt die entsprechende Zahlungsgruppe dar, die vom EFR-Steuerregistrierungsdienst unterstützt wird. Weitere Informationen zu Zahlungsgruppen, die EFR für Deutschland unterstützt, finden Sie unter [EFR-Referenz](https://public.efsta.net/efr/).

    Die Musterzuordnung von Zahlarten entspricht den Filialzahlarten, die in den Standard-Demodaten konfiguriert sind.

    | Zahlungsweise | Name der Zahlungsmethode |
    |----------------|---------------------|
    | 1              | Bargeld                |
    | 2              | Überprüfen               |
    | 3              | Karte                |
    | 4              | Debitorenkonto    |
    | 5              | Sonstige               |
    | 6              | Währung            |
    | 7              | Beleg             |
    | 8              | Geschenkkarte           |
    | 9              | Zahlungsmittel entfernen/Wechselgeld |
    | 10             | Treuekarten       |
    | 11             | Nicht-lokale Kontrollen    |

    Daher müssen Sie die Musterzuordnung entsprechend den Zahlungsmethoden ändern, die in Ihrer Anwendung konfiguriert sind.

- **Kundendaten einschließen** – Wenn dieser Parameter aktiviert ist, enthalten Anfragen an den Finanzdienst Kundeninformationen wie Namen und Adressen, wenn ein Kunde zu einer Transaktion hinzugefügt wird.
- **Zuordnung der Mehrwertsteuersätze (MwSt)** – Die Zuordnung von Steuerprozentsatzwerten, die für die Umsatzsteuerkennzeichen eingerichtet wurden, zu Werten der **TaxG** Attribute (Steuergruppe) in Anforderungen, die an den Finanzdienst gesendet werden. Hier ist die Standardzuordnung:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Die erste Komponente in jedem Paar stellt die entsprechende MwSt-Zahlungsgruppe dar, die vom EFR-Steuerregistrierungsdienst unterstützt wird. Die zweite Komponente stellt den entsprechenden Mehrwertsteuersatz dar. Weitere Informationen zu MwSt-Steuergruppen, die EFR für Deutschland unterstützt, finden Sie unter [EFR-Referenz](https://public.efsta.net/efr/).

- **Steuergruppe für Geschenkkarten und Einzahlungen** – Der Wert der **TaxG** Attribut in Anfragen, die an den Finanzdienst gesendet werden, basierend auf Vorgängen, die Geschenkkarten oder Einzahlungen beinhalten. Hier ist die Standardzuordnung:

    ```
    G
    ```

- **Steuergruppe für Mehrwertsteuer befreit** – Der Wert der **TaxG** Attribute in Anforderungen, die an den Finanzdienst gesendet werden, basierend auf Vorgängen, die von steuerlichen Verpflichtungen befreit sind. Hier ist die Standardzuordnung:

    ```
    F
    ```

> [!NOTE]
> Die Steuereinstellungen in der Standarddatenzuordnung sind für die Übereinstimmung der Steuereinstellungen im System und der Steuergruppen im EFR-Dienst verantwortlich. Steuergruppen können nur dann auf Quittungen gedruckt werden, wenn das Feld **Code zum Drucken** auf der Seite **Umsatzsteuerkennzeichen** festgelegt ist.

#### <a name="fiscal-connector-settings"></a>Konnektor-Einstellungen für Steuern

Die folgenden Einstellungen sind in der Konfiguration des Fiskalkonnektors enthalten, die als Teil des Beispiels für die Fiskalintegration bereitgestellt wird:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Zeitlimit** – Die Zeitdauer in Millisekunden (ms), die der Steuerkonnetor auf eine Antwort vom Steuererfassungsdienst wartet.
- **Benachrichtigungen zur Steuerregistrierung anzeigen** – Dieses Flag steuert, ob dem Operator Benachrichtigungen angezeigt werden sollen, dass der Steuerregistrierungsservice zurückkehrt.

### <a name="configure-channel-components"></a>Kanal-Komponenten konfigurieren

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Deutschland (Legacy)](emea-deu-fi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

#### <a name="set-up-the-development-environment"></a>Die Umgebung für die Entwicklung festlegen

Um eine Entwicklungsumgebung zum Testen und Erweitern des Beispiels festzulegen, gehen Sie wie folgt vor.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Retail SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Öffnen Sie die EFR-Lösung unter **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, und bauen Sie es auf.
1. Commerce Runtime Erweiterungen installieren:

    1. Suchen Sie das Installationsprogramm für die Erweiterung CRT:

        - **Commerce Scale Unit:** Im **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\Behälter\\Debuggen\\net461** Ordner, finden Sie das **ScaleUnit.EFR.Installer** Installationsprogramm.
        - **Lokal CRT in Modern POS:** Im **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\Behälter\\Debuggen\\net461** Ordner, finden Sie das **ModernPOS.EFR.Installer** Installationsprogramm.

    1. Starten Sie das Installationsprogramm für die CRT-Erweiterung über die Befehlszeile:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT auf Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installieren Sie die Hardware Station Extensions:

    - In **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\Behälter\\Debuggen\\net461** Ordner finden Sie das **HardwareStation.EFR.Installer** Installationsprogramm.
    - Starten Sie das Installationsprogramm für die Erweiterung über die Befehlszeile:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **EFR Build-pipeline.yml** Vorlagen-YAML-Datei finden Sie im **Pipeline\\YAML_Files** Ordner des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Die Beispiele für diese steuerliche Integration für Deutschland basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil der Retail SDK. Die Probe befindet sich im Ordner **src\\Fiscallntegration\\Efr** des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [die Stichprobe in Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung von CRT ist, und einem fiskalischen Konnektor, der eine Erweiterung von Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Deutschland (Legacy)](emea-deu-fi-sample-sdk.md). Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

### <a name="crt-extension-design"></a>CRT Erweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

#### <a name="request-handler"></a>Anforderungshandler

Es gibt einen Anforderungshandler für den Dokumentanbieter: **DocumentProviderEFRFiscalDEU**. Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen. Er wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Diese Anfrage gibt die Antwort zusammen mit erweiterten Daten zurück.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Steuerdokumenten befindet sich unter **src\\FiscalIntegration\\Efr\\Konfigurationen\\Dokumentenanbieter\\DocumentProviderFiscalEFRSampleGermany.xml** in dem [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Mit dieser Datei können Sie die Einstellungen des Anbieters von Fiskalbelegen von der Commerce-Zentrale aus festlegen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

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

Die Konfigurationsdatei für den Anbieter von Steuerkonnektoren befindet sich unter **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** in dem [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen des Fiskalkonnektors von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
