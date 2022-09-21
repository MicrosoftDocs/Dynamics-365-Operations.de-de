---
title: Beispiel für Integration des Steuererfassungsdienstes in Österreich
description: In diesem Artikel erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Österreich in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: f3429df2732d7d1ed6d2f0783a600c2b994c022b
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473876"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Beispiel für Integration des Steuererfassungsdienstes in Österreich

[!include [banner](../includes/banner.md)]

In diesem Artikel erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Österreich in Microsoft Dynamics 365 Commerce.

Um die lokalen steuerlichen Anforderungen für Kassen in Österreich zu erfüllen, umfassen die Dynamics 365 Retail-Funktionen für Österreich eine Beispielintegration der Verkaufsstelle (POS) in einen externen Steuerregistrierungsservice. Das Beispiel erweitert die [steuerliche Integrationsfunktionen](fiscal-integration-for-retail-channel.md). Es basiert auf der [EFR (Electronisches Fiskalregister)](https://www.efsta.eu/at/fiskalloesungen/oesterreich)-Lösung von [EFSTA](https://www.efsta.eu/at/) und ermöglicht die Kommunikation mit dem EFR-Service über das HTTPS-Protokoll. Der EFR-Dienst sollte entweder in der Retail Hardware station oder auf einem separaten Computer gehostet werden, zu dem von der Hardare station aus eine Verbindung hergestellt werden kann. Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Commerce Software Development Kit (SDK).

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

In diesem Abschnitt werden die Commerce-Einstellungen beschrieben, die für Österreich spezifisch und empfohlen sind. Weitere Informationen zur Einrichtung finden Sie unter [Commerce Homepage](../index.md).

Um die Österreich-spezifischen Funktionen zu verwenden, müssen Sie die folgenden Einstellungen angeben:

- Legen Sie in der primären Adresse der juristischen Person das Feld **Land/Region** auf **AUT** (Österreich) fest.
- Legen Sie im POS-Funktionsprofil jedes einzelnen Einzelhandelsgeschäfts in Österreich das Feld **ISO-Code** auf **AT** (Österreich) fest.

Sie müssen auch die folgenden Einstellungen für Österreich angeben. Beachten Sie, dass Sie entsprechende Verteilungseinzelvorgänge ausführen müssen, nachdem Sie die Einrichtung abschließen.

### <a name="enable-features-for-austria"></a>Funktionen für Österreiche aktivieren

Sie müssen im Arbeitsbereich **Funktionsverwaltung** die folgenden Funktionen aktivieren:

- (Österreich) Zusätzliche Überwachungsereignisse in POS aktivieren
- (Österreich) Zusätzliche Informationen in Tagesendauszügen in POS aktivieren

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

> [!NOTE]
> Es ist wichtig, dass Sie die richtigen benutzerdefinierten Feldnamen angeben, wie in der vorherigen Tabelle aufgeführt. Ein falscher benutzerdefinierter Feldname führt zu fehlenden Daten in Belegen.

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

    - **Steueraufschlüsselung**-Feldgruppe. Alle Felder in dieser Feldgruppe müssen in einer separaten Position gedruckt werden.

        - Feld **Steuerkennung**, das ein Standardfeld ist, das den Druck einer Mehrwertsteuerzusammenfassung für jeden Mehrwertsteuercode aktiviert. Das Feld muss einer neuen Position hinzugefügt werden.
        - **Steuerprozentsatz**-Feld, das ein Standardfeld ist, das zum Drucken des tatsächlichen Steuersatzes für den Mehrwertsteuercode verwendet wird.
        - Feld **Steuerbasis (Verkauf)**, das verwendet wird, um den Gesamtbarverkaufsbetrag für den Mehrwertsteuercode des Belegs zu drucken. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
        - Feld **Steuerbetrag (Verkauf)**, das verwendet wird, um den Steuerbetrag für Barverkäufe des Belegs für den Mehrwertsteuercode zu drucken.
        - Feld **Steuereinzelhandels-Druckcode**, das verwendet wird, um den abgekürzten Code zu drucken, der dem Mehrwertsteuercode entspricht.

    - Feld **QR-Code**, das verwendet wird, um den Verweis auf die erfasste Bargeldbuchung in der Form eines QR-Codes zu drucken.

        > [!NOTE]
        > Der **QR-Code** Wert wird aus der Antwort des Finanzregisters abgerufen. EFR gibt nur dann einen QR-Code in seiner Antwort zurück, wenn der Wert des Felds **Attribute** in der EFR-Konfiguration in der EFSTA-Dokumentation beschrieben ist. Das QR-Code-Format im **Attribut** Feld in der EFR-Konfiguration muss auf **BMP** festgelegt werden.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Einrichten und Entwerfen von Bonformaten](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Steuerintegration für Österreich einrichten

Die Beispiele für diese Steuerintegration für Österreich basiert auf der [Funktion zur Steuerintegration](fiscal-integration-for-retail-channel.md) und ist Teil der Commerce SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\Efr** des Respository [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Das [Beispiel](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) besteht aus einem Anbieter von Steuerbelegen, der eine Erweiterung der Commerce Runtime (CRT) ist, und einem Steuerconnector, der eine Erweiterung der Commerce Hardwarestation ist. Weitere Informationen zur Verwendung des Commerce SDK finden Sie unter [Laden Sie Beispiele und Referenzpakete für das Retail SDK von GitHub und NuGet herunter](../dev-itpro/retail-sdk/sdk-github.md) und [Buildpipeline für das unabhängige Verpackungs-SDK einrichten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Das Beispiel für die Integration des Steuerregistrierungsdienstes für Österreich ist im Commerce SDK ab Commerce-Version 10.0.29 verfügbar. In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf einem virtuellen Computer (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Österreich (Legacy)](emea-aut-fi-sample-sdk.md).

Schließen Sie die Schritte zur Einrichtung der steuerlichen Integration ab, wie unter [Einrichtung der steuerlichen Integration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) beschrieben:

1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Beachten Sie auch die Einstellungen für den Steuererfassungsprozess, die [für dieses Steuererfassungsdienst-Integrationsbeispiel spezifisch sind](#set-up-the-registration-process).
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurieren Sie die Channel-Komponenten](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Registrierungsprozess zu aktivieren, folgen Sie diesen Schritten, um die Commerce-Zentrale festzulegen. Weitere Informationen finden Sie unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion.
    1. Öffnen Sie **src \> FiscalIntegration \> Efr**.
    1. Öffnen Sie **Konfigurationen \> DocumentProviders** und laden Sie die Konfigurationsdateien für den Steuerbeleganbieter herunter: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Laden Sie die Laden Sie die Konfigurationsdatei für den Steuerconnector unter **Konfigurationen \> Connectors \> ConnectorEFRSample.xml** herunter.

    > [!NOTE]
    > In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf VM für Entwickler in LCS verwenden. Die Konfigurationsdateien für dieses Beispiel zur Fiskalintegration befinden sich in den folgenden Ordnern des Retail SDK auf einer Entwickler-VM in LCS:
    >
    > - **Steuerdokument-Anbieterkonfigurationsdateien:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Config
    > - **Steuer-Konnektr Konfigurationsdatei:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Konfiguration

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
1. Wechseln Sie zu **Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerdokumentanbieter**, und laden Sie die Steuer-Dokumentanbieterkonfigurationen, die Sie zuvor heruntergeladen haben.
1. Gehen Sie zu **Retail und Commerce \> Channel Einrichtung \> Fiskalische Integration \> Fiskalische Konnektoren**, und laden Sie die Konfigurationsdatei für den Fiskalischen Konnektor, die Sie zuvor heruntergeladen haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie zwei Konnektorfunktionsprofile, eines für jeden Steuer-Dokumentanbieter, den Sie zuvor geladen haben, und wählen Sie den Steuer-Konnektor aus, den Sie zuvor geladen haben. Aktualisieren Sie die [Einstellungen für die Datenzuordnung](#default-data-mapping) nach Bedarf.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Profil für den Konnektor und wählen Sie den Fiskalkonnektor, den Sie zuvor erstellt haben. Aktualisieren Sie die [Konnektor-Einstellungen](#fiscal-connector-settings) nach Bedarf.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**. Erstellen Sie zwei neue Steuerkonnektorgruppen, eine für jedes Konnektorfunktionsprofil, das Sie vorher erstellt haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Steuererfassungsprozess und zwei Steuererfassungsprozess-Schritte, und wählen Sie die Steuerkonnektorgruppen aus, die Sie vorher erstellt haben.
1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben. Um die Erfassung von nicht-steuerlichen Ereignisse im POS zu ermöglichen, legen Sie im Inforegister **Funktionen** unter **POS** die Option **Überwachen** auf **Ja** fest.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**. Wählen Sie ein Hardwareprofil aus, das mit der Hardwarestation verknüpft ist, mit der der Steuerregistrierungsdienst verbunden wird. Im Inforegister **Peripheriegeräte für die Steuerverwaltung** aktivieren Sie das technische Konnektorprofil, das Sie vorher erstellt haben.
1. Öffnen Sie den Vertriebsplan (**Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**), und wählen Sie Jobs **1070** und **1090** aus, um Daten zur Kanaldatenbank zu übertragen.

#### <a name="default-data-mapping"></a>Standarddatenzuordnung

Die folgende Standarddatenzuordnung ist in der Steuerbeleganbieter-Konfiguration enthalten, die als Teil des Steuerintegrationsbeispiels bereitgestellt wird:

- **Zuordnung der Mehrwertsteuersätze (MwSt)** – Die Zuordnung von Steuerprozentsatzwerten, die für die Umsatzsteuerkennzeichen eingerichtet wurden, zu Werten der **TaxG** Attribute (Steuergruppe) in Anforderungen, die an den Finanzdienst gesendet werden. Hier ist die Standardzuordnung:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Die erste Komponente in jedem Paar stellt die entsprechende MwSt-Zahlungsgruppe dar, die vom EFR-Steuerregistrierungsdienst unterstützt wird. Die zweite Komponente stellt den entsprechenden Mehrwertsteuersatz dar. Weitere Informationen zu MwSt-Steuergruppen, die EFR für Österreich unterstützt, finden Sie unter [EFR-Referenz](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Konnektor-Einstellungen für Steuern

Die folgenden Einstellungen sind in der Konfiguration des Fiskalkonnektors enthalten, die als Teil des Beispiels für die Fiskalintegration bereitgestellt wird:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Geräte-Timeout** – Die Zeitdauer in Millisekunden (ms), die der Steuerkonnetor auf eine Antwort vom Steuererfassungsdienst wartet.
- **Benachrichtigungen zur Steuerregistrierung anzeigen** – Dieses Flag steuert, ob dem Operator Benachrichtigungen angezeigt werden sollen, dass der Steuerregistrierungsservice zurückkehrt.

### <a name="configure-channel-components"></a>Konfigurieren Sie die Channel-Komponenten

> [!NOTE]
> - Das Beispiel für die Integration des Steuerregistrierungsdienstes für Österreich ist im Commerce SDK ab Commerce-Version 10.0.29 verfügbar. In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf VM für Entwickler in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Österreich (Legacy)](emea-aut-fi-sample-sdk.md).
> - Commerce-Beispiele, die in Ihrer Umgebung bereitgestellt werden, werden nicht automatisch aktualisiert, wenn Sie Dienst- oder Qualitätsupdates auf Commerce-Komponenten durchführen. Sie müssen die erforderlichen Beispiele manuell aktualisieren.

#### <a name="set-up-the-development-environment"></a>Die Umgebung für die Entwicklung festlegen

Um eine Entwicklungsumgebung zum Testen und Erweitern des Beispiels festzulegen, gehen Sie wie folgt vor.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Commerce SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Öffnen Sie die EFR-Lösung unter **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, und bauen Sie es auf.
1. Installieren von CRT Erweiterungen:

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

1. Installieren Sie die Erweiterungen des Fiskalkonnektors:

    Sie können fiskalische Konnektor-Erweiterungen auf der [Hardware Station](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) oder dem [POS Register](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) installieren.

    1. Installieren Sie die Hardware Station Extensions:

        1. In **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\Behälter\\Debuggen\\net461** Ordner finden Sie das **HardwareStation.EFR.Installer** Installationsprogramm.
        1. Starten Sie das Installationsprogramm für die Erweiterung von der Befehlszeile aus, indem Sie den folgenden Befehl ausführen.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Installieren Sie die POS-Erweiterungen:

        1. Öffnen Sie die Beispiellösung für den POS Fiscal Konnektor unter **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln**, und erstellen Sie sie.
        1. Im Ordner **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** finden Sie den **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** Installer.
        1. Starten Sie das Installationsprogramm für die Erweiterung von der Kommandozeile aus, indem Sie den folgenden Befehl ausführen.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **EFR Build-pipeline.yml** Vorlagen-YAML-Datei finden Sie im **Pipeline\\YAML_Files** Ordner des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Die Beispiele für diese Steuerintegration für Österreich basiert auf der [Funktion zur Steuerintegration](fiscal-integration-for-retail-channel.md) und ist Teil der Commerce SDK. Das Beispiel befindet sich im Ordner **src\\FiscalIntegration\\Efr** des Respository [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung von CRT ist, und einem fiskalischen Konnektor, der eine Erweiterung von Commerce Hardware Station ist. Weitere Informationen zur Verwendung des Commerce SDK finden Sie unter [Laden Sie Beispiele und Referenzpakete für das Retail SDK von GitHub und NuGet herunter](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Buildpipeline für das unabhängige Verpackungs-SDK einrichten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Das Beispiel für die Integration des Steuerregistrierungsdienstes für Österreich ist im Commerce SDK ab Commerce-Version 10.0.29 verfügbar. In der Commerce Version 10.0.28 oder früher müssen Sie die frühere Version des Retail SDK auf VM für Entwickler in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für Österreich (Legacy)](emea-aut-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf 

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

#### <a name="request-handler"></a>Anforderungshandler

Es gibt zwei Anforderungshandler für Dokumentanbieter:

- **DocumentProviderEFRFiscalAUT** – Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.
- **DocumentProviderEFRNonFiscalAUT** – Dieser Handler wird verwendet, um Steuerdokumente für den Steuererfassungsdienst zu erstellen.

Diese Handler werden von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetNonFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches nicht-steuerliche Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Aktuell werden die folgenden Ereignisse unterstützt: Vertrieb, Drucken von X-Bericht, Drucken von Z-Bericht, Debitorenkonto-Einzahlungen, Debitorenauftragseinzahlungen, Überwachungsereignisse und Nicht-Vertriebsbuchungen.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Diese Anforderung gibt die Antwort vom Steuererfassungsdienst zurück. Diese Antwort wird serialisiert, um eine Zeichenfolge zu bilden, sodass sie bereit zum Speichern ist.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Steuerdokumenten befindet sich im **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** Order im [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository:

- **DocumentProviderFiscalEFRSampleAustria** – Die Konfigurationsdatei für den Steuerdokumentanbeiter für Steuerdokumente.
- **DocumentProviderNonFiscalEFRSampleAustria** – Die Konfigurationsdatei für den Steuerdokumentanbeiter für Steuerdokumente.

Der Zweck dieser Dateien ist es, Einstellungen zu aktivieren, damit der Steuerdokumentanbieter von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Fiskalkonnektor-Erweiterung ist die Kommunikation mit dem Fiskalregistrierungsdienst. Die Erweiterung Hardwarestation verwendet die Protokolle HTTP und HTTPS, um Dokumente, die die Erweiterung CRT erzeugt, an den Fiskalregistrierungsdienst zu senden. Sie handhabt auch die Antworten, die vom Steuererfassungsdienst empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EFRHandler** ist der Einstiegspunkt für die Handhabung von Anforderungen an den Steuererfassungsdienst.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Steuerkonnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Steuererfassungsdienst und gibt eine Antwort von ihm zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsdiensts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Steuererfassungsdiensts verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Steuerkonnektoren befindet sich unter **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** in dem [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen des Fiskalkonnektors von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

### <a name="pos-fiscal-connector-extension-design"></a>Design der POS Fiskalkonnektor-Erweiterung

Der Zweck der POS Fiskalkonnektor-Erweiterung ist die Kommunikation mit dem Fiskalregistrierungsdienst von POS. Sie verwendet das HTTPS-Protokoll für die Kommunikation.

#### <a name="fiscal-connector-factory"></a>Fiscal Konnektor Fabrik

Die Fiskal Connector Fabrik factory ordnet den Namen des Konnektors der Implementierung des Fiskal Connectors zu und befindet sich in der Datei **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Der Name des Konnektors sollte mit dem Namen des steuerlichen Konnektors übereinstimmen, der in der Commerce-Zentrale angegeben ist.

#### <a name="efr-fiscal-connector"></a>EFR Fiskalischer Konnektor

Der EFR-Fiscal-Konnektor befindet sich in der Datei **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Es implementiert die Schnittstelle **IFiscalConnector**, die die folgenden Anfragen unterstützt:

- **FiscalRegisterSubmitDocumentClientRequest** - Diese Anfrage sendet Dokumente an den Fiskalregistrierungsdienst und gibt eine Antwort von ihm zurück.
- **FiscalRegisterIsReadyClientRequest** - Diese Anfrage wird für einen Gesundheitscheck des fiskalischen Registrierungsdienstes verwendet.
- **FiscalRegisterInitializeClientRequest** - Diese Anfrage wird zur Initialisierung des fiskalischen Registrierungsdienstes verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei befindet sich im Ordner **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** des [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck der Datei besteht darin, die Konfiguration der Einstellungen für den Fiskalkonnektor von der Commerce-Zentrale aus zu ermöglichen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet. Die folgenden Einstellungen werden hinzugefügt:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Timeout** - Die Zeitspanne in Millisekunden, die der Konnektor auf eine Antwort des fiskalischen Registrierungsdienstes warten wird.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
