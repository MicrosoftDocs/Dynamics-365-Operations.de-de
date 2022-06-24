---
title: Integrationsbeispiel für Steuererfassungsdienst für die Tschechische Republik
description: In diesem Artikel erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für die Tschechische Republik in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: d255b03242a4cb7a72cef1e8e6fab901ecf953e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910497"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Integrationsbeispiel für Steuererfassungsdienst für die Tschechische Republik

[!include[banner](../includes/banner.md)]

In diesem Artikel erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für die Tschechische Republik in Microsoft Dynamics 365 Commerce.

Um die lokalen steuerlichen Anforderungen für Kassen in der Tschechische Republik zu erfüllen, umfassen die Microsoft Dynamics 365 Commerce-Funktionen für die Tschechische Republik eine Beispielintegration der Verkaufsstelle (POS) in einen externen Steuerregistrierungsservice. Das Beispiel erweitert die [steuerliche Integrationsfunktionen](fiscal-integration-for-retail-channel.md). Es basiert auf der [EFR (Electronisches Fiskalregister)](https://efsta.org/sicherheitsloesungen/)-Lösung von [EFSTA](https://efsta.org/) und ermöglicht die Kommunikation mit dem EFR-Service über das HTTPS-Protokoll. Der EFR-Dienst gewährleistet die elektronische Registrierung von Verkäufen (EET – Elektronická Evidence tržeb), dh die Online-Übertragung der Verkaufsdaten an einen steuerlichen Webservice der Finanzbehörden.

Der EFR-Dienst sollte entweder in der Commerce Hardware-Station oder auf einem separaten Computer gehostet werden, zu dem von der Hardare-Station aus eine Verbindung hergestellt werden kann. Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Retail Software Development Kit (SDK).

Microsoft gibt keine Hardware, Software oder Dokumentation von EFSTA aus frei. Um Informationen darüber zu erhalten, wie Sie die EFR-Lösung beziehen und betreiben, wenden Sie sich an [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Szenarien

Die folgenden Szenarien werden im Beispiel für die Integration des Steuerregistrierungsservice für die Tschechische Republik abgedeckt:

- Registrierung der Bargeldbuchungen im Steuererfassungsdienst.

    - Senden Sie detaillierte Buchungsdaten zum Steuererfassungsdienst. Diese Daten beinhalten Informationen zu Verkaufspositionen sowie Informationen über Rabatte, Zahlungen und Steuern. Der Steuerregistrierungsdienst sendet die Daten außerdem an den Webdienst der Steuerbehörden und erhält von diesem eine Bestätigung, die den Steueridentifikationscode der Transaktion enthält.
    - Erfassen Sie eine Antwort vom Steuererfassungsdienst. Diese Antwort enthält Steuerdaten wie den Steueridentifikationscode und den Sicherheitscode der Transaktion usw.
    - Drucken Sie die Steuerdaten für eine erfasste Buchung auf den Beleg.

- Die Erfassung von Geschenkkartenvorgängen und Debitoreneinzahlungen als Sachbuchungen im Steuererfassungsdienst.

    - Stellen Sie eine Geschenkkarte aus oder laden Sie sie mit Geld auf.
    - Erfassen Sie eine Debitorenkonto-Einzahlung.
    - Erstellen Sie eine Kundenbestellung und registrieren Sie eine Anzahlung für die Bestellung.
    - Bearbeiten Sie eine Kundenbestellung und überschreiben Sie eine Anzahlung für die Bestellung.
    - Brechen Sie eine Kundenbestellung ab und machen Sie eine Rückerstattung für die Bestellung.

- Fehlerbehebung, wie beispielsweise die folgenden Optionen.

    - Versuchen Sie die Steuererfassung erneut, falls ein Neuversuch möglich ist, wie z. B. wenn der Steuererfassungsdienst nicht verfügbar ist, nicht bereit ist oder nicht reagiert.
    - Verschieben Sie die Steuererfassung.
    - Überspringen Sie Steuererfassung, oder markieren Sie die Buchung als erfasst, und schließen Sie Infocodes ein, um den Grund für den Fehler und zusätzliche Informationen zu erfassen.
    - Überprüfen Sie die Verfügbarkeit des Steuererfassungsdiensts, bevor eine neue Verkaufsbuchung geöffnet wird oder eine Verkaufsbuchung abgeschlossen wird.

### <a name="gift-cards"></a>Geschenkkarten

Das Steuererfassungsdienst-Integrationsbeispiel implementiert die folgenden Regeln bezüglich Geschenkkarten.

- Vertriebslinien, die sich auf *Geschenkkarte ausstellen* oder *Zur Geschenkkarte hinzufügen* Vorgänge in einer Verkaufstransaktion beziehen, werden mit einem speziellen Attribut gekennzeichnet, wenn die Transaktion im Steuerregistrierungsdienst registriert wird.
- Eine Zahlung per Geschenkkarte gilt als regelmäßige Zahlung und wird bei der Registrierung der Transaktion im Steuerregistrierungsdienst mit einem besonderen Attribut gekennzeichnet.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Debitoreneinlagen und Debitorenauftragseinlagen

Das Integrationsbeispiel des Steuererfassungsdiensts implementiert die folgenden Regeln in Bezug auf Debitorenkonten und Debitorenauftragseinzahlungen.

- Eine Transaktion, die sich auf eine Kundenkontoeinlage oder eine Kundenauftragseinlage bezieht, wird im Steuerregistrierungsservice als einzeilige Transaktion registriert und mit einem speziellen Attribut gekennzeichnet. In dieser Zeile wird die Mehrwertsteuergruppe in dieser Position angegeben.
- Beim Anlegen einer hybriden Kundenbestellung, d. h. einer Kundenbestellung, die Produkte enthält, die vom Kunden aus dem Geschäft ausgeführt werden können, sowie Produkte, die später abgeholt oder versendet werden, wird die Transaktion im Steuerregistrierungsservice registriert enthält Zeilen für die ausgeführten Produkte sowie eine Zeile für die Auftragseinzahlung.
- Eine Zahlung von einem Kundenkonto gilt als regelmäßige Zahlung und wird bei der Registrierung der Transaktion im Steuerregistrierungsdienst mit einem besonderen Attribut gekennzeichnet.
- Der Anzahlungsbetrag für eine Kundenbestellung, der auf einen Vorgang zur Abholung einer Kundenbestellung angewendet wird, wird als reguläre Zahlung betrachtet und mit einem speziellen Attribut gekennzeichnet, wenn die Transaktion im Fiskalregistrierungsdienst registriert wird.

### <a name="offline-registration"></a>Offline-Registrierung

Wenn der steuerrechtliche Registrierungsdienst keine Transaktionsdaten an den steuerrechtlichen Webdienst der Finanzbehörden übermittelt z. B. es eine lokale Signatur für die Transaktion generiert und diese sowie einen speziellen Fehlercode in die Antwort einfügt. Der Steuerregistrierungsdienst sendet Transaktionen in der ursprünglichen Reihenfolge im Hintergrund erneut, sobald die Netzwerkverbindung wiederhergestellt ist.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

Der Steuererfassungsdienst unterstützt nur Szenarien, bei denen die Mehrwertsteuer im Preis enthalten ist. Daher muss die Option **Preis in Mehrwertsteuer enthalten** auf **Ja** sowohl für Geschäfte als auch Debitoren festgelegt werden.

## <a name="set-up-commerce-for-the-czech-republic"></a>Lokalisierung von Commerce für die Tschechische Repulik einrichten

In diesem Abschnitt werden die Commerce-Einstellungen beschrieben, die für die Tschechische Repulik spezifisch und empfohlen sind. Weitere Informationen für das Einrichten finden Sie unter der [Commerce-Homepage](../index.md).

Um die für die Tschechische Repulik spezifischen Funktionen zu verwenden, müssen Sie die folgenden Einstellungen angeben.

- Legen Sie in der primären Adresse der juristischen Person das Feld **Land/Region** auf **CZE** (Tschechische Repulik) fest.
- Legen Sie im POS-Funktionsprofil jedes einzelnen Einzelhandelsgeschäfts in der Tschechische Repulik das Feld **ISO-Code** auf **CZ** (Tschechische Repulik) fest.

Sie müssen auch die folgenden Einstellungen für die Tschechische Repulik angeben. Beachten Sie, dass Sie entsprechende Verteilungseinzelvorgänge ausführen müssen, nachdem Sie die Einrichtung abschließen.

### <a name="set-up-vat-per-czech-republic-requirements"></a>MwSt. nach tschechischen Anforderungen einrichten


Sie müssen Mehrwertsteuercodes, Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen erstellen. Sie müssen auch Mehrwertsteuerinformationen für Produkte und Dienstleistungen einrichten. Weitere Informationen dazu, wie die Mehrwertsteuer in eingerichtet und verwendet wird, finden Sie unter [Mehrwertsteuerüberblick](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Shops einrichten

Aktualisieren Sie auf der Seite **Alle Geschäfte** die Details der Geschäfte. Legen Sie genauer die folgenden Parameter fest.

- Geben Sie im Feld **Mehrwertsteuergruppe** die Mehrwertsteuergruppe an, die für Verkäufe an den Standarddebitoren verwendet werden soll.
- Legen Sie die Option **Preis enthält Mehrwertsteuersatz** auf **Ja** fest.
- Legen Sie das Feld **Name** auf den Unternehmensnamen fest. Durch diese Änderung wird sichergestellt, dass der Unternehmensname auf dem Verkaufsbeleg erscheint. Alternativ können Sie den Unternehmensnamen im Verkaufsbeleglayout als Freiformtext hinzufügen.
- Legen Sie das Feld **Steuernummer (TIN)** auf die Unternehmenskennnummer fest. Durch diese Änderung wird sichergestellt, dass die Identifikationsnummer auf dem Verkaufsbeleg erscheint. Alternativ können Sie Unternehmenskennnummer dem Verkaufsbeleglayout als Freiformtext hinzufügen.

### <a name="set-up-functionality-profiles"></a>Einrichten von Funktionsprofilen

POS-Funktionsprofile einrichten.

- Richten Sie im Inforegister **Belegnummerierung** die Belegnummerierung ein, indem Sie Datensätzen für die Belegbuchungstypen **Verkauf**, **Auftrag** und **Retoure** erstellen oder aktualisieren.

### <a name="set-up-registration-numbers"></a>Legen Sie die Registierungsnummern fest

1. Navigieren Sie zu **Organisationsverwaltung \> Globales Adressbuch \> Erfassungstypen \> Erfassungstypen.**. Einen neuen Registrierungstyp erstellen. Präzisieren Sie das **Land/Region** Feld zu **CZE** (Tschechische Republik) und beschränken Sie es auf die Organisation.
2. Navigieren zur **Organisationsverwaltung \> Globales Adressbuch \> Registrierungstypen \> Registrierungskategorien**. Wählen Sie eine neue Registrierungskategorie aus. Wählen Sie den Registrierungstyp aus dem Schritt aus, den Sie zuvor erstellt haben, und wählen Sie anschließend im Feld **Registrierungskategorie** die **Geschäftsraumkennungs-ID** aus.
3. Rufen Sie **Organisationsverwaltung \> Organisationen \> Organisationseinheiten** auf. Wählen Sie für jedes Geschäft in der Tschechischen Republik die Einheit aus, die sich auf das Geschäft bezieht. Wählen Sie im Inforegister **Adressen** **Weitere Optionen** und anschließend in der Dropdownliste **Erweitert** aus. 
4. Auf der geöffneten Seite **Adressen verwalten** müssen Sie folgende Einstellung angeben.

    - Auf dem Inforegister **Adresse** legen Sie das Feld **Land/Region** auf **CZE** fest.
    - Im Inforegister **Registrierungs-ID** erstellen Sie einen neuen Datensatz. Wählen Sie den Registrierungstyp, den Sie zuvor erstellt haben udn legen sie die Registrierungsnummer fest.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurieren Sie benutzerdefinierte Felder, damit sie in Belegformate für Verkaufsbelege verwendet werden können

Sie können den Sprachtext und die benutzerdefinierten Felder konfigurieren, die in den POS-Belegformaten verwendet werden. Das Standardunternehmen des Benutzers, der die Boneinrichtung erstellt, sollte die gleiche juristische Person sein, in dem die Sprachtexteinstellung erstellt wird. Alternativ sollten dieselben Sprachtexte im Standardunternehmen des Benutzers und in der juristischen Person des Shops verwendet werden, für den das Setup erstellt wird.

Fügen Sie auf der Seite **Sprachentext** die folgenden Datensätze für die Beschriftungen der benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass **Sprachen-ID**, **Text-ID** und **Text**-Werte, die in der Tabelle angezeigt werden, nur Beispiele sind. Sie können sie ändern, damit sie Ihre Anforderungen erfüllen. Allerdings müssen die **Text-ID**-Werte, die Sie verwenden, eindeutig sein und gleich oder größer als 900001 sein.

Fügen Sie dem Abschnitt **POS** des **Sprachentext** aus der Tabelle die folgenden POS-Beschriftungen hinzu:

| Sprachkennung | Textkennung | Text                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Info                   |
| en-US       | 900006  | Laufende Nummer        |

Fügen Sie auf der Seite **Benutzerdefinierte Felder** die folgenden Datensätze für die benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass die Werte für **Textkennung Titel** den Werten **Textkennung** entsprechen müssen, die Sie auf der Seite **Sprachentext** angegeben haben:

| Name                 | Typ    | Textkennung Titel |
|----------------------|---------|-----------------|
| TLT                  | Zugang | 900001          |
| SEC                  | Zugang | 900002          |
| VORZEICHEN                 | Zugang | 900003          |
| STEUERLICH               | Zugang | 900004          |
| INFO                 | Zugang | 900005          |
| CONTINUOUSNUMBER     | Zugang | 900006          |

> [!NOTE]
> Es ist wichtig, dass Sie die richtigen benutzerdefinierten Feldnamen angeben, wie in der vorherigen Tabelle aufgeführt. Ein falscher benutzerdefinierter Feldname führt zu fehlenden Daten in Belegen.

### <a name="configure-receipt-formats"></a>Bonformate konfigurieren

Ändern Sie für jedes erforderliche Belegformat den Wert des Felds **Druckverhalten** auf **Immer drucken**.

In Designer für Bonformat fügen Sie die folgenden benutzerdefinierten Felder den entsprechenden Bonabschnitten hinzu. Beachten Sie, dass die Feldnamen den Sprachtexten entsprechen, die Sie im vorherigen Abschnitt definiert haben.

- **Kopfzeile:** Fügen Sie die folgenden Felder hinzu.

    - **Storename** und **Steueridentifikationsnummer**: Diese Felder werden zum Drucken des Unternehmensnamens und der Identitätsnummer auf Belegen verwendet werden. Alternativ können Sie den Unternehmensnamen und die Identitätsnummer im Layout als Freiformtext hinzufügen.
    - **Storeadresse**, **Datum**, **Zeit 24 h**, **Bonnummer** und **Registernummer**.
    - **Sequenznumemr**: Dieses Feld identifiziziert die Nummer der Bargeldbuchungen im Steuererfassungsdienst.

- **Positionen:** Fügen Sie die folgenden Felder hinzu.

    - **Artikelname**
    - **Mge**
    - **Gesamtpreis mit Steuer**

- **Fußzeile:** Fügen Sie die folgenden Felder hinzu.

    - Ändern Sie die Zahlungsfelder, damit die Zahlungsbeträge für jede Zahlungsmethode gedruckt werden. Beispiel: Fügen Sie die Felder **Name des Zahlungsmittels** und **Betrag des Zahlungsmittels** einer Position des Layouts hinzu.
    - **ID provozovny/pokladny**: In diesem Feld werden die Kennungen der Geschäftsräume und der Registrierkasse gedruckt.
    - **BKP**: In diesem Feld wird der Sicherheitscode des Steuerzahlers gedruckt, der vom Steuerregistrierungsdienst zugewiesen wird.
    - **FIK**: Dieses Feld druckt den Steueridentifikationscode der Transaktion, der im Falle einer erfolgreichen Online-Registrierung vom Web-Service der Steuerbehörden zugewiesen wird.
    - **PKP**: Dieses Feld druckt den Signaturcode des Steuerzahlers, der im Falle einer Offline-Registrierung vom Steuerregistrierungsdienst generiert wird.
    - **Info**: In diesem Feld werden die zusätzlichen Informationen des Steuerregistrierungsdienstes gedruckt.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Einrichten und Entwerfen von Bonformaten](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Steuerintegration für die Tschechische Repulik einrichten

Die Beispiele für diese steuerliche Integration für die Tschechische Repulik basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil der Retail SDK. Die Probe befindet sich im Ordner **src\\Fiscallntegration\\Efr** des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [die Stichprobe in Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung der Commerce Runtime (CRT) ist, und einem fiskalischen Konnektor, der eine Erweiterung der Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die vorherige Version des Retail SDK auf einer virtuellen Maschine (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für die Tschechische Repulik (Legacy)](emea-cze-fi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

Schließen Sie die Schritte zur Einrichtung der steuerlichen Integration ab, wie unter [Einrichtung der steuerlichen Integration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) beschrieben:

1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Beachten Sie auch die Einstellungen für den Steuererfassungsprozess, die [für dieses Steuererfassungsdienst-Integrationsbeispiel spezifisch sind](#set-up-the-registration-process).
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurieren Sie die Channel-Komponenten](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Registrierungsprozess zu aktivieren, folgen Sie diesen Schritten, um die Commerce-Zentrale festzulegen. Weitere Informationen finden Sie unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Wählen Sie eine korrekte Version des Release Branches entsprechend Ihrer SDK-/Anwendungsversion (zum Beispiel **[Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Öffnen Sie **src \> FiscalIntegration \> Efr**.
    1. Laden Sie die Konfigurationsdatei des Fiskaldokumentanbieters herunter unter **Konfigurationen \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** (zum Beispiel [die Datei für die Freigabe/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Laden Sie die Konnektor-Konfigurationsdatei des Fiskaldokumentanbieters herunter unter **Konfigurationen \> Konnektoren \> KonnektorEFRSample.xm.** (zum Beispiel, [die Datei für die Freigabe/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Die Konfigurationsdateien für dieses Beispiel zur Fiskalintegration befinden sich in den folgenden Ordnern des Retail SDK auf einer Entwickler-VM in LCS:
    >
    > - **Steuerdokument-Konfigurationsdatei-Anbieter:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Konfiguration\\DocumentProviderFiscalEFRSampleGermany.xml
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

- **Zuordnung der Mehrwertsteuersätze (MwSt)** – Die Zuordnung von Steuerprozentsatzwerten, die für die Umsatzsteuerkennzeichen eingerichtet wurden, zu Werten der **TaxG** Attribute (Steuergruppe) in Anforderungen, die an den Finanzdienst gesendet werden. Hier ist die Standardzuordnung:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Die erste Komponente in jedem Paar stellt die entsprechende MwSt-Zahlungsgruppe dar, die vom EFR-Steuerregistrierungsdienst unterstützt wird. Die zweite Komponente stellt den entsprechenden Mehrwertsteuersatz dar. Weitere Informationen zu MwSt-Steuergruppen, die EFR für die Tschechische Republik unterstützt, finden Sie unter [EFR-Referenz](https://public.efsta.net/efr/).

- **Standardmäßige Mehrwertsteuergruppenzuordnung** – Alle MwSt.-Beträge, die keiner der vordefinierten MwSt.-Gruppen zugeordnet werden können, werden der standardmäßigen (einfachen) MwSt.-Gruppe zugeordnet. Hier ist die Standardzuordnung:

    ```
    A
    ```

- **Zuordnung der Mehrwertsteuergruppe für Kautionen** – Kundeneinzahlungsbeträge und Kundeneinzahlungsbeträge werden der Einzahlungs-Mehrwertsteuergruppe zugeordnet. Hier ist die Standardzuordnung:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Konnektor-Einstellungen für Steuern

Die folgenden Einstellungen sind in der Konfiguration des Fiskalkonnektors enthalten, die als Teil des Beispiels für die Fiskalintegration bereitgestellt wird:

- **Endpunktadresse** – Die URL des Steuererfassungsdiensts.
- **Zeitlimit** – Die Zeitdauer in Millisekunden (ms), die der Steuerkonnetor auf eine Antwort vom Steuererfassungsdienst wartet.

### <a name="configure-channel-components"></a>Kanal-Komponenten konfigurieren

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für die Tschechische Repulik (Legacy)](emea-cze-fi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

#### <a name="set-up-the-development-environment"></a>Die Umgebung für die Entwicklung festlegen

Um eine Entwicklungsumgebung zum Testen und Erweitern des Beispiels festzulegen, gehen Sie wie folgt vor.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Retail SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
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
        1. Starten Sie das Installationsprogramm für die Erweiterung von der Befehlszeile aus, indem Sie den folgenden Befehl ausführen.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **EFR Build-pipeline.yml** Vorlagen-YAML-Datei finden Sie im **Pipeline\\YAML_Files** Ordner des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Die Beispiele für diese steuerliche Integration für die Tschechische Repulik basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil der Retail SDK. Die Probe befindet sich im Ordner **src\\Fiscallntegration\\Efr** des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [die Stichprobe in Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung von CRT ist, und einem fiskalischen Konnektor, der eine Erweiterung von Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für das Steuererfassungsdienst-Integrationsbeispiel für die Tschechische Repulik (Legacy)](emea-cze-fi-sample-sdk.md). Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter dienstspezifische Dokumente erzeugt und Antworten aus dem Steuererfassungsdienst handhabt.

#### <a name="request-handler"></a>Anforderungshandler

Es gibt einen einzelnen **DocumentProviderEFRFiscalCZE** Anfrage-Handler für Dokumentanbieter, der verwendet wird, um Steuerdokumente für den Steuerregistrierungsdienst zu generieren.

Dieser Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen.

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein dienstspezifisches Dokument zurück, dass im Steuererfassungsdienst erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden folgende Ereignisse unterstützt: Verkäufe, Kundenkontoeinlagen und Kundenauftragseinlagen.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Diese Anforderung gibt die Antwort vom Steuererfassungsdienst zurück. Diese Antwort wird serialisiert, um eine Zeichenfolge zu bilden, sodass sie bereit zum Speichern ist.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Steuerdokumenten befindet sich unter **src\\FiscalIntegration\\Efr\\Konfigurationen\\Dokumentenanbieter\\DocumentProviderFiscalEFRSampleCzech.xml** in dem [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Mit dieser Datei können Sie die Einstellungen des Anbieters von Fiskalbelegen von der Commerce-Zentrale aus festlegen. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuererfassungsdienst. Die Hardwarestation-Erweiterung verwendet das HTTP-Protokoll, um Dokumente, die die CRT-Erweiterung generiert, zum Steuererfassungsdienst zu übermitteln. Sie handhabt auch die Antworten, die vom Steuererfassungsdienst empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EFRHandler** ist der Einstiegspunkt für die Handhabung von Anforderungen an den Steuererfassungsdienst.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen.

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
